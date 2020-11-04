---
title: Pechar ofertas
description: Este tema ofrece información sobre o peche dunha oferta en Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cc3b2cdeb1ac46b7d927c1f96e94e9154d3eebf8
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076053"
---
# <a name="close-quotes"></a><span data-ttu-id="a113b-103">Pechar ofertas</span><span class="sxs-lookup"><span data-stu-id="a113b-103">Close quotes</span></span> 

<span data-ttu-id="a113b-104">_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="a113b-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a113b-105">Unha oferta de proxecto pódese pechar como gañada ou perdida.</span><span class="sxs-lookup"><span data-stu-id="a113b-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="a113b-106">As operacións de activar e revisar en ofertas non se admiten en Microsoft Dynamics 365 Project Operations, polo que se pode pechar un borrador de oferta.</span><span class="sxs-lookup"><span data-stu-id="a113b-106">The Activate and Revise operations on quotes is not supported in Microsoft Dynamics 365 Project Operations, so a draft quote can be closed.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="a113b-107">Pechar unha oferta como gañada</span><span class="sxs-lookup"><span data-stu-id="a113b-107">Close a quote as Won</span></span>

<span data-ttu-id="a113b-108">Ao pechar unha oferta de proxecto como Gañada, pecharase a oferta co estado establecido en Pechada e o motivo para o estado establecido en Gañada.</span><span class="sxs-lookup"><span data-stu-id="a113b-108">Closing a project quote as Won will close the quote with the status set to Closed and the status reason set to Won.</span></span> <span data-ttu-id="a113b-109">Pechar a oferta fai que a oferta de proxecto sexa de só lectura e se crea un borrador do contrato do proxecto que contén a información da oferta.</span><span class="sxs-lookup"><span data-stu-id="a113b-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="a113b-110">Debido a que non se pode volver abrir unha oferta pechada, aparece un diálogo de confirmación antes de que se fagan os cambios xa que non se pode volver abrir unha oferta pechada e os cambios son irreversibles.</span><span class="sxs-lookup"><span data-stu-id="a113b-110">Because a closed quote can't be reopened, a confirmation dialog There is a confirmation dialog before the changes are done since a closed quote cannot be re-opened and the changes are irreversible.</span></span>

<span data-ttu-id="a113b-111">Se a oferta se anexa a unha oportunidade, calquera outra oferta de proxecto da oportunidade péchase automaticamente como Perdida.</span><span class="sxs-lookup"><span data-stu-id="a113b-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="a113b-112">Impacto financeiro de pechar unha oferta como Gañada</span><span class="sxs-lookup"><span data-stu-id="a113b-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="a113b-113">Se houbo datos reais por tempo rexistrados nun proxecto mentres aínda está anexado a un borrador de oferta, só se rexistra o custo do tempo ou do gasto.</span><span class="sxs-lookup"><span data-stu-id="a113b-113">If there have been any actuals for time recorded on a project while it is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="a113b-114">Despois de pechar a oferta como Gañada, a aplicación refactorizará os custos revertendo os datos reais de custos máis antigos e creando novos datos reais de custos.</span><span class="sxs-lookup"><span data-stu-id="a113b-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="a113b-115">A aplicación procesará estes custos reais en función do método de facturación da liña de contrato do proxecto asociado.</span><span class="sxs-lookup"><span data-stu-id="a113b-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="a113b-116">Se os datos reais de custos fan referencia a unha liña de contrato de tempo e material, o sistema creará automaticamente os correspondentes datos reais de vendas non facturados para cando se peche a oferta e se cree o contrato do proxecto.</span><span class="sxs-lookup"><span data-stu-id="a113b-116">If the cost actuals reference a time and material contract line, the system will automatically create corresponding unbilled sales actuals for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="a113b-117">Se os datos reais de custos fan referencia a unha liña de contrato de prezo fixo, a aplicación deixará de procesar os datos reais de custos en función das regras de facturación dividida para os clientes do contrato do proxecto.</span><span class="sxs-lookup"><span data-stu-id="a113b-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="a113b-118">Peche dunha oferta como perdida:</span><span class="sxs-lookup"><span data-stu-id="a113b-118">Closing a quote as lost:</span></span>

<span data-ttu-id="a113b-119">Ao pechar unha oferta de proxecto como Perdida, establecerase o estado en Pechada e motivo para o estado en Perdida.</span><span class="sxs-lookup"><span data-stu-id="a113b-119">Closing a project quote as Lost will set the status to Closed and status reason to Lost.</span></span> <span data-ttu-id="a113b-120">O peche da oferta fai que a oferta de proxecto sexa de só lectura.</span><span class="sxs-lookup"><span data-stu-id="a113b-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="a113b-121">Debido a que non se pode volver abrir unha oferta pechada, antes de pechar unha oferta, un diálogo de confirmación confirmará os cambios.</span><span class="sxs-lookup"><span data-stu-id="a113b-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="a113b-122">Se a oferta proxecto pechada como Perdida ten un proxecto referenciado nalgunha das súas liñas, ese proxecto tamén se marcará como Pechado e cancelaranse as reservas de recursos a partir dese día.</span><span class="sxs-lookup"><span data-stu-id="a113b-122">If the project quote that is closed as Lost has a project referenced on any of its lines, that project is also marked as Closed and any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="a113b-123">En Project Operations, pechar unha oferta como Gañada ou Perdida non afectará a ese estado da Oportunidade, que permanecerá aberta ata que se peche manualmente.</span><span class="sxs-lookup"><span data-stu-id="a113b-123">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>
