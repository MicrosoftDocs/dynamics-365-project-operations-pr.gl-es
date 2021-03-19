---
title: Listas de prezos predefinidas
description: Este tema ofrece información sobre as listas de prezos de custo de vendas predefinidas en Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 04c97429ab8ac769dd22b4127432d80de8fde937
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275581"
---
# <a name="default-price-lists"></a>Listas de prezos predefinidas

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

## <a name="sales-price-lists"></a>Listas de prezos de vendas

Todas as ofertas e contratos do proxecto en Dynamics 365 Project Operations conteñen unha lista de prezos de venda predefinida. 

### <a name="price-list-default-on-project-quotes"></a>Lista de prezos predefinida nas ofertas de proxecto
O sistema completa o seguinte proceso para determinar que lista de prezos predefinirá nunha oferta de proxecto:

1. O sistema analiza as listas de prezos que se anexan ás listas de prezos de proxecto da conta. 
2. Se hai listas de prezos de proxecto anexadas ao rexistro da conta, o sistema examina as listas de prezos de vendas anexas aos parámetros do proxecto que coinciden coa moeda da oferta do proxecto.
3. A seguir, o sistema comproba a efectividade da data das listas de prezos que coinciden co intervalo de datas da oferta do proxecto. Especificamente, a data na que se creou a oferta.
4. Se hai varias listas de prezos efectivas para a data da oferta do proxecto, todas as listas de prezos predefínense na oferta do proxecto.
5. Se non hai listas de prezos en vigor para a data da oferta do proxecto, non hai ningunha lista de prezos predefinida na oferta do proxecto. Na oferta do proxecto aparecerá unha mensaxe de advertencia. A mensaxe indica que os datos reais e as estimacións do proxecto non terán prezo porque non hai listas de prezos do proxecto anexas.

### <a name="price-list-default-on-project-contracts"></a>Lista de prezos predefinida nos contratos de proxecto 
O sistema completa o seguinte proceso para determinar que lista de prezos predefinirá nun contrato de proxecto:

1. Se o contrato se crea a partir dunha oferta, as listas de prezos do proxecto cópianse por separado e anéxanse ao contrato do proxecto.
2. Se o contrato se crea desde cero, o sistema examina as listas de prezos que se anexan ás listas de prezos do proxecto da conta. Se non hai listas de prezos de proxecto anexadas ao rexistro da conta, o sistema busca listas de prezos de vendas anexas aos parámetros do proxecto que coinciden coa moeda do contrato do proxecto.
4. A seguir, o sistema comproba a efectividade da data das listas de prezos que coinciden co intervalo de datas do contrato do proxecto. Especificamente, a data na que se creou o contrato.
5. Se hai varias listas de prezos efectivas para a data do contrato do proxecto, todas as listas de prezos predefínense no contrato.
6. Se non hai listas de prezos en vigor para a data do contrato, non hai ningunha lista de prezos predefinida para o contrato. No contrato do proxecto aparecerá unha mensaxe de advertencia. A mensaxe indica que os datos reais e as estimacións do proxecto non terán prezo porque non hai listas de prezos do proxecto anexas.

## <a name="cost-price-lists"></a>Listas de prezos de custo

As listas de prezos de custo non están predefinidas en ningunha entidade en Project Operations. A determinación da lista de prezos de custo que se usa para os custos do proxecto sempre se fai no momento. O sistema completa o seguinte proceso para determinar que lista de prezos se usará para os custos do proxecto:

1. O sistema analiza primeiro as listas de prezos que se anexan á unidade da organización contratante do proxecto.
2. O sistema analiza a data de efectividade das listas de prezos que coinciden coa data da estimación entrante ou da liña real. Nesta situación, *liña de estimación* refírese aos tres contextos de estimación en Project Operations:

    - Liña de estimación de proxecto
    - Detalle da liña da oferta
    - Detalle da liña de contrato
  
3. Se hai varias listas de prezos efectivas para a data na estimación entrante ou o dato real, selecciónase a lista de prezos creada máis recentemente.
4. Se non hai listas de prezos anexadas á unidade da organización contratante do proxecto, o sistema examina as listas de prezos de custo anexas aos parámetros do proxecto que coinciden coa moeda do proxecto.
5. A seguir, o sistema analiza a data de efectividade das listas de prezos que coinciden coa data da estimación entrante ou da liña real. 
6. Se hai varias listas de prezos efectivas para a data na estimación entrante ou o dato real, selecciónase a lista de prezos creada máis recentemente.
7. Se non hai listas de prezos de custo anexas aos parámetros do proxecto que coincidan coa moeda e a data de efectividade, o sistema predefinirá a taxa de custo a cero (0) na estimación entrante ou na liña real.


[!INCLUDE[footer-include](../includes/footer-banner.md)]