---
title: "SetAssemblyFile2 (Método)"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IALink2.SetAssemblyFile2
api_location: alink.dll
api_type: COM
f1_keywords: SetAssemblyFile2
helpviewer_keywords: SetAssemblyFile2 method
ms.assetid: eedb9125-1ef1-4000-abfc-7de86e5a1f17
topic_type: apiref
caps.latest.revision: "9"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 7363a8f633d5f447f72e27ba03055f589564bdd2
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/21/2017
---
# <a name="setassemblyfile2-method"></a><span data-ttu-id="173d4-102">SetAssemblyFile2 (Método)</span><span class="sxs-lookup"><span data-stu-id="173d4-102">SetAssemblyFile2 Method</span></span>
<span data-ttu-id="173d4-103">Establece el nombre y las opciones para un nuevo ensamblado.</span><span class="sxs-lookup"><span data-stu-id="173d4-103">Sets the name of and options for a new assembly.</span></span> <span data-ttu-id="173d4-104">No llame a este método cuando se crean módulos no enlazados.</span><span class="sxs-lookup"><span data-stu-id="173d4-104">Do not call this method when you produce unbound modules.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="173d4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="173d4-105">Syntax</span></span>  
  
```  
HRESULT SetAssemblyFile2(  
    LPCWSTR pszFilename,  
    IMetaDataEmit2* pEmitter,  
    AssemblyFlags   afFlags,  
    mdAssembly* pAssemblyID  
) PURE;  
```  
  
#### <a name="parameters"></a><span data-ttu-id="173d4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="173d4-106">Parameters</span></span>  
 `pszFilename`  
 <span data-ttu-id="173d4-107">Nombre del archivo de manifiesto.</span><span class="sxs-lookup"><span data-stu-id="173d4-107">Name of manifest file.</span></span>  
  
 `pEmitter`  
 <span data-ttu-id="173d4-108">[IMetaDataEmit2 (interfaz)](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md) interfaz para este archivo.</span><span class="sxs-lookup"><span data-stu-id="173d4-108">[IMetaDataEmit2 Interface](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md) interface for this file.</span></span>  
  
 `afFlags`  
 <span data-ttu-id="173d4-109">Opciones representadas por [AssemblyFlags (enumeración)](../../../../docs/framework/unmanaged-api/metadata/assemblyflags-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="173d4-109">Options represented by [AssemblyFlags Enumeration](../../../../docs/framework/unmanaged-api/metadata/assemblyflags-enumeration.md).</span></span>  
  
 `pAssemblyID`  
 <span data-ttu-id="173d4-110">Recibe el identificador único para el ensamblado que se está construyendo.</span><span class="sxs-lookup"><span data-stu-id="173d4-110">Receives unique ID for the assembly being constructed.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="173d4-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="173d4-111">Return Value</span></span>  
 <span data-ttu-id="173d4-112">Devuelve S_OK si el método tiene éxito.</span><span class="sxs-lookup"><span data-stu-id="173d4-112">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="173d4-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="173d4-113">Requirements</span></span>  
 <span data-ttu-id="173d4-114">Requiere alink.h.</span><span class="sxs-lookup"><span data-stu-id="173d4-114">Requires alink.h.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="173d4-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="173d4-115">See Also</span></span>  
 [<span data-ttu-id="173d4-116">IALink2 (interfaz)</span><span class="sxs-lookup"><span data-stu-id="173d4-116">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)  
 [<span data-ttu-id="173d4-117">IALink (interfaz)</span><span class="sxs-lookup"><span data-stu-id="173d4-117">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)  
 [<span data-ttu-id="173d4-118">API de ALink</span><span class="sxs-lookup"><span data-stu-id="173d4-118">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)