---
title: "FTP Custom Feature Providers &lt;providers&gt;"
author: rick-anderson
description: "Overview The &lt;providers&gt; element of the &lt;customFeatures&gt; element specifies a collection of FTP custom feature providers for an FTP site. Note : T..."
ms.date: 09/26/2016
ms.assetid: 0f26ff01-703d-4ff5-a351-7f69747036bc
msc.legacyurl: /configreference/system.applicationhost/sites/site/ftpserver/customfeatures/providers
msc.type: config
---
# FTP Custom Feature Providers &lt;providers&gt;

<a id="001"></a>
## Overview

The `<providers>` element of the `<customFeatures>` element specifies a collection of FTP custom feature providers for an FTP site.

> [!NOTE]
> The providers that are added to this collection can implement custom logging or home directory lookups; custom FTP providers that implement authentication and role lookups are added to the `<ftpServer/security/authentication/customAuthentication>` collection.

> [!NOTE]
> The custom features that are added to the `<customFeatures/providers>` element must be registered in the `<system.ftpServer/providerDefinitions>` collection.

> [!NOTE]
> Support for creating custom feature providers was introduced in FTP 7.5. For additional information about how to create FTP custom feature providers, see the [Developing for FTP 7.5](https://www.iis.net/learn/develop/developing-for-ftp) topic on Microsoft's IIS.net Web site.

<a id="002"></a>
## Compatibility

| Version | Notes |
| --- | --- |
| IIS 10.0 | The `<providers>` element was not modified in IIS 10.0. |
| IIS 8.5 | The `<providers>` element was not modified in IIS 8.5. |
| IIS 8.0 | The `<providers>` element was not modified in IIS 8.0. |
| IIS 7.5 | The `<providers>` element of the `<customFeatures>` element ships as a feature of IIS 7.5. |
| IIS 7.0 | The `<providers>` element of the `<customFeatures>` element was introduced in FTP 7.0, which was a separate download for IIS 7.0. |
| IIS 6.0 | The FTP service in IIS 6.0 did not support extensibility. |

> [!NOTE]
> The FTP 7.0 and FTP 7.5 services shipped out-of-band for IIS 7.0, which required downloading and installing the modules from the following URL:
> 
> [https://www.iis.net/expand/FTP](https://www.iis.net/downloads/microsoft/ftp)

With Windows 7 and Windows Server 2008 R2, the FTP 7.5 service ships as a feature for IIS 7.5, so downloading the FTP service is no longer necessary.

<a id="003"></a>
## Setup

To support FTP publishing for your Web server, you must install the FTP service. To do so, use the following steps.

### Windows Server 2012 or Windows Server 2012 R2

1. On the taskbar, click **Server Manager**.
2. In **Server Manager**, click the **Manage** menu, and then click **Add Roles and Features**.
3. In the **Add Roles and Features** wizard, click **Next**. Select the installation type and click **Next**. Select the destination server and click **Next**.
4. On the **Server Roles** page, expand **Web Server (IIS)**, and then select **FTP Server**.  
  
    > [!NOTE]
    > To support ASP.Membership authentication or IIS Manager authentication for the FTP service, you will need to select **FTP Extensibility**, in addition to **FTP Service**.  
    [![Screenshot of Web server I I S pane displaying F T P Server and F T P Services selected with F T P Extensibility highlighted.](index/_static/image2.png)](index/_static/image1.png) .
5. Click **Next**, and then on the **Select features** page, click **Next** again.
6. On the **Confirm installation selections** page, click **Install**.
7. On the **Results** page, click **Close**.

### Windows 8 or Windows 8.1

1. On the **Start** screen, move the pointer all the way to the lower left corner, right-click the **Start** button, and then click **Control Panel**.
2. In **Control Panel**, click **Programs and Features**, and then click **Turn Windows features on or off**.
3. Expand **Internet Information Services**, and then select **FTP Server**.   
  
    > [!NOTE]
    > To support ASP.Membership authentication or IIS Manager authentication for the FTP service, you will also need to select **FTP Extensibility**.   
    [![Screenshot of Internet Information Services and F T P Server pane expanded with FTP Extensibility selected.](index/_static/image4.png)](index/_static/image3.png)
4. Click **OK**.
5. Click **Close**.

### Windows Server 2008 R2

1. On the taskbar, click **Start**, point to **Administrative Tools**, and then click **Server Manager**.
2. In the **Server Manager** hierarchy pane, expand **Roles**, and then click **Web Server (IIS)**.
3. In the **Web Server (IIS)** pane, scroll to the **Role Services** section, and then click **Add Role Services**.
4. On the **Select Role Services** page of the **Add Role Services Wizard**, expand **FTP Server**.
5. Select **FTP Service**.  
  
    > [!NOTE]
    > To support ASP.Membership authentication or IIS Manager authentication for the FTP service, you will also need to select **FTP Extensibility**.  
    [![Screenshot of F T P Server expanded pane in Select Role Services page with F T P Services selected. ](index/_static/image6.png)](index/_static/image5.png)
6. Click **Next**.
7. On the **Confirm Installation Selections** page, click **Install**.
8. On the **Results** page, click **Close**.

### Windows 7

1. On the taskbar, click **Start**, and then click **Control Panel**.
2. In **Control Panel**, click **Programs and Features**, and then click **Turn Windows Features on or off**.
3. Expand **Internet Information Services**, and then **FTP Server**.
4. Select **FTP Service**.  
  
    > [!NOTE]
    > To support ASP.Membership authentication or IIS Manager authentication for the FTP service, you will also need to select **FTP Extensibility**.   
    [![Screenshot of Internet Information Services and FTP Server pane expanded with F T P Service and F T P Extensibility selected.](index/_static/image8.png)](index/_static/image7.png)
5. Click **OK**.

### Windows Server 2008 or Windows Vista

1. Download the installation package from the following URL: 

    - [https://www.iis.net/expand/FTP](https://www.iis.net/downloads/microsoft/ftp)
2. Follow the instructions in the following walkthrough to install the FTP service: 

     - [Installing and Troubleshooting FTP 7](https://go.microsoft.com/fwlink/?LinkId=88547)

<a id="004"></a>
## How To

At this time there is no user interface that enables you to add custom features to a site. See the **Configuration** and **Sample Code** sections of this document for additional information about how to add custom features to an FTP site.

<a id="005"></a>
## Configuration

The `<providers>` element is configured at the site level.

### Attributes

None.

### Child Elements

| Element | Description |
| --- | --- |
| [`add`](add.md) | Optional element.<br><br>Adds a feature provider to the collection of FTP custom providers for an FTP site. |
| `clear` | Optional element.<br><br>Clears the collection of FTP custom providers for an FTP site. |
| `remove` | Optional element.<br><br>Removes a feature provider from the collection of FTP custom providers for an FTP site. |

### Configuration Sample

The following sample displays a `<customFeatures>` element for an FTP site that adds a custom logging provider that is named "FtpLoggingDemo" to an FTP site.

[!code-xml[Main](index/samples/sample1.xml)]
 
<a id="006"></a>
## Sample Code

The following examples demonstrate how to add a custom logging provider for an FTP site.

> [!NOTE]
> FTP custom features must be registered in the [`<system.ftpServer/providerDefinitions>`](../../../../../../system.ftpserver/providerdefinitions/index.md) collection.

### AppCmd.exe

[!code-console[Main](index/samples/sample2.cmd)]

> [!NOTE]
> You must be sure to set the **commit** parameter to `apphost` when you use AppCmd.exe to configure these settings. This commits the configuration settings to the appropriate location section in the ApplicationHost.config file.

### C\#

[!code-csharp[Main](index/samples/sample3.cs)]

### VB.NET

[!code-vb[Main](index/samples/sample4.vb)]

### JavaScript

[!code-javascript[Main](index/samples/sample5.js)]

### VBScript

[!code-vb[Main](index/samples/sample6.vb)]
