---
title: Configurar taxas de factura laboral - lite
description: Este tema ofrece información sobre como configurar as taxas de facturación de man de obra en Project Operations.
author: rumant
ms.date: 10/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9b8c4a19260156480e40f2cc26afa83df3ec9fe9de53edc0ad0ca8c7b78bf352
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007594"
---
# <a name="set-up-labor-bill-rates---lite"></a>Configurar taxas de factura laboral - lite

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

Cada lista de prezos ten un conxunto de prezos de rol ou taxas de man de obra que son efectivos para o contexto e a data de vixencia incluídos na cabeceira da lista de prezos. As taxas de facturación por tempo en Dynamics 365 Project Operations pódense configurar só nunha moeda, que é a moeda da cabeceira da lista de prezos.

1. Para configurar as taxas de facturación de man de obra para unha lista de prezos de vendas, cree unha lista de prezos baseada na cabeceira da lista de prezos. 
2. No separador **Prezos de rol**, na subgrade, seleccione **+ Novo prezo de rol**. 
3. No panel **Creación rápida**, introduza a combinación de rol e unidade de organización para a que precisa configurar a taxa de facturación.

  A seguinte táboa inclúe os campos do separador **Xeral** e o panel **Creación rápida** dunha liña de prezos de rol que debe ter en conta ao crear prezos de rol nunha lista de prezos de vendas:

  | Campo | Localización | Descripción | Impacto descendente |
  | --- | --- | --- | --- |
  | Rol | Separador **Xeral** e panel **Creación rápida** | Seleccione o rol para o que está a configurar a taxa de facturación. | O rol na estimación ou dato real entrante compararase con esta liña para predefinir a taxa de facturación do rol. |
  | Unidade de recursos | Separador **Xeral** e panel **Creación rápida** | Seleccione a unidade organizativa ou división da empresa á que pertence o rol. Por exemplo, un programador da división de robótica de Fabrikam India ou un programador da división de software de Fabrikam USA. | A unidade de recursos na estimación ou dato real entrante compararase con esta liña para predefinir a taxa de facturación do rol. |
  | Prezo | Separador **Xeral** e panel **Creación rápida** | Configure a taxa de facturación para a empresa de recursos de rol e a combinación de unidades de recursos. Por exemplo, un programador de Fabrikam India ten unha taxa de facturación de 100 USD ou un programador de Fabrikam USA ten unha taxa de facturación de 150 USD. | Este prezo é a taxa de facturación por defecto no prezo por unidade da liña de estimación ou dato real entrante para unha clase de transacción de Tempo. |
  | Moeda | Separador **Xeral** e panel **Creación rápida**| Por defecto, o valor de moeda procede da moeda da cabeceira da lista de prezos de vendas. Nunha lista de prezos de vendas, a moeda non se pode anular. | Esta moeda é a moeda por defecto do prezo de unidade da liña de dato real de vendas entrante para a clase de transacción de Tempo. |
  | Programación de unidades | Separador **Xeral** e panel **Creación rápida** | Esta programación e unidade é a predefinida en Tempo e non se pode cambiar na entidade de prezo de rol porque se usa para expresar tarifas por unidades de tempo. | Non hai ningún impacto descendente para este campo. |
  | Unidade | Separador **Xeral** e panel **Creación rápida** | O valor de moeda de unidade procede do campo **Unidade de tempo** na cabeceira da lista de prezos de vendas. Pero o valor non se pode anular. Por exemplo, un programador de Fabrikam India ten unha taxa de facturación de 1000 USD por **Día da India**. Un programador de Fabrikam USA ten unha taxa de facturación de 1500 USD por **Día dos EUA**. | Cando o prezo por unidade se predefine nunha liña de estimación ou dato real entrante, o sistema utiliza o sistema de unidades e a conversión en unidades base para calcular un prezo por unidade. Por exemplo, a estimación é un valor de 10 **Días da India** de traballo para un programador da India e a unidade Día da India defínese como 10 horas. Ao fixar o prezo desa liña de estimación, a aplicación calcula o prezo de unidade da estimación como 1000 USD/10 horas = 100 USD por hora. |


## <a name="transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions"></a>Transferir prezos ou configurar tarifas de facturación para recursos doutras unidades organizativas ou divisións 

As empresas baseadas en proxectos deben usar empregados de diferentes divisións da empresa para traballar en proxectos. Os proxectos pódense executar desde unha división mentres que os empregados ou consultores proveñen da mesma división ou dunha división diferente da empresa. O proxecto tamén podería estar formado por unha combinación de persoas de distintas divisións. En Project Operations, a empresa propietaria da entrega do proxecto chámase **Unidade de contratación**. Todas as outras divisións que proporcionan recursos chámanse **Unidades de recursos**. Debido ás diferenzas nos custos laborais entre varias zonas xeográficas e mercados laborais en todo o mundo, as taxas de facturación da man de obra tamén se configuran de xeito diferente para diferentes zonas xeográficas.

Por exemplo, un programador de Fabrikam India que traballa nun proxecto estadounidense factúrase á taxa de 100 USD por hora. Un programador de Fabrikam US que traballa nun proxecto estadounidense factúrase a 150 USD por hora.

### <a name="example-set-up-a-bill-rate"></a>Exemplo: Configurar unha taxa de facturación

1. Cree unha lista de prezos de vendas chamada *Taxas de facturación de Fabrikam US* e configure a vixencia da data.
2. Na lista de prezos de vendas, introduza a seguinte información de taxas:

    | Rol | Unidade organizativa | Taxa de facturación |
    | --- | --- | --- |
    | Programador | Fabrikam India | 100 dólares |
    | Programador | Fabrikam Philippines | 90 $ |
    | Programador | Fabrikam US | 150 $ |

3. Anexe a lista de prezos de vendas, **Taxas de facturación de Fabrikam US** á lista de prezos do contrato do proxecto ou a unha conta determinada.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]