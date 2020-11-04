---
title: Configurar fluxos de traballo de xestión de gastos
description: Pode configurar un proceso de fluxo de traballo para revisar e aprobar documentos de viaxes e gastos.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0af23ed2cf172e4c90de72f5db389c349303c039
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076286"
---
# <a name="set-up-expense-management-workflows"></a>Configurar fluxos de traballo de xestión de gastos

[!include [banner](../includes/banner.md)]

Pode configurar un proceso de fluxo de traballo que se empregue para revisar e aprobar documentos de viaxes e gastos. Os documentos para os que se poden definir fluxos de traballo inclúen informes de gastos, solicitudes de viaxes e solicitudes de adianto de efectivo.

Un fluxo de traballo representa un proceso de negocio. Define como un documento flúe a través do sistema e indica quen debe completar unha tarefa ou aproba un documento. Hai varios beneficios de usar o sistema de fluxo de traballo na súa organización:

-   **Procesos uniformes** : Pode definir o proceso de aprobación de documentos específicos, como solicitudes de compra e informes de gastos. O uso do sistema de fluxo de traballo axuda a garantir que os documentos se procesan e aproban de xeito uniforme e eficiente.

-   Visibilidade do proceso: Pode rastrexar o estado, o historial e os indicadores de rendemento dunha instancia de fluxo de traballo específica. Isto axúdalle a determinar se se deben facer cambios no fluxo de traballo para mellorar a eficiencia.

-   Lista de traballo centralizada: Os usuarios poden ver unha lista de traballo centralizada para ver as tarefas e aprobacións do fluxo de traballo que se lles atribuíron. 

**Os tipos de fluxos de traballo que pode crear**

A seguinte táboa mostra os tipos de fluxos de traballo que pode crear **Gastos**.


|              <strong>Tipo</strong>              |                   <strong>Use este tipo para</strong>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <strong>Informe de gastos</strong>         |            Cree fluxos de traballo de aprobación para informes de gastos.             |
|  <strong>Publicación automática de informes de gastos</strong>   |        Cree fluxos de traballo de publicación automática para informes de gastos.        |
|       <strong>Elemento de liña de gasto</strong>        |     Cree fluxos de traballo de aprobación para elementos de liña en informes de gastos.      |
| <strong>Publicación automática de elemento de liña de gasto</strong> | Cree fluxos de traballo de publicación automática para elementos de liña en informes de gastos. |
|       <strong>Requirimento de viaxe</strong>       |          Cree fluxos de traballo de aprobación para solicitudes de viaxes.           |
|      <strong>Solicitude de adianto de efectivo</strong>      |         Cree fluxos de traballo de aprobación para solicitudes de adianto de efectivo.          |
|        <strong>Recuperación do IVE</strong>        | Cree fluxos de traballo de aprobación para a recuperación do imposto sobre o valor engadido (IVE).  |
