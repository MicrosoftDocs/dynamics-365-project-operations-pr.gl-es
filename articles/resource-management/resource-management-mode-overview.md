---
title: Visión xeral dos modos de xestión de recursos
description: Neste artigo se proporciona información sobre a funcionalidade de xestión de recursos en Dynamics 365 Project Operations.
author: ruhercul
ms.date: 10/01/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: dd50d12686a6ad17f6a95ccf0c2f1447cc470bf7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928430"
---
# <a name="resource-management-modes-overview"></a>Visión xeral dos modos de xestión de recursos

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_


Dynamics 365 Project Operations admite dous modos para que poida executar o fluxo de reservas global. O modo de xestión defínese como un parámetro do proxecto e pódese modificar se o seu negocio precisa cambiar.    

## <a name="central-mode"></a>Modo central
Para as organizacións que centralizan a asignación de recursos a proxectos, o modo central proporciona un xeito de garantir que os xestores de proxectos poidan definir os requisitos de recursos a nivel de proxecto. O cumprimento dos requisitos de recursos delegase nun xestor de recursos. Os xestores de proxectos poden aceptar ou rexeitar os recursos propostos polo xestor de recursos.

![Modo central.](./media/resource-management-central.png)

Para xestionar recursos co modo Central, consulte:

- [Atribuír recursos reservables xenéricos a unha tarefa e xerar requisitos de recursos](/dynamics365/project-service/assign-generic-bookable-resource)
- [Reservar recursos nomeados a partir de requisitos de recursos](/dynamics365/project-service/book-named-resource)
- [Enviar unha solicitude de recurso](/dynamics365/project-service/submit-resource-request)
- [Cumprir unha solicitude de recursos](/dynamics365/project-service/resource-management-fulfill-requests)
- [Aceptar ou rexeitar un recurso de proxecto proposto desde unha solicitude de recurso](/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a>Modo híbrido
Para as organizacións que requiren flexibilidade na asignación de recursos, o modo híbrido permite tanto aos xestores de proxectos como aos xestores de recursos reservar recursos.

![Modo híbrido.](./media/resource-management-hybrid.png)

Ademais do proceso de modo central admitido, consulte os seguintes artigos para xestionar todos os demais fluxos de reservas admitidos no modo híbrido:

Reservar un recurso directamente para un proxecto:
- [Reservar recursos reservables nomeados para un equipo de proxectos e atribuír tarefas](/dynamics365/project-service/assign-named-bookable-resource)

Reservar un recursos a partir dun requisito de recursos:
- [Atribuír recursos reservables xenéricos a unha tarefa e xerar requisitos de recursos](/dynamics365/project-service/assign-generic-bookable-resource)
- [Reservar recursos nomeados a partir de requisitos de recursos](/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]