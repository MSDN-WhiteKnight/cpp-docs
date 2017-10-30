---
title: "NMAKE Fatal Error U1100 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: ["cpp-tools"]
ms.tgt_pltfrm: ""
ms.topic: "error-reference"
f1_keywords: ["U1100"]
dev_langs: ["C++"]
helpviewer_keywords: ["U1100"]
ms.assetid: c71910a7-c581-4d9c-a38c-d2d557d56289
caps.latest.revision: 6
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
---
# NMAKE Fatal Error U1100
macro 'macroname' is illegal in the context of batch rule 'rule'  
  
 NMAKE generates this error when the command block of a batch-mode rule directly or indirectly references a special file macro that is not $<.  
  
 $< is the only allowed macro for batch-mode rules.