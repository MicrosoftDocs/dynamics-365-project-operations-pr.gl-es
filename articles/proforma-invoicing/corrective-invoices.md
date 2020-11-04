---
title: Facturas corrixidas
description: Este tema fornece información sobre facturas corrixidas.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: b31e702cc15bbb3937e8c4b305064212f63ce919
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076300"
---
# <a name="corrected-invoices"></a><span data-ttu-id="ae316-103">Facturas corrixidas</span><span class="sxs-lookup"><span data-stu-id="ae316-103">Corrected invoices</span></span>

<span data-ttu-id="ae316-104">_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_</span><span class="sxs-lookup"><span data-stu-id="ae316-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="ae316-105">Pódense editar as facturas confirmadas.</span><span class="sxs-lookup"><span data-stu-id="ae316-105">Confirmed invoices can be edited.</span></span> <span data-ttu-id="ae316-106">Cando edite unha factura confirmada, créase un novo borrador de factura corrixida.</span><span class="sxs-lookup"><span data-stu-id="ae316-106">When you edit a confirmed invoice, a draft of the corrected invoice is created.</span></span> <span data-ttu-id="ae316-107">Dado que se supón que desexa reverter todas as transaccións e cantidades da factura orixinal, a factura corrixida inclúe todas as transaccións da factura orixinal e todas as cantidades que hai en ela son cero (0).</span><span class="sxs-lookup"><span data-stu-id="ae316-107">Because the assumption is that you want to reverse all the transactions and quantities from the original invoice, the corrected invoice includes all the transactions from the original invoice, and all the quantities on it are zero (0).</span></span>

<span data-ttu-id="ae316-108">Cando as transaccións non requiren corrección, pode eliminalas do borrador da factura correctora.</span><span class="sxs-lookup"><span data-stu-id="ae316-108">When transactions don't require correction, you can remove them from the draft corrective invoice.</span></span> <span data-ttu-id="ae316-109">Para inverter ou devolver só unha cantidade parcial, pode editar o campo Cantidade no detalle da liña.</span><span class="sxs-lookup"><span data-stu-id="ae316-109">To reverse or return only a partial quantity, you can edit the Quantity field on the line detail.</span></span> <span data-ttu-id="ae316-110">Se abre o detalle da liña de factura, pode ver a cantidade orixinal da factura.</span><span class="sxs-lookup"><span data-stu-id="ae316-110">If you open the invoice line detail, you can see the original invoice quantity.</span></span> <span data-ttu-id="ae316-111">Pode editar a cantidade da factura actual de xeito que sexa inferior ou superior á cantidade da factura orixinal.</span><span class="sxs-lookup"><span data-stu-id="ae316-111">You can then edit the current invoice quantity so that it's less than or more than the original invoice quantity.</span></span>

<span data-ttu-id="ae316-112">Cando se confirma unha factura correctora, invértese o datos real de vendas facturadas orixinais, e créase un novo dato real de vendas facturadas.</span><span class="sxs-lookup"><span data-stu-id="ae316-112">When you confirm a corrective invoice, the original billed sales actual is reversed, and a new billed sales actual is created.</span></span> <span data-ttu-id="ae316-113">Se a cantidade foi reducida, a diferenza fará que tamén se cree un novo dato real de vendas sen facturar.</span><span class="sxs-lookup"><span data-stu-id="ae316-113">If the quantity was reduced, the difference will cause a new unbilled sales actual to be created too.</span></span> <span data-ttu-id="ae316-114">Por exemplo, se a vendas orixinal facturada foi de oito horas e o detalle da liña de factura corrixida ten unha cantidade reducida de seis horas, a liña de vendas facturadas orixinal invértese e créanse dous novos datos reais:</span><span class="sxs-lookup"><span data-stu-id="ae316-114">For example, if the original billed sale was for eight hours, and the corrected invoice line detail has a reduced quantity of six hours, the original billed sales line is revered and two new actuals are created:</span></span>

- <span data-ttu-id="ae316-115">Un dato real de vendas facturadas de seis horas.</span><span class="sxs-lookup"><span data-stu-id="ae316-115">A billed sales actual for six hours.</span></span>
- <span data-ttu-id="ae316-116">Un dato real de vendas sen facturar das dúas horas restantes.</span><span class="sxs-lookup"><span data-stu-id="ae316-116">An unbilled sales actual for the remaining two hours.</span></span> <span data-ttu-id="ae316-117">Esta transacción pódese facturar posteriormente ou marcarse como non imputable, dependendo das negociacións co cliente.</span><span class="sxs-lookup"><span data-stu-id="ae316-117">This transaction can either be billed later or marked as non-chargeable, depending on the negotiations with the customer.</span></span>
