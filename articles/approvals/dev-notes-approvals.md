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
ms.openlocfilehash: 9e4e910d0ff0a5f2603148fcc5daa0d423a4d174
ms.sourcegitcommit: a9dbcd3aff4c6ae495412e4980e105ae160fd1ec
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 11/10/2020
ms.locfileid: "4483946"
---
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="e45a9-103">Notas do programador para as aprobacións</span><span class="sxs-lookup"><span data-stu-id="e45a9-103">Developer notes for Approvals</span></span>

<span data-ttu-id="e45a9-104">_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="e45a9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e45a9-105">Dynamics 365 Project Operations inclúe unha lóxica de validación que garante a transición correcta dos rexistros a través das etapas de aprobación.</span><span class="sxs-lookup"><span data-stu-id="e45a9-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="e45a9-106">As transicións correctas de rexistros garanten:</span><span class="sxs-lookup"><span data-stu-id="e45a9-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="e45a9-107">Todas as filas de apoio créanse en táboas relacionadas, como diarios e datos reais.</span><span class="sxs-lookup"><span data-stu-id="e45a9-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="e45a9-108">O responsable de aprobación está marcado como **Responsable de aprobación de proxecto** no proxecto antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="e45a9-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>
