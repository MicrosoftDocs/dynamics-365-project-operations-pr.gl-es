---
title: Crear un modelo de proxecto
description: Como crear un modelo de proxecto en Project Service
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 148bf1d42b640ff7b58b13bb0c30c7e583d803c8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997239"
---
# <a name="create-a-project-template-project-service"></a>Crear un modelo de proxecto (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Os modelos de proxecto afórranlle tempo se a súa empresa realiaza ofertas con regularidade en tipos de proxectos similares. Fornecen un conxunto de roles estándar e horas de traballo estimadas para un tipo de proxecto. Os xestores de contas e os xestores de proxectos poden crear proxectos baseados nun modelo de proxecto, ou poden copiar o modelo e facer un propio.  
  
## <a name="components-of-project-template"></a>Compoñentes do modelo de proxecto
 Un modelo de proxecto consta de tres compoñentes:  
  
- **Estrutura de subdivisión do traballo**: unha estrutura de subdivisión do traballo nun modelo de proxecto ten o mesmo conxunto de elementos que os do proxecto. Pode crear unha xerarquía de tarefas, asociar roles a tarefas, definir atributos de programación, definir dependencias e ver todos os datos no Gantt. A estrutura de subdivisión do traballo en modelos de proxecto tamén é compatible cos modos de tarefa para cada tarefa. Non hai ningunha diferenza entre un modelo de proxecto e un proxecto ao crear a programación de traballo.  
  
- **Estimacións de proxecto**: as estimacións de proxecto en modelos funcionan da mesma maneira que nos proxectos, excepto que as listas de prezos listas para definir o valor predefinido dos prezos de ventas e custo son sempre as listas de prezos e custo definidas nos parámetros de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. O resto das funcionalidades é o mesmo que nun proxecto.  
  
- **Formación do equipo de proxecto**: ao formar un equipo de proxecto para un modelo de proxecto, non se pode reservar un recurso nomeado nun modelo. Pode utilizar **Xerar equipo de proxecto** na estrutura de subdivisión do traballo para xerar un conxunto de recursos xenéricos. Tamén pode especificar os coñecementos e habilidades necesarios para os recursos xenéricos. Non se pode cambiar un recurso xenérico cun recurso reservable en modelos de proxecto.  
  
## <a name="create-a-project-from-a-template"></a>Crear un proxecto a partir dun modelo  
 Pode crear un proxecto a partir dun modelo destas maneiras:  
  
-   Ao crear un proxecto desde a oferta, pode escoller un modelo de proxecto no formulario de creación rápida de proxectos.  
  
-   Ao crear un proxecto premendo **Novo Proxecto**, o formulario de proxectos móstrase antes de gardar o rexistro. Desde aquí, pode premer o campo **Escoller un modelo** para escoller un valor da lista de modelos de proxecto predefinidos da súa organización.  
  
-   Prema **Crear proxecto a partir dun modelo** na páxina **Modelo de proxecto** para crear un proxecto a partir do modelo.  
  
## <a name="copying-components-of-a-template-to-a-project"></a>Copiar compoñentes dun modelo a un proxecto  
 Se copia compoñentes dun modelo a un proxecto, debe saber algunhas cousas.  
  
 **Copiar unha estrutura de subdivisión do traballo**: ao copiar a estrutura de subdivisión do traballo a partir dun modelo de proxecto, se o proxecto ten un calendario de proxecto diferente ao do modelo, as horas de traballo do calendario do proxecto aplicaranse á programación de tarefas. Isto axusta a programación no calendario de respaldo do proxecto. De forma similar, a primeira tarefa na estrutura de subdivisión do traballo colle a data de inicio do proxecto, de xeito que o resto da programación da xerarquía de tarefas actualízase segundo a duración e as dependencias especificadas na estrutura de subdivisión do traballo no modelo.  
  
 **Copiar estimacións do proxecto**: cando copia en liñas de estimación do proxecto, as listas de prezos actualízanse segundo a unidade propietaria do proxecto para a lista de prezos de custo e cliente para a lista de prezos de vendas. O custo unitario e os prezos de vendas determínanse desde estas listas de prezo en proxectos que están asociados a unha entidade de vendas.  
  
 **Copiar un equipo de proxecto**: ao copiar o equipo de proxecto a partir do modelo para un proxecto, os recursos xenéricos está tamén se copian, xunto cos coñecementos e habilidades definidos no modelo. As atribucións de recursos xenéricas tamén se manteñen iguais no modelo de proxecto.  
  
### <a name="see-also"></a>Consulte tamén  
 [Guía do xestor de proxectos](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]