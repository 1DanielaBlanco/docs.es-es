---
title: "Cómo: Compartir datos enlazados entre formularios mediante el componente BindingSource"
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
- examples [Windows Forms], BindingSource component
- data binding [Windows Forms], sharing data across forms
- BindingSource component [Windows Forms], examples
- BindingSource [Windows Forms], using with multiple forms
ms.assetid: a1a49630-db9c-4485-b888-1f62a373a4f7
caps.latest.revision: "8"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: 95fd7583e6d86aa84c53f6cee7056f1d631e948b
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/21/2017
---
# <a name="how-to-share-bound-data-across-forms-using-the-bindingsource-component"></a><span data-ttu-id="c92da-102">Cómo: Compartir datos enlazados entre formularios mediante el componente BindingSource</span><span class="sxs-lookup"><span data-stu-id="c92da-102">How to: Share Bound Data Across Forms Using the BindingSource Component</span></span>
<span data-ttu-id="c92da-103">Puede compartir datos fácilmente entre formularios con el componente <xref:System.Windows.Forms.BindingSource>.</span><span class="sxs-lookup"><span data-stu-id="c92da-103">You can easily share data across forms using the <xref:System.Windows.Forms.BindingSource> component.</span></span> <span data-ttu-id="c92da-104">Por ejemplo, quizás quiera mostrar un formulario de solo lectura que resume los datos del origen de datos y otro formulario editable que contiene información detallada sobre el elemento seleccionado actualmente en el origen de datos.</span><span class="sxs-lookup"><span data-stu-id="c92da-104">For example, you may want to display one read-only form that summarizes the data-source data and another editable form that contains detailed information about the currently selected item in the data source.</span></span> <span data-ttu-id="c92da-105">Este ejemplo muestra este escenario.</span><span class="sxs-lookup"><span data-stu-id="c92da-105">This example demonstrates this scenario.</span></span>  
  
## <a name="example"></a><span data-ttu-id="c92da-106">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c92da-106">Example</span></span>  
 <span data-ttu-id="c92da-107">En el ejemplo de código siguiente se muestra cómo compartir un <xref:System.Windows.Forms.BindingSource> y sus datos enlazados entre formularios.</span><span class="sxs-lookup"><span data-stu-id="c92da-107">The following code example demonstrates how to share a <xref:System.Windows.Forms.BindingSource> and its bound data across forms.</span></span> <span data-ttu-id="c92da-108">En este ejemplo, el <xref:System.Windows.Forms.BindingSource> compartido se pasa al constructor del formulario secundario.</span><span class="sxs-lookup"><span data-stu-id="c92da-108">In this example, the shared <xref:System.Windows.Forms.BindingSource> is passed to the constructor of the child form.</span></span> <span data-ttu-id="c92da-109">El formulario secundario permite al usuario editar los datos del elemento actualmente seleccionado en el formulario principal.</span><span class="sxs-lookup"><span data-stu-id="c92da-109">The child form allows the user to edit the data for the currently selected item in the main form.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="c92da-110">El evento <xref:System.Windows.Forms.BindingSource.BindingComplete> del componente <xref:System.Windows.Forms.BindingSource> se controla en el ejemplo para asegurarse de que los dos formularios permanecen sincronizadas.</span><span class="sxs-lookup"><span data-stu-id="c92da-110">The <xref:System.Windows.Forms.BindingSource.BindingComplete> event for the <xref:System.Windows.Forms.BindingSource> component is handled in the example to ensure that the two forms remain synchronized.</span></span> <span data-ttu-id="c92da-111">Para más información acerca de por qué se hace así, vea [Cómo: Garantizar varios controles enlazados al mismo origen de datos permanezcan sincronizados](../../../../docs/framework/winforms/multiple-controls-bound-to-data-source-synchronized.md).</span><span class="sxs-lookup"><span data-stu-id="c92da-111">For more information about why this is done, see [How to: Ensure Multiple Controls Bound to the Same Data Source Remain Synchronized](../../../../docs/framework/winforms/multiple-controls-bound-to-data-source-synchronized.md).</span></span>  
  
 [!code-csharp[System.Windows.Forms.BindingSourceMultipleForms#1](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.BindingSourceMultipleForms/CS/Form1.cs#1)]
 [!code-vb[System.Windows.Forms.BindingSourceMultipleForms#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.BindingSourceMultipleForms/VB/Form1.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="c92da-112">Compilar el código</span><span class="sxs-lookup"><span data-stu-id="c92da-112">Compiling the Code</span></span>  
 <span data-ttu-id="c92da-113">Para este ejemplo se necesita:</span><span class="sxs-lookup"><span data-stu-id="c92da-113">This example requires:</span></span>  
  
-   <span data-ttu-id="c92da-114">Referencias a los ensamblados System, System.Windows.Forms, System.Drawing, System.Data y System.Xml.</span><span class="sxs-lookup"><span data-stu-id="c92da-114">References to the System, System.Windows.Forms, System.Drawing, System.Data, and System.Xml assemblies.</span></span>  
  
 <span data-ttu-id="c92da-115">Para información sobre cómo compilar este ejemplo desde la línea de comandos para [!INCLUDE[vbprvb](../../../../includes/vbprvb-md.md)] o [!INCLUDE[csprcs](../../../../includes/csprcs-md.md)], consulte [Compilación desde la línea de comandos](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) o [Compilar desde la línea de comandos con csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span><span class="sxs-lookup"><span data-stu-id="c92da-115">For information about building this example from the command line for [!INCLUDE[vbprvb](../../../../includes/vbprvb-md.md)] or [!INCLUDE[csprcs](../../../../includes/csprcs-md.md)], see [Building from the Command Line](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) or [Command-line Building With csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span></span> <span data-ttu-id="c92da-116">También puede compilar este ejemplo en [!INCLUDE[vsprvs](../../../../includes/vsprvs-md.md)] pegando el código en un nuevo proyecto.</span><span class="sxs-lookup"><span data-stu-id="c92da-116">You can also build this example in [!INCLUDE[vsprvs](../../../../includes/vsprvs-md.md)] by pasting the code into a new project.</span></span>  <span data-ttu-id="c92da-117">Vea también [Cómo: Compilar y ejecutar un ejemplo de código completo de Windows Forms en Visual Studio](http://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).</span><span class="sxs-lookup"><span data-stu-id="c92da-117">Also see [How to: Compile and Run a Complete Windows Forms Code Example Using Visual Studio](http://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c92da-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="c92da-118">See Also</span></span>  
 [<span data-ttu-id="c92da-119">Componente BindingSource</span><span class="sxs-lookup"><span data-stu-id="c92da-119">BindingSource Component</span></span>](../../../../docs/framework/winforms/controls/bindingsource-component.md)  
 [<span data-ttu-id="c92da-120">Enlace de datos en Windows Forms</span><span class="sxs-lookup"><span data-stu-id="c92da-120">Windows Forms Data Binding</span></span>](../../../../docs/framework/winforms/windows-forms-data-binding.md)  
 [<span data-ttu-id="c92da-121">Cómo: Controlar errores y excepciones que se producen con el enlace de datos</span><span class="sxs-lookup"><span data-stu-id="c92da-121">How to: Handle Errors and Exceptions that Occur with Databinding</span></span>](../../../../docs/framework/winforms/controls/how-to-handle-errors-and-exceptions-that-occur-with-databinding.md)
