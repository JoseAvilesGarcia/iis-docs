---
title: IIS 10.0 Version 1709 HTTP Strict Transport Security (HSTS) Support
author: bangbingsyb
description: Describes how to enable HSTS and HTTP to HTTPS redirection at the site level in IIS 10.0 version 1709.
ms.author: yashi
ms.date: 10/24/2017
msc.type: authoredcontent
---
# IIS 10.0 Version 1709 HTTP Strict Transport Security (HSTS) Support

by [Yanbing Shi](https://github.com/bangbingsyb)

> In IIS 10.0 version 1709, the administrator has the option of enabling HSTS and HTTP to HTTPS redirection at site level.

## Compatibility

| Version | Notes |
| --- | --- |
| IIS 10.0 version 1709 | The features described in this article were introduced in IIS 10.0 version 1709 |
| IIS 10.0 and earlier | The features described in this article were not supported prior to IIS 10.0 version 1709 |

## HTTP Strict Transport Security (HSTS)

HTTP Strict Transport Security (HSTS), specified in [RFC 6797](https://tools.ietf.org/html/rfc6797), allows a website to declare itself as a secure host and to inform browsers that it should be contacted only through HTTPS connections. HSTS is an opt-in security enhancement that enforces HTTPS and significantly reduces the ability of man-in-the-middle type attacks to intercept requests and responses between servers and clients.

HSTS enforces the use of HTTPS through a policy that requires support from both web servers and browsers. An HSTS enabled web host can include a special HTTP response header "Strict-Transport-Security" (STS) along with a "max-age" directive in an HTTPS response to request the browser to use HTTPS for further communication. The browser receives the header, and memorizes the HSTS policy for the number of seconds specified by the “max-age” directive. Within this period, if an user tries to visit the same website but types http:// or omits the scheme at all, the browser will automatically turn the insecure link to the secure one (https://) and make an HTTPS connection to the server. Once a response is received through HTTPS, the browser also prevents the user from “clicking through” any security warning (e.g. a warning about an invalid server certificate). In order to take advantage of HSTS, the browser has to see the HSTS header at least once. To protect the user in the first connection to a given domain, HSTS has a separate mechanism to preload a list of registered domains to the browser out of the box.

## Challenges on Enabling HSTS before IIS 10.0 Version 1709

Before IIS 10.0 version 1709, enabling HSTS on an IIS server requires complex configuration.

Two solutions for enabling HSTS prior to IIS 10.0 version 1709 are provided for an example scenario: the web administrator wants to enable HSTS for a domain contoso.com that accepts both HTTP and HTTPS connections and to redirect all HTTP traffic to HTTPS. The redirection in this scenario is insecure by nature, but it is still a pattern followed by many websites that support HTTPS. The fundamental reason for still listening HTTP is that the website has no control over how visitors may try to connect it - over HTTPS or just plain HTTP. Enabling HSTS greatly reduces the number of insecure HTTP to HTTPS redirections under the condition that the browser sees the STS header during the first successful HTTPS connection (either through direct visit or through redirection).

### Solution 1: HTTP Redirect Module + Custom Headers

Redirecting all HTTP traffic to HTTPS can be achieved using the [HTTP Redirect Module](../../configuration/system.webserver/httpredirect/index.md) with two separate websites, one for HTTP and the other for HTTPS, to avoid an infinite redirect loop.

[!code-xml[Main](iis-10-version-1709-hsts/samples/sample-httpredirect-two-sites.xml)]

A redirection rule is configured in the web.config of the HTTP site to route all its traffic to the HTTPS site, and the later actually serves the contents.

[!code-xml[Main](iis-10-version-1709-hsts/samples/sample-httpredirect-http-site.xml)]

The STS header can be added through [Custom Headers](../../configuration/system.webServer/httpProtocol/customHeaders/index.md) by configuring the web.config of the HTTPS site.

[!code-xml[Main](iis-10-version-1709-hsts/samples/sample-httpredirect-https-site.xml)]

### Solution 2: URL Rewrite Module

An alternative solution is installing the [URL Rewrite Module](../../extensions/url-rewrite-module/using-the-url-rewrite-module.md) and configuring rewrite rules for a single website with both HTTP and HTTPS bindings. The HTTP to HTTPS redirection can be specified by an inbound rule while adding the STS header to HTTPS replies can be achieved by an outbound rule.

[!code-xml[Main](iis-10-version-1709-hsts/samples/sample-urlrewrite-single-site.xml)]

## IIS 10.0 Version 1709 Native HSTS Support

With the release of IIS 10.0 version 1709, HSTS is now supported natively. The configuration for enabling HSTS is significantly simplified - HSTS can be enabled at site-level by configuring the attributes of the `<hsts>` element under each `<site>` element - more details can be found in the configuration reference of HSTS [HSTS Settings for a Web Site \<HSTS>](../../configuration/system.applicationhost/sites/site/hsts.md).

The example scenario can be simply achieved by configuring the `enabled`, `max-age`, and `redirectHttpToHttps` attributes of the `<hsts>` element of the website using [IISAdministration PowerShell cmdlets](../whats-new-in-iis-10/iisadministration-powershell-cmdlets.md) following the [tutorial](https://blogs.iis.net/jeonghwan/how-to-use-iisadministration-powershell-cmdlets-to-configure-iis-configuration-settings).

[!code-powershell[Main](iis-10-version-1709-hsts/samples/sample-hsts-single-site.ps1)]

The HSTS configurations for the website are shown below:

[!code-xml[Main](iis-10-version-1709-hsts/samples/sample-hsts-single-site.xml)]

The native support of HSTS can also be used together with [HTTP Redirect Module](../../configuration/system.webserver/httpredirect/index.md) for more complex scenarios.

For example, a website contoso.com redirects all traffic to its subdomain `www.contoso.com`, and both websites accept HTTP and HTTPS connections. This is a typical scenario if the website is preferable to have a single canonical address. HSTS is recommended to be enabled for both the root domain and the subdomain because users may directly visit either one through HTTP or HTTPS. Enabling `includeSubDomains` attribute of the `<hsts>` element of the root domain further enhances the coverage of the HSTS policy to all its subdomains.

[!code-xml[Main](iis-10-version-1709-hsts/samples/sample-hsts-subdomain.xml)]

In addition, the redirection from the root domain to the subdomain can be configured through the `<httpRedirect>` element in the web.config of the root domain site. With such configuration, an HTTP request to contoso.com will first be redirected to HTTPS, and then the HTTPS request to the same site will be redirected to `www.contoso.com` with the STS header added in the response.

[!code-xml[Main](iis-10-version-1709-hsts/samples/sample-hsts-subdomain-redirect.xml)]

The sample configurations above also apply to the scenario of redirecting traffic from a source site to a destination site that is not a subdomain of the source site, with a minor configuration modification of disabling `includeSubDomains` for the source site.
