---
title: Novidades de decembro de 2021 - Despregamento de Project Operations lite
description: Este artigo ofrece información sobre as actualizacións de calidade que están dispoñibles na versión de decembro de 2021 do despregamento de Project Operations lite.
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
# <a name="whats-new-december-2021---project-operations-lite-deployment"></a>Novidades de decembro de 2021 - Despregamento de Project Operations lite

_Aplícase a: Despregamento de Lite - acordo para facturación proforma_

Este artigo aplícase aos seguintes compoñentes e versións de Microsoft Dynamics 365 Project Operations:

- Project Operations nun ambiente de Dataverse versión 4.27.0.195, 4.27.0.242, 4.27.0.244


## <a name="features-included-in-this-release"></a>Funcionalidades incluídas nesta versión

### <a name="subcontract-management"></a>Xestión de subcontratos 

- [Subcontratación de membros do equipo do proxecto](../subcontracting/subcontracting-project-team-members.md): Un xestor de proxectos pode crear membros do equipo nomeados ou xenéricos con subcontratos e liñas de subcontratación para afectar ao persoal e á estimación.
- [Opcións de subcontratación dos membros do equipo do proxecto](../subcontracting/subcon-options.md): Ao facer eleccións de persoal para membros do equipo do proxecto nomeados ou xenéricos, o director do proxecto pode revisar os subcontratos existentes ou crear novos subcontratos para un ou máis membros do equipo do proxecto. 
- [Estimación de custos das atribucións de recursos subcontratados](../subcontracting/costing-subcon-ra.md): A estimación do custo do proxecto terá en conta as atribucións de recursos subcontratados e determinará os seus custos utilizando as listas de prezos de compra asociadas aos subcontratos. 
- [Configurar o panel de programación para mostrar os traballadores contratados e a capacidade subcontratada](../subcontracting/configure-sb-subcon.md): O panel de programación en Project Operations agora pódese configurar para buscar e suxerir o tipo de traballadores contratados de recursos reservables e a capacidade subcontratada xunto cos empregados. Esta configuración pódese aplicar cando se buscan recursos no contexto da dotación de persoal para un requisito específico do proxecto ou cando se busca fóra do contexto dun requisito do proxecto.
- [Dotación de persoal dun proxecto con traballadores contratados e capacidade subcontratada](../subcontracting/staffing-cw.md): Agora pódense reservar traballadores por contrato en proxectos que aproveitan as experiencias do panel de programación.
- [Rexistro de tempo, gastos e uso de material en proxectos para compoñentes subcontratados](../subcontracting/recording-subcon-actuals.md): Os traballadores por contrato poden rexistrar o tempo e os gastos, e os membros do equipo do proxecto tamén poden rexistrar o uso dos materiais adquiridos mediante un subcontrato nun proxecto. Isto dará lugar ao rexistro de custos precisos nos proxectos que utilicen capacidade ou materiais adquiridos.
- [Transicións de estado nun subcontrato](../subcontracting/subcon-states.md): Pódense confirmar os subcontratos para completar a negociación co vendedor, pecharse para indicar a finalización da entrega ou cancelarse para indicar a rescisión do contrato co vendedor antes de completar a entrega.

### <a name="task-planning"></a>Planificación de tarefas
- Mellora da resolución de problemas para administradores do sistema. Cando un usuario non pode abrir un proxecto, o administrador pode revisar os erros non relacionados coa licenza xerados desde Project for the Web en [Rexistros de programación de proxectos](../../project-management/schedule-api-logs.md).
- [Usar listas de verificación de tarefas en Microsoft Project for the Web](https://support.microsoft.com/en-us/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c). En Microsoft Project for the Web, pode engadir unha lista de verificación a unha tarefa para facer un seguimento de elementos específicos.

## <a name="quality-updates"></a>Actualizacións de calidade

| **Área de funcionalidades** | **Número de referencia** | **Actualización de calidade** |
| --- | --- | --- |
| Planificación e rastrexo | 2392596 | As API de programación agora permiten actualizacións dos campos **Esforzo restante**, **Esforzo rematado** e **% completado**. |
| Planificación e rastrexo | 2478497 | Os campos **Número de actividade** e **ID de tarefa** das API de programación poden estar baleiros na entrada porque o sistema os encherá mediante a numeración automática.|
| Tempo e gasto | 2468135 | O número de reintentos de aprobación redúcese de cinco a tres. |
| Tempo e gasto | 2468188 | Solucionouse o problema co texto do rexistro que superaba a lonxitude máxima no atributo **notetext** da entidade **anotación**. |
