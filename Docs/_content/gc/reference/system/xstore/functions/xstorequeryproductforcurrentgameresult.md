---
author: M-Stahl
title: XStoreQueryProductForCurrentGameResult
description: Gets the results for a call to [XStoreQueryProductForCurrentGameAsync](xstorequeryproductforcurrentgameasync.md).
kindex: XStoreQueryProductForCurrentGameResult
ms.author: shanede
ms.topic: reference
edited: 07/02/2019
quality: good
security: public
applies-to: pc-gdk
---

# XStoreQueryProductForCurrentGameResult  
  
Gets the results for a call to [XStoreQueryProductForCurrentGameAsync](xstorequeryproductforcurrentgameasync.md).  

## Syntax  
  
```cpp
HRESULT XStoreQueryProductForCurrentGameResult(  
         XAsyncBlock* async,  
         XStoreProductQueryHandle* productQueryHandle  
)  
```  
  
### Parameters  
  
*async* &nbsp;&nbsp;\_Inout\_  
Type: [XAsyncBlock*](../../xasync/structs/xasyncblock.md)  
  
The XAsyncBlock that was passed to [XStoreQueryProductForCurrentGameAsync](xstorequeryproductforcurrentgameasync.md). The [XAsyncBlock](../../xasync/structs/xasyncblock.md) can be used to poll for the call's status and retrieve call results. See [XAsyncBlock](../../xasync/structs/xasyncblock.md) for more information.  
  
*productQueryHandle* &nbsp;&nbsp;\_Out\_  
Type: XStoreProductQueryHandle*  
  
On return, contains a XStoreProductQueryHandle representing the query. The returned XStoreProductQueryHandle can be passed to [XStoreEnumerateProductsQuery](xstoreenumerateproductsquery.md) to enumerate the products the query returned.
  
  
### Return value
Type: HRESULT
  
S_OK on success; otherwise, returns an error code.  
  
## Remarks  
  
This result function allows you to retrieve the execution results of [XStoreQueryProductForCurrentGameAsync](xstorequeryproductforcurrentgameasync.md), as well as the store product information called for if the execution was successful. As such, this function should be called after [XStoreQueryProductForCurrentGameAsync](xstorequeryproductforcurrentgameasync.md) has been called, usually in the context of a callback function.  
  
See [XStoreQueryProductForCurrentGameAsync](xstorequeryproductforcurrentgameasync.md) for a usage example.
  
## Requirements  
  
**Header:** XStore.h (included in XGameRuntime.h)
  
**Library:** xgameruntime.lib
  
**Supported platforms:** Windows, Xbox One family consoles and Xbox Series consoles  
  
## See also  
[XStore](../xstore_members.md)
[XStoreQueryAssociatedProductsAsync](xstorequeryassociatedproductsasync.md)  
[XStoreQueryEntitledProductsAsync](xstorequeryentitledproductsasync.md)  
[XStoreQueryProductsAsync](xstorequeryproductsasync.md)  
[XStoreQueryProductForCurrentGameAsync](xstorequeryproductforcurrentgameasync.md)  
[XStoreQueryProductForPackageAsync](xstorequeryproductforpackageasync.md)  

  