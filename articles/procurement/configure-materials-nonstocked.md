---
title: Configurar materiais sen fornecemento e facturas pendentes do fornecedor
description: Este tema explica como activar materiais sen fornecemento e facturas pendentes do fornecedor.
author: sigitac
ms.date: 06/22/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1b14ab17a317e7082bc9c24709590745a5c48ea8
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8592966"
---
# <a name="configure-non-stocked-materials-and-pending-vendor-invoices"></a>Configurar materiais sen fornecemento e facturas pendentes do fornecedor

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

## <a name="minimum-version-requirement"></a>Requisito de versión mínima

Usar materiais sen fornecemento e facturas pendentes do fornecedor para situacións baseadas en recursos/sen fornecemento de Dynamics 365 Project Operations require as seguintes versións:

Solucións de Dynamics 365 Dataverse:

- Project Operations – 4.9.0.221 ou superior
- Solución de orquestración de aplicacións de escrita dual: 2.2.2.23 ou superior

Dynamics 365 Finance:
- 10.0.18 (10.0.793.52) ou superior. Asegúrese de que o seu ambiente de Finance estea actualizado e que todas as actualizacións de calidade se apliquen para cumprir os requisitos mínimos de versión.

## <a name="run-dual-write-maps-for-non-stocked-materials-and-vendor-invoice-integration"></a>Executar mapas de escrita dual para a integración de materiais sen fornecemento facturas do fornecedor

Esta sección ofrece información sobre os mapas específicos necesarios para os materiais sen fornecemento e as facturas do fornecedor. Verifique que os mapas de requisitos previos listados no tema [Fornecer un novo ambiente](../environment/resource-provision-new-environment.md#run-project-operations-dual-write-maps) están a executarse no seu ambiente.

1. Vaia a Lifecycle Services (LCS), navegue ata o seu proxecto de LCS e vaia á páxina **Detalles do ambiente**.
2. Na sección **Información do ambiente de Common Data Service**, seleccione **Ligazón a CDS para aplicacións**. Despois de seleccionar a ligazón, redirixiráselle á lista de entidades nas asignacións.
3. Asegúrese de que se executan os seguintes mapas. Se non se están a executar, inícieos e asegúrese de incluír todos os mapas de táboas relacionados.

    - CDS lanzou distintos produtos (products)
    - Fornecedores v2 (msdyn_vendors)
    - Táboa de Project Operations para estimacións de material (msdyn_estimatelines)
    - Entidade de exportación de facturas do fornecedor do proxecto de integración de Project Operations (msdyn_projectvendorinvoices)
    - Entidade de exportación de liñas de facturas do fornecedor do proxecto de integración de Project Operations (msdyn_projectvendorinvoicelines)
    - Datos reais de integración de Project Operations (msdyn_actuals). Asegúrese de que está a executar a versión do mapa 1.0.0.14 ou superior. Pode ver a versión activa do mapa na columna **Versión** columna na páxina **Escrita dual**. Pode activar unha nova versión do mapa seleccionando **Versión do mapa de táboas** e logo gardar a versión seleccionada.

Se está a usar datos de demostración estándar, pode que tamén deba deter e reiniciar os seguintes mapas de entidades con sincronización inicial:
  - Días de pagamento CDS V2 (msdyn_paymentdays)
  - Programa de pagamentos (msdyn_paymentschedules)
  - Condicións de pagamento (msdyn_paymentterms)
  - Grupos de fornecedores (msdyn_vendorgroups)
  - Unidades (uom)

> [!NOTE]
> A sincronización inicial para grupos de fornecedores e unidades pode fallar para algúns rexistros no conxunto de datos de demostración existente. Pode ignorar os fallos xa que non lle impedirán empregar datos de demostración con Project Operations.

## <a name="configure-prerequisites-in-dataverse"></a>Configurar requisitos previos en Dataverse

### <a name="activate-workflow-to-create-accounts-based-on-vendor-entity"></a>Active o fluxo de traballo para crear contas baseadas na entidade do fornecedor

A solución de orquestración de escrita dual proporciona [Integración principal de fornecedores](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-mapping). Como requisito previo para esta funcionalidade, os datos do fornecedor deben crearse na entidade **Contas**. Active un proceso de fluxo de traballo de modelo para crear fornecedores na táboa **Contas** como se describe en [Cambiar entre deseños de fornecedores](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-switch).

### <a name="set-products-to-be-created-as-active"></a>Definir os produtos que se van crear como activos

Os materiais sen fornecemento deben configurarse como **Produtos lanzados** en Finance. A solución de orquestración de escrita dual proporciona unha [Integración de produtos lanzados inicial no Catálogo de produtos de Dataverse](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/product-mapping). Por defecto, os produtos de Finance están sincronizados con Dataverse nun estado de borrador. Para sincronizar o produto cun estado activo para que poida usarse directamente en documentos de uso de material ou facturas pendentes do fornecedor, vaia a **Sistema** > **Administración** > **Administración do sistema** > **Configuración do sistema**, e no separador **Sales**, estableza **Crear produtos en estado activo** en **Si**.

## <a name="configure-prerequisites-in-finance"></a>Configurar requisitos previos en Finance

### <a name="enable-the-feature-key-for-pending-vendor-invoices"></a>Active a clave da funcionalidade para as facturas pendentes do fornecedor

Realice os seguintes pasos para activar a funcionalidade de engadir detalles do proxecto nas liñas de facturas pendentes do fornecedor.

1. En Finance, vaia á área de traballo **Xestión de funcionalidades**.
2. Na lista de funcionalidades, busque a funcionalidade **Activar facturas pendentes do fornecedor en Project Operations para situacións baseadas en recursos/sen fornecemento** e seleccione **Activar**.

### <a name="define-category-groups-and-project-categories-for-items"></a>Definir grupos de categorías e categorías de proxecto para elementos

Configure polo menos un grupo de categorías para o tipo de transacción **Elemento** e polo menos unha categoría de proxecto que usa este grupo. Para obter máis información, consulte [Configurar categorías de proxecto](../project-accounting/configure-project-categories.md#category-groups).

Revise os perfís de custos e ingresos do proxecto e configure os axustes de contabilización del libro maior para as transaccións de elementos. Para obter máis información, consulte [Configurar a contabilidade para proxectos facturables](../project-accounting/configure-accounting-billable-projects.md).

### <a name="set-up-a-write-in-product"></a>Configurar un produto fóra de catálogo

En Project Operations, pode rexistrar estimacións de material e uso para produtos de catálogo configurados no catálogo de produtos publicado e para produtos fóra de catálogo. O uso de produtos fóra de catálogo require un único produto lanzado que estea configurado en Finance para este fin. Realice os seguintes pasos para configurar un produto fóra de catálogo. Repita estes pasos en cada entidade legal que use Project Operations para situacións baseadas en recursos/sen fornecemento.

1. En Finance, vaia a **Xestión de información de produtos** > **Produtos** > **Produtos lanzados** e seleccione **Novo**.
2. No campo **Tipo de produto**, seleccione **Elemento** e no campo **Subtipo de produto**, seleccione **Produto**.
3. Introduza o número do produto (WRITEIN) e o nome do produto (Produto fóra de catálogo).
4. Seleccionar o grupo de modelos de elemento. Asegúrese de que o grupo de modelos de elemento que seleccione teña o campo **Política de inventario Produto con fornecemento** definido como **Falso**.
5. Seleccione valores nos campos **Grupo de elementos**, **Grupo de dimensións de almacenamento** e **Grupo de dimensións de rastrexo**. Use a **Dimensión de almacenamento** só para **Sitio**, e no campo **Dimensións de rastrexo**, seleccione **Ningunha**.
6. Seleccione valores nos campos **Unidade de inventario**, **Unidade de compra** e **Unidade de vendas** e logo garde os seus cambios.
7. No separador **Plan**, configure os axustes de pedido predefinidos e no separador **Inventario**, configure o sitio e o almacén predefinidos.
8. Vaia a **Xestión e contabilidade de proxectos** > **Configurar** > **Parámetros de xestión e contabilidade de proxectos** e abra **Project Operations en Dynamics 365 Dataverse**. 
9. No separador **Materiais**, no campo **Produto fóra de catálogo**, seleccione o produto que creou.
10. No seu ambiente de Dataverse, no mapa do sitio, abra a entidade **Produtos** e busque o rexistro do produto fóra de catálogo. 
11. Abra os detalles do rexistro e estableza o estado do produto en **Retirado**. Este estado do produto impide que calquera usuario use este rexistro de xeito accidental directamente nas estimacións de material e nos documentos de uso.

### <a name="set-up-a-procurement-integration-account"></a>Configurar unha conta de integración de adquisicións

A conta de integración de adquisicións úsase como conta de compensación cando se contabiliza unha factura de fornecedor pendente con liñas atribuídas a un proxecto.

Cando o sistema contabiliza unha factura de fornecedor pendente, esta conta úsase para o importe do custo do proxecto. Os datos da factura do fornecedor son procesados en Dataverse e créase un dato real de proxecto correspondente. A información do dato real do proxecto engádese ao diario de integración de Project Operations. Ao contabilizar o diario de integración, o importe bórrase da conta de integración de adquisicións e rexístrase no custo do proxecto.

1. Para configurar unha conta de integración de adquisicións, vaia a **Xestión e contabilidade de proxectos** > **Configurar** > **Parámetros de xestión e contabilidade de proxectos** e abra **Project Operations en Dynamics 365 Dataverse**. 
2. Seleccione o separador **Materiais** e seleccione un valor no campo **Conta de integración de adquisicións**.

#### <a name="set-up-project-category-defaults-for-an-item"></a>Configure os valores predefinidos da categoría de proxecto para un elemento

1. En Finane, vaia a **Xestión e contabilidade de proxectos** > **Configurar** > **Parámetros de xestión e contabilidade de proxectos** e abra **Project Operations en Dynamics 365 Dataverse**. 
2. No separador **Valores predefinidos da categoría de proxecto**, no campo **Elemento**, seleccione un valor. Esta categoría de proxecto úsase para transaccións de materiais se a categoría de proxecto non se definiu no rexistro de datos reais do proxecto.
