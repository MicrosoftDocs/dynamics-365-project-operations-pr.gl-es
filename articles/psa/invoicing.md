---
title: Facturación en Project Service Automation
description: Este tema fornece información sobre facturación.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 08/03/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 0855e85c1f09d29d3ecb49ba517fd3043ae11140
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5151386"
---
# <a name="invoicing-in-project-service-automation"></a>Facturación en Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Facturación en Dynamics 365 Project Service Automation é útil porque proporciona aos xestores de proxectos un segundo nivel de aprobación antes de que creen facturas para os clientes. O primeiro nivel de aprobación complétase cando se aproban as entradas de tempo e gasto que envían os membros do equipo do proxecto.

PSA non se deseñou para xerar facturas orientadas ao cliente polas seguintes razóns:

- Non contén información fiscal.
- Non pode converter outras moedas á moeda de facturación mediante tipos de cambio configurados correctamente.
- Non pode formatar correctamente as facturas para que poidan imprimirse.

Pola contra, pode utilizar un sistema financeiro ou de contabilidade para crear facturas orientadas ao cliente que usan a información das propostas de facturas que se xeran en PSA.

## <a name="creating-project-invoices-in-psa"></a>Creación de facturas de proxecto en PSA

Pódense crear as facturas dun proxecto unha a unha ou en masa. Pode crealas manualmente ou pódense configurar para que se xeren de xeito automatizado.

### <a name="manually-create-project-invoices-in-psa"></a>Crear facturas de proxecto manualmente en PSA

Dende a páxina de lista **Contratos do proxecto**, pode crear facturas de proxecto por separado para cada contrato de proxecto, ou pode crear facturas en masa para varios contratos de proxecto.

Siga este paso para crear unha factura para un contrato de proxecto específico.

- Na páxina de lista **Contratos de proxecto**, abra un contrato de proxecto e, a seguir, seleccione **Crear factura**.

    ![Creación de facturas de proxecto para un contrato de proxecto específico](media/CreateProjectInvoicesOneByOne.png)

    Xérase unha factura para todas as transaccións do contrato de proxecto seleccionado que teñan un estado de **Listo para facturar**. Estas transaccións inclúen tempo, gastos, fitos e liñas de contratos baseadas en produtos.

Siga estes pasos para crear facturas en masa.

1. Na páxina de lista **Contratos do proxecto**, seleccione un ou máis contratos de proxecto para os que debe crear unha factura e logo seleccione **Crear facturas de proxecto**.

    ![Creación de facturas de proxecto en masa](media/CreateProjectInvoicesBulk.png)

    Unha mensaxe de aviso informa que pode haber un atraso antes de que se creen as facturas. Tamén se amosa o proceso.

2. Seleccione **Aceptar** para pechar a caixa de mensaxe.

    Xérase unha factura para todas as transaccións dunha liña de contrato que teñan un estado de **Listo para facturar**. Estas transaccións inclúen tempo, gastos, fitos e liñas de contratos baseadas en produtos.

3. Para ver as facturas que se xeran, vaia a **Vendas** \> **Facturación** \> **Facturas**. Verá unha factura por cada contrato do proxecto.

### <a name="set-up-automated-creation-of-project-invoices-in-psa"></a>Configurar a creación automatizada de facturas de proxectos en PSA

Siga estes pasos para configurar unha factura automatizada executada en PSA.

1. Vaia a **Project Service** \> **Configuración** \> **Traballos en lote**.
2. Cree un traballo en lotes e nomealo **PSA Crear facturas**. O nome do traballo por lotes debe incluír o termo "Crear facturas".
3. No campo **Tipo de traballo**, seleccione **Ningún**. Por defecto, as opcións **Frecuencia diaria** e **Está activo** están definidas en **Si**.
4. Seleccione **Executar fluxo de traballo**. Na caixa de diálogo **Buscar rexistro**, verá tres fluxos de traballo:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Seleccione **ProcessRunCaller** e, a seguir, seleccione **Engadir**.
6. Na caixa de diálogo seguinte, seleccione **Aceptar**. Un fluxo de traballo **Suspensión** vai seguido por fluxo de traballo **Proceso**.

    Tamén pode seleccionar **ProcessRunner** no paso 5. Entón, cando seleccione **Aceptar**, o fluxo de traballo **Proceso** vai seguido por un fluxo de traballo **Suspensión**.

Os fluxos de traballo **ProcessRunCaller** e **ProcessRunner** crean facturas. **ProcessRunCaller** chama a **ProcessRunner**. **ProcessRunner** é o fluxo de traballo que realmente crea as facturas. Percorre todas as liñas de contrato nas que deben crearse as facturas e crea facturas para esas liñas. Para determinar as liñas de contrato para as que deben crearse as facturas, o traballo analiza as datas de execución de facturas para as liñas de contrato. Se as liñas de contrato que pertencen a un contrato teñen a mesma data de execución de facturas, as transaccións combínanse nunha factura que ten dúas liñas de factura. Se non hai transaccións para as que crear facturas, o traballo omite a creación de facturas.

Despois de que **ProcessRunner** remate a execución, chama a **ProcessRunCaller**, fornece a hora de finalización e péchase. A seguir, **ProcessRunCaller** inicia un temporizador que se executa durante 24 horas desde a hora de finalización especificada. Ao final do temporizador, **ProcessRunCaller** péchase.

O traballo de proceso por lotes para crear facturas é un traballo recorrente. Se este proceso de lotes se executa moitas veces, créanse varias instancias do traballo e causan erros. Polo tanto, debe iniciar o proceso por lotes unha soa vez e só debe reinicialo se deixa de executarse.

> [!NOTE]
> A facturación por lotes en Project Service Automation só se executa para liñas de contrato de proxecto que están configuradas por programacións de facturas. Unha liña de contrato cun método de facturación de prezos fixos debe ter configurados os fitos. Unha liña de contrato de proxecto cun método de facturación de tempo e material necesitará unha programación de facturas baseado na data configurada. A información sobre a configuración de frecuencias de facturación no contexto dun proxecto baseado nunha liña de oferta inclúese no tema [Ofertas e liñas de oferta](basic-quote-lines.md#invoice-schedule). O mesmo se aplica a unha liña de contrato baseada nun proxecto.      
 
### <a name="edit-a-draft-psa-invoice"></a>Edita un borrador de factura PSA

Cando se crea un borrador de factura de proxecto, todas as transaccións de vendas non facturadas que se crearon cando se aprobaron as entradas de tempo e gasto son enviadas á factura. Pode realizar os seguintes axustes mentres a factura aínda está en fase de borrador:

- Eliminar ou editar os detalles da liña de factura.
- Editar e axustar a cantidade e o tipo de facturación.
- Engadir directamente tempo, gastos e taxas como transaccións na factura. Pode empregar esta funcionalidade se a liña de factura está asignada a unha liña de contrato que permite estas clases de transaccións.

Seleccione **Confirmar** para confirmar unha factura. A acción Confirmar é unha acción unidireccional. Cando seleccione **Confirmar**, o sistema fai a factura só de lectura e crea facturas de vendas facturadas a partir de cada detalle da liña de factura para cada liña de factura. Se o detalle da liña de factura fai referencia a un prezo real de vendas non facturadas, o sistema tamén inverte o dato real de vendas non facturadas. (Calquera detalle de liña de factura que se crease a partir dunha entrada de gasto ou referencia fará referencia a un dato real de vendas non facturadas). Os sistemas de integración de libro de contabilidade xeral poden usar esta inversión para inverter o traballo do proxecto (WIP) para contabilidade.

### <a name="correct-a-confirmed-psa-invoice"></a>Corrixir unha factura de PSA confirmada

Pódense editar (corrixir) as facturas de PSA confirmadas. Cando corrixa unha factura confirmada, créase un novo borrador de factura correctora. Dado que se supón que desexa reverter todas as transaccións e cantidades da factura orixinal, esta factura correctora inclúe todas as transaccións da factura orixinal e todas as cantidades que hai en ela son 0 (cero).

Se as transaccións non requiren corrección, pode eliminalas do borrador da factura correctora. Se desexa inverter ou devolver só unha cantidade parcial, pode editar o campo **Cantidade** no detalle da liña. Se abre o detalle da liña de factura, pode ver a cantidade orixinal da factura. Pode editar a cantidade da factura actual de xeito que sexa inferior ou superior á cantidade da factura orixinal.

Cando se confirma unha factura correctora, invértese o datos real de vendas facturadas orixinais, e créase un novo dato real de vendas facturadas. Se a cantidade foi reducida, a diferenza fará que tamén se cree un novo dato real de vendas sen facturar. Por exemplo, se as vendas orixinais facturadas foron de oito horas e o detalle da liña de factura correctora ten unha cantidade reducida de seis horas, PSA inverte a liña de vendas facturadas orixinal e crea dous novos datos reais:

- Un dato real de vendas facturadas de seis horas.
- Un dato real de vendas sen facturar das dúas horas restantes. Esta transacción pódese facturar posteriormente ou marcarse como non imputable, dependendo das negociacións co cliente.


[!INCLUDE[footer-include](../includes/footer-banner.md)]