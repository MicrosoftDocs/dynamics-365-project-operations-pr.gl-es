---
title: Configurar a contabilidade para proxectos internos
description: Este tema ofrece información sobre como configurar prácticas de contabilidade para proxectos internos en Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9f1cc75b12fec81d726e46f8d970dcfe030f6b29
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287596"
---
# <a name="configure-accounting-for-internal-projects"></a>Configurar a contabilidade para proxectos internos

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Os proxectos internos permiten ás empresas realizar un seguimento dos custos relacionados coas actividades que non se facturan a un cliente. Exemplos de proxectos internos inclúen:

- Desenvolvemento dun produto, como unha aplicación móbil, e rastrexo do custo asociado ao desenvolvemento.
- Xestión do tempo e os gastos previos á venda. Este proxecto interno de prevenda pódese converter máis tarde a un proxecto facturable se se gaña a oferta.

Calquera proxecto non asociado a un contrato en Dynamics 365 Project Operations é tratado como interno. Os perfís de custos e ingresos do proxecto non se usan para determinar as regras de contabilidade para o proxecto. O custo interno do proxecto sempre se contabiliza seguindo os principios de resultados. As contas de libro maior para os asentos defínense na páxina **Configuración de asentos de libro maior**.

- As transaccións de tempo contabilízanse cargando a conta de **Custo** conta e abonando a conta de **Asignación de nómina**.
- As transaccións de gasto contabilízanse cargando a conta de **Custo** conta e abonando a conta de **Conta compensada para gastos**.

Despois de que as transaccións se contabilicen no proxecto, se o proxecto está asociado a un contrato de proxecto, o sistema inverte todas as transaccións acumuladas e crea novas transaccións facturables. As transaccións facturables seguen as regras de contabilidade definidas no perfil de ingresos e custos do proxecto respectivo.




[!INCLUDE[footer-include](../includes/footer-banner.md)]