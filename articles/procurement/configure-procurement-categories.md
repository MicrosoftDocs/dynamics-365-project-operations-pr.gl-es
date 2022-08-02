---
title: Use categorías de adquisición con pedidos de compra de proxectos e facturas de provedores pendentes
description: Neste artigo descríbese como configurar categorías de adquisición que se poden usar con pedidos de compra de proxectos e facturas de provedores pendentes.
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
# <a name="use-procurement-categories-with-project-purchase-orders-and-pending-vendor-invoices"></a>Use categorías de adquisición con pedidos de compra de proxectos e facturas de provedores pendentes

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Os profesionais de compras poden crear e manter catálogos dos artigos e servizos que se poden utilizar nas ordes de compra do proxecto e nas facturas de provedores pendentes. [Catálogos de compras](/dynamics365/supply-chain/procurement/procurement-catalogs) ofrécelle un xeito sinxelo de clasificar as compras sen ter que configurar e utilizar un catálogo de produtos publicado. Cada categoría de adquisición pódese asignar a unha categoría de proxecto para transaccións de tempo, gastos ou artigos. Despois de publicar unha factura de provedor pendente que utiliza unha categoría de aprovisionamento, o sistema creará datos reais do proxecto de tempo, gasto ou material, transaccións do proxecto e asentos do libro principal.

## <a name="minimum-version-requirements"></a>Requisitos mínimos da versión

As seguintes versións son necesarias para usar categorías de adquisición con pedidos de compra de proxectos para Microsoft Dynamics 365 Project Operations escenarios non abastecidos ou baseados en recursos:

- Operacións do proxecto Dataverse versión de solución 4.41.0.45 ou posterior
- Entorno financeiro e operativo versión 10.0.26 ou posterior

## <a name="run-dual-write-maps-for-procurement-category-support"></a>Executa mapas de dobre escritura para compatibilidade con categorías de adquisición

Asegúrese de que o mapeo para **Entidade de exportación de liña de factura do provedor do proxecto de integración de operacións do proxecto msdyn\_ liñas de facturas do provedor do proxecto** usa a versión 1.0.0.4 ou posterior.

## <a name="enable-the-feature-key-for-procurement-categories"></a>Activa a clave de funcións para as categorías de adquisición

Siga estes pasos para activar a funcionalidade de uso de categorías de adquisición con pedidos de compra de proxectos.

1. En Dynamics 365 Finance, abra o **Xestión de características** espazo de traballo.
1. Na lista de funcións, busque o **Use categorías de adquisición en Operacións do proxecto para escenarios baseados en recursos/non abastecidos** función e, a continuación, seleccione **Activar**.

> [!IMPORTANT]
> Como requisito previo, tamén debes activar **Activa as facturas de provedores pendentes en Project Operations para escenarios baseados en recursos ou non almacenados** característica.

## <a name="map-project-categories-in-the-procurement-category-hierarchy"></a>Asigne as categorías de proxectos na xerarquía de categorías de Contratación

Siga estes pasos para asignar categorías de proxectos ás categorías de contratación no **Categoría de contratación** xerarquía:

1. Ir a **Adquisición e abastecemento \> Categorías de contratación**.
1. Seleccione **Editar a xerarquía de categorías**.
1. Seleccione o nodo de xerarquía de categorías desexado e, a continuación, no **Asignar categorías de proxectos** pestana, asocia o nodo coa categoría do proxecto do **Tempo**, **·**, ou, **Proxecto Item** categoría (é dicir, o **Hora predeterminada** ou **Gastos por defecto** categoría).
1. Seleccione **Gardar**.
1. Peche a páxina.

> [!NOTE]
> A asignación dunha categoría de adquisición a unha categoría de proxecto é opcional. Se unha categoría de adquisición non está mapeada, o sistema utilizará o valor que se establece en **Elemento** campo no **Valores predeterminados da categoría do proxecto** sección sobre o **Project Operations on Dynamics 365 Customer engagement** ficha da **Xestión de proxectos e parámetros contables** páxina.
