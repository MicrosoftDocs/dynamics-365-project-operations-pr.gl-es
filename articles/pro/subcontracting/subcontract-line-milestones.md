---
title: Fitos da liña de subcontrato
description: Este artigo explica como crear e manter un calendario de facturas baseado en fitos para un subcontrato cun provedor.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 431a57adf82c79f72d44886636183d48e0931f53
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522417"
---
# <a name="subcontract-line-milestones"></a>Fitos da liña de subcontrato

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

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

    | Campo | Descripción |Impacto funcional|
    | --- | --- |----------------------|
    | Nome do fito | O nome do fito. |Esta amosarase como a primeira columna en todas as buscas baseadas en fitos de liñas de subcontrato. A liña de factura do fornecedoor que se crea con base neste fito tamén empregará o nome do fito da liña de subcontrato como nome predefinido da liña de factura do fornecedor.|
    | Descripción | Unha descrición do fito. |A liña de factura do fornecedoor que se crea con base neste fito tamén empregará a descrición do fito da liña de subcontrato como descrición predefinida da liña de factura do fornecedor.|
    | Data do fito | A data na que o proceso de creación automática de facturas debería buscar o estado deste fito para consideralo para a facturación.| Este valor utilizarase como data predefinida da liña de factura do fornecedor ao facturar esta liña de subcontrato. |
    | Importe | O importe ou o valor do fito que se facturará ao cliente. |Este valor utilízase como importe predefinido da liña de factura do fornecedor ao facturar esta liña de subcontrato. |
    | Impostos | O importe do imposto aplicado no fito.| Este valor utilízase como importe de impostos predefinido da liña de factura do fornecedor ao facturar esta liña de subcontrato. |
    | Importe despois de impostos | Este campo de só lectura calcúlase como Importe + Imposto.|Este valor utilízase como valor predefinido da liña de factura do fornecedor ao facturar esta liña de subcontrato. |
    | Estado da factura | Cando se crea o fito, este estado sempre se define como **Non está listo para a facturación**.|  Cando o estado é **Listo para facturar**, a creación da factura do fornecedor inclúe este fito na factura do fornecedor. |

5. Seleccione **Gardar e pechar**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
