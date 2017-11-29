---
title: Erstellen und Implementieren von Schnittstellen (Visual Basic)
ms.custom: 
ms.date: 07/20/2015
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: devlang-visual-basic
ms.topic: article
helpviewer_keywords:
- interfaces [Visual Basic], walkthroughs
- interfaces [Visual Basic], testing
- interface implementation [Visual Basic], walkthrough
- interfaces [Visual Basic], creating
ms.assetid: ded82af2-9f52-4232-98ef-fe458180f112
caps.latest.revision: "22"
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: 08bf6dc7344d4f83c8ab1908fdeb29eb4a53e142
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/21/2017
---
# <a name="walkthrough-creating-and-implementing-interfaces-visual-basic"></a><span data-ttu-id="22701-102">Exemplarische Vorgehensweise: Erstellen und Implementieren von Schnittstellen (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="22701-102">Walkthrough: Creating and Implementing Interfaces (Visual Basic)</span></span>
<span data-ttu-id="22701-103">Schnittstellen beschreiben die Merkmale von Eigenschaften, Methoden und Ereignisse, sondern die Einzelheiten der Implementierung in Strukturen oder Klassen.</span><span class="sxs-lookup"><span data-stu-id="22701-103">Interfaces describe the characteristics of properties, methods, and events, but leave the implementation details up to structures or classes.</span></span>  
  
 <span data-ttu-id="22701-104">Diese exemplarische Vorgehensweise veranschaulicht das Deklarieren und Implementieren einer Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="22701-104">This walkthrough demonstrates how to declare and implement an interface.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="22701-105">In dieser exemplarischen Vorgehensweise stellt keine Informationen zum Erstellen einer Benutzeroberfläche bereit.</span><span class="sxs-lookup"><span data-stu-id="22701-105">This walkthrough doesn't provide information about how to create a user interface.</span></span>  
  
[!INCLUDE[note_settings_general](~/includes/note-settings-general-md.md)]  
  
### <a name="to-define-an-interface"></a><span data-ttu-id="22701-106">Um eine Schnittstelle zu definieren.</span><span class="sxs-lookup"><span data-stu-id="22701-106">To define an interface</span></span>  
  
1.  <span data-ttu-id="22701-107">Öffnen Sie ein neues [!INCLUDE[vbprvb](~/includes/vbprvb-md.md)]-Windows-Anwendungsprojekt.</span><span class="sxs-lookup"><span data-stu-id="22701-107">Open a new [!INCLUDE[vbprvb](~/includes/vbprvb-md.md)] Windows Application project.</span></span>  
  
2.  <span data-ttu-id="22701-108">Fügen Sie ein neues Modul für das Projekt, indem Sie auf **Modul hinzufügen** auf die **Projekt** Menü.</span><span class="sxs-lookup"><span data-stu-id="22701-108">Add a new module to the project by clicking **Add Module** on the **Project** menu.</span></span>  
  
3.  <span data-ttu-id="22701-109">Geben Sie dem neue Modul `Module1.vb` , und klicken Sie auf **hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="22701-109">Name the new module `Module1.vb` and click **Add**.</span></span> <span data-ttu-id="22701-110">Der Code für das neue Modul wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="22701-110">The code for the new module is displayed.</span></span>  
  
4.  <span data-ttu-id="22701-111">Definieren Sie eine Schnittstelle mit dem Namen `TestInterface` in `Module1` dazu `Interface TestInterface` zwischen der `Module` und `End Module` -Anweisungen, und drücken Sie die EINGABETASTE.</span><span class="sxs-lookup"><span data-stu-id="22701-111">Define an interface named `TestInterface` within `Module1` by typing `Interface TestInterface` between the `Module` and `End Module` statements, and then pressing ENTER.</span></span> <span data-ttu-id="22701-112">Die **Code-Editor** Einzüge der `Interface` Schlüsselwort und fügt eine `End Interface` Anweisung um einen Codeblock zu bilden.</span><span class="sxs-lookup"><span data-stu-id="22701-112">The **Code Editor** indents the `Interface` keyword and adds an `End Interface` statement to form a code block.</span></span>  
  
5.  <span data-ttu-id="22701-113">Definieren Sie eine Eigenschaft, Methode und Ereignis für die Schnittstelle durch Platzieren den folgenden Code zwischen den `Interface` und `End Interface` Anweisungen:</span><span class="sxs-lookup"><span data-stu-id="22701-113">Define a property, method, and event for the interface by placing the following code between the `Interface` and `End Interface` statements:</span></span>  
  
     [!code-vb[VbVbalrOOP#98](../../../../visual-basic/misc/codesnippet/VisualBasic/walkthrough-creating-and-implementing-interfaces_1.vb)]  
  
## <a name="implementation"></a><span data-ttu-id="22701-114">Implementierung</span><span class="sxs-lookup"><span data-stu-id="22701-114">Implementation</span></span>  
 <span data-ttu-id="22701-115">Sie können feststellen, dass die Syntax zum Deklarieren von Schnittstellenmembern Syntax zum Deklarieren von Klassenmembern unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="22701-115">You may notice that the syntax used to declare interface members is different from the syntax used to declare class members.</span></span> <span data-ttu-id="22701-116">Dieser Unterschied Deaktivierung, dass Schnittstellen Implementierungscode enthalten können.</span><span class="sxs-lookup"><span data-stu-id="22701-116">This difference reflects the fact that interfaces cannot contain implementation code.</span></span>  
  
#### <a name="to-implement-the-interface"></a><span data-ttu-id="22701-117">Implementieren die Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="22701-117">To implement the interface</span></span>  
  
1.  <span data-ttu-id="22701-118">Fügen Sie eine Klasse mit dem Namen `ImplementationClass` durch Hinzufügen folgender Anweisung zu `Module1`nach der `End Interface` Anweisung aber vor der `End Module` -Anweisung, und drücken Sie die EINGABETASTE:</span><span class="sxs-lookup"><span data-stu-id="22701-118">Add a class named `ImplementationClass` by adding the following statement to `Module1`, after the `End Interface` statement but before the `End Module` statement, and then pressing ENTER:</span></span>  
  
     [!code-vb[VbVbalrOOP#99](../../../../visual-basic/misc/codesnippet/VisualBasic/walkthrough-creating-and-implementing-interfaces_2.vb)]  
  
     <span data-ttu-id="22701-119">Wenn Sie in der integrierten Entwicklungsumgebung arbeiten die **Code-Editor** bereitstellt, einen übereinstimmenden `End Class` -Anweisung, wenn Sie die EINGABETASTE drücken.</span><span class="sxs-lookup"><span data-stu-id="22701-119">If you are working within the integrated development environment, the **Code Editor** supplies a matching `End Class` statement when you press ENTER.</span></span>  
  
2.  <span data-ttu-id="22701-120">Fügen Sie die folgenden `Implements` -Anweisung `ImplementationClass`, die die Schnittstelle der Klassennamen implementiert:</span><span class="sxs-lookup"><span data-stu-id="22701-120">Add the following `Implements` statement to `ImplementationClass`, which names the interface the class implements:</span></span>  
  
     [!code-vb[VbVbalrOOP#100](../../../../visual-basic/misc/codesnippet/VisualBasic/walkthrough-creating-and-implementing-interfaces_3.vb)]  
  
     <span data-ttu-id="22701-121">Wenn separat von anderen Elementen am Anfang einer Klasse oder Struktur, aufgeführt. die `Implements` Anweisung gibt an, dass die Klasse oder Struktur eine Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="22701-121">When listed separately from other items at the top of a class or structure, the `Implements` statement indicates that the class or structure implements an interface.</span></span>  
  
     <span data-ttu-id="22701-122">Wenn Sie in der integrierten Entwicklungsumgebung arbeiten die **Code-Editor** implementiert die erforderlichen Klassenmember `TestInterface` Wenn Sie die EINGABETASTE drücken und Sie können den nächsten Schritt überspringen.</span><span class="sxs-lookup"><span data-stu-id="22701-122">If you are working within the integrated development environment, the **Code Editor** implements the class members required by `TestInterface` when you press ENTER, and you can skip the next step.</span></span>  
  
3.  <span data-ttu-id="22701-123">Wenn Sie nicht innerhalb der integrierten Entwicklungsumgebung arbeiten, müssen Sie alle Member der Schnittstelle implementieren `MyInterface`.</span><span class="sxs-lookup"><span data-stu-id="22701-123">If you are not working within the integrated development environment, you must implement all the members of the interface `MyInterface`.</span></span> <span data-ttu-id="22701-124">Fügen Sie folgenden Code zum `ImplementationClass` implementieren `Event1`, `Method1`, und `Prop1`:</span><span class="sxs-lookup"><span data-stu-id="22701-124">Add the following code to `ImplementationClass` to implement `Event1`, `Method1`, and `Prop1`:</span></span>  
  
     [!code-vb[VbVbalrOOP#101](../../../../visual-basic/misc/codesnippet/VisualBasic/walkthrough-creating-and-implementing-interfaces_4.vb)]  
  
     <span data-ttu-id="22701-125">Die `Implements` Anweisung benennt die Schnittstelle und Schnittstellenmember implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="22701-125">The `Implements` statement names the interface and interface member being implemented.</span></span>  
  
4.  <span data-ttu-id="22701-126">Beenden Sie die Definition der `Prop1` durch Hinzufügen eines privaten Felds auf die Klasse, die den Wert der Eigenschaft gespeichert:</span><span class="sxs-lookup"><span data-stu-id="22701-126">Complete the definition of `Prop1` by adding a private field to the class that stored the property value:</span></span>  
  
     [!code-vb[VbVbalrOOP#102](../../../../visual-basic/misc/codesnippet/VisualBasic/walkthrough-creating-and-implementing-interfaces_5.vb)]  
  
     <span data-ttu-id="22701-127">Der Rückgabewert von der `pval` aus der Eigenschaft get-Zugriffsmethode.</span><span class="sxs-lookup"><span data-stu-id="22701-127">Return the value of the `pval` from the property get accessor.</span></span>  
  
     [!code-vb[VbVbalrOOP#103](../../../../visual-basic/misc/codesnippet/VisualBasic/walkthrough-creating-and-implementing-interfaces_6.vb)]  
  
     <span data-ttu-id="22701-128">Legen Sie den Wert des `pval` im Eigenschaftensatz-Zugriffsmethode.</span><span class="sxs-lookup"><span data-stu-id="22701-128">Set the value of `pval` in the property set accessor.</span></span>  
  
     [!code-vb[VbVbalrOOP#104](../../../../visual-basic/misc/codesnippet/VisualBasic/walkthrough-creating-and-implementing-interfaces_7.vb)]  
  
5.  <span data-ttu-id="22701-129">Beenden Sie die Definition der `Method1` durch den folgenden Code hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="22701-129">Complete the definition of `Method1` by adding the following code.</span></span>  
  
     [!code-vb[VbVbalrOOP#105](../../../../visual-basic/misc/codesnippet/VisualBasic/walkthrough-creating-and-implementing-interfaces_8.vb)]  
  
#### <a name="to-test-the-implementation-of-the-interface"></a><span data-ttu-id="22701-130">So testen Sie die Implementierung der Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="22701-130">To test the implementation of the interface</span></span>  
  
1.  <span data-ttu-id="22701-131">Mit der rechten Maustaste des Startformulars für das Projekt in der **Projektmappen-Explorer**, und klicken Sie auf **Code anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="22701-131">Right-click the startup form for your project in the **Solution Explorer**, and click **View Code**.</span></span> <span data-ttu-id="22701-132">Der Editor zeigt die Klasse für Ihr Startformular.</span><span class="sxs-lookup"><span data-stu-id="22701-132">The editor displays the class for your startup form.</span></span> <span data-ttu-id="22701-133">Standardmäßig heißt die Startformular `Form1`.</span><span class="sxs-lookup"><span data-stu-id="22701-133">By default, the startup form is called `Form1`.</span></span>  
  
2.  <span data-ttu-id="22701-134">Fügen Sie die folgenden `testInstance` -Feld der `Form1` Klasse:</span><span class="sxs-lookup"><span data-stu-id="22701-134">Add the following `testInstance` field to the `Form1` class:</span></span>  
  
     [!code-vb[VbVbalrOOP#120](../../../../visual-basic/misc/codesnippet/VisualBasic/walkthrough-creating-and-implementing-interfaces_9.vb)]  
  
     <span data-ttu-id="22701-135">Durch das Deklarieren von `testInstance` als `WithEvents`, die `Form1` Klasse seine Ereignisse behandeln kann.</span><span class="sxs-lookup"><span data-stu-id="22701-135">By declaring `testInstance` as `WithEvents`, the `Form1` class can handle its events.</span></span>  
  
3.  <span data-ttu-id="22701-136">Fügen Sie den folgenden Ereignishandler auf der `Form1` Klasse ausgelöste Ereignisse behandeln `testInstance`:</span><span class="sxs-lookup"><span data-stu-id="22701-136">Add the following event handler to the `Form1` class to handle events raised by `testInstance`:</span></span>  
  
     [!code-vb[VbVbalrOOP#106](../../../../visual-basic/misc/codesnippet/VisualBasic/walkthrough-creating-and-implementing-interfaces_10.vb)]  
  
4.  <span data-ttu-id="22701-137">Hinzufügen eine Unterroutine namens `Test` auf die `Form1` Klasse, um die Implementierungsklasse zu testen:</span><span class="sxs-lookup"><span data-stu-id="22701-137">Add a subroutine named `Test` to the `Form1` class to test the implementation class:</span></span>  
  
     [!code-vb[VbVbalrOOP#107](../../../../visual-basic/misc/codesnippet/VisualBasic/walkthrough-creating-and-implementing-interfaces_11.vb)]  
  
     <span data-ttu-id="22701-138">Die `Test` Prozedur erstellt eine Instanz der Klasse, die implementiert `MyInterface`, weist diese Instanz die `testInstance` Feld Festlegen einer Eigenschaft, und führt eine Methode über die Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="22701-138">The `Test` procedure creates an instance of the class that implements `MyInterface`, assigns that instance to the `testInstance` field, sets a property, and runs a method through the interface.</span></span>  
  
5.  <span data-ttu-id="22701-139">Fügen Sie Code zum Aufrufen der `Test` Prozedur aus der `Form1 Load` Prozedur mit dem Startformular:</span><span class="sxs-lookup"><span data-stu-id="22701-139">Add code to call the `Test` procedure from the `Form1 Load` procedure of your startup form:</span></span>  
  
     [!code-vb[VbVbalrOOP#108](../../../../visual-basic/misc/codesnippet/VisualBasic/walkthrough-creating-and-implementing-interfaces_12.vb)]  
  
6.  <span data-ttu-id="22701-140">Führen Sie die `Test` Prozedur durch Drücken von F5.</span><span class="sxs-lookup"><span data-stu-id="22701-140">Run the `Test` procedure by pressing F5.</span></span> <span data-ttu-id="22701-141">Die Meldung "Prop1 festlegen und 9" wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="22701-141">The message "Prop1 was set to 9" is displayed.</span></span> <span data-ttu-id="22701-142">Nachdem Sie nun der Nachricht klicken Sie auf "Parameters" X "für Method1 is 5" werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="22701-142">After you click OK, the message "The X parameter for Method1 is 5" is displayed.</span></span> <span data-ttu-id="22701-143">Klicken Sie auf OK, und die Meldung "der Ereignishandler das Ereignis abgefangen" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="22701-143">Click OK, and the message "The event handler caught the event" is displayed.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="22701-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="22701-144">See Also</span></span>  
 [<span data-ttu-id="22701-145">Implements-Anweisung</span><span class="sxs-lookup"><span data-stu-id="22701-145">Implements Statement</span></span>](../../../../visual-basic/language-reference/statements/implements-statement.md)  
 [<span data-ttu-id="22701-146">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="22701-146">Interfaces</span></span>](../../../../visual-basic/programming-guide/language-features/interfaces/index.md)  
 [<span data-ttu-id="22701-147">Interface-Anweisung</span><span class="sxs-lookup"><span data-stu-id="22701-147">Interface Statement</span></span>](../../../../visual-basic/language-reference/statements/interface-statement.md)  
 [<span data-ttu-id="22701-148">Event-Anweisung</span><span class="sxs-lookup"><span data-stu-id="22701-148">Event Statement</span></span>](../../../../visual-basic/language-reference/statements/event-statement.md)
