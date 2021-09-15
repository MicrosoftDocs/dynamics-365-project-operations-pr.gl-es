---
title: Fitos da liña de subcontrato
description: Este tema explica como crear e manter unha programación de facturas baseada en fitos para un subcontrato cun fornecedor.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3301e5a627e4842009fcd5e352f1b76fd3053ee3
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323774"
---
# <a name="subcontract-line-milestones"></a>Fitos da liña de subcontrato

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

En Dynamics 365 Project Operations, unha liña de subcontrato cun método de facturación a prezo fixo pode especificar unha programación de facturas baseado en fitos co fornecedor.

Os fitos para a facturación do fornecedor pódense xerar automaticamente usando unha frecuencia establecida ou pódense crear manualmente.

## <a name="automatically-create-a-milestone-based-invoice-schedule-for-a-subcontract-line"></a>Crear automaticamente unha programación de facturas baseada en fitos para unha liña de subcontrato

Complete os seguintes pasos para xerar automaticamente unha programación de facturas baseada en fitos para un conxunto fixo de fitos igualmente distribuídos.

1. Vaia a **Configuración** > **Frecuencias da factura** e configure a frecuencia da factura para as liñas de subcontrato.
2. Abra a páxina **Subcontratos**, abra o subcontrato co que desexa traballar e logo abra a liña de subcontrato a prezo fixo para a que vai crear unha programación de fitos.
3. No separador **Fitos da liña de subcontrato**, seleccione **Xerar fitos periódicos**.
4. Na caixa de diálogo, introduza ou seleccione un intervalo de datas, o número de fitos e a frecuencia da factura. Pode seleccionar unha data de inicio ou pode seleccionar o número de fitos e a frecuencia ou a data de inicio da factura ou pode seleccionar a data de finalización e a frecuencia da factura. Non pode seleccionar a data de finalización e o número de fitos.
Usando esta información, o sistema xera fitos e rexistros que se amosan na grade **Fitos**.

   - **Nome do fito** - O nome do fito establécese na data do fito en función da frecuencia da factura.
   - **Data do fito** - A data baseada na frecuencia da factura.
   - **Importe do fito** - Calculado dividindo o importe subtotal na liña de subcontrato polo número de fitos.

Se a liña de subcontrato ten un valor no campo **Importe do imposto estimado**, este valor engádese a cada fito por igual ao xerar fitos periódicos.

A suma dos importes dos fitos da liña de subcontrato debe ser igual ao valor da liña de subcontrato. Se non son iguais, prodúcese un erro. Pode corrixir o erro e verificar que o total do fito sexa igual ao valor da liña de subcontrato creando, editando ou eliminando importes de fito e impostos. Despois de realizados os cambios, garde e actualice a páxina para asegurarse de que non haxa máis erros.

## <a name="manually-create-subcontract-line-milestones"></a>Crear manualmente fitos de liña de subcontrato

Os fitos de prezo fixo nunha liña de subcontrato pódense xerar manualmente cando non se dividen periodicamente. Para crear un fito de liña de subcontrato manualmente, complete os seguintes pasos.

1. No panel de navegación, seleccione **Subcontratos** e abra o subcontrato co que desexa traballar.
2. Abra a liña de subcontrato de prezo fixo para a que desexa crear un fito.
3. No separador **Fitos da liña de subcontrato**, na subgrade, seleccione **+ Novo fito da liña de subcontrato**.
4. Na páxina **Fito da nova liña de subcontrato**, introduza a información requirida baseándose na seguinte táboa.

    | Campo | Descripción |
    | --- | --- |
    | Nome do fito | O nome do fito. |
    | Descripción | Unha descrición do fito.  |
    | Data do fito | A data na que o proceso de creación automática de facturas debería buscar o estado deste fito para consideralo para a facturación. Este valor inclúese na liña de factura do fornecedor ao facturar este subcontrato. |
    | Importe | O importe ou o valor do fito que se facturará ao cliente. Este valor inclúese na liña de factura do fornecedor ao facturar este subcontrato. |
    | Impostos | O importe do imposto aplicado no fito. Este valor inclúese na liña de factura do fornecedor ao facturar este subcontrato. |
    | Importe despois de impostos | Este campo de só lectura que se calcula como Importe + Imposto. Este valor inclúese na liña de factura do fornecedor ao facturar este subcontrato. |
    | Estado da factura | Cando se crea o fito, este estado sempre se define como **Non está listo para a facturación**.  Cando o estado é **Listo para facturar**, a creación da factura do fornecedor inclúe este fito na factura do fornecedor. |

5. Seleccione **Gardar e pechar**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
