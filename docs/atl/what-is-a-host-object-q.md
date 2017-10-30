---
title: "What Is a Host Object? (ATL) | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: ["cpp-windows"]
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: ["C++"]
helpviewer_keywords: ["host objects"]
ms.assetid: 4f8da992-b27e-45e8-b5e0-c8b1dcae4fac
caps.latest.revision: 12
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
---
# What Is a Host Object?
A host object is a COM object that represents the ActiveX control container supplied by ATL for a particular window. The host object subclasses the container window so that it can reflect messages to the control, it provides the necessary container interfaces to be used by the control, and it exposes the [IAxWinHostWindow](../atl/reference/iaxwinhostwindow-interface.md) and [IAxWinAmbientDispatch](../atl/reference/iaxwinambientdispatch-interface.md) interfaces to allow you to configure the environment of the control.  
  
 You can use the host object to set the ambient properties of the container.  
  
## See Also  
 [Control Containment FAQ](../atl/atl-control-containment-faq.md)
