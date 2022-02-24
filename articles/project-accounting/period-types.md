---
title: Tipos de período
description: Este tema ofrece información sobre como configurar os tipos de período para a estimación de ingresos.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6bcd988fbd074c66d64f7e327b4329d3de27e950
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531425"
---
# <a name="period-types"></a>Tipos de período

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Un tipo de período define a frecuencia coa que se calculan os ingresos dun proxecto. Este tema ofrece información sobre como configurar os tipos de período para a estimación de ingresos. 

## <a name="create-and-work-with-period-types"></a>Crear tipos de período e traballar con eles
Para crear e traballar con tipos de período, complete os seguintes pasos:

1. No seu ambiente de Dynamics 365 Finance, vaia a **Xestión e contabilidade de proxectos** > **Configuración** > **Estimacións** > **Tipos de período**.
2. Seleccione **Novo** para crear o novo tipo de período. Introduza un nome e unha descrición.
3. No campo **Frecuencia**, seleccione un valor:

    - Se selecciona **Semana**, **Quincenal**, **Semestral**, **Mes**, **Día**, **Trimestre**, ou **Ano**, o calendario usarase para xerar os períodos. 
    - Se selecciona **Período de libro maiore**, os períodos de libro maior da configuración do libro xeral utilizaranse para xerar períodos.
    - Se selecciona **Ilimitado**, pode especificar períodos personalizados.
4. Seleccione o rexistro do tipo de período e logo seleccione **Xerar períodos** para crear períodos para o tipo de período. En función da frecuencia do período que seleccionou, pode que teña a opción de especificar unha data de inicio ou o número de períodos a xerar.
5. Seleccione **Períodos** para revisar os períodos xerados.

