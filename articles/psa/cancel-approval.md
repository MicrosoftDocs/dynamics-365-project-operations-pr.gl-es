---
title: Cancelar as entradas de tempo e gasto aprobadas previamente
description: Este tema fornece información sobre como cancelar unha transacción de tempo e gasto de proxecto aprobada.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 0ea816040570cc8f6ddf3c5ec8a74ac092fc68b2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076307"
---
# <a name="cancel-previously-approved-time-or-expense-entries"></a>Cancelar as entradas de tempo ou gasto aprobadas previamente

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Na última versión de Dynamics 365 Project Service Automation, os responsables de aprobacións poden cancelar as entradas de tempo ou gasto que aprobaron previamente.

## <a name="cancel-a-previously-approved-time-or-expense-entry"></a>Cancelar una entrada de tempo ou gasto aprobada previamente

Siga estes pasos para cancelar unha entrada de tempo ou gasto que aprobou anteriormente.

1. Vaia a **Proxectos** \> **O meu traballo** \> **Aprobacións**.
2. Na páxina de lista **Aprobacións** , cambie a vista a **As miñas aprobacións pasadas**. Móstrase unha lista das entradas de tempo e gasto que aprobou anteriormente.
3. Seleccione unha ou máis entradas e logo seleccione **Cancelar a aprobación**. Recibirá unha mensaxe de aviso.
4. Para cancelar a aprobación, seleccione **Aceptar**.

## <a name="understand-the-impact-of-canceling-a-time-or-expense-entry-approval"></a>Comprender o impacto da cancelación dunha aprobación de entrada de tempo ou gasto

Cando se cancela unha aprobación, hai un impacto operativo e financeiro.

### <a name="operational-impact"></a>Impacto operativo

No lado das operacións, cando se cancela unha aprobación, o estado do rexistro restablécese a **Borrador** e a aprobación xa non aparece na vista **As miñas aprobacións pasadas**. Pola contra, a aprobación cancelada aparece na vista **Entradas de tempo para aprobación** ou na vista **Entradas de gasto para aprobación** , dependendo de se era unha entrada de tempo ou unha entrada de gasto. Ademais, o estado da entrada de tempo ou de gasto relacionada cambia a **Enviada** para que a entrada relacionada sexa coherente coas aprobacións que teñan un estado de **Borrador**.

Como responsable de aprobacións, pode editar algúns dos campos dunha aprobación que teña un estado de **Borrador**. Estes campos inclúen **Tipo de facturación** e **Horas facturables para entradas de tempo**. Despois de facer os cambios, pode aprobar o rexistro de novo. Alternativamente, pode rexeitar a entrada. Se rexeita a aprobación dunha entrada de tempo, o estado da entrada cambia a **Devolto**. Se rexeita a aprobación dunha entrada de gasto, o estado da entrada cambia a **Rexeitado**. Funcionalmente, as entradas devoltas e rexeitadas compórtanse igual que unha entrada co estado de **Borrador**. Un membro do equipo do proxecto pode facer calquera cambio necesario na entrada e logo enviala de novo para a súa aprobación ou ben eliminar a entrada por completo.

### <a name="financial-impact"></a>Impacto financeiro

Un proxecto tamén se ve afectado financeiramente cando se cancela unha aprobación. En primeiro lugar, os datos reais correspondentes de custo e vendas actualízanse do seguinte xeito:

- O estado de axuste está definido en **Axustado**.
- O estado de facturación está definido en **Cancelado**.

A continuación, créanse entradas de reversión na táboa de Datos reais. Para crear entradas de reversión, o sistema copia sobre os valores de campo a partir dos datos reais orixinais. Os únicos valores que non se copian son os valores de cantidade. Estes valores revértense. Os datos reais revertidos créanse para **Custo** e **Vendas sen facturar**. O campo **Estado de axuste** nos datos reais revertidos está definido en **Inaxustable** e o estado de facturación está definido en **Cancelado**.

Despois de realizar estes cambios, o importe que se rexistra como gastado no proxecto e os ingresos acumulados do proxecto contabilizarán as cantidades que representan estes datos reais.