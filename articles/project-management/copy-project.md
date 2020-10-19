---
title: Copiar un proxecto
description: Neste tema se proporciona información sobre copiar proxectos en Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e35dc725e7938e9f59f7151dd1b37500fabf77a4
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908121"
---
# <a name="copy-a-project"></a>Copiar un proxecto

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Con Dynamics 365 Project Operations, pode crear novos proxectos rapidamente usando a acción **Copiar proxecto** do formulario **Proxectos**. Para copiar un proxecto, seleccione un proxecto e logo seleccione **Copiar**. A acción copiará:

- Propiedades do obxecto
- A estrutura de subdivisión do traballo
- Membros do equipo do proxecto
- Estimacións do proxecto
- Estimación de gastos do proxecto

## <a name="project-properties"></a>Propiedades do proxecto

Cando se copia o proxecto, copianse os valores dos seguintes campos:

- Nome
- Descripción
- Cliente
- Modelo do calendario
- Moeda
- Unidade de contratación
- Xestor de proxectos
- Estado
- Estado xeral do proxecto
- Comentarios
- Estimacións
- Data de inicio estimada
- Data de finalización
- Esforzo (horas)
- Custo estimado do traballo
- Custo estimado dos gastos

## <a name="work-breakdown-structure"></a>Estrutura de subdivisión do traballo

Cando se copia o proxecto, copiase toda a estrutura de subdivisión do traballo cargada de recursos. Os recursos nomeados son substituídos por recursos xenéricos. Se os recursos nomeados non teñen as mesmas horas de traballo que o recurso xenérico, o calendario volverá calcularse e as duracións das tarefas poden cambiar.

## <a name="project-team-members"></a>Membros do equipo do proxecto

Cando se copia un equipo do proxecto dese o proxecto de orixe, cópianse os recursos xenéricos. As atribucións de recursos xenéricos tamén se manteñen igual que no proxecto de orixe. Os recursos nomeados converteranse en membros xenéricos do equipo.

## <a name="estimates"></a>Estimacións

Cando se copia o proxecto, as liñas de estimación de recursos e gastos copianse desde o proxecto de orixe.