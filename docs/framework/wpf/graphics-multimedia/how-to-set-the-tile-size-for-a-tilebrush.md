---
title: 'Gewusst wie: Festlegen der Flächengröße für ein TileBrush-Objekt'
ms.date: 03/30/2017
helpviewer_keywords:
- TileBrush [WPF], size of tilepropertys
- Viewport property of TileBrush [WPF]
ms.assetid: 04f41090-1b46-4e36-832f-d27d28708b8c
ms.openlocfilehash: e1ba1a25281ffdd1cc00e0bed0efe4f8508780be
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2018
ms.locfileid: "43467834"
---
# <a name="how-to-set-the-tile-size-for-a-tilebrush"></a>Gewusst wie: Festlegen der Flächengröße für ein TileBrush-Objekt
Dieses Beispiel veranschaulicht das Festlegen die Flächengröße für ein <xref:System.Windows.Media.TileBrush>. Standardmäßig eine <xref:System.Windows.Media.TileBrush> erzeugt eine einzelne Kachel, die den Bereich vollständig ausfüllt, die Sie zeichnen werden. Sie können dieses Verhalten überschreiben, indem Sie die Einstellung der <xref:System.Windows.Media.TileBrush.Viewport%2A> und <xref:System.Windows.Media.TileBrush.ViewportUnits%2A> Eigenschaften.  
  
 Die <xref:System.Windows.Media.TileBrush.Viewport%2A> Eigenschaft gibt die Flächengröße für ein <xref:System.Windows.Media.TileBrush>. Standardmäßig wird der Wert des der <xref:System.Windows.Media.TileBrush.Viewport%2A> Eigenschaft ist relativ zur Größe des gezeichneten Bereichs. Vornehmen der <xref:System.Windows.Media.TileBrush.Viewport%2A> Eigenschaft geben Sie eine absolute Flächengröße, legen Sie die <xref:System.Windows.Media.TileBrush.ViewportUnits%2A> Eigenschaft <xref:System.Windows.Media.BrushMappingMode.Absolute>.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird ein <xref:System.Windows.Media.ImageBrush>, einen Typ von <xref:System.Windows.Media.TileBrush>, um ein Rechteck mit Flächen gezeichnet werden soll. In diesem Beispiel werden die Seiten der einzelnen Flächen auf 50 x 50 Prozent der Seiten des Ausgabebereichs (des Rechtecks) festgelegt. Als Ergebnis wird das Rechteck mit vier Projektionen des Bilds gezeichnet.  
  
 In der folgenden Abbildung ist die von diesem Beispiel erstellte Ausgabe dargestellt.
  
 ![Beispiel für die Anordnung mit einem Bildpinsel](../../../../docs/framework/wpf/graphics-multimedia/media/0.png "0")  
  
 [!code-csharp[UsingImageBrush_snip#RelativeTileSizeExample](../../../../samples/snippets/csharp/VS_Snippets_Wpf/UsingImageBrush_snip/CSharp/TileSizeExample.cs#relativetilesizeexample)]  
  
 Im nächsten Beispiel wird erstellt eine <xref:System.Windows.Media.ImageBrush>, legt diese fest seine <xref:System.Windows.Media.TileBrush.Viewport%2A> zu `0,0,25,25` und die zugehörige <xref:System.Windows.Media.TileBrush.ViewportUnits%2A> zu <xref:System.Windows.Media.BrushMappingMode.Absolute>, und verwendet, um ein weiteres Rechteck gezeichnet. Als Ergebnis erzeugt der Pinsel Flächen mit einer Breite und Höhe von 25 Pixeln.  
  
 In der folgenden Abbildung ist die von diesem Beispiel erstellte Ausgabe dargestellt.  
  
 ![Flächen mit einem Viewport von 0,0,0.25,0.25](../../../../docs/framework/wpf/graphics-multimedia/media/25x25viewport.png "25x25viewport")  
  
 [!code-csharp[UsingImageBrush_snip#AbsoluteTileSizeExample](../../../../samples/snippets/csharp/VS_Snippets_Wpf/UsingImageBrush_snip/CSharp/TileSizeExample.cs#absolutetilesizeexample)]  
  
 Die vorangehenden Beispiele sind Teil eines umfangreicheren Beispiels. Das vollständige Beispiel finden Sie unter [Beispiel zu ImageBrush](https://go.microsoft.com/fwlink/?LinkID=160005).  
  
 Obwohl dieses Beispiel verwendet die <xref:System.Windows.Media.ImageBrush> -Klasse, die <xref:System.Windows.Media.TileBrush.Viewport%2A> und <xref:System.Windows.Media.TileBrush.ViewportUnits%2A> Eigenschaften verhalten sich identisch, für die anderen <xref:System.Windows.Media.TileBrush> Objekte, d. h. für <xref:System.Windows.Media.DrawingBrush> und <xref:System.Windows.Media.VisualBrush>. Weitere Informationen zu <xref:System.Windows.Media.ImageBrush> und die andere <xref:System.Windows.Media.TileBrush> Objekten finden Sie [Zeichnen mit Bildern, Zeichnungen und visuellen Elementen](../../../../docs/framework/wpf/graphics-multimedia/painting-with-images-drawings-and-visuals.md).  
  
## <a name="see-also"></a>Siehe auch  
 <xref:System.Windows.Media.TileBrush>  
 [Zeichnen mit Bildern, Zeichnungen und visuellen Elementen](../../../../docs/framework/wpf/graphics-multimedia/painting-with-images-drawings-and-visuals.md)  
 [Erstellen von unterschiedlichen Kachelmustern mit einem TileBrush](../../../../docs/framework/wpf/graphics-multimedia/how-to-create-different-tile-patterns-with-a-tilebrush.md)
