---
title: "FTP Deny URL Sequences &lt;denyUrlSequences&gt;"
author: rick-anderson
description: "Overview The &lt;denyUrlSequences&gt; element contains a collection of &lt;add&gt; elements that specify sequences of characters that IIS will deny, which he..."
ms.date: 09/26/2016
ms.assetid: 22fabbf8-ac3f-4d51-b5e3-d4bf777ff1f1
msc.legacyurl: /configreference/system.ftpserver/security/requestfiltering/denyurlsequences
msc.type: config
---
# FTP Deny URL Sequences &lt;denyUrlSequences&gt;

<a id="001"></a>
## Overview

The `<denyUrlSequences>` element contains a collection of `<add>` elements that specify sequences of characters that IIS will deny, which helps prevent URL-based attacks on the Web server.

> [!NOTE]
> When request filtering blocks an FTP request because of a denied URL sequence, FTP 7 will return an FTP error to the client and log the following FTP substatus that identifies the reason that the request was denied:

| FTP Substatus | Description |
| --- | --- |
| `9` | Denied URL sequence detected in the requested path. |

This substatus allows Web administrators to analyze their IIS logs and identify potential threats.

<a id="002"></a>
## Compatibility

| Version | Notes |
| --- | --- |
| IIS 10.0 | The `<denyUrlSequences>` element was not modified in IIS 10.0. |
| IIS 8.5 | The `<denyUrlSequences>` element was not modified in IIS 8.5. |
| IIS 8.0 | The `<denyUrlSequences>` element was not modified in IIS 8.0. |
| IIS 7.5 | The `<denyUrlSequences>` element of the `<requestFiltering>` element ships as a feature of IIS 7.5. |
| IIS 7.0 | The `<denyUrlSequences>` element of the `<requestFiltering>` element was introduced in FTP 7.0, which was a separate download for IIS 7.0. |
| IIS 6.0 | The FTP service in IIS 6.0 did not support request filtering. |

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
    [![Screenshot of the Server Roles page. Web Server I I S is expanded. F T P Server is expanded. F T P Extensibility is highlighted and selected.](index/_static/image2.png)](index/_static/image1.png) .
5. Click **Next**, and then on the **Select features** page, click **Next** again.
6. On the **Confirm installation selections** page, click **Install**.
7. On the **Results** page, click **Close**.

### Windows 8 or Windows 8.1

1. On the **Start** screen, move the pointer all the way to the lower left corner, right-click the **Start** button, and then click **Control Panel**.
2. In **Control Panel**, click **Programs and Features**, and then click **Turn Windows features on or off**.
3. Expand **Internet Information Services**, and then select **FTP Server**.   
  
    > [!NOTE]
    > To support ASP.Membership authentication or IIS Manager authentication for the FTP service, you will also need to select **FTP Extensibility**.   
    [![Screenshot of the Programs and Features navigation tree. F T P Extensibility is highlighted and selected.](index/_static/image4.png)](index/_static/image3.png)
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
    [![Screenshot of the Select Role Services page. F T P Server is expanded and F T P Service is highlighted and selected.](index/_static/image6.png)](index/_static/image5.png)
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
    [![Screenshot of the Programs and Features navigation tree. The Internet Information Services node is expanded and the F T P Server node is also expanded. F T P Service is selected.](index/_static/image8.png)](index/_static/image7.png)
5. Click **OK**.

### Windows Server 2008 or Windows Vista

1. Download the installation package from the following URL: 

    - [https://www.iis.net/expand/FTP](https://www.iis.net/downloads/microsoft/ftp)
2. Follow the instructions in the following walkthrough to install the FTP service: 

     - [Installing and Troubleshooting FTP 7](https://go.microsoft.com/fwlink/?LinkId=88547)
 
<a id="004"></a>
## How To

> [!NOTE]
> FTP Request Filtering did not have a user interface in the FTP 7.0 release; the FTP Request Filtering UI was added in the FTP 7.5 release.

### How to deny an FTP URL sequence

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
2. In the **Connections** pane, go to the site or directory for which you want to modify your request filtering settings.
3. In the **Home** pane, double-click **FTP Request Filtering**.  
    [![Screenshot of the contoso dot com home pane. The F T P Request icon is highlighted.](index/_static/image10.png)](index/_static/image9.png)
4. In the **FTP Request Filtering** pane, click the **Denied URL Sequences** tab.  
    [![Screenshot of the F T P Request Filtering pane. The Denied U R L Sequences tab is selected.](index/_static/image12.png)](index/_static/image11.png)
5. Click **Add URL Sequence...** in the **Actions** pane.
6. In the **Add Deny Sequence** dialog box, enter the URL sequence that you wish to block.  
    [![Screenshot of the Add Deny Sequence dialog box. The U R L sequence box is shown.](index/_static/image14.png)](index/_static/image13.png)
7. Click **OK**.

<a id="005"></a>
## Configuration

The `<denyUrlSequences>` element of the `<requestFiltering>` element is configured at the global, site or URL level.

### Attributes

None.

### Child Elements

| Element | Description |
| --- | --- |
| [`add`](add.md) | Optional element. <br><br>Adds a sequence to the collection of denied URL sequences. |
| `clear` | Optional element. <br><br>Removes all references to sequences from the `<denyUrlSequences>` collection. |
| `remove` | Optional element. <br><br>Removes a reference to a sequence from the `<denyUrlSequences>` collection. |

### Configuration Sample

The following sample illustrates several security-related configuration settings in the `<system.ftpServer>` element for an FTP site. More specifically, the `<location>` settings in this example demonstrate how to:

- Specify an FTP authorization rule for read and write access for the administrators group.
- Specify FTP request filtering options that deny \*.exe, \*.bat, and \*.cmd files.
- Specify FTP request limits for a maximum content length of 1000000 bytes and a maximum URL length of 1024 bytes.
- Block FTP access to the \_vti\_bin virtual directory, which is used with the FrontPage Server Extensions.
- Specify FTP IP filtering options that allow access from 127.0.0.1 and deny access from the 169.254.0.0/255.255.0.0 range of IP addresses.

[!code-xml[Main](index/samples/sample1.xml)]

<a id="006"></a>
## Sample Code

The following examples will deny the URL sequence "bin" for FTP, which will prevent access to the "bin", "\_vti\_bin", or "cgi-bin" paths, and also prevent uploading files with a file name extension of ".bin."

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
