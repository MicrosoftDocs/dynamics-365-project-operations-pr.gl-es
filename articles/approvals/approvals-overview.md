---
title: Visión xeral das aprobacións
description: Este artigo ofrece información sobre como traballar con aprobacións en Project Operations.
author: stsporen
ms.date: 03/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: d5b5c93dc948992505054ef7b17579aafcdf8f8d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924704"
---
# <a name="approvals-overview"></a>Visión xeral das aprobacións

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Os envíos de tempo, gasto e uso de material móvense a través dun fluxo de traballo de aprobación. Despois de que se aproben as entradas, as transaccións rexístranse en datos reais ou o tempo resérvase no programa.

## <a name="approvals-workflow"></a>Fluxo de traballo de aprobacións
Cando crea e envía unha entrada de tempo, gasto ou uso de material, créase un rexistro de aprobación. O responsable de aprobación ou o xestor do proxecto revisa e aproba a entrada. Se a entrada está relacionada cun proxecto, os datos reais crearanse cando se aprobe. Isto permite rastrexar o custo e a facturación.

## <a name="approve-an-entry"></a>Aprobar unha entrada
A páxina **Aprobacións** permite cambiar entre diferentes vistas para que poida ver os diferentes tipos de aprobacións.
  
1. Vaia á páxina **Aprobacións** e seleccione **Gastos**, **Tempo**, **Uso de material** ou **Retiradas**.
2. Revise cada aprobación e seleccione as que desexa aprobar.
3. Seleccione **Aprobar** para aprobar as entradas seleccionadas.
O sistema procesa estas entradas e crea datos reais.

## <a name="reject-an-entry"></a>Rexeitar unha entrada
Como responsable de aprobación do proxecto, é posible que deba devolver unha entrada a un usuario para a súa corrección.
  
1. Vaia á páxina **Aprobacións** e seleccione a entrada para rexeitar. 
2. Seleccione **Rexeitar**.
3. Opcionalmente, engada un comentario na caixa de diálogo **Comentarios de rexeitamento** para informar ao usuario por que se rexeita a entrada.
4. Seleccione **Aceptar**. A entrada devolverase ao usuario.
  
## <a name="cancel-approval"></a>Cancelar aprobación
Nalgúns casos, pode que teña que cancelar unha entrada previamente aprobada. A cancelación dunha entrada previamente aprobada terá un impacto financeiro. 

## <a name="approving-recall-requests"></a>Aprobación de solicitudes de retirada
Nalgúns casos, un consultor pode ter que retirar unha entrada previamente aprobada. A cancelación dunha entrada previamente aprobada terá un impacto financeiro. O responsable de aprobacións do proxecto está obrigado a aprobar a retirada para reverter a transacción en Datos reais.

## <a name="specify-project-approvers"></a>Especificar responsables de aprobación de proxectos
Cada proxecto ten un número de membros do equipo do proxecto. Pode especificar que membros do equipo tamén son responsables de aprobacións do proxecto.

1. Vaia á páxina **Proxectos** e abra o proxecto da lista.
2. No separador **Equipo**, seleccione o membro do equipo que aprobará o proxecto e seleccione **Editar**.
3. Configure o campo **Responsable de aprobación do proxecto** en **Si**.
4. Seleccione **Gardar**.
5. Repita os pasos 2 a 4 para engadir responsables de aprobacións do proxecto adicionais.

## <a name="configure-the-users-manager"></a>Configurar o xestor do usuario

1. Vaia a **Configuración** > **Seguranza** > **Usuarios**.
2. Seleccione o usuario ao que está asignando un xestor e na área **Información da organización** seleccione o xestor da lista. 
3. Seleccione **Gardar**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
