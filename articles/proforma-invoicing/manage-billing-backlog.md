---
title: Xestionar o traballo pendente de facturación
description: Este artigo ofrece información sobre como ver e traballar co atraso de facturación en Project Operations.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 5be05639650bb5b9d646067e8d83bada60824081
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929376"
---
# <a name="manage-billing-backlog"></a>Xestionar o traballo pendente de facturación

**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento

Dynamics 365 Project Operations ten vistas dedicadas para axudar a xestionar o traballo pendente de facturación. Para xestionar o traballo pendente de facturación, seleccione as ligazóns na área **Vendas**, en **Facturación**. 

Están dispoñibles as seguintes vistas:

- Retencións e anticipos
- Anticipos e retencións dispoñibles
- Fitos de prezo fixo
- Traballo pendente de facturación de tempo e material

## <a name="retainers-and-advances"></a>Retencións e anticipos

A vista **Retencións e adiantos** lista as retencións e adiantos en todos os contratos do proxecto. Despois de facturar unha retención ou un adianto, o importe do adianto estará dispoñible para o seu uso.

## <a name="available-retainers-and-advances"></a>Anticipos e retencións dispoñibles

A vista **Retencións e adiantos dispoñibles** lista as todas as retencións e adiantos dispoñibles en todos os contratos do proxecto. Despois de facturar unha retención ou un adianto, o importe do adianto estará dispoñible para o seu uso e engádese á lista. Despois de utilizar por completo o importe da retención ou adianto, elimínase da lista.

## <a name="fixed-price-milestones"></a>Fitos de prezo fixo

A vista **Fitos de prezo fixo** lista todos os fitos de prezo fixo en todas as liñas de contrato do proxecto. Desde esta vista, pódense marcar fitos simples ou múltiples como **Listo para facturar** ou **Non listo para facturar**. Ao marcar un fito como **Listo para facturar** estará dispoñible para poñelo nun borrador de factura.

Cando as liñas de contrato de varios clientes teñen un método de facturación de prezo fixo, créase un fito para cada cliente na liña de contrato. Pódese crear un fito e despois dividilo en rexistros de fitos específicos para cada cliente. Esta división é interna e está de acordo coa porcentaxe de facturación definida para cada cliente na liña de contrato. Na vista **Fitos de prezo fixo**, verá os rexistros de fitos específicos do cliente. Cada un destes rexistros de fitos pódese marcar como **Listo para facturar** separadamente desta vista. Cando un ou máis dos fitos relacionados están marcados como **Listo para facturar**, o estado da cabeceira actualízase a **En curso** desde **Non iniciado**. Cando se facturan todas as divisións do fito, o estado do fito da cabeceira actualízase a **Completado**.

Nesta vista móstrase fito nun borrador de factura cun estado de facturación de **Factura do cliente creada**. Cando se confirma o borrador da factura, actualízase o estado de facturación no rexistro a **Factura do cliente contabilizada**. 

> [!NOTE] 
> Non actualice este valor de estado usando código personalizado. Project Operations non funciona correctamente cando estes valores de estado se actualizan con código personalizado.

## <a name="time-and-material-billing-backlog"></a>Traballo pendente de facturación de tempo e material

A vista **Traballo pendente de facturación de tempo e material** mostra todas as vendas non facturadas de todos os contratos de proxecto no sistema que non se facturaron. Os datos reais de vendas sen facturar simples ou múltiples pódense marcar como **Listo para facturar** ou **Non listo para facturar** desde esta vista. Marcar un dato real de vendas sen facturar como **Listo para facturar** fai que estea dispoñible para poñelo nun borrador de factura.

Os datos reais de vendas non facturadas cun estado **Non exceder** de **Erro** non se poden marcar como **Listo para facturar**. Se hai que marcar os datos reais como **Listo para facturar**, restableza o estado doutros datos reais da liña de contrato comprometidos e, a seguir, avalíe de novo o estado **Non exceder**.

Se as liñas de contrato de varios clientes teñen un método de facturación de tempo e material, cando se aproban o tempo e os gastos, créase un dato real vendas non facturadas para cada cliente na liña de contrato segundo a porcentaxe de facturación dividida definida para cada un dos clientes. Na vista **Traballo pendente de facturación de tempo e material**, verá estes datos de vendas sen facturar específicos para cada cliente. Cada un destes rexistros de datos reais sen facturar pódese marcar como **Listo para facturar** separadamente desta vista.

Nesta vista móstranse as vendas non facturadas que figuran nun borrador de factura cun estado de facturación de **Factura do cliente creada**. Cando se confirma o borrador da factura, o estado de facturación deste rexistro actualízase a **Factura de cliente contabilizada**. 

> [!NOTE] 
> Non actualice este valor de estado usando código personalizado. Project Operations non funciona correctamente cando estes valores de estado se actualizan con código personalizado.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
