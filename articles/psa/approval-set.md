---
title: Conxuntos de aprobacións
description: Este tema ofrece información sobre o conxunto de aprobacións, as solicitudes e os subconxuntos desas operacións.
author: stsporen
manager: tfehr
ms.date: 05/28/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: ac73313420029ece740d0bdb9c21c7abaa9defc6
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116869"
---
# <a name="approval-sets"></a><span data-ttu-id="7b790-103">Conxuntos de aprobacións</span><span class="sxs-lookup"><span data-stu-id="7b790-103">Approval sets</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="7b790-104">Os conxuntos de aprobacións agrupan solicitudes de aprobación do grupo en subconxuntos de operacións máis pequenos.</span><span class="sxs-lookup"><span data-stu-id="7b790-104">Approval sets group approval requests together into smaller subsets of operations.</span></span> <span data-ttu-id="7b790-105">Esta agrupación permite que as aprobacións sexan procesadas en orde por Proxecto e permite reintentar e secuenciar.</span><span class="sxs-lookup"><span data-stu-id="7b790-105">This grouping allows approvals to be processed in order by Project and allows for retrying and sequencing.</span></span> <span data-ttu-id="7b790-106">A agrupación mellora a fiabilidade e a rastrexabilidade do procesamento de aprobacións para grandes volumes de aprobacións.</span><span class="sxs-lookup"><span data-stu-id="7b790-106">Grouping improves the reliability and traceability of approval processing for large volumes of approvals.</span></span>

<span data-ttu-id="7b790-107">Os conxuntos de aprobacións indican o estado global de procesamento dos seus rexistros relacionados.</span><span class="sxs-lookup"><span data-stu-id="7b790-107">Approval sets indicate the overall processing state of their related records.</span></span> <span data-ttu-id="7b790-108">Cando un rexistro de aprobación se procesa usando un conxunto de aprobacións, o rexistro pasa de **Enviado** a **Aprobado**, e está desvinculado do conxunto de aprobacións.</span><span class="sxs-lookup"><span data-stu-id="7b790-108">When an approval record is processed using an approval set, the record moves from **Submitted** to **Approved**, and is unlinked from the approval set.</span></span> <span data-ttu-id="7b790-109">Se un rexistro falla cando se somete a aprobación, o rexistro permanecerá nun estado de **Enviado** e o conxunto de aprobacións márcase como erro.</span><span class="sxs-lookup"><span data-stu-id="7b790-109">If a record fails when it is submitted for approval, the record remains in a status of **Submitted** and the approval set is marked as failed.</span></span> <span data-ttu-id="7b790-110">O conxunto de aprobacións rexistra a mensaxe de erro do fallo.</span><span class="sxs-lookup"><span data-stu-id="7b790-110">The approval set logs the error message of the failure.</span></span>

## <a name="processing-approvals-and-approval-sets"></a><span data-ttu-id="7b790-111">Tramitación de aprobacións e conxuntos de aprobacións</span><span class="sxs-lookup"><span data-stu-id="7b790-111">Processing approvals and approval sets</span></span>
<span data-ttu-id="7b790-112">As aprobacións que están na fila para o procesamento son visibles na vista **Aprobacións de procesamento**.</span><span class="sxs-lookup"><span data-stu-id="7b790-112">Approvals that are queued for processing are visible in the **Processing Approvals** view.</span></span> <span data-ttu-id="7b790-113">O sistema tenta procesar todas as entradas varias veces de xeito asíncrono, o que inclúe tentar de novo unha aprobación se fallaron os intentos anteriores.</span><span class="sxs-lookup"><span data-stu-id="7b790-113">The system tries to process all the entries multiple times asynchronously, including retrying an approval if previous attempts failed.</span></span>

<span data-ttu-id="7b790-114">O campo **Vida útil do conxunto de aprobacións** rexistra o número de intentos que quedan para procesar o conxunto antes de que se marque como erro.</span><span class="sxs-lookup"><span data-stu-id="7b790-114">The **Approval Set Lifetime** field records the number of attempts left to process the set before it's marked as failed.</span></span>

## <a name="failed-approvals-and-approval-sets"></a><span data-ttu-id="7b790-115">Aprobacións e conxuntos de aprobacións con erros</span><span class="sxs-lookup"><span data-stu-id="7b790-115">Failed approvals and approval sets</span></span>
<span data-ttu-id="7b790-116">A vista **Aprobacións con erros** mostra todas as aprobacións que requiren a intervención do usuario.</span><span class="sxs-lookup"><span data-stu-id="7b790-116">The **Failed Approvals** view lists all approvals that require user intervention.</span></span> <span data-ttu-id="7b790-117">Abra os rexistros de conxuntos de aprobacións asociados para identificar a causa do fallo.</span><span class="sxs-lookup"><span data-stu-id="7b790-117">Open the associated approval set logs to identify the cause of the failure.</span></span>
<span data-ttu-id="7b790-118">Seleccionar **Tentar de novo** engade ao reconto de vida útil do conxunto de aprobacións, traslada o conxunto de aprobacións a un estado de **Procesando** e tenta procesar os rexistros restantes.</span><span class="sxs-lookup"><span data-stu-id="7b790-118">Selecting **Retry** adds to the approval set lifetime count, moves the approval set back to a status of **Processing**, and attempts to process the remaining records.</span></span>

## <a name="configure-approval-sets"></a><span data-ttu-id="7b790-119">Configurar conxuntos de aprobacións</span><span class="sxs-lookup"><span data-stu-id="7b790-119">Configure approval sets</span></span>

###  <a name="enable-the-approval-sets-feature"></a><span data-ttu-id="7b790-120">Activar a funcionalidade de Conxuntos de aprobacións</span><span class="sxs-lookup"><span data-stu-id="7b790-120">Enable the Approval sets feature</span></span>
<span data-ttu-id="7b790-121">Antes de activar a funcionalidade de Conxuntos de aprobacións, comprobe que non hai aprobacións procesándose actualmente.</span><span class="sxs-lookup"><span data-stu-id="7b790-121">Before you enable the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="7b790-122">Vaia á páxina **Parámetros do proxecto** e seleccione **Control de funcionalidades** > **Activar aprobacións modernas**.</span><span class="sxs-lookup"><span data-stu-id="7b790-122">Go to the **Project parameters** page and select **Feature Control** > **Enable Modern Approvals**.</span></span>

### <a name="turn-off-the-approval-sets-feature"></a><span data-ttu-id="7b790-123">Desactivar a funcionalidade de Conxuntos de aprobacións</span><span class="sxs-lookup"><span data-stu-id="7b790-123">Turn off the Approval sets feature</span></span>
<span data-ttu-id="7b790-124">Antes de desactivar a funcionalidade de Conxuntos de aprobación, comprobe que non hai aprobacións procesándose actualmente.</span><span class="sxs-lookup"><span data-stu-id="7b790-124">Before you turn off the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="7b790-125">Vaia á páxina **Parámetros do proxecto** e seleccione **Control de funcionalidades** > **Desactivar aprobacións modernas**.</span><span class="sxs-lookup"><span data-stu-id="7b790-125">Go to the **Project Parameters** page and select **Feature Control** > **Disable Modern Approvals**.</span></span>

### <a name="configuring-the-asynchronous-threshold"></a><span data-ttu-id="7b790-126">Configuración do limiar asíncrono</span><span class="sxs-lookup"><span data-stu-id="7b790-126">Configuring the asynchronous threshold</span></span> 
<span data-ttu-id="7b790-127">Cando se crean conxuntos de aprobacións, o procesamento móvese a un segundo plano cando o número de rexistros seleccionado para a aprobación supera o limiar indicado.</span><span class="sxs-lookup"><span data-stu-id="7b790-127">When approval sets are created, processing moves to the background when the selected number of records for approval exceeds the indicated threshold.</span></span> <span data-ttu-id="7b790-128">Use o campo **Limiar asíncrono** para configurar cando o proceso de aprobación debe executarse de xeito síncrono ou asíncrono.</span><span class="sxs-lookup"><span data-stu-id="7b790-128">Use the **Asynchronous Threshold** field to configure when approval processing should be run synchronously or asynchronously.</span></span>
<span data-ttu-id="7b790-129">Os valores válidos son:</span><span class="sxs-lookup"><span data-stu-id="7b790-129">Valid values are:</span></span>

  - <span data-ttu-id="7b790-130">Cero: Todas as solicitudes deben procesarse de forma asíncrona.</span><span class="sxs-lookup"><span data-stu-id="7b790-130">Zero: All requests should be processed asynchronously.</span></span> 
  - <span data-ttu-id="7b790-131">Números superiores a cero: As aprobacións só se procesan de xeito asíncrono cando o número de aprobacións enviado supera este valor.</span><span class="sxs-lookup"><span data-stu-id="7b790-131">Numbers greater than zero: Approvals are processed asynchronously only when the submitted number of approvals exceeds this value.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
