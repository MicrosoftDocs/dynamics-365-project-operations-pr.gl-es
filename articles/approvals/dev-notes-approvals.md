---
title: Notas do programador para as aprobacións
description: Este tema ofrece información adicional para programadores sobre o traballo con aprobacións.
author: stsporen
manager: Annbe
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d58c776b0341c08b0292e1b459a7d7ebac550bcc
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290267"
---
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="78473-103">Notas do programador para as aprobacións</span><span class="sxs-lookup"><span data-stu-id="78473-103">Developer notes for Approvals</span></span>

<span data-ttu-id="78473-104">_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="78473-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="78473-105">Dynamics 365 Project Operations inclúe unha lóxica de validación que garante a transición correcta dos rexistros a través das etapas de aprobación.</span><span class="sxs-lookup"><span data-stu-id="78473-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="78473-106">As transicións correctas de rexistros garanten:</span><span class="sxs-lookup"><span data-stu-id="78473-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="78473-107">Todas as filas de apoio créanse en táboas relacionadas, como diarios e datos reais.</span><span class="sxs-lookup"><span data-stu-id="78473-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="78473-108">O responsable de aprobación está marcado como **Responsable de aprobación de proxecto** no proxecto antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="78473-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]