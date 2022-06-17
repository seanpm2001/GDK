---
author: M-Stahl
title: XGameUiShowPlayerProfileCardResult
description: Gets the result of a call to [XGameUiShowPlayerProfileCardAsync](xgameuishowplayerprofilecardasync.md).
kindex: XGameUiShowPlayerProfileCardResult
ms.author: aarocar
ms.topic: reference
edited: 01/11/2021
security: public
applies-to: pc-gdk
---

# XGameUiShowPlayerProfileCardResult  

Gets the result of a call to [XGameUiShowPlayerProfileCardAsync](xgameuishowplayerprofilecardasync.md).  

<a id="syntaxSection"></a>

## Syntax  

```cpp
HRESULT XGameUiShowPlayerProfileCardResult(  
         XAsyncBlock* async  
)  
```  

<a id="parametersSection"></a>

### Parameters  

*async* &nbsp;&nbsp;\_In\_  
Type: [XAsyncBlock](../../xasync/structs/xasyncblock.md)\*  

A pointer to the [XAsyncBlock](../../xasync/structs/xasyncblock.md) object that was passed to [XGameUiShowPlayerProfileCardAsync](xgameuishowplayerprofilecardasync.md).  

<a id="retvalSection"></a>

### Return value  

Type: HRESULT  

HRESULT success or error code.  

<a id="remarksSection"></a>

## Remarks  

Typically, you specify this function in [XAsyncBlock](../../xasync/structs/xasyncblock.md) as the callback function for [XGameUiShowPlayerProfileCardAsync](xgameuishowplayerprofilecardasync.md).  

You can also retrieve the result by calling this function after `XGameUiShowPlayerProfileCardAsync` completes.  

<a id="requirementsSection"></a>

## Requirements  

**Header:** XGameUI.h  

**Library:** xgameruntime.lib  

**Supported platforms:** Windows, Xbox One family consoles and Xbox Series consoles  

<a id="seealsoSection"></a>

## See also  

[XGameUI](../xgameui_members.md)  
  