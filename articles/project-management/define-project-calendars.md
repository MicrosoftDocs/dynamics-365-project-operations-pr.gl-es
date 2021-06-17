---
title: Definir calendarios de proxectos
description: Este tema ofrece información sobre como aplicar un modelo de calendario a un proxecto para rastrexar a programación do proxecto.
author: ruhercul
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 0d1a2c4bd2d4022bbf79afcef79170eb482e6418
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998994"
---
# <a name="define-project-calendars"></a>Definir calendarios de proxectos

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Para crear e xestionar un proxecto, debe aplicarlle un modelo de calendario. O modelo de calendario define os seguintes atributos do proxecto:

- Horas de traballo, incluídas as horas de inicio e fin
- Días laborables
- Excepcións do calendario como días non laborables

O modelo de calendario que se aplica a un proxecto é unha copia do modelo de calendario definido na configuración da súa organización.

> [!NOTE]
> Se cambia o modelo de calendario, eses cambios non se propagarán ás horas de traballo do proxecto. Para cambiar as horas de traballo do proxecto, hai que aplicar un novo modelo.

Para crear un modelo de calendario para a súa organización, hai dous requisitos clave:

- Defina as horas de traballo desexadas do modelo empregando un recurso reservable novo ou existente.
- Cree un novo modelo de calendario e asocie o modelo ao recurso reservable.

**Definir as horas de traballo do modelo**

1. Vaia a **Recursos** \> **Recursos**.
2. Cree un novo recurso para facer referencia a el no modelo de calendario ou seleccione un recurso existente.
3. Seleccione o separador **Horas de traballo** do recurso e siga as instrucións de [Establecer horas de traballo para un recurso](/dynamics365/field-service/set-work-hours-resource.md) para configurar as regras do calendario.

**Crear un novo modelo de calendario**

1. Vaia a **Configuración** \> **Modelo de calendario**.
2. Seleccione **Novo** e introduza un nome, unha descrición e un recurso do modelo.

> [!NOTE]
> Cando se fai referencia a un recurso nun modelo de calendario, asóciase unha copia do calendario do recurso ao modelo de calendario. Se cambian as horas de traballo do modelo copiado, eses cambios non se propagarán ao modelo de calendario.

Agora pode asociar o modelo de traballo a un modelo de calendario de proxecto.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

