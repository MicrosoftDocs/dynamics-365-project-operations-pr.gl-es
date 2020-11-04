---
title: Gastos entre empresas
description: Un traballador empregado por unha entidade legal nunha organización pode realizar traballos para outra entidade legal da mesma organización. Nesta situación, pode utilizar a función de gasto entre empresas para atribuír os gastos do traballador á entidade legal para a que se realizou o traballo.
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
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076283"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="8c8aa-104">Gastos entre empresas</span><span class="sxs-lookup"><span data-stu-id="8c8aa-104">Intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8c8aa-105">Un traballador empregado por unha entidade legal nunha organización pode realizar traballos para outra entidade legal da mesma organización.</span><span class="sxs-lookup"><span data-stu-id="8c8aa-105">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="8c8aa-106">Nesta situación, pode utilizar a función de gasto entre empresas para atribuír os gastos do traballador á entidade legal para a que se realizou o traballo.</span><span class="sxs-lookup"><span data-stu-id="8c8aa-106">In this situation, you can use the intercompany expense feature to assign the worker’s expenses to the legal entity for which the work was performed.</span></span> <span data-ttu-id="8c8aa-107">A entidade legal que emprega ao traballador denomínase entidade legal prestamista.</span><span class="sxs-lookup"><span data-stu-id="8c8aa-107">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="8c8aa-108">A entidade legal pola que o traballador incorre en gastos chámase entidade xurídica prestameira.</span><span class="sxs-lookup"><span data-stu-id="8c8aa-108">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="8c8aa-109">Antes de que un traballador poida crear e enviar gastos por traballos que se realicen para unha entidade legal diferente, na entidade legal prestamista, na páxina **Parámetros de xestión de gastos** , seleccione a opción **Permitir liñas de gasto entre empresas**.</span><span class="sxs-lookup"><span data-stu-id="8c8aa-109">Before a worker can create and submit expenses for work that is performed for a different legal entity, in the loaning legal entity, on the **Expense management parameters** page, select the **Allow intercompany expense lines** option.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="8c8aa-110">Contabilización de impostos por gastos entre empresas</span><span class="sxs-lookup"><span data-stu-id="8c8aa-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8c8aa-111">Se desexa usar grupos fiscais asociados á entidade legal prestamista (orixe) no canto da entidade legal prestameira (destino) no seu informe de gastos, deberá configuralo no imposto sobre vendas do libro maior.</span><span class="sxs-lookup"><span data-stu-id="8c8aa-111">If you want to use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you will need to configure this in the General ledger sales tax set up.</span></span> <span data-ttu-id="8c8aa-112">Cando o parámetro do libro maior **Entidade para a contabilización de impostos entre empresas** está establecido en **Orixe** e **Aplicar normas de tributación do imposto sobre as vendas** está establecido en **Non** , empregarase a combinación fiscal para a entidade legal prestamista.</span><span class="sxs-lookup"><span data-stu-id="8c8aa-112">When the General ledger parameter, **Legal entity for intercompany tax posting** is set to **Source** and **Apply sales tax taxation rules** is set to **No** , the tax combination for the loaning legal entity will be used.</span></span> <span data-ttu-id="8c8aa-113">Cando o mesmo parámetro está configurado en **Destino** , utilizarase a combinación fiscal para a entidade legal prestameira.</span><span class="sxs-lookup"><span data-stu-id="8c8aa-113">When the same parameter is set to **Destination** , the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="8c8aa-114">Para as entidades legais dos Estados Unidos, cando o parámetro está establecido en **Orixe** , o campo **Imposto sobre as vendas pendente de cobro** tamén debe configurarse na nova páxina **Grupos de contabilización de libro maior**.</span><span class="sxs-lookup"><span data-stu-id="8c8aa-114">For legal entities in the United States, when the parameter is set to **Source** , the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="8c8aa-115">O motor de contabilidade utilizará a información deste campo para a entrada contable relacionada cos impostos.</span><span class="sxs-lookup"><span data-stu-id="8c8aa-115">The accounting engine will use the information from this field for tax related accounting entry.</span></span>   
<span data-ttu-id="8c8aa-116">O comportamento é coherente para as liñas de gastos contabilizadas con ou sen proxecto.</span><span class="sxs-lookup"><span data-stu-id="8c8aa-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  
