---
title: Anular listas de prezos de vendas de proxecto
description: Este tema ofrece información sobre como crear listas de prezos de venda personalizadas.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: af9baca540d89f4e5e616bdfdd6111bef29abe28
ms.sourcegitcommit: 656a9d03f260c29e988e2ff05b6e07ae0365d6d0
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 12/04/2020
ms.locfileid: "4672229"
---
# <a name="override-project-sales-price-lists"></a>Anular listas de prezos de vendas de proxecto

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

## <a name="customer-specific-project-price-lists"></a>Listas de prezos de proxecto específicas do cliente

Os acordos de prezos específicos do cliente pódense configurar como listas de prezos do proxecto nun rexistro de conta en Dynamics 365 Project Operations.

Para configurar unha lista de prezos de proxecto específica do cliente, na área **Vendas**, navegue ata o rexistro da conta.

1. Abra a páxina de lista **Contas**.
2. Localice e prema dúas veces nun rexistro de cliente para abrir a páxina de detalles **Conta**.
3. No separador **Listas de prezos de proxecto**, seleccione **+ Nova lista de prezos de proxecto**.
4. Na páxina **Nova lista de prezos de proxecto**, seleccione unha lista de prezos no menú despregable. Só as listas de prezos que teñen o contexto establecido en **Vendas** e cuxa moeda coincide coa moeda da conta están incluídas.
5. Poña un nome á asociación e, a seguir, seleccione **Gardar**. Créase unha lista de prezos de proxecto específica do cliente. Esta lista de prezos usarase para predefinir os prezos do proxecto nas ofertas ou contratos de proxecto ou contratos creados para este cliente cando a data de creación da oferta ou contrato de proxecto entra dentro da data de efectividade da lista de prezos.

## <a name="custom-pricing-on-project-quotes"></a>Prezos personalizados en ofertas de proxecto

Nas ofertas de proxecto, pode ter prezos de proxectos que comecen cunha lista de prezos estándar predefinida que se obtén do cliente ou dos parámetros do proxecto.

Cando precisa un prezo personalizado para o traballo relacionado co proxecto cunha oferta concreta, pode obtelo na entidade asociada de listas de prezos de proxecto.

Complete os seguintes pasos para configurar os prezos do proxecto baseado en proxecto.

1. Abra a oferta de proxecto e seleccione o separador **Listas de prezos de proxecto**.
2. Na subgrade, seleccione **Crear prezos personalizados**.

Todas as listas de prezos do proxecto que se anexan á oferta cópianse en novas listas de prezos. Os nomes das novas listas de prezos reflicten o nome da oferta cun selo de data e hora para o momento no que se crearon estas listas de prezos.

Pode usar cada unha desas listas de prezos e actualizar os prezos da man de obra (prezo de rol) e de gasto (prezo de categoría). Estes prezos só serán aplicables a esta oferta de proxecto.

## <a name="price-lists-on-a-project-contract"></a>Listas de prezos nun contrato do proxecto

Nun contrato de proxecto, os prezos do proxecto sempre se predefinen como unha lista de prezos personalizada co nome do contrato e a o selo de data e hora de creación anexo ao nome. Isto é certo se o contrato se creou cando se gañou a oferta ou se o contrato se creou desde cero. Se é necesario, pode eliminar esta asociación á lista de prezos personalizada e asociar unha lista de prezos estándar ao contrato do proxecto.

Cando asocia unha lista de prezos estándar ás listas de prezos do proxecto na oferta ou no contrato, calquera cambio realizado nos prezos da lista de prezos afectará a todas as ofertas e contratos que usen a lista de prezos.


[!INCLUDE[footer-include](../includes/footer-banner.md)]