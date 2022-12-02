---
title: Dotación de persoal dun proxecto con traballadores contratados e capacidade subcontratada
description: Este artigo explica como se poden cubrir os requisitos do proxecto mediante traballadores contratados ou capacidade subcontratada en Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 30e16efeed93ab4568eac57fb3ed46067a08524d
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522433"
---
# <a name="staffing-a-project-with-contract-workers-and-subcontracted-capacity"></a>Dotación de persoal dun proxecto con traballadores contratados e capacidade subcontratada

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Os membros xenéricos do equipo do proxecto poden contar con empregados ou traballadores contratados. Ao dotar de persoal a un proxecto con traballadores contratados, pode limitar as súas opcións de persoal a traballadores contratados específicos que estean asignados a unha liña de subcontratación. 

## <a name="search-for-staff-resource-requirements-with-contract-workers-that-belong-to-a-specific-subcontract-line"></a>Busca de necesidades de recursos de persoal con traballadores contratados que pertenzan a unha liña de subcontratación específica

Para buscar de necesidades de recursos de persoal con traballadores contratados que pertenzan a unha liña de subcontratación específica, siga estes pasos:

1. Cree un membro xenérico do equipo do proxecto que faga referencia a unha subcontratación ou liña de subcontratación.
2. Xere un requisito de recursos para este membro xenérico do equipo do proxecto mediante o botón **Xerar requisito** na subgrade dos membros do equipo do proxecto.
3. Seleccione a fila do membro do equipo e, a seguir, seleccione o botón **Reservar** na subgrade. 
4. Isto abre o panel de programación co contexto dos requisitos. Xunto con outros atributos como datas, función e campos da unidade organizativa, os filtros do panel de programación tamén se enchen automaticamente cos campos de fornecedor, subcontratación e liña de subcontratación do requisito de recursos.
5. O sistema busca recursos que cumpran os criterios de filtro e enuméraos. 
6. Seleccione un dos recursos filtrados e reserve o recurso para o requisito. 
7. Un membro do equipo do proxecto créase e actualízase con referencias a unha subcontratación liña de subcontratación. Vaia a **Estimacións do proxecto** e seleccione **Actualizar prezos** para ver o custo actualizado da atribución de recursos. 

> [!NOTE]
> A actualización do membro do equipo do proxecto cunha referencia de ssubcontratación e liña de subcontratación pode non ser sempre posible durante a reserva se o recurso está atribuído a varias liñas de subcontratación. Se o sistema non pode actualizar o membro do equipo do proxecto cunha subcontratacióno e unha liña de subcontratación, abra o rexistro do membro do equipo do proxecto e actualice manualmente estes campos para que a estimación do custo financeiro reflicta con precisión o custo do subcontratista.

## <a name="search-for-and-staff-resource-requirements-with-any-contract-worker"></a>Buscar e dotar de persoal requisitos de recursos con calquera traballador contratado

Para buscar e dotar de persoal requisitos de recursos con calquera traballador contratado, siga estes pasos:

1. Cree un membro xenérico do equipo do proxecto.
2. Xere un requisito de recursos para este membro xenérico do equipo do proxecto mediante o botón **Xerar requisito** na subgrade dos membros do equipo do proxecto.
3. Seleccione a fila do membro do equipo e, a seguir, seleccione o botón **Reservar** na subgrade. 
4. Isto abre o panel de programación co contexto dos requisitos. Xunto con outros atributos como datas, función e campos da unidade organizativa, os filtros do panel de programación tamén se enchen automaticamente cos campos de fornecedor, subcontratación e liña de subcontratación do requisito de recursos. Como o requisito non tiña ningún valor de subcontratación ou liña de subcontratación cuberto, estes atributos estarán baleiros no panel de filtros.
5. O sistema busca recursos que cumpran os criterios de filtro e enuméraos.
6. Actualice o campo **Tipo de traballador** do panel de filtros a **Traballador por pontrato** para limitar a busca aos traballadores por contrato. Actualice o **Fornecedor** no panel de filtros para seleccionar un fornecedor para limitar a busca e mostrar só os traballadores por contrato que pertenzan a unha empresa fornecedora específica.
7. Seleccione un traballador por contrato da lista e reserve o recurso para o requisito.
8. Créase un membro do equipo do proxecto. Non obstante, o membro do equipo do proxecto non está actualizado con ningunha subcontratación pu liña de subcontratación e, polo tanto, o custo da atribución de recursos non se determinará utilizando o prezo de subcontratación. Actualice manualmente o membro do equipo do proxecto cunha liña de subcontratación e vaia a **Estimacións do proxecto** e seleccione **Actualizar prezos** para ver o custo actualizado da atribución de recursos.

> [!NOTE]
> Os membros do equipo do proxecto que teñen **Tipo de traballador** como **Traballador por contrato** pero non teñen unha referencia de subcontratación están marcados como **Non válido** na grade **Membros do equipo do proxecto**. Se hai algún membro do equipo do proxecto con este estado, abra o rexistro do membro do equipo do proxecto e actualice manualmente os campos de subacontratación e liña de subcontratación para que a estimación do custo financeiro reflicta con precisión o custo do subcontratista no separador **Estimacións**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
