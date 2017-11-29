---
title: "IMetaDataImport::GetRVA (Método)"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IMetaDataImport.GetRVA
api_location: mscoree.dll
api_type: COM
f1_keywords: IMetaDataImport::GetRVA
helpviewer_keywords:
- GetRVA method [.NET Framework metadata]
- IMetaDataImport::GetRVA method [.NET Framework metadata]
ms.assetid: ea422217-988b-4acd-b2db-c55357938275
topic_type: apiref
caps.latest.revision: "12"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: f64cc5b0aa6043c5408868a5a6bf23e24278ea26
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/21/2017
---
# <a name="imetadataimportgetrva-method"></a><span data-ttu-id="aa306-102">IMetaDataImport::GetRVA (Método)</span><span class="sxs-lookup"><span data-stu-id="aa306-102">IMetaDataImport::GetRVA Method</span></span>
<span data-ttu-id="aa306-103">Obtiene la dirección virtual relativa (RVA) y los marcadores de implementación del método o campo representado por el token especificado.</span><span class="sxs-lookup"><span data-stu-id="aa306-103">Gets the relative virtual address (RVA) and the implementation flags of the method or field represented by the specified token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="aa306-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aa306-104">Syntax</span></span>  
  
```  
HRESULT GetRVA (  
   [in]  mdToken     tk,   
   [out] ULONG       *pulCodeRVA,   
   [out]  DWORD      *pdwImplFlags  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="aa306-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="aa306-105">Parameters</span></span>  
 `tk`  
 <span data-ttu-id="aa306-106">[in] Un token de metadatos MethodDef o FieldDef que representa el objeto de código para devolver la RVA.</span><span class="sxs-lookup"><span data-stu-id="aa306-106">[in] A MethodDef or FieldDef metadata token that represents the code object to return the RVA for.</span></span> <span data-ttu-id="aa306-107">Si el token es un FieldDef, el campo debe ser una variable global.</span><span class="sxs-lookup"><span data-stu-id="aa306-107">If the token is a FieldDef, the field must be a global variable.</span></span>  
  
 `pulCodeRVA`  
 <span data-ttu-id="aa306-108">[out] Un puntero a la dirección virtual relativa del objeto de código representado por el token.</span><span class="sxs-lookup"><span data-stu-id="aa306-108">[out] A pointer to the relative virtual address of the code object represented by the token.</span></span>  
  
 `pdwImplFlags`  
 <span data-ttu-id="aa306-109">[out] Un puntero a los marcadores de implementación para el método.</span><span class="sxs-lookup"><span data-stu-id="aa306-109">[out] A pointer to the implementation flags for the method.</span></span> <span data-ttu-id="aa306-110">Este valor es una máscara de bits de la [CorMethodImpl](../../../../docs/framework/unmanaged-api/metadata/cormethodimpl-enumeration.md) enumeración.</span><span class="sxs-lookup"><span data-stu-id="aa306-110">This value is a bitmask from the [CorMethodImpl](../../../../docs/framework/unmanaged-api/metadata/cormethodimpl-enumeration.md) enumeration.</span></span> <span data-ttu-id="aa306-111">El valor de `pdwImplFlags` es válido únicamente si `tk` es un token de MethodDef.</span><span class="sxs-lookup"><span data-stu-id="aa306-111">The value of `pdwImplFlags` is valid only if `tk` is a MethodDef token.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="aa306-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa306-112">Requirements</span></span>  
 <span data-ttu-id="aa306-113">**Plataformas:** vea [requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="aa306-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="aa306-114">**Encabezado:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="aa306-114">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="aa306-115">**Biblioteca:** incluye como recurso en MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="aa306-115">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="aa306-116">**Versiones de .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="aa306-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="aa306-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="aa306-117">See Also</span></span>  
 [<span data-ttu-id="aa306-118">IMetaDataImport (interfaz)</span><span class="sxs-lookup"><span data-stu-id="aa306-118">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)  
 [<span data-ttu-id="aa306-119">IMetaDataImport2 (interfaz)</span><span class="sxs-lookup"><span data-stu-id="aa306-119">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)