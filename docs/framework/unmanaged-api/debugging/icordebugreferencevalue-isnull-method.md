---
title: ICorDebugReferenceValue::IsNull (Método)
ms.date: 03/30/2017
api_name:
- ICorDebugReferenceValue.IsNull
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugReferenceValue::IsNull
helpviewer_keywords:
- IsNull method, ICorDebugReferenceValue interface [.NET Framework debugging]
- ICorDebugReferenceValue::IsNull method [.NET Framework debugging]
ms.assetid: 99e8c8d7-a1c0-47c8-9dbd-03e0b2bcb4d5
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2c82c72350931bf3aed8ec6699cd0af834798e92
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/04/2018
ms.locfileid: "33417220"
---
# <a name="icordebugreferencevalueisnull-method"></a><span data-ttu-id="2b53f-102">ICorDebugReferenceValue::IsNull (Método)</span><span class="sxs-lookup"><span data-stu-id="2b53f-102">ICorDebugReferenceValue::IsNull Method</span></span>
<span data-ttu-id="2b53f-103">Obtiene un valor que indica si este ICorDebugReferenceValue es un valor null, en cuyo caso el `ICorDebugReferenceValue` no señala a un objeto.</span><span class="sxs-lookup"><span data-stu-id="2b53f-103">Gets a value that indicates whether this ICorDebugReferenceValue is a null value, in which case the `ICorDebugReferenceValue` does not point to an object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2b53f-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2b53f-104">Syntax</span></span>  
  
```  
HRESULT IsNull (  
    [out] BOOL   *pbNull  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="2b53f-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2b53f-105">Parameters</span></span>  
 `pbNull`  
 <span data-ttu-id="2b53f-106">[out] Un puntero a un valor booleano que es `true` si `ICorDebugReferenceValue` objeto es null; en caso contrario, `pbNull` es `false`.</span><span class="sxs-lookup"><span data-stu-id="2b53f-106">[out] A pointer to a Boolean value that is `true` if this `ICorDebugReferenceValue` object is null; otherwise, `pbNull` is `false`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2b53f-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b53f-107">Requirements</span></span>  
 <span data-ttu-id="2b53f-108">**Plataformas:** vea [requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="2b53f-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2b53f-109">**Encabezado:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="2b53f-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="2b53f-110">**Biblioteca:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="2b53f-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="2b53f-111">**Versiones de .NET framework:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2b53f-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
