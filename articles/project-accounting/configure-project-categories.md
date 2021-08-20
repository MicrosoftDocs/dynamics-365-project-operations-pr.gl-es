---
title: Configurar categorías de proxecto
description: Neste tema se proporciona información sobre a configuración das categorías de proxectos.
author: sigitac
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: cea43422469adf12f336f7686814a8199717090c18804d3d0a7509452349566e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997109"
---
# <a name="configure-project-categories"></a>Configurar categorías de proxecto

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Project Operations ofrece capacidades robustas para categorizar ingresos e gastos en proxectos. As categorías ofrecen a capacidade de informar e analizar as transaccións do proxecto e impulsar a contabilización no libro maior.

O seguinte diagrama ilustra a correlación entre categorías de transaccións, as categorías compartidas e as categorías de proxectos. 

As categorías de transaccións son a agrupación básica para as transaccións do proxecto. Dentro desa agrupación, hai un conxunto de categorías compartidas que se poden compartir entre aplicacións e módulos. Afondando aínda máis nos aspectos específicos, as categorías de proxectos son o nivel máis granular de categorías. As categorías de proxectos son específicas para a entidade legal, o módulo e a aplicación.

![Correlación entre categorías de transaccións, as categorías compartidas e as categorías de proxectos.](media/project-categories.png)

## <a name="transaction-categories"></a>Categorías de transaccións

As categorías de transaccións representan a agrupación básica para as transaccións do proxecto e non son específicas do tipo de empresa ou transacción. Por exemplo, Contoso Robotics utiliza as categorías de transaccións deseño, viaxes, instalación e servizo para agrupar as transaccións do proxecto.

As categorías de transaccións defínense no módulo Project Operations. 
1. Vaia a **Configuración** \> **Categorías de transaccións** para abrir o formulario. 
2. Cree unha nova categoría de transaccións seleccionando **Nova** ou seleccionando **Importar desde Excel**.

## <a name="shared-categories"></a>Categorías compartidas

Dynamics 365 utiliza o concepto de categorías compartidas para clasificar os gastos en diferentes aplicacións, como Dynamics 365 Finance, Dynamics 365 Supply Chain e Dynamics 365 Project Operations. Para cada categoría de transacción creada, Project Operations crea automaticamente catro categorías compartidas relacionadas: Horas, Gasto, Taxas e Elemento. Pode revisar e axustar as categorías compartidas indo a **Xestión de proxectos e contabilidade** \> **Configuración** \> **Categorías** \> **Categorías compartidas**.

## <a name="project-categories"></a>Categorías do proxecto

As categorías do proxecto representan o nivel máis granular da configuración de categorías e deben ser configuradas por separado e para cada empresa por un contable do proxecto.

1. Vaia a **Xestión e contabilidade de proxectos** \> **Configuración** \> **Categorías** \> **Categorías de proxectos**.
2. Seleccione **Nova**.
3. Seleccione a **ID de categoría** da categoría compartida que creou na sección anterior. Project Operations permite usar só as categorías compartidas asociadas a categorías de transaccións.
4. Seleccionar un grupo de categorías

## <a name="category-groups"></a>Grupos de categorías

Os grupos de categorías úsanse para compartir propiedades, principalmente publicar perfís, entre categorías de proxectos relacionadas. Debe haber polo menos un grupo de categorías para cada tipo de transacción e cada categoría de proxecto ten asignado un grupo.

As especificacións de contabilización en Project Operations están definidas polas regras do perfil de custos e ingresos do proxecto, as categorías de proxectos e os grupos de categorías. Pode configurar grupos de categorías indo a **Xestión e contabilidade de proxectos** \> **Configuración** \> **Categorías** \> **Grupos de categorías**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]