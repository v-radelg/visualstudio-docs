---
title: "Compiler Error CS1575"
ms.custom: na
ms.date: 10/01/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 76a9c57c-8f79-482e-9ae8-c70e8f199dd7
caps.latest.revision: 7
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
# Compiler Error CS1575
A stackalloc expression requires [] after type  
  
 The size of the requested allocation, with [stackalloc](../Topic/stackalloc%20\(C%23%20Reference\).md), must be specified in square brackets.  
  
 The following sample generates CS1575:  
  
```  
// CS1575.cs  
// compile with: /unsafe  
public class MyClass  
{  
   unsafe public static void Main()  
   {  
      int *p = stackalloc int (30);   // CS1575  
      // try the following line instead  
      // int *p = stackalloc int [30];  
   }  
}  
```