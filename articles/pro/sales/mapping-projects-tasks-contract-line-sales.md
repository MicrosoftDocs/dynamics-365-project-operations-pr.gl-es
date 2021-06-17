---
title: Asignar proxectos e tarefas a unha liña de contrato baseado en proxecto
description: Este tema ofrece información sobre como engadir e eliminar proxectos e tarefas a unha liña de contrato.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4b86e03192625b0dabb89080f2ade1ed9e3567cf
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994630"
---
# <a name="map-projects-and-tasks-to-a-project-based-contract-line"></a>Asignar proxectos e tarefas a unha liña de contrato baseada en proxecto 

_**Aplícase a:** Despregamento Lite - factura proforma, Project Operations para situacións baseadas en recursos/sen fornecemento_

Nas liñas de contrato baseado en proxecto, pode asignar tarefas específicas dun proxecto á liña de contrato.

Cando asigne tarefas específicas a unha liña de contrato, o método de facturación, as opcións de imputabilidade, os límites non superables e os clientes definidos na liña de contrato só serán aplicables a esas tarefas específicas.

Se ten un escenario onde unha fase dun proxecto, por exemplo a fase de prototipo, é de prezo fixo e todas as outras fases son de tempo e material, poderá asociar a fase de prototipo e todas as tarefas secundarias asociadas á liña de contrato para esa fase cun método de facturación de prezo fixo.

Todas as outras fases da estrutura de subdivisión do traballo (WBS) do proxecto poden asociarse á liña de contrato baseado e tempo e material.

## <a name="associate-tasks-to-project-based-contract-lines"></a>Asociar tarefas a liñas de contrato baseado en proxecto

As tarefas pódense asociar ás liñas de contrato no separador **Tarefas imputables** na páxina **Liña de contrato** ou no separador **Facturación de tarefas** na páxina de **Proxecto**.

### <a name="from-the-contract-line-page"></a>Desde a páxina Liña de contrato

Complete os seguintes pasos para asociar as tarefas do proxecto á liña de contrato no separador **Tarefas imputables** da páxina **Liña de contrato**.

1. No separador **Xeral** dunha liña de contrato baseado en proxecto, verifique que o campo **Proxecto** está enchido.
2. No campo **Tarefas incluídas**, seleccione **Só tarefas seleccionadas**.
3. Garde as modificacións. O formulario actualizarase e o separador **Tarefas imputables** será visible.
4. Seleccione o separador **Tarefas imputables** e na subgrade seleccione **Engadir unha tarefa de liña de contrato**.
5. Na páxina **Tarefas de liña de contrato**, no despregable **Tarefas**, seleccione a tarefa. 
6. Introduza información no campo **Tipo de facturación** e logo seleccione **Gardar e pechar**. A tarefa seleccionada asóciase á liña de contrato.

> [!NOTE]
> Esta non é a experiencia máis óptima para asociar tarefas de proxecto a liñas de contratación. Cada proxecto terá que asociarse manualmente nesta experiencia. A forma preferida é no separador **Facturación de tarefas** na páxina **Proxecto**.

### <a name="from-the-project-page"></a>Desde a páxina do proxecto

Este é o método óptimo para asociar tarefas a liñas de contrato. Pode seleccionar varias tarefas e asociar todas elas e as tarefas secundarias á liña de contrato seleccionada. Complete os seguintes pasos para asociar tarefas á liña de contrato desde a páxina **Proxecto**.

1. No separador **Xeral** dunha liña de contrato baseado en proxecto, verifique que o campo **Proxecto** está enchido.
2. No campo **Tarefas incluídas**, seleccione **Só tarefas seleccionadas**.
3. Garde a liña de contrato baseado en proxecto. O formulario actualizarase e o separador **Tarefas imputables** será visible. Isto é só para fins de verificación.
4. No separador **Xeral** da liña de contrato baseado en proxecto, no campo **Proxecto**, seleccione a ligazón do proxecto.
5. Na páxina **Proxecto**, seleccione o separador **Configuración de facturación de tarefas**.
6. Hai dúas grades. Unha grade é para as liñas de contrato que se aplican a todo o proxecto. A segunda grade aplícase á configuración de facturación específica da tarefa. Na segunda grade, seleccione unha ou máis tarefas e logo seleccione **Asociar liñas de contrato**.
7. Na páxina de diálogo que se abre, seleccione unha liña de contrato no menú despregable.
8. Use o despregable **Tipo de facturación** para marcar as tarefas como imputables ou non imputables.
9. Marque a caixa de verificación para indicar se a asociación tamén debería incluír tarefas secundarias das tarefas seleccionadas. Ao marcar a caixa tamén se asociarán as tarefas secundarias das tarefas seleccionadas á liña de contrato.
10. Seleccione **Aceptar** para pechar a caixa de diálogo.

## <a name="unassociate-tasks-from-project-based-contract-lines"></a>Desasociar tarefas de liñas de contrato baseado en proxecto

### <a name="from-the-contract-line-page"></a>Desde a páxina Liña de contrato

Complete os seguintes pasos para desasociar as tarefas do proxecto da liña de contrato no separador **Tarefas imputables** da páxina **Liña de contrato**.

1. No separador **Tarefas imputables**, seleccione **Eliminar unha tarefa de liña de contrato**.
2. Unha mensaxe de advertencia indica que a eliminación desta asociación podería provocar a reversión de calquera dato real rexistrado previamente na tarefa. Seleccione **Aceptar** no diálogo para eliminar a asociación entre a tarefa e a liña de contrato baseada en proxecto. 

> [!NOTE]
> Isto non elimina a tarefa do proxecto. Pola contra, elimina a asociación da tarefa da liña de contrato baseado en proxecto.

### <a name="from-the-project-page"></a>Desde a páxina do proxecto

Esta é a experiencia máis óptima para desasociar tarefas de liñas de contratación. Pode seleccionar varias tarefas e desasociar todas elas e as tarefas secundarias da liña de contrato seleccionada. Complete os seguintes pasos para desasociar tarefas da liña de contrato.

1. No separador **Xeral** da liña de contrato baseado en proxecto, no campo **Proxecto**, prema a ligazón para o proxecto.
2. Na páxina **Proxecto**, seleccione o separador **Configuración de facturación de tarefas**.
3. Hai dúas grades na páxina. Unha grade é para as liñas de contrato que se aplican a todo o proxecto e a segunda aplícase á configuración de facturación específica da tarefa. Na segunda grade, seleccione unha ou máis tarefas e logo seleccione **Desasociar liñas de contrato**.
4. Na páxina de diálogo que se abre, seleccione unha liña de contrato no menú despregable.
5. Marque a caixa de verificación para indicar se a asociación tamén debería eliminarse das tarefas secundarias das tarefas seleccionadas. Ao marcar a caixa tamén se desasociarán as tarefas secundarias das tarefas seleccionadas da liña de contrato.
6. Seleccione **Aceptar**. Unha mensaxe de advertencia indica que a eliminación desta asociación podería provocar a reversión de calquera dato real rexistrado na tarefa previamente. Seleccione **Aceptar** no diálogo de advertencia para eliminar a asociación entre a tarefa e a liña de contrato baseada en proxecto.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
