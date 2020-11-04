---
title: Copiar un proxecto
description: Neste tema se proporciona información sobre copiar proxectos en Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: cf80f2a1cd27aae33d123e45dee70d94ea4d01a9
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076073"
---
# <a name="copy-a-project"></a>Copiar un proxecto

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Con Dynamics 365 Project Operations, pode crear novos proxectos rapidamente seleccionando **Copiar proxecto** no formulario **Proxectos**. Para copiar un proxecto, abra o proxecto que desexe copiar e logo seleccione **Copiar proxecto**. A acción copiará:

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

Para obter información sobre como acceder por programación a Copiar proxecto, consulte[Desenvolver modelos de proxecto con Copiar proxecto](dev-copy-project.md).
