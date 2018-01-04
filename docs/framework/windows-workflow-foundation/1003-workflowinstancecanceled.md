---
title: 1003 - WorkflowInstanceCanceled
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 64754dc2-c160-4bf3-869a-13d56694e2dc
caps.latest.revision: "4"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: b264450703090edfcf99f9584c16d33eb82a76e3
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/22/2017
---
# <a name="1003---workflowinstancecanceled"></a><span data-ttu-id="42316-102">1003 - WorkflowInstanceCanceled</span><span class="sxs-lookup"><span data-stu-id="42316-102">1003 - WorkflowInstanceCanceled</span></span>
## <a name="properties"></a><span data-ttu-id="42316-103">Propiedades</span><span class="sxs-lookup"><span data-stu-id="42316-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="42316-104">Id.</span><span class="sxs-lookup"><span data-stu-id="42316-104">ID</span></span>|<span data-ttu-id="42316-105">1003</span><span class="sxs-lookup"><span data-stu-id="42316-105">1003</span></span>|  
|<span data-ttu-id="42316-106">Palabras clave</span><span class="sxs-lookup"><span data-stu-id="42316-106">Keywords</span></span>|<span data-ttu-id="42316-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="42316-107">WFRuntime</span></span>|  
|<span data-ttu-id="42316-108">Nivel</span><span class="sxs-lookup"><span data-stu-id="42316-108">Level</span></span>|<span data-ttu-id="42316-109">Información</span><span class="sxs-lookup"><span data-stu-id="42316-109">Information</span></span>|  
|<span data-ttu-id="42316-110">Canal</span><span class="sxs-lookup"><span data-stu-id="42316-110">Channel</span></span>|<span data-ttu-id="42316-111">Microsoft-Windows-Application Server-Applications/Debug</span><span class="sxs-lookup"><span data-stu-id="42316-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="42316-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="42316-112">Description</span></span>  
 <span data-ttu-id="42316-113">Indica que una instancia de flujo de trabajo ha finalizado en el estado Canceled.</span><span class="sxs-lookup"><span data-stu-id="42316-113">Indicates a workflow instance has completed in the Canceled state.</span></span>  
  
## <a name="message"></a><span data-ttu-id="42316-114">Mensaje</span><span class="sxs-lookup"><span data-stu-id="42316-114">Message</span></span>  
 <span data-ttu-id="42316-115">WorkflowInstance Id: '%1' se completó en el estado Canceled.</span><span class="sxs-lookup"><span data-stu-id="42316-115">WorkflowInstance Id: '%1' has completed in the Canceled state.</span></span>  
  
## <a name="details"></a><span data-ttu-id="42316-116">Detalles</span><span class="sxs-lookup"><span data-stu-id="42316-116">Details</span></span>  
  
|<span data-ttu-id="42316-117">Nombre del elemento de datos</span><span class="sxs-lookup"><span data-stu-id="42316-117">Data Item Name</span></span>|<span data-ttu-id="42316-118">Tipo del elemento de datos</span><span class="sxs-lookup"><span data-stu-id="42316-118">Data Item Type</span></span>|<span data-ttu-id="42316-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="42316-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="42316-120">WorkflowInstanceId</span><span class="sxs-lookup"><span data-stu-id="42316-120">WorkflowInstanceId</span></span>|`xs:string`|<span data-ttu-id="42316-121">El id. de instancia del flujo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="42316-121">The instance id for the workflow</span></span>|  
|<span data-ttu-id="42316-122">AppDomain</span><span class="sxs-lookup"><span data-stu-id="42316-122">AppDomain</span></span>|`xs:string`|<span data-ttu-id="42316-123">La cadena devuelta por AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="42316-123">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
