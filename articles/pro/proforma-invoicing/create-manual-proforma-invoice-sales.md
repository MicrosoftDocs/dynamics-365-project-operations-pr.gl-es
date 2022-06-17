---
title: Facturas proforma de proxecto
description: Este artigo ofrece información sobre as facturas de proxectos proforma en Project Operations.
author: rumant
ms.date: 04/06/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 8f028ec12aa3144a2c1bf13f6f8ce90c9de48519
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8934548"
---
# <a name="proforma-project-invoices"></a>Facturas proforma de proxecto

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

A facturación proforma do proxecto proporciona aos xestores de proxectos un segundo nivel de aprobación antes de que creen facturas para os clientes. O primeiro nivel de aprobación complétase cando se aproban as entradas de tempo, gasto e material que envían os membros do equipo do proxecto.

O despregamento lite de Dynamics 365 Project Operations non está deseñado para xerar facturas orientadas ao cliente. A seguinte lista mostra por que non se poden xerar facturas:

- Non contén información fiscal.
- Non se poden converter outras moedas á moeda de facturación.
- Non se poden formatar correctamente as facturas para imprimir.

Pola contra, pode utilizar un sistema financeiro ou de contabilidade para crear facturas orientadas ao cliente que usan a información das propostas de facturas xeradas.

## <a name="creating-project-invoices"></a>Creación de facturas de proxecto

Pódense crear as facturas dun proxecto unha a unha ou en masa. Pode crealas manualmente ou pódense configurar para que se xeren de xeito automatizado.

### <a name="manually-create-project-invoices"></a>Crear facturas de proxecto manualmente 

Na páxina de lista **Contratos do proxecto**, pode crear facturas de proxecto por separado para cada contrato de proxecto, ou pode crear facturas en masa para varios contratos de proxecto.

   - Para crear unha factura para un contrato de proxecto específico, na páxina de lista **Contratos do proxecto**, abra un contrato de proxecto e seleccione **Crear factura**.

   Xérase unha factura para todas as transaccións do contrato de proxecto seleccionado que teñan un estado de **Listo para facturar**. Estas transaccións inclúen tempo, gastos, materiais, fitos, liñas de contrato baseadas en produto e outras liñas de diario de vendas non facturadas que poden estar confirmadas.

Para crear facturas en masa:

1. Na páxina de lista **Contratos do proxecto**, seleccione un ou máis contratos de proxecto para crear unha factura e logo seleccione **Crear facturas de proxecto**.
2. Unha mensaxe de aviso informa que pode haber un atraso antes de que se creen as facturas. Tamén se amosa o proceso. Seleccione **Aceptar** para pechar a caixa de mensaxe.

   Xérase unha factura para todas as transaccións dunha liña de contrato que teñan un estado de **Listo para facturar**. Estas transaccións inclúen tempo, gastos, materiais, fitos, liñas de contrato baseadas en produto e outras liñas de diario de vendas non facturadas que poden estar confirmadas.

3. Vexa as facturas que se xeran indo a **Vendas** \> **Facturación** \> **Facturas**. Verá unha factura por cada contrato do proxecto.

### <a name="set-up-automated-creation-of-project-invoices"></a>Configurar a creación automatizada de facturas de proxectos 

Siga estes pasos para configurar unha factura automatizada executada.

1. Vaia a **Configuración** \> **Traballos en lote**.
2. Cree un traballo en lote e noméelo **Crear facturas de Project Operations**. O nome do traballo por lotes debe incluír o termo "Crear facturas".
3. No campo **Tipo de traballo**, seleccione **Ningún**. Por defecto, as opcións **Frecuencia diaria** e **Está activo** están definidas en **Si**.
4. Seleccione **Executar fluxo de traballo**. Na caixa de diálogo **Buscar rexistro**, verá os seguintes fluxos de traballo:

    - ProcessRunCaller
    - Executador do proceso
    - Actualizar uso de roles

5. Seleccione **ProcessRunCaller** e, a seguir, seleccione **Engadir**.
6. Na caixa de diálogo seguinte, seleccione **Aceptar**. Un fluxo de traballo **Suspensión** vai seguido por fluxo de traballo **Proceso**.

    Tamén pode seleccionar **ProcessRunner** no paso 5. Entón, cando seleccione **Aceptar**, o fluxo de traballo **Proceso** vai seguido por un fluxo de traballo **Suspensión**.

Os fluxos de traballo **ProcessRunCaller** e **ProcessRunner** crean facturas. **ProcessRunCaller** chama a **ProcessRunner**. **ProcessRunner** é o fluxo de traballo que crea as facturas. Este fluxo de traballo percorre todas as liñas de contrato nas que deben crearse as facturas e crea as facturas. Para determinar as liñas de contrato para as que deben crearse as facturas, o fluxo de traballo analiza as datas de execución de facturas para as liñas de contrato. Se as liñas de contrato que pertencen a un contrato teñen a mesma data de execución de facturas, as transaccións combínanse nunha factura que ten dúas liñas de factura. Se non hai transaccións para as que crear facturas, non se crean facturas.

Despois de que **ProcessRunner** remate a execución, chama a **ProcessRunCaller**, fornece a hora de finalización e péchase. A seguir, **ProcessRunCaller** inicia un temporizador que se executa durante 24 horas desde a hora de finalización especificada. Ao final do temporizador, **ProcessRunCaller** péchase.

O traballo de proceso por lotes para crear facturas é un traballo recorrente. Se este proceso de lotes se executa moitas veces, créanse varias instancias do traballo e pode causar erros. Para evitar este problema, inicie o proceso por lotes unha soa vez e reinícieo só se deixa de executarse.

> [!NOTE]
> A facturación por lotes só se executa para as liñas de contrato do proxecto que están configuradas por programacións de facturas. Unha liña de contrato cun método de facturación de prezos fixos debe ter configurados os fitos. Unha liña de contrato de proxecto cun método de facturación de tempo e material necesitará unha programación de facturas baseado na data configurada. O mesmo se aplica a unha liña de contrato baseada nun proxecto.      
 
### <a name="edit-a-draft-invoice"></a>Edita un borrador de factura

Cando se crea un borrador de factura de proxecto, todas as transaccións de vendas non facturadas que se crearon cando se aprobaron as entradas de tempo e gasto son enviadas á factura. Pode realizar os seguintes axustes mentres a factura aínda está en fase de borrador:

- Eliminar ou editar os detalles da liña de factura.
- Editar e axustar a cantidade e o tipo de facturación.
- Engadir directamente tempo, material e taxas como transaccións na factura. Pode empregar esta funcionalidade se a liña de factura está asignada a unha liña de contrato que permite estas clases de transaccións.

Seleccione **Confirmar** para confirmar unha factura. Esta acción é unha acción unidireccional. Cando seleccione **Confirmar**, a factura convértese en só de lectura e crea facturas de vendas facturadas a partir de cada detalle da liña de factura para cada liña de factura. Se o detalle da liña de factura fai referencia a un prezo real de vendas non facturadas, o dato real de vendas non facturadas invértese. Calquera detalle da liña de factura que se creou a partir dunha entrada de tempo, gasto ou uso de material fará referencia a un dato real de vendas non facturadas. Os sistemas de integración de libro maior poden usar esta reversión para reverter o traballo en curso do proxecto (WIP) con fins de contabilidade.

### <a name="correct-a-confirmed-invoice"></a>Corrixir unha factura confirmada

Pódense editar as facturas confirmadas. Cando corrixa unha factura confirmada, créase un novo borrador de factura correctora. Dado que se supón que desexa reverter todas as transaccións e cantidades da factura orixinal, esta factura correctora inclúe todas as transaccións da factura orixinal e todas as cantidades que hai en ela son cero.

Se hai transaccións que non requiren corrección, pode eliminalas do borrador da factura correctora. Se desexa inverter ou devolver só unha cantidade parcial, pode editar o campo **Cantidade** no detalle da liña. Se abre o detalle da liña de factura, pode ver a cantidade orixinal da factura. Pode editar a cantidade da factura actual de xeito que sexa inferior ou superior á cantidade da factura orixinal.

Cando se confirma unha factura correctora, invértese o datos real de vendas facturadas orixinais, e créase un novo dato real de vendas facturadas. Se a cantidade foi reducida, a diferenza fará que se cree un novo dato real de vendas sen facturar. Por exemplo, se a vendas orixinal facturada foi de oito horas e o detalle da liña de factura correctora ten unha cantidade reducida de seis horas, a liña de vendas facturadas orixinal invértese e créanse dous novos datos reais:

- Un dato real de vendas facturadas de seis horas.
- Un dato real de vendas sen facturar das dúas horas restantes. Esta transacción pódese facturar posteriormente ou marcarse como non imputable, dependendo das negociacións co cliente.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
