---
title: Por que non podo eliminar rexistros da entidade datos reais?
description: Este tema fornece información sobre por que non pode eliminar rexistros da entidade datos reais.
author: JPBurrows
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
ms.openlocfilehash: 434be93cedb4772616b1e6d5cbe15fc715eed19a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993099"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a><span data-ttu-id="57259-103">Por que non podo eliminar rexistros da entidade Datos reais?</span><span class="sxs-lookup"><span data-stu-id="57259-103">Why can’t I delete records from the Actuals entity?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="57259-104">Project Service Automation (PSA) non lle permite eliminar os datos reais porque serven como fonte de verdade para transaccións que teñen implicacións financeiras para os sistemas descendentes, como o libro de contabilidade xeral.</span><span class="sxs-lookup"><span data-stu-id="57259-104">Project Service Automation (PSA) doesn't allow you to delete actuals because they serve as the source of truth for transactions that have financial implications to downstream systems, such as the general ledger.</span></span> <span data-ttu-id="57259-105">Se se puidesen eliminar os datos reais, poderíase poñer en cuestión a integridade das transaccións dos informes financeiros.</span><span class="sxs-lookup"><span data-stu-id="57259-105">If actuals could be deleted, the integrity of the financial reporting transactions could be questioned.</span></span> <span data-ttu-id="57259-106">Para establecer un rexistro de auditoría, os clientes deberán usar diarios para crear transaccións compensatorias.</span><span class="sxs-lookup"><span data-stu-id="57259-106">To establish an audit trail, customers should use journals to create compensating transactions.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]