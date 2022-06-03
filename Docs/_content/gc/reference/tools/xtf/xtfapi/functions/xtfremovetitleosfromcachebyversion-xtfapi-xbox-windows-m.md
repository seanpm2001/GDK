---
author: aablackm
title: XtfRemoveTitleOSFromCacheByVersion
description: Removes the Game OS matching the specified [FourPartVersion](../structs/fourpartversion-xtfapi-xbox-windows-s.md) from the cache on the console.
kindex: XtfRemoveTitleOSFromCacheByVersion
ms.author: zhooper
ms.topic: reference
edited: 04/15/2020
security: public
---

# XtfRemoveTitleOSFromCacheByVersion
  
Removes the Game OS matching the specified [FourPartVersion](../structs/fourpartversion-xtfapi-xbox-windows-s.md) from the cache on the console.  
  
<a id="syntaxSection"></a>
  
## Syntax
  
```cpp
HRESULT XtfRemoveTitleOSFromCacheByVersion(
         PCWSTR address,
         FourPartVersion version
)  
```
  
<a id="parametersSection"></a>
  
### Parameters
  
*address*  
Type: PCWSTR  
  
\[in\] The address of the console.  
  
*version*  
Type: [FourPartVersion](../structs/fourpartversion-xtfapi-xbox-windows-s.md)  
  
\[in\] The four-part version number of the Game OS to remove.  
  
<a id="retvalSection"></a>
  
### Return value
  
Type: HRESULT  
  
Returns `S_OK` if successful; otherwise, returns an HRESULT error code.  
  
<a id="remarksSection"></a>
  
## Remarks
  
Use this function to manage provisioned Game OS files by removing the Game OS matching the specified `FourPartVersion` from the cache on the console. You can use the [XtfGetCachedTitleOSVersions](xtfgetcachedtitleosversions-xtfapi-xbox-windows-m.md) function to get the `FourPartVersion` of each Game OS cached on the console, or the [XtfGetTitleOSFourPartVersion](xtfgettitleosfourpartversion-xtfapi-xbox-windows-m.md) function to get the `FourPartVersion` of the Game OS for the currently running title. If you attempt to remove a Game OS flagged as a fallback OS, an error occurs.
  
If you don't have a [FourPartVersion](../structs/fourpartversion-xtfapi-xbox-windows-s.md) for the Game OS you want to remove, use the [XtfRemoveTitleOSFromCache](xtfremovetitleosfromcache-xtfapi-xbox-windows-m.md) function instead to remove a Game OS by specifying a different identifier, such as the full path and file name of the GameOs.vxd file for the Game OS to be removed.  
  
You can also add a Game OS to the cache on the console by calling the [XtfCacheTitleOS](xtfcachetitleos-xtfapi-xbox-windows-m.md) function. For more information about managing provisioned Game OS files, see [Application Management (xbapp.exe) (NDA topic)](../../../../../tools-console/xbox-tools-and-apis/commandlinetools/xbapp.md) and [Provision (xbprovision.exe) (NDA topic)](../../../../../tools-console/xbox-tools-and-apis/commandlinetools/xbprovision.md).  
  
<a id="requirementsSection"></a>
  
## Requirements
  
**Header:** xtfapi.h  
  
**Library:** XtfApi.lib  
  
**Supported platforms:** Windows (for Xbox console tools)  
  
<a id="seealsoSection"></a>
  
## See also  
  
[Run from PC Deployment (NDA topic)](../../../../../tools-console/usinggsdk/deployment/deployment.md)  
[XTF Transport Errors (NDA topic)](../../../../../tools-console/xbox-tools-and-apis/commandlinetools/xtf-transport-errors.md)  
[Additional Xtf APIs](../atoc-xtfapi.md)  
  