---
title: Desactivar listas de prezos
description: Este tema explica como desactivar ou eliminar listas de prezos non usadas ou antigas.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: aca58eed2a0ee5e108d40636529802a7feec5b8dd060ba6c0eabc6d0b92b2e2f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997649"
---
# <a name="deactivate-price-lists"></a>Desactivar listas de prezos 

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Para eliminar as listas de prezos antigas ou non usadas de Dynamics 365 Project Operations, hai dous pasos que debe completar. 

1. Elimine ou borre a lista de prezos de páxinas específicas.
2. Desactive ou elimine a lista de prezos das listas de prezos activas da páxina **Listas de prezos**.

>[!IMPORTANT]
> Debe completar os dous pasos para eliminar completamente unha lista de prezos. Non é suficiente só realizar o paso 2, que consiste en eliminar ou desactivar directamente a lista de prezos da vista Listas de prezos activos. Tamén debe eliminar a asociación desta lista de prezos de todos os lugares mencionados no paso 1.

## <a name="delete-the-price-list-from-specific-pages"></a>Eliminar a lista de prezos de páxinas específicas
1. Para eliminar unha lista de prezos de Project Operations, vaia ás seguintes páxinas:  

      - Páxna **Parámetros de proxecto** > separador **Listas de prezos**
      - Páxina **Unidade Organizativa** > grade **Listas de prezos**
      - Páxina **Conta** > grade **Listas de prezos de proxecto**
      - Páxina **Ofertas de proxecto** > grade **Listas de prezos de proxecto**: isto aplícase a todas as ofertas de proxectos activos.
      - Páxina **Contratos de proxecto** > grade **Listas de prezos de proxecto**: isto aplícase a todos os contratos de proxectos activos.

 2. Para cada páxina, ten que seleccionar a lista de prezos que desexa eliminar e, a seguir, seleccione **Eliminar**. 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a>Desactive ou elimine a lista de prezos da páxina Listas de prezos.
 
1. Para eliminar unha lista de prezos das listas de prezos activas, vaia a **Vendas** > **Clientes** > **Listas de prezos**. 
2. Seleccione a lista de prezos que desexa eliminar e, a seguir, seleccione **Eliminar**. Se fai referencia á lista de prezos nalgunha transacción existente, non poderá eliminala. Se isto ocorre, pode desactivar a lista de prezos para que non apareza en ningunha vista. 
3. Para desactivar a lista de prezos, seleccione de novo a lista de prezos e logo seleccione **Desactivar**.   
