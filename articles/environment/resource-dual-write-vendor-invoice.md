---
title: Integración de facturas do fornecedor
description: Este tema ofrece información sobre a integración de facturas do fornecedor en Project Operations.
author: sigitac
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 538a2694591f1d0d368ee0ffeed9bdf12cb47420c3d0571f75185fe433f23436
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986489"
---
# <a name="vendor-invoice-integration"></a>Integración de facturas do fornecedor

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

A adquisición relacionada co proxecto en Dynamics 365 Project Operations pódese rexistrar indo a **Contas pendentes de pago** > **Facturas** > **Facturas pendentes do fornecedor** e usando un documento de factura pendente do fornecedor. Para obter máis información, consulte [Comprar materiais sen fornecemento usando unha factura pendente do fornecedor](../procurement/pending-vendor-invoices.md).

> [!IMPORTANT]
> Antes de empregar a funcionalidade descrita neste tema, revise e aplique as configuracións necesarias. Para obter máis información, consulte [Activar materiais sen fornecemento e facturas pendentes do fornecedor](../procurement/configure-materials-nonstocked.md).

En Project Operations, as facturas do fornecedor relacionadas co proxecto contabilízanse utilizando regras especiais de contabilización:

- O custo relacionado co proxecto (incluído o imposto non recuperable) non se contabiliza de inmediato na conta de custos do proxecto no libro maior. En vez diso, o custo contabilízase na **Conta de integración de adquisicións**. Esta conta está configurada en **Xestión e contabilidade de proxectos** > **Configuración** > **Parámetros de xestión e contabilidade de proxectos** noseparador **Project Operations en Dynamics 365 Customer Engagement**.
- A escrita dual sincroniza os detalles da factura do fornecedor con Microsoft Dataverse usando os seguintes mapas de táboa:

     - **Entidade de exportación de facturas do fornecedor do proxecto de integración de Project Operations (msdyn_projectvendorinvoices)**: Este mapa de táboa sincroniza a información da cabeceira da factura do fornecedor. Só as facturas do fornecedor con polo menos unha liña que contén un ID de proxecto se sincronizan con Dataverse.
     - **Entidade de exportación de liñas de factura do fornecedor do proxecto de integración de Project Operations (msdyn_projectvendorinvoicelines)**: Este mapa de táboa sincroniza a información da liña da factura do fornecedor. Só as liñas que conteñen un ID de proxecto se sincronizan con Dataverse.

     > [!NOTE]
     > Os detalles da factura do fornecedor en Dataverse non son editables.

O libro auxiliar fiscal, o libro auxiliar do fornecedor e outras contabilizacións financeiras rexístranse segundo o caso en Dynamics 365 Finance cando se contabiliza a factura do fornecedor.

![Integración de facturas do fornecedor.](media/DW7VendorInvoice.png)

Cando se escriben os rexistros nunha entidade **Factura do fornecedor** en Dataverse, comeza un proceso automatizado de aprobación dos rexistros. Se é necesario, pódese revisar o estado do proceso de aprobación automatizado en Dataverse indo a **Configuración avanzada** > **Sistema** > **Traballos do sistema**. Despois de completar a aprobación, o sistema crea rexistros de clases de transaccións de material na entidade **Datos reais**.

Os datos reais relacionados co material son entón procesados usando o mapa de táboa de escrita dual **Datos reais de integración de Project Operations (msdynactuals)**. Para obter máis información, consulte [Estimacións e datos reais do proxecto](resource-dual-write-estimates-actuals.md).

O proceso periódico **Importar desde a transición** crea liñas de diario de integración de Project Operations relacionadas coa factura do fornecedor. A conta de compensación predefinida á conta de integración de adquisicións. Cando se contabiliza o diario de integración de contabilización, bórrase o saldo da conta para a transacción de factura do fornecedor e móvese o importe da liña á conta de custos do proxecto. Tamén se crean transaccións de libro auxiliar do proxecto para fins de facturación e recoñecemento de ingresos.
