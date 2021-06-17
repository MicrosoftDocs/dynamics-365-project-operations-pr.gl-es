---
title: Configurar listas de prezos
description: Este tema ofrece información sobre como configurar listas de prezos de custo e venda en Project Operations.
author: rumant
ms.date: 10/20/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 118c2bd6b59b509e5628ac00fc1607809458853b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005024"
---
# <a name="set-up-price-lists"></a>Configurar listas de prezos

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

As listas de prezos en Dynamics 365 Project Operations representan un catálogo de tarifas. As taxas expresan as taxas de custo, vendas e factura. Dependendo de se a lista de prezos expresa taxas de custo ou de vendas e factura, o contexto da lista de prezos é **Vendas** ou **Custo**.

As seguintes extensións son específicas para Project Operations e aplícanse ás listas de prezos de Dynamics 365 Sales.

- **Contexto**: Este campo ten os valores admitidos **Custo** e **Vendas**. O valor **Compra** non se admite. Estableza o contexto en **Custo** para facer unha lista de prezos de custo ou establecer o contexto en **Vendas** para unha lista de prezos de vendas. As listas de prezos de custo resolven o prezo do tipo de custo nos rexistros de estimacións e datos reais. As listas de prezos de vendas resolven o prezo en rexistros estimados e reais dos tipos de vendas non facturadas e facturadas.
- **Unidade de tempo**: Esta é a unidade de tempo predefinida para a que se establece o prezo na táboa **Prezo de rol** relacionada para esta lista de prezos.
- **Entidade de lista de prezos**: Este campo oculto é para que Project Operations diferencie as listas de prezos que son específicas da oferta ou do contrato das que son de aplicación estándar e global.

## <a name="price-list-header"></a>Cabeceira da lista de prezos

A seguinte táboa inclúe os campos do separador **Xeral** dunha lista de prezos exclusiva de Project Operations ou con cambios significativos no comportamento das listas de prezos en Vendas.

| Campo | Localización | Descripción | Impacto descendente |
| --- | --- | --- | --- |
| Nome | Separador **Xeral** e formularios de **Creación rápida** | A identidade da lista de prezos. | A lista de prezos móstrase con este valor en todas as páxinas da lista e opcións despregables.|
| Contexto | Separador **Xeral** e formularios de **Creación rápida** | Este campo pódese configurar como **Custo** ou **Vendas**. | Unha lista de prezos configurada en **Custo** utilízase para buscar o prezo para as estimacións de custos e os datos reais de custo. Unha lista de prezos configurada en **Vendas** utilízase para buscar o prezo para as estimacións de vendas e os datos reais de vendas. Só as listas de prezos que teñen o contexto establecido en **Vendas** poden anexarse a unha lista de prezos do proxecto para clientes, ofertas de proxecto e contratos de proxecto. |
| Data de inicio | Separador **Xeral** e formularios de **Creación rápida** | A data de inicio do período no que esta lista de prezos está vixente. | Co campo **Data de finalización**, este campo úsase para determinar que lista de prezos é aplicable para unha determinada estimación ou liña de datos reais. |
| Data de finalización | Separador **Xeral** e formularios de **Creación rápida** | A data de finalización do período no que esta lista de prezos está vixente. | Co campo **Data de inicio**, este campo úsase para determinar que lista de prezos é aplicable para unha determinada estimación ou liña de datos reais. |
| Moeda | Separador **Xeral** e formularios de **Creación rápida** | Este campo úsase para predefinir a moeda de cada liña de rol, categoría ou elemento da lista de prezos relacionada con esta lista de prezos. | Nas listas de prezos de **Vendas** as liñas de roles, categorías ou de elementos da lista de prezos non se poden crear noutra moeda distinta desta moeda. Nas listas de prezos de **Custo**, pode crear unha liña de prezo de rol en calquera moeda. A moeda aquí definida úsase como predefinida. A configuración do usuario relacionada cos prezos do rol pode anular este valor para permitir a configuración da taxa de custo laboral en calquera moeda. As taxas de custo das categorías e os custos dos elementos da lista de prezos só se poden configurar na moeda aquí definida. |
| Unidade de tempo | Separador **Xeral** e formularios de **Creación rápida** | Este campo úsase para predefinir a unidade de tempo de cada liña de rol relacionada con esta lista de prezos. | Este valor de campo só se usa na configuración do prezo do rol relacionado. Nas listas de prezos de **Custo** e **Vendas**, pode crear unha liña de prezo de rol en calquera unidade de tempo. A unidade de tempo aquí definida úsase como predefinida. A configuración do usuario relacionada cos prezos do rol pode anular este valor para permitir a configuración da taxa de custo laboral e factura en calquera unidade de tempo. |
| Descripción | Separador **Xeral** e formularios de **Creación rápida** | Este campo de texto e permítelle proporcionar unha descrición de varias liñas da lista de prezos. | Este campo móstrase nas vistas **Asociado** na lista de prezos en varias entidades que teñen listas de prezos relacionadas. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]