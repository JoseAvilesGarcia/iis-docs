---
title: "Trace Areas &lt;traceAreas&gt;"
author: rick-anderson
description: "Overview The &lt;traceAreas&gt; collection can contain a collection of &lt;add&gt; elements. Each &lt;add&gt; element defines the trace provider to use for f..."
ms.date: 09/26/2016
ms.assetid: bfdccf34-4139-43a4-94d5-f69f4265c839
msc.legacyurl: /configreference/system.webserver/tracing/tracefailedrequests/add/traceareas
msc.type: config
---
# Trace Areas &lt;traceAreas&gt;

<a id="001"></a>
## Overview

The `<traceAreas>` collection can contain a collection of `<add>` elements. Each `<add>` element defines the trace provider to use for failed request tracing, the provider-specific areas to enable, and the verbosity level of events to include in the trace.

<a id="002"></a>
## Compatibility

| Version | Notes |
| --- | --- |
| IIS 10.0 | The `<traceAreas>` element was not modified in IIS 10.0. |
| IIS 8.5 | The `<traceAreas>` element was not modified in IIS 8.5. |
| IIS 8.0 | The `<traceAreas>` element was not modified in IIS 8.0. |
| IIS 7.5 | The `<traceAreas>` element was not modified in IIS 7.5. |
| IIS 7.0 | The `<traceAreas>` element was introduced in IIS 7.0. |
| IIS 6.0 | N/A |

<a id="003"></a>
## Setup

After you finish the default installation of IIS 7 and later, you must install the tracing role service to use failed request tracing. After you install the role service, you still must enable failed request tracing at the site level, application level, or directory level.

### Windows Server 2012 or Windows Server 2012 R2

1. On the taskbar, click **Server Manager**.
2. In **Server Manager**, click the **Manage** menu, and then click **Add Roles and Features**.
3. In the **Add Roles and Features** wizard, click **Next**. Select the installation type and click **Next**. Select the destination server and click **Next**.
4. On the **Server Roles** page, expand **Web Server (IIS)**, expand **Web Server**, expand **Health and Diagnostics**, and then select **Tracing**. Click **Next**.  
    [![Screenshot of Web Server and Health and Diagnostics pane expanded with Tracing selected.](index/_static/image2.png)](index/_static/image1.png) .
5. On the **Select features** page, click **Next**.
6. On the **Confirm installation selections** page, click **Install**.
7. On the **Results** page, click **Close**.

### Windows 8 or Windows 8.1

1. On the **Start** screen, move the pointer all the way to the lower left corner, right-click the **Start** button, and then click **Control Panel**.
2. In **Control Panel**, click **Programs and Features**, and then click **Turn Windows features on or off**.
3. Expand **Internet Information Services**, expand **World Wide Web Services**, expand **Health and Diagnostics**, and then select **Tracing**.  
    [![Screenshot of World Wide Web Services and Health and Diagnostics pane expanded with Tracing selected.](index/_static/image4.png)](index/_static/image3.png)- Click **OK**.
4. Click **Close**.

### Windows Server 2008 or Windows Server 2008 R2

1. On the taskbar, click **Start**, point to **Administrative Tools**, and then click **Server Manager**.
2. In the **Server Manager** hierarchy pane, expand **Roles**, and then click **Web Server (IIS)**.
3. In the **Web Server (IIS)** pane, scroll to the **Role Services** section, and then click **Add Role Services**.
4. On the **Select Role Services** page of the **Add Role Services Wizard**, select **Tracing**, and then click **Next**.  
    [![Screenshot of Health and Diagnostics pane expanded in Select Role Services page showing Tracing selected.](index/_static/image6.png)](index/_static/image5.png)
5. On the **Confirm Installation Selections** page, click **Install**.
6. On the **Results** page, click **Close**.

### Windows Vista or Windows 7

1. On the taskbar, click **Start**, and then click **Control Panel**.
2. In **Control Panel**, click **Programs and Features**, and then click **Turn Windows Features on or off**.
3. Expand **Internet Information Services**, then **World Wide Web Services**, then **Health and Diagnostics**.
4. Select **Tracing**, and then click **OK**.  
    [![Screenshot of Internet Information Services and Health and Diagnostics pane expanded with Tracing highlighted.](index/_static/image8.png)](index/_static/image7.png)
 
<a id="004"></a>
## How To

### How to enable tracing

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
2. In the **Connections** pane, select the server connection, site, application, or directory for which you want to configure failed request tracing.
3. In the **Actions** pane, click **Failed Request Tracing...**  
    [![Screenshot of Default Web Site Home pane showing Failed Request Tracing selected in the Actions pane.](index/_static/image10.png)](index/_static/image9.png)
4. In the **Edit Web Site Failed Request Tracing Settings** dialog box, select the **Enable** check box to enable tracing, leave the default value or type a new directory where you want to store failed request log files in the **Directory** box, type the number of failed request trace files you want to store in the **Maximum number of trace files** box, and then click **OK**.  
    [![Screenshot of Edit Web Site Failed Request Tracing Settings dialog box showing Enable box selected and command populating Directory box.](index/_static/image12.png)](index/_static/image11.png)

### How to configure failure definitions

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
2. In the **Connections** pane, go to the connection, site, application, or directory for which you want to configure failed request tracing.
3. In the **Home** pane, double-click **Failed Request Tracing Rules**.  
    [![Screenshot of Home pane showing Failed Request Tracing Rules selected.](index/_static/image14.png)](index/_static/image13.png)
4. In the **Actions** pane, click **Add...**
5. On the **Specify Content to Trace** page of the **Add Failed Request Tracing Rule** Wizard, select the content type you want to trace, and then click **Next**.  
    [![Screenshot of Specify Content to Trace page showing All content selected for content type option.](index/_static/image16.png)](index/_static/image15.png)
6. On the **Define Trace Conditions** page, select the conditions you want to trace, and then click **Next**. Trace conditions can include any combination of status codes, a time limit that a request should take, or the event severity. If you specify all conditions, the first condition that is met generates the failed request trace log file.  
    [![Screenshot of Define Trace Condition page with Status code box selected and populated with the code.](index/_static/image18.png)](index/_static/image17.png)
7. On the **Select Trace Providers** page, select one or more of the trace providers under **Providers**.  
    [![Screenshot of Select Trace Providers page displaying list of providers under Providers box.](index/_static/image20.png)](index/_static/image19.png)
8. On the **Select Trace Providers** page, select one or more of the verbosity levels under **Verbosity**.  
    [![Screenshot of Select Trace Providers page showing Warnings selected for the verbosity level under Verbosity menu.](index/_static/image22.png)](index/_static/image21.png)
9. If you selected the **ASPNET** or **WWW Server** trace provider in step 8, select one or more functional areas for the provider to trace under **Areas** of the **Select Trace Providers** page.
10. Click **Finish**.

<a id="005"></a>
## Configuration

### Attributes

None.

### Child Elements

| Element | Description |
| --- | --- |
| [`add`](add.md) | Optional element. <br><br>Adds a trace area to the collection of trace areas. |
| `clear` | Optional element. <br><br>Removes a reference to a trace area from the trace areas collection. |
| `remove` | Optional element. <br><br>Removes all references to trace areas from the trace areas collection. |

### Configuration Sample

The following configuration example configures tracing at the server level in the ApplicationHost.config file. It sets tracing for all .aspx files, uses the `<traceAreas>` element to set the **ASPNET** provider and trace against all ASP.NET areas, which are **Infrastructure**, **Module**, **Page** and **AppServices**. The sample also uses the **verbosity** attribute to set the amount of information returned to the tracing file to **warning**. Lastly, the sample uses the `<failureDefinitions>` element to trace only requests that generate a HTTP 404 status code.

[!code-xml[Main](index/samples/sample1.xml)]

<a id="006"></a>
## Sample Code

The following examples enable verbose failed request tracing for HTTP 500 errors in ASP.NET content on all requests to \*.aspx pages.

### AppCmd.exe

[!code-console[Main](index/samples/sample2.cmd)]

### C\#

[!code-csharp[Main](index/samples/sample3.cs)]

### VB.NET

[!code-vb[Main](index/samples/sample4.vb)]

### JavaScript

[!code-javascript[Main](index/samples/sample5.js)]

### VBScript

[!code-vb[Main](index/samples/sample6.vb)]
