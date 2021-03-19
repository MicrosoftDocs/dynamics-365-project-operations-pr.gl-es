---
title: Crear unha factura proforma manual - lite
description: Este tema ofrece información sobre a creación dunha factura proforma manual en Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 104c2f3f7f0ca0682158d0f7fa0f50a4967e6dd0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274186"
---
# <a name="create-a-manual-proforma-invoice---lite"></a><span data-ttu-id="b0320-103">Crear unha factura proforma manual - lite</span><span class="sxs-lookup"><span data-stu-id="b0320-103">Create a manual proforma invoice - lite</span></span>

<span data-ttu-id="b0320-104">_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="b0320-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b0320-105">En Dynamics 365 Project Operations, as facturas proforma pódense crear manualmente segundo sexa necesario.</span><span class="sxs-lookup"><span data-stu-id="b0320-105">In Dynamics 365 Project Operations, proforma invoices can be created manually as needed.</span></span> <span data-ttu-id="b0320-106">Pode crear manualmente unha factura proforma desde a páxina de lista **Contratos de proxectos** ou desde a páxina de detalles **Contrato do proxecto**.</span><span class="sxs-lookup"><span data-stu-id="b0320-106">You can manually create a proforma invoice from the **Project Contracts** list page or from the **Project Contract** details page.</span></span>

##  <a name="project-contracts-list-page"></a><span data-ttu-id="b0320-107">Páxina de lista Contratos de proxectos</span><span class="sxs-lookup"><span data-stu-id="b0320-107">Project Contracts list page</span></span>

<span data-ttu-id="b0320-108">Desde a páxina de lista **Contratos de proxectos**, seleccione un ou máis contratos de proxectos e cree facturas para todos os rexistros seleccionados.</span><span class="sxs-lookup"><span data-stu-id="b0320-108">From **Project Contracts** list page, select one or more project contracts, and create invoices for all of the selected records.</span></span>

<span data-ttu-id="b0320-109">O sistema comproba para ver cal dos contratos do proxecto seleccionado ten un traballo pendente **Listo para facturar** con data anterior á data de hoxe.</span><span class="sxs-lookup"><span data-stu-id="b0320-109">The system checks to see which of the selected project contracts has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="b0320-110">A partir deses contratos, o sistema crea borradores de facturas proforma.</span><span class="sxs-lookup"><span data-stu-id="b0320-110">From those contracts, the system creates draft proforma invoices.</span></span> <span data-ttu-id="b0320-111">Se un contrato de proxecto ten varios clientes, pode haber unha factura creada por cliente e varias facturas por contrato de proxecto.</span><span class="sxs-lookup"><span data-stu-id="b0320-111">If a project contract has multiple customers, there may be one invoice created per customer, and multiple invoices per project contract.</span></span>

<span data-ttu-id="b0320-112">Todas as facturas do proxecto creado están dispoñibles na páxina **Factura** na sección **Facturación** da área **Vendas**.</span><span class="sxs-lookup"><span data-stu-id="b0320-112">All of the created project invoices are available on the **Invoice** page in the **Billing** section of the **Sales** area.</span></span>

## <a name="project-contract-details-page"></a><span data-ttu-id="b0320-113">Páxina de detalles de Contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="b0320-113">Project Contract details page</span></span>

<span data-ttu-id="b0320-114">Tamén se pode crear unha factura proforma desde a páxina de detalles **Contrato do proxecto**.</span><span class="sxs-lookup"><span data-stu-id="b0320-114">A proforma invoice can also be created from the **Project Contract** details page.</span></span> <span data-ttu-id="b0320-115">O sistema verifica que o contrato do proxecto seleccionado ten un traballo pendente **Listo para facturar** con data anterior á data de hoxe.</span><span class="sxs-lookup"><span data-stu-id="b0320-115">The system verifies the project contract has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="b0320-116">A partir destes contratos, o sistema crea borradores de facturas proforma en función do número de clientes en cada liña de contrato.</span><span class="sxs-lookup"><span data-stu-id="b0320-116">From these contracts, the system creates draft proforma invoices based on the number of customers on each contract line.</span></span>

<span data-ttu-id="b0320-117">Cando se crea unha única factura proforma, ábrese a páxina **Factura**.</span><span class="sxs-lookup"><span data-stu-id="b0320-117">When there's a single proforma invoice created, the **Invoice** page opens.</span></span> <span data-ttu-id="b0320-118">Se se crean varias facturas para ese contrato de proxecto, a páxina de lista **Facturas** ábrese para amosar todas as facturas creadas.</span><span class="sxs-lookup"><span data-stu-id="b0320-118">If multiple invoices are created for that project contract, the **Invoices** list page opens to show all of the created invoices.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]