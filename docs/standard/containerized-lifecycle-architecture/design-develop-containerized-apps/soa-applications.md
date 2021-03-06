---
title: Aplicaciones SOA
description: Tenga en cuenta que los contenedores también pueden ser una opción de implementación útil para las aplicaciones SOA.
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 02/15/2019
ms.openlocfilehash: 353ba738143b7dcd92c7c75ac27ea6a7370f9da6
ms.sourcegitcommit: 8f95d3a37e591963ebbb9af6e90686fd5f3b8707
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/23/2019
ms.locfileid: "56745838"
---
# <a name="service-oriented-applications"></a>Aplicaciones orientadas a servicios

Arquitectura orientada a servicios (SOA) era un término sobreutilizado que significaba muchas cosas diferentes para diferentes personas. Pero como denominador común, SOA significa que se estructura la arquitectura de la aplicación descomponiéndola en varios servicios (normalmente como servicios HTTP) que se pueden clasificar en tipos diferentes, como subsistemas o, en otros casos, como los niveles.

Hoy en día, puede implementar estos servicios como contenedores de Docker, lo que resolución problemas relacionados con la implementación, porque todas las dependencias se incluyen en la imagen de contenedor. Sin embargo, cuando necesite escalar horizontalmente SOA, pueden surgir desafíos si está implementando en función de instancias únicas. Este desafío puede controlarse mediante software de clústeres o un orquestador de Docker. Examinaremos los orquestadores con más detalle en la sección siguiente, cuando se exploración los enfoques de microservicios.

Los contenedores de Docker son útiles (pero no obligatorios) para las arquitecturas orientadas a servicios tradicionales y las arquitecturas de microservicios más avanzadas.

Al final del día, las soluciones de agrupación en clústeres de contenedor son útiles para ambas una arquitectura tradicional de SOA y para una arquitectura de microservicios más avanzada en la que cada microservicio posee su modelo de datos. Y gracias a varias bases de datos, también puede escalar horizontalmente el nivel de datos en lugar de trabajar con bases de datos monolíticas compartidas por los servicios SOA. Sin embargo, la discusión sobre cómo dividir los datos es puramente sobre arquitectura y diseño.

>[!div class="step-by-step"]
>[Anterior](state-and-data-in-docker-applications.md)
>[Siguiente](orchestrate-high-scalability-availability.md)
