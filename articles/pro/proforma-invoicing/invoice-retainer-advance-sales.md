---
title: Facturar unha retención ou un adianto
description: Este tema ofrece información sobre como facturar unha retención ou un adianto en Project Operations.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 12bf3822227badcf8c83d84d6aef6c0fdc7a972a
ms.sourcegitcommit: 250270409412ba4cad95fbd4c345a80d3d2b3e53
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 11/21/2020
ms.locfileid: "4596190"
---
# <a name="invoice-a-retainer-or-an-advance"></a>Facturar unha retención ou un adianto

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Dynamics 365 Project Operations admite contratos baseados en retencións e adiantos únicos. Nun contrato de proxecto, pode rexistrar unha programación de retencións ou un adianto único. Non obstante, o rexistro a nivel de contrato do proxecto non pon de inmediato dispoñible unha retención nin un adianto para o seu uso. Para usar unha retención ou un adianto nunha factura que realmente cobra ao cliente, primeiro debe facturarse a retención ou o adianto.

Complete os pasos seguintes para facturar unha retención ou un adianto.

1. Seleccione **Vendas** > **Facturación** > **Retencións e adiantos**. 
2. Na páxina **Adiantos e retencións**, use o filtro para seleccionar a retención ou o adianto específico para facturar e márqueo como **Listo para facturar**.
3. Crea unha factura manualmente desde a lista **Contrato de proxecto** ou a páxina de detalle. A retención ou o adianto móstrase no borrador de factura na sección **Adiantos e retencións** na páxina **Factura**.
4. Confirme a factura. Isto fará que a retención ou o adianto estean dispoñibles para o seu uso. Pode verificar a factura na páxina de lista **Retencións e adiantos**. Para un adianto ou retención facturado, o importe dispoñible móstrase na grade.

## <a name="create-a-retainer-or-advance-from-the-invoice-grid"></a>Crear unha retención ou un adianto desde a grade de facturas

Podes crear unha retención ou un adianto directamente nunha factura.

1. Nun borrador de factura, na subgrade **Adiantos e retencións**, seleccione **Novo** para crear un novo adianto ou retención. 
2. Na páxina **Creación rápida**, engada a información necesaria e logo seleccione **Gardar**. A retención ou o adianto créase no contrato do proxecto relacionado coa factura. A retención ou o adianto márcase automaticamente como **Listo para facturar** e logo engádese á subgrade **Adiantos e retencións** na páxina **Factura**.

## <a name="reconcile-an-invoiced-retainer-or-advance"></a>Conciliar unha retención ou un adianto facturado

Despois de facturar unha retención ou un adianto, pódense utilizar ou conciliar nunha factura con tempo, gastos, fitos ou outros cargos baseados no proxecto. O cliente verá reducido o importe da súa factura polo importe da retención ou o adianto utilizado nesta factura.

En cada factura que se xera para un contrato de proxecto que facturou retencións ou adiantos, a Project Operations aplica automaticamente a retención ou o adianto á factura.

Isto pódese ver na grade **Retencións e adiantos aplicados** na páxina **Factura**. A seguinte táboa ofrece información sobre os campos da grade **Retencións e adiantos aplicados** da páxina **Factura do proxecto**.

| Campo | Localización | Descripción | Impacto descendente |
| --- | --- | --- | --- |
| Descripción | Grade **Retencións e adiantos aplicados** na páxina **Factura do proxecto**. |Este campo de só lectura ofrece unha descrición da retención ou o adianto utilizado nesta factura. Este valor non se pode cambiar na factura. Este valor pódese actualizar na subgrade da páxina **Contrato do proxecto**. | Este campo pódese mostrar ao cliente na factura impresa para indicar que a retención ou o adianto se aplica na factura. |
| Data de entrega | Grade **Retencións e adiantos aplicados** na páxina **Factura do proxecto**.  | Este campo de só lectura indica a data da factura da retención ou o adianto utilizado nesta factura. Este valor non se pode cambiar na factura. Este valor pódese actualizar na subgrade da páxina **Contrato do proxecto**. | Este campo pódese mostrar ao cliente na factura impresa para indicar a data na que a retención ou o adianto se facturou por primeira vez ao cliente. |
| Importe  | Grade **Retencións e adiantos aplicados** na páxina **Factura do proxecto**.  | Este campo de só lectura indica o importe da retención ou o adianto utilizado nesta factura. Este valor non se pode cambiar na factura. Este valor pódese actualizar na subgrade da páxina **Contrato do proxecto**. | Este campo pódese mostrar ao cliente na factura impresa para indicar o importe orixinal da retención ou o adianto que cliente pagou o cliente. |
| Importe usado | Grade **Retencións e adiantos aplicados** na páxina **Factura do proxecto**.  | Este campo de só lectura proporciona o valor calculado que resume canto se utilizou da retención ou do adianto. | Este campo pódese mostrar ao cliente na factura impresa para indicar o importe orixinal desta retención ou adianto que xa se utilizou. |
| Importe estendido | Grade **Retencións e adiantos aplicados** na páxina **Factura do proxecto**.  | Este campo editable de só lectura indica o importe da retención ou o adianto que se está a utilizar nesta factura de proxecto. Esta cantidade non pode ser superior á dispoñible no adianto. O sistema calcula isto automaticamente como a diferenza entre os campos **Importe** e **Importe utilizado** da grade. Pode diminuír esta cantidade para usar menos do dispoñible, pero non pode aumentar o importe para usar máis do dispoñible. | Este campo pódese mostrar ao cliente na factura impresa para indicar o importe orixinal desta retención ou adianto que se vai utilizar na factura. |
| Importe da retención do saldo. | Grade **Retencións e adiantos aplicados** na páxina **Factura do proxecto**.  | Este campo de só lectura indica o valor do importe da retención ou o adianto que quedará despois de confirmarse a factura. | Este campo pódese mostrar ao cliente na factura impresa para indicar o importe que quedará desta retención ou adianto despois de que se conforme e pague a factura. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]