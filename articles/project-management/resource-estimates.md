---
title: Estimacións financeiras do tempo de recursos en proxectos
description: Este tema ofrece información sobre como se calculan as estimacións financeiras para o tempo.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: aab5c11a7dc23331c935403a4f96ec7197ec1572
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8592552"
---
# <a name="financial-estimates-for-resource-time-on-projects"></a>Estimacións financeiras do tempo de recursos en proxectos

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

As estimacións financeiras para o tempo calcúlanse en función de tres factores: 

- O tipo de membro xenérico ou nomeado do equipo atribuído a cada tarefa de nó folla no plan do proxecto. 
- O tipo ou complexidade do traballo.
- A extensión do esforzo para a atribución do recurso na tarefa. 

Os dous primeiros factores inflúen no custo unitario ou na taxa de facturación da atribución dun recurso. O custo unitario ou a taxa de facturación dunha atribución de recursos está determinado polos atributos do recurso atribuído. Estes atributos inclúen a unidade organizativa á que pertence o recurso e o rol estándar do recurso. Tamén pode engadir atributos personalizados relevantes para a súa empresa para o recurso, como o título estándar ou o nivel de experiencia, e que inflúan no custo unitario ou na taxa de facturación da tarefa.
Ademais dos atributos do recurso, os atributos do traballo, como a tarefa, tamén poden influír na taxa de facturación unitaria ou na taxa de custos da atribución. Por exemplo, cando certas tarefas son máis complexas, a atribución do recurso a esas tarefas específicas dá lugar a un custo unitario ou unha taxa de facturación superiores aos das tarefas menos complexas.   

O terceiro factor proporciona a cantidade de horas a esa taxa. Nos casos en que unha tarefa abrangue dous períodos de prezos, é probable que a primeira parte da atribución de recursos para esa tarefa teña un custo e un prezo diferentes dos da segunda parte da tarefa. A estimación do esforzo en cada atribución de recursos é un valor complexo almacenado coa distribución diaria do esforzo por día.

Para obter instrucións detalladas sobre como configurar atributos de traballo e recursos personalizados como dimensións de prezos e custos, consulte [Descrición xeral das dimensións de prezos](../pricing-costing/pricing-dimensions-overview.md).

A estimación financeira de cada atribución de recursos calcúlase como **taxa/hora para a tarefa multiplicada polo número de horas.**  De modo semellante á estimación do esforzo, a estimación financeira de custos e ingresos para cada atribución de recursos é un valor complexo almacenado coa distribución diaria de importe monetario por día. 

## <a name="summarizing-financial-estimates-for-time"></a>Resumo das estimacións financeiras para o tempo
Unha estimación financeira do tempo nunha tarefa de nó folla é a suma das estimacións financeiras de todas as atribucións de recursos para esa tarefa.

Unha estimación financeira do tempo nunha tarefa resumo ou principal é a suma das estimacións financeiras en todas as súas tarefas secundarias. Este é o custo laboral estimado no proxecto. 

![Estimacións de recursos.](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a>Prezo de custo e moeda de custos por defecto

O prezo de custo predefinido procede das listas de prezos anexas á unidade contratante do proxecto. A moeda de custo dun proxecto é sempre a moeda da unidade contratante do proxecto. Nunha atribución de recursos, a estimación financeira do custo almacénase na moeda de custos do proxecto. Ás veces, a moeda na que se establece a taxa de custo na lista de prezos é diferente da moeda de custos do proxecto. Nestes casos, a aplicación converte a moeda na que se establece o prezo de custo para a moeda do proxecto. Na grade **Estimacións**, todas as estimacións de custos móstranse e resúmense na moeda de custos do proxecto. 

## <a name="default-bill-rate-and-sales-currency"></a>Taxa de facturación de gastos e moeda de vendas por defecto

O prezo de venda predefinido procede das listas de prezos do proxecto anexas ao contrato de proxecto relacionado se se gaña o negocio, ou da oferta do proxecto relacionado se o negocio aínda está en fase de prevenda. A moeda de vendas do proxecto é sempre a moeda da oferta do proxecto ou do contrato do proxecto. Nunha atribución de recursos, a estimación financeira das vendas almacénase na moeda de vendas do proxecto. A diferenza do custo, o prezo de venda establecido na lista de prezos nunca pode ser diferente da moeda de vendas do proxecto. Non hai ningunha situación na que sexa necesaria a conversión de moeda. Na grade **Estimacións**, todas as estimacións de vendas móstranse e resúmense na moeda de vendas do proxecto. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
