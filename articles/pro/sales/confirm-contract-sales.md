---
title: Confirmar un contrato de proxecto
description: Este tema ofrece información sobre como confirmar un contrato en Project Operations.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b5eabcad028a8282f552f3571b170d9b933a7b88
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003674"
---
# <a name="confirm-a-project-contract"></a><span data-ttu-id="1b67e-103">Confirmar un contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="1b67e-103">Confirm a project contract</span></span>

<span data-ttu-id="1b67e-104">_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="1b67e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1b67e-105">Un contrato de proxecto en Dynamics 365 Project Operations pode estar activo cun motivo de **Confirmado** ou pechado cun motivo de **Perdido**.</span><span class="sxs-lookup"><span data-stu-id="1b67e-105">A project contract in Dynamics 365 Project Operations can be active with a reason of **Confirmed**, or closed with a reason of **Lost**.</span></span> <span data-ttu-id="1b67e-106">Cando confirme un contrato de proxecto, o estado actualízase de **Borrador** a **Activo** e o motivo para o estado é **Confirmado**.</span><span class="sxs-lookup"><span data-stu-id="1b67e-106">When you confirm a project contract, the status updates from **Draft** to **Active** and the status reason is **Confirmed**.</span></span> <span data-ttu-id="1b67e-107">Non se pode editar nin reabrir un contrato activo ou pechado.</span><span class="sxs-lookup"><span data-stu-id="1b67e-107">An active or closed contract can't be edited or reopened.</span></span> 

### <a name="financial-impact-of-confirming-a-project-contract"></a><span data-ttu-id="1b67e-108">Impacto financeiro da confirmación dun contrato de proxecto</span><span class="sxs-lookup"><span data-stu-id="1b67e-108">Financial impact of confirming a project contract</span></span>

<span data-ttu-id="1b67e-109">Despois de confirmar un contrato de proxecto, a aplicación calculará de novo os custos revertendo os datos reais de custos máis antigos e creando novos datos reais de custos.</span><span class="sxs-lookup"><span data-stu-id="1b67e-109">After a project contract is confirmed, the application recalculates the costs by reversing the older cost actuals and creating new cost actuals.</span></span> <span data-ttu-id="1b67e-110">Despois os novos datos reais de custos se procesan en función do método de facturación da liña de contrato do proxecto asociado.</span><span class="sxs-lookup"><span data-stu-id="1b67e-110">The new cost actuals are then processed based on the billing method of the associated project contract line.</span></span> <span data-ttu-id="1b67e-111">Se os datos reais de custos fan referencia a unha liña de contrato de tempo e material, a aplicación recrea automaticamente os datos reais de vendas non facturados correspondentes.</span><span class="sxs-lookup"><span data-stu-id="1b67e-111">If the cost actuals reference a Time and Material contract line, the application automatically re-creates corresponding unbilled sales actuals.</span></span> <span data-ttu-id="1b67e-112">Se os datos reais de custos fan referencia a unha liña de contrato de prezo fixo, a aplicación deixa de reprocesar os datos reais de custos.</span><span class="sxs-lookup"><span data-stu-id="1b67e-112">If the cost actuals reference a Fixed Price contract line, the application stops reprocessing the cost actuals.</span></span>

<span data-ttu-id="1b67e-113">Os límites non superables, a configuración de imputabilidade e os prezos e custos dos datos reais avalíanse e actualízanse como parte do proceso de confirmación.</span><span class="sxs-lookup"><span data-stu-id="1b67e-113">Not-to-exceed limits, chargeability setup, and pricing and costing on the actuals is evaluated and then updated as part of the confirmations process.</span></span>

## <a name="close-a-project-contract-as-lost"></a><span data-ttu-id="1b67e-114">Pechar un contrato de proxecto como perdido</span><span class="sxs-lookup"><span data-stu-id="1b67e-114">Close a project contract as lost</span></span>

<span data-ttu-id="1b67e-115">Cando pecha un contrato de proxecto como perdido, o estado do contrato actualízase a **Pechado** e o motivo para o estado é **Perdido**.</span><span class="sxs-lookup"><span data-stu-id="1b67e-115">When you close a project contract as lost, the contract status is updated to **Closed** and the status reason is **Lost**.</span></span> <span data-ttu-id="1b67e-116">O contrato de proxecto pasa a ser de só lectura.</span><span class="sxs-lookup"><span data-stu-id="1b67e-116">The project contract becomes read-only.</span></span> <span data-ttu-id="1b67e-117">Ofrécese un diálogo de confirmación antes de completar os cambios porque non pode volver abrir un contrato de proxecto pechado.</span><span class="sxs-lookup"><span data-stu-id="1b67e-117">A confirmation dialog is provided before the changes are complete because you can't reopen a closed project contract.</span></span>

<span data-ttu-id="1b67e-118">Se o contrato de proxecto pechado como perdido fai referencia a un proxecto nas súas liñas, ese proxecto tamén se marcará como pechado.</span><span class="sxs-lookup"><span data-stu-id="1b67e-118">If the project contract that is closed as lost references a project on its lines, that project is also marked as closed.</span></span> <span data-ttu-id="1b67e-119">Cancélanse as reservas de recursos a partir dese día.</span><span class="sxs-lookup"><span data-stu-id="1b67e-119">Any resource bookings from that day forward are canceled.</span></span> <span data-ttu-id="1b67e-120">Os datos reais de vendas non facturadas do contrato de proxecto que aínda non figuren nunha factura reverteranse.</span><span class="sxs-lookup"><span data-stu-id="1b67e-120">Any unbilled sales actuals on the project contract that aren't already on an invoice, will be reversed.</span></span>

> [!NOTE]
> <span data-ttu-id="1b67e-121">En Dynamics 365 Project Operations, pechar un contrato de proxecto como perdido non repercutirá nese estado da oportunidade asociada.</span><span class="sxs-lookup"><span data-stu-id="1b67e-121">In Dynamics 365 Project Operations, closing a project contract as lost will not impact that status of the associated opportunity.</span></span> <span data-ttu-id="1b67e-122">A oportunidade permanecerá aberta e debe pecharse manualmente.</span><span class="sxs-lookup"><span data-stu-id="1b67e-122">The opportunity will remain open and must be manually closed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]