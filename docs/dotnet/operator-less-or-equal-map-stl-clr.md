---
title: "operator&lt;= (map) (STL/CLR) | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: ["cpp-windows"]
ms.tgt_pltfrm: ""
ms.topic: "reference"
f1_keywords: ["cliext::map::operator<="]
dev_langs: ["C++"]
helpviewer_keywords: ["operator<= member [STL/CLR]"]
ms.assetid: 8209ce40-0b2d-470d-9c64-97743e305902
caps.latest.revision: 16
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
---
# operator&lt;= (map) (STL/CLR)
List less than or equal comparison.  
  
## Syntax  
  
```  
template<typename Key,  
    typename Mapped>  
    bool operator<=(map<Key, Mapped>% left,  
        map<Key, Mapped>% right);  
```  
  
#### Parameters  
 left  
 Left container to compare.  
  
 right  
 Right container to compare.  
  
## Remarks  
 The operator function returns `!(right < left)`. You use it to test whether `left` is not ordered after `right` when the two maps are compared element by element.  
  
## Example  
  
```  
// cliext_map_operator_le.cpp   
// compile with: /clr   
#include <cliext/map>   
  
typedef cliext::map<wchar_t, int> Mymap;   
int main()   
    {   
    Mymap c1;   
    c1.insert(Mymap::make_value(L'a', 1));   
    c1.insert(Mymap::make_value(L'b', 2));   
    c1.insert(Mymap::make_value(L'c', 3));   
  
// display contents " [a 1] [b 2] [c 3]"   
    for each (Mymap::value_type elem in c1)   
        System::Console::Write(" [{0} {1}]", elem->first, elem->second);   
    System::Console::WriteLine();   
  
// assign to a new container   
    Mymap c2;   
    c2.insert(Mymap::make_value(L'a', 1));   
    c2.insert(Mymap::make_value(L'b', 2));   
    c2.insert(Mymap::make_value(L'd', 4));   
  
// display contents " [a 1] [b 2] [d 4]"   
    for each (Mymap::value_type elem in c2)   
        System::Console::Write(" [{0} {1}]", elem->first, elem->second);   
    System::Console::WriteLine();   
  
    System::Console::WriteLine("[a b c] <= [a b c] is {0}",   
        c1 <= c1);   
    System::Console::WriteLine("[a b d] <= [a b c] is {0}",   
        c2 <= c1);   
    return (0);   
    }  
  
```  
  
```Output  
 [a 1] [b 2] [c 3]  
 [a 1] [b 2] [d 4]  
[a b c] <= [a b c] is True  
[a b d] <= [a b c] is False  
```  
  
## Requirements  
 **Header:** \<cliext/map>  
  
 **Namespace:** cliext  
  
## See Also  
 [map (STL/CLR)](../dotnet/map-stl-clr.md)   
 [operator== (map) (STL/CLR)](../dotnet/operator-equality-map-stl-clr.md)   
 [operator!= (map) (STL/CLR)](../dotnet/operator-inequality-map-stl-clr.md)   
 [operator\< (map) (STL/CLR)](../dotnet/operator-less-than-map-stl-clr.md)   
 [operator>= (map) (STL/CLR)](../dotnet/operator-greater-or-equal-map-stl-clr.md)   
 [operator> (map) (STL/CLR)](../dotnet/operator-greater-than-map-stl-clr.md)