---
title: "ICorDebugValue::GetAddress (Método)"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugValue.GetAddress
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugValue::GetAddress
helpviewer_keywords:
- ICorDebugValue::GetAddress method [.NET Framework debugging]
- GetAddress method, ICorDebugValue interface [.NET Framework debugging]
ms.assetid: a247c792-45e1-4538-9e1f-b46acca4a463
topic_type: apiref
caps.latest.revision: "11"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 7018dcb41f46d5407549f5c3d3029716781014e3
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/18/2017
---
# <a name="icordebugvaluegetaddress-method"></a><span data-ttu-id="2dedf-102">ICorDebugValue::GetAddress (Método)</span><span class="sxs-lookup"><span data-stu-id="2dedf-102">ICorDebugValue::GetAddress Method</span></span>
<span data-ttu-id="2dedf-103">Obtiene la dirección de este objeto de "ICorDebugValue", que está en el proceso que se está depurando.</span><span class="sxs-lookup"><span data-stu-id="2dedf-103">Gets the address of this "ICorDebugValue" object, which is in the process of being debugged.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2dedf-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2dedf-104">Syntax</span></span>  
  
```  
HRESULT GetAddress (  
    [out] CORDB_ADDRESS   *pAddress  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="2dedf-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2dedf-105">Parameters</span></span>  
 `pAddress`  
 <span data-ttu-id="2dedf-106">[out] Puntero a un `CORDB_ADDRESS` objeto que especifica la dirección de este objeto de valor.</span><span class="sxs-lookup"><span data-stu-id="2dedf-106">[out] Pointer to a `CORDB_ADDRESS` object that specifies the address of this value object.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="2dedf-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2dedf-107">Remarks</span></span>  
 <span data-ttu-id="2dedf-108">Si el valor no está disponible, se devuelve 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="2dedf-108">If the value is unavailable, 0 (zero) is returned.</span></span> <span data-ttu-id="2dedf-109">Esto puede suceder si el valor es al menos parcialmente en los registros o se almacenan en un identificador del recolector de elementos no utilizados (`GCHandle`).</span><span class="sxs-lookup"><span data-stu-id="2dedf-109">This could happen if the value is at least partly in registers or stored in a garbage collector handle (`GCHandle`).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2dedf-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2dedf-110">Requirements</span></span>  
 <span data-ttu-id="2dedf-111">**Plataformas:** vea [requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="2dedf-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2dedf-112">**Encabezado:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="2dedf-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="2dedf-113">**Biblioteca:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="2dedf-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="2dedf-114">**Versiones de .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2dedf-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2dedf-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="2dedf-115">See Also</span></span>  
 
