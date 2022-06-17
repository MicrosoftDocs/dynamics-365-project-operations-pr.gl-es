---
title: Tipos de período
description: Este artigo ofrece información sobre como configurar tipos de período para a estimación de ingresos.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5bbf2dcb4758611aa9d0591ddfec42869f4438c0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930960"
---
# <a name="period-types"></a>Tipos de período

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Un tipo de período define a frecuencia coa que se calculan os ingresos dun proxecto. Este artigo ofrece información sobre como configurar tipos de período para a estimación de ingresos. 

## <a name="create-and-work-with-period-types"></a>Crear tipos de período e traballar con eles
Para crear e traballar con tipos de período, complete os seguintes pasos:

1. No teu entorno Dynamics 365 Finance, vai a **Xestión de proxectos e contabilidade** > **Montar** > **Estimacións** > **Tipos de período**.
2. Seleccione **Novo** para crear o novo tipo de período. Introduza un nome e unha descrición.
3. No campo **Frecuencia**, seleccione un valor:

    - Se selecciona **Semana**, **Quincenal**, **Semestral**, **Mes**, **Día**, **Trimestre**, ou **Ano**, o calendario usarase para xerar os períodos. 
    - Se selecciona **Período de libro maiore**, os períodos de libro maior da configuración do libro xeral utilizaranse para xerar períodos.
    - Se selecciona **Ilimitado**, pode especificar períodos personalizados.
4. Seleccione o rexistro do tipo de período e logo seleccione **Xerar períodos** para crear períodos para o tipo de período. En función da frecuencia do período que seleccionou, pode que teña a opción de especificar unha data de inicio ou o número de períodos a xerar.
5. Seleccione **Períodos** para revisar os períodos xerados.



[!INCLUDE[footer-include](../includes/footer-banner.md)]