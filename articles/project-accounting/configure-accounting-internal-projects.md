---
title: Configurar a contabilidade para proxectos internos
description: Este tema ofrece información sobre como configurar prácticas de contabilidade para proxectos internos en Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9f1cc75b12fec81d726e46f8d970dcfe030f6b29
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287596"
---
# <a name="configure-accounting-for-internal-projects"></a><span data-ttu-id="25541-103">Configurar a contabilidade para proxectos internos</span><span class="sxs-lookup"><span data-stu-id="25541-103">Configure accounting for internal projects</span></span>

<span data-ttu-id="25541-104">_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_</span><span class="sxs-lookup"><span data-stu-id="25541-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="25541-105">Os proxectos internos permiten ás empresas realizar un seguimento dos custos relacionados coas actividades que non se facturan a un cliente.</span><span class="sxs-lookup"><span data-stu-id="25541-105">Internal projects allow companies track cost related to activities that aren't being billed to a customer.</span></span> <span data-ttu-id="25541-106">Exemplos de proxectos internos inclúen:</span><span class="sxs-lookup"><span data-stu-id="25541-106">Examples of internal projects include:</span></span>

- <span data-ttu-id="25541-107">Desenvolvemento dun produto, como unha aplicación móbil, e rastrexo do custo asociado ao desenvolvemento.</span><span class="sxs-lookup"><span data-stu-id="25541-107">Developing a product, such as a mobile app, and tracking the cost associated with the development.</span></span>
- <span data-ttu-id="25541-108">Xestión do tempo e os gastos previos á venda.</span><span class="sxs-lookup"><span data-stu-id="25541-108">Managing pre-sale time and expense.</span></span> <span data-ttu-id="25541-109">Este proxecto interno de prevenda pódese converter máis tarde a un proxecto facturable se se gaña a oferta.</span><span class="sxs-lookup"><span data-stu-id="25541-109">This pre-sale internal project can be converted later to a billable project if quote is won.</span></span>

<span data-ttu-id="25541-110">Calquera proxecto non asociado a un contrato en Dynamics 365 Project Operations é tratado como interno.</span><span class="sxs-lookup"><span data-stu-id="25541-110">Any project not associated with a contract in Dynamics 365 Project Operations is treated as internal.</span></span> <span data-ttu-id="25541-111">Os perfís de custos e ingresos do proxecto non se usan para determinar as regras de contabilidade para o proxecto.</span><span class="sxs-lookup"><span data-stu-id="25541-111">Project cost and revenue profiles aren't used to determine accounting rules for the project.</span></span> <span data-ttu-id="25541-112">O custo interno do proxecto sempre se contabiliza seguindo os principios de resultados.</span><span class="sxs-lookup"><span data-stu-id="25541-112">Internal project cost is always posted using profit and loss principles.</span></span> <span data-ttu-id="25541-113">As contas de libro maior para os asentos defínense na páxina **Configuración de asentos de libro maior**.</span><span class="sxs-lookup"><span data-stu-id="25541-113">Ledger accounts for postings are defined on the **Ledger posting setup** page.</span></span>

- <span data-ttu-id="25541-114">As transaccións de tempo contabilízanse cargando a conta de **Custo** conta e abonando a conta de **Asignación de nómina**.</span><span class="sxs-lookup"><span data-stu-id="25541-114">Time transactions are posted by debiting the **Cost** account and crediting the **Payroll allocation** account.</span></span>
- <span data-ttu-id="25541-115">As transaccións de gasto contabilízanse cargando a conta de **Custo** conta e abonando a conta de **Conta compensada para gastos**.</span><span class="sxs-lookup"><span data-stu-id="25541-115">Expense transactions are posted by debiting the **Cost** account and crediting the **Offset account for expense**.</span></span>

<span data-ttu-id="25541-116">Despois de que as transaccións se contabilicen no proxecto, se o proxecto está asociado a un contrato de proxecto, o sistema inverte todas as transaccións acumuladas e crea novas transaccións facturables.</span><span class="sxs-lookup"><span data-stu-id="25541-116">After transactions are posted to the project, if the project is associated with a project contract, the system reverses all accumulated transactions and creates new billable transactions.</span></span> <span data-ttu-id="25541-117">As transaccións facturables seguen as regras de contabilidade definidas no perfil de ingresos e custos do proxecto respectivo.</span><span class="sxs-lookup"><span data-stu-id="25541-117">The billable transactions follow the accounting rules defined in respective Project cost and revenue profile.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]