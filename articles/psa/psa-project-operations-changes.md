---
title: Cambios de funcionalidades de Project Service Automation a Project Operations
description: Este artigo ofrece unha visión xeral dos cambios de función de Project Service Automation a Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/03/2022
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: a9c69fc4296d30763f3994a4955e64ab258ceb4f
ms.sourcegitcommit: 675e9f3615e701c5f998de3a5ea3e25df11ae107
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 09/09/2022
ms.locfileid: "9459924"
---
# <a name="feature-changes-from-project-service-automation-to-project-operations"></a>Cambios de funcionalidades de Project Service Automation a Project Operations

A actualización de Dynamics 365 Project Service Automation a Dynamics 365 Project Operations Lite entregarase en tres fases. Este artigo ofrece información sobre os principais cambios que pode esperar ver cando se complete a actualización.

| Actualizar a entrega | Fase 1 <br>(xaneiro 2022) | Fase 2 <br>(novembro 2022) | Fase 3  |
|------------------|------------------------|---------------------------|---------------------------|
| Non depende da estrutura de desagregación do traballo (WBS) dos proxectos. | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| O WBS está incluído nos límites actualmente soportados das operacións do proxecto. | &nbsp; | :heavy_check_mark: | :heavy_check_mark: |
| O WBS fóra dos límites actualmente compatibles de Project Operations, incluído o soporte para o cliente de escritorio de Project. | &nbsp; | &nbsp; | :heavy_check_mark: |

## <a name="project-management"></a>Xestión de proxectos

Os cambios máis significativos na experiencia do usuario serán no ámbito da planificación do proxecto. Project Operations adopta unha nova experiencia moderna para xestionar unha estrutura de descomposición do traballo (WBS) aproveitando as capacidades de programación proporcionadas por [Proxecto para a Web](https://support.microsoft.com/en-us/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5).

## <a name="differences-in-the-scheduling-experience"></a>Diferenzas na experiencia de programación

A seguinte táboa resume as diferenzas de programación entre Project Service Automation e Project Operations.

|  Programando     |   Project Operations   |   PSA   |
|-----------------|------------------------|---------|
| Modelos de proxecto - Capacidade de definir e aplicar modelos de proxecto cando se crea un proxecto  |  &nbsp;    | :heavy_check_mark: |
| Integración da estrutura de descomposición do traballo do proxecto (WBS) co cliente de escritorio   |    &nbsp;  | :heavy_check_mark: |
| Restricións: non comece antes e remate como máis tarde  | :heavy_check_mark: |   &nbsp;  |
| Fitos - Tarefas con duración cero   | :heavy_check_mark:  |  &nbsp;  |
| As tarefas dirixidas aos recursos respectarán a dispoñibilidade dos recursos asignados   | :heavy_check_mark: |  &nbsp;    |
| Edición por fases - Edita plans e traballa día a día   |   &nbsp;  | :heavy_check_mark: |
| Programación automática/manual: use o motor de programación do proxecto para programar tarefas de forma automática ou manual |  &nbsp; | :heavy_check_mark:  |
| Edita proxectos grandes directamente na interface de usuario: non hai límite para o tamaño dos plans editables  | Límite de tarefas 500  | :heavy_check_mark:       |
| Porcentaxe completada: marca o progreso da tarefa   | :heavy_check_mark:  |  &nbsp;  |
| [Modos de programación do proxecto](../project-management/scheduling-modes.md) - Definir o proxecto como unidades fixas, esforzo fixo ou duración fixa | :heavy_check_mark: | &nbsp; |
| Cronoloxía: crea e personaliza a vista da cronoloxía para visualizar os detalles da programación e comunicarse coas partes interesadas. | :heavy_check_mark:  | &nbsp; |
| Tarefas orientadas ao esforzo: compatibilidade do motor de programación para programar unha tarefa como impulsado polo esforzo  | :heavy_check_mark:  | &nbsp; |
| **Información da tarefa** caixa de diálogo - Garda os detalles da tarefa mediante unha caixa de diálogo | :heavy_check_mark:  |  &nbsp;  |
| Arrastrar e soltar: seleccione varias tarefas e modifique a súa posición no WBS | :heavy_check_mark: | &nbsp;  |
| Vistas persistentes flexibles: define vistas máis granulares dos atributos da tarefa   | :heavy_check_mark:  | &nbsp; |
| Ordenar e filtrar o WBS  | :heavy_check_mark:  | &nbsp; |
| Vista de placas para a entrega de proxectos sen fervenza  | :heavy_check_mark:   | &nbsp; |
| Vista da liña de tempo - Diagrama de Gantt interactivo usado para visualizar e editar a WBS   | :heavy_check_mark:  | &nbsp; |
| Atallos de teclado: use atallos de teclado para operacións comúns, como sangrar ou inserir  | :heavy_check_mark:  |  &nbsp; |
| Desfacer varios niveis: realiza unha análise de semellanza para comprender completamente o impacto dos cambios invertendo e aplicando de novo todo un conxunto de operacións | :heavy_check_mark: | &nbsp; |
| Cortar/Copiar/Pegar: colabora no desenvolvemento da programación copiando e pegando detalles da programación entre aplicacións  | :heavy_check_mark: | &nbsp; |
| Listas de verificación de tarefas: engade ata 20 elementos da lista de verificación a unha tarefa   | :heavy_check_mark: | &nbsp; |

## <a name="project-planning"></a>Planificación de proxectos

O **Proxecto** páxina en Operacións do proxecto ten un número significativo de diferenzas en comparación co **Proxecto** páxina en Project Service Automation.

Elimináronse as seguintes accións do **Proxectos** páxina como parte da actualización da Fase 1:

  - **Abrir en MS Project**
  - **Crear modelo**
  - **Desligar de MS Project**

O **Proxecto** en Operacións do proxecto inclúe as seguintes pestanas novas.

- **Custos previstos de material**
- **Configuración de facturación de tarefas**

O **Estado** eliminouse a pestana e o **Estado** campo está agora no **Resumo** ficha co modo de programación do proxecto.

   ![Actualizacións na páxina do proxecto.](media/projectform.png)

O **Horario** cambiou o nome da pestana a **Tarefa** e presenta a nova experiencia de planificación de proxectos con Project for the Web.

   ![Nova pestana de tarefas do proxecto.](media/tasktab.png)

## <a name="scheduling-modes"></a>Modos de programación

Project Operations introduciu unha nova función, [Modos de programación](../project-management/scheduling-modes.md). Todos os proxectos existentes de Project Service Automation serán predeterminados **Duración fixa** en Operacións do Proxecto. Non obstante, a opción predeterminada para novos proxectos pódese xestionar indo a **Configuración** > **Parámetros** > **Parámetro** > **Modo de programación**.

   ![Configuración dos parámetros do proxecto para o modo de programación.](media/projectparameter.png)

## <a name="project-planning-limits"></a>Límites de planificación do proxecto

Project Operations depende de Project for the Web para todas as operacións de programación do proxecto. Project for the Web xestiona a estrutura de desagregación do traballo utilizando os límites da seguinte táboa.

| **Campo**                                          | **Límite**             |
|----------------------------------------------------|-----------------------|
| Total máximo de tarefas para un proxecto                  | 500                   |
| Duración máxima total para un proxecto               | 3650 días (10 anos)  |
| Total máximo de recursos para un proxecto              | 300                   |
| Total máximo de ligazóns (só sucesor) para un proxecto | 600                   |
| Total máximo de campos personalizados para un proxecto          | 1,0                    |
| Nivel máximo de xerarquía                            | 10 niveis             |
| Número máximo de ligazóns (sucesor + predecesor)            | 20                    |
| Duración máxima da tarefa folla                      | 1250 días             |
| Duración máxima dunha tarefa de resumo                 | 3650 días (10 anos)  |
| Máximo de recursos atribuídos a unha tarefa               | 20 recursos          |
| Intervalo de datas compatible para unha tarefa                    | 1/1/2000 - 12/31/2149 |
| Elementos da lista de comprobación                                    | 20                    |

## <a name="project-planning-extensibility-and-development"></a>Extensibilidade e desenvolvemento da planificación do proxecto

Despois de actualizar a Project Operations, debes usar as API de Project Scheduling para executar operacións de creación, actualización e eliminación nas seguintes entidades:

|   Nome da entidade           |   Nome lóxico da entidade       |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Tarefa do proxecto            | msdyn_projecttask           |
| Dependencia da tarefa do proxecto | msdyn_projecttaskdependency |
| Atribución do recurso     | msdyn_resourceassignment    |
| Depósito do proxecto          | msdyn_projectbucket         |
| Membro do equipo do proxecto     | msdyn_projectteam           |

Se actualmente tes personalizacións que impliquen estas entidades, consulta [Use as API de programación de proxectos para realizar operacións con entidades de programación](../project-management/schedule-api-preview.md) para orientación de implementación.

## <a name="data-model-changes"></a>Cambios no modelo de datos

Como parte da Fase 1 de actualización, hai cambios no modelo de datos. Estes cambios son principalmente cambios de campo para entidades existentes. Na Fase 1, as entidades, **msydn_project** e **msdyn_projectteam** son unha refactorización de personalizacións. 

> [!IMPORTANT]
> Esta sección actualizarase con entidades adicionais a medida que se completen as futuras fases de actualización.

Os seguintes campos foron substituídos por novos campos.

|   Entidad          |   Nome lóxico antigo   |   Novo nome lóxico    |
|-------------------|----------------------|-----------------------|
| msdyn_project     | msdyn_actualhours    | msdyn_effortcompleted |
| msdyn_project     | msdyn_plannedhours   | msdyn_effort          |
| msdyn_project     | msdyn_remaininghours | msdyn_effortremaining |
| msdyn_project     | msdyn_scheduledend   | msdyn_finish          |
| msdyn_project     | msdyn_wbsduration    | msdyn_duration        |
| msdyn_projectteam | msdyn_assignedhours  | msdyn_effort          |
| msdyn_projectteam | msdyn_de           | msdyn_start           |
| msdyn_projectteam | msdyn_to             | msdyn_finish          |

Engadíronse os seguintes campos.

|   Entidad          |   Nome lóxico                               |   Descripción |
|-------------------|----------------------------------------------|---------------|
| msdyn_project     | msdyn_actualfeesales                         | Mostra o agregado das vendas reais de taxas no proxecto. Só para usar en Project Service Automation. |
| msdyn_project     | msdyn_actualmaterialcost                     | Mostra o total do custo real do material no proxecto. Só para usar en Project Service Automation. |
| msdyn_project     | msdyn_actualmaterialsales                    | Mostra o conxunto das vendas reais de material no proxecto. Só para usar en Project Service Automation. |
| msdyn_project     | msdyn_businesscase                           |                |
| msdyn_project     | msdyn_contractlineproject                    | A liña de contrato asociada a este proxecto. |
| msdyn_project     | msdyn_copyprojectcorrelationid               | Este é un campo do sistema interno para o que se usa **Copiar proxecto** relacionados co identificador de correlación. Só para usar en Project Service Automation. |
| msdyn_project     | msdyn_copyprojectsessionid                   | Este é un campo do sistema interno, usado para **Copiar proxecto** relacionados co identificador de sesión. Só para usar en Project Service Automation. |
| msdyn_project     | msdyn_globalrevisiontoken                    | Última sincronización xRM Global Revision Token do servizo de programación do proxecto. |
| msdyn_project     | msdyn_msprojectdocument                      | O documento de Microsoft Project que pertence ao proxecto. |
| msdyn_project     | msdyn_plannedmaterialcost                    | O custo total do material previsto no proxecto. Só para usar en Project Service Automation. |
| msdyn_project     | msdyn_plannedmaterialsales                   | O agregado das vendas de material previstas no proxecto. Só para usar en Project Service Automation. |
| msdyn_project     | programa_msdyn                                | O programa co que está relacionado este proxecto. |
| msdyn_project     | msdyn_quotelineproject                       | A liña de cotización asociada a este proxecto. |
| msdyn_project     | msdyn_replaylogheader                        | A cabeceira dos rexistros de repetición. |
| msdyn_project     | msdyn_schedulemode                           | O modo de programación predeterminado usado para todas as tarefas do proxecto.  |
| msdyn_project     | msdyn_taskearlieststart                      | A data de inicio máis antiga de calquera tarefa no proxecto.  |
| msdyn_project     | msdyn_valuestatement                         |                |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | O membro do equipo do proxecto do que se copiou este membro do equipo do proxecto. |
| msdyn_projectteam | msdyn_creategenericteammemberwithrequirement | Indica se se crea o requisito de recursos para un membro do equipo xenérico recentemente creado.  |
| msdyn_projectteam | msdyn_deletestatus                           | O estado de eliminación do membro do equipo para rastrexar se hai unha solicitude de eliminación enviada ao servizo de programación do proxecto e se envía correctamente unha resposta dentro do período de tempo previsto. |
| msdyn_projectteam | msdyn_effortcompleted                        | Rastrexa o esforzo realizado polo membro do equipo nas súas tarefas. |
| msdyn_projectteam | msdyn_effortremaining                        | Fai un seguimento do esforzo que aínda debe completar o membro do equipo nas súas tarefas. |
| msdyn_projectteam | msdyn_markedfordeletiontimer                 | O período de espera desde que o membro do equipo envía unha solicitude de eliminación ao servizo de programación do proxecto ata que o membro do equipo é realmente eliminado o Microsoft Dataverse.|
| msdyn_projectteam | msdyn_markedfordeletiontimestamp             | A marca de tempo para rexistrar cando a solicitude de eliminación do membro do equipo se envía ao servizo de programación do proxecto. |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Mostra o membro do equipo do proxecto do que se copiou este membro do equipo do proxecto.  |

## <a name="project-templates"></a>Modelos de proxecto

Project Operations non ofrece soporte para modelos de proxecto. Non obstante, pode replicar gran parte da funcionalidade básica co uso do [Project Copy API](../project-management/dev-copy-project.md).

## <a name="desktop-add-in-support"></a>Soporte de complementos de escritorio

O soporte para o complemento de Microsoft Project Desktop non estará dispoñible nas dúas primeiras fases da actualización. Na Fase 3, os clientes que teñan proxectos maiores que os límites actualmente compatibles de Project for the Web poderán usar o complemento de escritorio.

## <a name="editing-resource-assignment-contours"></a>Edición de contornos de asignación de recursos

A posibilidade de editar os contornos de asignación de recursos estará dispoñible cando a Fase 2 de actualización estea dispoñible.

## <a name="billing-and-pricing"></a>Facturación e prezos

Engadíronse as seguintes novas funcións en Operacións do proxecto. Estas funcións son de natureza aditiva e non afectan o modelo de datos de Project Service Automation.

- [Rexistrar o uso do material en proxectos e tarefas do proxecto](../material/material-usage-log.md)
- [Xestión de subcontratación](../pro/subcontracting/managing-subcontracts-overview.md)
- [Contratos baseados en adiantos e retencións](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Estado de non exceder do contrato e validacións](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- [Facturación baseada en tarefas](../pro/sales/mapping-projects-tasks-quote-line-sales.md)

## <a name="deprecated-components"></a>Compoñentes obsoletos

As seguintes táboas documentan todos os campos obsoletos que se moven á solución de compoñentes obsoletos despois da actualización. Para obter máis información e unha ligazón á solución, consulte [Dynamics 365 Project Service Automation 3x a Project Operations 4x compoñentes obsoletos](https://github.com/microsoft/Dynamics365-Project-Operations-PowerApps/tree/main/3x-4x-deprecated-solution).

### <a name="invoicedetail"></a>Detalle da factura

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
|invoicedetail.msdyn_contractline    |

### <a name="msdyn_actual"></a>msdyn_actual

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_actual.msdyn_salescontractline                                                          |

### <a name="msdyn_characteristicreqforteammember"></a>msdyn_characteristicreqforteamember

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_characteristicreqforteammember.msdyn_characteristic                                     |
| msdyn_characteristicreqforteammember.msdyn_characteristicreqforteammemberid                   |
| msdyn_characteristicreqforteammember.msdyn_characteristictype                                 |
| msdyn_characteristicreqforteammember.msdyn_name                                               |
| msdyn_characteristicreqforteammember.msdyn_ratingvalue                                        |
| msdyn_characteristicreqforteammember.msdyn_resourcerequirementid                              |

### <a name="msdyn_contractlineinvoiceschedule"></a>msdyn_contractlineinvoiceschedule

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_contractlineinvoiceschedule.msdyn_contractline                                          |
| msdyn_contractlinesscheduleofvalue.msdyn_contractline                                          |
 
### <a name="msdyn_dataexport"></a>msdyn_dataexport

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_dataexport.msdyn_dataexportid                                                           |
| msdyn_dataexport.msdyn_datatoken                                                              |
| msdyn_dataexport.msdyn_entityname                                                             |
| msdyn_dataexport.msdyn_exportedrecordcount                                                    |
| msdyn_dataexport.msdyn_exportstatus                                                           |
| msdyn_dataexport.msdyn_linkedentitydata                                                       |
| msdyn_dataexport.msdyn_name                                                                   |
| msdyn_dataexport.msdyn_pagingdata                                                             |

### <a name="msdyn_fact"></a>msdyn_fact

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_fact.msdyn_salescontractline                                                            |

### <a name="msdyn_findworkevent"></a>msdyn_findworkevent

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_findworkevent.msdyn_bookableresource                                                    |
| msdyn_findworkevent.msdyn_findworkeventid                                                     |
| msdyn_findworkevent.msdyn_name                                                                |
| msdyn_findworkevent.msdyn_timestamp                                                           |
| msdyn_findworkevent.msdyn_type                                                                |
| msdyn_findworkevent.msdyn_value                                                               |
| msdyn_findworkevent.msdyn_work                                                                |

### <a name="msdyn_invoicelinetransaction"></a>msdyn_invoicelinetransaction

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_invoicelinetransaction.msdyn_invoiceline                                                |
| msdyn_invoicelinetransaction.msdyn_salescontractline                                          |

### <a name="msdyn_journalline"></a>msdyn_journalline

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_journalline.msdyn_salescontractline                                                     |

### <a name="msdyn_opportunitylineresourcecategory"></a>msdyn_opportunitylineresourcecategory

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylineresourcecategory.msdyn_billingtype                                       |
| msdyn_opportunitylineresourcecategory.msdyn_description                                       |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylineresourcecategoryid                 |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylinetransactionclassification          |
| msdyn_opportunitylineresourcecategory.msdyn_resourcecategory                                  |

### <a name="msdyn_opportunitylinetransaction"></a>msdyn_opportunitylinetransaction

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransaction.msdyn_accountcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_accountingdate                                         |
| msdyn_opportunitylinetransaction.msdyn_accountvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_amount                                                 |
| msdyn_opportunitylinetransaction.msdyn_amount_base                                            |
| msdyn_opportunitylinetransaction.msdyn_amountmethod                                           |
| msdyn_opportunitylinetransaction.msdyn_basisamount                                            |
| msdyn_opportunitylinetransaction.msdyn_basisamount_base                                       |
| msdyn_opportunitylinetransaction.msdyn_basisprice                                             |
| msdyn_opportunitylinetransaction.msdyn_basisprice_base                                        |
| msdyn_opportunitylinetransaction.msdyn_basisquantity                                          |
| msdyn_opportunitylinetransaction.msdyn_billingtype                                            |
| msdyn_opportunitylinetransaction.msdyn_bookableresource                                       |
| msdyn_opportunitylinetransaction.msdyn_contactcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_contactvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_customertype                                           |
| msdyn_opportunitylinetransaction.msdyn_description                                            |
| msdyn_opportunitylinetransaction.msdyn_documentdate                                           |
| msdyn_opportunitylinetransaction.msdyn_enddatetime                                            |
| msdyn_opportunitylinetransaction.msdyn_exchangeratedate                                       |
| msdyn_opportunitylinetransaction.msdyn_opportunityline                                        |
| msdyn_opportunitylinetransaction.msdyn_opportunitylinetransactionid                           |
| msdyn_opportunitylinetransaction.msdyn_percent                                                |
| msdyn_opportunitylinetransaction.msdyn_price                                                  |
| msdyn_opportunitylinetransaction.msdyn_price_base                                             |
| msdyn_opportunitylinetransaction.msdyn_pricelist                                              |
| msdyn_opportunitylinetransaction.msdyn_product                                                |
| msdyn_opportunitylinetransaction.msdyn_project                                                |
| msdyn_opportunitylinetransaction.msdyn_quantity                                               |
| msdyn_opportunitylinetransaction.msdyn_resourcecategory                                       |
| msdyn_opportunitylinetransaction.msdyn_resourceorganizationalunitid                           |
| msdyn_opportunitylinetransaction.msdyn_startdatetime                                          |
| msdyn_opportunitylinetransaction.msdyn_task                                                   |
| msdyn_opportunitylinetransaction.msdyn_transactioncategory                                    |
| msdyn_opportunitylinetransaction.msdyn_transactionclassification                              |
| msdyn_opportunitylinetransaction.msdyn_transactiontypecode                                    |
| msdyn_opportunitylinetransaction.msdyn_unit                                                   |
| msdyn_opportunitylinetransaction.msdyn_unitschedule                                           |
| msdyn_opportunitylinetransaction.msdyn_vendortype                                             |

### <a name="msdyn_opportunitylinetransactioncategory"></a>msdyn_opportunitylinetransactioncategory

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactioncategory.msdyn_billingtype                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_description                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactioncategoryid           |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactionclassification       |
| msdyn_opportunitylinetransactioncategory.msdyn_transactioncategory                            |

### <a name="msdyn_opportunitylinetransactionclassificatio"></a>msdyn_opportunitylinetransactionclassificatio

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactionclassificatio.msdyn_billingtype                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_description                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_include                                   |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunityline                           |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunitylinetransactionclassificatioid |
| msdyn_opportunitylinetransactionclassificatio.msdyn_transactionclassification                 |

### <a name="msdyn_orderlineresourcecategory"></a>msdyn_orderlineresourcecategory

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlineresourcecategory.msdyn_contractline                                            |

### <a name="msdyn_orderlinetransaction"></a>msdyn_orderlinetransaction

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransaction.msdyn_salescontractline                                            |
| msdyn_orderlinetransactioncategory.msdyn_contractline                                         |

### <a name="msdyn_orderlinetransactionclassification"></a>msdyn_orderlinetransactionclassification

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransactionclassification.msdyn_contractline                                   |

### <a name="msdyn_project"></a>msdyn_project

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_project.msdyn_actualdurationminutes                                                     |
| msdyn_project.msdyn_actualhours                                                               |
| msdyn_project.msdyn_template                                                                |
| msdyn_project.msdyn_plannedhours                                                              |
| msdyn_project.msdyn_projecttemplate                                                           |
| msdyn_project.msdyn_remaininghours                                                            |
| msdyn_project.msdyn_scheduldurationminutes                                                  |
| msdyn_project.msdyn_scheduledend                                                              |
| msdyn_project.msdyn_stagename                                                                 |
| msdyn_project.msdyn_wbsduration                                                               |


### <a name="msdyn_projecttask"></a>msdyn_projecttask

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttask.msdyn_actualdurationminutes                                                 |
| msdyn_projecttask.msdyn_actualeffort                                                          |
| msdyn_projecttask.msdyn_aggregationdirection                                                  |
| msdyn_projecttask.msdyn_assignedresources                                                     |
| msdyn_projecttask.msdyn_assignedteammembers                                                   |
| msdyn_projecttask.msdyn_autoscheduling                                                        |
| msdyn_projecttask.msdyn_costestimatecontour                                                   |
| msdyn_projecttask.msdyn_effortcontour                                                         |
| msdyn_projecttask.msdyn_islinetask                                                            |
| msdyn_projecttask.msdyn_numberofresources                                                     |
| msdyn_projecttask.msdyn_remaininghours                                                        |
| msdyn_projecttask.msdyn_resourceutilization                                                   |
| msdyn_projecttask.msdyn_salesestimatecontour                                                  |
| msdyn_projecttask.msdyn_scheduledhours                                                        |
| msdyn_projecttask.msdyn_wbsid                                                                 |

### <a name="msdyn_projecttaskstatususer"></a>msdyn_projecttaskstatususer

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttaskstatususer.msdyn_bookableresource                                            |
| msdyn_projecttaskstatususer.msdyn_description                                                 |
| msdyn_projecttaskstatususer.msdyn_expectedcompletiondate                                      |
| msdyn_projecttaskstatususer.msdyn_expectedhourstocompleter                                     |
| msdyn_projecttaskstatususer.msdyn_iscompleted                                                 |
| msdyn_projecttaskstatususer.msdyn_name                                                        |
| msdyn_projecttaskstatususer.msdyn_percentcomplete                                             |
| msdyn_projecttaskstatususer.msdyn_projecttaskid                                               |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatusindicator                                  |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatususerid                                     |

### <a name="msdyn_projectteam"></a>msdyn_projectteam

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteam.msdyn_applicantcount                                                        |
| msdyn_projectteam.msdyn_applicants dispoñible                                                   |
| msdyn_projectteam.msdyn_assignedhours                                                         |
| msdyn_projectteam.msdyn_description                                                           |
| msdyn_projectteam.msdyn_from                                                                  |
| msdyn_projectteam.msdyn_hoursrequested                                                        |
| msdyn_projectteam.msdyn_membershipstatus                                                      |
| msdyn_projectteam.msdyn_number                                                                |
| msdyn_projectteam.msdyn_to                                                                    |

### <a name="msdyn_projectteammembersignup"></a>msdyn_projectteammembersignup

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteammembersignup.msdyn_bookableresource                                          |
| msdyn_projectteammembersignup.msdyn_membershipstatus                                          |
| msdyn_projectteammembersignup.msdyn_name                                                      |
| msdyn_projectteammembersignup.msdyn_projectteammembersignupid                                 |
| msdyn_projectteammembersignup.msdyn_teammembership                                            |

### <a name="msdyn_projecttransactioncategory"></a>msdyn_projecttransactioncategory

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttransactioncategory.msdyn_billingtype                                            |
| msdyn_projecttransactioncategory.msdyn_name                                                   |
| msdyn_projecttransactioncategory.msdyn_project                                                |
| msdyn_projecttransactioncategory.msdyn_projecttransactioncategoryid                           |
| msdyn_projecttransactioncategory.msdyn_transactioncategory                                    |

### <a name="msdyn_quotelineinvoiceschedule"></a>msdyn_quotelineinvoiceschedule

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_quotelineinvoiceschedule.msdyn_quoteline                                                |
| msdyn_quotelineresourcecategory.msdyn_quoteline                                               |
| msdyn_quotelinesscheduleofvalue.msdyn_quoteline                                                |
| msdyn_quotelinetransaction.msdyn_quoteline                                                    |
| msdyn_quotelinetransactioncategory.msdyn_quoteline                                            |
| msdyn_quotelinetransactionclassification.msdyn_quoteline                                      |

### <a name="msdyn_resourceassignment"></a>msdyn_resourceassignment

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_resourceassignment.msdyn_hours                                                          |
| msdyn_resourceassignment.msdyn_fromdate                                                       |
| msdyn_resourceassignment.msdyn_msprojectclientid                                              |
| msdyn_resourceassignment.msdyn_todate                                                         |
| msdyn_resourceassignmentdetail.msdyn_duration                                                 |
| msdyn_resourceassignmentdetail.msdyn_from                                                     |
| msdyn_resourceassignmentdetail.msdyn_name                                                     |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentdetailid                               |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentid                                     |

### <a name="salesorderdetail"></a>Detalle do pedido de vendas

| Campos                                                    |
|-----------------------------------------------------------------------------------------------|
| salesorderdetail.msdyn_quoteline                                                              |

