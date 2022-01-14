---
title: Dotación de persoal dun proxecto con traballadores contratados e capacidade subcontratada
description: Este tema explica como se poden cubrir os requisitos do proxecto utilizando traballadores por contrato ou capacidade subcontratada en Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 7e9a0ca08f472999138589f31ca820b733b6303e
ms.sourcegitcommit: 45893132bd8bfaf944ee0ac855484684dd1ee945
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 12/09/2021
ms.locfileid: "7903021"
---
# <a name="staffing-a-project-with-contract-workers-and-subcontracted-capacity"></a>Dotación de persoal dun proxecto con traballadores contratados e capacidade subcontratada

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

Os membros xenéricos do equipo do proxecto poden contar con empregados ou traballadores contratados. Ao dotar de persoal a un proxecto con traballadores contratados, pode limitar as súas opcións de persoal a traballadores contratados específicos que estean asignados a unha liña de subcontratación. 

## <a name="search-for-staff-resource-requirements-with-contract-workers-that-belong-to-a-specific-subcontract-line"></a>Busca de necesidades de recursos de persoal con traballadores contratados que pertenzan a unha liña de subcontratación específica

Para buscar e requisitos de recursos de persoal con traballadores contratados que pertenzan a unha liña de subcontratación específica, siga estes pasos:

1. Crea un membro xenérico do equipo do proxecto que faga referencia a unha liña de subcontrato e subcontrato.
2. Xera un requisito de recursos para este membro xenérico do equipo do proxecto mediante o **Xerar esixencia** botón na subreixa dos membros do equipo do proxecto.
3. Seleccione a fila do membro do equipo e, a continuación, seleccione a **Libro** botón da subreixa. 
4. Isto abre o taboleiro de programación co contexto dos requisitos. Xunto con outros atributos como datas, funcións e campos da unidade organizativa, os filtros do cadro de programación tamén se enchen automaticamente cos campos de provedor, subcontrato e liña de subcontrato do requisito de recursos.
5. O sistema busca recursos que cumpran os criterios de filtro e enuméraos. 
6. Seleccione un dos recursos filtrados e reserve o recurso para o requisito. 
7. Créase e actualízase un membro do equipo do proxecto con referencias de subcontrato e liña de subcontrato. Ir a **Presupostos do proxecto** e selecciona **Actualizar prezos** para ver o custo actualizado da asignación de recursos. 

> [!NOTE]
> A actualización do membro do equipo do proxecto cunha referencia de subcontrato e liña de subcontrato pode non ser sempre posible durante a reserva se o recurso está asignado a varias liñas de subcontrato. Se o sistema non pode actualizar o membro do equipo do proxecto cunha liña de subcontrato e subcontrato, abra o rexistro do membro do equipo do proxecto e actualice manualmente estes campos para que a estimación do custo financeiro reflicta con precisión o custo do subcontratista.

## <a name="search-for-and-staff-resource-requirements-with-any-contract-worker"></a>Busca e requisitos de recursos de persoal con calquera traballador contratado

Para buscar e os requisitos de recursos de persoal con calquera traballador contratado, siga estes pasos:

1. Crea un membro xenérico do equipo do proxecto.
2. Xera un requisito de recursos para este membro xenérico do equipo do proxecto mediante o **Xerar esixencia** botón na subreixa dos membros do equipo do proxecto.
3. Seleccione a fila do membro do equipo e, a continuación, seleccione a **Libro** botón da subreixa. 
4. Isto abre o taboleiro de programación co contexto dos requisitos. Xunto con outros atributos como datas, funcións e campos da unidade organizativa, os filtros do cadro de programación tamén se enchen automaticamente cos campos de provedor, subcontrato e liña de subcontrato do requisito de recursos. Dado que o requisito non tiña ningún valor de liña de subcontrato ou subcontrato cuberto, estes atributos estarán baleiros no panel de filtros.
5. O sistema busca recursos que cumpran os criterios de filtro e enuméraos.
6. Actualiza o **Tipo de traballador** campo do panel de filtros para **Traballador por Contrato** limitar a busca aos traballadores contratados. Actualizar **Vendedor** no panel de filtros para seleccionar un provedor para limitar a busca para mostrar só os traballadores por contrato que pertenzan a unha empresa de provedores específica.
7. Seleccione un traballador contratado da lista e reserve o recurso para o requisito.
8. Créase un membro do equipo do proxecto. Non obstante, o membro do equipo do proxecto non está actualizado con ningunha liña de subcontrato ou subcontrato e, polo tanto, a asignación de recursos non se custará utilizando o prezo do subcontrato. Actualiza manualmente o membro do equipo do proxecto cunha liña de subcontrato e vai a **Presupostos do proxecto** e selecciona **Actualizar prezos** para ver o custo actualizado da asignación de recursos.

> [!NOTE]
> Membros do equipo do proxecto que teñan **Tipo de traballador** como **Traballador contratado** pero non teñen unha referencia de subcontrato están marcados como **Non válido** no **Membros do equipo do proxecto** reixa. Se hai algún membro do equipo do proxecto con este estado, abra o rexistro do membro do equipo do proxecto e actualice manualmente os campos da liña de subcontrato e subcontrato para que a estimación do custo financeiro reflicta con precisión o custo do subcontratista no **Estimacións** ficha. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
