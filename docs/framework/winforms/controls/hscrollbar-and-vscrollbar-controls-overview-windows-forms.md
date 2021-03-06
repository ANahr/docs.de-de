---
title: Übersicht über das HScrollBar-Steuerelement und das VScrollBar-Steuerelement (Windows Forms)
ms.date: 03/30/2017
f1_keywords:
- HScrollBar
- VScrollBar
helpviewer_keywords:
- ScrollBar control [Windows Forms]
- HScrollBar control [Windows Forms], about HScrollBar
- VScrollBar control [Windows Forms], about VScrollBar control
- ScrollBar control [Windows Forms], about ScrollBar control
- scroll bars [Windows Forms], about scroll bars
ms.assetid: 8b307679-1cae-41d8-99aa-3d1efd207cd6
ms.openlocfilehash: 2c6436e77753322733580acba5a20d6bb220f29c
ms.sourcegitcommit: ad99773e5e45068ce03b99518008397e1299e0d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2018
ms.locfileid: "46711089"
---
# <a name="hscrollbar-and-vscrollbar-controls-overview-windows-forms"></a>Übersicht über das HScrollBar-Steuerelement und das VScrollBar-Steuerelement (Windows Forms)
Windows Forms <xref:System.Windows.Forms.ScrollBar> Steuerelemente werden verwendet, um die einfache Navigation durch eine lange Liste von Elementen oder eine große Menge an Informationen horizontale oder vertikale innerhalb einer Anwendung oder eines Steuerelements angeben. Bildlaufleisten sind ein häufiges Element der Windows-Schnittstelle, sodass die <xref:System.Windows.Forms.ScrollBar> -Steuerelement wird häufig verwendet, mit Steuerelementen, die nicht von abgeleitet sind die <xref:System.Windows.Forms.ScrollableControl> Klasse. Viele Entwickler entscheiden sich auf ähnliche Weise integriert die <xref:System.Windows.Forms.ScrollBar> gesteuert werden, wenn ihre eigenen Benutzersteuerelemente zu erstellen.  
  
 Die <xref:System.Windows.Forms.HScrollBar> (horizontal) und <xref:System.Windows.Forms.VScrollBar> (vertikal) funktionieren Sie unabhängig von anderen Steuerelementen und verfügen über ihren eigenen Satz von Ereignissen, Eigenschaften und Methoden. <xref:System.Windows.Forms.ScrollBar> Steuerelemente sind nicht identisch mit den integrierten Bildlaufleisten, die Inhalt der Textfelder, Listenfelder, Kombinationsfelder oder MDI-Formularen zugeordnet sind (die <xref:System.Windows.Forms.TextBox> Steuerelement verfügt über eine <xref:System.Windows.Forms.TextBox.ScrollBars%2A> -Eigenschaft zum Anzeigen oder Ausblenden von Bildlaufleisten, die dem Steuerelement zugeordnet sind).  
  
 Die <xref:System.Windows.Forms.ScrollBar> steuert die Verwendung der <xref:System.Windows.Forms.ScrollBar.Scroll> Ereignis zum Überwachen von des Verschieben des Bildlauffelds (auch als Ziehpunkt bezeichnet) auf der Bildlaufleiste. Mithilfe der <xref:System.Windows.Forms.ScrollBar.Scroll> Ereignis ermöglicht den Zugriff auf den Wert der Bildlauf aus, wie es gezogen wird.  
  
## <a name="value-property"></a>Value-Eigenschaft  
 Die <xref:System.Windows.Forms.ScrollBar.Value%2A> -Eigenschaft (die Standardeinstellung 0 ist) ist ein `integer` Wert, der die Position des Bildlauffelds auf der Bildlaufleiste. Wenn die Position des Bildlauffelds auf der minimale Wert ist, verschiebt ihn auf die linke Position (für horizontale Scrollleisten) oder die obere Position (für vertikale Bildlaufleisten). Wenn das Bildlauffeld auf der maximale Wert, der verschoben, der die äußerste rechte oder die untere Position ist. Ein Wert in der Mitte zwischen dem unteren und oberen Ende des Bereichs platziert die führenden Rands des Bildlauffelds in der Mitte der Bildlaufleiste.  
  
 Zusätzlich zur Verwendung von Mausklicks, den Wert des Scroll-Leiste ändern, kann Benutzer auch das Bildlauffeld an einem beliebigen Punkt auf der Leiste ziehen. Der resultierende Wert hängt von der Position des Bildlauffelds, aber es ist immer innerhalb des Bereichs von der <xref:System.Windows.Forms.ScrollBar.Minimum%2A> zu <xref:System.Windows.Forms.ScrollBar.Maximum%2A> Eigenschaften, die vom Benutzer festgelegt wird.  
  
## <a name="largechange-and-smallchange-properties"></a>LargeChange und SmallChange-Eigenschaften  
 Wenn der Benutzer die Bild-auf oder Bild-ab-Taste drückt oder in der Schiebeleiste auf beiden Seiten des Bildlauffelds, klickt auf die <xref:System.Windows.Forms.ScrollBar.Value%2A> eigenschaftenänderungen entsprechend dem Wert, legen Sie in der <xref:System.Windows.Forms.ScrollBar.LargeChange%2A> Eigenschaft.  
  
 Tasten, oder auf eine der Schaltflächen der Bildlaufleiste, wenn der Benutzer eine der Pfeiltasten drückt die <xref:System.Windows.Forms.ScrollBar.Value%2A> eigenschaftenänderungen entsprechend dem Wert, legen Sie in der <xref:System.Windows.Forms.ScrollBar.SmallChange%2A> Eigenschaft.  
  
## <a name="see-also"></a>Siehe auch  
 <xref:System.Windows.Forms.HScrollBar>  
 <xref:System.Windows.Forms.VScrollBar>  
 [Ergänzungen zu Windows Forms für .NET Framework 2.0](https://msdn.microsoft.com/library/c61a923d-3d6a-4c8c-820c-e94c83f3f9a8)  
 [Windows Forms-Steuerelemente](../../../../docs/framework/winforms/controls/controls-to-use-on-windows-forms.md)
