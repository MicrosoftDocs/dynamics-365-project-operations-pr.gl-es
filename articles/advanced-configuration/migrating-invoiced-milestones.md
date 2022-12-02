---
title: Migrar fitos de facturación totalmente facturados na transición
description: Este artigo explica como migrar os fitos de facturación a prezos fixos que se facturaron ao cliente por contratos de proxectos abertos antes da data de publicación.
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
# <a name="migrate-fully-invoiced-billing-milestones-at-cutover"></a>Migrar fitos de facturación totalmente facturados na transición

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

## <a name="scenario"></a>Escenario

Contoso publicarase con Microsoft Dynamics 365 Project Operations para escenarios de recursos/sen fornecemento. Como parte das actividades de transición, o equipo de implementación debe migrar os contratos de proxectos abertos do sistema antigo. Algúns dos contratos do proxecto inclúen liñas de contrato que utilizan o método de facturación a prezo fixo e xa se facturaron parcialmente ao cliente final. O equipo de implementación debe migrar estes fitos de facturación como **Factura de cliente contabilizada**, porque deben incluírse no valor total do contrato para efectos de recoñecemento de ingresos. Non obstante, os saldos dos clientes en Contas pendentes de cobro e Libro maior non deben verse afectados.

## <a name="solution"></a>Solución

### <a name="prerequisites"></a>Requisitos previos

- Dynamics 365 Finance 10.0.24 ou posterior debe estar instalado.
- O ambiente onde se completarán os pasos de migración debe estar en modo de mantemento. Non se deben realizar outras actividades mentres se migran os fitos.
- Os pasos de migración deben seguirse exactamente como se describe aquí e só se poden usar para a actividade de transición. Microsoft non admite ningún outro uso desta capacidade.

### <a name="create-a-cutover-version-of-the-project-operations-integration-contract-line-milestones-dual-write-map"></a>Crear unha versión de transición do mapa de escrita dual de fitos de liña de contrato de integración de Project Operations 

1. Asegúrese de que a asignación de destino para a entidade **Fitos de liña de contrato de integración de Project Operations** está actualizada. 

    1. En Finance, vaia a **Xestión de datos** \> **Entidades de datos** e seleccione a entidade **Fitos de liña de contrato de integración de Project Operations**. 
    2. Seleccione **Modificar asignacións de destino**. 
    3. Na páxina **Fases de asignación a destino**, seleccione **Xerar asignación** e, a seguir, confirme que quere xerar a asignación.

2. Pare e actualice o mapa de escrita dual **Fitos de liña de contrato de integración de Project Operations** (**msdyn\_contractlinescheduleofvalues**). 

    1. Vaia a **Xestión de datos** \> **Escrita dual**, seleccione o mapa e abra os seus detalles. 
    2. Seleccione **Parar** e agarde ata que o sistema deteña o mapa. 
    3. Seleccione **Actualizar táboas**.

3. Engada unha asignación para o estado da transacción.

    1. Seleccione **Engadir asignación**.
    2. Na nova liña, na columna **Aplicacións de finanzas e operacións**, seleccione o campo **TRANSSTATUS \[TRANSSTATUS\]**.
    3. Na columna **Microsoft Dataverse**, seleccione **msdyn\_invoicestatus \[Estado da factura\]**.
    4. Na columna **Tipo de mapa**, seleccione a frecha cara á dereita (**\>**).
    5. Na caixa de diálogo que aparece, no campo **Dirección de sincronización**, seleccione **Dataverse ás aplicacións de finanzas e operacións**.
    6. Seleccione **Engadir transformación**.
    7. No campo **Tipo de transformación**, seleccione **ValueMap**.
    8. Seleccione **Engadir asignación de valores**.
    9. No campo esquerdo, introduza **4**. No campo dereito, introduza **192350001**. 
    10. Seleccione **Gardar** e peche a caixa de diálogo.

4. Seleccione **Gardar como** para gardar a versión do mapa de escrita dual. 
5. No panel **Engadir táboa**, no campo **Editor**, seleccione **Editor predeterminado**.
6. No campo **Versión**, introduza a versión.
7. No campo **Descrición**, introduza unha nota sobre esta versión de transición do mapa. 
8. Seleccione **Gardar**.
9. Inicie o mapa.

### <a name="migrate-invoiced-milestones-to-the-dataverse-environment"></a>Migrar os fitos facturados ao ambiente de Dataverse

1. No ambiente de Dataverse de Project Operations, cree fitos que teñan un estado de factura de **Listo para facturar**. Neste momento, non migre ningún fito que non teña facturado.

    > [!NOTE]
    > Antes de migrar os fitos de facturación, asegúrese de que as dimensións financeiras que están relacionadas coa liña de contrato do proxecto están definidas como se espera. Non se poden editar as dimensións financeiras despois de completar a migración.

2. Despois de migrar todos os fitos, deteña os seguintes mapas de escrita dual:

    - Fitos de liña de contrato de integración de Project Operations (msdyn\_contractlinescheduleofvalues)
    - Datos reais de integración de Project Operations (msdyn\_actuals)
    - Proposta de factura de proxecto V2 (facturas)

    Para deter os mapas, siga estes pasos:

    1. En Finance, vaia a **Xestión de datos** \> **Escrita dual**, seleccione un mapa e abra os seus detalles.
    2. Seleccione **Parar** e agarde ata que o sistema deteña o mapa.

3. No ambiente de Dataverse de Project Operations, cree e confirme facturas proforma para los fitos de facturación. 

    1. No mapa do sitio, vaia aos contratos do proxecto, seleccione os contratos e, a continuación, seleccione **Crear facturas**.
    2. Despois de crear as facturas, ábraas desde o menú **Facturas** no mapa do sitio e, a seguir, seleccione **Confirmar**.

    Este paso crea os rexistros necesarios no ambiente de Dataverse. Non obstante, non afecta ás contas financeiras nin ás contas pendentes de cobro, porque os mapas de escrita dual que se indicaban anteriormente foron detidos.

4. Despois de confirmar todas as facturas proforma, devolva todos os mapas de escrita dual ao seu estado inicial.

    1. Actualice a versión do mapa de escrita dual **Fitos de liña de contrato de integración de Project Operations** (**msdyn\_contractlinescheduleofvalues**) ao orixinal. 
    2. Seleccione o mapa de escrita dual na lista de mapas, seleccione **Versión de mapa de táboa** e, a seguir, seleccione a versión orixinal do mapa da táboa.
    3. Seleccione **Gardar**.
    4. Reinicie os seguintes mapas de escrita dual:

        - Fitos de liña de contrato de integración de Project Operations (msdyn\_contractlinescheduleofvalues)
        - Datos reais de integración de Project Operations (msdyn\_actuals)
        - Proposta de factura de proxecto V2 (facturas)

Os fitos están agora migrados e o sistema está preparado para os seguintes pasos da actividade de transición.
