---
title: Cancelar a aprobación de entradas aprobadas previamente
description: Este artigo explica como un xestor de proxecto pode cancelar a aprobación de entradas de tempo, gasto ou uso de material previamente aprobadas.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 08c2248a5fcfc9b7569871a76bc09234ffd172c7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930454"
---
# <a name="cancel-the-approval-of-previously-approved-entries"></a>Cancelar a aprobación de entradas aprobadas previamente

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Un xestor de proxecto ou un responsable de aprobación que aprobou previamente entradas de tempo, gasto ou uso de material pode cancelar a aprobación desas entradas de tempo. 

Siga estes pasos para cancelar a aprobación dunha entrada de tempo, gasto ou uso de material aprobada anteriormente.

1. Vaia a **Proxectos** \> **O meu traballo** \> **Aprobacións**.
2. A páxina de lista **Aprobacións** mostra todas as entradas de tempo que están agardando aprobación. Cambie a vista a **As miñas aprobacións pasadas**.
3. Seleccione as aprobacións de tempo, gasto ou material para cancelar. A continuación, no panel Acción, seleccione **Cancelar aprobación**.
4. Na caixa de mensaxe de confirmación que apareza, seleccione **Aceptar** para confirmar a aprobación.

> [!IMPORTANT]
> Non pode cancelar a aprobación dunha entrada de tempo, gasto e uso de material previamente aprobada que xa foi facturada ao cliente. Se o intenta, recibirá unha mensaxe que indica que a aprobación non se pode cancelar porque xa estaba facturada. Neste caso, só pode cancelar a aprobación se se utiliza unha factura correctiva para emitir un crédito ou reembolso completo ao cliente sobre a factura orixinal.

## <a name="impact-of-canceling-the-approval-of-a-previously-approved-entry"></a>Impacto de cancelar a aprobación dunha entrada previamente aprobada

Cando se cancela unha aprobación, hai un impacto operativo e financeiro.

### <a name="operational-impact"></a>Impacto operativo

Se se cancela a aprobación dunha entrada, o rexistro de aprobación márcase como **Enviado**. O estado da entrada cámbiase a **Enviado**. Nesta fase, un membro do equipo do proxecto pode retirar a entrada sen enviar unha solicitude de retirada.

O responsable de aprobación pode cambiar os valores de **Cantidade facturable** e **Tipo de facturación** e, a seguir, aprobar a entrada unha vez máis.

### <a name="financial-impact"></a>Impacto financeiro

Se se cancela a aprobación dunha entrada, os datos reais correspondentes de custo e vendas actualízanse do seguinte xeito:

- O campo **Estado de axuste** actualízase a **Axustado**.
- O campo **Estado de facturación** actualízase a **Cancelado**.

A continuación, créanse entradas de reversión na táboa de Datos reais. Para crear entradas de reversión, o sistema copia sobre os valores de campo a partir dos datos reais orixinais. Os únicos valores que non se copian son os valores de cantidade. Estes valores revértense. Os datos reais revertidos créanse para **Custo** e **Vendas sen facturar**. O campo **Estado de axuste** nos datos reais invertidos establecese en **Inaxustable**, e o campo **Estado de facturación** establécese en **Cancelado**. Debido a estes cambios, o importe que se rexistra como gastado no proxecto e os ingresos acumulados do proxecto xa non contabilizarán as cantidades que representan estes datos reais.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
