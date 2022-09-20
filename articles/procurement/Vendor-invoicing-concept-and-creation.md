---
title: Crear facturas de provedores
description: Este artigo describe o concepto de facturas de provedores e explica como crealas en Microsoft Dynamics 365 Project Operations.
author: suvaidya
ms.date: 9/12/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 7f6c1ec46f23b6823734b28755b80ced4e3f9325
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475461"
---
# <a name="create-vendor-invoices"></a>Crear facturas de provedores

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Para usar a funcionalidade descrita neste artigo, debes activar o **Activa o procesamento de subcontratos reais con Project Operations para escenarios baseados en recursos** característica no **Xestión de características** espazo de traballo.

Facturación de provedores en Microsoft Dynamics 365 Project Operations pode utilizarse para rexistrar os custos das entregas de servizos e/ou materiais nun proxecto que son rematados polos provedores.

Cando os servizos e/ou materiais son subcontratados a un provedor, un subcontrato representa o acordo contractual con ese provedor. A medida que o provedor presta os servizos ou a medida que se reciben e usan os materiais nas tarefas do proxecto, os custos rexístranse no proxecto. A continuación, o vendedor envía periodicamente facturas. Esas facturas verifícanse e combínanse cos custos que se rexistran no proxecto. Despois de completar o proceso de verificación, a factura do provedor é confirmada e liberada para o pago.

## <a name="scenarios-for-use"></a>Escenarios de uso

As facturas de provedores en Project Operations pódense usar para soportar dous escenarios distintos:

- Os clientes utilizan as experiencias completas de subcontratación.
- Os clientes non usan as experiencias de subcontratación completas, pero queren ter unha visión unificada dos custos dos proxectos en Operacións de proxectos.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Os clientes utilizan as experiencias completas de subcontratación

As experiencias de facturas de provedores proporcionan un xeito de verificar as entradas de tempo, o uso de material e as entradas de gastos que fan referencia a compoñentes subcontratados e combinalas coas liñas de facturas de provedores. Este proceso pódese usar para verificar a precisión das liñas de factura do provedor. Despois de completar o proceso de verificación e confirmar a factura do provedor, o sistema inverte os datos reais que foron rexistrados polos rexistros de tempo, gastos e uso de material aprobados e, a continuación, crea novos custos reais utilizando as liñas de factura do provedor.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Os clientes non usan as experiencias de subcontratación completas, pero queren ter unha visión unificada dos custos dos proxectos en Operacións de proxectos

Se estás facendo un seguimento do proceso de subcontratación nun sistema de terceiros, podes rexistrar os custos dese sistema de terceiros en Project Operations creando facturas de provedores que non fagan referencia a subcontratos. Deste xeito, os seus xestores de proxectos poden ter unha visión única e unificada de todos os custos dun proxecto determinado.

## <a name="create-vendor-invoices-in-project-operations"></a>Crea facturas de provedores en Project Operations

As facturas de provedores créanse en Dynamics 365 Finance usando o **Contas por pagar** módulo. Non podes crear facturas de provedores directamente en Dataverse.

### <a name="set-up-vendor-invoice-verification"></a>Configura a verificación da factura do provedor

Se a factura do provedor está destinada a un subcontrato en Dataverse, debes activar **É necesaria a verificación manual por PM** parámetro. A configuración da opción determina se a factura do provedor debe confirmarse automaticamente Dataverse, ou se require unha confirmación manual. A cabeceira de cada factura do provedor do proxecto inclúe unha opción co mesmo nome. De forma predeterminada, a opción da cabeceira de todas as facturas de provedores do proxecto está configurada co valor que definiches aquí. Non obstante, pode actualizar o valor segundo sexa necesario na cabeceira das facturas de provedores individuais.

Se a opción está definida como **Si**, a factura do provedor que se crea en Finanzas e se sincroniza con Dataverse ten **Borrador** estado. A factura debe ser validada e verificada polo xestor do proxecto e confirmada antes de ser procesada e contabilizada no proxecto específico e nas contas do libro maior en Finanzas.

Se a opción está definida como **Non**, a factura do provedor confírmase automaticamente. Non é necesaria ningunha acción adicional.

Para configurar a verificación da factura do provedor, siga estes pasos.

1. En Finanzas, vai a **Xestión de proxectos e contabilidade** \> **Montar** \> **Xestión de proxectos e parámetros contables**.
1. No **Financeiro** ficha, configure o **É necesaria a verificación manual por PM** opción a **Si** se a política da empresa require a verificación das facturas do provedor do subcontratista. Se non é necesaria a verificación do xestor do proxecto Dataverse, deixe o conxunto de opcións para **Non**. De forma predeterminada, a configuración empregarase en **Factura do provedor pendente** páxina.

> [!NOTE]
> Facturas de provedores que se crean para subcontratos en Dataverse só se pode procesar correctamente se o **É necesaria a verificación manual por PM** opción está definida en **Si**. O xestor do proxecto só pode relacionar manualmente os datos de custos de tempo, material e gastos que crean os subcontratistas coas liñas de factura do provedor se esta opción está definida como **Si**.

### <a name="set-up-a-procurement-integration-account-for-vendor-invoices"></a>Configure unha conta de integración de compras para as facturas de provedores

Cando se publica unha factura de provedor en Finanzas para operacións de proxectos - Contorno integrado (sen existencias), os datos financeiros publícanse na conta de integración de Adquisicións. O sistema xera os datos reais en Dataverse para a factura publicada. Estes datos reais publícanse en Finanzas mediante o diario de integración do proxecto. A publicación do diario de integración do proxecto contabiliza o custo real e inverte a conta de integración de Adquisicións.

Para configurar unha conta de integración de Adquisicións para facturas de provedores, siga estes pasos.

1. En Finanzas, vai a **Xestión de proxectos e contabilidade** \> **Montar** \> **Xestión de proxectos e parámetros contables**.
1. No **Operacións do proxecto na participación do cliente de Dynamics 365** ficha, seleccione **Materiais** \> **Conta de integración de compras**.

### <a name="create-and-post-subcontract-vendor-invoices"></a>Crear e publicar facturas de provedores de subcontratación

Cando un empregado de Contas a pagar recibe unha factura do subcontratista, créase unha nova factura en Finanzas.

1. En Finanzas, vai a **Contas a pagar** \> **Facturas** \> **Facturas de provedores pendentes**.
1. No **Panel de accións**, seleccione **Novo** para crear unha factura de provedor.
1. Na cabeceira da factura, no **Conta de factura** campo, seleccione **Subcontratista**.
1. Seleccione a data da factura.
1. No **Cabeceira** ficha, configure o **É necesaria a verificación manual por PM** opción a **Si**. A configuración predeterminada desta opción provén de **Xestión de proxectos e parámetros contables** páxina. Non obstante, pódese cambiar a nivel de factura do provedor.
1. No **Liña de factura** Ficha rápida, seleccione **Engadir liña** para crear unha liña de factura de provedor.
1. Seleccione a categoría de aprovisionamento que se creou para as liñas de subcontratación e introduza o prezo unitario, a unidade de medida e a cantidade.
1. Na sección de liñas de factura de provedores, no **Proxecto** ficha, seleccione o proxecto co que o subcontratista comparte a factura do subcontrato.
1. Seleccione a categoría do proxecto. Pode ser de calquera tipo **Elemento**, **·**, **·**, ou **Horario**.
1. Seleccione o rol só se a categoría de proxecto seleccionada é de **Hora** tipo.
1. Seleccione **Publicación** para publicar a factura do provedor.

Alternativamente, pode crear unha factura de provedor indo a **Contas por pagar** \> **Facturas** \> **Abrir facturas de provedores** e seleccionando **Novo**.

Cando se publica a factura do provedor, está dispoñible en Dataverse para a verificación e procesamento do xestor de proxectos.

## <a name="vendor-invoice-processing-in-dataverse"></a>Procesamento de facturas de provedores en Dataverse

Na factura do provedor que se crea en Dataverse, algúns valores de campo proceden da factura do provedor que se rexistra en Finanzas. Outros valores son valores predeterminados que proveñen do subcontrato.

Os seguintes campos e rexistros relacionados copiaranse do subcontrato á cabeceira da factura do provedor:

- Moeda
- Unidade de contratación
- Condicións de pagamento

Nas liñas de factura do provedor, Project Operations usa os seguintes valores de campo para introducir o subcontrato predeterminado e a referencia da liña de subcontrato:

- Clase de transacción
- Rol
- Categoría da transacción
- Campos de produtos
- Project
- Tarefa

> [!NOTE]
> As liñas de subcontratación de prezo fixo non se admiten nas operacións do proxecto.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
