---
title: Lembrar entradas previamente aprobadas
description: Este tema explica como un membro do equipo do proxecto pode solicitar a retirada dos rexistros de tempo, gastos e uso de material enviados e aprobados previamente, e como un xestor de proxecto pode aprobar ou rexeitar solicitudes de retirada.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 18796e803ff73806aaa60b453048ee3160406b40
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586572"
---
# <a name="recall-previously-approved-entries"></a>Lembrar entradas previamente aprobadas

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Un membro do equipo do proxecto que envíe unha entrada de tempo, gasto ou uso de material pode recordar esa entrada despois de que fose aprobada. O proceso de recuperación ten dous pasos principais:

1. Un solicitante solicita unha recuperación.
2. Un aprobador aproba a solicitude de retirada.

## <a name="request-a-recall"></a>Solicitar unha recuperación

Siga estes pasos para solicitar a retirada das entradas de tempo, gasto ou uso de material aprobados.

1. Siga un destes pasos, dependendo do tipo de entrada que quere recordar:

    - Para as entradas de tempo, vai a **Proxectos** \> **O meu traballo** \> **Entrada horaria**, e seleccione todas as entradas de tempo para unha combinación específica dun proxecto e unha tarefa. Alternativamente, na grade, seleccione as celas individuais para tempo nunha data concreta para un proxecto específico.
    - Para as entradas de gastos, vai a **Proxectos** \> **O meu traballo** \> **Gastos**, e seleccione a fila para recuperar a entrada de gasto.
    - Para as entradas de uso de material, vai a **Proxectos** \> **O meu traballo** \> **Rexistro de uso do material**, e seleccione a fila para a entrada de uso de material para recuperar.

2. Seleccione **Recuperar**. Aparecerá unha caixa de diálogo de confirmación. Se xa se aprobaron as entradas seleccionadas de tempo, gasto ou uso de material, solicitarase que introduza un motivo para a retirada.
3. Insira un motivo para a recuperación e seleccione **Aceptar** para confirmar a operación. O sistema envía á persoa que aprobou as entradas unha solicitude para aprobar a recuperación.

> [!IMPORTANT]
> Non podes crear unha solicitude de retirada para unha entrada de tempo, gasto ou uso de material aprobado que xa se facturara ao cliente. Se o intentas, recibirás unha mensaxe que indica que a entrada de tempo, gasto ou uso de material non se pode recuperar porque xa estaba facturada. Neste caso, pode solicitar a retirada da entrada só se se utiliza unha factura correctora para emitir un crédito ou reembolso completo ao cliente na factura orixinal.

## <a name="approve-or-reject-a-recall-request"></a>Aprobar ou rexeitar unha solicitude de recuperación

Siga estes pasos para aprobar ou rexeitar unha solicitude de recuperación.

1. Vaia a **Proxectos** \> **O meu traballo** \> **Aprobacións**.
2. Na páxina de lista **Aprobacións**, cambie a vista a **Solicitudes de recuperación para aprobación**. Móstrase unha lista de solicitudes de recuperación enviadas.
3. Seleccione unha ou máis entradas e logo seleccione **Aprobar** ou **Rexeitar**.
4. Se seleccionou **Aprobar**, recibirá unha mensaxe de aviso que explica o impacto da aprobación. Seleccione **Aceptar** para confirmar a operación. Apróbase a solicitude de recuperación.

    –ou–

    Se seleccionou **Rexeitar**, a solicitude de recuperación é rexeitada.

> [!IMPORTANT]
> Cando se aproba unha retirada, igual que cando se solicita, o sistema comproba se hai actividade de facturación nas entradas de tempo, gasto ou uso de material. Se xa se facturou unha entrada ou se está nun borrador de factura, o aprobador recibe unha mensaxe de erro que indica que o tempo ou o gasto non se pode aprobar para a súa retirada porque xa se facturou. Neste caso, o aprobador pode aprobar a retirada só se se utiliza unha factura correctiva para emitir un crédito ou reembolso completo ao cliente na factura orixinal.

## <a name="impact-of-a-recall-request"></a>Impacto dunha solicitude de recuperación

Cando se recupera unha aprobación, hai un impacto operativo e financeiro.

### <a name="operational-impact"></a>Impacto operativo

Se se aproba unha solicitude de recuperación, o rexistro de aprobación está marcado como **Rexeitado**. O estado da entrada cámbiase a calquera **Devolto** ou **Rexeitado**, dependendo de se se trata dunha entrada de tempo ou de gasto ou de uso de material.

O membro do equipo do proxecto pode ver entradas, editar e despois enviar de novo entradas ou eliminar entradas por completo.

Se se rexeita unha solicitude de recuperación, o estado da entrada permanece en **Aprobado** e a entrada non pode ser editada polo membro do equipo do proxecto nin polo responsable de aprobacións do proxecto.

### <a name="financial-impact"></a>Impacto financeiro

Se unha solicitude de recuperación é aprobada, os datos reais correspondentes de custo e vendas actualízanse do seguinte xeito:

- O campo **Estado de axuste** actualízase a **Axustado**.
- O campo **Estado de facturación** actualízase a **Cancelado**.

A continuación, créanse entradas de reversión na táboa de Datos reais. Para crear entradas de reversión, o sistema copia sobre os valores de campo a partir dos datos reais orixinais. Os únicos valores que non se copian son os valores de cantidade. Estes valores revértense. Os datos reais revertidos créanse para **Custo** e **Vendas sen facturar**. O campo **Estado de axuste** nos datos reais invertidos establecese en **Inaxustable**, e o campo **Estado de facturación** establécese en **Cancelado**. Debido a estes cambios, o importe que se rexistra como gastado no proxecto e os ingresos acumulados do proxecto xa non contabilizarán as cantidades que representan estes datos reais.

Se se rexeita a solicitude de recuperación, non hai impacto financeiro no proxecto.

## <a name="changes-to-time-entry-records"></a>Cambios nos rexistros de entrada de tempo

A seguinte ilustración mostra os cambios que se producen para as entradas de tempo aprobadas e os rexistros de aprobación correspondentes cando se recuperan.

![Transicións de estado de entrada de tempo.](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-and-material-usage-entry-records"></a>Cambios nos rexistros de entrada de gastos e uso de material

A seguinte ilustración mostra os cambios que se producen para as entradas de gastos e uso de material aprobados e os rexistros de aprobación correspondentes cando son retirados.

![Transicións de estado de entrada de gastos.](media/ExpenseEntryStateTransitions.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
