---
title: 'Beispiel XML-Datei: Testkonfiguration in einem Namespace1'
ms.custom: 
ms.date: 2015-07-20
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-csharp
ms.topic: article
dev_langs:
- CSharp
ms.assetid: e75ad1bc-5636-4623-9a34-a286a8c485d6
caps.latest.revision: 3
author: BillWagner
ms.author: wiwagn
translation.priority.mt:
- cs-cz
- pl-pl
- pt-br
- tr-tr
ms.translationtype: HT
ms.sourcegitcommit: 306c608dc7f97594ef6f72ae0f5aaba596c936e1
ms.openlocfilehash: 891616a9327add5671b512cf2d437f61cce947e7
ms.contentlocale: de-de
ms.lasthandoff: 07/28/2017

---
# <a name="sample-xml-file-test-configuration-in-a-namespace"></a><span data-ttu-id="eb7b2-102">Beispiel XML-Datei: Testkonfiguration in einem Namespace</span><span class="sxs-lookup"><span data-stu-id="eb7b2-102">Sample XML File: Test Configuration in a Namespace</span></span>
<span data-ttu-id="eb7b2-103">Die folgende XML-Datei wird in verschiedenen Beispielen in der [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)]-Dokumentation verwendet.</span><span class="sxs-lookup"><span data-stu-id="eb7b2-103">The following XML file is used in various examples in the [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] documentation.</span></span> <span data-ttu-id="eb7b2-104">Dies ist eine Testkonfigurationsdatei.</span><span class="sxs-lookup"><span data-stu-id="eb7b2-104">This is a test configuration file.</span></span> <span data-ttu-id="eb7b2-105">Der XML-Code befindet sich in einem Namespace.</span><span class="sxs-lookup"><span data-stu-id="eb7b2-105">The XML is in a namespace.</span></span>  
  
## <a name="testconfiginnamespacexml"></a><span data-ttu-id="eb7b2-106">TestConfigInNamespace.xml</span><span class="sxs-lookup"><span data-stu-id="eb7b2-106">TestConfigInNamespace.xml</span></span>  
  
```xml  
<?xml version="1.0"?>  
<Tests xmlns="http://www.adatum.com">  
  <Test TestId="0001" TestType="CMD">  
    <Name>Convert number to string</Name>  
    <CommandLine>Examp1.EXE</CommandLine>  
    <Input>1</Input>  
    <Output>One</Output>  
  </Test>  
  <Test TestId="0002" TestType="CMD">  
    <Name>Find succeeding characters</Name>  
    <CommandLine>Examp2.EXE</CommandLine>  
    <Input>abc</Input>  
    <Output>def</Output>  
  </Test>  
  <Test TestId="0003" TestType="GUI">  
    <Name>Convert multiple numbers to strings</Name>  
    <CommandLine>Examp2.EXE /Verbose</CommandLine>  
    <Input>123</Input>  
    <Output>One Two Three</Output>  
  </Test>  
  <Test TestId="0004" TestType="GUI">  
    <Name>Find correlated key</Name>  
    <CommandLine>Examp3.EXE</CommandLine>  
    <Input>a1</Input>  
    <Output>b1</Output>  
  </Test>  
  <Test TestId="0005" TestType="GUI">  
    <Name>Count characters</Name>  
    <CommandLine>FinalExamp.EXE</CommandLine>  
    <Input>This is a test</Input>  
    <Output>14</Output>  
  </Test>  
  <Test TestId="0006" TestType="GUI">  
    <Name>Another Test</Name>  
    <CommandLine>Examp2.EXE</CommandLine>  
    <Input>Test Input</Input>  
    <Output>10</Output>  
  </Test>  
</Tests>  
```  
  
## <a name="see-also"></a><span data-ttu-id="eb7b2-107">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eb7b2-107">See Also</span></span>  
 [<span data-ttu-id="eb7b2-108">XML-Beispieldokumente (LINQ to XML)</span><span class="sxs-lookup"><span data-stu-id="eb7b2-108">Sample XML Documents (LINQ to XML)</span></span>](../../../../csharp/programming-guide/concepts/linq/sample-xml-documents-linq-to-xml.md)

