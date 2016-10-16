---
title: "Map methods on the call stack while debugging in Visual Studio"
ms.custom: na
ms.date: 10/03/2016
ms.devlang: 
  - FSharp
  - VB
  - CSharp
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: get-started-article
ms.assetid: d6a72e5e-f88d-46fc-94a3-1789d34805ef
caps.latest.revision: 39
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
# Map methods on the call stack while debugging in Visual Studio
Create a code map to visually trace the call stack while you’re debugging. You can make notes on the map to track what the code is doing so you can focus on finding bugs.  
  
 ![Debugging with call stacks on code maps](../VS_debugger/media/DebuggerMap_Overview.png "DebuggerMap_Overview")  
  
 You’ll need:  
  
-   [Visual Studio Enterprise](https://www.visualstudio.com/downloads/download-visual-studio-vs)  
  
-   Code that you can debug, such as Visual C# .NET, Visual Basic .NET, C++, JavaScript, or X++  
  
 See: [Video: Debug visually with Code Map debugger integration (Channel 9)](http://go.microsoft.com/fwlink/?LinkId=293418) • [Map the call stack](#MapStack) • [Make notes about the code](#MakeNotes) • [Update the map with the next call stack](#UpdateMap) • [Add related code to the map](#AddRelatedCode) • [Find bugs using the map](#FindBugs) • [Q & A](#QA)  
  
 For details of the commands and actions you can use when working with code maps, see [Browse and rearrange code maps](../VS_IDE/Browse-and-rearrange-code-maps.md).  
  
##  <a name="MapStack"></a> Map the call stack  
  
1.  Start debugging. (Keyboard: **F5**)  
  
2.  After your app enters break mode or you step into a function, choose **Code Map**. (Keyboard: **Ctrl** + **Shift** + **`**)  
  
     ![Choose Code Map to start mapping call stack](../VS_debugger/media/DebuggerMap_ChooseCodeMap.png "DebuggerMap_ChooseCodeMap")  
  
     The current call stack appears in orange on a new code map:  
  
     ![See call stack on code map](../VS_debugger/media/DebuggerMap_SeeUndoCallStack.png "DebuggerMap_SeeUndoCallStack")  
  
     The map will update automatically while you continue debugging. See [Update the map with the next call stack](#UpdateMap).  
  
##  <a name="MakeNotes"></a> Make notes about the code  
 Add comments to track what’s happening in the code. To add a new line in a comment, press **Shift + Return**.  
  
 ![Add comment to call stack on code map](../VS_debugger/media/DebuggerMap_AddComment.png "DebuggerMap_AddComment")  
  
##  <a name="UpdateMap"></a> Update the map with the next call stack  
 Run your app to the next breakpoint or step into a function. The map adds a new call stack.  
  
 ![Update code map with next call stack](../VS_debugger/media/DebuggerMap_AddClearCallStack.png "DebuggerMap_AddClearCallStack")  
  
##  <a name="AddRelatedCode"></a> Add related code to the map  
 Now you’ve got a map – what next? If you’re working with Visual C# .NET or Visual Basic .NET, add items, such as fields, properties, and other methods, to track what’s happening in the code.  
  
 Double-click a method to see its code definition, or use the shortcut menu for the method. (Keyboard: Select the method on the map and press **F12**)  
  
 ![Go to code definition for a method on code map](../VS_debugger/media/DebuggerMap_GoToCodeDefinition.png "DebuggerMap_GoToCodeDefinition")  
  
 Add the items that you want to track on the map.  
  
 ![Show fields in a method on call stack code map](../VS_debugger/media/DebuggerMap_ShowFields.png "DebuggerMap_ShowFields")  
  
> [!NOTE]
>  By default, adding items to the map also adds the parent group nodes such as the class, namespace, and assembly. While this is useful, you can keep the map simple by turning off this feature using the **Include Parents** button on the map toolbar, or by pressing **CTRL** when you add items.  
  
 ![Fields related to a method on call stack code map](../VS_debugger/media/DebuggerMap_ShowedFields.png "DebuggerMap_ShowedFields")  
  
 Here you can easily see which methods use the same fields. The most recently added items appear in green.  
  
 Continue building the map to see more code.  
  
 ![See methods that use a field: call stack code map](../VS_debugger/media/DebuggerMap_FindAllReferences.png "DebuggerMap_FindAllReferences")  
  
 ![Methods that use a field on call stack code map](../VS_debugger/media/DebuggerMap_FoundAllReferences.png "DebuggerMap_FoundAllReferences")  
  
##  <a name="FindBugs"></a> Find bugs using the map  
 Visualizing your code can help you find bugs faster. For example, suppose you’re investigating a bug in a drawing program. When you draw a line and try to undo it, nothing happens until you draw another line.  
  
 So you set breakpoints in the `clear`, `undo`, and `Repaint` methods, start debugging, and build a map like this one:  
  
 ![Add another call stack to code map](../VS_debugger/media/DebuggerMap_AddPaintObjectCallStack.png "DebuggerMap_AddPaintObjectCallStack")  
  
 You notice that all the user gestures on the map call `Repaint`, except for `undo`. This might explain why `undo` doesn’t work immediately.  
  
 After you fix the bug and continue running the program, the map adds the new call from `undo` to `Repaint`:  
  
 ![Add new method call to call stack on code map](../VS_debugger/media/DebuggerMap_AddNewCallForRepaint.png "DebuggerMap_AddNewCallForRepaint")  
  
##  <a name="QA"></a> Q & A  
  
-   **Not all calls appear on the map. Why?**  
  
     By default, only your own code appears on the map. To see external code, turn it on in the **Call Stack** window:  
  
     ![Display external code using the Call Stack window](../VS_debugger/media/DebuggerMap_CallStackMenu.png "DebuggerMap_CallStackMenu")  
  
     or turn off **Enable Just My Code** in the Visual Studio debugging options:  
  
     ![Show external code using Options dialog](../VS_debugger/media/DebuggerMap_DebugOptions.png "DebuggerMap_DebugOptions")  
  
-   **Does changing the map affect the code?**  
  
     Changing the map doesn’t affect the code in any way. Feel free to rename, move, or remove anything on the map.  
  
-   **What does this message mean: “The diagram may be based on an older version of the code”?**  
  
     The code might have changed after you last updated the map. For example, a call on the map might not exist in code anymore. Close the message, then try rebuilding the solution before updating the map again.  
  
-   **How do I control the map’s layout?**  
  
     Open the **Layout** menu on the map toolbar:  
  
    -   Change the default layout.  
  
    -   To stop rearranging the map automatically, turn off **Automatically Layout when Debugging**.  
  
    -   To rearrange the map as little as possible when you add items, turn off **Incremental Layout**.  
  
-   **Can I share the map with others?**  
  
     You can export the map, send it to others if you have Microsoft Outlook, or save it to your solution so you can check it into Team Foundation version control.  
  
     ![Share call stack code map with others](../VS_debugger/media/DebuggerMap_ShareWithOthers.png "DebuggerMap_ShareWithOthers")  
  
-   **How do I stop the map from adding new call stacks automatically?**  
  
     Choose ![Button &#45; Show call stack on code map automatically](../VS_debugger/media/DebuggerMap_AutomaticUpdateIcon.gif "DebuggerMap_AutomaticUpdateIcon") on the map toolbar. To manually add the current call stack to the map, press **Ctrl** + **Shift** + **`**.  
  
     The map will continue highlighting existing call stacks on the map while you’re debugging.  
  
-   **What do the item icons and arrows mean?**  
  
     To get more info about an item, move the mouse pointer over it and look at the item’s tooltip. You can also look at the **Legend** to learn what each icon means.  
  
     ![What do icons on the call stack code map mean?](../VS_debugger/media/DebuggerMap_ShowLegend.png "DebuggerMap_ShowLegend")  
  
 See: [Map the call stack](#MapStack) • [Make notes about the code](#MakeNotes) • [Update the map with the next call stack](#UpdateMap) • [Add related code to the map](#AddRelatedCode) • [Find bugs using the map](#FindBugs)  
  
## See Also  
 [Map dependencies across your solutions](../VS_IDE/Map-dependencies-across-your-solutions.md)   
 [Use code maps to debug your applications](../VS_IDE/Use-code-maps-to-debug-your-applications.md)   
 [Find potential problems using code map analyzers](../VS_IDE/Find-potential-problems-using-code-map-analyzers.md)   
 [Browse and rearrange code maps](../VS_IDE/Browse-and-rearrange-code-maps.md)