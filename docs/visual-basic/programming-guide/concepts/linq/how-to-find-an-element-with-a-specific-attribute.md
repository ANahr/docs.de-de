---
title: 'Gewusst wie: Suchen nach einem Element mit bestimmten Attributen (Visual Basic) | Microsoft-Dokumentation'
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
ms.assetid: 59fb7c19-d42f-40eb-8cf8-f1d5b9658eb7
caps.latest.revision: 3
author: stevehoag
ms.author: shoag
translationtype: Machine Translation
ms.sourcegitcommit: a06bd2a17f1d6c7308fa6337c866c1ca2e7281c0
ms.openlocfilehash: ce57f1c7e0e1860d858d36ccaff256aa4afe7e2b
ms.lasthandoff: 03/13/2017


---
# <a name="how-to-find-an-element-with-a-specific-attribute-visual-basic"></a>Gewusst wie: Suchen nach einem Element mit bestimmten Attributen (Visual Basic)
In diesem Thema wird gezeigt, wie Sie nach einem Element mit einem bestimmten Wert suchen können.  
  
## <a name="example"></a>Beispiel  
 Das Beispiel zeigt die Suche nach dem `Address`-Element mit dem `Type`-Attribut und dem Wert "Billing".  
  
 Dieses Beispiel verwendet die folgende XML-Dokument: [XML-Beispieldatei: Typical Purchase Order (LINQ to XML)](../../../../visual-basic/programming-guide/concepts/linq/sample-xml-file-typical-purchase-order-linq-to-xml.md).  
  
```vb  
Dim root As XElement = XElement.Load("PurchaseOrder.xml")  
Dim address As IEnumerable(Of XElement) = _  
    From el In root.<Address> _  
    Where el.@Type = "Billing" _  
    Select el  
For Each el As XElement In address  
    Console.WriteLine(el)  
Next  
```  
  
 Dieser Code erzeugt die folgende Ausgabe:  
  
```xml  
  
          <Address Type="Billing">  
  <Name>Tai Yee</Name>  
  <Street>8 Oak Avenue</Street>  
  <City>Old Town</City>  
  <State>PA</State>  
  <Zip>95819</Zip>  
  <Country>USA</Country>  
</Address>  
```  
  
 Beachten Sie, die in diesem Beispiel verwendet die [XML Child Axis-Eigenschaft](../../../../visual-basic/language-reference/xml-axis/xml-child-axis-property.md), die [XML-Attribut Achseneigenschaft](../../../../visual-basic/language-reference/xml-axis/xml-attribute-axis-property.md), und die [XML Value-Eigenschaft](../../../../visual-basic/language-reference/xml-axis/xml-value-property.md).  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird dieselbe Abfrage für XML in einem Namespace gezeigt. Weitere Informationen finden Sie unter [arbeiten mit XML-Namespaces (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/working-with-xml-namespaces.md).  
  
 Dieses Beispiel verwendet die folgende XML-Dokument: [XML-Beispieldatei: Typical Purchase Order in einem Namespace](../../../../visual-basic/programming-guide/concepts/linq/sample-xml-file-typical-purchase-order-in-a-namespace.md).  
  
```vb  
Imports <xmlns:aw='http://www.adventure-works.com'>  
  
Module Module1  
    Sub Main()  
        Dim root As XElement = XElement.Load("PurchaseOrderInNamespace.xml")  
        Dim address As IEnumerable(Of XElement) = _  
            From el In root.<aw:Address> _  
            Where el.@aw:Type = "Billing" _  
            Select el  
        For Each el As XElement In address  
            Console.WriteLine(el)  
        Next  
    End Sub  
End Module  
```  
  
 Dieser Code erzeugt die folgende Ausgabe:  
  
```xml  
<aw:Address aw:Type="Billing" xmlns:aw="http://www.adventure-works.com">  
  <aw:Name>Tai Yee</aw:Name>  
  <aw:Street>8 Oak Avenue</aw:Street>  
  <aw:City>Old Town</aw:City>  
  <aw:State>PA</aw:State>  
  <aw:Zip>95819</aw:Zip>  
  <aw:Country>USA</aw:Country>  
</aw:Address>  
```  
  
## <a name="see-also"></a>Siehe auch  
 <xref:System.Xml.Linq.XElement.Attribute%2A></xref:System.Xml.Linq.XElement.Attribute%2A>   
 <xref:System.Xml.Linq.XContainer.Elements%2A></xref:System.Xml.Linq.XContainer.Elements%2A>   
 [Standardabfragen (LINQ to XML) (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/basic-queries-linq-to-xml.md)   
 [Standard Query Operators Overview (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/standard-query-operators-overview.md)   
 [Projektionsvorgänge (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/projection-operations.md)
