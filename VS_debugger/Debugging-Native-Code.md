---
title: "Debugging Native Code"
ms.custom: na
ms.date: 10/03/2016
ms.devlang: 
  - FSharp
  - VB
  - CSharp
  - C++
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d94eee90-7e0d-4cac-88c1-9831030daa5e
caps.latest.revision: 21
manager: ghogen
translation.priority.ht: 
  - cs-cz
  - de-de
  - es-es
  - fr-fr
  - it-it
  - ja-jp
  - ko-kr
  - pl-pl
  - pt-br
  - ru-ru
  - tr-tr
  - zh-cn
  - zh-tw
---
# Debugging Native Code
The section covers some common debugging problems and techniques for native applications. The techniques covered in this section are high-level techniques. For the mechanics of using the Visual Studio debugger, see [Debugger Roadmap](../VS_debugger/Debugger-Basics.md).  
  
## In This Section  
 [How to: Debug Optimized Code](../VS_debugger/How-to--Debug-Optimized-Code.md)  
 Gives tips for debugging optimized code, specifically, why you should debug an unoptimized version of your program, default optimization settings for Debug and Release configurations, and tips for finding bugs that only appear in optimized code (turning on optimization in a Debug build configuration).  
  
 [DebugBreak and __debugbreak](../VS_debugger/DebugBreak-and-__debugbreak.md)  
 Describes the Win32 `DebugBreak` function and provides a link to its reference topic in the Platform SDK. Also describes the `__debugbreak` intrinsic.  
  
 [C/C++ Assertions](../VS_debugger/C-C---Assertions.md)  
 Discusses assertion statements, how they work, the benefits of using them (catching logic errors, checking results of an operation, and testing error conditions), their interaction with `_DEBUG`, and the types of assertions supported in Visual Studio.  
  
 [How to: Debug Inline Assembly Code](../VS_debugger/How-to--Debug-Inline-Assembly-Code.md)  
 Provides short instructions on using the Disassembly window to view the assembly instructions and the Registers window to view register contents and provides links to topics regarding those windows.  
  
 [MFC Debugging Techniques](../VS_debugger/MFC-Debugging-Techniques.md)  
 Links you to debugging techniques for MFC programs, including: afxDebugBreak, the TRACE macro, detecting memory leaks in MFC, MFC assertions, and reducing the size of MFC Debug builds.  
  
 [CRT Debugging Techniques](../VS_debugger/CRT-Debugging-Techniques.md)  
 Links you to debugging techniques for the C Run-Time Library, including using the CRT Debug Library, macros for reporting, differences between malloc and _malloc_dbg, writing debug hook functions, and the CRT debug heap.  
  
 [Debugging Native Code FAQs](../VS_debugger/Debugging-Native-Code-FAQs.md)  
 Provides answers to frequently asked questions about debugging Visual C++ programs  
  
 [COM and ActiveX Debugging](../VS_debugger/COM-and-ActiveX-Debugging.md)  
 Provides information on debugging COM and ActiveX applications, including tools you can use for COM and ActiveX debugging.  
  
 [How to: Debug Native DLLs](../VS_debugger/How-to--Debug-Native-DLLs.md)  
 Explains how to set up debugging for DLLs from native code.  
  
 [How to: Debug Injected Code](../VS_debugger/How-to--Debug-Injected-Code.md)  
 Provides guidance on debugging code that uses attributes. Instructions include how to turn on Source Annotation, how to view injected code, and how to view the disassembly code at the current execution point.  
  
 [Walkthrough: Debugging a Parallel Application](../VS_debugger/Walkthrough--Debugging-a-Parallel-Application.md)  
 Describes how to use the **Parallel Tasks** and **Parallel Stacks** tool windows to debug a parallel application.  
  
## Related Sections  
 [Visual C++ Project Types](../VS_debugger/Debugging-Preparation--Visual-C---Project-Types.md)  
 Provides links to topics that describe how to debug the native project types created by the Visual C++ project templates.  
  
 [Debugging in Visual Studio](../VS_debugger/Debugging-in-Visual-Studio.md)  
 Provides links to the larger sections of the debugging documentation. Information includes what's new in the debugger, settings and preparation, breakpoints, handling exceptions, edit and continue, debugging managed code, debugging native code, debugging SQL, and the user interface references.  
  
## See Also  
 [Debugger Security](../VS_debugger/Debugger-Security.md)   
 [Debugging in Visual Studio](../VS_debugger/Debugging-in-Visual-Studio.md)