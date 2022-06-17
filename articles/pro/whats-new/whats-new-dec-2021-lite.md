---
title: 'Novidades de decembro de 2021: implantación lite de Project Operations'
description: Este artigo ofrece información sobre as actualizacións de calidade que están dispoñibles na versión de decembro de 2021 da implantación de Project Operations lite.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 301acc5be76fb0318d6298820b62ae5bb05efac3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914078"
---
# <a name="whats-new-december-2021---project-operations-lite-deployment"></a>Novidades de decembro de 2021: implantación lite de Project Operations

_Aplícase a: Despregamento de Lite - acordo para facturación proforma_

Este artigo aplícase aos seguintes compoñentes e versións de Microsoft Dynamics 365 Project Operations:

- Operacións do proxecto en a Dataverse versión do entorno 4.27.0.195, 4.27.0.242, 4.27.0.244


## <a name="features-included-in-this-release"></a>Funcionalidades incluídas nesta versión

### <a name="subcontract-management"></a>Xestión de subcontratación 

- [Subcontratación de membros do equipo do proxecto](../subcontracting/subcontracting-project-team-members.md) : Un xestor de proxecto pode crear membros do equipo nomeados ou xenéricos con subcontratos e liñas de subcontratos para afectar o persoal e a estimación.
- [Opcións de subcontratación dos membros do equipo do proxecto](../subcontracting/subcon-options.md) : ao facer eleccións de persoal para membros do equipo do proxecto nomeados ou xenéricos, o director do proxecto pode revisar os subcontratos existentes ou crear novos subcontratos para un ou máis membros do equipo do proxecto. 
- [Estimación de custos das asignacións de recursos subcontratados](../subcontracting/costing-subcon-ra.md) : A estimación do custo do proxecto terá en conta as asignacións de recursos subcontratados e custaraas mediante as listas de prezos de compra asociadas ás subcontratas. 
- [Configurar Schedule Board para mostrar os traballadores contratados e a capacidade subcontratada](../subcontracting/configure-sb-subcon.md) : O cadro de programación en Operacións do proxecto agora pódese configurar para buscar e suxerir o tipo de traballadores contratados de recursos reservables e capacidade subcontratada xunto cos empregados. Esta configuración pódese aplicar cando se buscan recursos no contexto da dotación de persoal para un requirimento específico do proxecto ou cando se busca fóra do contexto dun requisito do proxecto.
- [Dotación de persoal dun proxecto con traballadores contratados e capacidade subcontratada](../subcontracting/staffing-cw.md) : Agora pódense reservar traballadores por contrato en proxectos que aproveitan as experiencias do consello de programación.
- [Rexistro de tempo, gastos e uso de material en proxectos para compoñentes subcontratados](../subcontracting/recording-subcon-actuals.md) : Os traballadores contratados poden rexistrar o tempo e os gastos, e os membros do equipo do proxecto tamén poden rexistrar o uso dos materiais adquiridos mediante un subcontrato nun proxecto. Isto dará lugar ao rexistro de custos precisos nos proxectos que utilicen capacidade ou materiais adquiridos.
- [Transicións estatais nun subcontrato](../subcontracting/subcon-states.md) : Pódense confirmar os subcontratos para completar a negociación co provedor, pecharse para indicar a finalización da entrega ou cancelarse para indicar a rescisión do contrato co provedor antes de completar a entrega.

### <a name="task-planning"></a>Planificación de tarefas
- Resolución de problemas mellorada para administradores de sistemas. Cando un usuario non pode abrir un proxecto, o administrador pode revisar os erros non relacionados coa licenza xerados desde Project for the web en [Rexistros de programación de proxectos](../../project-management/schedule-api-logs.md).
- [Use listas de verificación de tarefas en Microsoft Project para a web](https://support.microsoft.com/en-us/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c). En Microsoft Project para a web, pode engadir unha lista de verificación a unha tarefa para facer un seguimento de elementos específicos.

## <a name="quality-updates"></a>Actualizacións de calidade

| **Área de funcionalidades** | **Número de referencia** | **Actualización de calidade** |
| --- | --- | --- |
| Planificación e rastrexo | 2392596 | As API de programación agora permiten actualizacións de **Esforzo restante**, **rematado**, e **% Completado** campos. |
| Planificación e rastrexo | 2478497 | Programar API **Número de actividade** e **ID da tarefa** Os campos poden estar en branco ao ingresar porque o sistema os encherá mediante a numeración automática.|
| Tempo e gasto | 2468135 | O número de reintentos de aprobación redúcese de cinco a tres. |
| Tempo e gasto | 2468188 | Solucionouse o problema co texto do rexistro que superaba a lonxitude máxima no ficheiro **texto de nota** atributo do **anotación** entidade. |
