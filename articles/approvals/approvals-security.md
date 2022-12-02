---
title: Seguridade e aprobacións
description: Este artigo ofrece información sobre a configuración de seguranza para traballar con aprobacións en Microsoft Dynamics 365 Project Operations.
author: stsporen
ms.date: 08/29/2022
ms.topic: security
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 0dcadaa142bf46e4c54f160759602ac749022108
ms.sourcegitcommit: 73aff2b3c5e5b8a2254735b0b25931cbb6754c87
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/20/2022
ms.locfileid: "9709395"
---
# <a name="security-and-approvals"></a>Seguridade e aprobacións

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Microsoft Dynamics 365 Project Operations usa dous roles de seguranza para permitir a aprobación de entradas de tempo, gastos e materiais:

- Responsable da aprobación do proxecto
- Administrador responsable da aprobación do proxecto

## <a name="project-approver"></a>Responsable da aprobación do proxecto

Debe ter o rol de seguranza **Responsable de aprobación do proxecto** para aprobar as entradas de tempo, gastos e materiais do proxecto. Tamén debe ter acceso ás entidades relacionadas relevantes, como **Proxecto**. Ese acceso pode ser asignado por alguén que teña o rol de **Xestor de proxectos**. Ademais, debe ser membro do equipo do proxecto e estar marcado como responsable de aprobación.

Para aprobar as entradas que non sexan do proxecto, debe ser o xestor do remitente.

## <a name="project-approver-admin"></a>Administrador responsable da aprobación do proxecto

> [!NOTE]
> A funcionalidade [Conxuntos de aprobacións](approval-sets.md) debe estar activada antes de poder usar a funcionalidade de administrador responsable de aprobación de proxectos.

O rol de seguranza **Administrador responsable de aprobación do proxecto** permite aos usuarios ignorar as políticas e permite a aprobación de entradas en todos os proxectos. A atribución deste rol ignorará a lóxica de validación que require a pertenza ao equipo e estar marcado como responsable de aprobación. Debe ter acceso ás táboas relacionadas relevantes, como **Proxecto**, a través das funcións de seguranza atribuídas a vostede.

O contexto de usuario do SISTEMA ignora as validacións do mesmo xeito que o rol de seguranza administrador responsable de aprobación do proxecto.
