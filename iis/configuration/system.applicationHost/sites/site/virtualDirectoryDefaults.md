---
title: "Virtual Directory Defaults for a Site &lt;virtualDirectoryDefaults&gt;"
author: rick-anderson
description: "Overview The &lt;virtualDirectoryDefaults&gt; element of the &lt;site&gt; element specifies the default settings for all virtual directories in the parent si..."
ms.date: 09/26/2016
ms.assetid: 2faecab1-fdc5-4a77-b49b-e0e2512c1b9b
msc.legacyurl: /configreference/system.applicationhost/sites/site/virtualdirectorydefaults
msc.type: config
---
# Virtual Directory Defaults for a Site &lt;virtualDirectoryDefaults&gt;

<a id="001"></a>
## Overview

The `<virtualDirectoryDefaults>` element of the `<site>` element specifies the default settings for all virtual directories in the parent site. The `<virtualDirectoryDefaults>` element is useful for defining the common attributes that you want all virtual directories in the parent site to implicitly share when they do not have explicitly-defined attributes.

> [!NOTE]
> If the same attribute or child element is configured in both the `<virtualDirectoryDefaults>` section and in the `<virtualDirectory>` section for a specific virtual directory, the configuration in the `<virtualDirectory>` section is used for that virtual directory.

<a id="002"></a>
## Compatibility

| Version | Notes |
| --- | --- |
| IIS 10.0 | The `<virtualDirectoryDefaults>` element was not modified in IIS 10.0. |
| IIS 8.5 | The `<virtualDirectoryDefaults>` element was not modified in IIS 8.5. |
| IIS 8.0 | The `<virtualDirectoryDefaults>` element was not modified in IIS 8.0. |
| IIS 7.5 | The `<virtualDirectoryDefaults>` element was not modified in IIS 7.5. |
| IIS 7.0 | The `<virtualDirectoryDefaults>` element of the `<site>` element was introduced in IIS 7.0. |
| IIS 6.0 | N/A |

<a id="003"></a>
## Setup

The `<virtualDirectoryDefaults>` element of the `<site>` element is included in the default installation of IIS 7.

<a id="004"></a>
## How To

### How to configure the default virtual directory credentials for a site

1. Open **Internet Information Services (IIS) Manager**: 

    - If you are using Windows Server 2012 or Windows Server 2012 R2: 

        - On the taskbar, click **Server Manager**, click **Tools**, and then click **Internet Information Services (IIS) Manager**.
    - If you are using Windows 8 or Windows 8.1: 

        - Hold down the **Windows** key, press the letter **X**, and then click **Control Panel**.
        - Click **Administrative Tools**, and then double-click **Internet Information Services (IIS) Manager**.
    - If you are using Windows Server 2008 or Windows Server 2008 R2: 

        - On the taskbar, click **Start**, point to **Administrative Tools**, and then click **Internet Information Services (IIS) Manager**.
    - If you are using Windows Vista or Windows 7: 

        - On the taskbar, click **Start**, and then click **Control Panel**.
        - Double-click **Administrative Tools**, and then double-click **Internet Information Services (IIS) Manager**.
2. In the **Connections** pane, expand the server name, expand the **Sites** node, and then click the name of the site.
3. In the site's **Home** pane, click **View Applications** in the **Actions** pane.  
    [![Screenshot that shows the Default Web Site Home pane.](virtualDirectoryDefaults/_static/image2.png)](virtualDirectoryDefaults/_static/image1.png)
4. In the site's **Application** pane, click **Set Application Defaults...** in the **Actions** pane.  
    [![Screenshot that shows the Applications pane. Add Application is hightlighted in the Actions pane.](virtualDirectoryDefaults/_static/image4.png)](virtualDirectoryDefaults/_static/image3.png)
5. In the **Application Defaults** dialog box, specify your default virtual directory credentials for the site, and then click **OK**.  
    [![Screenshot that shows the Application Defaults dialog box.](virtualDirectoryDefaults/_static/image6.png)](virtualDirectoryDefaults/_static/image5.png)

<a id="005"></a>
## Configuration

### Attributes

| Attribute | Description |
| --- | --- |
| `allowSubDirConfig` | Optional Boolean attribute.<br><br>Specifies whether IIS looks for Web.config files in content directories lower in the directory hierarchy than the current level (**true**) or does not look for Web.config files in content directories lower than the current level (**false**).<br><br>The default value is `true`. |
| `logonMethod` | Optional enum attribute.<br><br>Specifies the default logon method for all virtual directories in applications in the parent site.<br><br>The **logonMethod** attribute can be one of the following possible values. The default is `ClearText`. <table> <tbody> <tr> <th>Value</th> <th>Description</th></tr> <tr> <th><code>Batch</code></th> <td>This logon type is intended for batch servers, where processes may be executing on behalf of a user without that user's direct intervention. <p>The numeric value is <code>1</code>.</p></td></tr> <tr> <th><code>ClearText</code></th> <td>This logon type preserves the name and password in the authentication package, which allows the server to make connections to other network servers while impersonating the client. <p>The numeric value is <code>3</code>.</p></td></tr> <tr> <th><code>Interactive</code></th> <td>This logon type is intended for users who will be using the computer interactively. <p>The numeric value is <code>0</code>.</p></td></tr> <tr> <th><code>Network</code></th> <td>This logon type is intended for high performance servers that authenticate plaintext passwords. Credentials are not cached for this logon type. <p>The numeric value is <code>2</code>.</p></td></tr></tbody></table> For more information about these values, see [LogonUser](/windows/win32/api/winbase/nf-winbase-logonusera)
. |
| `password` | Optional string attribute.<br><br>Specifies the password associated with the user name.<br><br>**Note:** To avoid storing unencrypted password strings in configuration files, always use AppCmd.exe or IIS Manager to enter passwords. If you use these management tools, the password strings will be encrypted automatically before they are written to the XML configuration files. This provides better password security than storing unencrypted passwords. |
| `path` | Optional string attribute.<br><br>Specifies the default virtual path of all virtual directories in applications in the parent site. |
| `physicalPath` | Optional string attribute.<br><br>Specifies the default physical path of all virtual directories in applications in the parent site. |
| `userName` | Optional string attribute.<br><br>Specifies the default user name of an account that can access configuration files and content for all virtual directories in applications in the parent site. |

### Child Elements

None.

### Configuration Sample

The following configuration sample specifies the default logon method for virtual directories in the Default Web Site.

[!code-xml[Main](virtualDirectoryDefaults/samples/sample1.xml)]

<a id="006"></a>
## Sample Code

The following code samples specify the default logon method for virtual directories in the Default Web Site.

### AppCmd.exe

[!code-console[Main](virtualDirectoryDefaults/samples/sample2.cmd)]

> [!NOTE]
> You must be sure to set the **commit** parameter to `apphost` when you use AppCmd.exe to configure these settings. This commits the configuration settings to the appropriate location section in the ApplicationHost.config file.

### C\#

[!code-csharp[Main](virtualDirectoryDefaults/samples/sample3.cs)]

### VB.NET

[!code-vb[Main](virtualDirectoryDefaults/samples/sample4.vb)]

### JavaScript

[!code-javascript[Main](virtualDirectoryDefaults/samples/sample5.js)]

### VBScript

[!code-vb[Main](virtualDirectoryDefaults/samples/sample6.vb)]
