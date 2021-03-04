---
title: Xestionar oportunidades baseadas en proxectos
description: Este tema ofrece información sobre como traballar con oportunidades relacionadas cos proxectos.
author: rumant
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c5a8bfea5540432a62d7075443cf237571bfa4de
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4118471"
---
# <a name="manage-project-based-opportunities"></a>Xestionar oportunidades baseadas en proxectos

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

As empresas baseadas en proxectos normalmente teñen as súas operacións de entrega repartidas en varios países e zonas xeográficas. O custo da execución e entrega do proxecto pode variar segundo a zona xeográfica ou división que xestione a entrega. Á súa vez, isto pode afectar ás marxes do acordo. A entrega de servizos baseados en proxectos normalmente implica grandes cantidades de tempo de recursos humanos, gastos considerables de viaxe, custos materiais e outros gastos.

As oportunidades baseadas en proxecto en Dynamics 365 Project Operations deséñanse con extensións a Dynamics 365 Sales. O tema ofrece detalles sobre os diferentes campos e a lóxica empresarial incluídos na funcionalidade adicional que as empresas baseadas en proxectos requiren para xestionar oportunidades baseadas en proxectos.

## <a name="view-all-project-based-opportunities"></a>Ver todas as oportunidades baseadas en proxectos

Unha lista de todas as oportunidades baseadas en proxectos pódese ver na páxina de lista **Oportunidade**. 

1. Vaia a **Vendas** > **Oportunidades**.
2. Use o **Conmutador de visualizacións** para seleccionar outras vistas filtradas das oportunidades. Pode crear as súas propias visualizacións con criterios de filtro personalizados para configurar estas visualizacións e as opcións de navegación.

As oportunidades do proxecto pódense crear ou eliminar desta páxina de lista ou da páxina de detalles.

## <a name="business-process-flow-for-project-based-deals"></a>Fluxo do proceso de negocio para ofertas baseadas en proxecto

Os seguintes fluxos do proceso de negocio son compatibles con ofertas baseadas en proxecto en Project Operations:

- Proceso de negocio de cliente potencial a oportunidade
- Proceso de vendas de oportunidade

### <a name="lead-to-opportunity-business-process"></a>Proceso de negocio de cliente potencial a oportunidade 
O proceso de negocio de cliente potencial a oportunidade admite as seguintes fases:

| Fase | Entidade asignada | Funcionalidade |
| --- | --- | --- |
| Cualificar | Cliente potencial | Cualifique o cliente potencial para crear unha conta, un contacto e unha oportunidade. |
| Desenvolver | Oportunidade | Desenvolva a oportunidade de engadir máis información sobre o traballo involucrado, as partes interesadas e a competencia. |
| Propor | Oportunidade | Desenvolva a proposta e obteña a aprobación do equipo de revisión interno. |
| Pechar | Oportunidade | Gañe a oportunidade para pechar o acordo. |

### <a name="opportunity-sales-process"></a>Proceso de vendas de oportunidade
O proceso de venda de oportunidades en Project Operations é unha extensión ao fluxo de negocio de proceso de vendas de oportunidades na aplicación Sales. Este proceso de negocio está deseñado listo para usar para admitir as seguintes etapas nunha oportunidade baseada en proxectos.

| Fase | Entidade asignada | Funcionalidade |
| --- | --- | --- |
| Cualificar | Oportunidade | Cualifique o cliente potencial para crear unha conta, un contacto e unha oportunidade. |
| Propor | Oferta | Desenvolva a proposta utilizando ofertas de proxecto e obteña a aprobación do equipo de revisión interno. |
| Contrato | Contrato do proxecto | Gañe a oferta para crear o contrato e comezar a execución e entrega do proxecto. |
| Pechar | Contrato do proxecto | Remate o traballo con éxito e peche o contrato do proxecto. |

> [!NOTE]
> Se o acordo baseado en proxecto comezou cun cliente potencial, prevalecerá o proceso comercial de cliente potencial a oportunidade.
>
> Se o acordo baseado en proxecto comezou cunha oportunidade, prevalecerá o proceso de vendas de oportunidade.

Pode editar o fluxo do proceso de negocio do produto ou crear os seus propios fluxos do proceso de negocio para rastrexar o seu proceso de vendas segundo sexa necesario. Para obter máis información sobre o fluxos do proceso de negocio, consulte [Información xeral sobre fluxos do proceso de negocio](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/customize/business-process-flows-overview).


[!INCLUDE[footer-include](../includes/footer-banner.md)]