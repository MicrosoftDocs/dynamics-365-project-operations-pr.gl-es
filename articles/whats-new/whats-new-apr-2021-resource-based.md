---
title: Novidades de abril de 2021 - Project Operations para situacións baseadas en recursos/sen fornecemento
description: Este artigo ofrece información sobre as actualizacións de calidade dispoñibles na versión de abril de 2021 de Project Operations para escenarios baseados en recursos ou non almacenados.
author: sigitac
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: a060bdc4e4c9f37ec666b1cf4d078986ad1571db
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912422"
---
# <a name="whats-new-april-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades de abril de 2021 - Project Operations para situacións baseadas en recursos/sen fornecemento

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Este artigo aplícase ao seguinte Dynamics 365 Project Operations compoñentes e versións:

- Project Operations en ambiente de Dataverse versión 4.9.0.221
- Xestión de proxectos e contabilidade no entorno Dynamics 365 Finance versión 10.0.17

## <a name="features-included-in-this-release"></a>Funcionalidades incluídas nesta versión

As seguintes funcionalidades están incluídas nesta versión:

- Materiais sen fornecemento para proxectos. As principais capacidades son:
  - Estimación e fixación de prezos de materiais sen fornecemento durante o ciclo de vendas dun proxecto. Para obter máis información, consulte [Configurar taxas de custo e vendas para produtos de catálogo - lite](../pro/pricing-costing/set-up-cost-sales-rates-catalog-products.md).
  - Rastrexo do uso de materiais sen fornecemento durante a entrega do proxecto. Para obter máis información, consulte [Rexistrar o uso do material en proxectos e tarefas de proxecto](../material/material-usage-log.md).
  - Facturación de custos de material sen fornecemento usado. Para obter máis información, consulte [Xestionar o traballo pendente de facturación](../proforma-invoicing/manage-billing-backlog.md).
  - Para obter información sobre como configurar esta funcionalidade, consulte [Configurar materiais sen fornecemento e facturas pendentes do fornecedor](../procurement/configure-materials-nonstocked.md)
- Facturación baseada en tarefas: Engadiuse a posibilidade de asociar tarefas do proxecto ás liñas de contrato do proxecto, someténdoas ao mesmo método de facturación, frecuencia de facturación e clientes que o da liña de contrato. Esta asociación garante a facturación, a contabilidade, a estimación de ingresos e o recoñecemento precisos para traballar de acordo con esta configuración nas tarefas do proxecto.
- As novas API en Dynamics 365 Dataverse permiten crear, actualizar e eliminar operacións con **Entidades de programación**. Para obter máis información, consulte [Usar as API de programación para realizar operacións con entidades de programación](../project-management/schedule-api-preview.md).

## <a name="project-operations-dual-write-maps-updates"></a>Actualizacións de mapas de escrita dual en Project Operations

A seguinte lista mostra os mapas de escrita dual que foron modificados ou engadidos na versión de Project Operations de abril de 2021.

| **Mapa de entidades** | **Versión actualizada** | **Comentarios** |
| --- | --- | --- |
| Datos reais de integración de Project Operations (msdyn\_actuals) | 1.0.0.14 | Mapa modificado para sincronizar os datos reais do proxecto de material. |
| Entidade de integración de Project Operations para estimacións de gastos (msdyn\_estimateslines) | 1.0.0.2 | Engadiuse a sincronización da liña do contrato do proxecto ás aplicacións de Finanzas e Operacións para a compatibilidade de facturación baseada en tarefas. |
| Entidade de integración de Project Operations para estimacións de horas (msdyn\_resourceassignments) | 1.0.0.5 | Engadiuse a sincronización da liña do contrato do proxecto ás aplicacións de Finanzas e Operacións para a compatibilidade de facturación baseada en tarefas. |
| Táboa de integración de Project Operations para estimacións de material (msdyn\_estimatelines) | 1.0.0.0 | Novo mapa de táboa para sincronizar as estimacións de materiais desde Dataverse ás aplicacións de Finanzas e Operacións. |
| Entidade de exportación de facturas do fornecedor do proxecto de integración de Project Operations (msdyn\_projectvendorinvoices) | 1.0.0.0 | Novo mapa de táboas para sincronizar as cabeceiras das facturas de provedores das aplicacións de Finanzas e Operacións con Dataverse. |
| Entidade de exportación de liñas de facturas do fornecedor do proxecto de integración de Project Operations (msdyn\_projectvendorinvoicelines) | 1.0.0.0 | Novo mapa de táboas para sincronizar as liñas de facturas de provedores das aplicacións de Finanzas e Operacións a Dataverse. |

Sempre debes executar a versión máis recente do mapa no teu entorno e activar todos os mapas de táboas relacionados mentres actualizas as operacións do teu proxecto.Dataverse solución e versión da solución de Finanzas e Operacións. É posible que certas funcionalidades e capacidades non funcionen correctamente se a última versión do mapa non está activada. Pode ver a versión activa do mapa na columna **Versión** columna na páxina **Escrita dual**. Pode activar unha nova versión do mapa seleccionando **Versións do mapa de táboa**, seleccionando a versión máis recente e logo gardar a versión seleccionada. Se personalizou un mapa de táboa listo para usar, aplique de novo os cambios. Para obter máis información, consulte [Xestión do ciclo de vida da aplicación](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se ten algún problema ao iniciar o mapa, siga as instrucións da sección [Problema de falta de columnas da táboa nos mapas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) da guía de resolución de problemas de escrita dual.

## <a name="quality-updates"></a>Actualizacións de calidade

### <a name="project-operations-in-dynamics-365-dataverse"></a>Project Operations en Dynamics 365 Dataverse

| **Área de funcionalidades** | **Número de referencia** | **Actualización de calidade** |
| --- | --- | --- |
| Facturación e prezos | 2124532 | O botón **Corrixir factura** móstrase nunha factura proforma cando o importe de retención ou o importe de retención aplicado está presente na factura orixinal. O botón só se amosa para ambientes coa versión de Finance 10.0.19 ou superior. |
| Facturación e prezos | 2224568 | Engadiuse lóxica para permitir as personalizacións que implican invocar o complemento de confirmación da factura. |
| Facturación e prezos | 2101098 | Mellorouse a lóxica dos campos predefinidos para a factura proforma: **Enderezo de facturación**, **Nome de facturación** e **Condicións de pagamento** agora son os predefinidos no rexistro de cliente do contrato do proxecto correspondente. |
| Facturación e prezos | 2021413 | Actualizáronse os campos **Custo real** e **Vendas** na entidade **Tarefa** para incluír valores de vendas de gastos non facturados e facturados en tarefas. |
| Facturación e prezos | 2182110 | Ao copiar un contrato de proxecto, o ID da liña de contrato rexenerase no contrato de proxecto de destino para garantir que sexa único. |
| Xestión de oportunidades | 2186741 | Engadíronse validacións para garantir que o campo **Orixe** e **Tipo de transacción** non se poden actualizar nos detalles da liña de oferta existente. |
| Xestión de oportunidades | 2191353 | Non se deben crear fitos nunha liña de contrato de tempo e material. |
| Xestión de oportunidades | 2216956 | Solucionáronse problemas con **Actualizar prezos**. |
| Planificación e rastrexo | 2182979 | Mellorouse a función de copia do proxecto para garantir que se copian as liñas de estimación de gastos do proxecto orixinal. |
| Planificación e rastrexo | 2184144 | Mellorouse a función de copia do proxecto para garantir que se copia o nome do posto do recurso do proxecto orixinal. |
| Planificación e rastrexo | 2184799 | Copia do proxecto: Axustouse o control para garantir que a data estimada de inicio non se poida cambiar mentres a copia estea en curso. |
| Planificación e rastrexo | 2185134 | Copia do proxecto: A data de inicio estimada do proxecto de destino establécese na data de hoxe. |
| Planificación e rastrexo | 2196373 | Copia do proxecto: Garantir que o xestor do proxecto e os rexistros dos membros do equipo non están duplicados no equipo do proxecto. |
| Planificación e rastrexo | 2211833 | Copia do proxecto: As atribucións de recursos cópianse da tarefa do proxecto de orixe ao proxecto de destino. |
| Planificación e rastrexo | 2186541 | Solucionáronse problemas na grade **Estimacións** ao agruparse por recurso. |
| Planificación e rastrexo | 2166906 | A categoría de transacción dunha tarefa debe copiarse na entidade **Atribución de recursos**. |
| Xestión de recursos | 2125362 | Solucionáronse problemas coa creación dun membro xenérico do equipo mediante un método de asignación baseado en horas. |
| Tempo e gasto | 2113603 | Solucionouse o problema relacionado coa personalización coa eliminación de atributos da páxina **Entrada de tempo**. Agora o sistema comproba se o atributo existe na páxina antes de acceder a eles mediante un script. |
| Tempo e gasto | 2204377 | As follas de control horario copiadas deben amosarse automaticamente cando selecciona **Copiar Semana** durante a entrada de tempo. |
| Tempo e gasto | 2209059 | O campo **Estado** pode editarse para entradas de tempo de Dynamics 365 Field Service. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Xestión de proxectos e contabilidade en Dynamics 365 Finance

| **Área de funcionalidades** | **Número de referencia** | **Actualización de calidade** |
| --- | --- | --- |
| Xestión e contabilidade de proxectos | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | A eliminación da estimación inversa non funciona na sección **Periódico**.  |
| Xestión e contabilidade de proxectos | [509773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509773) | A funcionalidade **Axuste contable** crea un problema coas contas de libro maior que teñen **Non permitir a entrada manual** seleccionado. |
| Xestión e contabilidade de proxectos | [510728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=5109728) | Engadiuse unha lóxica empresarial para procesar as facturas de corrección, incluído o importe da retención ou o importe da retención aplicada. |
| Xestión e contabilidade de proxectos | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | A contabilización do valor das vendas WIP na facturación de proxectos entre empresas escolle unha conta inesperada. |
| Xestión e contabilidade de proxectos | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | Cando se traballa con retencións en Project Operations, cambiar o proxecto por defecto nun contrato despois de facturar os pagos anticipados provoca problemas coas deducións entrantes. |
| Xestión e contabilidade de proxectos | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | En Project Operations, eliminar un proxecto dun contrato debería restablecer o proxecto predefinido do contrato, se fose necesario. |
| Xestión e contabilidade de proxectos | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | En Project Operations, as liñas de gasto incorrectas móstranse na lista **Engadir liña** na factura entre empresas. |
| Xestión e contabilidade de proxectos | [543968](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543968) | En Project Operations, a páxina **Contrato de compra** non é visible nas entidades legais de Finance integradas con Project Operations. |
| Xestión e contabilidade de proxectos | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | Por mor dun erro de integración de Dataverse, non pode converter unha oferta en gañada en Project Operations. |
| Xestión e contabilidade de proxectos | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | **ProjCDSProjectContractEntity** pode definir o enderezo da factura da orixe de financiamento dun cliente diferente.  |
| Xestión e contabilidade de proxectos | [557376](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557376) | En Project Operations, non se selecciona ningunha dimensión cando se crea unha factura de contabilización para una transacción. |
| Viaxes e gasto | [441256](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441256) | O saldo anticipado de efectivo non se actualiza para un informe de gastos se se aproba e contabiliza liña por liña. |
| Viaxes e gasto | [482041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482041) | Os impostos para informes detallados de gastos entre empresas non se calculan correctamente. |
| Viaxes e gasto | [483469](https://fix.lcs.dynamics.com/Issue/Details/?bugId=483469) | Os campos adicionais relacionados cos proxectos móstranse na páxina **Informes de gastos entre empresas** modificada. |
| Viaxes e gasto | [486592](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486592) | Aparece unha mensaxe de erro incorrecta nos recibos de cabeceira dos informes de gastos. |
| Viaxes e gasto | [487971](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487971) | Un informe de gastos contabilízase incorrectamente nunha situación entre empresas se o imposto sobre as vendas se contabiliza na entidade legal de destino. |
| Viaxes e gasto | [505696](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505696) | As datas de envío de informes non se imprimen nos informes de gastos aprobados. |
| Viaxes e gasto | [508726](https://fix.lcs.dynamics.com/Issue/Details/?bugId=508726) | Os campos **Data de aprobación** e **Data de rexeitamento** non se enchen despois de aprobarse un gasto. |
| Viaxes e gasto | [509913](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509913) | Unha solicitude de viaxe creada para un traballador pódese utilizar para o informe de gastos doutro traballador. |
| Viaxes e gasto | [518186](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518186) | As categorías de gasto bloquéanse ao engadir unha nova liña de gasto. |
| Viaxes e gasto | [520914](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520914) | Ao detallar unha liña de informe de gastos xa dividida prodúcese unha contabilización incompleta do bono contas pendentes de pago/libro maior e falla o explorador de orixe de contabilidade porque **TRVEXPTRANS.SOURCEDOCUMENTLINE** está duplicado. |
| Viaxes e gasto | [521943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521943) | A política de solicitude de viaxes non funciona como se esperaba. |
| Viaxes e gasto | [522567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522567) | O nome da conta do fornecedor non aparece nas transaccións do proxecto contabilizadas para os informes de gastos. |
| Viaxes e gasto | [525106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525106) | En Project Operations, non pode aprobar o tempo cunha tarefa para un proxecto entre empresas. |
| Viaxes e gasto | [526336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=526336) | A categoría de devolución de adianto de efectivo non actualiza os saldos de adianto efectivo cando se contabiliza. |
| Viaxes e gasto | [527218](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527218) | O prezo de venda calcúlase incorrectamente nos informes de gastos creados en moeda estranxeira mediante transaccións de tarxeta de crédito importadas e asociados a un proxecto. |
| Viaxes e gasto | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | Retrocedeu a entidade de datos **TrvRequisitionLine** e o índice único asociado. |
| Viaxes e gasto | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | Engadiuse instrumentación á xeración de **SOURCEDOCUMENTLINE**. |
| Viaxes e gasto | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | O diario de contabilidade auxiliar incorrecto móstrase nunha situación entre empresas se o imposto sobre as vendas se contabiliza na entidade legal de destino. |
| Viaxes e gasto | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | En Project Operations, as estimacións de gastos non se eliminan de Finance cando se eliminan de Dataverse. |
| Viaxes e gasto | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | Cando unha categoría de gasto non é unha categoría de proxecto, as dimensións financeiras seleccionadas na páxina **Gasto** non se copian no informe de gastos. |
