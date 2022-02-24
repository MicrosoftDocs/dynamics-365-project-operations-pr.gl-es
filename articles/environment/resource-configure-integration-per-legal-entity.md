---
title: Configurar a integración Project Operations por entidade legal
description: Este tema ofrece información sobre como configurar a integración por entidade legal en Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5d2bb415362a088e01253fbe54f9f06569b4a921
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122881"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a>Configurar a integración Project Operations por entidade legal 

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Este tema guíalle polos pasos necesarios para configurar Dynamics 365 Project Project Operations por entidade legal.

## <a name="enable-feature-keys-in-dynamics-365-finance"></a>Activar claves de funcionalidade en Dynamics 365 Finance

Complete os seguintes pasos para activar as funcionalidades requiridas.

1. En Dynamics 365 Finance, vaia á área de traballo **Xestión de funcionalidades**.
2. En **Lista de funcionalidades**, busque e active as seguintes funcionalidades:
  
    - **Activar varias liñas de contrato para un proxecto**
    - **Activar Project Operations en Dynamics 365 Customer Engagement**

> [!NOTE]
> Se non ve as **Claves de funcionalidade** na lista, verifique que a súa versión de Finance cumpra o requisito mínimo de versión (versión da aplicación 10.0.13 con todas as actualizacións de calidade aplicadas ou superior). Seleccione **Comprobar se hai actualizacións** para actualizar a lista de funcionalidades.

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a>Definir o escenario de despregamento de Project Operations para unha entidade legal

Pode activar Project Operationes en Dynamics 365 Customer Engagement a nivel de entidade legal. Pode ter unha entidade legal usando Project Operations en Dynamics 365 Customer Engagement para escenarios baseados en recursos/sen fornecemento. No mesmo ambiente, pode ter outra entidade legal que empregue Project Operations para escenarios de de produción/con fornecemento.

1. En Dynamics 365 Finance, vaia a **Xestión e contabilidade de proxectos** > **Configuración** > **Parámetros globais de Xestión e contabilidade de proxectos**.
2. Na lista de entidades legais dispoñibles, seleccione as entidades onde hai varias liñas de contrato e activaranse as funcionalidades de Project Operationes en Dynamics 365 Customer Engagement. Deixa sen seleccionar as entidades legais que empregarán Project Operations para escenarios de produción/con fornecemento.

> [!NOTE]
> Só se pode seleccionar unha entidade legal se non ten ningún proxecto existente.

## <a name="configure-project-management-and-accounting-parameters"></a>Configurar os parámetros de Xestión e contabilidade de proxectos

Cada entidade legal que usa Projecto Operations en Dynamics 365 Customer Engagement precisa dun conxunto de parámetros predefinidos. Estes parámetros configúranse no separador **Projecto Operations** na páxina **Parámetros de Xestión e contabilidade de proxectos**. Os parámetros son:

  - **Valores predefinidos do tipo de facturación**: Project Operations emprega un conxunto fixo de valores predefinidos do tipo de facturación que se deben atribuñir ás propiedades de liña de Finance. Cree un rexistro para cada tipo de facturación: **Non especificado**, **Imputable**, **Non imputable**, **Gratuíto** e **Non dispoñible**.
  - **Valores predefinidos de categoría de proxecto**: Seleccione as categorías de proxecto predefinidas que se empregarán para cada tipo de transacción. Estes valores predefinidos utilizaranse no **Diario de integración de Project Operations** e nas estimacións onde non se especifica ningunha categoría de transacción para o datos real do proxecto.
  - **Previsións**: Seleccione o modelo de previsión que se utilizará para estimacións de tempo e gastos.
