---
title: Verificación de facturas de fornecedor con datos reais aprobados
description: Este artigo explica como Microsoft Dynamics 365 Project Operations permite aos xestores de proxectos verificar as facturas dos fornecedores cos datos reais que foron aprobadas cando os contratistas realizaron traballos e rexistraron o tempo, e os gastos e materiais que foron utilizados polos membros do equipo do proxecto.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 67e0a0143fa354ca9a87bfac5fbbd6306a97811c
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522932"
---
# <a name="verification-of-vendor-invoices-with-approved-actuals"></a>Verificación de facturas de fornecedor con datos reais aprobados

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Microsoft Dynamics 365 Project Operations permite que os xestores de proxectos verifiquen as liñas de factura do fornecedor das seguintes formas:

- Use o campo **Estado de verificación** nas liñas de factura do fornecedor.
- Se as liñas de factura do fornecedor fan referencia a unha liña de subcontratación, vincule os datos reais de custo da actividade do subcontratista a esas liñas de factura do fornecedor. A ligazón créase facendo coincidir os datos reais de custo coas liñas de factura do fornecedor.

    > [!NOTE]
    > Aínda que se pode seguir o estado de verificación para as liñas de facturas de fornecedor que non fan referencia a un subcontrato, os datos reais de custo non se poden vincular a esas liñas de facturas de fornecedor.

## <a name="verification-status"></a>Estado da verificación

O campo **Estado de verificación** nunha liña de factura de fornecedor indica ese estado da verificación. Admítense os seguintes estados:

1. Sen iniciar
2. En curso
3. Concluída

As liñas de factura de fornecedor que teñen un estado de verificación de **Non iniciada** pódense editar.

As liñas de factura de fornecedor que teñen un estado de verificación de **En progreso** xa non se poden editar. Para unha liña de factura de fornecedor que fai referencia a un subcontrato, o estado de verificación establécese automaticamente en **En progreso** tan pronto como o primeiro dato real custo coincida coa liña de factura do fornecedor.

As liñas de factura de fornecedor que teñen un estado de verificación de **Completa** xa non se poden editar. Cando todas as liñas dunha factura de fornecedor teñan este estado de verificación distinto, a factura do fornecedor pódese confirmar.

## <a name="match-cost-actuals-to-vendor-invoice-lines"></a>Coincidencia dos datos reais de custo coas liñas de factura de fornecedor

A coincidencia dos datos reais de custo axuda co proceso de verificación nunha liña de factura de fornecedor. Para facer coincidir os datos reais de custo cunha liña de factura de fornecedor, siga estes pasos.

1. Abra a liña de factura do fornecedor e seleccione o separador **Datos reais de custo sen coincidencia**. Unha grade mostra unha lista de datos reais de custo que fan referencia á mesma liña de subcontrato que a liña de factura do fornecedor.
2. Seleccione un ou máis dos datos reais de custo e, a seguir, seleccione **Facer coincidir** na barra de ferramentas situada enriba da grade. O sistema valida que os datos reais de custo seleccionados poden coincidir. Despois de pasar a validación, os datos reais de custo están ligados á liña de factura do fornecedor.

### <a name="validation-criteria-that-are-used-to-link-cost-actuals-to-vendor-invoice-lines"></a>Criterios de validación que se utilizan para vincular os datos reais de custo ás liñas de factura de fornecedor

Durante o proceso de coincidencia, só se pode establecer un vínculo entre un dato real de custo e unha liña de factura do fornecedor se se cumpren as dúas condicións seguintes:

- O campo **Estado de axuste** para cada dato real de custo seleccionado debe estar en branco. Noutras palabras, os datos reais de custo non deben ser substituídos por outros datos reais de custo durante un proceso de recuperación, cancelación de aprobación ou diario de corrección.
- Os valores dos seguintes campos coinciden entre a liña de factura do fornecedor e o dato real de custo seleccionado. Se algún campo non está definido na liña de factura do fornecedor, non se considera para a coincidencia.

    - Contrato do proxecto
    - Liña de contrato do proxecto
    - Clase de transacción
    - Project
    - Tarefa
    - Categoría de recurso
    - Categoría da transacción
    - Produto
    - Liña de subcontratación
    - Recurso reservable

## <a name="unmatch-cost-actuals-from-a-vendor-invoice-line"></a>Anular coincidencia de datos reais de custo dunha liña de factura de fornecedor

A anulación da coincidencia dos datos reais de custo tamén pode axudar co proceso de verificación dunha factura de fornecedor ao permitir que se eliminen as ligazóns establecidas previamente. Os datos reais de custo só se poden desvincular das liñas de factura de fornecedor que teñen un estado de verificación de **En progreso**. Para anular a coincidencia dos datos reais de custo dunha liña de factura de fornecedor, siga estes pasos.

1. Abra a liña de factura do fornecedor e seleccione o separador **Datos reais de custo con coincidencia**. Unha grade mostra unha lista de datos reais de custo que fan referencia á liña de factura do fornecedor.
2. Seleccione un ou máis dos datos reais de custo e, a seguir, seleccione **Anular coincidencia** na barra de ferramentas situada enriba da grade.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
