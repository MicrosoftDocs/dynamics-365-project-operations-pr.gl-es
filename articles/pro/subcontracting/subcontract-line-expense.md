---
title: Liñas de subcontrato para categorías de gastos
description: Este tema explica como rexistrar liñas de subcontrato para gastos e usar os campos para rexistrar a compra de tempo de fornecedores.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9e8e7bb66063dab6db1ac8da1753913aee0ef3fc
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323819"
---
#  <a name="subcontract-lines-for-expense-categories"></a>Liñas de subcontrato para categorías de gastos

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

Un subcontrato en Dynamics 365 Project Operations pode ter unha liña para categorías de gastos. As liñas de subcontrato para categorías de gastos permiten a un xestor de proxectos mercar categorías de servizos ou produtos a fornecedores que poden cobrar nun proxecto.

Para crear unha liña de subcontrato para categorías de gastos en Project Operations, complete os seguintes pasos.

1. No panel de navegación, seleccione **Subcontratos** e abra o subcontrato co que desexa traballar.
2. No separador **Liñas de subcontrato**, seleccione **Nova** para crear unha nova liña.
3. Na páxina **Creación rápida**, no campo **Clase de transacción**, seleccione **Gasto** e introduza ou seleccione calquera outra información de campo requirida.

A seguinte táboa ofrece información sobre os campos na páxina de detalles **Liña de subcontrato** páxina de detalles e a páxina **Creación rápida**.

| **Campo** |  **Descrición** |
| ----------| ---------------- |
| Nome | O nome da liña de subcontrato. |
| Descripción | Unha breve descrición das categorías de servizos ou produtos que se van mercar na liña de subcontrato. |
| Tipo de liña | Este campo ten un valor predefinido de **Baseado na cantidade**.  |
| Método de facturación | O método de facturación da liña de subcontrato. En función do método de facturación da liña, está dispoñible un calendario de facturas baseado en fitos para o método de facturación a prezo fixo.  |
| Clase de transacción | Este campo ten un valor predefinido de **Tempo**. Para crear liñas de subcontrato para mercar produtos, configure o campo **Clase de transacción** en **Gasto**. Este valor de campo indica que a liña de subcontrato vaise empregar para rexistrar a compra dunha categoría de produtos ou servizos que se utilizarán en proxectos. |
| Categoría da transacción | Seleccione a categoría da transacción. |
| Inicio solicitado | A data na que as categorías de compra deben estar dispoñibles no fornecedor. O inicio solicitado úsase para escoller unha lista de prezos do proxecto das listas de prezos do proxecto anexadas ao subcontrato. O custo da categoría na liña de subcontrato é o predefinido desa lista de prezos. |
| Finalización solicitada | A data na que xa non son necesarias as categorías de compra. Esta data activa unha advertencia cando un xefe de proxecto asocia esta liña de subcontrato a estimacións de gastos específicas nos proxectos que teñen data posterior a esta data. |
| Cantidade solicitada | A cantidade da categoría que se vai comprar ao fornecedor. Cando un xestor de proxectos supera a cantidade comprada, producirase unha advertencia.  |
| Grupo de unidades | Este valor de campo baséase no grupo de unidades predefinido que está configurado para a categoría seleccionada. |
| Unidade | Este valor de campo baséase na unidade predefinida que está configurada para a categoría seleccionada. A combinación de categoría e unidade úsase para predefinir o prezo unitario na liña de subcontrato. |
| Prezo por unidade | O valor do campo do prezo unitario é o predefinido na combinación da categoría e dos prezos da categoría relacionados coa lista de prezos do proxecto que é aplicable para o inicio solicitado da liña de subcontrato.  |
| Subtotal | Este campo de só lectura calcúlase automaticamente como prezo unitario da cantidade se se introducen tanto os valores de cantidade como os do prezo unitario. Se un ou ambos campos están baleiros, pode introducir manualmente un valor neste campo.  |
| Imposto de vendas | Introduza o importe do imposto de vendas.  |
| Cantidade total | O importe total da liña de subcontrato, incluídos os impostos. Este campo calcúlase como subtotal + imposto sobre as vendas.  |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
