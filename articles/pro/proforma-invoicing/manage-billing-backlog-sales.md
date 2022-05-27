---
title: Xestionar o traballo pendente de facturación de proxecto
description: Este tema ofrece información sobre as distintas vistas dispoñibles para usar ao xestionar o traballo pendente de facturación en proxectos.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b3a90d50fcca8824db10594352cbd1e204665c53
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578139"
---
# <a name="manage-project-billing-backlog"></a>Xestionar o traballo pendente de facturación de proxecto 

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

Dynamics 365 Project Operations ten vistas dedicadas para axudar a xestionar o traballo pendente de facturación. Para xestionar o traballo pendente de facturación, seleccione as ligazóns na área **Vendas**, en **Facturación**. 

Están dispoñibles as seguintes vistas:

- Retencións e anticipos
- Anticipos e retencións dispoñibles
- Fitos de prezo fixo
- Traballo pendente de facturación de produtos
- Traballo pendente de facturación de tempo e material

## <a name="retainers-and-advances"></a>Retencións e anticipos

A vista **Retencións e adiantos** mostra todas as retencións e adiantos en todos os contratos de proxecto do sistema. Despois de facturar unha retención ou un adianto, o importe do adianto estará dispoñible para o seu uso.

## <a name="available-retainers-and-advances"></a>Anticipos e retencións dispoñibles

A vista **Retencións e adiantos dispoñibles** mostra todas as retencións e adiantos dispoñibles en todos os contratos de proxecto do sistema. Despois de facturar unha retención ou un adianto, o importe do adianto estará dispoñible para o seu uso e engádese á lista. Despois de usar por completo o importe da retención ou adianto, elimínase da lista.

## <a name="fixed-price-milestones"></a>Fitos de prezo fixo

A vista **Fitos de prezo fixo** mostra todos os fitos de prezo fixo en todas as liñas de contrato de proxecto no sistema. Os fitos simples ou múltiples pódense marcar como **Listo para facturar** ou **Non listo para facturar** desde esta vista. Ao marcar un fito como **Listo para facturar** estará dispoñible para poñelo nun borrador de factura.

Cando as liñas de contrato de varios clientes teñen un método de facturación de prezo fixo, créase un fito para cada cliente na liña de contrato. Pódese crear un fito e despois dividilo en rexistros de fitos específicos para cada cliente. Esta división é interna e está de acordo coa porcentaxe de facturación definida para cada cliente na liña de contrato. Na vista **Fitos de prezo fixo**, verá os rexistros de fitos específicos do cliente. Cada un destes rexistros de fitos pódese marcar como **Listo para facturar** separadamente desta vista. Cando un ou máis dos fitos relacionados están marcados como **Listo para facturar**, o estado da cabeceira actualízase a **En curso** desde **Non iniciado**. Cando se facturan todas as divisións de fitos, o estado do fito de cabeceira actualízase a **Completado**.

Nesta vista móstrase fito nun borrador de factura cun estado de facturación de **Factura do cliente creada**. Cando se confirma o borrador da factura, actualízase o estado de facturación no rexistro a **Factura do cliente contabilizada**. Non actualice este valor de estado usando código personalizado. Project Operations non funciona correctamente cando estes valores de estado se actualizan con código personalizado.

## <a name="product-billing-backlog"></a>Traballo pendente de facturación de produtos

A vista **Traballo pendente de facturación de produtos** mostra todas as liñas de contrato baseado en produtos en todos os contratos de proxecto do sistema. As liñas de contrato baseado en produto simples ou múltiples pódense marcar como **Listo para facturar** ou **Non listo para facturar** desde esta vista. Ao marcar unha liña de contrato baseado en produto como **Listo para facturar** estará dispoñible para poñela nun borrador de factura.

Nesta vista móstrase unha liña de contrato baseado en produto que figura nun borrador de factura cun estado de facturación de **Factura de cliente creada**. Cando se confirma o borrador da factura, o estado de facturación deste rexistro actualízase a **Factura de cliente contabilizada**. Non actualice este valor de estado usando código personalizado. Project Operations non funciona correctamente cando estes valores de estado se actualizan con código personalizado.

## <a name="time-and-material-billing-backlog"></a>Traballo pendente de facturación de tempo e material

A vista **Traballo pendente de facturación de tempo e material** mostra todas as vendas non facturadas de todos os contratos de proxecto no sistema que non se facturaron. Os datos reais de vendas sen facturar simples ou múltiples pódense marcar como **Listo para facturar** ou **Non listo para facturar** desde esta vista. Marcar un dato real de vendas sen facturar como **Listo para facturar** fai que estea dispoñible para poñelo nun borrador de factura.

Os datos reais de vendas non facturadas cun estado **Non exceder** de **Erro** non se poden marcar como **Listo para facturar**. Se hai que marcar os datos reais como **Listo para facturar**, restableza o estado doutros datos reais da liña de contrato comprometidos. e logo avalíe de novo o estado **Non exceder**.

Se as liñas de contrato de varios clientes teñen un método de facturación de tempo e material, cando se aproban o tempo e os gastos, créase un dato real vendas non facturadas para cada cliente na liña de contrato segundo a porcentaxe de facturación dividida definida para cada un dos clientes. Na vista **Traballo pendente de facturación de tempo e material**, verá estes datos de vendas sen facturar específicos para cada cliente. Cada un destes rexistros de datos reais sen facturar pódese marcar como **Listo para facturar** separadamente desta vista.

Un dato real de vendas sen facturar que figura nun borrador de factura cun estado de facturación de **Factura de cliente creada**. Cando se confirma o borrador da factura, o estado de facturación deste rexistro actualízase a **Factura de cliente contabilizada**. Non actualice este valor de estado usando código personalizado. Project Operations non funciona correctamente cando estes valores de estado se actualizan con código personalizado.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
