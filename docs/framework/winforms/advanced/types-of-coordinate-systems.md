---
title: Typen von Koordinatensystemen
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-winforms
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- csharp
- vb
helpviewer_keywords:
- transformations [Windows Forms], page
- unit of measure
- world coordinate system
- page coordinate system
- page transformation
- device coordinate system
- world transformation
- coordinate systems
- transformations [Windows Forms], world
ms.assetid: c61ff50a-eb1d-4e6c-83cd-f7e9764cfa9f
caps.latest.revision: "15"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 287b1c9eddef882041d9e4eac44a06190f3585a4
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/22/2017
---
# <a name="types-of-coordinate-systems"></a><span data-ttu-id="37f0f-102">Typen von Koordinatensystemen</span><span class="sxs-lookup"><span data-stu-id="37f0f-102">Types of Coordinate Systems</span></span>
[!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)]<span data-ttu-id="37f0f-103">verwendet drei Koordinatensysteme: Global, Seite und Gerät.</span><span class="sxs-lookup"><span data-stu-id="37f0f-103"> uses three coordinate spaces: world, page, and device.</span></span> <span data-ttu-id="37f0f-104">Globalen Koordinaten sind die Koordinaten verwendet, um eine bestimmte Grafik World modellieren und die Koordinaten, die Sie an Methoden in .NET Framework zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="37f0f-104">World coordinates are the coordinates used to model a particular graphic world and are the coordinates you pass to methods in the .NET Framework.</span></span> <span data-ttu-id="37f0f-105">Seitenkoordinaten beziehen sich auf das Koordinatensystem, die von einer Zeichenoberfläche, z. B. eines Formulars oder Steuerelements verwendet.</span><span class="sxs-lookup"><span data-stu-id="37f0f-105">Page coordinates refer to the coordinate system used by a drawing surface, such as a form or control.</span></span> <span data-ttu-id="37f0f-106">Gerätekoordinaten sind die Koordinaten, die durch das physische Gerät, z. B. einem Bildschirm oder Blatt Papier gezeichnet werden verwendet.</span><span class="sxs-lookup"><span data-stu-id="37f0f-106">Device coordinates are the coordinates used by the physical device being drawn on, such as a screen or sheet of paper.</span></span> <span data-ttu-id="37f0f-107">Stellen Sie, wenn den Aufruf `myGraphics.DrawLine(myPen, 0, 0, 160, 80)`, die Punkte, die Sie zum Übergeben der <xref:System.Drawing.Graphics.DrawLine%2A> Methode –`(0, 0)` und `(160, 80)`– befinden sich in der ganzen Welt Koordinatenbereich.</span><span class="sxs-lookup"><span data-stu-id="37f0f-107">When you make the call `myGraphics.DrawLine(myPen, 0, 0, 160, 80)`, the points that you pass to the <xref:System.Drawing.Graphics.DrawLine%2A> method—`(0, 0)` and `(160, 80)`—are in the world coordinate space.</span></span> <span data-ttu-id="37f0f-108">Vor dem [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] können die Linie auf dem Bildschirm, durchlaufen die Koordinaten auf eine Sequenz von Transformationen.</span><span class="sxs-lookup"><span data-stu-id="37f0f-108">Before [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] can draw the line on the screen, the coordinates pass through a sequence of transformations.</span></span> <span data-ttu-id="37f0f-109">Eine Transformation, die die globale Transformation aufgerufen globalen Koordinaten Seitenkoordinaten konvertiert und eine andere Transformation, die Seitentransformation aufgerufen konvertiert Seitenkoordinaten in logische Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="37f0f-109">One transformation, called the world transformation, converts world coordinates to page coordinates, and another transformation, called the page transformation, converts page coordinates to device coordinates.</span></span>  
  
## <a name="transforms-and-coordinate-systems"></a><span data-ttu-id="37f0f-110">Transformationen und Koordinatensysteme</span><span class="sxs-lookup"><span data-stu-id="37f0f-110">Transforms and Coordinate Systems</span></span>  
 <span data-ttu-id="37f0f-111">Angenommen Sie, Sie arbeiten mit einem Koordinatensystem, die seinen Ursprung im Text des Clientbereichs statt in der oberen linken Ecke hat möchten.</span><span class="sxs-lookup"><span data-stu-id="37f0f-111">Suppose you want to work with a coordinate system that has its origin in the body of the client area rather than the upper-left corner.</span></span> <span data-ttu-id="37f0f-112">Nehmen Sie z. B., den Ursprung 100 Pixel vom linken Rand des Clientbereichs und 50 Pixel vom oberen Rand des Clientbereichs sein soll.</span><span class="sxs-lookup"><span data-stu-id="37f0f-112">Say, for example, that you want the origin to be 100 pixels from the left edge of the client area and 50 pixels from the top of the client area.</span></span> <span data-ttu-id="37f0f-113">Die folgende Abbildung zeigt eine solche einem Koordinatensystem.</span><span class="sxs-lookup"><span data-stu-id="37f0f-113">The following illustration shows such a coordinate system.</span></span>  
  
 <span data-ttu-id="37f0f-114">![Koordinatensystem](../../../../docs/framework/winforms/advanced/media/aboutgdip05-art01.gif "AboutGdip05_art01")</span><span class="sxs-lookup"><span data-stu-id="37f0f-114">![Coordinate System](../../../../docs/framework/winforms/advanced/media/aboutgdip05-art01.gif "AboutGdip05_art01")</span></span>  
  
 <span data-ttu-id="37f0f-115">Stellen Sie, wenn den Aufruf `myGraphics.DrawLine(myPen, 0, 0, 160, 80)`, erhalten Sie die Zeile in der folgenden Abbildung gezeigt.</span><span class="sxs-lookup"><span data-stu-id="37f0f-115">When you make the call `myGraphics.DrawLine(myPen, 0, 0, 160, 80)`, you get the line shown in the following illustration.</span></span>  
  
 <span data-ttu-id="37f0f-116">![Koordinatensystem](../../../../docs/framework/winforms/advanced/media/aboutgdip05-art02.gif "AboutGdip05_art02")</span><span class="sxs-lookup"><span data-stu-id="37f0f-116">![Coordinate System](../../../../docs/framework/winforms/advanced/media/aboutgdip05-art02.gif "AboutGdip05_art02")</span></span>  
  
 <span data-ttu-id="37f0f-117">Die Koordinaten der Endpunkte der Linie in den drei Koordinatensystemen lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="37f0f-117">The coordinates of the endpoints of your line in the three coordinate spaces are as follows:</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="37f0f-118">World</span><span class="sxs-lookup"><span data-stu-id="37f0f-118">World</span></span>|<span data-ttu-id="37f0f-119">(0, 0), (160, 80)</span><span class="sxs-lookup"><span data-stu-id="37f0f-119">(0, 0) to (160, 80)</span></span>|  
|<span data-ttu-id="37f0f-120">Seite</span><span class="sxs-lookup"><span data-stu-id="37f0f-120">Page</span></span>|<span data-ttu-id="37f0f-121">(100, 50), (260, 130)</span><span class="sxs-lookup"><span data-stu-id="37f0f-121">(100, 50) to (260, 130)</span></span>|  
|<span data-ttu-id="37f0f-122">Gerät</span><span class="sxs-lookup"><span data-stu-id="37f0f-122">Device</span></span>|<span data-ttu-id="37f0f-123">(100, 50), (260, 130)</span><span class="sxs-lookup"><span data-stu-id="37f0f-123">(100, 50) to (260, 130)</span></span>|  
  
 <span data-ttu-id="37f0f-124">Beachten Sie, dass die Seite Koordinatenbereich auf der linken oberen Ecke des Clientbereichs Ursprungssite verfügt; Dies wird immer der Fall sein.</span><span class="sxs-lookup"><span data-stu-id="37f0f-124">Note that the page coordinate space has its origin at the upper-left corner of the client area; this will always be the case.</span></span> <span data-ttu-id="37f0f-125">Beachten Sie außerdem, da die Maßeinheit Pixel ist, die Gerätekoordinaten der Seitenkoordinaten identisch sind.</span><span class="sxs-lookup"><span data-stu-id="37f0f-125">Also note that because the unit of measure is the pixel, the device coordinates are the same as the page coordinates.</span></span> <span data-ttu-id="37f0f-126">Wenn Sie die Maßeinheit auf einen anderen Wert als Pixel (z. B. Zoll) festlegen, werden die Gerätekoordinaten mit den Seitenkoordinaten abweichen.</span><span class="sxs-lookup"><span data-stu-id="37f0f-126">If you set the unit of measure to something other than pixels (for example, inches), then the device coordinates will be different from the page coordinates.</span></span>  
  
 <span data-ttu-id="37f0f-127">Die globale Transformation, die globalen Koordinaten Seitenkoordinaten zuordnet, gehalten wird, der <xref:System.Drawing.Graphics.Transform%2A> Eigenschaft von der <xref:System.Drawing.Graphics> Klasse.</span><span class="sxs-lookup"><span data-stu-id="37f0f-127">The world transformation, which maps world coordinates to page coordinates, is held in the <xref:System.Drawing.Graphics.Transform%2A> property of the <xref:System.Drawing.Graphics> class.</span></span> <span data-ttu-id="37f0f-128">Im vorherigen Beispiel wird die globale Transformation 100 Übersetzungseinheiten in X-Richtung und 50 Einheiten entlang der y-Achse an.</span><span class="sxs-lookup"><span data-stu-id="37f0f-128">In the preceding example, the world transformation is a translation 100 units in the x direction and 50 units in the y direction.</span></span> <span data-ttu-id="37f0f-129">Im folgenden Beispiel wird die globale Transformation für eine <xref:System.Drawing.Graphics> Objekt, und klicken Sie dann verwendet, die <xref:System.Drawing.Graphics> Objekt zum Zeichnen der Linie, die in der obigen Abbildung gezeigt:</span><span class="sxs-lookup"><span data-stu-id="37f0f-129">The following example sets the world transformation of a <xref:System.Drawing.Graphics> object and then uses that <xref:System.Drawing.Graphics> object to draw the line shown in the preceding figure:</span></span>  
  
 [!code-csharp[System.Drawing.CoordinateSystems#31](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.CoordinateSystems/CS/Class1.cs#31)]
 [!code-vb[System.Drawing.CoordinateSystems#31](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.CoordinateSystems/VB/Class1.vb#31)]  
  
 <span data-ttu-id="37f0f-130">Die Seitentransformation ordnet Seitenkoordinaten Gerätekoordinaten.</span><span class="sxs-lookup"><span data-stu-id="37f0f-130">The page transformation maps page coordinates to device coordinates.</span></span> <span data-ttu-id="37f0f-131">Die <xref:System.Drawing.Graphics> -Klasse stellt die <xref:System.Drawing.Graphics.PageUnit%2A> und <xref:System.Drawing.Graphics.PageScale%2A> Eigenschaften zum Bearbeiten der Seitentransformation.</span><span class="sxs-lookup"><span data-stu-id="37f0f-131">The <xref:System.Drawing.Graphics> class provides the <xref:System.Drawing.Graphics.PageUnit%2A> and <xref:System.Drawing.Graphics.PageScale%2A> properties for manipulating the page transformation.</span></span> <span data-ttu-id="37f0f-132">Die <xref:System.Drawing.Graphics> Klasse bietet auch zwei schreibgeschützte Eigenschaften <xref:System.Drawing.Graphics.DpiX%2A> und <xref:System.Drawing.Graphics.DpiY%2A>, untersuchen Sie die horizontalen und vertikalen Punkte pro Zoll des Geräts angezeigt.</span><span class="sxs-lookup"><span data-stu-id="37f0f-132">The <xref:System.Drawing.Graphics> class also provides two read-only properties, <xref:System.Drawing.Graphics.DpiX%2A> and <xref:System.Drawing.Graphics.DpiY%2A>, for examining the horizontal and vertical dots per inch of the display device.</span></span>  
  
 <span data-ttu-id="37f0f-133">Können Sie die <xref:System.Drawing.Graphics.PageUnit%2A> Eigenschaft von der <xref:System.Drawing.Graphics> Klasse, um eine Maßeinheit als Pixel anzugeben.</span><span class="sxs-lookup"><span data-stu-id="37f0f-133">You can use the <xref:System.Drawing.Graphics.PageUnit%2A> property of the <xref:System.Drawing.Graphics> class to specify a unit of measure other than the pixel.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="37f0f-134">Kann nicht festgelegt werden die <xref:System.Drawing.Graphics.PageUnit%2A> Eigenschaft <xref:System.Drawing.GraphicsUnit.World>, wie dies eine physische fehlereinheit ist und wird eine Ausnahme ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="37f0f-134">You cannot set the <xref:System.Drawing.Graphics.PageUnit%2A> property to <xref:System.Drawing.GraphicsUnit.World>, as this is not a physical unit and will cause an exception.</span></span>  
  
 <span data-ttu-id="37f0f-135">Im folgende Beispiel zeichnet eine verbindende Linie aus (0, 0), (2, 1), in dem der Punkt (2, 1) 2 Zoll rechts und 1 Zoll nach unten ab dem Punkt (0, 0) ist:</span><span class="sxs-lookup"><span data-stu-id="37f0f-135">The following example draws a line from (0, 0) to (2, 1), where the point (2, 1) is 2 inches to the right and 1 inch down from the point (0, 0):</span></span>  
  
 [!code-csharp[System.Drawing.CoordinateSystems#32](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.CoordinateSystems/CS/Class1.cs#32)]
 [!code-vb[System.Drawing.CoordinateSystems#32](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.CoordinateSystems/VB/Class1.vb#32)]  
  
> [!NOTE]
>  <span data-ttu-id="37f0f-136">Wenn Sie beim Erstellen des Stifts eine Breite nicht angeben, wird im vorherige Beispiel eine Linie gezeichnet, die einen Zoll breit ist.</span><span class="sxs-lookup"><span data-stu-id="37f0f-136">If you don't specify a pen width when you construct your pen, the preceding example will draw a line that is one inch wide.</span></span> <span data-ttu-id="37f0f-137">Sie können die Stiftbreite angeben, in das zweite Argument der <xref:System.Drawing.Pen> Konstruktor:</span><span class="sxs-lookup"><span data-stu-id="37f0f-137">You can specify the pen width in the second argument to the <xref:System.Drawing.Pen> constructor:</span></span>  
  
 [!code-csharp[System.Drawing.CoordinateSystems#33](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.CoordinateSystems/CS/Class1.cs#33)]
 [!code-vb[System.Drawing.CoordinateSystems#33](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.CoordinateSystems/VB/Class1.vb#33)]  
  
 <span data-ttu-id="37f0f-138">Wenn Sie davon ausgehen, dass die Anzeigegerät 96 dpi in horizontaler Richtung und 96 dpi in vertikaler Richtung aufweist, sind die Endpunkte der Linie im vorherigen Beispiel folgenden Koordinaten in drei Koordinatensysteme:</span><span class="sxs-lookup"><span data-stu-id="37f0f-138">If we assume that the display device has 96 dots per inch in the horizontal direction and 96 dots per inch in the vertical direction, the endpoints of the line in the preceding example have the following coordinates in the three coordinate spaces:</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="37f0f-139">World</span><span class="sxs-lookup"><span data-stu-id="37f0f-139">World</span></span>|<span data-ttu-id="37f0f-140">(0, 0), (2, 1)</span><span class="sxs-lookup"><span data-stu-id="37f0f-140">(0, 0) to (2, 1)</span></span>|  
|<span data-ttu-id="37f0f-141">Seite</span><span class="sxs-lookup"><span data-stu-id="37f0f-141">Page</span></span>|<span data-ttu-id="37f0f-142">(0, 0), (2, 1)</span><span class="sxs-lookup"><span data-stu-id="37f0f-142">(0, 0) to (2, 1)</span></span>|  
|<span data-ttu-id="37f0f-143">Gerät</span><span class="sxs-lookup"><span data-stu-id="37f0f-143">Device</span></span>|<span data-ttu-id="37f0f-144">(0, 0 (null), (192, 96)</span><span class="sxs-lookup"><span data-stu-id="37f0f-144">(0, 0, to (192, 96)</span></span>|  
  
 <span data-ttu-id="37f0f-145">Beachten Sie, dass da des Ursprungs von der ganzen Welt Koordinatenbereich auf der linken oberen Ecke des Clientbereichs ist, die Seitenkoordinaten mit den globalen Koordinaten identisch sind.</span><span class="sxs-lookup"><span data-stu-id="37f0f-145">Note that because the origin of the world coordinate space is at the upper-left corner of the client area, the page coordinates are the same as the world coordinates.</span></span>  
  
 <span data-ttu-id="37f0f-146">Sie können die World Transformation und der Seitentransformation um eine Vielzahl von Effekte erzielen kombinieren.</span><span class="sxs-lookup"><span data-stu-id="37f0f-146">You can combine the world and page transformations to achieve a variety of effects.</span></span> <span data-ttu-id="37f0f-147">Nehmen wir beispielsweise an Zoll als Maßeinheit verwendet werden sollen, und den Ursprung des Koordinatensystems vom linken Rand des Clientbereichs und 1/2-Zoll vom oberen Rand des Clientbereichs von 2 Zoll sein sollen.</span><span class="sxs-lookup"><span data-stu-id="37f0f-147">For example, suppose you want to use inches as the unit of measure and you want the origin of your coordinate system to be 2 inches from the left edge of the client area and 1/2 inch from the top of the client area.</span></span> <span data-ttu-id="37f0f-148">Im folgenden Beispiel wird die World Transformation und der Seitentransformation ein <xref:System.Drawing.Graphics> Objekt, und klicken Sie dann zeichnet eine verbindende Linie aus (0, 0), (2, 1):</span><span class="sxs-lookup"><span data-stu-id="37f0f-148">The following example sets the world and page transformations of a <xref:System.Drawing.Graphics> object and then draws a line from (0, 0) to (2, 1):</span></span>  
  
 [!code-csharp[System.Drawing.CoordinateSystems#34](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.CoordinateSystems/CS/Class1.cs#34)]
 [!code-vb[System.Drawing.CoordinateSystems#34](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.CoordinateSystems/VB/Class1.vb#34)]  
  
 <span data-ttu-id="37f0f-149">Die folgende Abbildung zeigt die Zeile und das Koordinatensystem.</span><span class="sxs-lookup"><span data-stu-id="37f0f-149">The following illustration shows the line and coordinate system.</span></span>  
  
 <span data-ttu-id="37f0f-150">![Koordinatensystem](../../../../docs/framework/winforms/advanced/media/aboutgdip05-art03.gif "AboutGdip05_art03")</span><span class="sxs-lookup"><span data-stu-id="37f0f-150">![Coordinate System](../../../../docs/framework/winforms/advanced/media/aboutgdip05-art03.gif "AboutGdip05_art03")</span></span>  
  
 <span data-ttu-id="37f0f-151">Wenn Sie davon ausgehen, dass die Anzeigegerät 96 dpi in horizontaler Richtung und 96 dpi in vertikaler Richtung aufweist, sind die Endpunkte der Linie im vorherigen Beispiel folgenden Koordinaten in drei Koordinatensysteme:</span><span class="sxs-lookup"><span data-stu-id="37f0f-151">If we assume that the display device has 96 dots per inch in the horizontal direction and 96 dots per inch in the vertical direction, the endpoints of the line in the preceding example have the following coordinates in the three coordinate spaces:</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="37f0f-152">World</span><span class="sxs-lookup"><span data-stu-id="37f0f-152">World</span></span>|<span data-ttu-id="37f0f-153">(0, 0), (2, 1)</span><span class="sxs-lookup"><span data-stu-id="37f0f-153">(0, 0) to (2, 1)</span></span>|  
|<span data-ttu-id="37f0f-154">Seite</span><span class="sxs-lookup"><span data-stu-id="37f0f-154">Page</span></span>|<span data-ttu-id="37f0f-155">(2, 0,5), (4, 1.5)</span><span class="sxs-lookup"><span data-stu-id="37f0f-155">(2, 0.5) to (4, 1.5)</span></span>|  
|<span data-ttu-id="37f0f-156">Gerät</span><span class="sxs-lookup"><span data-stu-id="37f0f-156">Device</span></span>|<span data-ttu-id="37f0f-157">(192, 48) an (384, 144)</span><span class="sxs-lookup"><span data-stu-id="37f0f-157">(192, 48) to (384, 144)</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="37f0f-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="37f0f-158">See Also</span></span>  
 [<span data-ttu-id="37f0f-159">Koordinatensysteme und Transformationen</span><span class="sxs-lookup"><span data-stu-id="37f0f-159">Coordinate Systems and Transformations</span></span>](../../../../docs/framework/winforms/advanced/coordinate-systems-and-transformations.md)  
 [<span data-ttu-id="37f0f-160">Matrixdarstellung von Transformationen</span><span class="sxs-lookup"><span data-stu-id="37f0f-160">Matrix Representation of Transformations</span></span>](../../../../docs/framework/winforms/advanced/matrix-representation-of-transformations.md)
