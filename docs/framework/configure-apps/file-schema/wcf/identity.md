---
title: '&lt;identity&gt;'
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: c1d2ae56-e231-4a07-9c3f-9f13381dc0d8
caps.latest.revision: "18"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: e583acee6309b6f8145cf8567cff12cea1c237e7
ms.sourcegitcommit: c0dd436f6f8f44dc80dc43b07f6841a00b74b23f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/19/2018
---
# <a name="ltidentitygt"></a><span data-ttu-id="44336-102">&lt;identity&gt;</span><span class="sxs-lookup"><span data-stu-id="44336-102">&lt;identity&gt;</span></span>
<span data-ttu-id="44336-103">El elemento de identidad permite a un programador del cliente especificar en tiempo de diseño la identidad esperada del servicio.</span><span class="sxs-lookup"><span data-stu-id="44336-103">The identity element allows a client developer to specify at design time the expected identity of the service.</span></span> <span data-ttu-id="44336-104">En el proceso de protocolo de enlace entre el cliente y el servicio, la infraestructura de [!INCLUDE[indigo1](../../../../../includes/indigo1-md.md)] se asegurará de que la identidad del servicio esperado coincida con los valores de este elemento y, por tanto, pueda autenticarse.</span><span class="sxs-lookup"><span data-stu-id="44336-104">In the handshake process between the client and service, the [!INCLUDE[indigo1](../../../../../includes/indigo1-md.md)] infrastructure will ensure that the identity of the expected service matches the values of this element, and thus can be authenticated.</span></span> <span data-ttu-id="44336-105">Para obtener más información, consulte [autenticación e identidad de servicio](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md).</span><span class="sxs-lookup"><span data-stu-id="44336-105">For more information, see [Service Identity and Authentication](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md).</span></span>  
  
 <span data-ttu-id="44336-106">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="44336-106">\<system.ServiceModel></span></span>  
<span data-ttu-id="44336-107">\<client></span><span class="sxs-lookup"><span data-stu-id="44336-107">\<client></span></span>  
<span data-ttu-id="44336-108">\<punto de conexión ></span><span class="sxs-lookup"><span data-stu-id="44336-108">\<endpoint></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="44336-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="44336-109">Syntax</span></span>  
  
```xml  
<identity>  
    <certificate encodedValue="String"/>  
    <certificateReference findValue="String"   
       isChainIncluded="Boolean"  
       storeName="AddressBook/AuthRoot/CertificateAuthority/Disallowed/My/Root/TrustedPeople/TrustedPublisher"storeName="  
       storeLocation="LocalMachine/CurrentUser"  
       X509FindType= Enumeration./>  
    <dns value="String"/>  
    <rsa value="String"/>  
    <servicePrincipalName value="String"/>  
    <usePrincipalName value="String"/>  
</identity>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="44336-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="44336-110">Attributes and Elements</span></span>  
 <span data-ttu-id="44336-111">En las siguientes secciones se describen los atributos, los elementos secundarios y los elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="44336-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="44336-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="44336-112">Attributes</span></span>  
 <span data-ttu-id="44336-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="44336-113">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="44336-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="44336-114">Child Elements</span></span>  
  
|<span data-ttu-id="44336-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="44336-115">Element</span></span>|<span data-ttu-id="44336-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="44336-116">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="44336-117">certificate</span><span class="sxs-lookup"><span data-stu-id="44336-117">certificate</span></span>|<span data-ttu-id="44336-118">Especifica los valores de un certificado X.509.</span><span class="sxs-lookup"><span data-stu-id="44336-118">Specifies settings of an X.509 certificate.</span></span> <span data-ttu-id="44336-119">Este elemento es del tipo <xref:System.ServiceModel.Configuration.CertificateElement>.</span><span class="sxs-lookup"><span data-stu-id="44336-119">This element is of type <xref:System.ServiceModel.Configuration.CertificateElement>.</span></span> <span data-ttu-id="44336-120">Contiene un atributo `encodedValue` que es una cadena, que especifica el valor codificado por este certificado.</span><span class="sxs-lookup"><span data-stu-id="44336-120">It contains an attribute `encodedValue` that is a string, which specifies the value encoded by this certificate.</span></span>|  
|<span data-ttu-id="44336-121">certificateReference</span><span class="sxs-lookup"><span data-stu-id="44336-121">certificateReference</span></span>|<span data-ttu-id="44336-122">Especifica los valores para la validación del certificado X.509.</span><span class="sxs-lookup"><span data-stu-id="44336-122">Specifies settings for X.509 certificate validation.</span></span> <span data-ttu-id="44336-123">Este elemento es del tipo <xref:System.ServiceModel.Configuration.CertificateReferenceElement>.</span><span class="sxs-lookup"><span data-stu-id="44336-123">This element is of type <xref:System.ServiceModel.Configuration.CertificateReferenceElement>.</span></span>|  
|<span data-ttu-id="44336-124">dns</span><span class="sxs-lookup"><span data-stu-id="44336-124">dns</span></span>|<span data-ttu-id="44336-125">Especifica el DNS de un certificado X.509 usado para autenticar un servicio.</span><span class="sxs-lookup"><span data-stu-id="44336-125">Specifies the DNS of an X.509 certificate used to authenticate a service.</span></span> <span data-ttu-id="44336-126">Este elemento contiene un atributo `value` que es una cadena y contiene la identidad real.</span><span class="sxs-lookup"><span data-stu-id="44336-126">This element contains an attribute `value` that is a string, and contains the actual identity.</span></span>|  
|<span data-ttu-id="44336-127">rsa</span><span class="sxs-lookup"><span data-stu-id="44336-127">rsa</span></span>|<span data-ttu-id="44336-128">Especifica el valor del campo RSA de un certificado X.509 usado para autenticar un servicio a un cliente.</span><span class="sxs-lookup"><span data-stu-id="44336-128">Specifies the value of the RSA field of an X.509 certificate used to authenticate a service to a client.</span></span> <span data-ttu-id="44336-129">Este elemento contiene un atributo `value` que es una cadena y contiene la identidad real.</span><span class="sxs-lookup"><span data-stu-id="44336-129">This element contains an attribute `value` that is a string, and contains the actual identity</span></span>|  
|<span data-ttu-id="44336-130">servicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="44336-130">servicePrincipalName</span></span>|<span data-ttu-id="44336-131">Especifica una identidad del nombre de entidad de seguridad de servidor (SPN) que es el nombre de entidad de seguridad usado por un cliente para identificar de manera unívoca una instancia de un servicio.</span><span class="sxs-lookup"><span data-stu-id="44336-131">Specifies a server principal name (SPN) identity, which is the principal name used by a client to uniquely identify an instance of a service.</span></span> <span data-ttu-id="44336-132">Este elemento contiene un atributo `value` que es una cadena y contiene el nombre de entidad de seguridad real.</span><span class="sxs-lookup"><span data-stu-id="44336-132">This element contains an attribute `value` that is a string, and contains the actual principal name.</span></span> <span data-ttu-id="44336-133">Este elemento es del tipo <xref:System.ServiceModel.Configuration.ServicePrincipalNameElement>.</span><span class="sxs-lookup"><span data-stu-id="44336-133">This element is of type <xref:System.ServiceModel.Configuration.ServicePrincipalNameElement>.</span></span>|  
|<span data-ttu-id="44336-134">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="44336-134">userPrincipalName</span></span>|<span data-ttu-id="44336-135">Especifica una identidad del nombre principal del usuario (UPN), que es el tipo de nombre de inicio de sesión de un usuario en una red.</span><span class="sxs-lookup"><span data-stu-id="44336-135">Specifies a user principal name (UPN) identity, which is the logon name type of a user on a network.</span></span> <span data-ttu-id="44336-136">El nombre principal del usuario se compone del nombre de objeto del usuario usado en Active Directory, seguido por el símbolo (@) y a continuación, normalmente, el dominio primario del Sistema de nombres de dominio (DNS).</span><span class="sxs-lookup"><span data-stu-id="44336-136">The user principal name consists of the user object name used in Active Directory, followed by the at symbol (@) and then, typically, the Domain Name System parent domain.</span></span> <span data-ttu-id="44336-137">Por ejemplo, Jeff en el árbol de dominios de Fabrikam.com podría tener el nombre principal de usuario [ jeff@fabrikam.com ](mailto:jeffsmith@fabrikam.com).  Este elemento contiene un atributo `value` que es una cadena y contiene el nombre de entidad de seguridad real.</span><span class="sxs-lookup"><span data-stu-id="44336-137">For example, Jeff in the Fabrikam.com domain tree might have the user principal name [jeff@fabrikam.com](mailto:jeffsmith@fabrikam.com).  This element contains an attribute `value` that is a string, and contains the actual principal name.</span></span> <span data-ttu-id="44336-138">Este elemento es del tipo <xref:System.ServiceModel.Configuration.UserPrincipalNameElement>.</span><span class="sxs-lookup"><span data-stu-id="44336-138">This element is of type <xref:System.ServiceModel.Configuration.UserPrincipalNameElement>.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="44336-139">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="44336-139">Parent Elements</span></span>  
  
|<span data-ttu-id="44336-140">Elemento</span><span class="sxs-lookup"><span data-stu-id="44336-140">Element</span></span>|<span data-ttu-id="44336-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="44336-141">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="44336-142">\<custom></span><span class="sxs-lookup"><span data-stu-id="44336-142">\<custom></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/custom.md)|<span data-ttu-id="44336-143">Especifica la resolución del mismo nivel personalizado de un netPeerTcpBinding.</span><span class="sxs-lookup"><span data-stu-id="44336-143">Specifies a custom peer resolver for a netPeerTcpBinding.</span></span>|  
|[<span data-ttu-id="44336-144">\<endpoint></span><span class="sxs-lookup"><span data-stu-id="44336-144">\<endpoint></span></span>](http://msdn.microsoft.com/library/13aa23b7-2f08-4add-8dbf-a99f8127c017)|<span data-ttu-id="44336-145">Configura tipos diferentes de puntos de conexión.</span><span class="sxs-lookup"><span data-stu-id="44336-145">Configures different types of endpoints.</span></span>|  
|[<span data-ttu-id="44336-146">\<issuer></span><span class="sxs-lookup"><span data-stu-id="44336-146">\<issuer></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/issuer.md)|<span data-ttu-id="44336-147">Especifica el servicio de token de seguridad (STS) para el servicio aliado.</span><span class="sxs-lookup"><span data-stu-id="44336-147">Specifies the Security Token Service (STS) for the federated service.</span></span>|  
|[<span data-ttu-id="44336-148">\<issuerMetadata></span><span class="sxs-lookup"><span data-stu-id="44336-148">\<issuerMetadata></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/issuermetadata.md)|<span data-ttu-id="44336-149">Especifica el punto de conexión de metadatos para el servicio de token de seguridad (STS) de un servicio aliado.</span><span class="sxs-lookup"><span data-stu-id="44336-149">Specifies the metadata endpoint for the Security Token Service (STS) of a federated service.</span></span>|  
|[<span data-ttu-id="44336-150">\<issuedTokenParameters></span><span class="sxs-lookup"><span data-stu-id="44336-150">\<issuedTokenParameters></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/issuedtokenparameters.md)|<span data-ttu-id="44336-151">Define los parámetros para un token emitido en un enlace personalizado.</span><span class="sxs-lookup"><span data-stu-id="44336-151">Defines parameters for an issued token in a custom binding.</span></span>|  
|[<span data-ttu-id="44336-152">\<localIssuer></span><span class="sxs-lookup"><span data-stu-id="44336-152">\<localIssuer></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/localissuer.md)|<span data-ttu-id="44336-153">Especifica un servicio de token de seguridad (STS) local.</span><span class="sxs-lookup"><span data-stu-id="44336-153">Specifies a local Security Token Service (STS).</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="44336-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="44336-154">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.IdentityElement>  
 <xref:System.ServiceModel.EndpointAddress>  
 <xref:System.ServiceModel.EndpointAddress.Identity%2A>  
 [<span data-ttu-id="44336-155">Identidad del servicio y autenticación</span><span class="sxs-lookup"><span data-stu-id="44336-155">Service Identity and Authentication</span></span>](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md)  
 [<span data-ttu-id="44336-156">Puntos de conexión: direcciones, enlaces y contratos</span><span class="sxs-lookup"><span data-stu-id="44336-156">Endpoints: Addresses, Bindings, and Contracts</span></span>](../../../../../docs/framework/wcf/feature-details/endpoints-addresses-bindings-and-contracts.md)
