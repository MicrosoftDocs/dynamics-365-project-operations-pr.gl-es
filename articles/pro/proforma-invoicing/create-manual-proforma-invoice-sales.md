---
title: Crear unha factura proforma manual - lite
description: Este tema ofrece información sobre a creación dunha factura proforma manual en Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 87ef090454b2a7ab997e7c21d8d10badc31c8235
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176384"
---
# <a name="create-a-manual-proforma-invoice---lite"></a>Crear unha factura proforma manual - lite

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

En Dynamics 365 Project Operations, as facturas proforma pódense crear manualmente segundo sexa necesario. Pode crear manualmente unha factura proforma desde a páxina de lista **Contratos de proxectos** ou desde a páxina de detalles **Contrato do proxecto**.

##  <a name="project-contracts-list-page"></a>Páxina de lista Contratos de proxectos

Desde a páxina de lista **Contratos de proxectos**, seleccione un ou máis contratos de proxectos e cree facturas para todos os rexistros seleccionados.

O sistema comproba para ver cal dos contratos do proxecto seleccionado ten un traballo pendente **Listo para facturar** con data anterior á data de hoxe. A partir deses contratos, o sistema crea borradores de facturas proforma. Se un contrato de proxecto ten varios clientes, pode haber unha factura creada por cliente e varias facturas por contrato de proxecto.

Todas as facturas do proxecto creado están dispoñibles na páxina **Factura** na sección **Facturación** da área **Vendas**.

## <a name="project-contract-details-page"></a>Páxina de detalles de Contrato de proxecto

Tamén se pode crear unha factura proforma desde a páxina de detalles **Contrato de proxecto**, que crea a factura dese contrato de proxecto específico. O sistema verifica que o contratos do proxecto ten un traballo pendente **Listo para facturar** con data anterior á data de hoxe. A partir destes contratos, o sistema crea borradores de facturas proforma en función do número de clientes en cada liña de contrato.

Cando se crea unha única factura proforma, ábrese a páxina **Factura**. Se hai varias facturas creadas para ese contrato de proxecto, ábrese a páxina de lista **Facturas** para amosar todas as facturas creadas.
