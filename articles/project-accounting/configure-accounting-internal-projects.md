---
title: Configurar a contabilidade para proxectos internos
description: Este artigo ofrece información sobre como configurar prácticas de contabilidade para proxectos internos en Project Operations.
author: sigitac
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 7fc2b7247da699a194688b18aa0a695b06cc44c6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919460"
---
# <a name="configure-accounting-for-internal-projects"></a>Configurar a contabilidade para proxectos internos

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Os proxectos internos permiten ás empresas realizar un seguimento dos custos relacionados coas actividades que non se facturan a un cliente. Exemplos de proxectos internos inclúen:

- Desenvolvemento dun produto, como unha aplicación móbil, e rastrexo do custo asociado ao desenvolvemento.
- Xestión do tempo e os gastos previos á venda. Este proxecto interno de prevenda pódese converter máis tarde a un proxecto facturable se se gaña a oferta.

Calquera proxecto non asociado a un contrato en Dynamics 365 Project Operations é tratado como interno. Os perfís de custos e ingresos do proxecto non se usan para determinar as regras de contabilidade para o proxecto. O custo interno do proxecto sempre se contabiliza seguindo os principios de resultados. As contas de libro maior para os asentos defínense na páxina **Configuración de asentos de libro maior**.

- As transaccións de tempo contabilízanse cargando a conta de **Custo** conta e abonando a conta de **Asignación de nómina**.
- As transaccións de gasto contabilízanse cargando a conta de **Custo** conta e abonando a conta de **Conta compensada para gastos**.
- As transaccións de artigos contabilízanse cargando a conta de **Custo** e abonando a conta de **Custo - Elemento**.

Despois de que as transaccións se contabilicen no proxecto, se o proxecto está asociado a un contrato de proxecto, o sistema inverte todas as transaccións acumuladas e crea novas transaccións facturables. As transaccións facturables seguen as regras de contabilidade definidas no perfil de ingresos e custos do proxecto respectivo.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
