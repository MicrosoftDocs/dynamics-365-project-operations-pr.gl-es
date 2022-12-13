---
title: Crear un anticipo ad hoc nun contrato de proxecto
description: Este artigo ofrece información sobre como crear un adianto nun contrato segundo sexa necesario.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 62e41e5faeb5e40143e26e2cdf48c1279941a6b4
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824842"
---
# <a name="create-an-ad-hoc-advance-on-a-project-contract"></a>Crear un anticipo ad hoc nun contrato de proxecto

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Microsoft Dynamics 365 Project Operations admite escenarios de facturación que implican pagamentos anticipados e adiantos. O proceso para usar **Adiantos** en **Project Operations** é semellante aos contratos de **Retención**. 

Complete os seguintes pasos para facturar ao cliente un adianto.

1. Vaia á páxina **Contrato do proxecto** e seleccione o separador **Adiantos e retencións**.
2. Na subgrade que lista todos os adiantos e pagamentos anticipados rexistrados previamente, seleccione **+ Nova retención de contrato de proxecto**. 

    Ábrese o formulario **Creación rápida** para rexistrar un pagamento anticipado ou un adianto.
    
3. A táboa seguinte mostra os campos para rexistrar un adianto e as consideracións que hai que ter en conta ao crear outros novos:

    | Campo | Descripción | Impacto descendente |
    | --- | --- | --- |
    | **Cliente do contrato do proxecto** | Este campo indica a que cliente do contrato se lle facturará este adianto. | Se ten varios clientes no contrato e quere facturar a cada un deles un importe específico de retención ou adianto, cree un adianto para cada cliente individualmente. |
    | **Descrición** | A descrición do propósito ou o momento do adianto para axudar a identificar este adianto. | Esta descrición móstrase na liña de factura deste adianto. |
    | **Importe** | O importe do pagamento anticipado ou adianto. | Este importe móstrase na liña de factura deste adianto. |
    | **Data da factura** | A data na que se factura este adianto ao cliente. | Esta é a data para o proceso automatizado de creación de facturas para crear unha liña de factura para este adianto. |
    | **Estado da factura** | Esta é unha configuración de opción que indica se este adianto se engade a un borrador de factura para este cliente. Os valores posibles son:</br>- **Non está listo para facturar**</br>- **Listo para facturar** | Cando un adianto ou pagamento anticipado está marcado como **Listo para facturar**, engádese como tempo de liña nun borrador de factura. Só se pode empregar un adianto totalmente facturado para conciliar cos custos do proxecto para o seguinte período de facturación. |

4. Seleccione **Gardar e pechar** no diálogo de creación rápida para rexistrar o adianto ou o pagamento anticipado.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
