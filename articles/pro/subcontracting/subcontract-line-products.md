---
title: Liñas de subcontrato para produtos
description: Este artigo explica como rexistrar liñas de subcontratación de produtos e utilizar os distintos campos para rexistrar as compras de produtos dos provedores.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b5852df1876eff591ae6a131b229d979eacf5aad
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/11/2022
ms.locfileid: "9262108"
---
# <a name="subcontract-lines-for-products"></a>Liñas de subcontrato para produtos

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

Un subcontrato en Dynamics 365 Project Operations pode ter unha liña de subcontrato para produtos. Estas liñas permiten a un xestor de proxectos mercar produtos de fornecedores que logo poden usar nas tarefas do proxecto.

Complete os seguintes pasos para crear unha liña de subcontrato para produtos en Project Operations.

1. Na páxina de navegación, seleccione **Subcontratos** e abra o subcontrato co que desexa traballar. 
2. No separador **Liñas de subcontrato**, seleccione **+ Nova** para crear unha nova liña de subcontrato.
3. Na páxina **Creación rápida**, no campo **Clase de transacción**, seleccione **Material** e introduza ou seleccione a información de campo requirida. 
4. Seleccione **Gardar**.

A seguinte táboa ofrece información sobre os campos na páxina **Detalles de liña de subcontrato** e a páxina **Creación rápida**, xa que son relevantes para comprar produtos.

| Campo | Descripción | Impacto funcional|
| ----- | ----------- | ----------- |
| Nome | Nome da liña de subcontrato para axudar na identificación. |Esta amosarase como a primeira columna en todas as buscas baseadas en liñas de subcontrato.
| Descripción | Unha breve descrición dos produtos que se van pedir na liña de subcontrato. | Nada |
| Tipo de liña | Este campo ten un valor predefinido de **Baseado na cantidade**. |Nada |
| Método de facturación | Este é un conxunto de opcións que representa os dous principais modelos de contratación admitidos por Project Operations: **Prezo fixo** e **Tempo e Material**. | Segundo o método de facturación seleccionado, unha programación de facturas baseada en fitos está dispoñible para as liñas de subcontrato co método de facturación de prezo fixo. |
| Clase de transacción |Este campo ten un valor predefinido de **Tempo**. Para crear liñas de subcontrato para mercar produtos, configure o campo **Clase de transacción** en **Material**.  | Isto indica que a liña de subcontrato se está a utilizar para rexistrar a compra dos produtos que se utilizarán en proxectos. |
| Seleccionar produto | Seleccione se o produto que se está a mercar se mantén no catálogo de produtos ou se é un produto rexistrado. |Nada |
| Produto | Seleccione un produto activo do catálogo. Este campo só está dispoñible cando **Seleccionar produto** está axustado en **Existente**. |A combinación de **Produto** e **Unidade** usarase como predefinida ou computada para o prezo unitario da liña de subcontrato.
| Produto fóra de catálogo | Introduza o nome do produto fóra de catálogo. Este campo só está dispoñible cando **Seleccionar produto** está axustado en **Fóra de catálogo**.  |O prezo de compra non se cubrirá automaticamente para os produtos fóra de catálogo.|
| Data de entrega solicitada | Introduza a data de entrega requirida para os produtos.| Esta data tamén se usa para escoller unha lista de prezos do proxecto das listas de prezos do proxecto anexadas ao subcontrato. O custo do produto na liña de subcontrato é o predefinido desa lista de prezos. |
| Data de entrega contratada | Introduza a data na que se acorda contractualmente a entrega dos produtos.  |Nada|
| Cantidade solicitada | Introduza a cantidade do produto que se vai comprar ao fornecedor.| Isto usarase para amosar avisos cando un xestor de proxecto está a extraer demasiado desta cantidade.|
| Grupo de unidades | Este valor é o predefinido só para produtos de catálogo. |Cando se seleccionan **Produto** e **Data de entrega solicitada**, o sistema selecciona a lista de prezos aplicable en función da data de entrega. Consúltanse os elementos da lista de prezos relacionados co produto coincidente. Os valores da unidade e do grupo de unidades predefinidos na configuración do rexistro de elementos da lista de prezos. |
| Unidade | Este valor predefinido é a unidade configurada no rexistro de elementos da lista de prezos. Pode cambiar isto por outra unidade segundo sexa necesario.| A combinación de produto e unidade úsase para predefinir o prezo unitario na liña de subcontrato para os produtos de catálogo existentes. |
| Prezo por unidade | O valor do campo do prezo unitario é o predefinido usando a combinación do produto e a unidade dos elementos da lista de prezos relacionados que é aplicable para a data de entrega solicitada da liña de subcontrato.  |Nada |
| Subtotal | Este campo de só lectura calcúlase como Cantidade x Prezo unitario se os dous campos teñen valores introducidos. Se o campo **Cantidade**, o campo **Prezo unitario** ou ambos están baleiros, pode introducir un valor manualmente.  |Nada |
| Imposto de vendas | Introduza o valor do imposto sobre as vendas. |Nada |
| Cantidade total | Este campo calculado mostra o importe total da liña de subcontrato despois de incluír os impostos. O valor deste campo calcúlase como Subtotal + Imposto. |Nada |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
