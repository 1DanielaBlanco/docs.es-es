---
title: GetHashFromHandle (Función)
ms.date: 03/30/2017
api_name:
- GetHashFromHandle
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- GetHashFromHandle
helpviewer_keywords:
- GetHashFromHandle function [.NET Framework strong naming]
ms.assetid: 9e00337f-b307-4602-9bc3-965a8dbf02cd
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: defa18bde8e5ce0f1cc7ff040aaa4fa0e95fd7e1
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/23/2019
ms.locfileid: "54619231"
---
# <a name="gethashfromhandle-function"></a>GetHashFromHandle (Función)
Genera un hash a partir del contenido del archivo con el identificador de archivos especificado mediante un algoritmo hash concreto.  
  
 Esta función está desusada. Use la [ICLRStrongName](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-gethashfromhandle-method.md) método en su lugar.  
  
## <a name="syntax"></a>Sintaxis  
  
```  
HRESULT GetHashFromHandle (  
    [in]  HANDLE   hFile,  
    [in, out] unsigned int   *piHashAlg,  
    [out] BYTE     *pbHash,  
    [in]  DWORD    cchHash,  
    [out] DWORD    *pchHash  
);  
```  
  
#### <a name="parameters"></a>Parámetros  
 `hFile`  
 [in] El identificador del archivo que se aplica un algoritmo hash.  
  
 `piHashAlg`  
 [in, out] Una constante que especifica el algoritmo hash. Usar cero para el algoritmo predeterminado.  
  
 `pbHash`  
 [out] El búfer hash devuelto.  
  
 `cchHash`  
 [in] El tamaño máximo solicitado de `pbHash`.  
  
 `pchHash`  
 [out] El tamaño, en bytes, del devuelto `pbHash`.  
  
## <a name="requirements"></a>Requisitos  
 **Plataformas:** Consulte [Requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Encabezado**: StrongName.h  
  
 **Biblioteca:** Incluye como recurso en MsCorEE.dll  
  
 **Versiones de .NET Framework:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Vea también
- [GetHashFromHandle (método)](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-gethashfromhandle-method.md)
- [ICLRStrongName (interfaz)](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)
