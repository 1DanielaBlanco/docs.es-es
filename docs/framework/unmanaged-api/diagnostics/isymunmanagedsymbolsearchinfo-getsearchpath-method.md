---
title: "ISymUnmanagedSymbolSearchInfo::GetSearchPath (Método)"
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
- ISymUnmanagedSymbolSearchInfo.GetSearchPath
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedSymbolSearchInfo::GetSearchPath
helpviewer_keywords:
- GetSearchPath method [.NET Framework debugging]
- ISymUnmanagedSymbolSearchInfo::GetSearchPath method [.NET Framework debugging]
ms.assetid: b588d470-53c2-4492-be8c-957323eaca0b
topic_type:
- apiref
caps.latest.revision: 
author: mairaw
ms.author: mairaw
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: d1c4e1873aa3441e0348751717443e8189a67e61
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/22/2017
---
# <a name="isymunmanagedsymbolsearchinfogetsearchpath-method"></a><span data-ttu-id="0a10c-102">ISymUnmanagedSymbolSearchInfo::GetSearchPath (Método)</span><span class="sxs-lookup"><span data-stu-id="0a10c-102">ISymUnmanagedSymbolSearchInfo::GetSearchPath Method</span></span>
<span data-ttu-id="0a10c-103">Obtiene la ruta de acceso de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="0a10c-103">Gets the search path.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0a10c-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0a10c-104">Syntax</span></span>  
  
```  
HRESULT GetSearchPathLength(  
    [out] ULONG32 *pcchPath);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="0a10c-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0a10c-105">Parameters</span></span>  
 `pcchPath`  
 <span data-ttu-id="0a10c-106">[out] Un puntero a un `ULONG32` que recibe el tamaño, en caracteres, del búfer necesario para contener la ruta de acceso de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="0a10c-106">[out] A pointer to a `ULONG32` that receives the size, in characters, of the buffer required to contain the search path.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="0a10c-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0a10c-107">Return Value</span></span>  
 <span data-ttu-id="0a10c-108">S_OK si el método tiene éxito; en caso contrario, E_FAIL u otro código de error.</span><span class="sxs-lookup"><span data-stu-id="0a10c-108">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0a10c-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a10c-109">Requirements</span></span>  
 <span data-ttu-id="0a10c-110">**Encabezado:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="0a10c-110">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0a10c-111">Vea también</span><span class="sxs-lookup"><span data-stu-id="0a10c-111">See Also</span></span>  
 [<span data-ttu-id="0a10c-112">ISymUnmanagedSymbolSearchInfo (interfaz)</span><span class="sxs-lookup"><span data-stu-id="0a10c-112">ISymUnmanagedSymbolSearchInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedsymbolsearchinfo-interface.md)
