---
title: Configurar taxas de custo e vendas para produtos de catálogo - lite
description: Este tema ofrece información sobre como configurar as taxas de custo e vendas de elementos dun catálogo de produtos.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 135b182af73bdab7a3520589431332ad059ec497
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176699"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Configurar taxas de custo e vendas para produtos de catálogo - lite

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_


A configuración dos prezos dos elementos do catálogo de produtos en Dynamics 365 Project Operations é a mesma que en Dynamics 365 Sales.

Debido a que os produtos non se poden estimar nin usar en proxectos en Project Operations, non é necesario establecer prezos do catálogo de produtos nas listas de prezos do proxecto para ofertas e contratos.

Os prezos do catálogo de produtos deben establecerse no campo **Prezo do produto** dunha oferta, contrato ou conta. Non configure os prezos do catálogo de produtos nas listas de prezos do proxecto para estas entidades. As listas de prezos do proxecto son exclusivas de Project Operations. Existe unha lóxica de negocio específica da aplicación que copia as listas de prezos dunha oferta a un contrato. O resultado é unha lista de prezos específica para o contrato. A operación de copia pode retrasar o proceso de gañar a oferta se a lista de prezos do proxecto da oferta é demasiado grande. As listas de prezos de produtos non se copian para crear listas de prezos personalizadas nos contratos. Isto significa que as listas de prezos de produtos non afectan ao rendemento do proceso de gañar a oferta.
