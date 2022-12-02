---
title: Crear facturas de fornecedor
description: Este artigo describe o concepto de facturas de fornecedor e explica como crealas en Microsoft Dynamics 365 Project Operations.
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
# <a name="create-vendor-invoices"></a>Crear facturas de fornecedor

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Para usar a funcionalidade descrita neste artigo, debe activar a funcionalidade **Activa o procesamento de datos reais de subcontratos con Project Operations para escenarios baseados en recursos** na área de traballo **Xestión de características**.

A facturación de fornecedores en Microsoft Dynamics 365 Project Operations pódese usar para rexistrar os custos das entregas de servizos e/ou materiais nun proxecto completado por parte dos fornecedores.

Cando os servizos e/ou materiais son subcontratados a un fornecedor, un subcontrato representa o acordo contractual con ese fornecedor. A medida que o fornecedor presta os servizos ou cando os materiais son recibidos e utilizados nas tarefas do proxecto, os custos rexístranse no proxecto. A seguir, o fornecedor envía periodicamente facturas. Esas facturas se verifican e coinciden cos custos que se rexistran no proxecto. Despois de completar o proceso de verificación, a factura do fornecedor é confirmada e liberada para o pago.

## <a name="scenarios-for-use"></a>Escenarios de uso

As facturas de fornecedor en Project Operations pódense usar para dous escenarios distintos:

- Os clientes utilizan as experiencias completas de subcontratación.
- Os clientes non usan as experiencias de subcontratación completas, pero queren ter unha visión unificada dos custos dos proxectos en Project Operations.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Os clientes utilizan as experiencias completas de subcontratación

As experiencias de factura de fornecedor ofrecen un xeito de verificar as entradas de tempo, o uso de material e as entradas de gastos que fan referencia a compoñentes subcontratados e facelas coincidir coas liñas de factura do fornecedor. Este proceso pódese usar para verificar a precisión das liñas de factura do fornecedor. Despois de que se complete o proceso de verificación e se confirme a factura do fornecedor, o sistema reverte os datos reais que foron rexistrados polos rexistros de tempo, gastos e uso de material aprobados e logo crea novos datos reais de custo mediante as liñas de factura do fornecedor.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Os clientes non usan as experiencias de subcontratación completas, pero queren ter unha visión unificada dos custos dos proxectos en Project Operations

Se está a facer un seguimento do proceso de subcontratación nun sistema de terceiros, pode rexistrar os custos dese sistema de terceiros en Project Operations creando facturas do fornecedor que non fagan referencia a subcontratos. Deste xeito, os seus xestores de proxectos poden ter unha visión única e unificada de todos os custos dun proxecto determinado.

## <a name="create-vendor-invoices-in-project-operations"></a>Crear facturas do fornecedor en Project Operations

As facturas de fornecedor créanse en Dynamics 365 Finance mediante o módulo **Contas pendentes de pago**. Non pode crear facturas de fornecedor directamente en Dataverse.

### <a name="set-up-vendor-invoice-verification"></a>Configurar a verificación de facturas do provedor

Se a factura do fornecedor está destinada a un subcontrato en Dataverse, debe activar o parámetro **É necesaria a verificación manual por PM**. A configuración da opción determina se a factura do fornecedor debe confirmarse automaticamente en Dataverse ou se se require unha confirmación manual. A cabeceira de cada factura do fornecedor do proxecto inclúe unha opción co mesmo nome. De forma predefinida, a opción da cabeceira de todas as facturas do fornecedor do proxecto está configurada co valor que definiu aquí. Non obstante, pode actualizar o valor segundo sexa necesario na cabeceira das facturas de fornecedor individuais.

Se a opción está definida como **Si**, a factura do fornecedor que se crea en Finance e se sincroniza con Dataverse ten o estado **Borrador**. A factura debe ser validada e verificada polo xestor do proxecto e confirmada antes de ser procesada e contabilizada no proxecto específico e nas contas do libro maior en Finance.

Se a opción está definida como **Non**, a factura do fornecedor confírmase automaticamente. Non son necesarias máis accións.

Para configurar a verificación de facturas do fornecedor, siga estes pasos.

1. En Finace, vaia a **Xestión e contabilidade de proxectos** \> **Configuración** \> **Parámetros de Xestión e contabilidade de proxectos**.
1. No separador **Financeiro**, configure a opción **É necesaria a verificación manual por PM** como **Si** se a política da empresa require a verificación das facturas do fornecedor do subcontratista. Se non é necesaria a verificación do xestor do proxecto en Dataverse, deixe o conxunto de opcións en **Non**. De forma predefinida, a configuración empregarase na páxina **Factura do fornecedor pendente**.

> [!NOTE]
> As facturas de fornecedor que se crean para subcontratos en Dataverse só se pode procesar correctamente se a opción **É necesaria a verificación manual por PM** está definida en **Si**. O xestor do proxecto só pode relacionar manualmente os datos reais de custos de tempo, material e gastos que crean os subcontratistas coas liñas de factura do fornecedor se esta opción está definida como **Si**.

### <a name="set-up-a-procurement-integration-account-for-vendor-invoices"></a>Configurar unha conta de integración de adquisicións para facturas do fornecedor

Cando se contabiliza unha factura de provedor en Finance para Project Operations - Ambiente integrado (sen fornecemento), os datos financeiros contabilízanse na conta de integración de adquisicións. O sistema xera os datos reais en Dataverse para a factura contabilizada. Estes datos reais publícanse en Finance mediante o diario de integración do proxecto. A contabilización do diario de integración de proxectos contabiliza o custo real e anula a conta de integración de adquisicións.

Para configurar unha conta de integración de adquisicións para facturas do fornecedor, siga estes pasos.

1. En Finace, vaia a **Xestión e contabilidade de proxectos** \> **Configuración** \> **Parámetros de Xestión e contabilidade de proxectos**.
1. No separador **Project Operations en Dynamics 365 Customer Engagement**, seleccione **Materiais** \> **Conta de integración de adquisicións**.

### <a name="create-and-post-subcontract-vendor-invoices"></a>Crear e contabilizar facturas do fornecedor subcontrato

Cando un empregado de Contas pendentes de pago recibe unha factura do subcontratista, créase unha nova factura en Finance.

1. En Finance, vaia a **Contas pendentes de pago** \> **Facturas** \> **Facturas de ecedorforn pendentes**.
1. No **Panel de accións**, seleccione **Nova** para crear unha factura do fornecedor.
1. Na cabeceira da factura, no campo **Conta de factura**, seleccione **Subcontratista**.
1. Seleccione a data da factura.
1. No separador **Cabeceira**, configure a opción **É necesaria a verificación manual por PM** en **Si**. A configuración predefinida desta opción provén da páxina **Parámetros de xestión e contabilidade de proxectos**. Non obstante, pódese cambiar a nivel de factura do fornecedor.
1. No separador rápido **Liña de factura**, seleccione **Engadir liña** para crear unha liña de factura do fornecedor.
1. Seleccione a categoría de adquisición que se creou para as liñas de subcontratación e introduza o prezo unitario, a unidade de medida e a cantidade.
1. Na sección de liñas de factura do fornecedor, no separador **Proxecto**, seleccione o proxecto co que o subcontratista comparte a factura do subcontrato.
1. Seleccione a categoría do proxecto. Pode ser de calquera tipo de **Elemento**, **Gasto**, **Materiais** ou **Horas**.
1. Seleccione o rol só se a categoría de proxecto seleccionada é de tipo **Hora**.
1. Seleccione **Contabilizar** para contabilizar a factura do fornecedor.

Alternativamente, pode crear unha factura de fornecedor indo a **Contas pendentes de pago** \> **Facturas** \> **Abrir facturas de fornecedores** e seleccione **Nova**.

Cando se publica a factura do fornecedor, está dispoñible en Dataverse para a verificación e procesamento do xestor de proxectos.

## <a name="vendor-invoice-processing-in-dataverse"></a>Procesamento da factura do fornecedor en Dataverse

Na factura do fornecedor que se crea en Dataverse, algúns valores de campo proceden da factura do fornecedor que está rexistrada en Finance. Outros valores son valores predefinidos que proveñen do subcontrato.

Os seguintes campos e rexistros relacionados copiaranse do subcontrato á cabeceira da factura do fornecedor:

- Moeda
- Unidade de contratación
- Condicións de pagamento

Nas liñas de factura do fornecedor, Project Operations usa os seguintes valores de campo para introducir o subcontrato predefinido e a referencia da liña de subcontrato:

- Clase de transacción
- Rol
- Categoría da transacción
- Campos do produto
- Project
- Tarefa

> [!NOTE]
> As liñas de subcontratación de prezo fixo non se admiten en Project Operations.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
