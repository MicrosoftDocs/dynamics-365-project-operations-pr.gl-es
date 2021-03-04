---
title: Visión xeral das aprobacións
description: Este tema ofrece información sobre como traballar con aprobacións en Project Operations.
author: stsporen
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 14c6914cf9b5fb52e7554e51604e79f0920064df
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123826"
---
# <a name="approvals-overview"></a>Visión xeral das aprobacións

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Os envíos de tempo e gasto pasan por un fluxo de traballo de aprobación. Despois de que se aproben as entradas, as transaccións rexístranse en datos reais ou o tempo resérvase no programa.

## <a name="approvals-workflow"></a>Fluxo de traballo de aprobacións
Cando crea e envía unha entrada de tempo ou gasto, créase unha entrada de aprobación. O responsable de aprobación do proxecto ou o seu xestor revisa e aproba a súa entrada. Se a entrada está relacionada cun proxecto, cando se aprobe, crearanse os datos reais. Isto permite rastrexar o custo e a facturación. 

## <a name="approve-an-entry"></a>Aprobar unha entrada
O formulario **Aprobacións** permítelle cambiar entre diferentes vistas para que poida ver os diferentes tipos de aprobacións.
  
1. Vaia ao formulario **Aprobacións** e seleccione **Gastos**, **Tempo** ou **Recuperacións**.
2. Revise cada aprobación e seleccione as que desexa aprobar.
3. Seleccione **Aprobar** para aprobar as entradas seleccionadas.
O sistema procesará estas entradas e creará datos reais ou unha reserva.

## <a name="reject-an-entry"></a>Rexeitar unha entrada
Como responsable de aprobación do proxecto, é posible que deba devolver unha entrada a un usuario para a súa corrección.
  
1. Vaia ao formulario **Aprobacións** e seleccione a entrada para rexeitar. 
2. Seleccione **Rexeitar**.
3. Opcional - Engada un comentario no diálogo **Comentarios de rexeitamento** para informar ao usuario de por que se rexeita a entrada.
4. Seleccione **Aceptar**. A entrada devolverase ao usuario.
  
## <a name="recall-entries"></a>Recuperar entradas
Nalgún momento, é posible que teña que recuperar unha entrada enviada. Se a entrada non foi aprobada, devolverase inmediatamente. Non obstante, unha entrada aprobada pode ter un impacto substancial. O responsable de aprobacións do proxecto está obrigado a aprobar a recuperación para reverter a transacción en Datos reais.

## <a name="specify-project-approvers"></a>Especificar responsables de aprobación de proxectos
Cada proxecto ten un número de membros do equipo do proxecto. Pode especificar que membros do equipo tamén son responsables de aprobacións do proxecto.

1. Vaia ao formulario **Proxectos** e abra o proxecto desde a lista.
2. No separador **Equipo**, seleccione o membro do equipo que aprobará o proxecto e seleccione **Editar**.
3. Configure o campo **Responsable de aprobación do proxecto** en **Si**.
4. Seleccione **Gardar**.
5. Repita os pasos 2 a 4 para engadir responsables de aprobacións do proxecto adicionais.

## <a name="configure-the-users-manager"></a>Configurar o xestor do usuario

1. Vaia a **Configuración** > **Seguranza** > **Usuarios**.
2. Seleccione o usuario ao que está asignando un xestor e na área **Información da organización** seleccione o xestor da lista. 
3. Seleccione **Gardar**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]