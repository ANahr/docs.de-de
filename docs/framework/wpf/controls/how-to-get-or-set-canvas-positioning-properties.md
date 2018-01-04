---
title: 'Gewusst wie: Abrufen und Festlegen von Canvas-Positionierungseigenschaften'
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-wpf
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- csharp
- vb
helpviewer_keywords: Canvas control [WPF], setting positioning properties
ms.assetid: 1636b950-2b5a-4507-8a10-c5034cc58b1c
caps.latest.revision: "10"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: d2b01657088c388ad09037716278dc0788de2abb
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/22/2017
---
# <a name="how-to-get-or-set-canvas-positioning-properties"></a><span data-ttu-id="3efb0-102">Gewusst wie: Abrufen und Festlegen von Canvas-Positionierungseigenschaften</span><span class="sxs-lookup"><span data-stu-id="3efb0-102">How to: Get or Set Canvas Positioning Properties</span></span>
<span data-ttu-id="3efb0-103">Dieses Beispiel zeigt, wie die Positionierung Methoden die <xref:System.Windows.Controls.Canvas> Element des untergeordneten Inhalts zu positionieren.</span><span class="sxs-lookup"><span data-stu-id="3efb0-103">This example shows how to use the positioning methods of the <xref:System.Windows.Controls.Canvas> element to position child content.</span></span> <span data-ttu-id="3efb0-104">In diesem Beispiel verwendet den Inhalt in einen <xref:System.Windows.Controls.ListBoxItem> zur Darstellung Werte positionieren und konvertiert die Werte in Instanzen von <xref:System.Double>, dies ist ein erforderliches Argument für die Positionierung.</span><span class="sxs-lookup"><span data-stu-id="3efb0-104">This example uses content in a <xref:System.Windows.Controls.ListBoxItem> to represent positioning values and converts the values into instances of <xref:System.Double>, which is a required argument for positioning.</span></span> <span data-ttu-id="3efb0-105">Die Werte sind dann wieder in Zeichenfolgen konvertiert und als Text im angezeigt ein <xref:System.Windows.Controls.TextBlock> -Element mithilfe der <xref:System.Windows.Controls.Canvas.GetLeft%2A> Methode.</span><span class="sxs-lookup"><span data-stu-id="3efb0-105">The values are then converted back into strings and displayed as text in a <xref:System.Windows.Controls.TextBlock> element by using the <xref:System.Windows.Controls.Canvas.GetLeft%2A> method.</span></span>  
  
## <a name="example"></a><span data-ttu-id="3efb0-106">Beispiel</span><span class="sxs-lookup"><span data-stu-id="3efb0-106">Example</span></span>  
 <span data-ttu-id="3efb0-107">Das folgende Beispiel erstellt eine <xref:System.Windows.Controls.ListBox> Element, das elf auswählbare hat <xref:System.Windows.Controls.ListBoxItem> Elemente.</span><span class="sxs-lookup"><span data-stu-id="3efb0-107">The following example creates a <xref:System.Windows.Controls.ListBox> element that has eleven selectable <xref:System.Windows.Controls.ListBoxItem> elements.</span></span> <span data-ttu-id="3efb0-108">Die <xref:System.Windows.Controls.Primitives.Selector.SelectionChanged> Ereignistriggern der `ChangeLeft` benutzerdefinierte Methode, die im nachfolgenden Codeblock definiert.</span><span class="sxs-lookup"><span data-stu-id="3efb0-108">The <xref:System.Windows.Controls.Primitives.Selector.SelectionChanged> event triggers the `ChangeLeft` custom method, which the subsequent code block defines.</span></span>  
  
 <span data-ttu-id="3efb0-109">Jedes <xref:System.Windows.Controls.ListBoxItem> stellt eine <xref:System.Double> Wert, der eines der Argumente ist, der <xref:System.Windows.Controls.Canvas.SetLeft%2A> Methode <xref:System.Windows.Controls.Canvas> akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="3efb0-109">Each <xref:System.Windows.Controls.ListBoxItem> represents a <xref:System.Double> value, which is one of the arguments that the <xref:System.Windows.Controls.Canvas.SetLeft%2A> method of <xref:System.Windows.Controls.Canvas> accepts.</span></span> <span data-ttu-id="3efb0-110">Zum Verwenden einer <xref:System.Windows.Controls.ListBoxItem> zur Darstellung einer Instanz von <xref:System.Double>, müssen Sie zuerst Konvertieren der <xref:System.Windows.Controls.ListBoxItem> in den richtigen Datentyp.</span><span class="sxs-lookup"><span data-stu-id="3efb0-110">In order to use a <xref:System.Windows.Controls.ListBoxItem> to represent an instance of <xref:System.Double>, you must first convert the <xref:System.Windows.Controls.ListBoxItem> to the correct data type.</span></span>  
  
 [!code-xaml[CanvasPositioningProperties#1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/CanvasPositioningProperties/CSharp/Window1.xaml#1)]  
  
 <span data-ttu-id="3efb0-111">Wenn ein Benutzer ändert die <xref:System.Windows.Controls.ListBox> Auswahl, ruft der `ChangeLeft` benutzerdefinierte Methode.</span><span class="sxs-lookup"><span data-stu-id="3efb0-111">When a user changes the <xref:System.Windows.Controls.ListBox> selection, it invokes the `ChangeLeft` custom method.</span></span> <span data-ttu-id="3efb0-112">Diese Methode übergibt der <xref:System.Windows.Controls.ListBoxItem> auf eine <xref:System.Windows.LengthConverter> -Objekt, das konvertiert die <xref:System.Windows.Controls.ContentControl.Content%2A> des eine <xref:System.Windows.Controls.ListBoxItem> mit einer Instanz von <xref:System.Double> (Beachten Sie, das diesen Wert auf bereits konvertiert wurde eine <xref:System.String> mithilfe der <xref:System.Windows.Controls.Control.ToString%2A> die Methode).</span><span class="sxs-lookup"><span data-stu-id="3efb0-112">This method passes the <xref:System.Windows.Controls.ListBoxItem> to a <xref:System.Windows.LengthConverter> object, which converts the <xref:System.Windows.Controls.ContentControl.Content%2A> of a <xref:System.Windows.Controls.ListBoxItem> to an instance of <xref:System.Double> (notice that this value has already been converted to a <xref:System.String> by using the <xref:System.Windows.Controls.Control.ToString%2A> method).</span></span> <span data-ttu-id="3efb0-113">Dieser Wert wird dann zurück zum Übergeben der <xref:System.Windows.Controls.Canvas.SetLeft%2A> und <xref:System.Windows.Controls.Canvas.GetLeft%2A> Methoden der <xref:System.Windows.Controls.Canvas> damit ändern Sie die Position von der `text1` Objekt.</span><span class="sxs-lookup"><span data-stu-id="3efb0-113">This value is then passed back to the <xref:System.Windows.Controls.Canvas.SetLeft%2A> and <xref:System.Windows.Controls.Canvas.GetLeft%2A> methods of <xref:System.Windows.Controls.Canvas> in order to change the position of the `text1` object.</span></span>  
  
 [!code-csharp[CanvasPositioningProperties#2](../../../../samples/snippets/csharp/VS_Snippets_Wpf/CanvasPositioningProperties/CSharp/Window1.xaml.cs#2)]
 [!code-vb[CanvasPositioningProperties#2](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/CanvasPositioningProperties/VisualBasic/Window1.xaml.vb#2)]  
  
## <a name="see-also"></a><span data-ttu-id="3efb0-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3efb0-114">See Also</span></span>  
 <xref:System.Windows.Controls.Canvas>  
 <xref:System.Windows.Controls.ListBoxItem>  
 <xref:System.Windows.LengthConverter>  
 [<span data-ttu-id="3efb0-115">Übersicht über Panel-Elemente</span><span class="sxs-lookup"><span data-stu-id="3efb0-115">Panels Overview</span></span>](../../../../docs/framework/wpf/controls/panels-overview.md)
