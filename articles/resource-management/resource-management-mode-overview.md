---
title: Visión xeral dos modos de xestión de recursos
description: Neste tema se proporciona información sobre a funcionalidade de xestión de recursos en Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4a8e605109e48b50da68abeee989f8ac8d3d659c
ms.sourcegitcommit: cf79185c8c84c55fbae55f9cfc1b17840e072b49
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930089"
---
# <a name="resource-management-modes-overview"></a>Visión xeral dos modos de xestión de recursos

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_


Dynamics 365 Project Operations admite dous modos para que poida executar o fluxo de reservas global. O modo de xestión defínese como un parámetro do proxecto e pódese modificar se o seu negocio precisa cambiar.    

## <a name="central-mode"></a>Modo central
Para as organizacións que centralizan a asignación de recursos a proxectos, o modo central proporciona un xeito de garantir que os xestores de proxectos poidan definir os requisitos de recursos a nivel de proxecto. O cumprimento dos requisitos de recursos delegase nun xestor de recursos. Os xestores de proxectos poden aceptar ou rexeitar os recursos propostos polo xestor de recursos.

![Modo central](./media/resource-management-central.png)

Para xestionar recursos co modo Central, consulte:

- [Atribuír recursos reservables xenéricos a unha tarefa e xerar requisitos de recursos](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [Reservar recursos nomeados a partir de requisitos de recursos](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [Enviar unha solicitude de recurso](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [Cumprir unha solicitude de recursos](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [Aceptar ou rexeitar un recurso de proxecto proposto desde unha solicitude de recurso](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a>Modo híbrido
Para as organizacións que requiren flexibilidade na asignación de recursos, o modo híbrido permite tanto aos xestores de proxectos como aos xestores de recursos reservar recursos.

![Modo híbrido](./media/resource-management-hybrid.png)

Ademais do proceso de modo central admitido, consulte os seguintes temas para xestionar todos os demais fluxos de reservas admitidos no modo híbrido:

Reservar un recurso directamente para un proxecto:
- [Reservar recursos reservables nomeados para un equipo de proxectos e atribuír tarefas](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

Reservar un recursos a partir dun requisito de recursos:
- [Atribuír recursos reservables xenéricos a unha tarefa e xerar requisitos de recursos](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [Reservar recursos nomeados a partir de requisitos de recursos](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
