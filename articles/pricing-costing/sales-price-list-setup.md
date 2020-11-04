---
title: Configuración de lista de prezos de vendas
description: Este tema ofrece información sobre listas de prezos de vendas para a fixación de prezos de proxectos.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1d2c797b72666123eb0a18d2d0c1df9fe3d207f7
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076187"
---
# <a name="sales-price-list-setup"></a>Configuración de lista de prezos de vendas

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Para as ofertas e contratos de proxectos, a lista de prezos dun proxecto ten un padrón de anulación de prezos diferente do que ten unha lista de prezos de produtos. Nunha liña de oferta baseada en catálogo de produtos, pode anular o prezo aos roles e categorías directamente na liña de oferta, porque cada liña de oferta apunta exactamente a un elemento do catálogo. Non obstante, nunha liña de oferta baseada en proxectos, non pode anular o prezo aos roles e categorías directamente na liña de oferta. Pode usar a lista de prezos de proxectos para traballar cos dous padróns de anulación distintos.

> [!NOTE]
> Recomendamos que teña unha lista de prezos independente para os recursos do proxecto e os elementos do seu catálogo, debido ás diferenzas de comportamento entre ambas cando anula os prezos.

Cada unha das seguintes entidades pode ter unha ou varias listas de prezos de vendas asociadas para os prezos de proxectos:

- Cliente (conta) 
- Oportunidade 
- Oferta 
- Contrato do proxecto

A asociación destas entidades cunha lista de prezos está indicada polas listas de prezos do proxecto. Pode asociar unha ou varias listas de prezos ás entidades de vendas Cliente, Oportunidade, Oferta e Contrato de Proxecto.

Non se introduce automaticamente unha lista de prezos do proxecto predefinida nun rexistro de clientes. Non obstante, pode anexar manualmente unha lista de prezos do proxecto ao rexistro de clientes. Non obstante, debe anexar manualmente unha lista de prezos do proxecto só cando teña un acordo de prezos personalizado co cliente. 

Cando unha lista de prezos do proxecto está anexada a unha entidade de vendas, valídase a seguinte información:

- A lista de prezos ten un contexto de **Vendas** 
- A moeda da lista de prezos coincide coa moeda do cliente. 

No contrato do proxecto, a seguinte orde de precedencia utilízase para establecer automaticamente as listas de prezos de proxecto relacionadas:

1. Oferta
2. Oportunidade
3. Cliente 
4. Configuración global 

Cando se introduce de xeito predeterminado unha lista de prezos do proxecto, o sistema valida que a moeda coincide coa moeda do cliente e que as listas de prezos por defecto que se introduciron teñen un contexto de **Vendas**.

Pode asociar varias listas de prezos ás entidades de vendas Cliente, Oportunidade, Oferta e Contrato de Proxecto. Esta capacidade admite prezos predefinidos específicos da data para un contrato de proxecto de longa duración, onde pode requirir máis dunha lista de prezos para dar conta das actualizacións de prezos que se producen por mor da inflación. Non obstante, se as listas de prezos que asocie á entidade Cliente, Oportunidade, Oferta ou Contrato de proxecto teñen efectividade de datas superpostas, os prezos por defecto poderían ser incorrectos. Polo tanto, ten que asegurarse de que as listas de prezos do proxecto que teñan data de superposición non estean asociadas a esas entidades.
