---
title: Usar a categoría de transacción como dimensión de prezos
description: Este tema fornece información sobre como usar o campo Categoría de transacción como dimensión de prezos.
author: rumant
manager: tfehr
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c84d3aaf7cd7577dcd15311f225c82b538586445
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274591"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>Usar a categoría de transacción como dimensión de prezos


_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_


Este tema explica como usar o campo **Categoría de transacción** como dimensión de prezos. 

## <a name="prerequisites"></a>Requisitos previos
Antes de completar os procedementos deste tema, debe ter unha nova solución de dimensión de prezos para a súa organización. Se aínda non a creou, consulte [Crear campos e entidades personalizados como dimensións de prezos](create-custom-fields-entities-pricing-dimensions.md).

## <a name="add-the-transaction-category-field-to-forms-and-views"></a>Engadir o campo Categoría de transacción a formularios e vistas
Para facer o campo **Categoría de transacción** visible na solución de dimensión de prezos, cómpre engadir o campo a todos os formularios e vistas como unha entidade.

A seguinte táboa indica todos os formularios e vistas listos para usar, por entidade. Tamén necesitará engadir o novo campo a calquera formulario ou vista adicional nas súas entidades personalizadas.

|  Entity        | Formularios     |Visualizacións        |
| ------------------------------|---------------------------------|----------------------------------|
|  Prezo do rol| Información |- Prezos de categorías de recursos activos<br> - Visualización asociada do prezo da categoría de recursos |
|  Sobreprezo do prezo da función| Información|- Sobreprezo do prezo do rol activo<br>- Sobreprezo do prezo do rol asociado |
|  Detalle da liña da oferta|- Información do proxecto<br>- Creación rápida do proxecto| - Detalles da liña de oferta activos<br>- Detalles da liña de oferta combinados<br>- Detalles da liña de oferta asociada |
|  Detalle da liña de contrato do proxecto|- Información do proxecto<br>- Creación rápida do proxecto|- Detalles da liña de contrato combinados<br>- Detalles activos da liña de contrato<br>- Detalles da liña de contrato asociada |
|  Tarefa do proxecto|- Información<br>- Novo formulario| &nbsp; |
|  Membro do equipo do proxecto|- Información<br>- Novo formulario|- Membros do equipo de proxecto activos<br>- Membros do equipo do proxecto<br>- Membros do equipo de proxecto asociados |
|  Entrada de tempo|- Información<br>- Crear entrada de tempo|- As miñas entradas de tempo por data<br>- As miñas entradas de tempo desta semana<br>- Entradas de tempo para aprobación|
|  Liña de diario|- Información<br>- Creación rápida|- Liñas de diario activas<br>- Liña de diario asociada|
|  Detalle da liña da factura|- Información<br>- Creación rápida|- Detalles da liña de factura activa<br>- Transaccións de facturas imputables<br>- Transaccións de facturas complementarias<br>- Detalles da liña de factura asociada <br>- Transaccións de facturas non imputables|
|  Dato real|- Información<br>- Datos reais activos| Datos reais asociados |

## <a name="set-up-the-transaction-category-field-as-a-pricing-dimension"></a>Configurar o campo Categoría de transacción como dimensión de prezos

1. Vaia a **Configuración** > **Parámetros**. 
2. Na páxina **Parámetros**, no separador **Dimensións de prezos baseados na cantidade**, verifique que a grade do separador mostra os rexistros da entidade **Dimensións de prezos**.
3. Engada **Categoría de transaccións** a esta lista e configure os campos **Aplicable ao custo** e **Aplicable á venda** en **Si**.
4. No capo **Tipo de dimensión**, seleccione **Baseado na cantidade** e, seguir, seleccione a prioridade para a **Categoría de transacción** relacionada co custo e as vendas.


[!INCLUDE[footer-include](../includes/footer-banner.md)]