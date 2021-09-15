---
title: Liñas de subcontrato para produtos
description: Este tema explica como rexistrar liñas de subcontrato para produtos e usar os distintos campos para rexistrar compras de produtos de fornecedores.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c0ddc39638ae9830eacc57f3e1def75aa36e6553
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323684"
---
# <a name="subcontract-lines-for-products"></a>Liñas de subcontrato para produtos

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

Un subcontrato en Dynamics 365 Project Operations pode ter unha liña de subcontrato para produtos. Estas liñas permiten a un xestor de proxectos mercar produtos de fornecedores que logo poden usar nas tarefas do proxecto.

Complete os seguintes pasos para crear unha liña de subcontrato para produtos en Project Operations.

1. Na páxina de navegación, seleccione **Subcontratos** e abra o subcontrato co que desexa traballar. 
2. No separador **Liñas de subcontrato**, seleccione **+ Nova** para crear unha nova liña de subcontrato.
3. Na páxina **Creación rápida**, no campo **Clase de transacción**, seleccione **Material** e introduza ou seleccione a información de campo requirida. 
4. Seleccione **Gardar**.

A seguinte táboa ofrece información sobre os campos na páxina **Detalles de liña de subcontrato** e a páxina **Creación rápida**, xa que son relevantes para comprar produtos.

| Campo | Descripción |
| ----- | ----------- |
| Nome | O nome da liña de subcontrato. |
| Descripción | Unha breve descrición dos produtos que se van pedir na liña de subcontrato. |
| Tipo de liña | Este campo ten un valor predefinido de **Baseado na cantidade**. |
| Método de facturación |  O método de facturación da liña de subcontrato. Está dispoñible unha programación de facturas baseada en fitos para métodos de facturación a prezo fixo. |
| Clase de transacción | Este campo ten un valor predefinido de **Tempo**. Para crear liñas de subcontrato para mercar produtos, no campo **Clase de transacción** seleccione **Material**. Esta selección de campo indica que a liña de subcontrato se emprega para rexistrar a compra de produtos que se utilizarán en proxectos. |
| Seleccionar produto | Seleccione se o produto que se está a mercar se mantén no catálogo de produtos ou se é un produto rexistrado. |
| Produto | Seleccione un produto activo do catálogo. Este campo só está dispoñible cando **Seleccionar produto** está axustado en **Existente**. |
| Produto fóra de catálogo | Introduza o nome do produto fóra de catálogo. Este campo só está dispoñible cando **Seleccionar produto** está axustado en **Fóra de catálogo**.  |
| Data de entrega solicitada | Seleccione a data de entrega requirida para os produtos. Esta data tamén se usa para escoller unha lista de prezos do proxecto das listas de prezos do proxecto anexadas ao subcontrato. O custo do produto na liña de subcontrato é o predefinido desa lista de prezos. |
| Data de entrega contratada | Seleccione a data na que se acorda a entrega dos produtos.  |
| Cantidade solicitada | Introduza a cantidade do produto que se vai comprar ao fornecedor. Cando un xestor de proxectos supera esta cantidade, producirase unha advertencia. |
| Grupo de unidades | Este valor é o predefinido só para produtos de catálogo. Cando se seleccionan **Produto** e **Data de entrega solicitada**, o sistema selecciona a lista de prezos aplicable en función da data de entrega. Consúltanse os elementos da lista de prezos relacionados co produto coincidente. Os valores da unidade e do grupo de unidades predefinidos na configuración do rexistro de elementos da lista de prezos. |
| Unidade | Este valor predefinido é a configuración da unidade no rexistro de elementos da lista de prezos. Pode cambiar isto por outra unidade segundo sexa necesario. A combinación de produto e unidade úsase para predefinir o prezo unitario na liña de subcontrato para os produtos de catálogo existentes. |
| Prezo por unidade | O valor do campo do prezo unitario é o predefinido usando a combinación do produto e a unidade dos elementos da lista de prezos relacionados que é aplicable para a data de entrega solicitada da liña de subcontrato.  |
| Subtotal | Este campo de só lectura calcúlase como Cantidade x Prezo unitario se os dous campos teñen valores introducidos. Se o campo **Cantidade**, o campo **Prezo unitario** ou ambos están baleiros, pode introducir un valor manualmente.  |
| Imposto de vendas | Introduza o valor do imposto sobre as vendas. |
| Cantidade total | Este campo calculado mostra o importe total da liña de subcontrato despois de incluír os impostos. O valor deste campo calcúlase como subtotal + imposto. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
