---
title: Páxina de inicio de dimensións de prezos e custos
description: Este tema ofrece unha visión xeral das dimensións dos prezos.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 137fee27dd2302d47ae12faccde1682cff43db93
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5284131"
---
# <a name="pricing-and-costing-dimensions-home-page"></a>Páxina de inicio de dimensións de prezos e custos

[!include [banner](../includes/psa-now-project-operations.md)]

As dimensións empregadas para fixar os prezos e os custos da man de obra en organizacións baseadas en proxectos están influenciadas polos seguintes atributos:

- Persoas que fan traballos similares á súa experiencia, rol ou zona xeográfica
- Traballo que se realizará de xeito similar á súa complexidade ou hora do día

Dada a natureza típica destes atributos do traballo e das persoas necesarias para realizar o traballo, hai dous tipos de valores de dimensión de prezos dispoñibles en Project Service Automation: 

- **Conxuntos de opcións**: Atributos que son enumeracións fixas para un conxunto de valores.
- **Valores baseados en entidades**: Atributos que poden ter un conxunto variado de valores que son finitos pero que poden cambiar co paso do tempo.

## <a name="pricing-dimensions"></a>Dimensións de prezos

PSA envíase cun conxunto predefinido de dimensións de prezos. Podes velas indo a **Project Service** > **Parámetros**. No rexistro de parámetros, no separador **Dimensións de prezos baseados na cantidade**, verifique que o rol, **msdyn_resourcecategory**, e a unidade organizativa de recursos, **msdyn_organizationalunit** teñan os campos **Aplicable a vendas** e **Aplicable a custo** establecidos en **Si**. Isto permitirá establecer o prezo e o custo para cada combinación de roles e unidades organizativas.

![Captura de pantalla dos parámetros de Project Service con "Aplicable a vendas" resaltado](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> Se estivo a usar os campos listos para usar de rol e unidade organizativa como dimensións de prezos antes da versión 3 de PSA, non haberá ningún cambio observable. Pode seguir usando o Project Service como sempre. 

Se precisa un prezo ou custo para os seus recursos usando atributos adicionais, pode crear campos, entidades e dimensións personalizados. Para obter máis información, consulte os temas seguintes, pero teña en conta que debe completar os procedementos na orde que aparece a continuación:

- [Crear campos e entidades personalizados](create-custom-fields-entities.md)
- [Engadir campos personalizados a configuración de prezos e entidades transaccionais](field-references.md)
- [Configurar campos personalizados como dimensións de prezos ](set-up-pricing-dimensions.md)
- [Actualizar os atributos do complemento para incluír novas dimensións de prezos](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a>Prezos do tempo de recursos humanos
Como unha organización valora o tempo dos recursos humanos é moitas veces unha consideración estratéxica importante que afecta directamente á rendibilidade da organización. Traballe cos equipos financeiros e os responsables de prácticas cando a súa organización estea preparada para identificar como quere configurar os tipos de factura e custos para o tempo de recursos humanos.

Outras consideracións para fixar os prezos inclúen se hai que volver usar campos ou entidades que actualmente non teñen dimensións de prezos pero que se aplican como dimensión de prezos para a súa organización. Campos como **Categoría de transacción** (**msdyn_transactioncategory**) e **Recurso reservable** ( **bookableresource**) son exemplos de dimensións do candidato. 

Considere se a súa dimensión de prezos debe ser unha táboa ou un conxunto de opcións. Se prevé cambios nos valores dunha dimensión que serán máis de 10 ou 12 e necesita atributos adicionais nestes valores, podería crear unha entidade en lugar dun conxunto de opcións. Manter un conxunto de opcións, como engadir ou eliminar valores, require un administrador ou programador, mentres que a adición de novas filas a unha táboa pode facelo a maioría dos usuarios empresariais.

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]