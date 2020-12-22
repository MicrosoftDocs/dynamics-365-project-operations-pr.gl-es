---
title: Proxectos de estimación de ingresos a prezo fixo
description: Este tema fornece información sobre os ingresos a prezo fixo en proxectos.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 80fe1d4171d80ca39e8b7ebb1eefaa524a4f2b07
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531426"
---
# <a name="fixed-price-revenue-estimate-projects"></a>Proxectos de estimación de ingresos a prezo fixo 

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Cando crea unha liña de contrato de proxecto cos seguintes atributos en Dynamics 365 Project Operations en Microsoft Dataverse, o sistema crea automaticamente un proxecto de estimación de ingresos a prezo fixo. A información deste proxecto baséase no seguinte:

  - Un método de facturación a prezo fixo.
  - Un proxecto asociado.
  - Polo menos un fito definido no separador **Programación de facturas** na páxina **Liña de contrato do proxecto**.

## <a name="review-fixed-price-revenue-estimates-projects"></a>Revisar proxectos de estimacións de ingresos a prezo fixo
Para revisar os proxectos de estimación de ingresos a prezo fixo, complete os seguintes pasos:

1. No ambiente de Dynamics 365 Finance, vaia a **Xestión e contabilidade de proxectos** > **Proxectos** > **Proxectos de estimación de ingresos a prezo fixo**.
2. Seleccione o proxecto que desexa ver e prema dúas veces en **ID do proxecto de estimación** para abrir o rexistro e revisar os detalles do proxecto.
3. Expanda o separador **Proxecto**. Verá un proxecto na grade **Proxectos seleccionados**. O sistema usa isto como proxecto predefinido porque é o proxecto asociado á liña de contrato do proxecto. 
4. Para cambiar a asociación, seleccione proxectos adicionais e engádaos á grade **Proxectos seleccionados**. Se se seleccionan varios proxectos nesta grade, a porcentaxe de finalización do proxecto e as estimacións de ingresos calcúlanse conxuntamente para todos os proxectos seleccionados.

  O custo do proxecto, o perfil de ingresos, o modelo de custo e o código do período pódense configurar manualmente. Se non se configuran manualmente, os valores son os predefinidos durante o primeiro cálculo de estimación do proxecto empregando as regras configuradas para os perfís de custos e ingresos do proxecto.

