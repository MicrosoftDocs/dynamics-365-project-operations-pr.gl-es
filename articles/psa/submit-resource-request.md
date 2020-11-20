---
title: Enviar unha solicitude de recurso
description: Este tema fornece información sobre o envío dunha solicitude dun recurso de proxecto.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
ms.topic: article
author: JohnPBurrows
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 50f076b89c5ac7fee4866534cbd47d81f92f3ab3
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131263"
---
# <a name="submitting-a-resource-request"></a><span data-ttu-id="5de24-103">Enviar unha solicitude de recurso</span><span class="sxs-lookup"><span data-stu-id="5de24-103">Submitting a resource request</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="5de24-104">Pode enviar un requisito de recurso xerado como solicitude de recurso.</span><span class="sxs-lookup"><span data-stu-id="5de24-104">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="5de24-105">A solicitude envíase a un xestor de recursos para o seu cumprimento.</span><span class="sxs-lookup"><span data-stu-id="5de24-105">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="5de24-106">En Project Service Automation (PSA), na páxina **Proxectos** prema no separador **Equipo** para ver unha lista de recursos reservables.</span><span class="sxs-lookup"><span data-stu-id="5de24-106">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab to view a list bookable resources.</span></span> 
2. <span data-ttu-id="5de24-107">Seleccione o recurso xenérico que ten un requisito de recurso da lista e, a seguir, prema en **Enviar solicitude**.</span><span class="sxs-lookup"><span data-stu-id="5de24-107">Select the generic resource that has a resource requirement from the list and then click **Submit Request**.</span></span>

![Enviar unha solicitude de recurso](media/RM-how-to-18.png)

<span data-ttu-id="5de24-109">O estado da solicitude de membro xenérico do equipo cambiará a **Enviado**.</span><span class="sxs-lookup"><span data-stu-id="5de24-109">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="5de24-110">Despois de que o xestor de recursos cumpra a solicitude, o recurso xenérico substituirase por un recurso nomeado se o xestor de recursos cumpre a solicitude coa reserva dun recurso nomeado.</span><span class="sxs-lookup"><span data-stu-id="5de24-110">After the request is fulfilled by the resource manager, the generic resource will be replaced by a named resource if the resource manager fulfills the request with the booking of a named resource.</span></span> <span data-ttu-id="5de24-111">Se non, o recurso xenérico permanecerá no equipo e o estado da solicitude cambiará a **Necesita revisión**, se o xestor de recursos propuxo un recurso nomeado.</span><span class="sxs-lookup"><span data-stu-id="5de24-111">Otherwise, the generic resource will remain on the team and the request status will change to **Needs Review**, if the resource manager has proposed a named resource.</span></span>
