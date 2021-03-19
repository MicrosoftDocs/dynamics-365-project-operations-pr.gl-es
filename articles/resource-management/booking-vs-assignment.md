---
title: Reservas fronte a atribucións
description: Este tema ofrece información sobre as diferenzas entre as reservas de recursos e as atribucións de recursos.
author: ruhercul
manager: Annbe
ms.date: 01/08/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3aaf8dcbae0a5762879c2b1223eba3bdc33af1a7
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279901"
---
# <a name="bookings-vs-assignments"></a>Reservas fronte a atribucións

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

As reservas son a atribución branda o dura de recursos a un proxecto. As reservas duras consumen a capacidade dun recurso. As reservas representan conceptos organizativos para os equipos para que poidan comprender como se utilizarán os recursos en varios proxectos. Dynamics 365 Project Operations considera que as reservas son un concepto a nivel de proxecto. 

A diferenza das reservas, as atribucións son o compromiso de recursos para as tarefas do proxecto na programación do proxecto. Os recursos poden ser nomeados ou xenéricos.  Cando se deriva un requisito de recurso das atribucións de tarefas do proxecto, Project Operations utiliza os contornos de esforzo da atribución de recursos para construír os contornos dos detalles do requisito de recurso. Non obstante, non se mantén a referencia ás atribucións de recursos. As actualizacións das reservas derivadas do requisito de recurso non actualizan ningunha atribución de recurso.

Normalmente, a suma das reservas dun recurso igualará a suma das atribucións do recurso nunha ou varias tarefas. Non obstante, Project Operations non fai cumprir este acordo. A vista **Conciliación** mostra ao xestor de proxectos lugares onde as reservas e atribucións dun recurso non coinciden.




[!INCLUDE[footer-include](../includes/footer-banner.md)]