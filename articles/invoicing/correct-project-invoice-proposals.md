---
title: Corrixir a contabilidade no borrador de propostas de factura do proxecto
description: Este artigo explica como axustar a información relacionada coa contabilidade nun borrador de proposta de factura.
author: sigitac
ms.date: 01/05/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 32f566a798d07b698693392f3aa1823f91fe5408
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921208"
---
# <a name="correct-the-accounting-on-draft-project-invoice-proposals"></a>Corrixir a contabilidade no borrador de propostas de factura do proxecto

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

O xestor do proxecto mantén os *Detalles operativos* para as facturas do proxecto nunha factura proforma. Estes detalles inclúen a decisión sobre as horas, gastos, materiais ou fitos que se deben facturar, as taxas e a aplicación dos importes de adiantos e retencións. Despois de confirmar a factura proforma orixinal, pode axustar os detalles operativos creando e confirmando unha [factura pro forma correctiva](../proforma-invoicing/corrective-invoices.md).

os *Detalles de contabilidade* para as facturas do proxecto mantéñense nun documento de factura orientado ao cliente. Estes detalles inclúen o cálculo do imposto sobre as vendas e as dimensións financeiras que se aplican á factura. Este artigo ofrece detalles sobre como se poden axustar estes detalles de contabilidade nun borrador de proposta de factura do proxecto.

## <a name="adjust-sales-tax"></a>Axustar imposto sobre as vendas

Os grupos de impostos sobre as vendas de facturación por defecto e os grupos de impostos sobre as vendas de elementos pódense axustar directamente no documento de proposta de factura. Para axustar estes grupos, seleccione **Editar** e, a seguir, en cada liña de proposta de factura do proxecto, introduza un novo valor no campo **Grupo do imposto sobre as vendas** ou **Grupo do imposto sobre as vendas de elementos**.

## <a name="adjust-financial-dimensions"></a>Axustar as dimensións financeiras

### <a name="header-dimensions"></a>Dimensións da cabeceira

De forma predefinida, as dimensións financeiras das facturas derívanse dos rexistros de transaccións do proxecto non facturados que se están a facturar. Non obstante, a configuración do sistema permítelle utilizar dimensións financeiras na cabeceira das propostas de factura do proxecto para contabilizar os saldos dos clientes. Para activar esta función, seleccione **Permitir actualizacións das dimensións do proxecto para as contas pendentes de cobro** no separador **Finanzas** da páxina **Xestión e contabilidade de proxectos**.

As dimensións financeiras das cabeceiras das facturas pódense editar antes de que se contabilice unha factura. Na páxina **Proposta de factura do proxecto**, cambie á vista **Cabeceira** e, a seguir, edite os valores no separador **Dimensións financeiras**.

A vista **cabeceira** está dispoñible só despois de que o administrador do sistema active a funcionalidade **Usar os formularios de proposta de factura e diario de factura do proxecto coa vista de Cabeceira e Liñas** na área de traballo **Xestión de funcionalidades**. Esta función require a actualización de Finance 10.0.25 ou posterior.

### <a name="line-dimensions"></a>Dimensións de liña

As dimensións financeiras non se poden editar directamente nunha liña de proposta de factura do proxecto. Pola contra, siga estes pasos para axustar as dimensións financeiras nunha proposta de factura do proxecto.

1. Na proposta de factura do proxecto, seleccione **Elimina todas** para eliminar as liñas de proposta de factura do proxecto.

    O botón **Elimina todas** está dispoñible só despois de que o administrador do sistema active a funcionalidade **Eliminar as liñas de proposta de factura cando se usa Project Operations para situacións baseadas en recursos/sen fornecemento** na área de traballo **Xestión de funcionalidades**.

2. Axustar as dimensións financeiras:

    - **Transaccións a conta (fitos de facturación):** Vaia a **Todos os proxectos** \> **Xestionar** \> **Transaccións a conta** e seleccione o fito que require axuste. Entón, no separador **Dimensións financeiras**, actualice os valores segundo sexa necesario.
    - **Tempo, gastos e transaccións materiais:** Na páxina **Transaccións do proxecto contabilizadas**, seleccione **Axustar contabilidade** para actualizar as dimensións financeiras.

3. Despois de rematar de axustar os valores da dimensión financeira, vaia a **Xestión e contabilidade de proxectos** \> **Periódico** \> **Integración de Project Operations** e seleccione **Importar da táboa de transición** para executar o proceso periódico. Ese proceso utiliza os valores de dimensión financeira actualizados para recrear as liñas de proposta de factura do proxecto. Os valores actualizados úsanse entón no subrexistro do proxecto e no libro maior cando se publica a factura do proxecto.
