---
title: 'Gewusst wie: Erfassen von Benutzereingaben in einem "PrintDialog" zur Laufzeit'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- print options [Windows Forms], changing at run time
- printing [Windows Forms], options
- print options
- run time [Windows Forms], changing print options
ms.assetid: 438501d8-9a70-4fb3-aae6-e46579aba0c6
ms.openlocfilehash: 554c3c43f8ac4d41ddfc8651472d0b7fbed960bb
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
ms.locfileid: "33522875"
---
# <a name="how-to-capture-user-input-from-a-printdialog-at-run-time"></a><span data-ttu-id="ca205-102">Gewusst wie: Erfassen von Benutzereingaben in einem "PrintDialog" zur Laufzeit</span><span class="sxs-lookup"><span data-stu-id="ca205-102">How to: Capture User Input from a PrintDialog at Run Time</span></span>
<span data-ttu-id="ca205-103">Druckoptionen zur Entwurfszeit festgelegt werden kann, sollten Sie manchmal zur Laufzeit, wahrscheinlich aufgrund der vom Benutzer ausgewählten Optionen diese Optionen ändern.</span><span class="sxs-lookup"><span data-stu-id="ca205-103">While you can set options related to printing at design time, you will sometimes want to change these options at run time, most likely because of choices made by the user.</span></span> <span data-ttu-id="ca205-104">Sie können Erfassen von Benutzereingaben zum Drucken von einem Dokument mithilfe der <xref:System.Windows.Forms.PrintDialog> und die <xref:System.Drawing.Printing.PrintDocument> Komponenten.</span><span class="sxs-lookup"><span data-stu-id="ca205-104">You can capture user input for printing a document using the <xref:System.Windows.Forms.PrintDialog> and the <xref:System.Drawing.Printing.PrintDocument> components.</span></span>  
  
### <a name="to-change-print-options-programmatically"></a><span data-ttu-id="ca205-105">So ändern Sie die Druckoptionen programmgesteuert</span><span class="sxs-lookup"><span data-stu-id="ca205-105">To change print options programmatically</span></span>  
  
1.  <span data-ttu-id="ca205-106">Hinzufügen einer <xref:System.Windows.Forms.PrintDialog> und ein <xref:System.Drawing.Printing.PrintDocument> -Komponente in Ihr Formular.</span><span class="sxs-lookup"><span data-stu-id="ca205-106">Add a <xref:System.Windows.Forms.PrintDialog> and a <xref:System.Drawing.Printing.PrintDocument> component to your form.</span></span>  
  
2.  <span data-ttu-id="ca205-107">Festlegen der <xref:System.Windows.Forms.PrintDialog.Document%2A> Eigenschaft von der <xref:System.Windows.Forms.PrintDialog> auf der <xref:System.Drawing.Printing.PrintDocument> dem Formular hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="ca205-107">Set the <xref:System.Windows.Forms.PrintDialog.Document%2A> property of the <xref:System.Windows.Forms.PrintDialog> to the <xref:System.Drawing.Printing.PrintDocument> added to the form.</span></span>  
  
    ```vb  
    PrintDialog1.Document = PrintDocument1  
    ```  
  
    ```csharp  
    printDialog1.Document = PrintDocument1;  
    ```  
  
    ```cpp  
    printDialog1->Document = PrintDocument1;  
    ```  
  
3.  <span data-ttu-id="ca205-108">Anzeigen der <xref:System.Windows.Forms.PrintDialog> Komponente, indem die <xref:System.Windows.Forms.CommonDialog.ShowDialog%2A> Methode.</span><span class="sxs-lookup"><span data-stu-id="ca205-108">Display the <xref:System.Windows.Forms.PrintDialog> component by using the <xref:System.Windows.Forms.CommonDialog.ShowDialog%2A> method.</span></span>  
  
    ```vb  
    PrintDialog1.ShowDialog()  
    ```  
  
    ```csharp  
    printDialog1.ShowDialog();  
    ```  
  
    ```cpp  
    printDialog1->ShowDialog();  
    ```  
  
4.  <span data-ttu-id="ca205-109">Des Benutzers, die im Dialogfeld ausgewählten Druckoptionen kopiert werden die <xref:System.Drawing.Printing.PrinterSettings> Eigenschaft von der <xref:System.Drawing.Printing.PrintDocument> Komponente.</span><span class="sxs-lookup"><span data-stu-id="ca205-109">The user's printing choices from the dialog will be copied to the <xref:System.Drawing.Printing.PrinterSettings> property of the <xref:System.Drawing.Printing.PrintDocument> component.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ca205-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ca205-110">See Also</span></span>  
 [<span data-ttu-id="ca205-111">Vorgehensweise: Drucken einer mehrseitigen Textdatei in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="ca205-111">How to: Print a Multi-Page Text File in Windows Forms</span></span>](../../../../docs/framework/winforms/advanced/how-to-print-a-multi-page-text-file-in-windows-forms.md)  
 [<span data-ttu-id="ca205-112">Druckunterstützung in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="ca205-112">Windows Forms Print Support</span></span>](../../../../docs/framework/winforms/advanced/windows-forms-print-support.md)
