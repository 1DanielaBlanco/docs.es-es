---
title: "Cómo: buscar un atributo del elemento primario (XPath-LINQ to XML) (Visual Basic) | Documentos de Microsoft"
ms.custom: 
ms.date: 2015-07-20
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-visual-basic
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- VB
ms.assetid: 9d2572fd-27d4-426c-b079-16854cb9ec7d
caps.latest.revision: 3
author: stevehoag
ms.author: shoag
translationtype: Machine Translation
ms.sourcegitcommit: a06bd2a17f1d6c7308fa6337c866c1ca2e7281c0
ms.openlocfilehash: adaece829b167e432963980f7fb4cbc326b0cfda
ms.lasthandoff: 03/13/2017


---
# <a name="how-to-find-an-attribute-of-the-parent-xpath-linq-to-xml-visual-basic"></a>Cómo: buscar un atributo del elemento primario (XPath-LINQ to XML) (Visual Basic)
En este tema se muestra cómo desplazarse hasta el elemento primario y buscar un atributo en él.  
  
 La expresión XPath es:  
  
 `../@id`  
  
## <a name="example"></a>Ejemplo  
 Este ejemplo busca primero un elemento `Author`. Después busca el atributo `id` del elemento primario.  
  
 Este ejemplo utiliza el siguiente documento XML: [archivo XML de ejemplo: libros (LINQ to XML)](../../../../visual-basic/programming-guide/concepts/linq/sample-xml-file-books-linq-to-xml.md).  
  
```vb  
Dim books As XDocument = XDocument.Load("Books.xml")  
Dim author As XElement = books.Root.<Book>.<Author>.FirstOrDefault()  
  
' LINQ to XML query  
Dim att1 As XAttribute = author.Parent.Attribute("id")  
  
' XPath expression  
Dim att2 As XAttribute = DirectCast(author.XPathEvaluate("../@id"),  _  
    IEnumerable).Cast(Of XAttribute)().First()  
  
If att1 Is att2 Then  
    Console.WriteLine("Results are identical")  
Else  
    Console.WriteLine("Results differ")  
End If  
Console.WriteLine(att1)  
  
```  
  
 Este ejemplo produce el siguiente resultado:  
  
```  
Results are identical  
id="bk101"  
```  
  
## <a name="see-also"></a>Vea también  
 [LINQ to XML para usuarios de XPath (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/linq-to-xml-for-xpath-users.md)
