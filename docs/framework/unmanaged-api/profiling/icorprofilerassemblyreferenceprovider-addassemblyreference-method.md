---
title: "ICorProfilerAssemblyReferenceProvider::AddAssemblyReference (Método)"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
dev_langs: cpp
api_name: ICorProfilerAssemblyReferenceProvider.AddAssemblyReference
api_location: mscorwks.dll
api_type: COM
ms.assetid: 3d5af8e7-c337-48f4-9fa6-97c83878b9b1
topic_type: apiref
caps.latest.revision: "5"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: f67ef9832a7fb1ff1ec153a4f8aff74079e3b76c
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/21/2017
---
# <a name="icorprofilerassemblyreferenceprovideraddassemblyreference-method"></a><span data-ttu-id="a68dc-102">ICorProfilerAssemblyReferenceProvider::AddAssemblyReference (Método)</span><span class="sxs-lookup"><span data-stu-id="a68dc-102">ICorProfilerAssemblyReferenceProvider::AddAssemblyReference Method</span></span>
<span data-ttu-id="a68dc-103">[Compatible con .NET Framework 4.5.2 y versiones posteriores]</span><span class="sxs-lookup"><span data-stu-id="a68dc-103">[Supported in the .NET Framework 4.5.2 and later versions]</span></span>  
  
 <span data-ttu-id="a68dc-104">Informa a common language runtime (CLR) de una referencia de ensamblado que el generador de perfiles planea agregar en el [ICorProfilerCallback:: ModuleLoadFinished](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-moduleloadfinished-method.md) devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="a68dc-104">Informs the common language runtime (CLR) of an assembly reference that the profiler plans to add in the [ICorProfilerCallback::ModuleLoadFinished](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-moduleloadfinished-method.md) callback.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a68dc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a68dc-105">Syntax</span></span>  
  
```cpp
HRESULT AddAssemblyReference(  
        const COR_PRF_ASSEMBLY_REFERENCE_INFO* pAssemblyRefInfo  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="a68dc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a68dc-106">Parameters</span></span>  
 <span data-ttu-id="a68dc-107">pAssemblyRefInfo</span><span class="sxs-lookup"><span data-stu-id="a68dc-107">pAssemblyRefInfo</span></span>  
 <span data-ttu-id="a68dc-108">Un puntero a un [COR_PRF_ASSEMBLY_REFERENCE_INFO](../../../../docs/framework/unmanaged-api/profiling/cor-prf-assembly-reference-info-structure.md) estructura que proporciona información sobre una referencia de ensamblado que debe tener en cuenta al realizar un rastreo de cierre de referencias de ensamblado CLR.</span><span class="sxs-lookup"><span data-stu-id="a68dc-108">A pointer to a [COR_PRF_ASSEMBLY_REFERENCE_INFO](../../../../docs/framework/unmanaged-api/profiling/cor-prf-assembly-reference-info-structure.md) structure that provides the CLR with information about an assembly reference that it should consider when performing an assembly reference closure walk.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="a68dc-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a68dc-109">Remarks</span></span>  
 <span data-ttu-id="a68dc-110">El generador de perfiles llama a este método para cada ensamblado de destino lo planeado hacer referencia desde el ensamblado especificado en el `wszAssemblyPath` argumento de la [icorprofilercallback6:: Getassemblyreferences](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback6-getassemblyreferences-method.md) devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="a68dc-110">The profiler calls this method for each target assembly it plans to reference from the assembly specified in the `wszAssemblyPath` argument of the [ICorProfilerCallback6::GetAssemblyReferences](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback6-getassemblyreferences-method.md) callback.</span></span> <span data-ttu-id="a68dc-111">El [ICorProfilerAssemblyReferenceProvider](../../../../docs/framework/unmanaged-api/profiling/icorprofilerassemblyreferenceprovider-interface.md) objeto de interfaz se pasa al generador de perfiles [icorprofilercallback6:: Getassemblyreferences](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback6-getassemblyreferences-method.md) devolución de llamada, junto con la ruta de acceso del ensamblado y el nombre en el `wszAssemblyPath` argumento.</span><span class="sxs-lookup"><span data-stu-id="a68dc-111">The [ICorProfilerAssemblyReferenceProvider](../../../../docs/framework/unmanaged-api/profiling/icorprofilerassemblyreferenceprovider-interface.md) interface object is passed to the profiler's [ICorProfilerCallback6::GetAssemblyReferences](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback6-getassemblyreferences-method.md) callback, along with the assembly path and name in the `wszAssemblyPath` argument.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a68dc-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a68dc-112">Requirements</span></span>  
 <span data-ttu-id="a68dc-113">**Plataformas:** vea [requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a68dc-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a68dc-114">**Encabezado:** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="a68dc-114">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="a68dc-115">**Biblioteca:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="a68dc-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="a68dc-116">**Versiones de .NET framework:**[!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a68dc-116">**.NET Framework Versions:** [!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a68dc-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="a68dc-117">See Also</span></span>  
 [<span data-ttu-id="a68dc-118">ICorProfilerAssemblyReferenceProvider (interfaz)</span><span class="sxs-lookup"><span data-stu-id="a68dc-118">ICorProfilerAssemblyReferenceProvider Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerassemblyreferenceprovider-interface.md)  
 [<span data-ttu-id="a68dc-119">GetAssemblyReferences (método)</span><span class="sxs-lookup"><span data-stu-id="a68dc-119">GetAssemblyReferences Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback6-getassemblyreferences-method.md)  
 [<span data-ttu-id="a68dc-120">ModuleLoadFinished (método)</span><span class="sxs-lookup"><span data-stu-id="a68dc-120">ModuleLoadFinished Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-moduleloadfinished-method.md)