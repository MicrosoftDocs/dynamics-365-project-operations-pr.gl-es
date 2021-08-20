---
title: Visión xeral das dimensións de prezos
description: Este tema fornece información sobre as dimensións de prezos en Dynamics 365 Project Operations.
author: rumant
ms.date: 11/30/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 4b3b71c0b64a24f6914c70c4383eee654e7d4947ececaf9b4e6394f45a081a4c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001969"
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

Dynamics 365 Project Operations envíase cun conxunto predefinido de dimensións de prezos. Pode ver estas dimensións de prezos indo a **Project Operations** > **Parámetros**. No rexistro de parámetros, no separador **Dimensións de prezos baseados na cantidade**, verifique que o rol, **msdyn_resourcecategory**, e a unidade organizativa de recursos, **msdyn_organizationalunit** teñan os campos **Aplicable a vendas** e **Aplicable a custo** establecidos en **Si**. Con estes campos activados, pode establecer o prezo e o custo para cada combinación de roles e unidades organizativas.

![Captura de pantalla dos parámetros de Project Service con "Aplicable a vendas" resaltado.](media/PS-OOB-parameters.png)

Se precisa un prezo ou custo para os seus recursos usando atributos adicionais, pode crear campos, entidades e dimensións personalizados. Para obter máis información, consulte os temas seguintes. 
  
  > [!NOTE]
  > Os procedementos deben completarse na orde na que aparecen.

1. [Crear unha solución para as dimensións de prezos personalizadas](../sales/create-solution-custompd.md)
2. [Crear campos e entidades personalizados](create-custom-fields-entities-pricing-dimensions.md)
3. [Engadir campos personalizados á configuración de prezos e ás entidades transaccionais ](add-custom-fields-price-setup-transactional-entities.md)
4. [Configurar campos personalizados como dimensións de prezos ](set-up-custom-fields-pricing-dimensions.md)
5. [Actualizar os atributos do complemento para incluír novas dimensións de prezos](update-plugin-attributes-pd.md)


## <a name="pricing-human-resource-time"></a>Prezos do tempo de recursos humanos
Como unha organización valora o tempo dos recursos humanos é moitas veces unha consideración estratéxica importante que afecta directamente á rendibilidade da organización. Traballe cos equipos financeiros e os responsables de prácticas cando a súa organización estea preparada para identificar como quere configurar os tipos de factura e custos para o tempo de recursos humanos.

Outras consideracións para fixar os prezos inclúen se hai que volver usar campos ou entidades que actualmente non teñen dimensións de prezos pero que se aplican como dimensión de prezos para a súa organización. Campos como **Categoría de transacción** (**msdyn_transactioncategory**) e **Recurso reservable** ( **bookableresource**) son exemplos de dimensións do candidato. 

Considere se a súa dimensión de prezos debe ser unha táboa ou un conxunto de opcións. Se prevé cambios nos valores dunha dimensión que serán máis de 10 ou 12 e necesita atributos adicionais nestes valores, pode crear unha entidade en lugar dun conxunto de opcións. Manter un conxunto de opcións, como engadir ou eliminar valores, require un administrador ou programador, mentres que a adición de novas filas a unha táboa pode facelo a maioría dos usuarios.

O seguinte exemplo mostra os tipos de facturación que se configuran en función do rol e da unidade organizativa de recursos á que pertenza o recurso. As taxas de custo baséanse normalmente na banda salarial do empregado e a unidade organizativa á que pertenza. Neste exemplo, as táboas de taxa de facturación e taxa de custo terán o seguinte aspecto.

**Exemplo de taxas de facturación**

| Rol        | Unidade organizativa    |Unidade      |Prezo      |Moeda  |
| ------------|-------------|----------|----------:|----------|
| Programador   | Contoso EUA  |Hora | 200|USD     |
| Programador   | Contoso India |Hora|   112|USD     |


**Exempo de taxas de custo**

| Banda salarial     | Unidade organizativa    |Unidade      |Prezo      |Moeda  |
| ----------------|-------------|----------|----------:|----------|
| A miña empresa_Banda1 | Contoso EUA  |Hora | 145|USD     |
| A miña empresa_Banda2 | Contoso India |Hora|   67|USD     |


[!INCLUDE[footer-include](../includes/footer-banner.md)]