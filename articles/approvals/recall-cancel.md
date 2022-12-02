---
title: Recuperación de entradas aprobadas previamente
description: Este artigo explica como un membro do equipo do proxecto pode solicitar a retirada dos rexistros de tempo, gastos e uso de material enviados e aprobados anteriormente e como un xestor de proxecto pode aprobar ou rexeitar solicitudes de retirada.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 54fc7ac2301a4423ebf70b0b67ad489580c347b5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930362"
---
# <a name="recall-previously-approved-entries"></a>Recuperación de entradas aprobadas previamente

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Un membro do equipo do proxecto que envíe unha entrada de tempo, gasto ou uso de material pode recuperar esa entrada de tempo ou gasto despois de que foi aprobada. O proceso de recuperación ten dous pasos principais:

1. Un solicitante solicita unha recuperación.
2. Un responsable de aprobación aproba a solicitude de recuperación.

## <a name="request-a-recall"></a>Solicitar unha recuperación

Siga estes pasos para solicitar unha recuperación de entradas de tempo, gasto ou uso de material aprobadas.

1. Siga un destes pasos, dependendo do tipo de entrada que queira recuperar:

    - Para as entradas de tempo, vaia a **Proxectos** \> **O meu traballo** \> **Entrada de tempo** e seleccione todas as entradas de tempo para unha combinación específica dun proxecto e unha tarefa. Alternativamente, na grade, seleccione as celas individuais para tempo nunha data concreta para un proxecto específico.
    - Para as entradas de gasto, vaia a **Proxectos** \> **O meu traballo** \> **Gastos** e seleccione a fila da entrada de gasto para recuperar.
    - Para as entradas de uso de material, vaia a **Proxectos** \> **O meu traballo** \> **Rexistros de uso de material** e seleccione a fila da entrada de uso de material para recuperar.

2. Seleccione **Recuperar**. Aparecerá unha caixa de diálogo de confirmación. Se as entradas de tempo, gasto e uso de material seleccionadas xa foron aprobadas, solicitaráselle que introduza un motivo para a recuperación.
3. Insira un motivo para a recuperación e seleccione **Aceptar** para confirmar a operación. O sistema envía á persoa que aprobou as entradas unha solicitude para aprobar a recuperación.

> [!IMPORTANT]
> Non pode crear unha solicitude de recuperación para unha entrada de tempo, gasto ou uso de material previamente aprobada que xa foi facturada ao cliente. Se o intenta, recibirá unha mensaxe que afirma que non se pode recuperar a entrada de tempo, gasto ou uso de material porque xa foi facturada. Neste caso, só pode solicitar a recuperación da entrada se se utiliza unha factura correctiva para emitir un crédito ou reembolso completo ao cliente sobre a factura orixinal.

## <a name="approve-or-reject-a-recall-request"></a>Aprobar ou rexeitar unha solicitude de recuperación

Siga estes pasos para aprobar ou rexeitar unha solicitude de recuperación.

1. Vaia a **Proxectos** \> **O meu traballo** \> **Aprobacións**.
2. Na páxina de lista **Aprobacións**, cambie a vista a **Solicitudes de recuperación para aprobación**. Móstrase unha lista de solicitudes de recuperación enviadas.
3. Seleccione unha ou máis entradas e logo seleccione **Aprobar** ou **Rexeitar**.
4. Se seleccionou **Aprobar**, recibirá unha mensaxe de aviso que explica o impacto da aprobación. Seleccione **Aceptar** para confirmar a operación. Apróbase a solicitude de recuperación.

    –ou–

    Se seleccionou **Rexeitar**, a solicitude de recuperación é rexeitada.

> [!IMPORTANT]
> Cando se aproba unha recuperación, como cando se solicita, o sistema verifica calquera actividade de facturación nas entradas de tempo, gasto ou uso de material. Se unha entrada xa foi facturada ou se está nun borrador de factura, o responsable de aprobacións recibe unha mensaxe de erro que afirma que o tempo ou gasto non se poden aprobar para a súa recuperación porque xa foi facturado. Neste caso, o responsable de aprobación só pode aprobar a recuperación se se utiliza unha factura correctiva para emitir un crédito ou reembolso completo ao cliente sobre a factura orixinal.

## <a name="impact-of-a-recall-request"></a>Impacto dunha solicitude de recuperación

Cando se recupera unha aprobación, hai un impacto operativo e financeiro.

### <a name="operational-impact"></a>Impacto operativo

Se se aproba unha solicitude de recuperación, o rexistro de aprobación está marcado como **Rexeitado**. O estado da entrada cambia a **Devolto** ou **Rexeitado**, segundo sexa unha entrada de tempo ou unha entrada de gasto ou uso de material.

O membro do equipo do proxecto pode ver as entradas, editar e volver enviar as entradas ou borrar por completo as entradas.

Se se rexeita unha solicitude de recuperación, o estado da entrada permanece en **Aprobado** e a entrada non pode ser editada polo membro do equipo do proxecto nin polo responsable de aprobacións do proxecto.

### <a name="financial-impact"></a>Impacto financeiro

Se unha solicitude de recuperación é aprobada, os datos reais correspondentes de custo e vendas actualízanse do seguinte xeito:

- O campo **Estado de axuste** actualízase a **Axustado**.
- O campo **Estado de facturación** actualízase a **Cancelado**.

A continuación, créanse entradas de reversión na táboa de Datos reais. Para crear entradas de reversión, o sistema copia sobre os valores de campo a partir dos datos reais orixinais. Os únicos valores que non se copian son os valores de cantidade. Estes valores revértense. Os datos reais revertidos créanse para **Custo** e **Vendas sen facturar**. O campo **Estado de axuste** nos datos reais invertidos establecese en **Inaxustable**, e o campo **Estado de facturación** establécese en **Cancelado**. Debido a estes cambios, o importe que se rexistra como gastado no proxecto e os ingresos acumulados do proxecto xa non contabilizarán as cantidades que representan estes datos reais.

Se se rexeita a solicitude de recuperación, non hai impacto financeiro no proxecto.

## <a name="changes-to-time-entry-records"></a>Cambios nos rexistros de entrada de tempo

A seguinte ilustración mostra os cambios que se producen para as entradas de tempo aprobadas e os rexistros de aprobación cando se recuperan.

![Transicións de estado de entradas de tempo.](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-and-material-usage-entry-records"></a>Cambios nos rexistros de entrada de gasto e uso de material

A seguinte ilustración mostra os cambios que se producen para as entradas de gasto e uso de material aprobadas e os rexistros de aprobación cando se recuperan.

![Transicións de estado de entradas de gasto.](media/ExpenseEntryStateTransitions.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
