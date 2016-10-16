---
title: "Compiler Error CS1513"
ms.custom: na
ms.date: 10/02/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 28dacbb5-bf60-49ac-878e-c0ce469114eb
caps.latest.revision: 6
manager: douge
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
# Compiler Error CS1513
} expected  
  
 The compiler expected a closing curly brace (`}`) that was not found.  
  
 The following sample generates CS1513:  
  
```  
// CS1513  
namespace y   // CS1513, no close curly brace  
{  
   class x  
   {  
      public static void Main()  
      {  
      }  
   }  
```