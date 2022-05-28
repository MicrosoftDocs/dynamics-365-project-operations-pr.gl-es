---
title: Verificación de facturas de provedores con datos reais aprobados
description: Este tema explica como Microsoft Dynamics 365 Project Operations imos que os xestores de proxectos verifiquen as facturas dos provedores coas cifras reais que foron aprobadas cando os contratistas realizaron traballos e rexistraron o tempo, e os gastos e materiais que foron utilizados polos membros do equipo do proxecto.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3350a51bde2872036b79a789fae23ea6790fb21a
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585468"
---
# <a name="verification-of-vendor-invoices-with-approved-actuals"></a>Verificación de facturas de provedores con datos reais aprobados

[!include [banner](../../includes/dataverse-preview.md)]

_ **Aplícase a:** Implementación simplificada: tramitar a facturación proforma

Microsoft Dynamics 365 Project Operations imos que os xestores de proxectos verifiquen as liñas de factura do provedor das seguintes formas:

- Usa o **Estado de verificación** campo nas liñas de factura do provedor.
- Se as liñas de factura do provedor fan referencia a unha liña de subcontrato, vincula os custos reais da actividade do subcontratista a esas liñas de factura do provedor. A ligazón créase facendo coincidir os custos reais coas liñas de factura do provedor.

    > [!NOTE]
    > Aínda que se pode seguir o estado de verificación para as liñas de factura de provedores que non fan referencia a un subcontrato, os custos reais non se poden vincular a esas liñas de factura de provedores.

## <a name="verification-status"></a>Estado de verificación

O **Estado de verificación** campo nunha liña de factura de provedor indica ese estado da verificación. Admítense os seguintes estados:

1. Sen iniciar
2. En curso
3. Concluída

Liñas de facturas de provedores que teñen un estado de verificación de **Non comezou** pódese editar.

Liñas de facturas de provedores que teñen un estado de verificación de **En progreso** xa non se pode editar. Para unha liña de factura de provedor que fai referencia a un subcontrato, o estado de verificación establécese automaticamente en **En progreso** tan pronto como o primeiro custo real coincida coa liña de factura do provedor.

Liñas de facturas de provedores que teñen un estado de verificación de **Completa** xa non se pode editar. Cando todas as liñas dunha factura de provedor teñen este estado de verificación, pódese confirmar a factura de provedor.

## <a name="match-cost-actuals-to-vendor-invoice-lines"></a>Relaciona os custos reais coas liñas de factura do provedor

A coincidencia dos custos reais axuda co proceso de verificación nunha liña de factura de provedor. Para relacionar os custos reais cunha liña de factura de provedor, siga estes pasos.

1. Abra a liña de factura do provedor e seleccione **Custos reais incomparables** ficha. Unha cuadrícula mostra unha lista de custos reais que fan referencia á mesma liña de subcontrato que a liña de factura do provedor.
2. Seleccione un ou máis dos custos reais e, a continuación, seleccione **Partido** na barra de ferramentas situada enriba da grade. O sistema valida que os custos reais seleccionados poidan coincidir. Despois de pasar a validación, os custos reais están ligados á liña de factura do provedor.

### <a name="validation-criteria-that-are-used-to-link-cost-actuals-to-vendor-invoice-lines"></a>Criterios de validación que se utilizan para vincular os custos reais ás liñas de facturas de provedores

Durante o proceso de coincidencia, só se pode establecer un vínculo entre un custo real e unha liña de factura do provedor se se cumpren as dúas condicións seguintes:

- O **Estado de axuste** campo para cada custo real seleccionado debe estar en branco. Noutras palabras, os custos reais non deben ser substituídos por outros custos reais durante un proceso de retirada, cancelación de aprobación ou diario de corrección.
- Os valores dos seguintes campos coinciden entre a liña de factura do provedor e o custo real seleccionado. Se algún campo non está definido na liña de factura do provedor, non se considera para a correspondencia.

    - Contrato do proxecto
    - Liña de contrato do proxecto
    - Clase de transacción
    - Project
    - Tarefa
    - Categoría de recursos
    - Categoría da transacción
    - Produto
    - Liña de subcontratación
    - Recurso reservable

## <a name="unmatch-cost-actuals-from-a-vendor-invoice-line"></a>Descompare os custos reais dunha liña de factura de provedor

A non coincidencia dos custos reais tamén pode axudar co proceso de verificación dunha factura do provedor ao permitir que se eliminen as ligazóns establecidas previamente. Os custos reais só poden ser incomparables das liñas de factura de provedores que teñan un estado de verificación de **En progreso**. Para non comparar os custos reais dunha liña de factura de provedor, siga estes pasos.

1. Abra a liña de factura do provedor e seleccione **Custos reais coincidentes** ficha. Unha cuadrícula mostra unha lista de custos reais que fan referencia á liña de factura do provedor.
2. Seleccione un ou máis dos custos reais e, a continuación, seleccione **Descompar** na barra de ferramentas situada enriba da grade.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
