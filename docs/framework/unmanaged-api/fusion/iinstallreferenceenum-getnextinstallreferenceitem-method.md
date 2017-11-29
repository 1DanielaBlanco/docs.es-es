---
title: "IInstallReferenceEnum::GetNextInstallReferenceItem (Método)"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IInstallReferenceEnum.GetNextInstallReferenceItem
api_location: fusion.dll
api_type: COM
f1_keywords: IInstallReferenceEnum::GetNextInstallReferenceItem
helpviewer_keywords:
- IInstallReferenceEnum::GetNextInstallReferenceItem method [.NET Framework fusion]
- GetNextInstallReferenceItem method [.NET Framework fusion]
ms.assetid: ce969c9d-6538-4c34-8784-148ffd99fe7a
topic_type: apiref
caps.latest.revision: "7"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: db7e8bfaf396293f89f4b2e2bb20b5f6f532db19
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/21/2017
---
# <a name="iinstallreferenceenumgetnextinstallreferenceitem-method"></a><span data-ttu-id="0f293-102">IInstallReferenceEnum::GetNextInstallReferenceItem (Método)</span><span class="sxs-lookup"><span data-stu-id="0f293-102">IInstallReferenceEnum::GetNextInstallReferenceItem Method</span></span>
<span data-ttu-id="0f293-103">Obtiene un puntero a la siguiente [IInstallReferenceItem](../../../../docs/framework/unmanaged-api/fusion/iinstallreferenceitem-interface.md) objetos incluidos en este [IInstallReferenceEnum](../../../../docs/framework/unmanaged-api/fusion/iinstallreferenceenum-interface.md) objeto.</span><span class="sxs-lookup"><span data-stu-id="0f293-103">Gets a pointer to the next [IInstallReferenceItem](../../../../docs/framework/unmanaged-api/fusion/iinstallreferenceitem-interface.md) object contained in this [IInstallReferenceEnum](../../../../docs/framework/unmanaged-api/fusion/iinstallreferenceenum-interface.md) object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0f293-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0f293-104">Syntax</span></span>  
  
```  
HRESULT GetNextInstallReferenceItem (  
    [out] IInstallReferenceItem **ppRefItem,  
    [in]  DWORD dwFlags,  
    [in]  LPVOID pvReserved  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="0f293-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0f293-105">Parameters</span></span>  
 `ppRefItem`  
 <span data-ttu-id="0f293-106">[out] El valor devuelto `IInstallReferenceItem` puntero.</span><span class="sxs-lookup"><span data-stu-id="0f293-106">[out] The returned `IInstallReferenceItem` pointer.</span></span>  
  
 `dwFlags`  
 <span data-ttu-id="0f293-107">[in] Reservado para extensibilidad futura.</span><span class="sxs-lookup"><span data-stu-id="0f293-107">[in] Reserved for future extensibility.</span></span> <span data-ttu-id="0f293-108">`dwFlags`debe ser 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="0f293-108">`dwFlags` must be 0 (zero).</span></span>  
  
 `pvReserved`  
 <span data-ttu-id="0f293-109">[in] Reservado para extensibilidad futura.</span><span class="sxs-lookup"><span data-stu-id="0f293-109">[in] Reserved for future extensibility.</span></span> <span data-ttu-id="0f293-110">`pvReserved`debe ser una referencia nula.</span><span class="sxs-lookup"><span data-stu-id="0f293-110">`pvReserved` must be a null reference.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0f293-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f293-111">Requirements</span></span>  
 <span data-ttu-id="0f293-112">**Plataformas:** vea [requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0f293-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0f293-113">**Encabezado:** Fusion.h</span><span class="sxs-lookup"><span data-stu-id="0f293-113">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="0f293-114">**Versiones de .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0f293-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0f293-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="0f293-115">See Also</span></span>  
 [<span data-ttu-id="0f293-116">IInstallReferenceItem (interfaz)</span><span class="sxs-lookup"><span data-stu-id="0f293-116">IInstallReferenceItem Interface</span></span>](../../../../docs/framework/unmanaged-api/fusion/iinstallreferenceitem-interface.md)  
 [<span data-ttu-id="0f293-117">IInstallReferenceEnum (interfaz)</span><span class="sxs-lookup"><span data-stu-id="0f293-117">IInstallReferenceEnum Interface</span></span>](../../../../docs/framework/unmanaged-api/fusion/iinstallreferenceenum-interface.md)