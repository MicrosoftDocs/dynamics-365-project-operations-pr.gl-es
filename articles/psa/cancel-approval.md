---
title: Cancelar as entradas de tempo e gasto aprobadas previamente
description: Este tema fornece información sobre como cancelar unha transacción de tempo e gasto de proxecto aprobada.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: bf3d146d2b07723b4d2e6e85eafd6f1b23b8b83f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014744"
---
# <a name="cancel-previously-approved-time-or-expense-entries"></a><span data-ttu-id="05b29-103">Cancelar as entradas de tempo ou gasto aprobadas previamente</span><span class="sxs-lookup"><span data-stu-id="05b29-103">Cancel previously approved time or expense entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="05b29-104">Na última versión de Dynamics 365 Project Service Automation, os responsables de aprobacións poden cancelar as entradas de tempo ou gasto que aprobaron previamente.</span><span class="sxs-lookup"><span data-stu-id="05b29-104">In the latest version of Dynamics 365 Project Service Automation, approvers can cancel time or expense entries that they previously approved.</span></span>

## <a name="cancel-a-previously-approved-time-or-expense-entry"></a><span data-ttu-id="05b29-105">Cancelar una entrada de tempo ou gasto aprobada previamente</span><span class="sxs-lookup"><span data-stu-id="05b29-105">Cancel a previously approved time or expense entry</span></span>

<span data-ttu-id="05b29-106">Siga estes pasos para cancelar unha entrada de tempo ou gasto que aprobou anteriormente.</span><span class="sxs-lookup"><span data-stu-id="05b29-106">Follow these steps to cancel a time or expense entry that you previously approved.</span></span>

1. <span data-ttu-id="05b29-107">Vaia a **Proxectos** \> **O meu traballo** \> **Aprobacións**.</span><span class="sxs-lookup"><span data-stu-id="05b29-107">Go to **Projects** \> **My Work** \> **Approvals**.</span></span>
2. <span data-ttu-id="05b29-108">Na páxina de lista **Aprobacións**, cambie a vista a **As miñas aprobacións pasadas**.</span><span class="sxs-lookup"><span data-stu-id="05b29-108">On the **Approvals** list page, change the view to **My past approvals**.</span></span> <span data-ttu-id="05b29-109">Móstrase unha lista das entradas de tempo e gasto que aprobou anteriormente.</span><span class="sxs-lookup"><span data-stu-id="05b29-109">A list of the time and expense entries that you previously approved is shown.</span></span>
3. <span data-ttu-id="05b29-110">Seleccione unha ou máis entradas e logo seleccione **Cancelar a aprobación**.</span><span class="sxs-lookup"><span data-stu-id="05b29-110">Select one or more entries, and then select **Cancel approval**.</span></span> <span data-ttu-id="05b29-111">Recibirá unha mensaxe de aviso.</span><span class="sxs-lookup"><span data-stu-id="05b29-111">You receive a warning message.</span></span>
4. <span data-ttu-id="05b29-112">Para cancelar a aprobación, seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="05b29-112">Select **OK** to cancel the approval.</span></span>

## <a name="understand-the-impact-of-canceling-a-time-or-expense-entry-approval"></a><span data-ttu-id="05b29-113">Comprender o impacto da cancelación dunha aprobación de entrada de tempo ou gasto</span><span class="sxs-lookup"><span data-stu-id="05b29-113">Understand the impact of canceling a time or expense entry approval</span></span>

<span data-ttu-id="05b29-114">Cando se cancela unha aprobación, hai un impacto operativo e financeiro.</span><span class="sxs-lookup"><span data-stu-id="05b29-114">When an approval is canceled, there is both operational impact and financial impact.</span></span>

### <a name="operational-impact"></a><span data-ttu-id="05b29-115">Impacto operativo</span><span class="sxs-lookup"><span data-stu-id="05b29-115">Operational impact</span></span>

<span data-ttu-id="05b29-116">No lado das operacións, cando se cancela unha aprobación, o estado do rexistro restablécese a **Borrador** e a aprobación xa non aparece na vista **As miñas aprobacións pasadas**.</span><span class="sxs-lookup"><span data-stu-id="05b29-116">On the operations side, when an approval is canceled, the status of the record is reset to **Draft**, and the approval no longer appears in the **My past approvals** view.</span></span> <span data-ttu-id="05b29-117">Pola contra, a aprobación cancelada aparece na vista **Entradas de tempo para aprobación** ou na vista **Entradas de gasto para aprobación**, dependendo de se era unha entrada de tempo ou unha entrada de gasto.</span><span class="sxs-lookup"><span data-stu-id="05b29-117">Instead, the canceled approval appears in either the **Time entries for approval** view or the **Expense entries for approval** view, depending on whether it was a time entry or an expense entry.</span></span> <span data-ttu-id="05b29-118">Ademais, o estado da entrada de tempo ou de gasto relacionada cambia a **Enviada** para que a entrada relacionada sexa coherente coas aprobacións que teñan un estado de **Borrador**.</span><span class="sxs-lookup"><span data-stu-id="05b29-118">Additionally, the status of the related time or expense entry is changed to **Submitted**, so that the related entry is consistent with approvals that have a status of **Draft**.</span></span>

<span data-ttu-id="05b29-119">Como responsable de aprobacións, pode editar algúns dos campos dunha aprobación que teña un estado de **Borrador**.</span><span class="sxs-lookup"><span data-stu-id="05b29-119">As an approver, you can edit some of the fields of an approval that has a status of **Draft**.</span></span> <span data-ttu-id="05b29-120">Estes campos inclúen **Tipo de facturación** e **Horas facturables para entradas de tempo**.</span><span class="sxs-lookup"><span data-stu-id="05b29-120">These fields include **Billing Type** and **Billable Hours for Time Entries**.</span></span> <span data-ttu-id="05b29-121">Despois de facer os cambios, pode aprobar o rexistro de novo.</span><span class="sxs-lookup"><span data-stu-id="05b29-121">After you make changes, you can approve the record again.</span></span> <span data-ttu-id="05b29-122">Alternativamente, pode rexeitar a entrada.</span><span class="sxs-lookup"><span data-stu-id="05b29-122">Alternatively, you can reject the entry.</span></span> <span data-ttu-id="05b29-123">Se rexeita a aprobación dunha entrada de tempo, o estado da entrada cambia a **Devolto**.</span><span class="sxs-lookup"><span data-stu-id="05b29-123">If you reject the approval of a time entry, the status of the entry is changed to **Returned**.</span></span> <span data-ttu-id="05b29-124">Se rexeita a aprobación dunha entrada de gasto, o estado da entrada cambia a **Rexeitado**.</span><span class="sxs-lookup"><span data-stu-id="05b29-124">If you reject the approval of an expense entry, the status is changed to **Rejected**.</span></span> <span data-ttu-id="05b29-125">Funcionalmente, as entradas devoltas e rexeitadas compórtanse igual que unha entrada co estado de **Borrador**.</span><span class="sxs-lookup"><span data-stu-id="05b29-125">Functionally, both returned and rejected entries behave the same as an entry that has a status of **Draft**.</span></span> <span data-ttu-id="05b29-126">Un membro do equipo do proxecto pode facer calquera cambio necesario na entrada e logo enviala de novo para a súa aprobación ou ben eliminar a entrada por completo.</span><span class="sxs-lookup"><span data-stu-id="05b29-126">A project team member can either make any required changes to the entry and then resubmit it for approval, or delete the entry entirely.</span></span>

### <a name="financial-impact"></a><span data-ttu-id="05b29-127">Impacto financeiro</span><span class="sxs-lookup"><span data-stu-id="05b29-127">Financial impact</span></span>

<span data-ttu-id="05b29-128">Un proxecto tamén se ve afectado financeiramente cando se cancela unha aprobación.</span><span class="sxs-lookup"><span data-stu-id="05b29-128">A project is also affected financially when an approval is canceled.</span></span> <span data-ttu-id="05b29-129">En primeiro lugar, os datos reais correspondentes de custo e vendas actualízanse do seguinte xeito:</span><span class="sxs-lookup"><span data-stu-id="05b29-129">First, the corresponding actuals for cost and sales are updated in the following manner:</span></span>

- <span data-ttu-id="05b29-130">O estado de axuste está definido en **Axustado**.</span><span class="sxs-lookup"><span data-stu-id="05b29-130">The adjustment status is set to **Adjusted**.</span></span>
- <span data-ttu-id="05b29-131">O estado de facturación está definido en **Cancelado**.</span><span class="sxs-lookup"><span data-stu-id="05b29-131">The billing status is set to **Canceled**.</span></span>

<span data-ttu-id="05b29-132">A continuación, créanse entradas de reversión na táboa de Datos reais.</span><span class="sxs-lookup"><span data-stu-id="05b29-132">Next, reversal entries are created in the Actuals table.</span></span> <span data-ttu-id="05b29-133">Para crear entradas de reversión, o sistema copia sobre os valores de campo a partir dos datos reais orixinais.</span><span class="sxs-lookup"><span data-stu-id="05b29-133">To create reversal entries, the system copies over the field values from the original actuals.</span></span> <span data-ttu-id="05b29-134">Os únicos valores que non se copian son os valores de cantidade.</span><span class="sxs-lookup"><span data-stu-id="05b29-134">The only values that aren't copied over are the quantity values.</span></span> <span data-ttu-id="05b29-135">Estes valores revértense.</span><span class="sxs-lookup"><span data-stu-id="05b29-135">These values are reversed instead.</span></span> <span data-ttu-id="05b29-136">Os datos reais revertidos créanse para **Custo** e **Vendas sen facturar**.</span><span class="sxs-lookup"><span data-stu-id="05b29-136">Reversed actuals are created for both **Cost** and **Unbilled Sales** actuals.</span></span> <span data-ttu-id="05b29-137">O campo **Estado de axuste** nos datos reais revertidos está definido en **Inaxustable** e o estado de facturación está definido en **Cancelado**.</span><span class="sxs-lookup"><span data-stu-id="05b29-137">The **Adjustment Status** field on the reversed actuals is set to **Unadjustable**, and the billing status is set to **Canceled**.</span></span>

<span data-ttu-id="05b29-138">Despois de realizar estes cambios, o importe que se rexistra como gastado no proxecto e os ingresos acumulados do proxecto contabilizarán as cantidades que representan estes datos reais.</span><span class="sxs-lookup"><span data-stu-id="05b29-138">After these changes are made, the amount that is recorded as spent on the project and the revenue backlog on the project will longer account for the amounts that these actuals represent.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]