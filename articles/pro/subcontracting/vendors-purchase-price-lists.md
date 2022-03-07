---
title: Xestión de fornecedores listas de prezos de compra en Project Operations
description: Este tema ofrece información que lle axudará a crear e manter datos de fornecedores e listas de prezos de compra para subcontratación.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cf62ef8eb87ac2bc138e63c7f92132e00451df6d7766291a8399a94a070799ab
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994139"
---
# <a name="vendor-and-purchase-price-list-management-in-project-operations"></a>Xestión de fornecedores listas de prezos de compra en Project Operations

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

## <a name="vendors-in-project-operations"></a>Fornecedores en Project Operations

En Microsoft Dynamics 365 Project Operations, as contas de fornecedor teñen un tipo de relación de **Fornecedor** ou **Provedor**. Só pode seleccionar un rexistro de conta que teña un destes tipos de relación como fornecedor nun subcontrato.

Pode asociar unha ou máis listas de prezos de compra a un rexistro de fornecedor. Non obstante, cada lista de prezos de compra asociada a un rexistro de fornecedor debería ter unha efectividade de data distinta. Project Operations non admite a superposición de efectividade de datas para listas de prezos de compra.

De xeito predefinido, os seguintes campos e conceptos nun rexistro de fornecedor úsanse para calquera subcontrato que se cree para o fornecedor:

- Condicións de pagamento
- Contacto de facturación
- Contacto principal

    > [!NOTE]
    > Por defecto, o contacto principal do fornecedor úsase como xestor de contas do subcontrato.

- Moeda
- Listas de prezos de compra actuais

## <a name="purchase-price-lists-in-project-operations"></a>Listas de prezos de compra en Project Operations

Unha lista de prezos onde o campo **Contexto** está definido como **Compra** considérase unha lista de prezos de compra. As listas de prezos de compra pódense definir para representar un catálogo de taxas de compra de tempo, gastos e materiais. As listas de prezos de compra aseméllanse ás listas de custos e prezos de venda en Project Operations. Os seguintes conceptos aplícanse ás listas de prezos de compra do mesmo xeito que ás listas de custos e prezos de venda:

- **Efectividade de datas** - As listas de prezos de compra teñen efectividade de datas. A efectividade de datas represéntase nos campos de data de inicio e data de finalización de cada lista de prezos. O tempo entre a data de inicio e a data de finalización é o período efectivo da data.
- **Moeda** - A moeda da cabeceira da lista de prezos úsase como a moeda na que se expresan os prezos de compra para man de obra, categorías de gastos e produtos do catálogo.
- **Unidade de tempo predefinida** - A unidade de tempo predefinida expresa os prezos de man de obra para as compras. O campo da unidade de tempo nunha lista de prezos úsase só para proporcionar un valor predefinido. Ese valor pódese cambiar en filas de prezos de roles individuais.

As listas de prezos de compra pódense anexar aos rexistros de fornecedores como asociacións coñecidas como listas de prezos do proxecto. Estas listas de prezos úsanse para introducir prezos predefinidos nas liñas de subcontrato. De xeito predefinido, cando se xuntan varias listas de prezos de compra a un rexistro de fornecedor, a lista de prezos máis recente úsase para os subcontratos creados para o fornecedor. Só listas de prezos onde o campo **Contexto** está definido como **Compra** pódese anexar aos rexistros do fornecedor.

### <a name="subcontract-specific-purchase-price-lists"></a>Listas de prezos de compra específicas para subcontratos

As listas de prezos de compra tamén se poden anexar aos subcontratos como asociacións coñecidas como listas de prezos do proxecto. Estas listas de prezos úsanse para introducir prezos predefinidos nas liñas de subcontrato. De xeito predefinido, cando hai varias listas de prezos de compra anexas a un subcontrato, cada unha delas debe ter unha efectividade de datas distinta. Project Operations non admite listas de prezos de compra que teñan efectividade de datas superposta. Só listas de prezos onde o campo **Contexto** está definido como **Compra** pódese anexar aos subcontratos.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
