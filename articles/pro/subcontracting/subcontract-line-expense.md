---
title: Liñas de subcontrato para categorías de gastos
description: Este artigo explica como rexistrar liñas de subcontrato para gastos e usar os campos para rexistrar a compra de tempo dos provedores.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0b02a8aa0fce7bcb52374c0755d4bb85db16dad3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921024"
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

| **Campo** | **Descrición** | **Impacto funcional** |
| --- | --- | --- |
| Nome | Nome da liña de subcontrato para axudar na identificación. | Esta amosarase como a primeira columna en todas as buscas baseadas en liñas de subcontrato. |
| Descripción | Unha breve descrición das categorías de gastos que se están a mercar na liña de subcontrato. | Nada |
|Tipo de liña | Este campo ten un valor predefinido de **Baseado na cantidade**. |Nada |
| Método de facturación | Este é un conxunto de opcións que representa os dous principais modelos de contratación admitidos por Project Operations: **Prezo fixo** e **Tempo e Material**. | Unha programación de facturas baseada en fitos está dispoñible para as liñas de subcontrato se se selecciona o método de facturación de prezo fixo. |
| Clase de transacción | Este campo ten un valor predefinido de **Tempo**. Para crear liñas de subcontrato para mercar produtos, configure o campo **Clase de transacción** en **Gasto**.  | Isto indica que a liña de subcontrato se está a utilizar para rexistrar a compra dunha categoría de gastos que se utilizarán en proxectos. |
| Categoría da transacción | Mostra unha lista de categorías de transaccións activas no sistema. |Nada |
| Inicio solicitado | Introduza a data na que as categorías de compra deben estar dispoñibles do fornecedor. | O inicio solicitado úsase para escoller unha lista de prezos do proxecto das listas de prezos do proxecto anexas ao subcontrato. O custo da categoría na liña de subcontrato procede desa lista de prezos. |
| Finalización solicitada | Introduza a data na que xa non serían necesarias as categorías de compra. | Utilizarase para amosar avisos cando un xestor de proxecto asocie esta liña de subcontrato a estimacións de gastos específicas do proxecto que sexan necesarias despois desta data. |
| Cantidade solicitada | Cantidade da categoría que se compra ao fornecedor. | Isto usarase para amosar avisos cando un xestor de proxecto está a extraer demasiado desta cantidade.|
| Grupo de unidades | O valor predefinido baséase no grupo de unidades predefinido configurado para a categoría seleccionada. |Nada |
| Unidade | O valor predefinido baséase na unidade predefinida configurada para a categoría seleccionada.  | A combinación de **Categoría** e **Unidade** usarase como predefinida ou computada para o prezo unitario da liña de subcontrato.  |
| Prezo por unidade | O valor predefinido usa a combinación de **Categoría** e **Unidade** dos prezos de categoría relacionados coa lista de prezos do proxecto, que é aplicable para o inicio solicitado da liña de subcontrato. |Nada |
| Subtotal | Este é un campo de só lectura que se calcula como Cantidade X Prezo unitario, se se introducen tanto a cantidade como os valores do prezo unitario. Se un ou ambos campos están en branco, pode introducir un valor neste campo. |Nada |
| Imposto de vendas | Introduza o importe do imposto de vendas. |Nada |
| Cantidade total | O importe total da liña de subcontrato, incluídos os impostos. Este campo calcúlase como Subtotal + Imposto sobre as vendas. |Nada |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
