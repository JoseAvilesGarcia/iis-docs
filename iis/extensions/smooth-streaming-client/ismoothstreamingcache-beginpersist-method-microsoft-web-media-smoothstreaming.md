---
title: ISmoothStreamingCache.BeginPersist Method  (Microsoft.Web.Media.SmoothStreaming)
TOCTitle: BeginPersist Method
description: "The ISmoothStreamingCache.BeginPersist method begins to persist a cache response. This article describes its syntax, examples, and version information."
ms:assetid: M:Microsoft.Web.Media.SmoothStreaming.ISmoothStreamingCache.BeginPersist(Microsoft.Web.Media.SmoothStreaming.CacheRequest,Microsoft.Web.Media.SmoothStreaming.CacheResponse,System.AsyncCallback,System.Object)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.web.media.smoothstreaming.ismoothstreamingcache.beginpersist(v=VS.90)
ms:contentKeyID: 31469282
ms.date: 05/02/2012
mtps_version: v=VS.90
f1_keywords:
- Microsoft.Web.Media.SmoothStreaming.ISmoothStreamingCache.BeginPersist
dev_langs:
- csharp
- jscript
- vb
- cpp
api_location:
- Microsoft.Web.Media.SmoothStreaming.dll
api_name:
- Microsoft.Web.Media.SmoothStreaming.ISmoothStreamingCache.BeginPersist
api_type:
  - Assembly
topic_type:
- apiref
product_family_name: VS
---

# BeginPersist Method

Begins to persist a cache response. This function is called whenever in the course of normal playback a Smooth Streaming object chunk, manifest, or key frame is received from the network and it might be useful to persist the item for later use.

**Namespace:**  [Microsoft.Web.Media.SmoothStreaming](microsoft-web-media-smoothstreaming-namespace_1.md)  
**Assembly:**  Microsoft.Web.Media.SmoothStreaming (in Microsoft.Web.Media.SmoothStreaming.dll)

## Syntax

```vb
'Declaration

  Function BeginPersist ( _
    request As CacheRequest, _
    response As CacheResponse, _
    callback As AsyncCallback, _
    state As Object _
) As IAsyncResult
'Usage

  Dim instance As ISmoothStreamingCache
Dim request As CacheRequest
Dim response As CacheResponse
Dim callback As AsyncCallback
Dim state As Object
Dim returnValue As IAsyncResult

returnValue = instance.BeginPersist(request, _
    response, callback, state)
```

```csharp
  IAsyncResult BeginPersist(
    CacheRequest request,
    CacheResponse response,
    AsyncCallback callback,
    Object state
)
```

```cpp
  IAsyncResult^ BeginPersist(
    CacheRequest^ request, 
    CacheResponse^ response, 
    AsyncCallback^ callback, 
    Object^ state
)
```

```jscript
  function BeginPersist(
    request : CacheRequest, 
    response : CacheResponse, 
    callback : AsyncCallback, 
    state : Object
) : IAsyncResult
```

### Parameters

  - request  
    Type: [Microsoft.Web.Media.SmoothStreaming.CacheRequest](cacherequest-class-microsoft-web-media-smoothstreaming_1.md)  
    A [CacheRequest](cacherequest-class-microsoft-web-media-smoothstreaming_1.md) object.  

<!-- end list -->

  - response  
    Type: [Microsoft.Web.Media.SmoothStreaming.CacheResponse](cacheresponse-class-microsoft-web-media-smoothstreaming_1.md)  
    A [CacheResponse](cacheresponse-class-microsoft-web-media-smoothstreaming_1.md) object.  

<!-- end list -->

  - callback  
    Type: [System.AsyncCallback](https://msdn.microsoft.com/library/ckbe7yh5)  
    A [AsyncCallback](https://msdn.microsoft.com/library/ckbe7yh5) delegate method to complete the operation.  

<!-- end list -->

  - state  
    Type: [System.Object](https://msdn.microsoft.com/library/e5kfa45b)  
    A [Object](https://msdn.microsoft.com/library/e5kfa45b) that represents state for the request.  

### Return Value

Type: [System.IAsyncResult](https://msdn.microsoft.com/library/ft8a6455)  
An [IAsyncResult](https://msdn.microsoft.com/library/ft8a6455) object.  

## Remarks

A [Silverlight IIS Smooth Streaming Offline Cache Sample](http://www.iis.net/community/default.aspx?tabid=34&g=6&i=2013) that demonstrates implementation of [ISmoothStreamingCache](ismoothstreamingcache-interface-microsoft-web-media-smoothstreaming_1.md) is available on the IIS Website.

For documentation of the sample, see [Cache Plug-in Implementation of ISmoothStreamingCache](cache-plug-in-implementation-of-ismoothstreamingcache_1.md).

## Examples

The following code shows an implementation of the BeginPersist(CacheRequest, CacheResponse, AsyncCallback, Object) method.

``` 
    public IAsyncResult BeginPersist(CacheRequest request, CacheResponse response, AsyncCallback callback, object state)
    {
        state = false;
        CacheAsyncResult ar = new CacheAsyncResult();

        if (!keyUrls.ContainsKey(request.CanonicalUri.ToString()))
        {
            state = true;
            ar.strUrl = request.CanonicalUri.ToString();
            ar.Complete(response, (bool)state);
            return ar;
        }

        ar.Complete(null, true);
        return ar;
    }
```

## Version Information

### Silverlight

Supported in: 4  

### Silverlight for Windows Phone

Supported in: Windows Phone OS 7.0  

## Permissions

  - Full trust for the immediate caller. This member cannot be used by partially trusted code. For more information, see [Using Libraries from Partially Trusted Code](https://msdn.microsoft.com/library/8skskf63).

## See Also

### Reference

[ISmoothStreamingCache Interface](ismoothstreamingcache-interface-microsoft-web-media-smoothstreaming_1.md)

[Microsoft.Web.Media.SmoothStreaming Namespace](microsoft-web-media-smoothstreaming-namespace_1.md)
