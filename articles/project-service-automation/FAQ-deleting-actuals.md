---
title: Por que non podo eliminar rexistros da entidade datos reais?
description: Este tema fornece información sobre por que non pode eliminar rexistros da entidade datos reais.
author: JPBurrows
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 11/6/2018
ms.topic: article
ms.prod: Project Service
ms.technology: Applies to all versions of Project Service
ms.assetid: ff504c34-7337-474f-89e8-d8afdd1e0a98
ms.author: Jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 5817940933c161dccac0fe549fabacbe57e7077a
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751339"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a>Por que non podo eliminar rexistros da entidade Datos reais?

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Project Service Automation (PSA) non lle permite eliminar os datos reais porque serven como fonte de verdade para transaccións que teñen implicacións financeiras para os sistemas descendentes, como o libro de contabilidade xeral. Se se puidesen eliminar os datos reais, poderíase poñer en cuestión a integridade das transaccións dos informes financeiros. Para establecer un rexistro de auditoría, os clientes deberán usar diarios para crear transaccións compensatorias.

