---
author: joannaleecy
title: XblPrivacyGetMuteListResultCount
description: Get result count for an XblPrivacyGetMuteListAsync call.
kindex: XblPrivacyGetMuteListResultCount
ms.author: migreen
ms.topic: reference
security: public
edited: 00/00/0000
applies-to: pc-gdk
---

# XblPrivacyGetMuteListResultCount  

Get result count for an XblPrivacyGetMuteListAsync call.  

## Syntax  
  
```cpp
HRESULT XblPrivacyGetMuteListResultCount(  
         XAsyncBlock* async,  
         size_t* xuidCount  
)  
```  
  
### Parameters  
  
*async* &nbsp;&nbsp;\_In\_  
Type: XAsyncBlock*  
  
The AsyncBlock for this operation.  
  
*xuidCount* &nbsp;&nbsp;\_Out\_  
Type: size_t*  
  
Passes back the number of Xuids in the mute list.  
  
  
### Return value  
Type: HRESULT
  
HRESULT return code for this API operation.
  
## Requirements  
  
**Header:** privacy_c.h
  
**Library:** Microsoft.Xbox.Services.141.GSDK.C.lib
  
## See also  
[privacy_c](../privacy_c_members.md)  
  
  