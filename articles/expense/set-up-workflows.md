---
title: Configurar fluxos de traballo para a xestión de gastos
description: Pode configurar un proceso de fluxo de traballo que se empregue para revisar e aprobar documentos de viaxes e gastos.
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: aab6e18d1ddcffa57cf7cd4cb09eec5a4b89c0fd
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001019"
---
# <a name="set-up-workflows-for-expense-management"></a>Configurar fluxos de traballo para a xestión de gastos

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Pode configurar un proceso de fluxo de traballo para revisar e aprobar documentos de viaxes e gastos. Pode definir fluxos de traballo para informes de gastos, solicitudes de viaxes e solicitudes de adianto de efectivo.

Un fluxo de traballo representa un proceso de negocio e define como un documento flúe a través do sistema. O fluxo de traballo tamén indica quen debe completar unha tarefa ou aprobar un documento. Hai varios beneficios de usar o sistema de fluxo de traballo na súa organización:

- **Procesos uniformes**: Pode definir o proceso de aprobación de documentos específicos, como solicitudes de compra e informes de gastos. O uso do sistema de fluxo de traballo axuda a garantir que os documentos se procesan e aproban de xeito uniforme e eficiente.
- **Visibilidade do proceso**: Pode rastrexar o estado, o historial e os indicadores de rendemento dunha instancia de fluxo de traballo específica. Isto axúdalle a determinar se se deben facer cambios no fluxo de traballo para mellorar a eficiencia.
- **Lista de traballo centralizada**: Os usuarios poden ver unha lista de traballo centralizada para ver as tarefas e aprobacións do fluxo de traballo que se lles atribuíron. 

## <a name="workflow-types"></a>Tipos de fluxo de traballo

A seguinte táboa mostra os tipos de fluxos de traballo que pode crear **Xestión de gastos**.


|              <strong>Tipo</strong>              |                   <strong>Use este tipo para</strong>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <strong>Aprobación automática de informes de gastos</strong> |            Cree fluxos de traballo de aprobación para informes de gastos.             |
|  <strong>Publicación automática de informes de gastos</strong>   |        Cree fluxos de traballo de publicación automática para informes de gastos.        |
|       <strong>Elemento de liña de gasto</strong>        |     Cree fluxos de traballo de aprobación para elementos de liña en informes de gastos.      |
| <strong>Publicación automática de elemento de liña de gasto</strong> | Cree fluxos de traballo de publicación automática para elementos de liña en informes de gastos. |
|       <strong>Requirimento de viaxe</strong>       |          Cree fluxos de traballo de aprobación para solicitudes de viaxes.           |
|      <strong>Solicitude de adianto de efectivo</strong>      |         Cree fluxos de traballo de aprobación para solicitudes de adianto de efectivo.          |
|        <strong>Recuperación do IVE</strong>        | Cree fluxos de traballo de aprobación para a recuperación do imposto sobre o valor engadido (IVE).  |


[!INCLUDE[footer-include](../includes/footer-banner.md)]