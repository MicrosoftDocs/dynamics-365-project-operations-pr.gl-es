---
title: Enviar unha solicitude de recurso
description: Este tema fornece información sobre o envío dunha solicitude dun recurso de proxecto.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
author: JohnPBurrows
ms.assetid: 9f4a6315-3905-4b15-8d06-e5dae30ccbb8
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 2b706ae25af5ba85647c98353b5950663fafc292
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751431"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="0ebc3-103">Enviar unha solicitude de recurso</span><span class="sxs-lookup"><span data-stu-id="0ebc3-103">Submit a resource request</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="0ebc3-104">Pode enviar un requisito de recurso xerado como solicitude de recurso.</span><span class="sxs-lookup"><span data-stu-id="0ebc3-104">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="0ebc3-105">A solicitude envíase a un xestor de recursos para o seu cumprimento.</span><span class="sxs-lookup"><span data-stu-id="0ebc3-105">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="0ebc3-106">En Project Service Automation (PSA), na páxina **Proxectos** prema no separador **Equipo** para ver unha lista de recursos reservables.</span><span class="sxs-lookup"><span data-stu-id="0ebc3-106">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab to view a list bookable resources.</span></span> 
2. <span data-ttu-id="0ebc3-107">Seleccione o recurso xenérico que ten un requisito de recurso da lista e, a seguir, prema en **Enviar solicitude**.</span><span class="sxs-lookup"><span data-stu-id="0ebc3-107">Select the generic resource that has a resource requirement from the list and then click **Submit Request**.</span></span>

![Enviar unha solicitude de recurso](media/RM-how-to-18.png)

<span data-ttu-id="0ebc3-109">O estado da solicitude de membro xenérico do equipo cambiará a **Enviado**.</span><span class="sxs-lookup"><span data-stu-id="0ebc3-109">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="0ebc3-110">Despois de que o xestor de recursos cumpra a solicitude, o recurso xenérico substituirase por un recurso nomeado se o xestor de recursos cumpre a solicitude coa reserva dun recurso nomeado.</span><span class="sxs-lookup"><span data-stu-id="0ebc3-110">After the request is fulfilled by the resource manager, the generic resource will be replaced by a named resource if the resource manager fulfills the request with the booking of a named resource.</span></span> <span data-ttu-id="0ebc3-111">Se non, o recurso xenérico permanecerá no equipo e o estado da solicitude cambiará a **Necesita revisión**, se o xestor de recursos propuxo un recurso nomeado.</span><span class="sxs-lookup"><span data-stu-id="0ebc3-111">Otherwise, the generic resource will remain on the team and the request status will change to **Needs Review**, if the resource manager has proposed a named resource.</span></span>
