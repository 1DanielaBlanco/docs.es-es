---
title: "WindowsRuntimeStreamExtensions.AsRandomAccessStream(System.IO.Stream) (Método)"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-standard
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- csharp
- vb
api_name: System.IO.WindowsRuntimeStreamExtensions.AsRandomAccessStream
api_location: System.Runtime.WindowsRuntime.dll
ms.assetid: dcc72283-caed-49ee-b45d-ccaf94e97129
caps.latest.revision: "12"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: be93ddc0f3bf0a5079f31bfa0ff5caa882342c37
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/21/2017
---
# <a name="windowsruntimestreamextensionsasrandomaccessstreamsystemiostream-method"></a><span data-ttu-id="9f0b6-102">WindowsRuntimeStreamExtensions.AsRandomAccessStream(System.IO.Stream) (Método)</span><span class="sxs-lookup"><span data-stu-id="9f0b6-102">WindowsRuntimeStreamExtensions.AsRandomAccessStream(System.IO.Stream) Method</span></span>
<span data-ttu-id="9f0b6-103">[Compatible con .NET Framework 4.5.1 y versiones posteriores]</span><span class="sxs-lookup"><span data-stu-id="9f0b6-103">[Supported in the .NET Framework 4.5.1 and later versions]</span></span>  
  
 <span data-ttu-id="9f0b6-104">Convierte la secuencia especificada en una secuencia de acceso aleatorio.</span><span class="sxs-lookup"><span data-stu-id="9f0b6-104">Converts the specified stream to a random access stream.</span></span>  
  
 <span data-ttu-id="9f0b6-105">**Namespace:**<xref:System.IO?displayProperty=nameWithType></span><span class="sxs-lookup"><span data-stu-id="9f0b6-105">**Namespace:** <xref:System.IO?displayProperty=nameWithType></span></span>  
 <span data-ttu-id="9f0b6-106">**Ensamblado:** System.Runtime.WindowsRuntime (de System.Runtime.WindowsRuntime.dll)</span><span class="sxs-lookup"><span data-stu-id="9f0b6-106">**Assembly:** System.Runtime.WindowsRuntime (in System.Runtime.WindowsRuntime.dll)</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9f0b6-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9f0b6-107">Syntax</span></span>  
  
```csharp  
[CLSCompliantAttribute(false)]  
public static  IRandomAccessStream AsRandomAccessStream(Stream stream)  
```  
  
```vb  
'Declaration  
<ExtensionAttribute> _  
<CLSCompliantAttribute(False)> _  
Public Shared Function AsRandomAccessStream ( _  
        stream As Stream) As IRandomAccessStream  
```  
  
#### <a name="parameters"></a><span data-ttu-id="9f0b6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9f0b6-108">Parameters</span></span>  
 `stream`  
  
 <span data-ttu-id="9f0b6-109">Tipo: <xref:System.IO.Stream?displayProperty=nameWithType></span><span class="sxs-lookup"><span data-stu-id="9f0b6-109">Type: <xref:System.IO.Stream?displayProperty=nameWithType></span></span>  
<span data-ttu-id="9f0b6-110">La secuencia que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="9f0b6-110">The stream to convert.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="9f0b6-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9f0b6-111">Return Value</span></span>  
 <span data-ttu-id="9f0b6-112">Tipo: [Windows.Storage.Streams.RandomAccessStream](http://msdn.microsoft.com/library/windows/apps/windows.storage.streams.randomaccessstream.aspx)</span><span class="sxs-lookup"><span data-stu-id="9f0b6-112">Type: [Windows.Storage.Streams.RandomAccessStream](http://msdn.microsoft.com/library/windows/apps/windows.storage.streams.randomaccessstream.aspx)</span></span>  
<span data-ttu-id="9f0b6-113">Un [!INCLUDE[wrt](../../../includes/wrt-md.md)] secuencia de acceso aleatorio, que representa la secuencia convertida.</span><span class="sxs-lookup"><span data-stu-id="9f0b6-113">A [!INCLUDE[wrt](../../../includes/wrt-md.md)] random access stream, which represents the converted stream.</span></span>  
  
## <a name="exceptions"></a><span data-ttu-id="9f0b6-114">Excepciones</span><span class="sxs-lookup"><span data-stu-id="9f0b6-114">Exceptions</span></span>  
  
|<span data-ttu-id="9f0b6-115">Excepción</span><span class="sxs-lookup"><span data-stu-id="9f0b6-115">Exception</span></span>|<span data-ttu-id="9f0b6-116">Condición</span><span class="sxs-lookup"><span data-stu-id="9f0b6-116">Condition</span></span>|  
|---------------|---------------|  
|<xref:System.NotSupportedException>|<span data-ttu-id="9f0b6-117">La secuencia que se va a convertir no admite operaciones de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="9f0b6-117">The stream to convert does not support seeking.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="9f0b6-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9f0b6-118">Remarks</span></span>  
 <span data-ttu-id="9f0b6-119">Este método de extensión solo está disponible al desarrollar aplicaciones de la Tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="9f0b6-119">This extension method is available only when you develop Windows Store apps.</span></span> <span data-ttu-id="9f0b6-120">Este método proporciona una forma cómoda de trabajar con secuencias en las aplicaciones de la Tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="9f0b6-120">This method provides a convenient way of working with streams in Windows Store apps.</span></span> <span data-ttu-id="9f0b6-121">La secuencia de .NET Framework que desea convertir debe admitir operaciones de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="9f0b6-121">The .NET Framework stream you want to convert must support seeking.</span></span> <span data-ttu-id="9f0b6-122">Para obtener más información, vea el método <xref:System.IO.Stream.Seek%2A?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="9f0b6-122">For more information, see the <xref:System.IO.Stream.Seek%2A?displayProperty=nameWithType> method.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="9f0b6-123">Esta API es compatible con .NET Framework 4.5.1 y versiones posteriores, pero no con la versión 4.5.</span><span class="sxs-lookup"><span data-stu-id="9f0b6-123">This API is supported in the .NET Framework 4.5.1 and later versions, but not in version 4.5.</span></span>  
  
## <a name="version-information"></a><span data-ttu-id="9f0b6-124">Información de versión</span><span class="sxs-lookup"><span data-stu-id="9f0b6-124">Version Information</span></span>  
 <span data-ttu-id="9f0b6-125">**.NET para aplicaciones de la tienda de Windows**</span><span class="sxs-lookup"><span data-stu-id="9f0b6-125">**.NET for Windows Store apps**</span></span>  
  
 <span data-ttu-id="9f0b6-126">Se admite en: Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="9f0b6-126">Supported in: Windows 8.1</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9f0b6-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="9f0b6-127">See Also</span></span>  
 <!--zz <xref:System.IO.WindowsRuntimeStreamExtensions>--> `System.IO.WindowsRuntimeStreamExtensions`  
 [<span data-ttu-id="9f0b6-128">Convertir flujos de .NET Framework en flujos de Windows Runtime y viceversa</span><span class="sxs-lookup"><span data-stu-id="9f0b6-128">How to: Convert Between .NET Framework Streams and Windows Runtime Streams</span></span>](../../../docs/standard/io/how-to-convert-between-dotnet-streams-and-winrt-streams.md)
