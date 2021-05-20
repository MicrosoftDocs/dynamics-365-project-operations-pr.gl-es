---
title: Integración de escrita dual de Project Operations
description: Este tema ofrece unha visión xeral da integración da escrita dual de Project Operations.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d9d6a7c367872219b4aca32aecb15d6837ebe296
ms.sourcegitcommit: 02f00960198cc78a5e96955a9e4390c2c6393bbf
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "5955656"
---
# <a name="project-operations-dual-write-integration-overview"></a><span data-ttu-id="dd715-103">Visión xeral da integración de escrita dual de Project Operations</span><span class="sxs-lookup"><span data-stu-id="dd715-103">Project Operations dual-write integration overview</span></span>

<span data-ttu-id="dd715-104">_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_</span><span class="sxs-lookup"><span data-stu-id="dd715-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="dd715-105">Project Operations usa as [capacidades de escrita dual](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) para sincronizar datos entre Microsoft Dataverse e Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="dd715-105">Project Operations uses [dual-write capabilities](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) to synchronize data across Microsoft Dataverse and Dynamics 365 Finance.</span></span>

<span data-ttu-id="dd715-106">A seguinte ilustración mostra como se sincronizan os datos como parte desta integración entre Dataverse e Finance.</span><span class="sxs-lookup"><span data-stu-id="dd715-106">The following illustration shows how data is synchronized as part of this integration between Dataverse and Finance.</span></span>

![Visión xeral dos fluxos de datos de Project Operations](./media/ProjectOperationsFlows.jpg)

<span data-ttu-id="dd715-108">Project Operations en Dataverse ofrece unha interface de usuario moderna (IU) e unha fácil extensibilidade sen código/de código baixo utilizando as capacidades de Power Platform.</span><span class="sxs-lookup"><span data-stu-id="dd715-108">Project Operations on Dataverse provides a modern user interface (UI) and easy no-code/low-code extensibility using Power Platform capabilities.</span></span> <span data-ttu-id="dd715-109">Xestores de proxectos, xestores de recursos, membros do equipo do proxecto e outras persoas de atención ao cliente realizan as súas actividades en Project Operations en Dataverse.</span><span class="sxs-lookup"><span data-stu-id="dd715-109">Project managers, Resource managers, Project team members, and other front-office personas, perform their activities in Project Operations on Dataverse.</span></span>

<span data-ttu-id="dd715-110">Project Operations en Finance ofrece asistencia para recoñecemento de ingresos e contabilidade de proxectos.</span><span class="sxs-lookup"><span data-stu-id="dd715-110">Project Operations in Finance provides project accounting and revenue recognition support.</span></span> <span data-ttu-id="dd715-111">Project Operations conéctase ao marco financeiro de Finance para o cálculo do imposto sobre as vendas, as taxas de cambio de divisas, a información de dimensións financeiras e moito máis.</span><span class="sxs-lookup"><span data-stu-id="dd715-111">Project Operations plugs in to the financial framework in Finance for sales tax calculation, currency exchange rates, financial dimension reporting, and more.</span></span> <span data-ttu-id="dd715-112">As experiencias do contable do proxecto baséanse principalmente en Finance.</span><span class="sxs-lookup"><span data-stu-id="dd715-112">The Project accountant experiences are mostly based in Finance.</span></span>

<span data-ttu-id="dd715-113">A integración de Project Operations consiste na seguinte integración de compoñentes:</span><span class="sxs-lookup"><span data-stu-id="dd715-113">Project Operations integration consists of the following component integration:</span></span>


- [<span data-ttu-id="dd715-114">Integración de datos de instalación e configuración de Project Operations</span><span class="sxs-lookup"><span data-stu-id="dd715-114">Project Operations setup and configuration data integration</span></span>](resource-dual-write-setup-integration.md) 
- [<span data-ttu-id="dd715-115">Estimacións e datos reais do proxecto</span><span class="sxs-lookup"><span data-stu-id="dd715-115">Project estimates and actuals</span></span>](resource-dual-write-estimates-actuals.md)
- [<span data-ttu-id="dd715-116">Facturas do proxecto</span><span class="sxs-lookup"><span data-stu-id="dd715-116">Project invoices</span></span>](resource-dual-write-project-invoice.md)
- [<span data-ttu-id="dd715-117">Xestión de gastos</span><span class="sxs-lookup"><span data-stu-id="dd715-117">Expense management</span></span>](resource-dual-write-expense.md)
- [<span data-ttu-id="dd715-118">Factura do fornecedor</span><span class="sxs-lookup"><span data-stu-id="dd715-118">Vendor invoice</span></span>](resource-dual-write-vendor-invoice.md)
