---
title: Configurar taxas de custo e vendas para produtos de catálogo - lite
description: Este artigo ofrece información sobre como configurar os custos e as tarifas de vendas dos artigos dun catálogo de produtos.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4689d6929e24ebaa992232f809a7ec60908ee517
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917390"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Configurar taxas de custo e vendas para produtos de catálogo - lite

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_


A configuración de prezos para elementos do catálogo de produtos en Dynamics 365 Project Operations é igual que en Dynamics 365 Sales.

En Project Operations, os produtos non se poden estimar nin usar en proxectos, polo que non é preciso fixar os prezos do catálogo de produtos nas listas de prezos do proxecto para ofertas e contratos.

Use o campo **Prezo do produto** dunha oferta, contrato ou conta para configurar os prezos do catálogo de produtos. Non configure os prezos do catálogo de produtos nas listas de prezos do proxecto. As listas de prezos do proxecto son exclusivas de Project Operations. A lóxica empresarial específica da aplicación copia as listas de prezos dunha oferta a un contrato. O resultado é unha lista de prezos específica para o contrato. A operación de copia pode retrasar o proceso de gañar a oferta se a lista de prezos do proxecto da oferta é demasiado grande. As listas de prezos de produtos non se copian para crear listas de prezos personalizadas nos contratos. Debido a que non hai copia, o rendemento do proceso da oferta non se ve afectado.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]