---
title: Espacios de nombres (F#)
description: "Obtenga información acerca de cómo un espacio de nombres de F # permite organizar el código en las áreas de funcionalidad relacionada por lo que le permite asociar un nombre a una agrupación de elementos de programa."
keywords: "visual f#, f#, programación funcional"
author: cartermp
ms.author: phcart
ms.date: 04/24/2017
ms.topic: language-reference
ms.prod: .net
ms.technology: devlang-fsharp
ms.devlang: fsharp
ms.assetid: ea42156f-e1b9-4535-9383-b45f46f3f7ca
ms.openlocfilehash: 4378afebe6fd0d9317f734457576dc75d7488bf0
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/18/2017
---
# <a name="namespaces"></a><span data-ttu-id="7de4e-104">Espacios de nombres</span><span class="sxs-lookup"><span data-stu-id="7de4e-104">Namespaces</span></span>

<span data-ttu-id="7de4e-105">Un espacio de nombres permite organizar el código en áreas de funcionalidad relacionada, lo que permite adjuntar un nombre a una agrupación de elementos de programa.</span><span class="sxs-lookup"><span data-stu-id="7de4e-105">A namespace lets you organize code into areas of related functionality by enabling you to attach a name to a grouping of program elements.</span></span>


## <a name="syntax"></a><span data-ttu-id="7de4e-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7de4e-106">Syntax</span></span>

```fsharp
namespace [parent-namespaces.]identifier
```

## <a name="remarks"></a><span data-ttu-id="7de4e-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7de4e-107">Remarks</span></span>
<span data-ttu-id="7de4e-108">Si desea colocar código en un espacio de nombres, la primera declaración en el archivo debe declarar el espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="7de4e-108">If you want to put code in a namespace, the first declaration in the file must declare the namespace.</span></span> <span data-ttu-id="7de4e-109">El contenido de todo el archivo, a continuación, pasan a formar parte del espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="7de4e-109">The contents of the entire file then become part of the namespace.</span></span>

<span data-ttu-id="7de4e-110">Espacios de nombres no pueden contener directamente valores y funciones.</span><span class="sxs-lookup"><span data-stu-id="7de4e-110">Namespaces cannot directly contain values and functions.</span></span> <span data-ttu-id="7de4e-111">En su lugar, valores y funciones que deben incluirse en los módulos y los módulos se incluyen en los espacios de nombres.</span><span class="sxs-lookup"><span data-stu-id="7de4e-111">Instead, values and functions must be included in modules, and modules are included in namespaces.</span></span> <span data-ttu-id="7de4e-112">Espacios de nombres pueden contener tipos de módulos.</span><span class="sxs-lookup"><span data-stu-id="7de4e-112">Namespaces can contain types, modules.</span></span>

<span data-ttu-id="7de4e-113">Espacios de nombres pueden declararse explícitamente con la palabra clave namespace o implícitamente al declarar un módulo.</span><span class="sxs-lookup"><span data-stu-id="7de4e-113">Namespaces can be declared explicitly with the namespace keyword, or implicitly when declaring a module.</span></span> <span data-ttu-id="7de4e-114">Para declarar un espacio de nombres explícitamente, utilice la palabra clave de espacio de nombres seguida del nombre de espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="7de4e-114">To declare a namespace explicitly, use the namespace keyword followed by the namespace name.</span></span> <span data-ttu-id="7de4e-115">En el ejemplo siguiente se muestra un archivo de código que declara un espacio de nombres Widgets con un tipo y un módulo incluido en ese espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="7de4e-115">The following example shows a code file that declares a namespace Widgets with a type and a module included in that namespace.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet6406.fs)]

<span data-ttu-id="7de4e-116">Si todo el contenido del archivo se encuentran en un módulo, también puede declarar espacios de nombres implícitamente mediante el uso de la `module` (palabra clave) y proporcionar el nuevo nombre de espacio de nombres en el nombre completo del módulo.</span><span class="sxs-lookup"><span data-stu-id="7de4e-116">If the entire contents of the file are in one module, you can also declare namespaces implicitly by using the `module` keyword and providing the new namespace name in the fully qualified module name.</span></span> <span data-ttu-id="7de4e-117">En el ejemplo siguiente se muestra un archivo de código que declara un espacio de nombres `Widgets` y un módulo `WidgetsModule`, que contiene una función.</span><span class="sxs-lookup"><span data-stu-id="7de4e-117">The following example shows a code file that declares a namespace `Widgets` and a module `WidgetsModule`, which contains a function.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet6401.fs)]

<span data-ttu-id="7de4e-118">El código siguiente es equivalente al código anterior, pero el módulo es una declaración de módulo local.</span><span class="sxs-lookup"><span data-stu-id="7de4e-118">The following code is equivalent to the preceding code, but the module is a local module declaration.</span></span> <span data-ttu-id="7de4e-119">En ese caso, el espacio de nombres debe aparecer en su propia línea.</span><span class="sxs-lookup"><span data-stu-id="7de4e-119">In that case, the namespace must appear on its own line.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/namespaces/snippet6402.fs)]

<span data-ttu-id="7de4e-120">Si se requiere más de un módulo en el mismo archivo en uno o varios espacios de nombres, debe utilizar las declaraciones de módulo local.</span><span class="sxs-lookup"><span data-stu-id="7de4e-120">If more than one module is required in the same file in one or more namespaces, you must use local module declarations.</span></span> <span data-ttu-id="7de4e-121">Cuando utiliza las declaraciones de módulo local, no puede usar el espacio de nombres completo en las declaraciones de módulo.</span><span class="sxs-lookup"><span data-stu-id="7de4e-121">When you use local module declarations, you cannot use the qualified namespace in the module declarations.</span></span> <span data-ttu-id="7de4e-122">El código siguiente muestra un archivo que tiene una declaración de espacio de nombres y dos declaraciones de módulo locales.</span><span class="sxs-lookup"><span data-stu-id="7de4e-122">The following code shows a file that has a namespace declaration and two local module declarations.</span></span> <span data-ttu-id="7de4e-123">En este caso, los módulos están contenidos directamente en el espacio de nombres; No hay ningún módulo creado implícitamente que tiene el mismo nombre que el archivo.</span><span class="sxs-lookup"><span data-stu-id="7de4e-123">In this case, the modules are contained directly in the namespace; there is no implicitly created module that has the same name as the file.</span></span> <span data-ttu-id="7de4e-124">Cualquier otro código en el archivo, como un `do` enlace, está en el espacio de nombres pero no en los módulos internos, por lo que necesita calificar el miembro de módulo `widgetFunction` utilizando el nombre del módulo.</span><span class="sxs-lookup"><span data-stu-id="7de4e-124">Any other code in the file, such as a `do` binding, is in the namespace but not in the inner modules, so you need to qualify the module member `widgetFunction` by using the module name.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet6403.fs)]

<span data-ttu-id="7de4e-125">La salida de este ejemplo es la siguiente.</span><span class="sxs-lookup"><span data-stu-id="7de4e-125">The output of this example is as follows.</span></span>

```fsharp
Module1 10 20
Module2 5 6
```

<span data-ttu-id="7de4e-126">Para obtener más información, consulte [módulos](modules.md).</span><span class="sxs-lookup"><span data-stu-id="7de4e-126">For more information, see [Modules](modules.md).</span></span>

## <a name="nested-namespaces"></a><span data-ttu-id="7de4e-127">Espacios de nombres anidados</span><span class="sxs-lookup"><span data-stu-id="7de4e-127">Nested Namespaces</span></span>
<span data-ttu-id="7de4e-128">Cuando se crea un espacio de nombres anidado, debe calificar totalmente.</span><span class="sxs-lookup"><span data-stu-id="7de4e-128">When you create a nested namespace, you must fully qualify it.</span></span> <span data-ttu-id="7de4e-129">En caso contrario, cree un nuevo espacio de nombres de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="7de4e-129">Otherwise, you create a new top-level namespace.</span></span> <span data-ttu-id="7de4e-130">Sangría se omite en las declaraciones de espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="7de4e-130">Indentation is ignored in namespace declarations.</span></span>

<span data-ttu-id="7de4e-131">En el ejemplo siguiente se muestra cómo declarar un espacio de nombres anidado.</span><span class="sxs-lookup"><span data-stu-id="7de4e-131">The following example shows how to declare a nested namespace.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet6404.fs)]

## <a name="namespaces-in-files-and-assemblies"></a><span data-ttu-id="7de4e-132">Espacios de nombres de archivos y ensamblados</span><span class="sxs-lookup"><span data-stu-id="7de4e-132">Namespaces in Files and Assemblies</span></span>
<span data-ttu-id="7de4e-133">Espacios de nombres pueden abarcar varios archivos en un solo proyecto o de compilación.</span><span class="sxs-lookup"><span data-stu-id="7de4e-133">Namespaces can span multiple files in a single project or compilation.</span></span> <span data-ttu-id="7de4e-134">El término *fragmento de espacio de nombres* describe la parte del espacio de nombres que se incluye en un archivo.</span><span class="sxs-lookup"><span data-stu-id="7de4e-134">The term *namespace fragment* describes the part of a namespace that is included in one file.</span></span> <span data-ttu-id="7de4e-135">Espacios de nombres también pueden abarcar varios ensamblados.</span><span class="sxs-lookup"><span data-stu-id="7de4e-135">Namespaces can also span multiple assemblies.</span></span> <span data-ttu-id="7de4e-136">Por ejemplo, el `System` espacio de nombres incluye todo .NET Framework, que abarca muchos ensamblados y contiene muchos espacios de nombres anidados.</span><span class="sxs-lookup"><span data-stu-id="7de4e-136">For example, the `System` namespace includes the whole .NET Framework, which spans many assemblies and contains many nested namespaces.</span></span>


## <a name="global-namespace"></a><span data-ttu-id="7de4e-137">Namespace global</span><span class="sxs-lookup"><span data-stu-id="7de4e-137">Global Namespace</span></span>
<span data-ttu-id="7de4e-138">Usar el espacio de nombres predefinido `global` colocar los nombres en el espacio de nombres de nivel superior. NET.</span><span class="sxs-lookup"><span data-stu-id="7de4e-138">You use the predefined namespace `global` to put names in the .NET top-level namespace.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet6407.fs)]

<span data-ttu-id="7de4e-139">También puede utilizar global para hacer referencia el espacio de nombres .NET nivel superior, por ejemplo, para resolver conflictos de nombres con otros espacios de nombres.</span><span class="sxs-lookup"><span data-stu-id="7de4e-139">You can also use global to reference the top-level .NET namespace, for example, to resolve name conflicts with other namespaces.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet6408.fs)]

##

<span data-ttu-id="7de4e-140">F # 4.1 presenta la noción de espacios de nombres que permiten todo el código independiente para ser mutuamente recursivas.</span><span class="sxs-lookup"><span data-stu-id="7de4e-140">F# 4.1 introduces the notion of namespaces which allow for all contained code to be mutually recursive.</span></span>  <span data-ttu-id="7de4e-141">Esto se realiza mediante `namespace rec`.</span><span class="sxs-lookup"><span data-stu-id="7de4e-141">This is done via `namespace rec`.</span></span>  <span data-ttu-id="7de4e-142">El uso de `namespace rec` puede solucionar algunos problemas no se pueda escribir código mutuamente referencial entre tipos y módulos.</span><span class="sxs-lookup"><span data-stu-id="7de4e-142">Use of `namespace rec` can alleviate some pains in not being able to write mutually referential code between types and modules.</span></span>  <span data-ttu-id="7de4e-143">El siguiente es un ejemplo de esto:</span><span class="sxs-lookup"><span data-stu-id="7de4e-143">The following is an example of this:</span></span>

```fsharp
namespace rec MutualReferences

type Orientation = Up | Down
type PeelState = Peeled | Unpeeled

// This exception depends on the type below.
exception DontSqueezeTheBananaException of Banana

type BananaPeel() = class end

type Banana(orientation : Orientation) =
    member val IsPeeled = false with get, set
    member val Orientation = orientation with get, set
    member val Sides: PeelState list = [ Unpeeled; Unpeeled; Unpeeled; Unpeeled] with get, set
    
    member self.Peel() = BananaHelpers.peel self // Note the dependency on the BananaHelpers module.
    member self.SqueezeJuiceOut() = raise (DontSqueezeTheBananaException self) // This member depends on the exception above.

module BananaHelpers =
    let peel (b : Banana) =
        let flip banana =
            match banana.Orientation with
            | Up -> 
                banana.Orientation <- Down
                banana
            | Down -> banana

        let peelSides banana =
            for side in banana.Sides do
                if side = Unpeeled then
                    side <- Peeled

        match b.Orientation with
        | Up ->   b |> flip |> peelSides
        | Down -> b |> peelSides
```

<span data-ttu-id="7de4e-144">Tenga en cuenta que la excepción `DontSqueezeTheBananaException` y la clase `Banana` ambos hacen referencia a entre sí.</span><span class="sxs-lookup"><span data-stu-id="7de4e-144">Note that the exception `DontSqueezeTheBananaException` and the class `Banana` both refer to each other.</span></span>  <span data-ttu-id="7de4e-145">Además, el módulo `BananaHelpers` y la clase `Banana` también hacer referencia a entre sí.</span><span class="sxs-lookup"><span data-stu-id="7de4e-145">Additionally, the module `BananaHelpers` and the class `Banana` also refer to each other.</span></span>  <span data-ttu-id="7de4e-146">Esto no sería posible expresar en F #, si quita el `rec` palabra clave de la `MutualReferences` espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="7de4e-146">This would not be possible to express in F# if you removed the `rec` keyword from the `MutualReferences` namespace.</span></span>

<span data-ttu-id="7de4e-147">Esta característica también está disponible para su nivel superior [módulos](modules.md) en F # 4.1 o posterior.</span><span class="sxs-lookup"><span data-stu-id="7de4e-147">This feature is also available for top-level [Modules](modules.md) in F# 4.1 or higher.</span></span>

## <a name="see-also"></a><span data-ttu-id="7de4e-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="7de4e-148">See Also</span></span>
[<span data-ttu-id="7de4e-149">Referencia del lenguaje F#</span><span class="sxs-lookup"><span data-stu-id="7de4e-149">F# Language Reference</span></span>](index.md)

[<span data-ttu-id="7de4e-150">Módulos</span><span class="sxs-lookup"><span data-stu-id="7de4e-150">Modules</span></span>](modules.md)

[<span data-ttu-id="7de4e-151">F # RFC FS-1009 - permitir módulos y tipos mutuamente referenciales a través de ámbitos mayores de archivos</span><span class="sxs-lookup"><span data-stu-id="7de4e-151">F# RFC FS-1009 - Allow mutually referential types and modules over larger scopes within files</span></span>](https://github.com/fsharp/fslang-design/blob/master/FSharp-4.1/FS-1009-mutually-referential-types-and-modules-single-scope.md)