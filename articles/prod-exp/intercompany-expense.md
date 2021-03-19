---
title: Gastos entre empresas
description: Este tema ofrece información sobre como usar os gastos entre empresas para atribuír os gastos dun traballador á entidade legal para a que se realizou o traballo.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d908a1c062f5b7f01cf340dcd6f7f24714a992bf
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271531"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="ccafa-103">Gastos entre empresas</span><span class="sxs-lookup"><span data-stu-id="ccafa-103">Intercompany expenses</span></span>

<span data-ttu-id="ccafa-104">Un traballador empregado por unha entidade legal nunha organización pode realizar traballos para outra entidade legal da mesma organización.</span><span class="sxs-lookup"><span data-stu-id="ccafa-104">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="ccafa-105">Pode usar os gastos entre empresas para atribuír os gastos do traballador á entidade legal para a que se realizou o traballo.</span><span class="sxs-lookup"><span data-stu-id="ccafa-105">You can use intercompany expenses to assign the worker’s expenses to the legal entity for which the  work was performed.</span></span> <span data-ttu-id="ccafa-106">A entidade legal que emprega ao traballador denomínase entidade legal prestamista.</span><span class="sxs-lookup"><span data-stu-id="ccafa-106">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="ccafa-107">A entidade legal pola que o traballador incorre en gastos chámase entidade xurídica prestameira.</span><span class="sxs-lookup"><span data-stu-id="ccafa-107">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="ccafa-108">Antes de que un traballador poida crear e enviar gastos entre empresas, ten que activar as liñas de gastos entre empresas.</span><span class="sxs-lookup"><span data-stu-id="ccafa-108">Before a worker can create and submit intercompany expenses, you must enable intercompany expense lines.</span></span> <span data-ttu-id="ccafa-109">Na entidade legal prestamista, na páxina **Parámetros de xestión de gastos**, seleccione **Permitir liñas de gasto entre empresas**.</span><span class="sxs-lookup"><span data-stu-id="ccafa-109">In the loaning legal entity, on the **Expense management parameters** page, select **Allow intercompany expense lines**.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="ccafa-110">Contabilización de impostos por gastos entre empresas</span><span class="sxs-lookup"><span data-stu-id="ccafa-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ccafa-111">Antes de poder empregar no seu informe de gastos os grupos fiscais asociados á entidade legal prestamista (orixe) en lugar da entidade legal prestameira (destino), debe activar a funcionalidade na configuración do imposto sobre as vendas do libro maior.</span><span class="sxs-lookup"><span data-stu-id="ccafa-111">Before you can use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you must enable the functionality in the General ledger sales tax setup.</span></span> <span data-ttu-id="ccafa-112">Cando o parámetro **Entidade legal para a contabilización de impostos entre empresas** está definido como **Orixe** e **Aplicar regras de tributación do imposto sobre as vendas** está fixado en **Non**, úsase a combinación de impostos para a entidade legal prestamista.</span><span class="sxs-lookup"><span data-stu-id="ccafa-112">When the **Legal entity for intercompany tax posting** parameter is set to **Source** and **Apply sales tax taxation rules** is set to **No**, the tax combination for the loaning legal entity is used.</span></span> <span data-ttu-id="ccafa-113">Cando o mesmo parámetro está configurado en **Destino**, utilizarase a combinación fiscal para a entidade legal prestameira.</span><span class="sxs-lookup"><span data-stu-id="ccafa-113">When the same parameter is set to **Destination**, the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="ccafa-114">Para as entidades legais dos Estados Unidos, cando o parámetro está establecido en **Orixe**, o campo **Imposto sobre as vendas pendente de cobro** tamén debe configurarse na nova páxina **Grupos de contabilización de libro maior**.</span><span class="sxs-lookup"><span data-stu-id="ccafa-114">For legal entities in the United States, when the parameter is set to **Source**, the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="ccafa-115">O motor de contabilidade utilizará a información deste campo para a entrada contable relacionada cos impostos.</span><span class="sxs-lookup"><span data-stu-id="ccafa-115">The accounting engine will use the information from this field for tax-related accounting entry.</span></span>   
<span data-ttu-id="ccafa-116">O comportamento é coherente para as liñas de gastos contabilizadas con ou sen proxecto.</span><span class="sxs-lookup"><span data-stu-id="ccafa-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  


[!INCLUDE[footer-include](../includes/footer-banner.md)]