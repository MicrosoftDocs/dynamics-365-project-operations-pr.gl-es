---
title: Cancelar a aprobación de entradas previamente aprobadas
description: Este tema explica como un xestor de proxecto pode cancelar a aprobación de entradas de tempo, gastos ou uso de material previamente aprobadas.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 03d4511e85e9fc8d596b269274c4a7e10016244c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584778"
---
# <a name="cancel-the-approval-of-previously-approved-entries"></a>Cancelar a aprobación de entradas previamente aprobadas

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Un director de proxecto ou aprobador que aprobou previamente as entradas de tempo, gasto ou uso de material pode cancelar a súa aprobación desas entradas. 

Siga estes pasos para cancelar a aprobación dunha entrada de tempo, gasto ou uso de material previamente aprobada.

1. Vaia a **Proxectos** \> **O meu traballo** \> **Aprobacións**.
2. O **Aprobacións** A páxina da lista mostra todas as entradas de tempo que están agardando aprobación. Cambia a vista a **As miñas aprobacións pasadas**.
3. Seleccione o tempo, o gasto ou as aprobacións de material para cancelar. A continuación, no Panel de accións, seleccione **Cancelar aprobación**.
4. Na caixa de mensaxe de confirmación que aparece, seleccione **Ok** para confirmar a operación.

> [!IMPORTANT]
> Non pode cancelar a aprobación dunha entrada de tempo, gasto e uso de material previamente aprobada que xa foi facturada ao cliente. Se o intentas, recibirás unha mensaxe que indica que a aprobación non se pode cancelar porque xa estaba facturada. Neste caso, só pode cancelar a aprobación se se utiliza unha factura correctiva para emitir un crédito ou reembolso completo ao cliente na factura orixinal.

## <a name="impact-of-canceling-the-approval-of-a-previously-approved-entry"></a>Impacto da anulación da aprobación dunha entrada previamente aprobada

Cando se cancela unha aprobación, hai un impacto operativo e financeiro.

### <a name="operational-impact"></a>Impacto operativo

Se se cancela a aprobación dunha entrada, o rexistro de aprobación márcase como **Enviado**. O estado da entrada cámbiase a **Enviado**. Nesta fase, un membro do equipo do proxecto pode recordar a entrada sen enviar unha solicitude de retirada.

O aprobador pode cambiar o **Cantidade facturable** e **Tipo de facturación** valores e, a continuación, aprobe a entrada unha vez máis.

### <a name="financial-impact"></a>Impacto financeiro

Se se anula a aprobación dunha entrada, os correspondentes reais de custo e vendas actualízanse do seguinte xeito:

- O campo **Estado de axuste** actualízase a **Axustado**.
- O campo **Estado de facturación** actualízase a **Cancelado**.

A continuación, créanse entradas de reversión na táboa de Datos reais. Para crear entradas de reversión, o sistema copia sobre os valores de campo a partir dos datos reais orixinais. Os únicos valores que non se copian son os valores de cantidade. Estes valores revértense. Os datos reais revertidos créanse para **Custo** e **Vendas sen facturar**. O campo **Estado de axuste** nos datos reais invertidos establecese en **Inaxustable**, e o campo **Estado de facturación** establécese en **Cancelado**. Debido a estes cambios, o importe que se rexistra como gastado no proxecto e os ingresos acumulados do proxecto xa non contabilizarán as cantidades que representan estes datos reais.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
