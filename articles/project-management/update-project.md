---
title: Crear e actualizar un proxecto
description: Neste tema se proporciona información sobre actualizar proxectos en Project Operations.
author: ruhercul
ms.date: 10/20/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 07f96973a1341e65e648f126a931d72454334e9c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8592506"
---
# <a name="create-and-update-a-project"></a>Crear e actualizar un proxecto

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

O seguinte é un resumo dos campos que se poden actualizar nun proxecto despois da súa creación. Isto tamén inclúe todas as implicacións aplicables en función destas actualizacións.

## <a name="project-detail-fields"></a>Campos de detalle do proxecto

- **Nome**: O título do proxecto.
- **Descrición**: Unha visión xeral do proxecto.
- **Cliente**: A empresa á que se entregará o proxecto.
- **Modelo de calendario**: As horas de traballo do proxecto. Cando se cambia o campo, recalculase toda a programación.
- **Moeda**: A moeda para o proxecto. O valor predefinido deste campo baséase na moeda definida na unidade de contratación. Cando se actualiza a unidade de contratación, tamén se actualiza o campo.
- **Unidade de contratación**: A unidade organizativa que representa ao grupo ou división da empresa que é o principal responsable de gañar a venda e xestionar a entrega de traballos e servizos ao cliente.  Cando a unidade organizativa do xestor do proxecto non está definida, este campo adopta por defecto o valor definido nos parámetros do proxecto.
- **Xestor de proxectos**: O membro do equipo do proxecto que ten a autoridade para revisar e aprobar as entradas de tempo e os gastos.

## <a name="estimate-fields"></a>Estimar campos

- **Data de inicio estimada**: A data na que comezará o proxecto. Cando se actualiza este campo, as tarefas do proxecto moveranse proporcionalmente coa nova data de inicio.
- **Data de finalización**: A data na que está previsto que remate o proxecto.
- **Esforzo**: O esforzo estimado do proxecto. Cando se engaden tarefas ao proxecto, este campo xa non se pode editar.
- **Custo laboral estimado**: O custo laboral estimado do proxecto. Cando se engaden custos laborais ao proxecto, este campo xa non se pode editar.
- **Gastos estimados**: Os gastos estimados do proxecto. Cando se engaden gastos ao proxecto, este campo xa non se pode editar.

## <a name="project-actual-fields"></a>Campos reais do proxecto
- **Inicio real**: A data de inicio do proxecto.
- **Final real**: Actualizarase cando se complete un proxecto.

## <a name="project-status-fields"></a>Campos de estado do proxecto

- **Estado xeral do proxecto**: A saúde xeral do proxecto proporcionada polo xestor do proxecto.
- **Comentarios**: Unha narración sobre a saúde actual do proxecto proporcionada polo xestor do proxecto.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
