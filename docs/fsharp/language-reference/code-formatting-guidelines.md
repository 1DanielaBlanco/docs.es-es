---
title: "Instrucciones de formato de código (F#)"
description: "Obtenga información acerca de las instrucciones de formato de sangría de código para el lenguaje de programación para mejorar la legibilidad, la estética, la normalización y la compilación de F #."
keywords: "visual f#, f#, programación funcional"
author: cartermp
ms.author: phcart
ms.date: 05/16/2016
ms.topic: language-reference
ms.prod: .net
ms.technology: devlang-fsharp
ms.devlang: fsharp
ms.assetid: 3f79717c-f84e-448d-9ce4-90e40a644ba1
ms.openlocfilehash: cc56c67f356b99defd8dc28770f87be1f58443c5
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/18/2017
---
# <a name="code-formatting-guidelines"></a><span data-ttu-id="8fee7-104">Instrucciones de formato de código</span><span class="sxs-lookup"><span data-stu-id="8fee7-104">Code Formatting Guidelines</span></span>

<span data-ttu-id="8fee7-105">En este tema se resume las instrucciones de sangría del código de F #.</span><span class="sxs-lookup"><span data-stu-id="8fee7-105">This topic summarizes code indentation guidelines for F#.</span></span> <span data-ttu-id="8fee7-106">Dado que el lenguaje F # es sensible a los saltos de línea y sangría, no es simplemente un problema de legibilidad, problema estético o codificación problema de normalización para aplicar formato al código correctamente.</span><span class="sxs-lookup"><span data-stu-id="8fee7-106">Because the F# language is sensitive to line breaks and indentation, it is not just a readability issue, aesthetic issue, or coding standardization issue to format your code correctly.</span></span> <span data-ttu-id="8fee7-107">Debe aplicar formato al código correctamente para que se compile correctamente.</span><span class="sxs-lookup"><span data-stu-id="8fee7-107">You must format your code correctly for it to compile correctly.</span></span>


## <a name="general-rules-for-indentation"></a><span data-ttu-id="8fee7-108">Reglas generales para la sangría</span><span class="sxs-lookup"><span data-stu-id="8fee7-108">General Rules for Indentation</span></span>
<span data-ttu-id="8fee7-109">Cuando es necesario aplicar sangría, debe usar espacios, no tabulaciones.</span><span class="sxs-lookup"><span data-stu-id="8fee7-109">When indentation is required, you must use spaces, not tabs.</span></span> <span data-ttu-id="8fee7-110">Se requiere al menos un espacio.</span><span class="sxs-lookup"><span data-stu-id="8fee7-110">At least one space is required.</span></span> <span data-ttu-id="8fee7-111">Su organización puede crear los estándares de codificación para especificar el número de espacios que se utilizarán para la sangría; es típico de tres o cuatro espacios de sangría en cada nivel donde se produce la sangría.</span><span class="sxs-lookup"><span data-stu-id="8fee7-111">Your organization can create coding standards to specify the number of spaces to use for indentation; three or four spaces of indentation at each level where indentation occurs is typical.</span></span> <span data-ttu-id="8fee7-112">Puede configurar Visual Studio para que coincida con las normas de sangría de su organización cambiando las opciones de la `Options` cuadro de diálogo, que está disponible en la `Tools` menú.</span><span class="sxs-lookup"><span data-stu-id="8fee7-112">You can configure Visual Studio to match your organization's indentation standards by changing the options in the `Options` dialog box, which is available from the `Tools` menu.</span></span> <span data-ttu-id="8fee7-113">En el `Text Editor` nodo, expanda `F#` y, a continuación, haga clic en `Tabs`.</span><span class="sxs-lookup"><span data-stu-id="8fee7-113">In the `Text Editor` node, expand `F#` and then click `Tabs`.</span></span> <span data-ttu-id="8fee7-114">Para obtener una descripción de las opciones disponibles, consulte [opciones, Editor de texto, todos los lenguajes, pestañas](https://msdn.microsoft.com/library/7sffa753.aspx).</span><span class="sxs-lookup"><span data-stu-id="8fee7-114">For a description of the available options, see [Options, Text Editor, All Languages, Tabs](https://msdn.microsoft.com/library/7sffa753.aspx).</span></span>

<span data-ttu-id="8fee7-115">En general, cuando el compilador analiza el código, mantiene una pila interna que indica el nivel de anidamiento actual.</span><span class="sxs-lookup"><span data-stu-id="8fee7-115">In general, when the compiler parses your code, it maintains an internal stack that indicates the current level of nesting.</span></span> <span data-ttu-id="8fee7-116">Cuando se aplica sangría al código, un nuevo nivel de anidamiento se crea o se inserta en la pila interna.</span><span class="sxs-lookup"><span data-stu-id="8fee7-116">When code is indented, a new level of nesting is created, or pushed onto this internal stack.</span></span> <span data-ttu-id="8fee7-117">Cuando una construcción finaliza, se extrae el nivel.</span><span class="sxs-lookup"><span data-stu-id="8fee7-117">When a construct ends, the level is popped.</span></span> <span data-ttu-id="8fee7-118">La sangría es una manera de indicar el final de un nivel y sacar la pila interna, pero algunos tokens provocar también el nivel sacar, como la `end` de palabra clave, o una llave de cierre o un paréntesis.</span><span class="sxs-lookup"><span data-stu-id="8fee7-118">Indentation is one way to signal the end of a level and pop the internal stack, but certain tokens also cause the level to be popped, such as the `end` keyword, or a closing brace or parenthesis.</span></span>

<span data-ttu-id="8fee7-119">Definición de función, el código de una construcción de varias líneas, como una definición de tipo, `try...with` construcción, construcciones de bucle y, se deben aplicar sangría con respecto a la línea de apertura de la construcción.</span><span class="sxs-lookup"><span data-stu-id="8fee7-119">Code in a multiline construct, such as a type definition, function definition, `try...with` construct, and looping constructs, must be indented relative to the opening line of the construct.</span></span> <span data-ttu-id="8fee7-120">La primera línea con sangría, Establece la posición de una columna para el código subsiguiente en la misma construcción.</span><span class="sxs-lookup"><span data-stu-id="8fee7-120">The first indented line establishes a column position for subsequent code in the same construct.</span></span> <span data-ttu-id="8fee7-121">El nivel de sangría se denomina un *contexto*.</span><span class="sxs-lookup"><span data-stu-id="8fee7-121">The indentation level is called a *context*.</span></span> <span data-ttu-id="8fee7-122">La posición de la columna establece una columna mínima, que se conoce como un *línea de contexto*, para las líneas de código siguientes que se encuentran en el mismo contexto.</span><span class="sxs-lookup"><span data-stu-id="8fee7-122">The column position sets a minimum column, referred to as an *offside line*, for subsequent lines of code that are in the same context.</span></span> <span data-ttu-id="8fee7-123">Cuando se encuentra una línea de código que tiene menos sangría que esta posición de columna establecida, el compilador supone que el contexto ha finalizado y que ahora escribe código en el siguiente nivel hacia arriba, en el contexto anterior.</span><span class="sxs-lookup"><span data-stu-id="8fee7-123">When a line of code is encountered that is indented less than this established column position, the compiler assumes that the context has ended and that you are now coding at the next level up, in the previous context.</span></span> <span data-ttu-id="8fee7-124">El término *fuera de contexto* se utiliza para describir la condición en la que una línea de código desencadena el final de una construcción porque lo suficientemente alejado no se aplica una sangría.</span><span class="sxs-lookup"><span data-stu-id="8fee7-124">The term *offside* is used to describe the condition in which a line of code triggers the end of a construct because it is not indented far enough.</span></span> <span data-ttu-id="8fee7-125">En otras palabras, el código a la izquierda de una línea de contexto está fuera de contexto.</span><span class="sxs-lookup"><span data-stu-id="8fee7-125">In other words, code to the left of an offside line is offside.</span></span> <span data-ttu-id="8fee7-126">En el código con sangría correctamente, sacar partido de la regla de fuera de contexto para delinear el final de las construcciones.</span><span class="sxs-lookup"><span data-stu-id="8fee7-126">In correctly indented code, you take advantage of the offside rule in order to delineate the end of constructs.</span></span> <span data-ttu-id="8fee7-127">Si usas sangría incorrectamente, una condición de contexto puede hacer que el compilador emita una advertencia o puede dar lugar a la interpretación incorrecta de su código.</span><span class="sxs-lookup"><span data-stu-id="8fee7-127">If you use indentation improperly, an offside condition can cause the compiler to issue a warning or can lead to the incorrect interpretation of your code.</span></span>

<span data-ttu-id="8fee7-128">Líneas de contexto se determinan como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="8fee7-128">Offside lines are determined as follows.</span></span>


- <span data-ttu-id="8fee7-129">Un `=` token de cancelación asociado con un `let` presenta una línea de contexto en la columna del primer token después de la `=` inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="8fee7-129">An `=` token associated with a `let` introduces an offside line at the column of the first token after the `=` sign.</span></span>


- <span data-ttu-id="8fee7-130">En un `if...then...else` expresión, la posición de la columna del primer token después de la `then` palabra clave o el `else` palabra clave presenta una línea de contexto.</span><span class="sxs-lookup"><span data-stu-id="8fee7-130">In an `if...then...else` expression, the column position of the first token after the `then` keyword or the `else` keyword introduces an offside line.</span></span>


- <span data-ttu-id="8fee7-131">En un `try...with` expresión, el primer token después `try` presenta una línea de contexto.</span><span class="sxs-lookup"><span data-stu-id="8fee7-131">In a `try...with` expression, the first token after `try` introduces an offside line.</span></span>


- <span data-ttu-id="8fee7-132">En un `match` expresión, el primer token después `with` y el primer token después de cada uno `->` introducen líneas de contexto.</span><span class="sxs-lookup"><span data-stu-id="8fee7-132">In a `match` expression, the first token after `with` and the first token after each `->` introduce offside lines.</span></span>


- <span data-ttu-id="8fee7-133">El primer token después `with` en un tipo de extensión presenta una línea de contexto.</span><span class="sxs-lookup"><span data-stu-id="8fee7-133">The first token after `with` in a type extension introduces an offside line.</span></span>


- <span data-ttu-id="8fee7-134">El primer token después de una llave de apertura o paréntesis o después de la `begin` de palabra clave, presenta una línea de contexto.</span><span class="sxs-lookup"><span data-stu-id="8fee7-134">The first token after an opening brace or parenthesis, or after the `begin` keyword, introduces an offside line.</span></span>


- <span data-ttu-id="8fee7-135">El primer carácter de las palabras clave `let`, `if`, y `module` introducen líneas de contexto.</span><span class="sxs-lookup"><span data-stu-id="8fee7-135">The first character in the keywords `let`, `if`, and `module` introduce offside lines.</span></span>


<span data-ttu-id="8fee7-136">Los ejemplos de código siguiente muestran las reglas de sangría.</span><span class="sxs-lookup"><span data-stu-id="8fee7-136">The following code examples illustrate the indentation rules.</span></span> <span data-ttu-id="8fee7-137">En este caso, las instrucciones de impresión se basan en la sangría para asociarlos con el contexto adecuado.</span><span class="sxs-lookup"><span data-stu-id="8fee7-137">Here, the print statements rely on indentation to associate them with the appropriate context.</span></span> <span data-ttu-id="8fee7-138">Cada vez que se desplaza a la sangría, el contexto se extrae y devuelve al contexto anterior.</span><span class="sxs-lookup"><span data-stu-id="8fee7-138">Every time the indentation shifts, the context is popped and returns to the previous context.</span></span> <span data-ttu-id="8fee7-139">Por lo tanto, se imprime un espacio al final de cada iteración; "Listo".</span><span class="sxs-lookup"><span data-stu-id="8fee7-139">Therefore, a space is printed at the end of each iteration; "Done!"</span></span> <span data-ttu-id="8fee7-140">solo se imprime una vez porque la sangría fuera de contexto establece que no es parte del bucle.</span><span class="sxs-lookup"><span data-stu-id="8fee7-140">is only printed one time because the offside indentation establishes that it is not part of the loop.</span></span> <span data-ttu-id="8fee7-141">La impresión de la cadena "Top-Level context" no forma parte de la función.</span><span class="sxs-lookup"><span data-stu-id="8fee7-141">The printing of the string "Top-level context" is not part of the function.</span></span> <span data-ttu-id="8fee7-142">Por lo tanto, se imprime en primer lugar, durante la inicialización estática, antes de llama a la función.</span><span class="sxs-lookup"><span data-stu-id="8fee7-142">Therefore, it is printed first, during the static initialization, before the function is called.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/code-formatting/snippet1.fs)]

<span data-ttu-id="8fee7-143">La salida es la siguiente.</span><span class="sxs-lookup"><span data-stu-id="8fee7-143">The output is as follows.</span></span>

```
Top-level context

(Negative number) Zero 1 2 3 Done!
```

<span data-ttu-id="8fee7-144">Cuando se interrumpe las líneas largas, la continuación de la línea debe tener más sangría la construcción envolvente.</span><span class="sxs-lookup"><span data-stu-id="8fee7-144">When you break long lines, the continuation of the line must be indented farther than the enclosing construct.</span></span> <span data-ttu-id="8fee7-145">Por ejemplo, los argumentos de función deben tener más sangría el primer carácter del nombre de función, como se muestra en el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="8fee7-145">For example, function arguments must be indented farther than the first character of the function name, as shown in the following code.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/code-formatting/snippet2.fs)]

<span data-ttu-id="8fee7-146">Existen excepciones a estas reglas, tal como se describe en la sección siguiente.</span><span class="sxs-lookup"><span data-stu-id="8fee7-146">There are exceptions to these rules, as described in the next section.</span></span>


## <a name="indentation-in-modules"></a><span data-ttu-id="8fee7-147">Sangría en los módulos</span><span class="sxs-lookup"><span data-stu-id="8fee7-147">Indentation in Modules</span></span>
<span data-ttu-id="8fee7-148">Código en un módulo local se debe aplicar la sangría en relación con el módulo, pero no es necesario que el código en un módulo de nivel superior se aplique sangría.</span><span class="sxs-lookup"><span data-stu-id="8fee7-148">Code in a local module must be indented relative to the module, but code in a top-level module does not have to be indented.</span></span> <span data-ttu-id="8fee7-149">Elementos de Namespace no es necesario que tenga la sangría.</span><span class="sxs-lookup"><span data-stu-id="8fee7-149">Namespace elements do not have to be indented.</span></span>

<span data-ttu-id="8fee7-150">Ejemplos de código siguientes ilustran esto.</span><span class="sxs-lookup"><span data-stu-id="8fee7-150">The following code examples illustrate this.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/code-formatting/snippet3.fs)]
[!code-fsharp[Main](../../../samples/snippets/fsharp/code-formatting/snippet4.fs)]

<span data-ttu-id="8fee7-151">Para obtener más información, consulte [módulos](modules.md).</span><span class="sxs-lookup"><span data-stu-id="8fee7-151">For more information, see [Modules](modules.md).</span></span>


## <a name="exceptions-to-the-basic-indentation-rules"></a><span data-ttu-id="8fee7-152">Excepciones a las reglas de sangría básicas</span><span class="sxs-lookup"><span data-stu-id="8fee7-152">Exceptions to the Basic Indentation Rules</span></span>
<span data-ttu-id="8fee7-153">La regla general, como se describe en la sección anterior, es que se debe aplicar sangría código construcciones de varias líneas en relación con la sangría de la primera línea de la construcción, y que el final de la construcción viene determinado por cuando se produce la primera línea de contexto.</span><span class="sxs-lookup"><span data-stu-id="8fee7-153">The general rule, as described in the previous section, is that code in multiline constructs must be indented relative to the indentation of the first line of the construct, and that the end of the construct is determined by when the first offside line occurs.</span></span> <span data-ttu-id="8fee7-154">Una excepción a la regla acerca de la finalización de contextos que algunas construcciones, como el `try...with` expresión, el `if...then...else` expresión y el uso de `and` sintaxis para declarar mutuamente funciones recursivas o tipos, tienen varias partes.</span><span class="sxs-lookup"><span data-stu-id="8fee7-154">An exception to the rule about when contexts end is that some constructs, such as the `try...with` expression, the `if...then...else` expression, and the use of `and` syntax for declaring mutually recursive functions or types, have multiple parts.</span></span> <span data-ttu-id="8fee7-155">Aplica sangría a las partes de una versión posterior, como `then` y `else` en un `if...then...else` expresión, en el mismo nivel que el token que inicia la expresión, pero en lugar de indicar un final del contexto, representa la siguiente parte del mismo contexto.</span><span class="sxs-lookup"><span data-stu-id="8fee7-155">You indent the later parts, such as `then` and `else` in an `if...then...else` expression, at the same level as the token that starts the expression, but instead of indicating an end to the context, it represents the next part of the same context.</span></span> <span data-ttu-id="8fee7-156">Por lo tanto, un `if...then...else` expresión puede escribirse como en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="8fee7-156">Therefore, an `if...then...else` expression can be written as in the following code example.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/code-formatting/snippet5.fs)]

<span data-ttu-id="8fee7-157">La excepción a la regla de fuera de contexto solo se aplica a la `then` y `else` palabras clave.</span><span class="sxs-lookup"><span data-stu-id="8fee7-157">The exception to the offside rule applies only to the `then` and `else` keywords.</span></span> <span data-ttu-id="8fee7-158">Por lo tanto, aunque no es un error para aplicar sangría a la `then` y `else` aún más, no puede aplicar sangría a las líneas de código en un `then` bloque genera una advertencia.</span><span class="sxs-lookup"><span data-stu-id="8fee7-158">Therefore, although it is not an error to indent the `then` and `else` further, failing to indent the lines of code in a `then` block produces a warning.</span></span> <span data-ttu-id="8fee7-159">Esto se muestra en las siguientes líneas de código.</span><span class="sxs-lookup"><span data-stu-id="8fee7-159">This is illustrated in the following lines of code.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/code-formatting/snippet6.fs)]
[!code-fsharp[Main](../../../samples/snippets/fsharp/code-formatting/snippet7.fs)]

<span data-ttu-id="8fee7-160">Para el código en un `else` se aplica el bloque, una regla especial adicional.</span><span class="sxs-lookup"><span data-stu-id="8fee7-160">For code in an `else` block, an additional special rule applies.</span></span> <span data-ttu-id="8fee7-161">Se produce la advertencia en el ejemplo anterior solo en el código en el `then` bloque, no en el código en el `else` bloque.</span><span class="sxs-lookup"><span data-stu-id="8fee7-161">The warning in the previous example occurs only on the code in the `then` block, not on the code in the `else` block.</span></span> <span data-ttu-id="8fee7-162">Esto le permite escribir código que comprueba si hay varias condiciones al principio de una función sin forzar el resto del código de la función, que podría estar en un `else` bloque, que se aplique sangría.</span><span class="sxs-lookup"><span data-stu-id="8fee7-162">This allows you to write code that checks for various conditions at the beginning of a function without forcing the rest of the code for the function, which might be in an `else` block, to be indented.</span></span> <span data-ttu-id="8fee7-163">Por lo tanto, puede escribir lo siguiente sin generar una advertencia.</span><span class="sxs-lookup"><span data-stu-id="8fee7-163">Thus, you can write the following without producing a warning.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/code-formatting/snippet8.fs)]

<span data-ttu-id="8fee7-164">Otro tipo de excepción a la regla que los contextos finalizan cuando una línea no se aplica ninguna sangría como una línea anterior es para los operadores de infijo, como `+` y `|>`.</span><span class="sxs-lookup"><span data-stu-id="8fee7-164">Another exception to the rule that contexts end when a line is not indented as far as a previous line is for infix operators, such as `+` and `|>`.</span></span> <span data-ttu-id="8fee7-165">Líneas que comienzan con los operadores de infijo tienen permiso para iniciar `(1 + oplength)` columnas antes de la posición normal sin desencadenar un final del contexto, donde `oplength` es el número de caracteres que componen el operador.</span><span class="sxs-lookup"><span data-stu-id="8fee7-165">Lines that start with infix operators are permitted to begin `(1 + oplength)` columns before the normal position without triggering an end to the context, where `oplength` is the number of characters that make up the operator.</span></span> <span data-ttu-id="8fee7-166">Esto hace que el primer token después del operador para alinearse con la línea anterior.</span><span class="sxs-lookup"><span data-stu-id="8fee7-166">This causes the first token after the operator to align with the previous line.</span></span>

<span data-ttu-id="8fee7-167">Por ejemplo, en el código siguiente, la `+` símbolo se permite que dos columnas con sangría menor que la línea anterior.</span><span class="sxs-lookup"><span data-stu-id="8fee7-167">For example, in the following code, the `+` symbol is permitted to be indented two columns less than the previous line.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/code-formatting/snippet9.fs)]

<span data-ttu-id="8fee7-168">Aunque la sangría normalmente aumenta cuanto más alto el nivel de anidamiento, hay varias construcciones en la que el compilador permite restablecer la sangría en una posición inferior de la columna.</span><span class="sxs-lookup"><span data-stu-id="8fee7-168">Although indentation usually increases as the level of nesting becomes higher, there are several constructs in which the compiler allows you to reset the indentation to a lower column position.</span></span>

<span data-ttu-id="8fee7-169">Las construcciones que permiten restablecer la posición de columna son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="8fee7-169">The constructs that permit a reset of column position are as follows:</span></span>


- <span data-ttu-id="8fee7-170">Cuerpos de funciones anónimas.</span><span class="sxs-lookup"><span data-stu-id="8fee7-170">Bodies of anonymous functions.</span></span> <span data-ttu-id="8fee7-171">En el código siguiente, la expresión de impresión se inicia en una posición de columna que esté situado más a la izquierda de la `fun` (palabra clave).</span><span class="sxs-lookup"><span data-stu-id="8fee7-171">In the following code, the print expression starts at a column position that is farther to the left than the `fun` keyword.</span></span> <span data-ttu-id="8fee7-172">Sin embargo, la línea no debe comenzar en una columna a la izquierda del inicio del nivel de sangría anterior (es decir, a la izquierda de la `L` en `List`).</span><span class="sxs-lookup"><span data-stu-id="8fee7-172">However, the line must not start at a column to the left of the start of the previous indentation level (that is, to the left of the `L` in `List`).</span></span>
[!code-fsharp[Main](../../../samples/snippets/fsharp/code-formatting/snippet10.fs)]

- <span data-ttu-id="8fee7-173">Construcciones que van entre paréntesis o por `begin` y `end` en un `then` o `else` bloquear de un `if...then...else` expresión, proporciona la sangría no sea inferior a la posición de la columna de la `if` (palabra clave).</span><span class="sxs-lookup"><span data-stu-id="8fee7-173">Constructs enclosed by parentheses or by `begin` and `end` in a `then` or `else` block of an `if...then...else` expression, provided the indentation is no less than the column position of the `if` keyword.</span></span> <span data-ttu-id="8fee7-174">Esta excepción permite un estilo de codificación en la que un paréntesis de apertura o `begin` se utiliza al final de una línea después de `then` o `else`.</span><span class="sxs-lookup"><span data-stu-id="8fee7-174">This exception allows for a coding style in which an opening parenthesis or `begin` is used at the end of a line after `then` or `else`.</span></span>


- <span data-ttu-id="8fee7-175">Cuerpos de módulos, clases, interfaces y estructuras delimitados por `begin...end`, `{...}`, `class...end`, o `interface...end`.</span><span class="sxs-lookup"><span data-stu-id="8fee7-175">Bodies of modules, classes, interfaces, and structures delimited by `begin...end`, `{...}`, `class...end`, or `interface...end`.</span></span> <span data-ttu-id="8fee7-176">Esto permite un estilo en el que puede ser la palabra clave de apertura de una definición de tipo en la misma línea que el nombre del tipo sin forzar el cuerpo entero sea más la palabra clave de apertura sangría.</span><span class="sxs-lookup"><span data-stu-id="8fee7-176">This allows for a style in which the opening keyword of a type definition can be on the same line as the type name without forcing the whole body to be indented farther than the opening keyword.</span></span>
[!code-fsharp[Main](../../../samples/snippets/fsharp/code-formatting/snippet13.fs)]


## <a name="see-also"></a><span data-ttu-id="8fee7-177">Vea también</span><span class="sxs-lookup"><span data-stu-id="8fee7-177">See Also</span></span>
[<span data-ttu-id="8fee7-178">Referencia del lenguaje F#</span><span class="sxs-lookup"><span data-stu-id="8fee7-178">F# Language Reference</span></span>](index.md)