---
title: x:Array-Markuperweiterung
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-wpf
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- x:Array
- xArray
helpviewer_keywords:
- x:Array [XAML Services]
- XAML [XAML Services], x:Array markup extension
ms.assetid: c5358e14-d24c-44c7-b5eb-6062a4fd981c
caps.latest.revision: "20"
author: wadepickett
ms.author: wpickett
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: bc2304ba68956b705904c72e29a17bdac4536c79
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/22/2017
---
# <a name="xarray-markup-extension"></a><span data-ttu-id="ef9c8-102">x:Array-Markuperweiterung</span><span class="sxs-lookup"><span data-stu-id="ef9c8-102">x:Array Markup Extension</span></span>
<span data-ttu-id="ef9c8-103">Bietet allgemeine Unterstützung für Arrays von Objekten in XAML durch eine Markuperweiterung.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-103">Provides general support for arrays of objects in XAML through a markup extension.</span></span> <span data-ttu-id="ef9c8-104">Dies entspricht der `x:ArrayExtension` XAML-Typ in [MS-XAML].</span><span class="sxs-lookup"><span data-stu-id="ef9c8-104">This corresponds to the `x:ArrayExtension` XAML type in [MS-XAML].</span></span>  
  
## <a name="xaml-object-element-usage"></a><span data-ttu-id="ef9c8-105">Verwendung von XAML-Objektelementen</span><span class="sxs-lookup"><span data-stu-id="ef9c8-105">XAML Object Element Usage</span></span>  
  
```  
<x:Array Type="typeName">  
  arrayContents  
</x:Array>  
```  
  
## <a name="xaml-values"></a><span data-ttu-id="ef9c8-106">XAML-Werte</span><span class="sxs-lookup"><span data-stu-id="ef9c8-106">XAML Values</span></span>  
  
|||  
|-|-|  
|`typeName`|<span data-ttu-id="ef9c8-107">Der Name des Typs, die Ihre `x:Array` enthält.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-107">The name of the type that your `x:Array` will contain.</span></span> <span data-ttu-id="ef9c8-108">`typeName`Möglicherweise hat (und häufig) als Präfix für einen XAML-Namespace, den XAML-Code enthält, Typdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-108">`typeName` may be (and often is) prefixed for a XAML namespace that contains the XAML type definitions.</span></span>|  
|`arrayContents`|<span data-ttu-id="ef9c8-109">Die Elemente Inhalte, die systeminterne Funktion zugewiesen wird `ArrayExtension.Items` Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-109">The items content that is assigned to the intrinsic `ArrayExtension.Items` property.</span></span> <span data-ttu-id="ef9c8-110">Normalerweise werden diese Elemente als eine oder mehrere Objektelemente enthaltenen angegeben die `x:Array` Start- und Endtags.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-110">Typically, these items are specified as one or more object elements contained within the `x:Array` opening and closing tags.</span></span> <span data-ttu-id="ef9c8-111">Objekten angegeben hier voraussichtlich im angegebenen XAML-Typ zugeordnet werden `typeName`.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-111">Objects specified here are expected to be assignable to the XAML type specified in `typeName`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ef9c8-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ef9c8-112">Remarks</span></span>  
 <span data-ttu-id="ef9c8-113">`Type`ist ein erforderliches Attribut für alle `x:Array` Objektelemente.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-113">`Type` is a required attribute for all `x:Array` object elements.</span></span> <span data-ttu-id="ef9c8-114">Ein `Type` Parameterwert muss nicht mit einer `x:Type` Markuperweiterung; der kurze Name des Typs ist ein XAML-Typ, der als Zeichenfolge angegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-114">A `Type` parameter value does not need to use an `x:Type` markup extension; the short name of the type is   a XAML type, which can be specified as a string.</span></span>  
  
 <span data-ttu-id="ef9c8-115">In der .NET Framework-XAML-Dienste-Implementierung, die die Beziehung zwischen der Verwendung von XAML-Typ der Eingabe und die Ausgabe CLR <xref:System.Type> der das erstellte Array von Dienstkontext für Markuperweiterungen beeinflusst wird.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-115">In the .NET Framework XAML Services implementation, the relationship between the input XAML type and the output CLR <xref:System.Type> of the created array is influenced by service context for markup extensions.</span></span> <span data-ttu-id="ef9c8-116">Die Ausgabe <xref:System.Type> ist die <xref:System.Xaml.XamlType.UnderlyingType%2A> von der Verwendung von XAML-Typ der Eingabe, nach der Suche nach den erforderlichen <xref:System.Xaml.XamlType> basierend auf XAML-Schemakontext und der <xref:System.Windows.Markup.IXamlTypeResolver> Dienst, der den Kontext bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-116">The output <xref:System.Type> is the <xref:System.Xaml.XamlType.UnderlyingType%2A> of the input XAML type, after looking up the necessary <xref:System.Xaml.XamlType> based on XAML schema context and the <xref:System.Windows.Markup.IXamlTypeResolver> service the context provides.</span></span>  
  
 <span data-ttu-id="ef9c8-117">Bei der Verarbeitung der Arrayinhalt zugewiesen sind die `ArrayExtension.Items` systeminterne-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-117">When processed, the array contents are assigned to the `ArrayExtension.Items` intrinsic property.</span></span> <span data-ttu-id="ef9c8-118">In der <xref:System.Windows.Markup.ArrayExtension> -Implementierung wird dies durch <xref:System.Windows.Markup.ArrayExtension.Items%2A?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-118">In the <xref:System.Windows.Markup.ArrayExtension> implementation, this is represented by <xref:System.Windows.Markup.ArrayExtension.Items%2A?displayProperty=nameWithType>.</span></span>  
  
 <span data-ttu-id="ef9c8-119">In der .NET Framework-XAML-Dienste-Implementierung wird durch die Verarbeitung für diese Markuperweiterung definiert die <xref:System.Windows.Markup.ArrayExtension> Klasse.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-119">In the .NET Framework XAML Services implementation, the handling for this markup extension is defined by the <xref:System.Windows.Markup.ArrayExtension> class.</span></span> <span data-ttu-id="ef9c8-120"><xref:System.Windows.Markup.ArrayExtension>ist nicht versiegelt und kann als Grundlage für eine Markuperweiterungsimplementierung für einen benutzerdefinierten Arraytyp verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-120"><xref:System.Windows.Markup.ArrayExtension> is not sealed, and could be used as the basis for a markup extension implementation for a custom array type.</span></span>  
  
 <span data-ttu-id="ef9c8-121">`x:Array`Weitere Sprache Erweiterbarkeit in XAML für allgemeine vorgesehen ist.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-121">`x:Array` is more intended for general language extensibility in XAML.</span></span> <span data-ttu-id="ef9c8-122">Aber `x:Array` kann auch zum Angeben der Verwendung von XAML-Werte mancher Eigenschaften, die XAML unterstützt Auflistungen als ihren Inhalt strukturierte Eigenschaft akzeptieren nützlich sein.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-122">But `x:Array` can also be useful for specifying XAML values of certain properties that take XAML-supported collections as their structured property content.</span></span> <span data-ttu-id="ef9c8-123">Beispielsweise können Sie angeben, den Inhalt des ein <xref:System.Collections.IEnumerable> Eigenschaft mit einer `x:Array` Verwendung.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-123">For example, you could specify the contents of an <xref:System.Collections.IEnumerable> property with an `x:Array` usage.</span></span>  
  
 <span data-ttu-id="ef9c8-124">`x:Array` ist eine Markuperweiterung.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-124">`x:Array` is a markup extension.</span></span> <span data-ttu-id="ef9c8-125">Markuperweiterungen werden in der Regel implementiert, wenn Attributwerte mit Escapezeichen versehen werden müssen, damit diese nicht als literale Werte oder als Handlernamen betrachtet werden, und diese Anforderung eher global und nicht nur durch den Einsatz von Typkonvertern für bestimmte Typen oder Eigenschaften erfüllt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-125">Markup extensions are typically implemented when there is a requirement to escape attribute values to be other than literal values or handler names, and the requirement is more global than just putting type converters on certain types or properties.</span></span> <span data-ttu-id="ef9c8-126">`x:Array`ist teilweise eine Ausnahme von dieser Regel, da statt alternatives Attribut-Wert-Behandlung `x:Array` alternative Behandlung des inneren Textinhalts enthält.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-126">`x:Array` is partially an exception to that rule because instead of providing alternative attribute value handling, `x:Array` provides alternative handling of its inner text content.</span></span> <span data-ttu-id="ef9c8-127">Dieses Verhalten ermöglicht die Typen, die von einer vorhandenen Inhaltsmodell in einem Array gruppiert werden und später im Code-Behind verwiesen wird, durch den Zugriff auf das benannte Array nicht unterstützt werden können. Sie können Aufrufen <xref:System.Array> Methoden, um einzelne Arrayelemente abzurufen.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-127">This behavior enables types that might not be supported by an existing content model to be grouped into an array and referenced later in code-behind by accessing the named array; you can call <xref:System.Array> methods to get individual array items.</span></span>  
  
 <span data-ttu-id="ef9c8-128">Alle Markuperweiterungen in XAML verwenden Sie die geschweiften Klammern ({,}`)` in der Attributsyntax, also die Konvention, die mit dem ein XAML-Prozessor erkennt, dass eine Markuperweiterung den Attributwert verarbeiten muss.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-128">All markup extensions in XAML use the braces ({,}`)` in their attribute syntax, which is the convention by which a XAML processor recognizes that a markup extension must process the attribute value.</span></span> <span data-ttu-id="ef9c8-129">Weitere Informationen über Markuperweiterungen finden Sie unter [Typkonverter und Markuperweiterungen für XAML](../../../docs/framework/xaml-services/type-converters-and-markup-extensions-for-xaml.md).</span><span class="sxs-lookup"><span data-stu-id="ef9c8-129">For more information about markup extensions in general, see [Type Converters and Markup Extensions for XAML](../../../docs/framework/xaml-services/type-converters-and-markup-extensions-for-xaml.md).</span></span>  
  
 <span data-ttu-id="ef9c8-130">In XAML 2009 `x:Array` als Sprachprimitive anstelle einer Markuperweiterung definiert ist.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-130">In XAML 2009, `x:Array` is defined as a language primitive instead of a markup extension.</span></span> <span data-ttu-id="ef9c8-131">Weitere Informationen finden Sie unter [integrierte Typen für häufige XAML-Sprachprimitive](../../../docs/framework/xaml-services/built-in-types-for-common-xaml-language-primitives.md).</span><span class="sxs-lookup"><span data-stu-id="ef9c8-131">For more information, see [Built-in Types for Common XAML Language Primitives](../../../docs/framework/xaml-services/built-in-types-for-common-xaml-language-primitives.md).</span></span>  
  
## <a name="wpf-usage-notes"></a><span data-ttu-id="ef9c8-132">Hinweise zur WPF-Verwendung</span><span class="sxs-lookup"><span data-stu-id="ef9c8-132">WPF Usage Notes</span></span>  
 <span data-ttu-id="ef9c8-133">In der Regel die Objektelemente, die Auffüllen einer `x:Array` sind keine Elemente, die in der [!INCLUDE[TLA2#tla_winclient](../../../includes/tla2sharptla-winclient-md.md)] XAML-Namespace und erfordern eine/Präfix-Zuordnung zu einem nicht standardmäßigen XAML-Namespace.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-133">Typically, the object elements that populate an `x:Array` are not elements that exist in the [!INCLUDE[TLA2#tla_winclient](../../../includes/tla2sharptla-winclient-md.md)] XAML namespace, and require a prefix mapping to a non-default XAML namespace.</span></span>  
  
 <span data-ttu-id="ef9c8-134">Im folgenden ist beispielsweise ein einfaches Array von zwei Zeichenfolgen mit der `sys` Präfix (und auch `x`) auf der Ebene des Arrays definiert.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-134">For example, the following is a simple array of two strings, with the `sys` prefix (and also `x`) defined at the level of the array.</span></span>  
  
 <span data-ttu-id="ef9c8-135">[xaml]</span><span class="sxs-lookup"><span data-stu-id="ef9c8-135">[xaml]</span></span>  
  
 `<x:Array Type="sys:String" xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"`  
  
 `xmlns:sys="clr-namespace:System;assembly=mscorlib">`  
  
 `<sys:String>Hello</sys:String>`  
  
 `<sys:String>World</sys:String>`  
  
 `</x:Array>`  
  
 <span data-ttu-id="ef9c8-136">Für benutzerdefinierte Typen, die als Elemente des Arrays verwendet werden, muss die Klasse auch die Anforderungen für die in XAML instanziiert wird, die als Objektelemente unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ef9c8-136">For custom types that are used as array elements, the class must also support the requirements for being instantiated in XAML as object elements.</span></span> <span data-ttu-id="ef9c8-137">Weitere Informationen finden Sie unter [XAML und benutzerdefinierte Klassen für WPF](../../../docs/framework/wpf/advanced/xaml-and-custom-classes-for-wpf.md).</span><span class="sxs-lookup"><span data-stu-id="ef9c8-137">For more information, see [XAML and Custom Classes for WPF](../../../docs/framework/wpf/advanced/xaml-and-custom-classes-for-wpf.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ef9c8-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ef9c8-138">See Also</span></span>  
 [<span data-ttu-id="ef9c8-139">Markuperweiterungen und WPF-XAML</span><span class="sxs-lookup"><span data-stu-id="ef9c8-139">Markup Extensions and WPF XAML</span></span>](../../../docs/framework/wpf/advanced/markup-extensions-and-wpf-xaml.md)  
 [<span data-ttu-id="ef9c8-140">Aus WPF zu System.Xaml migrierte Typen</span><span class="sxs-lookup"><span data-stu-id="ef9c8-140">Types Migrated from WPF to System.Xaml</span></span>](../../../docs/framework/xaml-services/types-migrated-from-wpf-to-system-xaml.md)
