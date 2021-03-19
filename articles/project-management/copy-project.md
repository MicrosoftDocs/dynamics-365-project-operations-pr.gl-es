---
title: Copiar un proxecto
description: Neste tema se proporciona información sobre copiar proxectos en Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 02/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: af1942e81691d9e13fdcbbf68599c1a8a4004582
ms.sourcegitcommit: 24528bb9c0ef8898077cb3bc672daa211c0e73aa
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 03/04/2021
ms.locfileid: "5479517"
---
# <a name="copy-a-project"></a>Copiar un proxecto

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Con Dynamics 365 Project Operations, pode crear rapidamente novos proxectos seleccionando **Copiar proxecto** no formulario **Proxectos**. Para copiar un proxecto, abra o proxecto que desexe copiar e logo seleccione **Copiar proxecto**. A acción copiará:

- Propiedades do proxecto (a data estimada de inicio copiase do proxecto de orixe)
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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
