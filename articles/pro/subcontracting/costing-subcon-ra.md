---
title: Estimación de custos das atribucións de recursos subcontratados
description: Este artigo explica como Microsoft Dynamics 365 Project Operations calcula a estimación do custo das atribucións de recursos subcontratados.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 9fded1baa63d2defc134994c858dfc6c09f75082
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522652"
---
# <a name="cost-estimation-of-subcontracted-resource-assignments"></a>Estimación de custos das atribucións de recursos subcontratados

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

O custo das atribucións de tarefas dos membros do equipo do proxecto subcontratados determínase mediante a lista de prezos **Compra** anexa ao subcontrato no rexistro do membro do equipo relacionado. Isto é diferente de como se determina o custo dos recursos dos empregados cando o custo das atribucións de tarefas dos recursos de empregados se determina usando a lista de prezos **Custo** que se anexa á unidade de contratación do proxecto. 

Para os membros xenéricos do equipo do proxecto que se subcontratan, as atribucións se calculan utilizando una configuración de prezos baseada no rol na lista de prezos de compra anexa ao subcontrato. Os prezos de compra tamén se poden configurar especificamente para cada recurso. Estes prezos específicos de recursos terán prioridade cando as atribucións de tarefas dos membros do equipo do proxecto nomeados sexan traballadores por contrato. 

A prioridade de usar o prezo de compra específico do rol fronte ao específico do recurso está determinada pola configuración da prioridade da dimensión de prezos en **Parámetros > Dimensións de prezos baseadas na cantidade**.

Esta funcionalidade de derivación dinámica dos prezos en función da configuración de dimensións para os prezos de compra dos subcontratistas é semellante á forma en que se derivan as taxas de custo e facturación para os empregados a tempo completo. 

## <a name="creating-task-assignments-for-getting-cost-estimates-of-subcontractor-resources"></a>Creación de tarefas para obter estimacións de custos dos recursos dos subcontratistas

As atribucións de tarefas para os subcontratistas pódense crear de dúas formas: 
- Usando o separador **Tarefas**.
- Usando o separador **Equipo**.

### <a name="creating-resources-assignments-using-the-tasks-tab"></a>Creación de atribucións de recursos mediante o separador Tarefas
Usando a lista **Recursos** no separador **Tarefas** para unha tarefa específica, pode crear unha atribución de tarefas para un recurso nomeado ou un recurso xenérico. Se selecciona un recurso nomeado do menú despregable **Recursos atribuídos** na tarefa e este recurso é un traballador por contrato, o recurso nomeado atribúese á tarefa e créase un rexistro de membro do equipo do proxecto correspondente co tipo de traballador definido como **Traballador por contrato** e **Validez** configurada en **Non válido**. Como paso seguinte, terá que abrir o rexistro do membro do equipo do proxecto e seleccionar un subcontrato e unha liña de subcontrato. Isto actualizará a atribución de tarefas para ter unha referencia ao subcontrato e á liña de subcontrato e tamén actualizará o estado do membro do equipo a **Válido**.

Se decide crear un membro xenérico do equipo desde o menú despregable **Recursos atribuídos** na tarefa, a caixa de diálogo **Creación de membro de equipo xenérico** permitirá seleccionar un subcontrato e unha liña de subcontrato. Cando se lle atribúe o recurso xenérico á tarefa e se crea o correspondente rexistro do membro do equipo do proxecto, verá que o rexistro do membro do equipo do proxecto se crea co tipo de traballador definido como **Traballador por contrato** e **Validez** configurado en **Válido**.

### <a name="creating-project-team-members-using-the-team-tab"></a>Creación membros do equipo do proxecto usando o separador Equipo
Usando o separador Equipo no proxecto, pode crear un membro do equipo xenérico ou nomeado. Ao crear o membro do equipo, pode seleccionar o subcontrato e a liña de subcontrato. Despois de crear o membro do equipo, terá que atribuílo a unha tarefa mediante o menú despregable **Recursos asignados** na tarefa. 

## <a name="updating-estimates"></a>Actualización de estimacións
Despois de atribuír tarefas aos membros do equipo do proxecto, terá que navegar ata o separador **Estimacións** no proxecto e seleccionar **Actualizar prezos** para garantir que as taxas de custo das atribucións de recursos do subcontratista se actualicen en función da lista de prezos de compra adxunta ao subcontrato. Non se xeran estimacións para tarefas non atribuídas en Microsoft Dynamics 365 Project Operations. Como resultado, terá que crear tarefas para determinar o prezo e o custo de varias tarefas do seu proxecto. 

> [NOTA!] Os membros do equipo do proxecto que teñen **Tipo de traballador** como **Traballador por contrato** pero non teñen unha referencia de subcontrato están marcados como **Non válido** na grade **Membros do equipo do proxecto**. Se hai algún membro do equipo do proxecto con este estado, abra o rexistro do membro do equipo do proxecto e actualice manualmente os campos de subacontratación e liña de subcontratación para que a estimación do custo financeiro reflicta con precisión o custo do subcontratista no separador **Estimacións**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
