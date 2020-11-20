---
title: Por que non podo eliminar rexistros da entidade datos reais?
description: Este tema fornece información sobre por que non pode eliminar rexistros da entidade datos reais.
author: JPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/6/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: b9b45e3ae0cd9273af4d2a5cd9cce30502c0aa78
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127156"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a><span data-ttu-id="c70b7-103">Por que non podo eliminar rexistros da entidade Datos reais?</span><span class="sxs-lookup"><span data-stu-id="c70b7-103">Why can’t I delete records from the Actuals entity?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="c70b7-104">Project Service Automation (PSA) non lle permite eliminar os datos reais porque serven como fonte de verdade para transaccións que teñen implicacións financeiras para os sistemas descendentes, como o libro de contabilidade xeral.</span><span class="sxs-lookup"><span data-stu-id="c70b7-104">Project Service Automation (PSA) doesn't allow you to delete actuals because they serve as the source of truth for transactions that have financial implications to downstream systems, such as the general ledger.</span></span> <span data-ttu-id="c70b7-105">Se se puidesen eliminar os datos reais, poderíase poñer en cuestión a integridade das transaccións dos informes financeiros.</span><span class="sxs-lookup"><span data-stu-id="c70b7-105">If actuals could be deleted, the integrity of the financial reporting transactions could be questioned.</span></span> <span data-ttu-id="c70b7-106">Para establecer un rexistro de auditoría, os clientes deberán usar diarios para crear transaccións compensatorias.</span><span class="sxs-lookup"><span data-stu-id="c70b7-106">To establish an audit trail, customers should use journals to create compensating transactions.</span></span>

