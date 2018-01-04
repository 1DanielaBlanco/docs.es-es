---
title: "Cómo: Impedir la adición y eliminación de filas en el control DataGridView de formularios Windows Forms mediante el Diseñador"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-winforms
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords: DataGridView control [Windows Forms], preventing row addition or deletion
ms.assetid: a17722bd-9400-41e6-8dcc-c9c151f0a749
caps.latest.revision: "11"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: b7671c3629830de871585dacc1afa89dde14ec50
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/22/2017
---
# <a name="how-to-prevent-row-addition-and-deletion-in-the-windows-forms-datagridview-control-using-the-designer"></a><span data-ttu-id="0c651-102">Cómo: Impedir la adición y eliminación de filas en el control DataGridView de formularios Windows Forms mediante el Diseñador</span><span class="sxs-lookup"><span data-stu-id="0c651-102">How to: Prevent Row Addition and Deletion in the Windows Forms DataGridView Control Using the Designer</span></span>
<span data-ttu-id="0c651-103">En algunos casos, querrá impedir que los usuarios incluyan nuevas filas de datos o eliminen las filas existentes en el control <xref:System.Windows.Forms.DataGridView>.</span><span class="sxs-lookup"><span data-stu-id="0c651-103">Sometimes you will want to prevent users from entering new rows of data or deleting existing rows in your <xref:System.Windows.Forms.DataGridView> control.</span></span> <span data-ttu-id="0c651-104">Nuevas filas se escriben en la fila especial para los nuevos registros en la parte inferior del control.</span><span class="sxs-lookup"><span data-stu-id="0c651-104">New rows are entered in the special row for new records at the bottom of the control.</span></span> <span data-ttu-id="0c651-105">Al deshabilitar la adición de la fila, no se muestra la fila de nuevos registros.</span><span class="sxs-lookup"><span data-stu-id="0c651-105">When you disable row addition, the row for new records is not displayed.</span></span> <span data-ttu-id="0c651-106">A continuación, hacer que el control sea de solo lectura deshabilitando la eliminación de filas y la modificación de las celdas.</span><span class="sxs-lookup"><span data-stu-id="0c651-106">You can then make the control entirely read-only by disabling row deletion and cell editing.</span></span>  
  
 <span data-ttu-id="0c651-107">El procedimiento siguiente requiere un **aplicación de Windows** proyecto con un formulario que contenga un <xref:System.Windows.Forms.DataGridView> control.</span><span class="sxs-lookup"><span data-stu-id="0c651-107">The following procedure requires a **Windows Application** project with a form containing a <xref:System.Windows.Forms.DataGridView> control.</span></span> <span data-ttu-id="0c651-108">Para obtener información acerca de cómo configurar un proyecto de este tipo, consulte [Cómo: crear un proyecto de aplicación de Windows](http://msdn.microsoft.com/en-us/b2f93fed-c635-4705-8d0e-cf079a264efa) y [Cómo: agregar controles a formularios Windows Forms](../../../../docs/framework/winforms/controls/how-to-add-controls-to-windows-forms.md).</span><span class="sxs-lookup"><span data-stu-id="0c651-108">For information about setting up such a project, see [How to: Create a Windows Application Project](http://msdn.microsoft.com/en-us/b2f93fed-c635-4705-8d0e-cf079a264efa) and [How to: Add Controls to Windows Forms](../../../../docs/framework/winforms/controls/how-to-add-controls-to-windows-forms.md).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="0c651-109">Los cuadros de diálogo y comandos de menú que se ven pueden diferir de los descritos en la Ayuda, en función de los valores de configuración o de edición activos.</span><span class="sxs-lookup"><span data-stu-id="0c651-109">The dialog boxes and menu commands you see might differ from those described in Help depending on your active settings or edition.</span></span> <span data-ttu-id="0c651-110">Para cambiar la configuración, elija la opción **Importar y exportar configuraciones** del menú **Herramientas** .</span><span class="sxs-lookup"><span data-stu-id="0c651-110">To change your settings, choose **Import and Export Settings** on the **Tools** menu.</span></span> <span data-ttu-id="0c651-111">Para obtener más información, consulte [Personalizar la configuración de desarrollo en Visual Studio](http://msdn.microsoft.com/en-us/22c4debb-4e31-47a8-8f19-16f328d7dcd3).</span><span class="sxs-lookup"><span data-stu-id="0c651-111">For more information, see [Customizing Development Settings in Visual Studio](http://msdn.microsoft.com/en-us/22c4debb-4e31-47a8-8f19-16f328d7dcd3).</span></span>  
  
### <a name="to-prevent-row-addition-and-deletion"></a><span data-ttu-id="0c651-112">Para evitar la eliminación y adición de fila</span><span class="sxs-lookup"><span data-stu-id="0c651-112">To prevent row addition and deletion</span></span>  
  
-   <span data-ttu-id="0c651-113">Haga clic en el glifo de etiqueta inteligente (![glifo de etiqueta inteligente](../../../../docs/framework/winforms/controls/media/vs-winformsmttagglyph.gif "VS_WinFormSmtTagGlyph")) en la esquina superior derecha de la <xref:System.Windows.Forms.DataGridView> de control y, a continuación, desactive la **Habilitar acción de agregar** y **Habilitar eliminación** casillas de verificación.</span><span class="sxs-lookup"><span data-stu-id="0c651-113">Click the smart tag glyph (![Smart Tag Glyph](../../../../docs/framework/winforms/controls/media/vs-winformsmttagglyph.gif "VS_WinFormSmtTagGlyph")) on the upper-right corner of the <xref:System.Windows.Forms.DataGridView> control, and then clear the **Enable Adding** and **Enable Deleting** check boxes.</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="0c651-114">Para que el control sea de solo lectura, desactive la **Habilitar edición** también la casilla de verificación.</span><span class="sxs-lookup"><span data-stu-id="0c651-114">To make the control entirely read-only, clear the **Enable Editing** check box as well.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0c651-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="0c651-115">See Also</span></span>  
 <xref:System.Windows.Forms.DataGridView>  
 <xref:System.Windows.Forms.DataGridView.AllowUserToAddRows%2A?displayProperty=nameWithType>  
 [<span data-ttu-id="0c651-116">Cómo: crear un proyecto de aplicación de Windows</span><span class="sxs-lookup"><span data-stu-id="0c651-116">How to: Create a Windows Application Project</span></span>](http://msdn.microsoft.com/en-us/b2f93fed-c635-4705-8d0e-cf079a264efa)  
 [<span data-ttu-id="0c651-117">Cómo: Agregar controles a Windows Forms</span><span class="sxs-lookup"><span data-stu-id="0c651-117">How to: Add Controls to Windows Forms</span></span>](../../../../docs/framework/winforms/controls/how-to-add-controls-to-windows-forms.md)
