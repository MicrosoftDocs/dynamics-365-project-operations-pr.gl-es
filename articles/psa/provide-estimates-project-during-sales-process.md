---
title: Fornecer estimacións de traballo para un proxecto durante o proceso de vendas
description: Como fornecer estimacións de traballo para un proxecto durante o proceso de vendas en Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 7bd83b6872d437f1d074d6ea2336c751bdfdd9e6
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120586"
---
# <a name="provide-work-estimates-for-a-project-during-the-sales-process-project-service"></a>Fornecer estimacións de traballo para un proxecto durante o proceso de vendas (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Durante o proceso de vendas, pode calcular estimacións de vendas desde o principio con liñas de oferta. As capacidades de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] en [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] proporcionan unha forma máis científica e coherente de calcular estimacións de vendas desagregando elementos de traballo e asociando os atributos relevantes que contribúen ás estimacións para o proxecto na estrutura de subdivisión do traballo.  
  
 Unha vez gañada a venda, pode utilizar a estrutura de subdivisión do traballo asociada no seu plan de proxecto, precisándoa segundo sexa necesario para a conclusión correcta do seu proxecto.  
  
## <a name="link-a-project-to-a-quote-line"></a>Ligar un proxecto a unha liña de oferta  
 Ao crear unha liña de oferta baseada en proxecto, pode crear un novo proxecto desde a liña da oferta. Despois pode utilizar modelos de proxecto, que poden ser estimacións financeiras e plans de proxecto predefinido estándar configurados previamente comúns para a súa organización, ou unha copia dunha estimación ou un plan de proxecto dun proxecto anterior. Ao crear un proxecto, escoller un modelo de proxecto fornece a base para refinar os requirimentos do plan, a estimación e o rol do proxecto. Ao crear o proxecto desde unha oferta, o proxecto asóciase automaticamente á liña de oferta.  
  
## <a name="project-estimate-components"></a>Compoñentes de estimate de proxecto  
 A estrutura de subdivisión do traballo nun proxecto proporciona unha forma de dividir o traballo en tarefas, manter unha xerarquía de tarefas e atribuír unha estimación de esforzo necesaria para completar as tarefas. Tamén pode asociar os roles a unha tarefa para indicar unha estimación do tipo de recurso necesario para finalizar unha tarefa e unha programación.  
  
 A estrutura de subdivisión do traballo axuda a determinar o esforzo de traballo e as estimacións de programación. Por defecto, o proxecto utiliza listas de prezos predefinidas que definiu anteriormente. Os prezos de custos e vendas definidos nas listas de prezos axudan a determinar estimacións financeiras para a subdivisión do traballo.  
  
 Se o seu proxecto está asociado a unha oferta, e a oferta ten unha lista de prezos diferente da predefinida, a lista de prezos da oferta úsase para estimacións de actividades financeiras.  
  
## <a name="import-estimates-from-a-project-into-a-quote"></a>Estimacións de importación dun proxecto a unha oferta  
 Unha vez teña estimacións de proxecto nun proxecto, pode importar estas estimacións na liña da oferta:  
  
-   En **Detalles da liña de oferta**, prema en **Importar de estimacións**. 

-   Seleccione se desexa importar estimacións de proxecto resumidas por tipo de transacción, rol ou nivel de nó da estrutura de subdivisión do traballo.  
  
### <a name="see-also"></a>Consulte tamén  
 [Guía do xestor de proxectos](../psa/project-manager-guide.md)
