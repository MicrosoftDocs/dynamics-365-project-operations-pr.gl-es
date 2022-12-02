---
title: Use categorías de adquisición con pedidos de compra de proxectos e facturas de fornecedores pendentes
description: Neste artigo descríbese como configurar categorías de adquisición que se poden usar con pedidos de compra de proxectos e facturas de fornecedores pendentes.
author: sigitac
ms.date: 04/07/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: f71c6bfcd183613471a4cc10e16a5a54571fac31
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028608"
---
# <a name="use-procurement-categories-with-project-purchase-orders-and-pending-vendor-invoices"></a>Use categorías de adquisición con pedidos de compra de proxectos e facturas de fornecedores pendentes

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Os profesionais de compras poden crear e manter catálogos dos artigos e servizos que se poden utilizar nas ordes de compra do proxecto e nas facturas de fornecedores pendentes. [Catálogos de adquisicións](/dynamics365/supply-chain/procurement/procurement-catalogs) ofrécelle un xeito sinxelo de clasificar as compras sen ter que configurar e utilizar un catálogo de produtos publicado. Cada categoría de adquisición pódese asignar a unha categoría de proxecto para transaccións de tempo, gasto ou artigo. Despois de publicar unha factura de fornecedor pendente que utiliza unha categoría de adquisición, o sistema creará datos reais do proxecto de tempo, gasto ou material, transaccións do proxecto e asentos do libro auxiliar.

## <a name="minimum-version-requirements"></a>Requisitos de versión mínima

As seguintes versións son necesarias para usar categorías de adquisición con pedidos de compra de proxectos para escenarios de Microsoft Dynamics 365 Project Operations sen fornecemento/baseados en recursos:

- Solución Project Operations Dataverse versión 4.41.0.45 ou posterior
- Ambiente de finanzas e operacións versión 10.0.26 ou posterior

## <a name="run-dual-write-maps-for-procurement-category-support"></a>Executar mapas de escrita dual para compatibilidade con categorías de adquisición

Asegúrese de que a asignación para **Entidade de exportación de liñas de factura do fornecedor do proxecto de integración de Project Operations msdyn\_projectvendorinvoicelines** utiliza a versión 1.0.0.4 ou posterior.

## <a name="enable-the-feature-key-for-procurement-categories"></a>Activar a clave de funcionalidade para as categorías de adquisición

Siga estes pasos para activar a funcionalidade de uso de categorías de adquisición con pedidos de compra de proxectos.

1. En Dynamics 365 Finance, abra a área de trabalo **Xestión de funcionalidades**.
1. Na lista de funcionalidades, busque a funcionalidade **Usar categorías de adquisición en Project Operations para situacións baseadas en recursos/sen fornecemento** e seleccione **Activar**.

> [!IMPORTANT]
> Como requisito previo, debe tamén activar a funcionalidade **Activar facturas pendentes do fornecedor en Project Operations para situacións baseadas en recursos/sen fornecemento** e seleccione Activar.

## <a name="map-project-categories-in-the-procurement-category-hierarchy"></a>Asignar categorías de proxectos na xerarquía de categorías de adquisición

Siga estes pasos para asignar categorías de proxectos ás categorías de contratación na xerarquía **Categoría de adquisición**:

1. Vaia a **Adquisición e abastecemento \> Categorías de adquisición**.
1. Seleccione **Editar a xerarquía de categorías**.
1. Seleccione o nó da xerarquía de categorías desexado e, a seguir, no separador **Atribuír categorías de proxecto**, asocie o nó á categoría de proxecto **Tempo**, **Gasto** ou **Artigo** (é dicir, **Tempo predefinido** ou **Gasto predefinido**).
1. Seleccione **Gardar**.
1. Peche a páxina.

> [!NOTE]
> A asignación dunha categoría de adquisición a unha categoría de proxecto é opcional. Se unha categoría de adquisición non está asignada, o sistema usará o valor que está establecido no campo **Artigo** da sección **Valores predefinidos da categoría de proxecto** no separador **Project Operations on Dynamics 365 Customer Engagement** da páxina **Parámetros de xestión e contabilidade de proxectos**.
