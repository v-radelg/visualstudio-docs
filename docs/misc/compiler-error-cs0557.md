---
title: "Compiler Error CS0557"
ms.custom: na
ms.date: "10/13/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "CS0557"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0557"
ms.assetid: beca353e-4fea-4e4f-a48a-eddeebb153bb
caps.latest.revision: 9
ms.author: "billchi"
manager: "douge"
translation.priority.ht: 
  - "de-de"
  - "es-es"
  - "fr-fr"
  - "it-it"
  - "ja-jp"
  - "ko-kr"
  - "ru-ru"
  - "zh-cn"
  - "zh-tw"
translation.priority.mt: 
  - "cs-cz"
  - "pl-pl"
  - "pt-br"
  - "tr-tr"
---
# Compiler Error CS0557
Duplicate user-defined conversion in type 'class'  
  
 Duplicate conversion routines are not allowed in a class.  
  
 The following example generates CS0557:  
  
```  
// CS0557.cs  
namespace x  
{  
    public class ii  
    {  
        public class iii  
        {  
        public static implicit operator int(iii aa)  
        {  
            return 0;  
        }  
  
    // CS0557, delete duplicate  
        public static explicit operator int(iii aa)  
        {  
            return 0;  
        }  
        }  
  
        public static void Main()  
        {  
        }  
    }  
}  
```