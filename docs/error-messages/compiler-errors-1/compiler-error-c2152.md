---
title: "Compiler Error C2152 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: ["cpp-tools"]
ms.tgt_pltfrm: ""
ms.topic: "error-reference"
f1_keywords: ["C2152"]
dev_langs: ["C++"]
helpviewer_keywords: ["C2152"]
ms.assetid: a9ea2b0c-d55d-41c7-ba9f-dd75592ffc8a
caps.latest.revision: 6
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
---
# Compiler Error C2152
'identifier' : pointers to functions with different attributes  
  
 A pointer to a function with one calling convention (`__cdecl`, `__stdcall`, or `__fastcall`) is assigned to a pointer to a function with another calling convention.