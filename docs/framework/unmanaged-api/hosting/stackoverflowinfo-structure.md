---
title: StackOverflowInfo (Estructura)
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: StackOverflowInfo
api_location: mscoree.dll
api_type: COM
f1_keywords: StackOverflowInfo
helpviewer_keywords: StackOverflowInfo structure [.NET Framework hosting]
ms.assetid: 519389f2-0217-436c-99d4-93a76ebce5b5
topic_type: apiref
caps.latest.revision: "9"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 102f744ecc769a10161cd20767e8e49c838252a7
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/18/2017
---
# <a name="stackoverflowinfo-structure"></a><span data-ttu-id="59e8c-102">StackOverflowInfo (Estructura)</span><span class="sxs-lookup"><span data-stu-id="59e8c-102">StackOverflowInfo Structure</span></span>
<span data-ttu-id="59e8c-103">Almacena el tipo de desbordamiento que se produjo y obtener información sobre la excepción que se produce porque el desbordamiento.</span><span class="sxs-lookup"><span data-stu-id="59e8c-103">Stores the type of overflow that occurred and information on the exception that was thrown due to the overflow.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="59e8c-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="59e8c-104">Syntax</span></span>  
  
```  
typedef struct _StackOverflowInfo {  
    StackOverflowType   soType;  
    EXCEPTION_POINTERS  *pExceptionInfo;  
} StackOverflowInfo;  
```  
  
## <a name="members"></a><span data-ttu-id="59e8c-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="59e8c-105">Members</span></span>  
  
|<span data-ttu-id="59e8c-106">Miembro</span><span class="sxs-lookup"><span data-stu-id="59e8c-106">Member</span></span>|<span data-ttu-id="59e8c-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="59e8c-107">Description</span></span>|  
|------------|-----------------|  
|`soType`|<span data-ttu-id="59e8c-108">Un valor de la [StackOverflowType](../../../../docs/framework/unmanaged-api/hosting/stackoverflowtype-enumeration.md) enumeración que especifica el tipo de desbordamiento.</span><span class="sxs-lookup"><span data-stu-id="59e8c-108">A value of the [StackOverflowType](../../../../docs/framework/unmanaged-api/hosting/stackoverflowtype-enumeration.md) enumeration that specifies the type of overflow.</span></span>|  
|`pExceptionInfo`|<span data-ttu-id="59e8c-109">Un puntero a Win32 `EXCEPTION_POINTERS` objeto, que contiene un registro de excepciones con una descripción independiente del equipo de una excepción y un registro de contexto con una descripción de dependientes del equipo del contexto del procesador en el momento de la excepción.</span><span class="sxs-lookup"><span data-stu-id="59e8c-109">A pointer to a Win32 `EXCEPTION_POINTERS` object, which contains an exception record with a machine-independent description of an exception and a context record with a machine-dependent description of the processor context at the time of the exception.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="59e8c-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="59e8c-110">Remarks</span></span>  
 <span data-ttu-id="59e8c-111">A `StackOverflowInfo` objeto se pasa a la [IActionOnCLREvent:: OnEvent](../../../../docs/framework/unmanaged-api/hosting/iactiononclrevent-onevent-method.md) método para `Event_StackOverflow` eventos.</span><span class="sxs-lookup"><span data-stu-id="59e8c-111">A `StackOverflowInfo` object is passed to the [IActionOnCLREvent::OnEvent](../../../../docs/framework/unmanaged-api/hosting/iactiononclrevent-onevent-method.md) method for `Event_StackOverflow` events.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="59e8c-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59e8c-112">Requirements</span></span>  
 <span data-ttu-id="59e8c-113">**Plataformas:** vea [requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="59e8c-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="59e8c-114">**Encabezado:** MSCorEE.idl</span><span class="sxs-lookup"><span data-stu-id="59e8c-114">**Header:** MSCorEE.idl</span></span>  
  
 <span data-ttu-id="59e8c-115">**Biblioteca:** incluye como recurso en MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="59e8c-115">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="59e8c-116">**Versiones de .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="59e8c-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="59e8c-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="59e8c-117">See Also</span></span>  
 [<span data-ttu-id="59e8c-118">Estructuras de hospedaje</span><span class="sxs-lookup"><span data-stu-id="59e8c-118">Hosting Structures</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-structures.md)