---
title: Configurar a integración Project Operations por entidade legal
description: Este artigo ofrece información sobre como configurar a integración por persoa xurídica en Project Operations.
author: sigitac
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3f33e641ee0932655282618c99a26e2603660059
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914676"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a>Configurar a integración Project Operations por entidade legal 

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Este artigo explica os pasos necesarios para configurar Dynamics 365 Project Operations por persoa xurídica.

## <a name="enable-feature-keys-in-dynamics-365-finance"></a>Activa as claves de función en Dynamics 365 Finance

Complete os seguintes pasos para activar as funcionalidades requiridas.

1. En Dynamics 365 Finance, vai ao **Xestión de características** espazo de traballo.
2. En **Lista de funcionalidades**, busque e active as seguintes funcionalidades:
  
    - **Activar varias liñas de contrato para un proxecto**
    - **Activa as operacións do proxecto en Dynamics 365 Customer Engagement**

> [!NOTE]
> Se non ve as **Claves de funcionalidade** na lista, verifique que a súa versión de Finance cumpra o requisito mínimo de versión (versión da aplicación 10.0.13 con todas as actualizacións de calidade aplicadas ou superior). Seleccione **Comprobar se hai actualizacións** para actualizar a lista de funcionalidades.

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a>Definir o escenario de despregamento de Project Operations para unha entidade legal

Podes activar as operacións do proxecto en Dynamics 365 Customer Engagement a nivel de persoa xurídica. Podes ter unha persoa xurídica usando Project Operations en Dynamics 365 Customer Engagement para escenarios baseados en recursos/non abastecidos. No mesmo ambiente, pode ter outra entidade legal que empregue Project Operations para escenarios de de produción/con fornecemento.

1. En Dynamics 365 Finance, vai a **Xestión de proxectos e contabilidade** > **Montar** > **Xestión de proxectos globais e parámetros contables**.
2. Na lista de entidades xurídicas dispoñibles, selecciona as entidades nas que se activarán as funcións de varias liñas de contrato e Operacións de proxectos en Dynamics 365 Customer Engagement. Deixa sen seleccionar as entidades legais que empregarán Project Operations para escenarios de produción/con fornecemento.

> [!NOTE]
> Só se pode seleccionar unha entidade legal se non ten ningún proxecto existente.

## <a name="configure-project-management-and-accounting-parameters"></a>Configurar os parámetros de Xestión e contabilidade de proxectos

Cada entidade xurídica que utilice Project Operations en Dynamics 365 Customer Engagement necesita un conxunto de parámetros predeterminados. Estes parámetros configúranse no separador **Projecto Operations** na páxina **Parámetros de Xestión e contabilidade de proxectos**. Os parámetros son:

  - **Valores predefinidos do tipo de facturación**: Project Operations emprega un conxunto fixo de valores predefinidos do tipo de facturación que se deben atribuñir ás propiedades de liña de Finance. Cree un rexistro para cada tipo de facturación: **Non especificado**, **Imputable**, **Non imputable**, **Gratuíto** e **Non dispoñible**.
  - **Valores predefinidos de categoría de proxecto**: Seleccione as categorías de proxecto predefinidas que se empregarán para cada tipo de transacción. Estes valores predefinidos utilizaranse no **Diario de integración de Project Operations** e nas estimacións onde non se especifica ningunha categoría de transacción para o datos real do proxecto.
  - **Previsións**: Seleccione o modelo de previsión que se utilizará para estimacións de tempo e gastos.


[!INCLUDE[footer-include](../includes/footer-banner.md)]