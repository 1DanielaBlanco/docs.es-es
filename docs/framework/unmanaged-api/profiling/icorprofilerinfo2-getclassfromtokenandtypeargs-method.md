---
title: "ICorProfilerInfo2::GetClassFromTokenAndTypeArgs (Método)"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorProfilerInfo2.GetClassFromTokenAndTypeArgs
api_location: mscorwks.dll
api_type: COM
f1_keywords: ICorProfilerInfo2::GetClassFromTokenAndTypeArgs
helpviewer_keywords:
- GetClassFromTokenAndTypeArgs method [.NET Framework profiling]
- ICorProfilerInfo2::GetClassFromTokenAndTypeArgs method [.NET Framework profiling]
ms.assetid: b25c88f0-71b9-443b-8eea-1c94db0a44b9
topic_type: apiref
caps.latest.revision: "11"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 332be5616ac11fc89df8c8d54aa5c0cbc49491ff
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/21/2017
---
# <a name="icorprofilerinfo2getclassfromtokenandtypeargs-method"></a><span data-ttu-id="2457d-102">ICorProfilerInfo2::GetClassFromTokenAndTypeArgs (Método)</span><span class="sxs-lookup"><span data-stu-id="2457d-102">ICorProfilerInfo2::GetClassFromTokenAndTypeArgs Method</span></span>
<span data-ttu-id="2457d-103">Obtiene el `ClassID` de un tipo mediante el token de metadatos especificado y la `ClassID` valores de cualquier tipo de argumentos.</span><span class="sxs-lookup"><span data-stu-id="2457d-103">Gets the `ClassID` of a type by using the specified metadata token and the `ClassID` values of any type arguments.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2457d-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2457d-104">Syntax</span></span>  
  
```  
HRESULT GetClassFromTokenAndTypeArgs(  
    [in] ModuleID moduleID,  
    [in] mdTypeDef typeDef,  
    [in] ULONG32 cTypeArgs,  
    [in, size_is(cTypeArgs)] ClassID typeArgs[],  
    [out] ClassID* pClassID);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="2457d-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2457d-105">Parameters</span></span>  
 `moduleID`  
 <span data-ttu-id="2457d-106">[in] El identificador del módulo en el que reside el tipo.</span><span class="sxs-lookup"><span data-stu-id="2457d-106">[in] The ID of the module in which the type resides.</span></span>  
  
 `typeDef`  
 <span data-ttu-id="2457d-107">[in] Un `mdTypeDef` símbolo (token) de metadatos que hace referencia al tipo.</span><span class="sxs-lookup"><span data-stu-id="2457d-107">[in] An `mdTypeDef` metadata token that references the type.</span></span>  
  
 `cTypeArgs`  
 <span data-ttu-id="2457d-108">[in] El número de parámetros de tipo para el tipo dado.</span><span class="sxs-lookup"><span data-stu-id="2457d-108">[in] The number of type parameters for the given type.</span></span> <span data-ttu-id="2457d-109">Este valor debe ser cero para tipos no genéricos.</span><span class="sxs-lookup"><span data-stu-id="2457d-109">This value must be zero for non-generic types.</span></span>  
  
 `typeArgs`  
 <span data-ttu-id="2457d-110">[in] Una matriz de `ClassID` valores, cada uno de los cuales es un argumento del tipo.</span><span class="sxs-lookup"><span data-stu-id="2457d-110">[in] An array of `ClassID` values, each of which is an argument of the type.</span></span> <span data-ttu-id="2457d-111">El valor de `typeArgs` puede ser NULL si `cTypeArgs` se establece en cero.</span><span class="sxs-lookup"><span data-stu-id="2457d-111">The value of `typeArgs` can be NULL if `cTypeArgs` is set to zero.</span></span>  
  
 `pClassID`  
 <span data-ttu-id="2457d-112">[out] Un puntero a la `ClassID` del tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="2457d-112">[out] A pointer to the `ClassID` of the specified type.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="2457d-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2457d-113">Remarks</span></span>  
 <span data-ttu-id="2457d-114">Llamar a la `GetClassFromTokenAndTypeArgs` método con un `mdTypeRef` en lugar de un `mdTypeDef` símbolo (token) de metadatos puede tener resultados imprevisibles; los llamadores deben resolver el `mdTypeRef` para un `mdTypeDef` al pasarla.</span><span class="sxs-lookup"><span data-stu-id="2457d-114">Calling the `GetClassFromTokenAndTypeArgs` method with an `mdTypeRef` instead of an `mdTypeDef` metadata token can have unpredictable results; callers should resolve the `mdTypeRef` to an `mdTypeDef` when passing it.</span></span>  
  
 <span data-ttu-id="2457d-115">Si ya no se carga el tipo, una llamada a `GetClassFromTokenAndTypeArgs` se desencadena la carga, que es una operación peligrosa en muchos contextos.</span><span class="sxs-lookup"><span data-stu-id="2457d-115">If the type is not already loaded, calling `GetClassFromTokenAndTypeArgs` will trigger loading, which is a dangerous operation in many contexts.</span></span> <span data-ttu-id="2457d-116">Por ejemplo, llamar a este método durante la carga de módulos u otros tipos podría provocar un bucle infinito como el tiempo de ejecución intenta la carga circular.</span><span class="sxs-lookup"><span data-stu-id="2457d-116">For example, calling this method during loading of modules or other types could lead to an infinite loop as the runtime attempts to circularly load things.</span></span>  
  
 <span data-ttu-id="2457d-117">En general, uso de `GetClassFromTokenAndTypeArgs` se desaconseja.</span><span class="sxs-lookup"><span data-stu-id="2457d-117">In general, use of `GetClassFromTokenAndTypeArgs` is discouraged.</span></span> <span data-ttu-id="2457d-118">Si los generadores de perfiles están interesados en los eventos de un tipo determinado, debe almacenar el `ModuleID` y `mdTypeDef` de ese tipo y el uso [ICorProfilerInfo2:: Getclassidinfo2](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-getclassidinfo2-method.md) para comprobar si un determinado `ClassID` es el de la tipo deseado.</span><span class="sxs-lookup"><span data-stu-id="2457d-118">If profilers are interested in events for a particular type, they should store the `ModuleID` and `mdTypeDef` of that type, and use [ICorProfilerInfo2::GetClassIDInfo2](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-getclassidinfo2-method.md) to check whether a given `ClassID` is that of the desired type.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2457d-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2457d-119">Requirements</span></span>  
 <span data-ttu-id="2457d-120">**Plataformas:** vea [requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="2457d-120">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2457d-121">**Encabezado:** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="2457d-121">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="2457d-122">**Biblioteca:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="2457d-122">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="2457d-123">**Versiones de .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2457d-123">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2457d-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="2457d-124">See Also</span></span>  
 [<span data-ttu-id="2457d-125">ICorProfilerInfo (interfaz)</span><span class="sxs-lookup"><span data-stu-id="2457d-125">ICorProfilerInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)  
 [<span data-ttu-id="2457d-126">ICorProfilerInfo2 (interfaz)</span><span class="sxs-lookup"><span data-stu-id="2457d-126">ICorProfilerInfo2 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-interface.md)