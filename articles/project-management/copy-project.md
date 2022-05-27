---
title: Copiar un proxecto
description: Neste tema se proporciona información sobre copiar proxectos en Dynamics 365 Project Operations.
author: ruhercul
ms.date: 03/07/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: e9b637d2d282d123dfacb8a295292ea06549aa1e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574428"
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
- Listas de verificación do proxecto
- Cubos de proxectos

## <a name="project-properties"></a>Propiedades do obxecto

Cando se copia o proxecto, cópianse os valores dos seguintes campos.

| Campo | Operacións do proxecto Materiais non almacenados | Proxecto Operacións Lite | Proxecto para a Web |
|-------|------------------------------------------|-------------------------|---------------------|
| Nome | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Descripción | :heavy_check_mark: | :heavy_check_mark: | |
| cliente/a | :heavy_check_mark: | :heavy_check_mark: | |
| Modelo do calendario | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Moeda | :heavy_check_mark: | :heavy_check_mark: | |
| Unidade de contratación | :heavy_check_mark: | :heavy_check_mark: | |
| Empresa propietaria | :heavy_check_mark: | | |
| Xestor de proxectos | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Progresión | :heavy_check_mark: | :heavy_check_mark: | |
| Estado xeral do proxecto | :heavy_check_mark: | :heavy_check_mark: | |
| Comentarios | :heavy_check_mark: | :heavy_check_mark: | |
| Estimacións | :heavy_check_mark: | :heavy_check_mark: | |
| <p>Data de inicio estimada</p><p><strong>Nota:</strong> Este campo especifica a data na que se crea o proxecto a partir da copia. | :heavy_check_mark: | :heavy_check_mark: | |
| <p>Data estimada de finalización</p><p><strong>Nota:</strong> A data neste campo axústase en función da data de inicio do novo proxecto que se fixo a partir da copia.</p> | :heavy_check_mark: | :heavy_check_mark: | |
| Esforzo (horas) | :heavy_check_mark: | :heavy_check_mark: | |
| Custo estimado do traballo | :heavy_check_mark: | :heavy_check_mark: | |
| Custo estimado dos gastos | :heavy_check_mark: | :heavy_check_mark: | |
| Custo previsto do material | | :heavy_check_mark: | |

> [!NOTE]
> A copia do proxecto é unha operación de longa duración. Tamén se copian os rexistros do proxecto, os seus atributos relevantes e moitas entidades relacionadas. Debido á natureza de longa duración da operación, despois de que comece a copia, a páxina do proxecto de destino quédase bloqueada para a edición ata completar a operación de copia.

## <a name="work-breakdown-structure"></a>Estrutura de subdivisión do traballo

Cando se copia o proxecto, copiase toda a estrutura de subdivisión do traballo cargada de recursos. Os recursos nomeados son substituídos por recursos xenéricos. Se os recursos nomeados non teñen o mesmo horario de traballo que o recurso xenérico, a programación volverase calcular e a duración das tarefas pode cambiar.

## <a name="project-team-members"></a>Membros do equipo do proxecto

Cando se copia un equipo do proxecto dese o proxecto de orixe, cópianse os recursos xenéricos. As atribucións de recursos xenéricos tamén se manteñen igual que no proxecto de orixe. Os recursos nomeados converteranse en membros xenéricos do equipo.

> [!NOTE]
> Os membros do equipo e as tarefas non se copian en Project for the Web.

## <a name="estimates"></a>Estimacións

Cando se copia o proxecto, as liñas de estimación de recursos, gastos e material cópianse do proxecto de orixe. 

Para obter información sobre como acceder por programación a Copiar proxecto, consulte[Desenvolver modelos de proxecto con Copiar proxecto](dev-copy-project.md).

## <a name="quotes-and-contracts"></a>Ofertas e contratos

As cotizacións e os contratos non están vinculados ao proxecto de destino.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
