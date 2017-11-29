---
title: "IAssemblyName::GetVersion (Método)"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IAssemblyName.GetVersion
api_location: fusion.dll
api_type: COM
f1_keywords: IAssemblyName::GetVersion
helpviewer_keywords:
- IAssemblyName::GetVersion method [.NET Framework fusion]
- GetVersion method, IAssemblyName interface [.NET Framework fusion]
ms.assetid: 42230928-2c33-41fd-9519-d96efef6c7af
topic_type: apiref
caps.latest.revision: "7"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 5a843ca1ebc12b0ae9aaf1d9dbb4e5d845fb61fe
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/18/2017
---
# <a name="iassemblynamegetversion-method"></a><span data-ttu-id="cf1b2-102">IAssemblyName::GetVersion (Método)</span><span class="sxs-lookup"><span data-stu-id="cf1b2-102">IAssemblyName::GetVersion Method</span></span>
<span data-ttu-id="cf1b2-103">Obtiene la información de versión del ensamblado que hace referencia esta [IAssemblyName](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-interface.md) objeto.</span><span class="sxs-lookup"><span data-stu-id="cf1b2-103">Gets the version information for the assembly referenced by this [IAssemblyName](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-interface.md) object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cf1b2-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cf1b2-104">Syntax</span></span>  
  
```  
HRESULT GetVersion (  
    [out] LPDWORD pdwVersionHi,  
    [out] LPDWORD pdwVersionLow  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="cf1b2-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cf1b2-105">Parameters</span></span>  
 `pdwVersionHi`  
 <span data-ttu-id="cf1b2-106">[out] Los 32 bits superiores de la versión.</span><span class="sxs-lookup"><span data-stu-id="cf1b2-106">[out] The high 32 bits of the version.</span></span>  
  
 `pdwVersionLow`  
 <span data-ttu-id="cf1b2-107">[out] Los 32 bits inferiores de la versión.</span><span class="sxs-lookup"><span data-stu-id="cf1b2-107">[out] The low 32 bits of the version.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="cf1b2-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf1b2-108">Requirements</span></span>  
 <span data-ttu-id="cf1b2-109">**Plataformas:** vea [requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="cf1b2-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="cf1b2-110">**Encabezado:** Fusion.h</span><span class="sxs-lookup"><span data-stu-id="cf1b2-110">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="cf1b2-111">**Versiones de .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="cf1b2-111">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cf1b2-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="cf1b2-112">See Also</span></span>  
 [<span data-ttu-id="cf1b2-113">IAssemblyName (interfaz)</span><span class="sxs-lookup"><span data-stu-id="cf1b2-113">IAssemblyName Interface</span></span>](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-interface.md)
