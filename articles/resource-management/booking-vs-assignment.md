---
title: Reservas fronte a atribucións
description: Este tema ofrece información sobre as diferenzas entre as reservas de recursos e as atribucións de recursos.
author: ruhercul
ms.date: 01/08/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: b06555ec48e50f88c11872336539ca88c5cef34a
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591264"
---
# <a name="bookings-vs-assignments"></a>Reservas fronte a atribucións

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

As reservas son a atribución branda o dura de recursos a un proxecto. As reservas duras consumen a capacidade dun recurso. As reservas representan conceptos organizativos para os equipos para que poidan comprender como se utilizarán os recursos en varios proxectos. Dynamics 365 Project Operations considera que as reservas son un concepto a nivel de proxecto. 

A diferenza das reservas, as atribucións son o compromiso de recursos para as tarefas do proxecto na programación do proxecto. Os recursos poden ser nomeados ou xenéricos.  Cando se deriva un requisito de recurso das atribucións de tarefas do proxecto, Project Operations utiliza os contornos de esforzo da atribución de recursos para construír os contornos dos detalles do requisito de recurso. Non obstante, non se mantén a referencia ás atribucións de recursos. As actualizacións das reservas derivadas do requisito de recurso non actualizan ningunha atribución de recurso.

Normalmente, a suma das reservas dun recurso igualará a suma das atribucións do recurso nunha ou varias tarefas. Non obstante, Project Operations non fai cumprir este acordo. A vista **Conciliación** mostra ao xestor de proxectos lugares onde as reservas e atribucións dun recurso non coinciden.




[!INCLUDE[footer-include](../includes/footer-banner.md)]