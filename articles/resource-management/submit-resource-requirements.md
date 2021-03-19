---
title: Enviar unha solicitude de recurso
description: Pode enviar un requisito de recurso xerado como solicitude de recurso. A solicitude envíase a un xestor de recursos para o seu cumprimento.
author: ruhercul
manager: Annbe
ms.date: 10/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: bc97af1ec90e60417c502eb329a85004e769e05b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279136"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="a5863-104">Enviar unha solicitude de recurso</span><span class="sxs-lookup"><span data-stu-id="a5863-104">Submit a resource request</span></span>

<span data-ttu-id="a5863-105">_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="a5863-105">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a5863-106">Pode enviar un requisito de recurso xerado como solicitude de recurso.</span><span class="sxs-lookup"><span data-stu-id="a5863-106">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="a5863-107">A solicitude envíase a un xestor de recursos para o seu cumprimento.</span><span class="sxs-lookup"><span data-stu-id="a5863-107">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="a5863-108">En Dynamics 365 Project Operations, na páxina **Proxectos**, seleccione o separador **Equipo** para ver unha lista de recursos reservables.</span><span class="sxs-lookup"><span data-stu-id="a5863-108">In Dynamics 365 Project Operations, on the **Projects** page, select the **Team** tab to view a list of bookable resources.</span></span> 
2. <span data-ttu-id="a5863-109">Seleccione o recurso xenérico que ten un requisito de recurso da lista e prema en **Enviar solicitude**.</span><span class="sxs-lookup"><span data-stu-id="a5863-109">Select the generic resource that has a resource requirement from the list, and then click **Submit Request**.</span></span>

<span data-ttu-id="a5863-110">O estado da solicitude de membro xenérico do equipo cambiará a **Enviado**.</span><span class="sxs-lookup"><span data-stu-id="a5863-110">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="a5863-111">Despois de que se cumpra a solicitude, o recurso xenérico substitúese por un recurso nomeado se o xestor de recursos cumpre a solicitude coa reserva dun recurso nomeado.</span><span class="sxs-lookup"><span data-stu-id="a5863-111">After the request is fulfilled, the generic resource is replaced by a named resource if the resource manager fulfills the request by booking a named resource.</span></span> <span data-ttu-id="a5863-112">Se non, se o xestor de recursos propón un recurso nomeado, o recurso xenérico permanece no equipo e o estado da solicitude cambiará a **Necesita revisión**.</span><span class="sxs-lookup"><span data-stu-id="a5863-112">Otherwise, if the resource manager proposes a named resource, the generic resource remains on the team and the request status will change to **Needs Review**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]