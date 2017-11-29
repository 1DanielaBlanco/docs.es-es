---
title: AXL_AUTHENTICODE_SIGNER_INFO (Estructura)
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
ms.assetid: 81c0f8b4-ce35-4716-8651-b642d40648a2
caps.latest.revision: "3"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: c53ca8073adda5cba497e9f45404024435cc161f
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/18/2017
---
# <a name="axlauthenticodesignerinfo-structure"></a>AXL_AUTHENTICODE_SIGNER_INFO (Estructura)
Define la información del firmante de Authenticode.  
  
## <a name="syntax"></a>Sintaxis  
  
```  
typedef struct _AXL_AUTHENTICODE_SIGNER_INFO {  
    DWORD cbSize;  
    HRESULT dwError;  
    ALG_ID algHash;  
    LPCWSTR pwszHash  
    LPCWSTR pwszDescription;  
    LPCWSTR pwszDescriptionUrl;  
    PCCERT_CHAIN_CONTEXT pChainContext  
} AXL_AUTHENTICODE_SIGNER_INFO, * PAXL_AUTHENTICODE_SIGNER_INFO;  
```  
  
## <a name="members"></a>Miembros  
  
|Miembro|Descripción|  
|------------|-----------------|  
|`cbSize`|Tamaño de esta estructura.|  
|`dwError`|Código de error.|  
|`algHash`|Algoritmo hash.|  
|`pwszHash`|Hash.|  
|`pwszDescription`|Description.|  
|`pwszDescriptionUrl`|Dirección URL de la descripción.|  
|`pChainContext`|Contexto de cadena del firmante. Consulte la [CERT_CONTEXT](http://msdn.microsoft.com/library/windows/desktop/aa377189.aspx) estructura.|  
  
## <a name="see-also"></a>Vea también  
 [Authenticode](../../../../docs/framework/unmanaged-api/authenticode/index.md)
