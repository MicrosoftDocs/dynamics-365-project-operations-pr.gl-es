---
title: Copiar un proxecto
description: Neste tema se proporciona información sobre copiar proxectos en Dynamics 365 Project Operations.
author: ruhercul
ms.date: 05/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fe76f59b315fd0f46b25e1d116acde1f6b2864d1753e01d6311ea93ae7d116fc
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007189"
---
# <a name="copy-a-project"></a>Copiar un proxecto

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Con Dynamics 365 Project Operations, pode crear rapidamente novos proxectos seleccionando **Copiar proxecto** no formulario **Proxectos**. Para copiar un proxecto, abra o proxecto que desexe copiar e logo seleccione **Copiar proxecto**. A acción copiará o seguinte:

- Propiedades do obxecto 
- Estrutura de subdivisión do traballo
- Membros do equipo do proxecto
- Estimacións do proxecto
- Estimación de gastos do proxecto
- Estimacións de material do proxecto

## <a name="project-properties"></a>Propiedades do obxecto

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
- Data de inicio estimada: é a data na que se crea o proxecto a partir da copia.
- Data de finalización estimada: Esta data axústase en función da data de inicio do novo proxecto que se fixo a partir da copia.
- Esforzo (horas)
- Custo estimado do traballo
- Custo estimado dos gastos
- Custo previsto do material

> [!NOTE]
> A copia do proxecto é unha operación de longa duración. Tamén se copian os rexistros do proxecto, os seus atributos relevantes e moitas entidades relacionadas. Debido á natureza de longa duración da operación, despois de que comece a copia, a páxina do proxecto de destino quédase bloqueada para a edición ata completar a operación de copia.

## <a name="work-breakdown-structure"></a>Estrutura de subdivisión do traballo

Cando se copia o proxecto, copiase toda a estrutura de subdivisión do traballo cargada de recursos. Os recursos nomeados son substituídos por recursos xenéricos. Se os recursos nomeados non teñen as mesmas horas de traballo que o recurso xenérico, o calendario volverá calcularse e as duracións das tarefas poden cambiar.

## <a name="project-team-members"></a>Membros do equipo do proxecto

Cando se copia un equipo do proxecto dese o proxecto de orixe, cópianse os recursos xenéricos. As atribucións de recursos xenéricos tamén se manteñen igual que no proxecto de orixe. Os recursos nomeados converteranse en membros xenéricos do equipo.

## <a name="estimates"></a>Estimacións

Cando se copia o proxecto, as liñas de estimación de recursos, gastos e material cópianse do proxecto de orixe. 

Para obter información sobre como acceder por programación a Copiar proxecto, consulte[Desenvolver modelos de proxecto con Copiar proxecto](dev-copy-project.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
