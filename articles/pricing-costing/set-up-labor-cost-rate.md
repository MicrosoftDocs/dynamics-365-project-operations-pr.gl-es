---
title: Configurar taxas de custo laboral
description: Este tema ofrece información sobre como configurar as taxas de custo de man de obra en Project Operations
author: rumant
manager: Annbe
ms.date: 10/12/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d17f266b6e34fc2a2743fe19fd18b15fb992ceef
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076029"
---
# <a name="set-up-labor-cost-rates"></a>Configurar taxas de custo laboral

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_


Cada lista de prezos ten un conxunto de taxas de man de obra (prezos de rol) que se aliñan co contido e a data de vixencia da lista de prezos.

1. Cree unha lista de prezos no separador **Prezo de rol** , na subgrade, seleccione **Novo rol**.
2. Na páxina **Creación rápida** , seleccione o rol e a unidade organizativa.
3. Introduza calquera outra información de campo necesaria.

A seguinte táboa inclúe algúns dos campos que son importantes á hora de crear taxas de man de obra nunha lista de prezos de custo.

| Campo | Localización | Relevancia, finalidade e orientación | Impacto descendente |
| --- | --- | --- | --- |
| Rol | Separador **Xeral** e páxinas de **Creación rápida** | Seleccione o rol á que se aplica a taxa de custo. | O rol na estimación ou dato real entrante compararase con esta liña para predefinir o custo do rol. |
| Empresa de recursos | Separador **Xeral** e páxinas de **Creación rápida** | Seleccione a entidade legal á que está atribuído o rol. Por exemplo, un programador de Fabrikam India ou un programador de Fabrikam USA. | A empresa de recursos na estimación ou dato real entrante compararase con esta liña para predefinir a taxa de custo do rol. |
| Unidade de recursos | Separador **Xeral** e páxinas de **Creación rápida** | Seleccione a unidade organizativa ou división da empresa desde a que se usará este rol. Por exemplo, un programador da división de robótica de Fabrikam India ou un programador da división de software de Fabrikam USA. | A unidade de recursos na estimación ou dato real entrante compararase con esta liña para predefinir o custo do rol. |
| Prezo | Separador **Xeral** e páxinas de **Creación rápida** | Configure o custo para a combinación de rol, empresa de recursos e unidad de recursos. Por exemplo, un programador de Fabrikam India custa 1000 INR ou un programador de Fabrikam USA custa 150 USD. | O prezo é a taxa de custo por defecto no custo por unidade da estimación entrante ou da liña de dato real para unha clase de transacción de **Tempo**. |
| Moeda | Separador **Xeral** e páxinas de **Creación rápida** | Por defecto, o valor de moeda procede da moeda da cabeceira da lista de prezos de custo pero se pode anular. Por exemplo, un programador de Fabrikam India custa 1000 INR. Un programador de Fabrikam USA custa 150 USD. | Esta moeda predefínese no custo por unidade da liña de custo real entrante para a clase de transacción de **Tempo**. Nunha estimación de proxecto, o valor da moeda convértese á moeda do proxecto e móstrase na vista temporal da estimación. |
| Programación de unidades | Separador **Xeral** e páxinas de **Creación rápida** | A programación de unidade é a predefinida en Tempo e non se pode cambiar na entidade de prezo de rol porque se usa para expresar taxas por unidades de tempo. | Non se produce un impacto descendente. |
| Unidade | Separador **Xeral** e páxinas de **Creación rápida** | Por defecto, o valor procede do campo **Unidade de tempo** na cabeceira da lista de prezos de custo. O valor non se pode anular. Por exemplo, un programador de Fabrikam India custa 1000 INR por **Día da India**. Un programador de Fabrikam USA custa 150 USD por **Día dos EUA**. | O sistema utiliza o sistema de unidades e a conversión en unidades base para computar un custo por unidade para calcular o prezo por unidade predefinido nunha liña de estimación ou dato real entrante. Por exemplo, a estimación é un valor de 10 **Días da India** de traballo para un programador da India e a unidade **Día da India** defínese como 10 horas. Ao fixar o custo desa liña de estimación, a aplicación calcula o custo de unidade da estimación como: 1000 INR/10 horas = 100 INR por hora, que se converte en USD e se mostra como o custo de unidade na páxina **Estimacións do proxecto**. |

## <a name="transfer-pricing-and-costs-for-resources-outside-of-your-division-or-legal-entity"></a>Transferir prezos e custos para recursos fóra da súa división ou entidade legal

As empresas baseadas en proxectos é frecuente usar empregados de diferentes entidades legais ou divisións en proxectos. Un proxecto pode ser executado por unha entidade legal, pero os empregados ou consultores que traballan no proxecto poderían proceder da mesma entidade legal e división ou doutra diferente, ou pode haber unha combinación de ambas. En Dynamics 365 Project Operations, a entidade legal propietaria da entrega do proxecto é a **Empresa propietaria** e a división propietaria da entrega é a **Unidade de Contratación**. Outras entidades legais que proporcionan recursos son as **Empresas de recursos** e as divisións que proporcionan recursos son as **Unidades de recursos**. Na maioría dos países, as empresas están obrigadas a garantir que a entidade legal ou a división de recursos cobran á empresa propietaria e á unidade contratante polo uso dos recursos.

Por exemplo, a corporación Fabrikam debe asegurarse de que Fabrikam India-Robotics negocie unha taxa de custo con Fabrikam US-Robotics ou Fabrikam UK-Robotics.

Un programador de Fabrikam India-Robotic cobra 100 $ cando se lle presta a Fabrikam US-Robotics e 150 $ cando se lle presta a Fabrikam UK-Robotics.

### <a name="set-up-costs-for-outside-resources"></a>Configurar custos para recursos externos

1. Cree unha lista de prezos de custo chamada *Taxas de custos de Fabrikam US-Robotics* e defina un intervalo de vixencia de datas.
2. Na lista de prezos de custo, configure tarifas utilizando a información da seguinte táboa. 

| Rol | Empresa de recursos | Unidade de recursos | Taxa de custo |
| --- | --- | --- | --- |
| Programador | Fabrikam India | Fabrikam India-Robotics | 100 dólares |
| Programador | Fabrikam Philippines | Fabrikam Philippines-Robotics | 90 $ |
| Programador | Fabrikam EE. UU. | Fabrikam US-Robotics | 150 $ |

3. Anexe esta lista de prezos de custo á unidade organizativa Fabrikam US-Robotics.

### <a name="set-up-transfer-pricing-for-a-resource-in-the-appropriate-currency"></a>Configure os prezos de transferencia dun recurso na moeda adecuada 

En Project Operations, o prezo dos recursos pódese configurar en calquera moeda. A moeda predefinida é a que figura na cabeceira da lista de prezos, pero pódese cambiar.

Usando o exemplo para a configuración do prezo de transferencia, a información podería cambiar a:

A corporación Fabrikam debe asegurarse de que Fabrikam India-Robotics negocie unha taxa de custo con Fabrikam US-Robotics ou Fabrikam UK-Robotics.

Un programador de Fabrikam India-Robotics custa 5000 INR cando se lle presta a Fabrikam US-Robotics e 5500 INR cando se lle presta a Fabrikam UK-Robotics.

Na lista de prezos de custo de Fabrikam US-Robotics, as taxas de custo pódense expresar como:

| Rol | Empresa de recursos | Custo |
| --- | --- | --- |
| Programador | Fabrikam India | 5000 INR |
| Programador | Fabrikam US | 115 USD |

Na lista de prezos de custo de Fabrikam UK-Robotics, as taxas de custo pódense expresar como:

| Rol | Empresa de recursos | Custo |
| --- | --- | --- |
| Programador | Fabrikam India | 5500 INR |
| Programador | Fabrikam UK | 115 GBP |

A lista de prezos de custo pode proporcionar taxas de man de obra en moedas múltiples. Ao xerar unha estimación do custo do proxecto, Project Operations converterá estas taxas de custo na moeda do proxecto e mostrarana ao usuario. Cando se aproba unha entrada de tempo e se crea un dato real de custo, o dato real de custo ten un prezo na moeda desa liña de prezo de rol coincidente na lista de prezos de custo. Os datos reais de custo por tempo nun mesmo proxecto pódense rexistrar en varias moedas. Non obstante, ao acumular ou resumir os custos reais de man de obra a nivel de proxecto, as Project Operations converterá todos os custos de man de obra na moeda do proxecto que o usuario pode ver.
