---
title: "IDiaSession::findFileById"
ms.custom: na
ms.date: 10/03/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 710efe04-78b5-4f3e-a1d8-f9b069063503
caps.latest.revision: 9
manager: ghogen
translation.priority.ht: 
  - de-de
  - es-es
  - fr-fr
  - it-it
  - ja-jp
  - ko-kr
  - ru-ru
  - zh-cn
  - zh-tw
translation.priority.mt: 
  - cs-cz
  - pl-pl
  - pt-br
  - tr-tr
---
# IDiaSession::findFileById
Retrieves a source file by source file identifier.  
  
## Syntax  
  
```cpp#  
HRESULT findFileById (   
   DWORD            uniqueId,  
   IDiaSourceFile** ppResult  
);  
```  
  
#### Parameters  
 `uniqueId`  
 [in] Specifies the source file identifier.  
  
 `ppResult`  
 [out] Returns an [IDiaSourceFile](../VS_debugger/IDiaSourceFile.md) object that represents the source file retrieved.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 The source file identifier is a unique value used internally to the DIA SDK to make all source files unique. This method is typically used internally to the DIA SDK.  
  
## See Also  
 [IDiaSession](../VS_debugger/IDiaSession.md)   
 [IDiaSession::findFile](../VS_debugger/IDiaSession--findFile.md)   
 [IDiaSourceFile](../VS_debugger/IDiaSourceFile.md)