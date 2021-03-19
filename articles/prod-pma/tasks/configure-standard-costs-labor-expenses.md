---
title: Configurar os custos estándar de man de obra e gastos
description: Este tema explica como configurar os custos estándar de man de obra e gastos para un proxecto.
author: Yowelle
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b16ed50584b2b4535d1c61fe7069708182a4820e
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288332"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a>Configurar os custos estándar de man de obra e gastos

[!include [banner](../../includes/banner.md)]

Este tema explica como configurar os custos estándar de man de obra e gastos para un proxecto. Esta tarefa utiliza o conxunto de datos USSI.

1. No panel de navegación, vaia a **Módulos > Xestión de proxectos e contabilidade > Configuración > Prezos > Prezo de custo (hora)**.
2. Seleccione **Nova**.
3. No campo **Data de entrada en vigor**, introduza unha data.
4. No campo **Prezo de custo**, introduza un número. Pode configurar un prezo de custo estándar para a categoría de proxecto ou pode configurar un prezo de custo por número de traballador, número de proxecto, categoría, data ou calquera combinación destes. O prezo de custo que se aplica é o prezo de custo co maior nivel de detalle.  
5. Seleccione **Gardar**.
6. No panel de navegación, vaia a **Módulos > Xestión de proxectos e contabilidade > Configuración > Prezos > Prezo de venda (hora)**.
7. Seleccione **Nova**.
8. No campo **Data de entrada en vigor**, introduza unha data.
9. No campo **Válido para**, seleccione unha opción.
10. No campo **Prezos**, introduza un número. Pode configurar un prezo de venda estándar para transaccións por horas ou para unha categoría de proxecto. Tamén pode configurar os prezos de venda por número de traballador, número de proxecto, categoría, data de transacción ou calquera combinación destes. O prezo de venda real, que se aplica cando un traballador realiza unha transacción no diario de horas, é o prezo de venda co maior nivel de detalle. Por exemplo, se se establecen tanto un prezo de venda xeral como un prezo de venda específico para o traballador, úsase o prezo de venda específico para o traballador.  
11. Seleccione **Gardar**.
12. Peche a páxina.
13. No panel de navegación, vaia a **Módulos > Xestión de proxectos e contabilidade > Configuración > Prezos > Prezo de custo (gasto)**.
14. Seleccione **Nova**.
15. No campo **Data de entrada en vigor**, introduza unha data.
16. No campo **Prezo de custo**, introduza un número. Pódense encher varios campos, pero este é o mínimo necesario para gardar o rexistro.  
17. Seleccione **Gardar**.
18. No panel de navegación, vaia a **Módulos > Xestión de proxectos e contabilidade > Configuración > Prezos > Prezo de venda (gasto)**.
19. Seleccione **Nova**.
20. No campo **Data de entrada en vigor**, introduza unha data.
21. No campo **Válido para**, seleccione unha opción.
22. No campo **Prezos**, introduza un número. O prezo de venda real, que se aplica cando un traballador introduce trasaccións no diario de gastos, é o prezo de venda co maior nivel de detalle. Por exemplo, se se establecen tanto un prezo de venda xeral como un prezo de venda específico para o traballador, úsase o prezo de venda específico para o traballador.  
23. Seleccione **Gardar**.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]