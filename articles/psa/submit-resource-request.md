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
ms.openlocfilehash: 173572be43149aea253bf7beddb993f8c50ab337
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149721"
---
# <a name="submitting-a-resource-request"></a><span data-ttu-id="5ed79-103">Enviar unha solicitude de recurso</span><span class="sxs-lookup"><span data-stu-id="5ed79-103">Submitting a resource request</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="5ed79-104">Pode enviar un requisito de recurso xerado como solicitude de recurso.</span><span class="sxs-lookup"><span data-stu-id="5ed79-104">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="5ed79-105">A solicitude envíase a un xestor de recursos para o seu cumprimento.</span><span class="sxs-lookup"><span data-stu-id="5ed79-105">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="5ed79-106">En Project Service Automation (PSA), na páxina **Proxectos** prema no separador **Equipo** para ver unha lista de recursos reservables.</span><span class="sxs-lookup"><span data-stu-id="5ed79-106">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab to view a list bookable resources.</span></span> 
2. <span data-ttu-id="5ed79-107">Seleccione o recurso xenérico que ten un requisito de recurso da lista e, a seguir, prema en **Enviar solicitude**.</span><span class="sxs-lookup"><span data-stu-id="5ed79-107">Select the generic resource that has a resource requirement from the list and then click **Submit Request**.</span></span>

![Enviar unha solicitude de recurso](media/RM-how-to-18.png)

<span data-ttu-id="5ed79-109">O estado da solicitude de membro xenérico do equipo cambiará a **Enviado**.</span><span class="sxs-lookup"><span data-stu-id="5ed79-109">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="5ed79-110">Despois de que o xestor de recursos cumpra a solicitude, o recurso xenérico substituirase por un recurso nomeado se o xestor de recursos cumpre a solicitude coa reserva dun recurso nomeado.</span><span class="sxs-lookup"><span data-stu-id="5ed79-110">After the request is fulfilled by the resource manager, the generic resource will be replaced by a named resource if the resource manager fulfills the request with the booking of a named resource.</span></span> <span data-ttu-id="5ed79-111">Se non, o recurso xenérico permanecerá no equipo e o estado da solicitude cambiará a **Necesita revisión**, se o xestor de recursos propuxo un recurso nomeado.</span><span class="sxs-lookup"><span data-stu-id="5ed79-111">Otherwise, the generic resource will remain on the team and the request status will change to **Needs Review**, if the resource manager has proposed a named resource.</span></span>
