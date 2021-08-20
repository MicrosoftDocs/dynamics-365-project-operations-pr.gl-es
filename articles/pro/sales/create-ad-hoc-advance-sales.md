---
title: Creación dun adianto ad hoc nun contrato
description: Este tema ofrece información sobre como crear un adianto nun contrato segundo sexa necesario.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: bceed1372dbaf523426a4c34da7152d77fe108240c8c3e4e1390c43b1cf536a4
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6999134"
---
# <a name="creating-an-ad-hoc-advance-on-a-contract"></a>Creación dun adianto ad hoc nun contrato

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