---
title: Pechar unha oferta
description: Este tema ofrece información sobre o peche de ofertas en Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a2c752ba6395ed4bf025092219350dc245f7428f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277246"
---
# <a name="close-a-quote"></a><span data-ttu-id="77863-103">Pechar unha oferta</span><span class="sxs-lookup"><span data-stu-id="77863-103">Close a quote</span></span>

<span data-ttu-id="77863-104">_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_</span><span class="sxs-lookup"><span data-stu-id="77863-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="77863-105">Unha oferta de proxecto pódese pechar como gañada ou perdida.</span><span class="sxs-lookup"><span data-stu-id="77863-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="77863-106">Debido a que as funcións Activar e Revisar non se admiten nas ofertas en Microsoft Dynamics 365 Project Operations, pode pechar un borrador de oferta.</span><span class="sxs-lookup"><span data-stu-id="77863-106">Because the functions Activate and Revise are not supported on quotes in Microsoft Dynamics 365 Project Operations, you can close a draft quote.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="77863-107">Pechar unha oferta como gañada</span><span class="sxs-lookup"><span data-stu-id="77863-107">Close a quote as Won</span></span>

<span data-ttu-id="77863-108">Ao pechar unha oferta de proxecto como Gañada, o estado da oferta establecerase en **Pechada** e o motivo para o estado establecido en **Gañada**.</span><span class="sxs-lookup"><span data-stu-id="77863-108">Closing a project quote as Won will set the status of the quote to **Closed** and status reason to **Won**.</span></span> <span data-ttu-id="77863-109">Pechar as ofertas fai que sexan de só lectura e se crea un borrador do contrato do proxecto con toda a información da oferta.</span><span class="sxs-lookup"><span data-stu-id="77863-109">Closing the quotes makes it read-only and creates a draft project contract with all the quote information.</span></span> <span data-ttu-id="77863-110">Debido a que non se pode volver abrir unha oferta pechada, antes de pechar unha oferta, un diálogo de confirmación confirmará os cambios.</span><span class="sxs-lookup"><span data-stu-id="77863-110">Because a closed quote can't be reopened, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="77863-111">O contrato do proxecto creado a partir dunha oferta de proxecto tamén está dispoñible no módulo de xestión e contabilidade de proxectos de Project Operations.</span><span class="sxs-lookup"><span data-stu-id="77863-111">The project contract created from a project quote is also made available in the Project management and accounting module of Project Operations.</span></span> <span data-ttu-id="77863-112">Se un contrato de proxecto non está asociado a un proxecto en ningunha das súas liñas, este contrato de proxecto ponse a disposición como un contrato de proxecto inactivo e faise activo en canto un proxecto se asigna a polo menos unha das súas liñas de contrato.</span><span class="sxs-lookup"><span data-stu-id="77863-112">If a project contract is not mapped to a project on any of its lines, this project contract is made available as an inactive project contract and becomes active as soon as a project is mapped to at least one of its contract lines.</span></span>

<span data-ttu-id="77863-113">Se a oferta se anexa a unha oportunidade, calquera outra oferta de proxecto da oportunidade péchase automaticamente como Perdida.</span><span class="sxs-lookup"><span data-stu-id="77863-113">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="77863-114">Impacto financeiro de pechar unha oferta como Gañada</span><span class="sxs-lookup"><span data-stu-id="77863-114">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="77863-115">Se houbo datos reais por tempo rexistrados nun proxecto mentres aínda está anexado a un borrador de oferta, só se rexistra o custo do tempo ou do gasto.</span><span class="sxs-lookup"><span data-stu-id="77863-115">If there have been any actuals for time recorded on a project while it is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="77863-116">Despois de pechar a oferta como Gañada, a aplicación refactorizará os custos revertendo os datos reais de custos máis antigos e creando novos datos reais de custos.</span><span class="sxs-lookup"><span data-stu-id="77863-116">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="77863-117">A aplicación procesará estes custos reais en función do método de facturación da liña de contrato do proxecto asociado.</span><span class="sxs-lookup"><span data-stu-id="77863-117">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="77863-118">Se os datos reais de custos fan referencia a unha liña de contrato de tempo e material, o sistema creará automaticamente os correspondentes datos reais de vendas non facturados para cando se peche a oferta e se cree o contrato do proxecto.</span><span class="sxs-lookup"><span data-stu-id="77863-118">If the cost actuals reference a time and material contract line, the system will automatically create corresponding unbilled sales actuals for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="77863-119">Se os datos reais de custos fan referencia a unha liña de contrato de prezo fixo, a aplicación deixará de procesar os datos reais de custos en función das regras de facturación dividida para os clientes do contrato do proxecto.</span><span class="sxs-lookup"><span data-stu-id="77863-119">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals based on the split billing rules for the project contract customers.</span></span>

<span data-ttu-id="77863-120">Todos os datos reais reprocesados están dispoñibles no módulo de xestión e contabilidade do proxecto para que o contable do proxecto poida revisalos, actualizalos e contabilizalos no libro maior.</span><span class="sxs-lookup"><span data-stu-id="77863-120">All reprocessed actuals are available in the Project management and accounting module for the Project accountant to review, update, and post to the General ledger.</span></span> 

## <a name="close-a-quote-as-lost"></a><span data-ttu-id="77863-121">Pechar unha oferta como Perdida</span><span class="sxs-lookup"><span data-stu-id="77863-121">Close a quote as Lost</span></span>

<span data-ttu-id="77863-122">Ao pechar unha oferta de proxecto como Perdida, establecerase o estado en **Pechada** e motivo para o estado en **Perdida**.</span><span class="sxs-lookup"><span data-stu-id="77863-122">Closing a project quote as Lost will set the status to **Closed** and status reason to **Lost**.</span></span> <span data-ttu-id="77863-123">Pechar a oferta fai que sexa só de lectura.</span><span class="sxs-lookup"><span data-stu-id="77863-123">Closing the quote makes it read-only.</span></span> <span data-ttu-id="77863-124">Debido a que non se pode volver abrir unha oferta pechada, antes de pechar unha oferta, un diálogo de confirmación confirmará os cambios.</span><span class="sxs-lookup"><span data-stu-id="77863-124">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="77863-125">Se a oferta proxecto pechada como Perdida ten un proxecto referenciado nalgunha das súas liñas, ese proxecto tamén se marcará como Pechado e cancelaranse as reservas de recursos a partir dese día.</span><span class="sxs-lookup"><span data-stu-id="77863-125">If the project quote that is closed as Lost has a project referenced on any of its lines, that project is also marked as Closed and any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="77863-126">En Project Operations, pechar unha oferta como Gañada ou Perdida non afectará a ese estado da Oportunidade, que permanecerá aberta ata que se peche manualmente.</span><span class="sxs-lookup"><span data-stu-id="77863-126">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]