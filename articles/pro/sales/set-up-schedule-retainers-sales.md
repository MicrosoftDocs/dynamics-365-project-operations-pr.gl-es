---
title: Configurar unha programación de retención
description: Este tema ofrece información sobre como configurar unha programación de retencións en Project Operations.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d90781407f11c93b9fb9e0cd2446e102e216b8db
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272255"
---
# <a name="set-up-a-retainer-schedule"></a>Configurar unha programación de retención

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

As programacións de retencións configúranse na páxina **Contrato de proxecto** en Dynamics 365 Project Operations.

1. Na páxina **Contrato de proxecto**, no separador **Adiantos e retencións**, seleccione **Configurar programación de retencións**.
2. Na páxina de diálogo que se abre, móstranse os campos listados na seguinte táboa. A táboa dá unha idea de como os valores introducidos impactan ou inflúen na programación de retencións que se creará.

| Campo | Descripción | Impacto descendente |
| --- | --- | --- |
| Cliente do contrato do proxecto | O cliente do contrato a quen se lle facturará esta retención ou adianto. | Se ten varios clientes no contrato e se necesita facturar a cada un deles un importe específico de retención ou adianto, cree manualmente unha factura para cada cliente. |
| Inicio da programación de retención | Escriba a data de comezo da programación de retencións. | É posible que esta data non sexa a data na que se creou o primeiro adianto ou retención. A data na que se crea a primeira retención ou adianto tamén está influenciada pola frecuencia da factura. |
| Finalización da programación de retención | Escriba a data de finalización da programación de retencións. | É posible que esta data non sexa a data na que se creou o último adianto ou retención. A data na que se crea a última retención ou adianto tamén está influenciada pola frecuencia da factura. |
| Número de retencións que se van crear | Cando introduce o número de retencións para crear, o sistema usa a data e a frecuencia de inicio para crear o número neste campo. | Cando este campo se actualiza manualmente, o sistema ignora o valor do campo **Fin da programación de retencións** e no seu lugar crea o número específico de retencións ou adiantos. |
| Frecuencia da factura | Frecuencia coa que a aplicación creará retencións e adiantos. | Este valor inflúe directamente no número de retencións e adianto e nas datas de creación. |
| Cantidade total | O importe total é o importe que se divide nos pagamentos individuais de retencións ou adiantos que se crearán. | Non hai ningún impacto descendente para este campo. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]