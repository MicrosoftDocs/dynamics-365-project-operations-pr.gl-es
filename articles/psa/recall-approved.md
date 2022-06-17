---
title: Recuperar entradas de tempo ou gasto aprobadas previamente
description: Este artigo ofrece información sobre como recuperar unha transacción de tempo ou gasto previamente aprobada.
author: rumant
ms.custom: ''
ms.author: rumant
ms.date: 03/08/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: e106ee8734a7c4986693aa06ce6a3b7349a27ac4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910722"
---
# <a name="recall-approved-time-or-expense-entries"></a>Recuperar entradas de tempo ou gasto aprobadas previamente

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Un membro do equipo do proxecto ou outra persoa que envíe unha entrada de tempo ou gasto pode lembrar esa entrada de tempo ou gasto despois de que foi aprobada. O proceso para recuperar unha entrada de tempo ou gasto aprobada ten dous pasos:

1. Un solicitante solicita unha recuperación.
2. Un responsable de aprobación aproba a recuperación.

## <a name="request-a-recall"></a>Solicitar unha recuperación

Siga estes pasos para solicitar unha recuperación dunha entrada de tempo ou gasto que aprobada.

1. Para as entradas de tempo, vaia a **Proxectos** \> **O meu traballo** \> **Entrada de tempo**.

    –ou–

    Para as entradas de gasto, vaia a **Proxectos** \> **O meu traballo** \> **Gastos**.

2. Para as entradas de tempo, seleccione todas as entradas de tempo para unha combinación específica dun proxecto e unha tarefa. Alternativamente, na grade, seleccione as celas individuais para tempo nunha data concreta para un proxecto específico.

    –ou–

    Para as entradas de gasto, seleccione a fila da entrada de gasto para recuperar.

3. Seleccione **Recuperar**. Aparecerá unha caixa de diálogo de confirmación. Se as entradas de tempo e gasto seleccionadas xa foron aprobadas, solicitaráselle que introduza un motivo para a recuperación.
4. Insira un motivo para a recuperación e seleccione **Aceptar** para confirmar a operación. O sistema envía á persoa que aprobou as entradas unha solicitude para aprobar a recuperación.

> [!NOTE]
> Aínda que se poden recuperar as entradas de tempo e gasto aprobadas, se xa se facturou ao cliente un tempo ou gasto aprobado, non se pode crear unha solicitude de recuperación. Un usuario que intente crear unha solicitude de recuperación recibirá unha mensaxe que afirma que non se pode recuperar o tempo nin o gasto porque xa foi facturado.

## <a name="approve-or-reject-a-recall-request"></a>Aprobar ou rexeitar unha solicitude de recuperación

Siga estes pasos para aprobar ou rexeitar unha solicitude de recuperación.

1. Vaia a **Proxectos** \> **O meu traballo** \> **Aprobacións**.
2. Na páxina de lista **Aprobacións**, cambie a vista a **Solicitudes de recuperación para aprobación**. Móstrase unha lista de solicitudes de recuperación enviadas.
3. Seleccione unha ou máis entradas e logo seleccione **Aprobar** ou **Rexeitar**.
4. Se seleccionou **Aprobar**, recibirá unha mensaxe de aviso que explica o impacto da aprobación. Seleccione **Aceptar** para confirmar a operación. Apróbase a solicitude de recuperación.

    –ou–

    Se seleccionou **Rexeitar**, a solicitude de recuperación é rexeitada.

> [!NOTE]
> Como cando se solicita unha recuperación, cando se aproba unha recuperación, o sistema verifica calquera actividade de facturación nas entradas de tempo ou gasto. Se unha entrada xa foi facturada ou se está nun borrador de factura, o responsable de aprobacións recibirá unha mensaxe de erro que afirma que o tempo ou gasto non se poden aprobar para a súa recuperación porque xa foi facturado.

## <a name="impact-of-a-recall-request"></a>Impacto dunha solicitude de recuperación

Cando se recupera unha aprobación, hai un impacto operativo e financeiro.

### <a name="operational-impact"></a>Impacto operativo

Se se aproba unha solicitude de recuperación, o rexistro de aprobación está marcado como **Rexeitado**. O estado da entrada cambia a **Devolto** ou **Rexeitado**, segundo sexa unha entrada de tempo ou unha entrada de gasto.

O membro do equipo do proxecto pode ver as entradas, editar e volver enviar as entradas ou borrar por completo as entradas.

Se se rexeita unha solicitude de recuperación, o estado da entrada permanece en **Aprobado** e a entrada non pode ser editada polo membro do equipo do proxecto nin polo responsable de aprobacións do proxecto.

### <a name="financial-impact"></a>Impacto financeiro

Se unha solicitude de recuperación é aprobada, os datos reais correspondentes de custo e vendas actualízanse do seguinte xeito:

- O campo **Estado de axuste** actualízase a **Axustado**.
- O campo **Estado de facturación** actualízase a **Cancelado**.

A continuación, créanse entradas de reversión na táboa de Datos reais. Para crear entradas de reversión, o sistema copia sobre os valores de campo a partir dos datos reais orixinais. Os únicos valores que non se copian son os valores de cantidade. Estes valores revértense. Os datos reais revertidos créanse para **Custo** e **Vendas sen facturar**. O campo **Estado de axuste** nos datos reais invertidos establecese en **Inaxustable**, e o campo **Estado de facturación** establécese en **Cancelado**. Debido a estes cambios, o importe que se rexistra como gastado no proxecto e os ingresos acumulados do proxecto xa non contabilizarán as cantidades que representan estes datos reais.

Se se rexeita a solicitude de recuperación, non hai impacto financeiro no proxecto.

## <a name="changes-to-time-entry-records"></a>Cambios nos rexistros de entrada de tempo

A seguinte ilustración mostra os cambios que se producen para as entradas de tempo aprobadas cando se recuperan.

![Transicións de estado de entradas de tempo.](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-entry-records"></a>Cambios nos rexistros de entrada de gasto

A seguinte ilustración mostra os cambios que se producen para as entradas de gasto aprobadas cando se recuperan.

![Transicións de estado de entradas de gasto.](media/ExpenseEntryStateTransitions.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
