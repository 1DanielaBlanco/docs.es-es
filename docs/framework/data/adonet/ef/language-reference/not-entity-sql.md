---
title: '! (NOT) (Entity SQL)'
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-ado
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: a1447a34-df06-4393-93c3-0612ebd41abc
caps.latest.revision: "3"
author: JennieHubbard
ms.author: jhubbard
manager: jhubbard
ms.openlocfilehash: 1f10e65e284a14d6d86f9722cf44f080321fa0b2
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/18/2017
---
# <a name="-not-entity-sql"></a><span data-ttu-id="c0520-103">!</span><span class="sxs-lookup"><span data-stu-id="c0520-103">!</span></span> <span data-ttu-id="c0520-104">(NOT) (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="c0520-104">(NOT) (Entity SQL)</span></span>
<span data-ttu-id="c0520-105">Niega una expresión `Boolean` .</span><span class="sxs-lookup"><span data-stu-id="c0520-105">Negates a `Boolean` expression.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c0520-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c0520-106">Syntax</span></span>  
  
```  
NOT boolean_expression  
or  
! boolean_expression  
```  
  
## <a name="arguments"></a><span data-ttu-id="c0520-107">Argumentos</span><span class="sxs-lookup"><span data-stu-id="c0520-107">Arguments</span></span>  
 `boolean_expression`  
 <span data-ttu-id="c0520-108">Cualquier expresión válida que devuelve un valor booleano.</span><span class="sxs-lookup"><span data-stu-id="c0520-108">Any valid expression that returns a Boolean.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="c0520-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c0520-109">Remarks</span></span>  
 <span data-ttu-id="c0520-110">El signo de admiración (!) tiene la misma funcionalidad que el operador NOT.</span><span class="sxs-lookup"><span data-stu-id="c0520-110">The exclamation point (!) has the same functionality as the NOT operator.</span></span>  
  
## <a name="example"></a><span data-ttu-id="c0520-111">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c0520-111">Example</span></span>  
 <span data-ttu-id="c0520-112">La siguiente consulta de Entity SQL usa el operador NOT para negar una expresión `Boolean` .</span><span class="sxs-lookup"><span data-stu-id="c0520-112">The following Entity SQL query uses the NOT operator to negates a `Boolean` expression.</span></span> <span data-ttu-id="c0520-113">La consulta se basa en el modelo AdventureWorks Sales.</span><span class="sxs-lookup"><span data-stu-id="c0520-113">The query is based on the AdventureWorks Sales Model.</span></span> <span data-ttu-id="c0520-114">Para compilar y ejecutar esta consulta, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="c0520-114">To compile and run this query, follow these steps:</span></span>  
  
1.  <span data-ttu-id="c0520-115">Siga el procedimiento de [How to: Execute a Query that Returns StructuralType Results](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span><span class="sxs-lookup"><span data-stu-id="c0520-115">Follow the procedure in [How to: Execute a Query that Returns StructuralType Results](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span></span>  
  
2.  <span data-ttu-id="c0520-116">Pase la consulta siguiente como argumento al método `ExecuteStructuralTypeQuery` :</span><span class="sxs-lookup"><span data-stu-id="c0520-116">Pass the following query as an argument to the `ExecuteStructuralTypeQuery` method:</span></span>  
  
 [!code-csharp[DP EntityServices Concepts 2#NOT](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#not)]  
  
## <a name="see-also"></a><span data-ttu-id="c0520-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="c0520-117">See Also</span></span>  
 [<span data-ttu-id="c0520-118">Referencia de Entity SQL</span><span class="sxs-lookup"><span data-stu-id="c0520-118">Entity SQL Reference</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
