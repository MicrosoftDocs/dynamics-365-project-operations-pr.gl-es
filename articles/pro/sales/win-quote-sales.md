---
title: Pechar unha oferta - lite
description: Este tema ofrece información sobre o peche dunha oferta en Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 75345fed57dcbdb84f2a82587c7d0c152530c72b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994134"
---
# <a name="close-a-quote---lite"></a><span data-ttu-id="c0f67-103">Pechar unha oferta - lite</span><span class="sxs-lookup"><span data-stu-id="c0f67-103">Close a quote - lite</span></span>

<span data-ttu-id="c0f67-104">_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="c0f67-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c0f67-105">Unha oferta de proxecto pódese pechar como gañada ou perdida.</span><span class="sxs-lookup"><span data-stu-id="c0f67-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="c0f67-106">Pódese pechar un borrador de oferta porque as operacións Activar e Revisar de ofertas non son compatibles con Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="c0f67-106">A draft quote can be closed because the Activate and Revise operations on quotes isn't supported in Microsoft Dynamics 365 Project Operations.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="c0f67-107">Pechar unha oferta como gañada</span><span class="sxs-lookup"><span data-stu-id="c0f67-107">Close a quote as Won</span></span>

<span data-ttu-id="c0f67-108">Cando pecha unha oferta de proxecto como Gañada, o estado establécese en Pechada e o motivo para o estado é Gañada.</span><span class="sxs-lookup"><span data-stu-id="c0f67-108">When you close a project quote as Won, the status is set to Closed and the status reason is Won.</span></span> <span data-ttu-id="c0f67-109">Pechar a oferta fai que a oferta de proxecto sexa de só lectura e se crea un borrador do contrato do proxecto que contén a información da oferta.</span><span class="sxs-lookup"><span data-stu-id="c0f67-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="c0f67-110">Debido a que non se pode volver abrir unha oferta pechada, un diálogo de confirmación confirmará os seus cambios.</span><span class="sxs-lookup"><span data-stu-id="c0f67-110">Because a closed quote can't be reopened, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="c0f67-111">Se a oferta se anexa a unha oportunidade, calquera outra oferta de proxecto da oportunidade péchase automaticamente como Perdida.</span><span class="sxs-lookup"><span data-stu-id="c0f67-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="c0f67-112">Impacto financeiro de pechar unha oferta como Gañada</span><span class="sxs-lookup"><span data-stu-id="c0f67-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="c0f67-113">Se hai algún dato real nun proxecto mentres aínda está anexo a un borrador de oferta, só se rexistra o custo do tempo ou do gasto.</span><span class="sxs-lookup"><span data-stu-id="c0f67-113">If there are any actuals for time on a project while is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="c0f67-114">Despois de pechar a oferta como Gañada, a aplicación refactorizará os custos revertendo os datos reais de custos máis antigos e creando novos datos reais de custos.</span><span class="sxs-lookup"><span data-stu-id="c0f67-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="c0f67-115">A aplicación procesará estes custos reais en función do método de facturación da liña de contrato do proxecto asociado.</span><span class="sxs-lookup"><span data-stu-id="c0f67-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="c0f67-116">Se os datos reais de custo fan referencia a unha liña de contrato de tempo e material, créanse as vendas sen facturar correspondentes cando se pecha a oferta e se crea o contrato do proxecto.</span><span class="sxs-lookup"><span data-stu-id="c0f67-116">If the cost actuals reference a time and material contract line, corresponding unbilled sales actuals are created for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="c0f67-117">Se os datos reais de custo fan referencia a unha liña de contrato de prezo fixo, a aplicación deixará de reprocesar os custos reais baseados nas regras de facturación divididas para os clientes do contrato do proxecto.</span><span class="sxs-lookup"><span data-stu-id="c0f67-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals that are based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="c0f67-118">Peche dunha oferta como perdida:</span><span class="sxs-lookup"><span data-stu-id="c0f67-118">Closing a quote as lost:</span></span>

<span data-ttu-id="c0f67-119">Cando pecha unha oferta de proxecto como Perdida, o estado establécese en Pechada e o motivo para o estado é Perdida.</span><span class="sxs-lookup"><span data-stu-id="c0f67-119">When you close a project quote as Lost, the status is set to Closed and status reason is Lost.</span></span> <span data-ttu-id="c0f67-120">O peche da oferta fai que a oferta de proxecto sexa de só lectura.</span><span class="sxs-lookup"><span data-stu-id="c0f67-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="c0f67-121">Debido a que non se pode volver abrir unha oferta pechada, antes de pechar unha oferta, un diálogo de confirmación confirmará os cambios.</span><span class="sxs-lookup"><span data-stu-id="c0f67-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="c0f67-122">Se a oferta do proxecto pechada como Perdida fai referencia a un proxecto nalgunha das súas liñas, ese proxecto tamén se marcará como Pechado.</span><span class="sxs-lookup"><span data-stu-id="c0f67-122">If the project quote that is closed as Lost references a project on any of its lines, that project is also marked as Closed.</span></span> <span data-ttu-id="c0f67-123">Cancélanse as reservas de recursos a partir dese día.</span><span class="sxs-lookup"><span data-stu-id="c0f67-123">Any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="c0f67-124">En Project Operations, pechar unha oferta como Gañada ou Perdida non afectará a ese estado da Oportunidade, que permanecerá aberta ata que se peche manualmente.</span><span class="sxs-lookup"><span data-stu-id="c0f67-124">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]