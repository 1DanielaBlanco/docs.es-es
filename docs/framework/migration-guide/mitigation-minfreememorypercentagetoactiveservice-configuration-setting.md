---
title: "Mitigación: Valor de configuración minFreeMemoryPercentageToActiveService | Microsoft Docs"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology:
- dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: a7875f26-0da8-4afe-9846-7a21778f757b
caps.latest.revision: 4
author: rpetrusha
ms.author: ronpet
manager: wpickett
translationtype: Human Translation
ms.sourcegitcommit: 9f5b8ebb69c9206ff90b05e748c64d29d82f7a16
ms.openlocfilehash: 783dd4fb28f1590722833ce9a456b9c2c76ecd80
ms.lasthandoff: 04/18/2017

---
# <a name="mitigation-minfreememorypercentagetoactiveservice-configuration-setting"></a>Mitigación: Valor de configuración minFreeMemoryPercentageToActiveService
En [!INCLUDE[net_v451](../../../includes/net-v451-md.md)], se produce una excepción si la memoria disponible en el servidor web es menor que el porcentaje especificado por la opción de configuración [minFreeMemoryPercentageToActivateService](../../../docs/framework/configure-apps/file-schema/wcf/servicehostingenvironment.md). En [!INCLUDE[net_v45](../../../includes/net-v45-md.md)], este valor se omite.  
  
## <a name="impact"></a>Impacto  
 En la mayoría de los casos, el impacto de aplicar la opción [minFreeMemoryPercentageToActivateService](../../../docs/framework/configure-apps/file-schema/wcf/servicehostingenvironment.md) s deseable: mejora la estabilidad del sistema evitando las excepciones <xref:System.OutOfMemoryException> que pueden aparecer cuando se inicia un servicio de Windows Communication Foundation (WCF) en un sistema que tiene memoria restringida.  
  
 Sin embargo, en algunos casos, es posible que un servicio iniciado correctamente con anterioridad no se pueda iniciar. En ese caso, aparece un mensaje de error detallado:  
  
```Output  
Memory gates checking failed because the free memory (nnnn bytes) is less than nn% of total memory. As a result, the service will not be available for incoming requests. To resolve this, either reduce the load on the machine or adjust the value of minFreeMemoryPercentageToActivateService on the serviceHostingEnvironment config element.  
```  
  
## <a name="mitigation"></a>Mitigación  
 Para revertir al comportamiento anterior, donde se omitía la configuración [minFreeMemoryPercentageToActivateService](../../../docs/framework/configure-apps/file-schema/wcf/servicehostingenvironment.md), modifique el archivo web.config de la manera siguiente:  
  
```  
  
<serviceHostingEnvironment multipleSiteBindingsEnabled="true"   
                           minFreeMemoryPercentageToActivateService="0">  
   <serviceActivations>  
   ...  
   </serviceActivations>  
</serviceHostingEnvironment>  
  
```  
  
## <a name="see-also"></a>Vea también  
 [Cambios en el runtime](../../../docs/framework/migration-guide/runtime-changes-in-the-net-framework-4-5-1.md)
