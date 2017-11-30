---
title: "Cómo: Utilizar punteros para copiar una matriz de bytes (Guía de programación de C#)"
ms.date: 07/20/2015
ms.prod: .net
ms.technology: devlang-csharp
ms.topic: article
helpviewer_keywords:
- byte arrays [C#]
- arrays [C#], byte
- pointers [C#], to copy bytes
ms.assetid: ec16fbb4-a24e-45f5-a763-9499d3fabe0a
caps.latest.revision: "21"
author: BillWagner
ms.author: wiwagn
ms.openlocfilehash: 375cab76063e4c77515d6b05b42f2d97ff3efc44
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/21/2017
---
# <a name="how-to-use-pointers-to-copy-an-array-of-bytes--c-programming-guide"></a><span data-ttu-id="7c8d4-102">Cómo: Utilizar punteros para copiar una matriz de bytes (Guía de programación de C#)</span><span class="sxs-lookup"><span data-stu-id="7c8d4-102">How to: Use Pointers to Copy an Array of Bytes  (C# Programming Guide)</span></span>
<span data-ttu-id="7c8d4-103">En el ejemplo siguiente se usan punteros para copiar bytes de una matriz a otra.</span><span class="sxs-lookup"><span data-stu-id="7c8d4-103">The following example uses pointers to copy bytes from one array to another.</span></span>  
  
 <span data-ttu-id="7c8d4-104">En este ejemplo se usa la palabra clave [unsafe](../../../csharp/language-reference/keywords/unsafe.md), que permite el uso de punteros en el método `Copy`.</span><span class="sxs-lookup"><span data-stu-id="7c8d4-104">This example uses the [unsafe](../../../csharp/language-reference/keywords/unsafe.md) keyword, which enables you to use pointers in the `Copy` method.</span></span> <span data-ttu-id="7c8d4-105">La instrucción [fixed](../../../csharp/language-reference/keywords/fixed-statement.md) se usa para declarar punteros a las matrices de origen y destino.</span><span class="sxs-lookup"><span data-stu-id="7c8d4-105">The [fixed](../../../csharp/language-reference/keywords/fixed-statement.md) statement is used to declare pointers to the source and destination arrays.</span></span> <span data-ttu-id="7c8d4-106">Esto *ancla* la ubicación de las matrices de origen y destino en memoria, para que no puedan ser desplazadas por la recolección de elementos no utilizados.</span><span class="sxs-lookup"><span data-stu-id="7c8d4-106">This *pins* the location of the source and destination arrays in memory so that they will not be moved by garbage collection.</span></span> <span data-ttu-id="7c8d4-107">Estos bloques de memoria para las matrices se desanclan cuando finaliza el bloque `fixed`.</span><span class="sxs-lookup"><span data-stu-id="7c8d4-107">The memory blocks for the arrays are unpinned when the `fixed` block is completed.</span></span> <span data-ttu-id="7c8d4-108">Dado que el método `Copy` en este ejemplo usa la palabra clave `unsafe`, se debe compilar con la opción del compilador **/unsafe**.</span><span class="sxs-lookup"><span data-stu-id="7c8d4-108">Because the `Copy` method in this example uses the `unsafe` keyword, it must be compiled with the **/unsafe** compiler option.</span></span> <span data-ttu-id="7c8d4-109">Para establecer la opción en Visual Studio, haga clic con el botón derecho en el nombre del proyecto y, después, haga clic en **Propiedades**.</span><span class="sxs-lookup"><span data-stu-id="7c8d4-109">To set the option in Visual Studio, right-click the project name, and then click **Properties**.</span></span> <span data-ttu-id="7c8d4-110">En la pestaña **Compilar**, seleccione **Permitir código no seguro**.</span><span class="sxs-lookup"><span data-stu-id="7c8d4-110">On the **Build** tab, select **Allow unsafe code**.</span></span>  
  
## <a name="example"></a><span data-ttu-id="7c8d4-111">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7c8d4-111">Example</span></span>  
 [!code-csharp[csProgGuidePointers#3](../../../csharp/programming-guide/unsafe-code-pointers/codesnippet/CSharp/how-to-use-pointers-to-copy-an-array-of-bytes_1.cs)]  
  
 [!code-csharp[csProgGuidePointers#18](../../../csharp/programming-guide/unsafe-code-pointers/codesnippet/CSharp/how-to-use-pointers-to-copy-an-array-of-bytes_2.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="7c8d4-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="7c8d4-112">See Also</span></span>  
 [<span data-ttu-id="7c8d4-113">Guía de programación de C#</span><span class="sxs-lookup"><span data-stu-id="7c8d4-113">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="7c8d4-114">Código no seguro y punteros</span><span class="sxs-lookup"><span data-stu-id="7c8d4-114">Unsafe Code and Pointers</span></span>](../../../csharp/programming-guide/unsafe-code-pointers/index.md)  
 [<span data-ttu-id="7c8d4-115">/unsafe (Opciones del compilador de C#)</span><span class="sxs-lookup"><span data-stu-id="7c8d4-115">/unsafe (C# Compiler Options)</span></span>](../../../csharp/language-reference/compiler-options/unsafe-compiler-option.md)  
 [<span data-ttu-id="7c8d4-116">Recolección de elementos no utilizados</span><span class="sxs-lookup"><span data-stu-id="7c8d4-116">Garbage Collection</span></span>](../../../standard/garbage-collection/index.md)
