---
title: Instancias por segundo
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 74579397-1058-4278-80cf-2d00854a480f
caps.latest.revision: "7"
author: Erikre
ms.author: erikre
manager: erikre
ms.openlocfilehash: 18423684e6f816ae2d2e2829664b1be71939335d
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/18/2017
---
# <a name="instances-per-second"></a><span data-ttu-id="17ec3-102">Instancias por segundo</span><span class="sxs-lookup"><span data-stu-id="17ec3-102">Instances Per Second</span></span>
<span data-ttu-id="17ec3-103">Nombre de contador: Instancias creadas por segundo.</span><span class="sxs-lookup"><span data-stu-id="17ec3-103">Counter Name: Instances Created Per Second.</span></span>  
  
## <a name="description"></a><span data-ttu-id="17ec3-104">Descripción</span><span class="sxs-lookup"><span data-stu-id="17ec3-104">Description</span></span>  
 <span data-ttu-id="17ec3-105">Número de instancias del servicio creadas en un segundo.</span><span class="sxs-lookup"><span data-stu-id="17ec3-105">Total number of service instances created in a second.</span></span>  
  
 <span data-ttu-id="17ec3-106">Este contador es de tipo de contador de rendimiento [PERF_COUNTER_COUNTER](http://go.microsoft.com/fwlink/?LinkID=94649), cuyo valor se calcula con la siguiente fórmula.</span><span class="sxs-lookup"><span data-stu-id="17ec3-106">This counter is of performance counter type [PERF_COUNTER_COUNTER](http://go.microsoft.com/fwlink/?LinkID=94649), whose value is calculated using the following formula.</span></span>  
  
 <span data-ttu-id="17ec3-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span><span class="sxs-lookup"><span data-stu-id="17ec3-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span></span>
