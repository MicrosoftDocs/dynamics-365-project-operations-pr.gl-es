---
title: Xestionar o traballo pendente de facturación
description: Este tema ofrece información sobre como ver e traballar co traballo pendente de facturación en Project Operations.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ec77f3911a460b96414a61bc44ea254f1b7da660
ms.sourcegitcommit: f8edff6422b82fdf2cea897faa6abb51e2c0c3c8
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/21/2020
ms.locfileid: "4087912"
---
# <a name="manage-the-billing-backlog"></a>Xestionar o traballo pendente de facturación

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Dynamics 365 Project Operations ten dúas vistas dedicadas para axudarlle a traballar e xestionar o traballo pendente de facturación. Son **Fitos de prezo fixo** e **Traballo pendente de facturación de tempo e material** Para seleccionar unha vista, na área **Vendas** de Project Operations, na páxina de navegación esquerda, seleccione **Facturación**. As ligazóns de traballo pendente de facturación almacénanse alí.

## <a name="fixed-price-milestones"></a>Fitos de prezo fixo

Esta vista mostra todos os fitos de prezo fixo en todas as liñas de contrato de proxecto no sistema. Os fitos simples ou múltiples pódense marcar como **Listo para facturar** ou **Non listo para facturar** desde esta vista. Cando marca un fito como **Listo para facturar** , o fito está dispoñible para un borrador de factura.

Cando as liñas de contrato de varios clientes teñen un método de facturación de prezo fixo, créase un fito para cada cliente na liña de contrato. O usuario crea un fito e ese fito divídese en rexistros de fitos específicos do cliente internamente, segundo a división da porcentaxe de facturación definida para cada cliente na liña de contrato. Na vista **Fitos de prezo fixo** , verá rexistros de fitos específicos do cliente individual. Cada un destes rexistros de fitos pódese marcar como **Listo para facturar** separadamente desta vista. Cando un ou máis dos fitos relacionados están marcados como **Listo para facturar** , a cabeceira pasa a un estado de **En curso** desde **Non iniciado**. Cando se facturen todas as divisións de fitos, o estado do fito de cabeceira pasa a ser **Completado**.

Nesta vista móstrase fito nun borrador de factura cun estado de facturación de **Factura do cliente creada**. Cando se confirma o borrador da factura, o estado de facturación deste rexistro actualízase a **Factura contabilizada**. Non se recomenda actualizar este valor de estado usando código personalizado. Project Operations non funcionará correctamente se estes valores de estado se actualizan con código personalizado.

## <a name="time-and-material-billing-backlog"></a>Traballo pendente de facturación de tempo e material

Esta vista mostra todos os datos reais de vendas non facturados que non se facturaron en todos os contratos do proxecto no sistema. Os datos reais de vendas sen facturar simples ou múltiples pódense marcar como **Listo para facturar** ou **Non listo para facturar** desde esta vista. Marcar un dato real de vendas sen facturar como **Listo para facturar** fai que estea dispoñible para poñelo nun borrador de factura.

Os datos reais de vendas sen facturar que teñen un estado **Non superable** de **Con erros** non se poden marcar como **Listo para facturar**. Se hai que marcar así estes datos reais, restableza o estado doutros datos reais da liña de contrato que estean confirmados e avalíe o estado **Non superable**.

No caso das liñas de contratos con varios clientes que teñan un método de facturación de tempo e material, cando se aproban o tempo e os gastos, créanse vendas reais non facturadas para cada cliente na liña de contrato segundo a división da porcentaxe de facturación definida para cada cliente na liña de contrato. Na vista **Traballo pendente de facturación de tempo e material** , verá estes datos de vendas sen facturar específicos do cliente individual. Cada un destes rexistros de datos reais sen facturar pódese marcar como **Listo para facturar** separadamente desta vista.

Nesta vista móstrase un dato real de vendas sen facturar nun borrador de factura cun **Estado de facturación** de **Factura do cliente creada**. Cando se confirma o borrador da factura, o estado de facturación deste rexistro actualízase a **Factura de cliente contabilizada**. Non se recomenda actualizar este valor de estado cando está neste estado usando código personalizado. Project Operations non funcionará correctamente cando estes valores de estado se actualicen con código personalizado.