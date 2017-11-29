---
title: "ICoreClrDebugTarget::EnumProcesses (Método)"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICoreClrDebugTarget.EnumProcesses
api_location: mscordbi_macx86.dll
api_type: COM
f1_keywords: ICoreClrDebugTarget::EnumProcesses
helpviewer_keywords:
- remote debugging API [Silverlight]
- EnumProcesses method, ICorClrDebugTarget interface [Silverlight debugging]
- ICorClrDebugTarget::EnumProcesses method [Silverlight debugging]
- Silverlight, remote debugging
ms.assetid: e00fd477-4f49-43d3-bd0e-3094824b1136
topic_type: apiref
caps.latest.revision: "4"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: abdbf506505e9a49103a93ca2dc92bd805cfd509
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/18/2017
---
# <a name="icoreclrdebugtargetenumprocesses-method"></a><span data-ttu-id="2bbd5-102">ICoreClrDebugTarget::EnumProcesses (Método)</span><span class="sxs-lookup"><span data-stu-id="2bbd5-102">ICoreClrDebugTarget::EnumProcesses Method</span></span>
<span data-ttu-id="2bbd5-103">Enumera los procesos que se ejecutan en un equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="2bbd5-103">Enumerates the processes that are running on a remote computer.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2bbd5-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2bbd5-104">Syntax</span></span>  
  
```  
HRESULT EnumProcesses (  
       [out]  DWORD*                  pcProcs,   
       [out]  CoreClrDebugProcInfo**  ppProcs  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="2bbd5-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2bbd5-105">Parameters</span></span>  
 `pcProcs`  
 <span data-ttu-id="2bbd5-106">[out] Número de procesos que se devuelve en `ppProcs`.</span><span class="sxs-lookup"><span data-stu-id="2bbd5-106">[out] The number of processes returned in `ppProcs`.</span></span> <span data-ttu-id="2bbd5-107">Este valor puede ser 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="2bbd5-107">This value can be 0 (zero).</span></span>  
  
 `ppProcs`  
 <span data-ttu-id="2bbd5-108">[out] Una matriz de [CoreClrDebugProcInfo](../../../../docs/framework/unmanaged-api/debugging/coreclrdebugprocinfo-structure.md) estructuras que representan los procesos que se ejecutan en el equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="2bbd5-108">[out] An array of [CoreClrDebugProcInfo](../../../../docs/framework/unmanaged-api/debugging/coreclrdebugprocinfo-structure.md) structures that represent the processes running on the remote computer.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="2bbd5-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2bbd5-109">Return Value</span></span>  
 <span data-ttu-id="2bbd5-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="2bbd5-110">S_OK</span></span>  
 <span data-ttu-id="2bbd5-111">Correcto.</span><span class="sxs-lookup"><span data-stu-id="2bbd5-111">Success.</span></span>  
  
 <span data-ttu-id="2bbd5-112">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="2bbd5-112">E_OUTOFMEMORY</span></span>  
 <span data-ttu-id="2bbd5-113">No se puede asignar memoria suficiente para `ppProcs`.</span><span class="sxs-lookup"><span data-stu-id="2bbd5-113">Unable to allocate enough memory for `ppProcs`.</span></span>  
  
 <span data-ttu-id="2bbd5-114">E_FAIL (u otros códigos devueltos de E_)</span><span class="sxs-lookup"><span data-stu-id="2bbd5-114">E_FAIL (or other E_ return codes)</span></span>  
 <span data-ttu-id="2bbd5-115">Otros errores.</span><span class="sxs-lookup"><span data-stu-id="2bbd5-115">Other failures.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="2bbd5-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2bbd5-116">Remarks</span></span>  
 <span data-ttu-id="2bbd5-117">Para liberar la memoria asignada por este método, llame a la [Icoreclrdebugtarget](../../../../docs/framework/unmanaged-api/debugging/icoreclrdebugtarget-freememory-method.md) método.</span><span class="sxs-lookup"><span data-stu-id="2bbd5-117">To free the memory that was allocated by this method, call the [ICoreClrDebugTarget::FreeMemory](../../../../docs/framework/unmanaged-api/debugging/icoreclrdebugtarget-freememory-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2bbd5-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2bbd5-118">Requirements</span></span>  
 <span data-ttu-id="2bbd5-119">**Plataformas:** vea [requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="2bbd5-119">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2bbd5-120">**Encabezado:** CoreClrRemoteDebuggingInterfaces.h</span><span class="sxs-lookup"><span data-stu-id="2bbd5-120">**Header:** CoreClrRemoteDebuggingInterfaces.h</span></span>  
  
 <span data-ttu-id="2bbd5-121">**Biblioteca:** mscordbi_macx86.dll</span><span class="sxs-lookup"><span data-stu-id="2bbd5-121">**Library:** mscordbi_macx86.dll</span></span>  
  
 <span data-ttu-id="2bbd5-122">**Versiones de .NET framework:** 3.5 SP1</span><span class="sxs-lookup"><span data-stu-id="2bbd5-122">**.NET Framework Versions:** 3.5 SP1</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2bbd5-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="2bbd5-123">See Also</span></span>  
 [<span data-ttu-id="2bbd5-124">ICoreClrDebugTarget (interfaz)</span><span class="sxs-lookup"><span data-stu-id="2bbd5-124">ICoreClrDebugTarget Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icoreclrdebugtarget-interface.md)