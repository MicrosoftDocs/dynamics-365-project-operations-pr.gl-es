---
title: Páxina de inicio de dimensións de prezos e custos
description: Este tema ofrece unha visión xeral das dimensións dos prezos.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 425d7bb8-9015-4f67-b9c9-cf3602e9afe8
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 2379d0d2e038f28a1a8df87a851e9bf7db7fe33f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751367"
---
# <a name="pricing-and-costing-dimensions-home-page"></a>Páxina de inicio de dimensións de prezos e custos

As dimensións que se usan en recursos humanos para configurar prezos e custos inclúense en dúas categorías:

- Persoas
- Traballo planificado

Por iso, hai dous tipos de valores de dimensión de prezos dispoñibles en Project Service Automation (PSA): 

- **Conxuntos de opcións** - Dimensións que son enumeracións fixas para un conxunto de valores.
- **Valores baseados en entidades** - Dimensións que poden ser un conxunto variado de valores.

## <a name="pricing-dimensions"></a>Dimensións de prezos

PSA envíase cun conxunto predefinido de dimensións de prezos. Podes velas indo a **Project Service** > **Parámetros**. No rexistro de parámetros, no separador **Dimensións de prezos baseados na cantidade**, verifique que o rol, **msdyn_resourcecategory**, e a unidade organizativa de recursos, **msdyn_organizationalunit** teñan os campos **Aplicable a vendas** e **Aplicable a custo** establecidos en **Si**. Isto permitirá establecer o prezo e o custo para cada combinación de roles e unidades organizativas.

![Captura de pantalla dos parámetros de Project Service con "Aplicable a vendas" resaltado](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> Se estivo a usar os campos listos para usar de rol e unidade organizativa como dimensións de prezos antes da versión 3 de PSA, non haberá ningún cambio observable. Pode seguir usando o Project Service como sempre. 

Se precisa un prezo ou custo para os seus recursos usando atributos adicionais, pode crear campos, entidades e dimensións personalizados. Para obter máis información, consulte os temas seguintes, pero teña en conta que debe completar os procedementos na orde que aparece a continuación:

- [Crear campos e entidades personalizados](create-custom-fields-entities.md)
- [Engadir campos personalizados a configuración de prezos e entidades transaccionais](field-references.md)
- [Configurar campos personalizados como dimensións de prezos](set-up-pricing-dimensions.md)
- [Actualizar os atributos do complemento para incluír novas dimensións de prezos](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a>Prezos do tempo de recursos humanos
Como unha organización valora o tempo dos recursos humanos é moitas veces unha consideración estratéxica importante que afecta directamente á rendibilidade da organización. Traballe cos equipos financeiros e os responsables de prácticas cando a súa organización estea preparada para identificar como quere configurar os tipos de factura e custos para o tempo de recursos humanos.

Outras consideracións para fixar os prezos inclúen se hai que volver usar campos ou entidades que actualmente non teñen dimensións de prezos pero que se aplican como dimensión de prezos para a súa organización. Campos como **Categoría de transacción** (**msdyn_transactioncategory**) e **Recurso reservable** ( **bookableresource**) son exemplos de dimensións do candidato. 

Tamén debe considerar se a súa dimensión de prezos debe ser unha táboa ou un conxunto de opcións. Se prevé cambios nos valores dunha dimensión que serán máis de 10 ou 12 e necesita atributos adicionais nestes valores, pode crear unha entidade en lugar dun conxunto de opcións. Manter un conxunto de opcións, como engadir ou eliminar valores, require un administrador ou programador, mentres que a adición de novas filas a unha táboa pode facelo a maioría dos usuarios.

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
