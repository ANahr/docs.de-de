---
title: 'Vorgehensweise: Abonnieren von Ereignissen und Kündigen von Ereignisabonnements – C#-Programmierhandbuch'
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- event handlers [C#], creating
- Code Editor, event handlers
- events [C#], creating using the IDE
ms.assetid: 6319f39f-282c-4173-8a62-6c4657cf51cd
ms.openlocfilehash: 89647687c73cdb9b81625b830f0c9a77f1c67d13
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/11/2018
ms.locfileid: "53241086"
---
# <a name="how-to-subscribe-to-and-unsubscribe-from-events-c-programming-guide"></a>Vorgehensweise: Abonnieren von Ereignissen und Kündigen von Ereignisabonnements (C#-Programmierhandbuch)
Wenn Sie benutzerdefinierten Code schreiben möchten, der aufgerufen wird, wenn dieses Ereignis ausgelöst wird, können Sie ein Ereignis abonnieren, das von einer anderen Klasse veröffentlicht wurde. Sie können z.B. das `click`-Ereignis einer Schaltfläche abonnieren, damit Ihre Anwendung etwas nützliches macht, wenn ein Benutzer auf die Schaltfläche klickt.  
  
### <a name="to-subscribe-to-events-by-using-the-visual-studio-ide"></a>So abonnieren Sie Ereignisse mit der Visual Studio IDE  
  
1.  Wenn Sie in der Ansicht **Entwurf** das Fenster **Eigenschaften** nicht sehen können, klicken Sie mit der rechten Maustaste auf das Formular oder das Kontrollelement, für das Sie einen Ereignishandler erstellen möchten, und wählen Sie anschließen **Eigenschaften** aus.  
  
2.  Klicken Sie oben im Fenster **Eigenschaften** auf das Symbol **Ereignisse**.  
  
3.  Doppelklicken Sie auf das Ereignis, das Sie erstellen möchten, z.B. das `Load`-Ereignis.  
  
     Visual C# erstellt eine leere Ereignishandlermethode, und fügt diese in den Code ein. Alternativ können Sie den Code auch manuell in der **Codeansicht** einfügen. Die folgenden Codezeilen deklarieren beispielsweise eine Eventhandlermethode, die aufgerufen wird, wenn die Klasse `Form` das `Load`-Ereignis auslöst.  
  
     [!code-csharp[csProgGuideEvents#11](../../../csharp/programming-guide/events/codesnippet/CSharp/how-to-subscribe-to-and-unsubscribe-from-events_1.cs)]  
  
     Die Codezeile, die für das Abonnement des Ereignisses erforderlich ist, wird auch automatisch in der `InitializeComponent`-Methode in der Datei „Form1.Designer.cs“ in Ihrem Projekt generiert. Sie sieht ungefähr so aus:  
  
    ```csharp
    this.Load += new System.EventHandler(this.Form1_Load);  
    ```  
  
### <a name="to-subscribe-to-events-programmatically"></a>So abonnieren Sie Ereignisse programmgesteuert  
  
1.  Definieren Sie eine Ereignishandlermethode, deren Signatur mit der Delegatsignatur des Ereignisses übereinstimmt. Wenn das Ereignis z.B. auf dem Delegattyp <xref:System.EventHandler> basiert, repräsentiert der folgende Code den Methodenstub:  
  
    ```csharp
    void HandleCustomEvent(object sender, CustomEventArgs a)  
    {  
       // Do something useful here.  
    }  
    ```  
  
2.  Verwenden Sie den Additionszuweisungsoperator (`+=`), um ihren Ereignishandler Ihrem Ereignis anzufügen. Gehen Sie in folgendem Beispiel davon aus, dass ein Objekt mit dem Namen `publisher` ein Ereignis mit dem Namen `RaiseCustomEvent` aufweist. Beachten Sie, dass die Abonnementklasse einen Verweis auf die Herausgeberklasse benötigt, um deren Ereignis abonnieren zu können.  
  
    ```csharp
    publisher.RaiseCustomEvent += HandleCustomEvent;  
    ```  
  
     Beachten Sie, dass die oben stehende Syntax in C# 2.0 neu ist. Sie entsprechen der Syntax in C# 1.0, in der der kapselnde Delegat mithilfe des Schlüsselwort `new` explizit erstellt werden muss:  
  
    ```csharp
    publisher.RaiseCustomEvent += new CustomEventHandler(HandleCustomEvent);  
    ```  
  
     Ein Ereignishandler kann auch mithilfe eines Lambdaausdruckes hinzugefügt werden:  
  
    ```csharp
    public Form1()  
    {  
        InitializeComponent();  
        // Use a lambda expression to define an event handler.  
        this.Click += (s,e) => { MessageBox.Show(  
           ((MouseEventArgs)e).Location.ToString());};  
    }  
    ```  
  
     Weitere Informationen finden Sie unter [Vorgehensweise: Verwenden von Lambdaausdrücken außerhalb von LINQ](../../../csharp/programming-guide/statements-expressions-operators/how-to-use-lambda-expressions-outside-linq.md).  
  
### <a name="to-subscribe-to-events-by-using-an-anonymous-method"></a>So abonnieren Sie Ereignisse mit einer anonymen Methode  
  
-   Wenn Sie das Abonnement eines Ereignisses später nicht kündigen müssen, können Sie den Additionszuweisungsoperator (`+=`) verwenden, um eine anonyme Methode an das Ereignis anzufügen. Gehen Sie in folgendem Beispiel davon aus, dass ein Objekt mit dem Namen `publisher` ein Ereignis mit dem Namen `RaiseCustomEvent` aufweist, und dass eine `CustomEventArgs`-Klasse so definiert wurde, dass Sie eine Art von spezialisierter Ereignisinformation enthält. Beachten Sie, dass die Abonnementklasse einen Verweis auf die `publisher` benötigt, um deren Ereignis abonnieren zu können.  
  
    ```csharp
    publisher.RaiseCustomEvent += delegate(object o, CustomEventArgs e)  
    {  
      string s = o.ToString() + " " + e.ToString();  
      Console.WriteLine(s);  
    };  
    ```  
  
     Nehmen Sie auch zur Kenntnis, dass Sie das Abonnement eines Ereignisses nicht ohne Weiteres kündigen können, wenn Sie eine anonyme Funktion für das Abonnement verwendet haben. Um in einem derartigen Szenario das Abonnement kündigen zu können, müssen Sie zu dem Code zurückkehren, mit dem Sie das Ereignis abonniert haben; speichern Sie anschließend die anonyme Methode in einer Delegatvariablen, und fügen Sie dann den Delegaten in das Ereignis ein. Grundsätzlich wird empfohlen, keine anonymen Funktionen für das Abonnieren von Ereignissen zu verwenden, wenn Sie das Abonnement an einer späteren Stelle in Ihrem Code noch einmal kündigen müssen. Informationen zu anonymen Funktionen finden Sie unter [Anonyme Funktionen](../../../csharp/programming-guide/statements-expressions-operators/anonymous-functions.md).  
  
## <a name="unsubscribing"></a>Kündigen des Abonnements  
 Kündigen Sie das Ereignisabonnement, um ein Abrufen des Ereignishandlers beim Auslösen des Ereignisses zu verhindern. Sie sollten das Ereignisabonnement kündigen, bevor Sie ein Abonnentenobjekt verwerfen, um Ressourcenverluste zu verhindern. Bis zur Kündigung Ihres Ereignisabonnements verweist der Multicastdelegat, der dem Ereignis im Veröffentlichungsobjekt zugrunde liegt, auf einen Delegaten, der den Ereignishandler des Abonnenten einkapselt. Solange das Veröffentlichungsobjekt diesen Verweis enthält, wird Ihr Abonnentenobjekt bei der automatische Speicherbereinigung nicht gelöscht.  
  
#### <a name="to-unsubscribe-from-an-event"></a>So kündigen Sie ein Ereignisabonnement  
  
-   Verwenden Sie den Subtraktionszuweisungsoperator (`-=`), um ein Ereignisabonnement zu kündigen:  
  
    ```csharp
    publisher.RaiseCustomEvent -= HandleCustomEvent;  
    ```  
  
     Wenn alle Abonnenten ihr Ereignisabonnement gekündigt haben, wird die Ereignisinstanz in der Herausgeberklasse auf `null` festgelegt.  
  
## <a name="see-also"></a>Siehe auch

- [Ereignisse](../../../csharp/programming-guide/events/index.md)  
- [event](../../../csharp/language-reference/keywords/event.md)  
- [Vorgehensweise: Veröffentlichen von Ereignissen, die den .NET Framework-Richtlinien entsprechen](../../../csharp/programming-guide/events/how-to-publish-events-that-conform-to-net-framework-guidelines.md)  
- [-= Operator (C#-Referenz)](../../language-reference/operators/subtraction-assignment-operator.md)  
- [+=-Operator](../../../csharp/language-reference/operators/addition-assignment-operator.md)