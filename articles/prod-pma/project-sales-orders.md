---
title: Pedidos de venda de proxectos para proxectos de tempo e material
description: Este tema explica como crear pedidos de venda baseados en proxectos para proxectos de tempo e material.
author: Yowelle
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 3653a6869dab323be88f1fd0f9fd0f2cb35c456f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076117"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a>Pedidos de venda de proxectos para proxectos de tempo e material

[!include[banner](../includes/banner.md)]

Este tema describe como crear un pedido de venda para un proxecto. Os pedidos de venda só se poden crear para proxectos de tipo **tempo e material**.

Se un proxecto de tempo e material ten varias fontes de financiamento no contrato do proxecto, debe habilitar o parámetro **Permitir pedidos de venda para proxectos con varias fontes de financiamento** na páxina **Parámetros de xestión de proxectos e contabilidade**. 

> [!NOTE]
> - A asistencia para pedidos de vendas de proxectos con varias fontes de financiamento está dispoñible a partir da versión da aplicación 10.0.2 e superior.
> - O parámetro para habilitar a asistencia para pedidos de venda de proxectos con varias fontes de financiamento eliminarase na onda da versión de abril de 2020, despois do cal a funcionalidade sempre estará habilitada.

Pode crear pedidos de venda baseados en proxectos de dous xeitos:

- Vaia ao propio proxecto. No panel Acción, seleccione **Xestionar > Tarefas do artigo > Pedido de venda**. A información do proxecto será o pedido de venda predefinido do proxecto. Se o contrato do proxecto ten máis dunha fonte de financiamento, deberá seleccionar a fonte de financiamento para configurar o cliente para o pedido de venda. Se só hai unha fonte de financiamento para o proxecto, o cliente configurarase automaticamente.
- Vaia á páxina de lista **Todos os pedidos de venda** e cree un novo pedido de venda. Deberá seleccionar o proxecto para o pedido de venda. Despois de seleccionar o proxecto, configurarase o cliente desde a fonte de financiamento ou deberá seleccionar a fonte de financiamento se o contrato do proxecto ten varias fontes de financiamento.
