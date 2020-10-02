---
title: Visión xeral das dimensións de prezos
description: Este tema fornece información sobre as dimensións de prezos en Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: fe2ab3a1b12c00e346e27709d66b5a0cb81a3b56
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898214"
---
# <a name="pricing-dimensions-overview"></a>Visión xeral das dimensións de prezos

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

As dimensións que se usan en recursos humanos para configurar prezos e custos inclúense en dúas categorías:

- Persoas
- Traballo planificado

Por iso, hai dous tipos de valores de dimensión de prezos dispoñibles:

- **Conxuntos de opcións**: Dimensións que son enumeracións fixas para un conxunto de valores.
- **Valores baseados en entidades**: Dimensións que poden ser un conxunto variado de valores.

## <a name="pricing-dimensions"></a>Dimensións de prezos

Dynamics 365 Project Operations inclúese cun conxunto predefinido de dimensións de prezos. Pode ver estas dimensións de prezos indo a **Project Operations** > **Parámetros**. No rexistro de parámetros, no separador **Dimensións de prezos baseados na cantidade**, verifique que o rol, **msdyn_resourcecategory**, e a unidade organizativa de recursos, **msdyn_organizationalunit** teñan os campos **Aplicable a vendas** e **Aplicable a custo** establecidos en **Si**. Con estes campos activados, pode establecer o prezo e o custo para cada combinación de roles e unidades organizativas.

Se precisa un prezo ou custo para os seus recursos usando atributos adicionais, pode crear campos, entidades e dimensións personalizados.

## <a name="pricing-human-resource-time"></a>Prezos do tempo de recursos humanos
Como unha organización valora o tempo dos recursos humanos é moitas veces unha consideración estratéxica importante que afecta directamente á rendibilidade da organización. Traballe cos equipos financeiros e os responsables de prácticas cando a súa organización estea preparada para identificar como quere configurar os tipos de factura e custos para o tempo de recursos humanos.

Outras consideracións para fixar os prezos inclúen se hai que volver usar campos ou entidades que actualmente non teñen dimensións de prezos pero que se aplican como dimensión de prezos para a súa organización. Campos como **Categoría de transacción** (**msdyn_transactioncategory**) e **Recurso reservable** ( **bookableresource**) son exemplos de dimensións do candidato. 

Considere se a súa dimensión de prezos debe ser unha táboa ou un conxunto de opcións. Se prevé cambios nos valores dunha dimensión que serán máis de 10 ou 12 e necesita atributos adicionais nestes valores, pode crear unha entidade en lugar dun conxunto de opcións. Manter un conxunto de opcións, como engadir ou eliminar valores, require un administrador ou programador, mentres que a adición de novas filas a unha táboa pode facelo a maioría dos usuarios.

O seguinte exemplo mostra os tipos de facturación que se configuran en función do rol e da unidade organizativa de recursos á que pertenza o recurso. As taxas de custo baséanse normalmente na banda salarial do empregado e a unidade organizativa á que pertenza. Neste exemplo, as táboas de taxa de facturación e taxa de custo terán o seguinte aspecto.

**Exemplo de taxas de facturación**

| Rol        | Unidade organizativa    |Unidade      |Prezo      |Moeda  |
| ------------|-------------|----------|----------:|----------|
| Programador   | Contoso EUA  |Hour | 200|USD     |
| Programador   | Contoso India |Hour|   112|USD     |


**Exempo de taxas de custo**

| Banda salarial     | Unidade organizativa    |Unidade      |Prezo      |Moeda  |
| ----------------|-------------|----------|----------:|----------|
| A miña empresa_Banda1 | Contoso EUA  |Hour | 145|USD     |
| A miña empresa_Banda2 | Contoso India |Hour|   67|USD     |
