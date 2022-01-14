---
title: Estimación de custos das asignacións de recursos subcontratados
description: Este tema explica como Microsoft Dynamics 365 Project Operations calcula a estimación do custo das asignacións de recursos subcontratados.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 5a94840a3735639532683153105fea85bea99c9d
ms.sourcegitcommit: 45893132bd8bfaf944ee0ac855484684dd1ee945
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 12/09/2021
ms.locfileid: "7903016"
---
# <a name="cost-estimation-of-subcontracted-resource-assignments"></a>Estimación de custos das asignacións de recursos subcontratados

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

As asignacións de tarefas dos membros do equipo do proxecto subcontratados cústanse mediante o **Compra** lista de prezos adxunta ao subcontrato no rexistro do membro do equipo relacionado. Isto é diferente da forma en que se custa as asignacións de recursos dos empregados cando as asignacións de tarefas dos recursos dos empregados se custan usando o **Custo** lista de prezos que se anexa á unidade de contratación do proxecto. 

Para os membros xenéricos do equipo do proxecto que están subcontratados, as tarefas cústanse mediante unha configuración de prezos baseada en funcións na lista de prezos de compra adxunta ao subcontrato. Os prezos de compra tamén se poden configurar específicamente para cada recurso. Estes prezos específicos de recursos terán prioridade cando se custe as asignacións de tarefas dos membros do equipo do proxecto nomeados son traballadores por contrato. 

A prioridade de usar o prezo de compra específico do rol fronte ao recurso específico está determinada pola configuración da prioridade da dimensión de prezos en **Parámetros > Dimensións de prezos baseadas na cantidade**.

Esta funcionalidade de derivación dinámica dos prezos en función da configuración de dimensións para os prezos de compra dos subcontratistas é semellante á forma en que se derivan os custos e as tarifas de factura para os empregados a tempo completo. 

## <a name="creating-task-assignments-for-getting-cost-estimates-of-subcontractor-resources"></a>Creación de tarefas para obter estimacións de custos dos recursos dos subcontratistas

As asignacións de tarefas para os subcontratistas pódense crear de dúas formas: 
- Usando o **Tarefas** ficha.
- Usando o **Equipo** ficha.

### <a name="creating-resources-assignments-using-the-tasks-tab"></a>Creación de asignacións de recursos mediante a pestana Tarefas
Usando o **Recursos** lista na **Tarefas** para unha tarefa específica, pode crear unha asignación de tarefas para un recurso con nome ou un recurso xenérico. Se selecciona un recurso nomeado do **Recursos asignados** menú despregable na tarefa e este recurso é un traballador por contrato, o recurso nomeado asígnase á tarefa e créase un rexistro de membro do equipo do proxecto correspondente co tipo de traballador definido como **Traballador por Contrato** e **Validez** configurado para **Non válido**. Como seguinte paso, terás que abrir o rexistro do membro do equipo do proxecto e seleccionar unha liña de subcontrato e subcontrato. Isto actualizará a asignación de tarefas para ter unha referencia á liña de subcontrato e subcontrato e tamén actualizará o estado do membro do equipo para **Válido**.

Se decides crear un membro xenérico do equipo desde o **Recursos asignados** menú despregable na tarefa, o **Creación xenérica de membros do equipo** O diálogo permitirá seleccionar unha liña de subcontrato e subcontrato. Cando se asigna o recurso xenérico á tarefa e se crea o correspondente rexistro do membro do equipo do proxecto, notará que o rexistro do membro do equipo do proxecto se crea co tipo de traballador definido como **Traballador por Contrato** e **Validez** configurado para **Válido**.

### <a name="creating-project-team-members-using-the-team-tab"></a>Creando membros do equipo do proxecto usando a pestana Equipo
Usando a pestana Equipo do proxecto, pode crear un membro do equipo xenérico ou nomeado. Ao crear o membro do equipo, tes a opción de seleccionar a liña de subcontrato e subcontrato. Despois de crear o membro do equipo, terás que asignalo a unha tarefa usando o **Recursos asignados** menú despregable na tarefa. 

## <a name="updating-estimates"></a>Actualizando estimacións
Despois de asignar aos membros do equipo do proxecto tarefas, terás que navegar ata o **Estimacións** ficha no proxecto e seleccione **Actualizar prezos** para garantir que as taxas de custo das asignacións de recursos do subcontratista se actualicen en función da lista de prezos de compra adxunta ao subcontrato. Teña en conta que non se xeran estimacións para tarefas non asignadas en Microsoft Dynamics 365 Project Operations. Como resultado, terás que crear tarefas para determinar o prezo e o custo de varias tarefas do teu proxecto. 

> [NOTA!] Membros do equipo do proxecto que teñen **Tipo de traballador** como **Traballador contratado** pero non teñen unha referencia de subcontrato están marcados como **Non válido** no **Membros do equipo do proxecto** reixa. Se hai algún membro do equipo do proxecto con este estado, abra o rexistro do membro do equipo do proxecto e actualice manualmente os campos da liña de subcontrato e subcontrato para que a estimación do custo financeiro reflicta con precisión o custo do subcontratista no **Estimacións** ficha. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
