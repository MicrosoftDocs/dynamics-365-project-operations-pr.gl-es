---
title: Por que non podo eliminar rexistros da entidade datos reais?
description: Este artigo ofrece información sobre por que non podes eliminar rexistros da entidade reais.
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
ms.reviewer: johnmichalak
ms.openlocfilehash: bd446961432a8f18895db45699d7a731d55235b5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925578"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a>Por que non podo eliminar rexistros da entidade Datos reais?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Project Service Automation (PSA) non lle permite eliminar os datos reais porque serven como fonte de verdade para transaccións que teñen implicacións financeiras para os sistemas descendentes, como o libro de contabilidade xeral. Se se puidesen eliminar os datos reais, poderíase poñer en cuestión a integridade das transaccións dos informes financeiros. Para establecer un rexistro de auditoría, os clientes deberán usar diarios para crear transaccións compensatorias.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
