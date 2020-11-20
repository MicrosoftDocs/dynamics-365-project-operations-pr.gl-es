---
title: Notas do programador para as aprobacións
description: Este tema ofrece información adicional para programadores sobre o traballo con aprobacións.
author: stsporen
manager: Annbe
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 9e4e910d0ff0a5f2603148fcc5daa0d423a4d174
ms.sourcegitcommit: a9dbcd3aff4c6ae495412e4980e105ae160fd1ec
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 11/10/2020
ms.locfileid: "4483946"
---
# <a name="developer-notes-for-approvals"></a>Notas do programador para as aprobacións

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Dynamics 365 Project Operations inclúe unha lóxica de validación que garante a transición correcta dos rexistros a través das etapas de aprobación. As transicións correctas de rexistros garanten: 

  - Todas as filas de apoio créanse en táboas relacionadas, como diarios e datos reais.
  - O responsable de aprobación está marcado como **Responsable de aprobación de proxecto** no proxecto antes de continuar.
