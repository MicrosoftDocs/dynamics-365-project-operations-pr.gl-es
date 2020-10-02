---
title: Cumprimento dos requisitos de recursos xenéricos
description: Este tema proporciona información sobre a reserva de recursos nomeados para un requisito de recursos xenérico.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 76dd47fa2451b5cb61298ff332d77bae646a288a
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897584"
---
# <a name="generic-resource-requirement-fulfillment"></a>Cumprimento dos requisitos de recursos xenéricos

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Pode reservar un recurso nomeado para substituír un recurso xenérico que teña un requisito de recursos.

1. Na páxina **Proxectos**, seleccione o separador **Equipo**.
2. Seleccione o recurso xenérico que ten un requisito de recursos da lista e logo seleccione **Reservar**. Ou abra o requisito de recursos e logo seleccione **Reservar**.
3. Na páxina **Asistente de programación**, seleccione un recurso nomeado para reservar no seu equipo de proxecto e logo seleccione **Reservar**.

Cando a reserva está completa e cumprida por un recurso nomeado, o recurso xenérico substitúese polo recurso nomeado.

As asignacións do programa actualízanse co recurso nomeado tamén.

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a>Cumprir un recurso xenérico con varios recursos nomeados
Cumprir un requisito para un recurso xenérico con varios recursos nomeados é similar a asignar un único recurso nomeado. Por exemplo, hai unha tarefa cunha duración de cinco días e 120 horas de esforzo. Esta tarefa non se pode completar cun recurso que traballa un día típico de oito horas durante unha semana de cinco días. 

O requisito é de 120 horas de enxeñería robótica durante cinco días, é dicir, 24 horas ao día.

Este é un exemplo de cando se necesitan varios recursos nomeados para cumprir unha solicitude de recursos xenéricos. Deberá reservar varios recursos para cumprir o requisito.

A principal diferenza neste escenario é que o recurso xenérico permanece no equipo asignado á tarefa e os membros do equipo de recursos nomeados reservados non se asignan como parte do posto. O xestor do proxecto pode atribuír o traballo segundo corresponda aos recursos nomeados. A vista **Reconciliación** pode axudar a un xestor de proxectos a dividir as reservas entre varios recursos para a asignación de tarefas. Isto non se fai de xeito automático porque en calquera escenario máis complicado que o simple exemplo anterior, como cando hai un paquete de tarefas que conforman o requisito ou a intención de como o xestor de proxectos quere atribuír debe ser asumida polo sistema. Debido a que o sistema non pode entender a intención, é probable que as suposicións sexan diferentes do previsto e se produza un resultado incorrecto ou imprevisible. O resultado previsible é que o recurso xenérico permaneza asignado ata que o responsable do proxecto cree asignacións deliberadamente, coa asistencia da vista **Reconciliación**.


