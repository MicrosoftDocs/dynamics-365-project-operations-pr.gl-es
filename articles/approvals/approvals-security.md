---
title: Seguridade e homologacións
description: Este artigo ofrece información sobre a configuración de seguranza para traballar con aprobacións en Microsoft Dynamics 365 Project Operations.
author: stsporen
ms.date: 08/29/2022
ms.topic: security
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: bc33f63f66bdcf1470e5d9386cfc3661774436fd
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 09/16/2022
ms.locfileid: "9525403"
---
# <a name="security-and-approvals"></a>Seguridade e homologacións

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Microsoft Dynamics 365 Project Operations usa dous roles de seguranza para permitir a aprobación de entradas de tempo, gastos e materiais:

- Responsable da aprobación do proxecto
- Administrador Aprobador de Proxectos

## <a name="project-approver"></a>Responsable da aprobación do proxecto

Debes ter o **Aprobador do proxecto** rol de seguranza para aprobar as entradas de tempo, gastos e materiais do proxecto. Tamén debes ter acceso ás entidades relacionadas relevantes, como **Proxecto**. Ese acceso pode ser asignado por alguén que teña o **Xerente de proxecto** papel. Ademais, debes ser membro do equipo do proxecto e estar marcado como aprobador.

Para aprobar as entradas que non sexan do proxecto, debes ser o xestor do remitente.

## <a name="project-approver-admin"></a>Administrador Aprobador de Proxectos

> [!NOTE]
> O [Conxuntos de aprobación](approval-sets.md) A función debe estar activada antes de poder usar a funcionalidade de administrador do aprobador de proxectos.

O **Administrador Aprobador de Proxectos** rol de seguranza permite aos usuarios ignorar as políticas e permite a aprobación de entradas en todos os proxectos. A asignación deste rol ignorará a lóxica de validación que require a pertenza ao equipo e que se marque como aprobador. Debes ter acceso ás entidades relacionadas relevantes, como **Proxecto**. Ese acceso pode ser asignado por alguén que teña o **Xerente de proxecto** papel.

O contexto de usuario SISTEMA omite validacións do mesmo xeito que o administrador do aprobador de proxectos rol de seguranza.
