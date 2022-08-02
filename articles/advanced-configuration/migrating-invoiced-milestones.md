---
title: Migre os hitos de facturación totalmente facturados no momento do cambio
description: Este artigo explica como migrar os fitos de facturación a prezos fixos que se facturaron ao cliente por contratos de proxectos abertos antes da data de posta en funcionamento.
author: sigitac
ms.date: 01/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 05cd71f9860b5698e3a26bc72660b0b2044206c8
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028700"
---
# <a name="migrate-fully-invoiced-billing-milestones-at-cutover"></a>Migre os hitos de facturación totalmente facturados no momento do cambio

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

## <a name="scenario"></a>Escenario

Contoso estará en directo con Microsoft Dynamics 365 Project Operations para escenarios de recursos/non abastecidos. Como parte das actividades de transferencia, o equipo de implementación debe migrar os contratos de proxectos abertos do sistema antigo. Algúns dos contratos do proxecto inclúen liñas de contrato que utilizan o método de facturación a prezo fixo e xa se facturaron parcialmente ao cliente final. O equipo de implementación debe migrar estes fitos de facturación como **Factura do cliente publicada**, porque deben incluírse no valor total do contrato para efectos de recoñecemento de ingresos. Non obstante, os saldos dos clientes en Contas por cobrar e Libro maior non deben verse afectados.

## <a name="solution"></a>Solución

### <a name="prerequisites"></a>Requisitos previos

- Debe instalarse Dynamics 365 Finance 10.0.24 ou posterior.
- O entorno onde se completarán os pasos de migración debe estar en modo de mantemento. Non se deben realizar outras actividades mentres se migran os fitos.
- Os pasos de migración deben seguirse exactamente como se describe aquí e só se poden usar para a actividade de corte. Microsoft non admite ningún outro uso desta capacidade.

### <a name="create-a-cutover-version-of-the-project-operations-integration-contract-line-milestones-dual-write-map"></a>Crea unha versión de corte do mapa de dobre escritura de fitos de liña de contrato de integración de Project Operations 

1. Asegúrese de que a asignación de destino para o **Liña de contratos de integración de operacións de proxectos** a entidade está actualizada. 

    1. En Finanzas, vai a **Xestión de datos** \> **Entidades de datos**, e seleccione o **Liña de contratos de integración de operacións de proxectos** entidade. 
    2. Seleccione **Modificar mapas de destino**. 
    3. No **Creación de mapas para orientar** páxina, seleccione **Xerar mapeo** e, a continuación, confirme que quere xerar a asignación.

2. Detén e refresca o **Liña de contratos de integración de operacións de proxectos** (**msdyn\_ axenda de valores de liñas contractuais**) mapa de dobre escritura. 

    1. Ir a **Xestión de datos** \> **Escritura dual**, seleccione o mapa e abra os seus detalles. 
    2. Seleccione **Pare**, e agarde ata que o sistema deteña o mapa. 
    3. Seleccione **Actualizar táboas**.

3. Engade unha asignación para o estado da transacción.

    1. Seleccione **Engadir mapeo**.
    2. Na nova liña, na **Aplicacións de finanzas e operacións** columna, seleccione a **TRANSSTATUS\[ TRANSSTATUS\]** campo.
    3. No **Microsoft Dataverse** columna, seleccione **msdyn\_ estado da factura\[ Estado da factura\]**.
    4. No **Tipo de mapa** columna, seleccione a frecha cara á dereita (**\>**).
    5. No cadro de diálogo que aparece, no **Dirección de sincronización** campo, seleccione **Dataverse ás aplicacións de Finanzas e Operacións**.
    6. Seleccione **Engadir transformación**.
    7. No **Tipo de transformación** campo, seleccione **ValueMap**.
    8. Seleccione **Mapeo de valor engadido**.
    9. No campo esquerdo, introduza **4**. No campo da dereita, introduza **192350001**. 
    10. Seleccione **Gardar**, e despois pecha a caixa de diálogo.

4. Seleccione **Gardar como** para gardar a versión do mapa de dobre escritura. 
5. No **Engadir táboa** panel, no **Editora** campo, seleccione **Editor predeterminado**.
6. No **Versión** campo, introduza a versión.
7. No **Descrición** campo, introduza unha nota sobre esta versión de corte do mapa. 
8. Seleccione **Gardar**.
9. Inicia o mapa.

### <a name="migrate-invoiced-milestones-to-the-dataverse-environment"></a>Migrar os fitos facturados ao Dataverse ambiente

1. No Proxecto Operacións Dataverse ambiente, crear fitos que teñan un estado de factura de **Listo para facturar**. Neste momento, non migre ningún fito que non teña facturado.

    > [!NOTE]
    > Antes de migrar os fitos de facturación, asegúrese de que as dimensións financeiras que están relacionadas coa liña de contrato do proxecto están definidas como se espera. Non se poden editar as dimensións financeiras despois de completar a migración.

2. Despois de migrar todos os fitos, detén os seguintes mapas de dobre escritura:

    - Fitos da liña de contrato de integración de operacións do proxecto (msdyn\_ axenda de valores de liñas de contrato)
    - Datos reais de integración de Project Operations (msdyn\_actuals)
    - Proposta de factura de proxecto V2 (facturas)

    Para deter os mapas, siga estes pasos:

    1. En Finanzas, vai a **Xestión de datos** \> **Escritura dual**, seleccione un mapa e abra os seus detalles.
    2. Seleccione **Pare**, e agarde ata que o sistema deteña o mapa.

3. No Proxecto Operacións Dataverse entorno, crear y confirmar facturas pro forma para los hitos de facturación. 

    1. No mapa do sitio, vaia aos contratos do proxecto, seleccione os contratos e, a continuación, seleccione **Crea facturas**.
    2. Despois de crear as facturas, ábreas desde o **Facturas** menú no mapa do sitio e, a continuación, seleccione **Confirmar**.

    Este paso crea os rexistros necesarios no ficheiro Dataverse ambiente. Non obstante, non afecta ás contas financeiras nin ás contas por cobrar, porque os mapas de dobre escritura que se indicaban anteriormente foron detidos.

4. Despois de confirmar todas as facturas proforma, devolve todos os mapas de dobre escritura ao seu estado inicial.

    1. Actualiza a versión do **Liña de contratos de integración de operacións de proxectos** (**msdyn\_ axenda de valores de liñas contractuais**) mapa de dobre escritura de volta ao orixinal. 
    2. Seleccione o mapa de escritura dual na lista de mapas, seleccione **Versión de mapa de táboa** e, a continuación, seleccione a versión orixinal do mapa da táboa.
    3. Seleccione **Gardar**.
    4. Reinicia os seguintes mapas de dobre escritura:

        - Fitos da liña de contrato de integración de operacións do proxecto (msdyn\_ axenda de valores de liñas de contrato)
        - Datos reais de integración de Project Operations (msdyn\_actuals)
        - Proposta de factura de proxecto V2 (facturas)

Os fitos están agora migrados e o sistema está preparado para os seguintes pasos da actividade de cambio.
