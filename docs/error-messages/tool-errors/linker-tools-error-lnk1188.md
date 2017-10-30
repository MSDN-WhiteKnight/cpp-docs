---
title: "Linker Tools Error LNK1188 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: ["cpp-tools"]
ms.tgt_pltfrm: ""
ms.topic: "error-reference"
f1_keywords: ["LNK1188"]
dev_langs: ["C++"]
helpviewer_keywords: ["LNK1188"]
ms.assetid: 4af574b0-5b41-4580-9a37-52a634add995
caps.latest.revision: 6
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
---
# Linker Tools Error LNK1188
BADFIXUPSECTION:: invalid fixup target 'symbol'; possible zero length section  
  
 During a VxD link, the target of a relocation did not have a section. With LINK386 (an older version), an OMF GROUP record (generated by a MASM GROUP directive) may have been used to combine the zero length section with another non-zero length section. COFF format does not support the GROUP directive and zero-length sections. When LINK automatically converts this type of OMF objects to COFF, this error may occur.