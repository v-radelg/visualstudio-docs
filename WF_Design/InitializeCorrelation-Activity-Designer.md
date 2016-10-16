---
title: "InitializeCorrelation Activity Designer"
ms.custom: na
ms.date: 10/02/2016
ms.prod: .net-framework-4.6
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: 4c54f34c-ee84-42a6-abb0-ec260c1ccb76
caps.latest.revision: 6
manager: erikre
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
# InitializeCorrelation Activity Designer
The **InitializeCorrelation** activity designer is used to create and configure an <xref:System.ServiceModel.Activities.InitializeCorrelation?qualifyHint=False> activity that is used to establish a correlation between messages prior to sending or receiving them.  
  
## The InitializeCorrelation Activity  
 An <xref:System.ServiceModel.Activities.InitializeCorrelation?qualifyHint=False> activity is used to initialize correlations without sending or receiving a message. Typically correlation is initialized when sending or receiving a message. If correlation must be established before a message is sent or received, use <xref:System.ServiceModel.Activities.InitializeCorrelation?qualifyHint=False> to initialize the correlation.  
  
### Using the InitializeCorrelation Activity Designer  
 The **InitializeCorrelation** activity designer can be found in the **Messaging** category of the **Toolbox**, which is accessed by clicking the **Toolbox** tab on the Workflow Designer (Alternatively, select **Toolbar** from the **View** menu or CTRL+ALT+X.)  
  
 The **InitializeCorrelation** activity designer can be dragged from the **Toolbox** and dropped on to the Workflow Designer surface. This creates a <xref:System.ServiceModel.Activities.InitializeCorrelation?qualifyHint=False> activity with a default <xref:System.Activities.Activity.DisplayName?qualifyHint=False> of InitializeCorrelation.The <xref:System.Activities.Activity.DisplayName?qualifyHint=False> can be edited in the header of the **InitializeCorrelation** activity designer or in the **DisplayName** box of the **Properties** window.  
  
 The <xref:System.ServiceModel.Activities.CorrelationHandle?qualifyHint=False> can be specifies in the **Correlation** field in **Properties** window on the **InitializeCorrelation** activity designer surface.  
  
 Clicking the ellipse button besides the **CorrelationData** field in **Properties** window or the “View …” hint text on **InitializeCorrelation** activity designer surface displays the **Initialize Correlation** dialog box in which you can specify the correlation handle and the key-value pairs used to initialize it. For more information about using this dialog box, see the [Type Collection Editor Dialog Box](../WF_Design/Type-Collection-Editor-Dialog-Box.md) topic.  
  
### The InitializeCorrelation Properties  
 The following table shows the <xref:System.ServiceModel.Activities.InitializeCorrelation?qualifyHint=False> properties and describes how they are used in the designer. These properties can be edited in **Properties** window or on Workflow Designer surface.  
  
|Property Name|Required|Usage|  
|-------------------|--------------|-----------|  
|<xref:System.Activities.Activity.DisplayName?qualifyHint=False>|False|The friendly name of the <xref:System.ServiceModel.Activities.InitializeCorrelation?qualifyHint=False> activity. The default value is InitializeCorrelation.<br /><br /> Although the use of a non-default value for the friendly <xref:System.Activities.Activity.DisplayName?qualifyHint=False> is not strictly required, it is a best practice to use such a value.|  
|<xref:System.ServiceModel.Activities.InitializeCorrelation.Correlation?qualifyHint=False>|False|The <xref:System.ServiceModel.Activities.CorrelationHandle?qualifyHint=False> used to associate workflow activities in the correlation.|  
|<xref:System.ServiceModel.Activities.InitializeCorrelation.CorrelationData?qualifyHint=False>|False|A dictionary of correlation data that relates messages to the workflow instance.<br /><br /> Use the **Initialize Correlation** dialog box to configure the <xref:System.ServiceModel.Activities.InitializeCorrelation.CorrelationData?qualifyHint=False>. For more information about the use this dialog box, see the [Type Collection Editor Dialog Box](../WF_Design/Type-Collection-Editor-Dialog-Box.md) topic.|  
  
## See Also  
 [CorrelationScope](../WF_Design/CorrelationScope-Activity-Designer.md)   
 [Receive](../WF_Design/Receive-Activity-Designer.md)   
 [ReceiveAndSendReply](../WF_Design/ReceiveAndSendReply-Template-Designer.md)   
 [Send](../WF_Design/Send-Activity-Designer.md)   
 [SendAndReceiveReply](../WF_Design/SendAndReceiveReply-Template-Designer.md)   
 [TransactedReceiveScope](../WF_Design/TransactedReceiveScope-Activity-Designer.md)