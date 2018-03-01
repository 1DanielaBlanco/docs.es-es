---
title: "ICorDebugReferenceValue::SetValue (Método)"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology:
- dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name:
- ICorDebugReferenceValue.SetValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugReferenceValue::SetValue
helpviewer_keywords:
- SetValue method, ICorDebugReferenceValue interface [.NET Framework debugging]
- ICorDebugReferenceValue::SetValue method [.NET Framework debugging]
ms.assetid: 3d3f6eec-d772-401f-a028-1a2ecdc31e95
topic_type:
- apiref
caps.latest.revision: 
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: 71250155d0c71b9b8f9cddad57d0c74b4ffc7991
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/22/2017
---
# <a name="icordebugreferencevaluesetvalue-method"></a><span data-ttu-id="4b345-102">ICorDebugReferenceValue::SetValue (Método)</span><span class="sxs-lookup"><span data-stu-id="4b345-102">ICorDebugReferenceValue::SetValue Method</span></span>
<span data-ttu-id="4b345-103">Establece la dirección de memoria especificada.</span><span class="sxs-lookup"><span data-stu-id="4b345-103">Sets the specified memory address.</span></span> <span data-ttu-id="4b345-104">Es decir, este método establece ICorDebugReferenceValue para que señale a un objeto.</span><span class="sxs-lookup"><span data-stu-id="4b345-104">That is, this method sets this ICorDebugReferenceValue to point to an object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4b345-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4b345-105">Syntax</span></span>  
  
```  
HRESULT SetValue (  
    [in] CORDB_ADDRESS    value  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="4b345-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4b345-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="4b345-107">[in] A `CORDB_ADDRESS` valor que especifica la dirección del objeto a la que se `ICorDebugReferenceValue` puntos.</span><span class="sxs-lookup"><span data-stu-id="4b345-107">[in] A `CORDB_ADDRESS` value that specifies the address of the object to which this `ICorDebugReferenceValue` points.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4b345-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b345-108">Requirements</span></span>  
 <span data-ttu-id="4b345-109">**Plataformas:** vea [requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="4b345-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4b345-110">**Encabezado:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="4b345-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="4b345-111">**Biblioteca:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="4b345-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="4b345-112">**Versiones de .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4b345-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
