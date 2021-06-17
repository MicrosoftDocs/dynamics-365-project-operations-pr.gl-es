---
title: Novidades de xaneiro de 2021 - Project Operations para situacións baseadas en recursos/sen fornecemento
description: Este tema ofrece información sobre as actualizacións de calidade dispoñibles na versión de xaneiro de 2021 de Project Operations para situacións baseadas en recursos/sen fornecemento.
author: sigitac
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: c600c30acd5e07e6370459928e33033a6ba418d6
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995754"
---
# <a name="whats-new-january-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades de xaneiro de 2021 - Project Operations para situacións baseadas en recursos/sen fornecemento

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_


Este tema aplícase aos seguintes compoñentes e versións de Dynamics 365 Project Operations:

  - Project Operations en ambiente de Dataverse versión 4.6.0.154
  - Xestión e contabilidade de proxectos en ambiente de Dynamics 365 Finance versión 10.0.16

## <a name="quality-updates"></a>Actualizacións de calidade

### <a name="project-operations-on-dataverse"></a>Project Operations en Dataverse

| **Área de funcionalidades** | **Número de referencia** | **Actualización de calidade** |
| --- | --- | --- |
| **Despregamento e configuración** | 2106818 | Corrixiuse o cambio de nome do recurso web que causaba problemas relacionados coa personalización dunha páxina. |
| **Facturación e prezos** | 2091908 | Corrixiuse a visibilidade das opcións **Bloqueo de prezos** e **Usar o prezo actual** na páxina **Factura** páxina cando se instala Project Operations xunto con Dynamics 365 Field Service. |
| **Facturación e prezos** | 2103058 | Actualizouse **Totais do proxecto** para xestionar valores nulos para o custo real dunha tarefa. |
| **Facturación e prezos** | 2116100 | Melloráronse as mensaxes de erro empregadas coa funcionalidade **Corrixir entradas correctas en datos reais**. |
| **Facturación e prezos** | 2116129 | Mellorouse a visibilidade das estimacións de gastos no separador **Estimacións** na páxina **Proxectos**. |
| **Facturación e prezos** | 2119112 | Corrixiuse a agregación das vendas reais e do custo real cando se utilizan diferentes taxas de cambio. |
| **Facturación e prezos** | 2134705 | Corrixiuse o erro "Non se pode ler a propiedade **getResourceString** de indefinido" cando a páxina **Factura** está aberta e Field Service está instalado. |
| **Xestión de oportunidades** | 2022195 | A grade de facturación baseada en tarefas na páxina **Proxecto** inclúe unha icona que indica que hai un contrato ou liña de oferta ligado a esa tarefa. |
| **Xestión de oportunidades** | 2029135 | Corrixiuse o erro do proceso de negocio que se produce cando un usuario intenta abrir unha liña de factura nunha factura confirmada que ten un importe anticipado facturado. |
| **Xestión de oportunidades** | 2040713 | Corrixiuse o erro de script que se producía ao crear unha factura a partir dun contrato e está instalado Field Service. |
| **Planificación e rastrexo de proxectos** | 2090202 | Regras de negocio marcadas que xa non se usan como **Obsoleto**. |
| **Tempo e gasto** | 2091249 | Reforzáronse os controis para que os usuarios non poidan cambiar a tarefa nunha entrada de tempo aprobada ou enviada. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Xestión e contabilidade de proxectos en Dynamics 365 Finance

| **Área de funcionalidades** | **Número de referencia** | **Actualización de calidade** |
| --- | --- | --- |
| **Xestión e contabilidade de proxectos** | [478667](https://fix.lcs.dynamics.com/Issue/Details/?bugId=478667) | Importe incorrecto do contrato na páxina **A conta** para un proxecto a prezo fixo con varias fontes de financiamento. |
| **Xestión e contabilidade de proxectos** | [480260](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480260) | O marcador de posición **Invoiceproposal.PSAnfRefProjId** non mostra o ID do proxecto para o fluxo de traballo **Revisar as propostas de factura do proxecto**. |
| **Xestión e contabilidade de proxectos** | [481227](https://fix.lcs.dynamics.com/Issue/Details/?bugId=481227) | Utilízase a data de desconto de efectivo incorrecta ao contabilizar as propostas de factura do proxecto. |
| **Xestión e contabilidade de proxectos** | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558) | Eliminar e ler as atribucións de recursos en Project Operations duplica as entradas de previsión do proxecto en Finance. |
| **Xestión e contabilidade de proxectos** | [484468](https://fix.lcs.dynamics.com/Issue/Details/?bugId=484468) | En Project Operations, non pode crear estimacións do proxecto en Dataverse sen ter unha liña de contrato no proxecto. |
| **Xestión e contabilidade de proxectos** | [485871](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485871) | A dimensión financeira dunha transacción de gastos do proxecto non está sincronizada co vale relacionado e coa distribución contable do informe de gastos cando os custos se contabilizan no saldo. |
| **Xestión e contabilidade de proxectos** | [488382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488382) | O filtro de **Estado da factura** nas transaccións do proxecto publicado para proxectos de prezo fixo non funciona. |
| **Xestión e contabilidade de proxectos** | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | A eliminación da estimación inversa non funciona na sección **Periódico**. |
| **Xestión e contabilidade de proxectos** | [509989](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509989) | As liñas de proposta de factura pódense eliminar en Project Operations cando se integra con Dataverse. |
| **Xestión e contabilidade de proxectos** | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041) | Impida activar a funcionalidade de varias liñas de contrato sen a integración de Dataverse. |
| **Xestión e contabilidade de proxectos** | [510527](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510527) | Cando a facturación a conta é igual aos resultados, os ingresos facturados aparecen como cero na páxina Estimacións. |
| **Xestión e contabilidade de proxectos** | [514167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514167) | As correccións de facturas non funcionan en ambientes integrados. |
| **Xestión e contabilidade de proxectos** | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | Cando se contabiliza o valor das vendas WIP na facturación de proxectos entre empresas, selecciónase unha conta incorrecta. |
| **Xestión e contabilidade de proxectos** | [514385](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514385) | En Project Operations, as dependencias das tarefas estimadas en Dataverse non se poden actualizar. |
| **Xestión e contabilidade de proxectos** | [515258](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515258) | Eliminar repetidamente os diarios de integración de Project Operations en Finance leva á perda de datos. |
| **Xestión e contabilidade de proxectos** | [519716](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519716) | Prodúcese o seguinte erro ao contabilizar a proposta de factura do proxecto: "A transacción non se salda na divisa de informes cando se engade de novo a factura de anticipo deducida". |
| **Xestión e contabilidade de proxectos** | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | Inclúese o ID de proxecto incorrecto nas deducións despois de que o contrato de proxecto predeterminado se actualice en Project Operations. |
| **Xestión e contabilidade de proxectos** | [522799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522799) | O recoñecemento de estimacións e ingresos non se pode completar cando se activa Project Operations. |
| **Xestión e contabilidade de proxectos** | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | En Project Operations, eliminar un proxecto dun contrato non restablece o proxecto predefinido no contrato. |
| **Xestión e contabilidade de proxectos** | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | En Project Operations, nunha factura entre empresas, as liñas de gasto incorrectas aparecen na lista **Engadir liña**. |
| **Viaxes e gasto** | [515334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515334) | Non se poden contabilizar liñas de gastos porque falta a configuración de horas na liña de contrato. |
| **Viaxes e gasto** | [437673](https://fix.lcs.dynamics.com/Issue/Details/?bugId=437673) | Cando a validación do proxecto/categoría é obrigatoria, as categorías de gastos asociadas ao proxecto non son visibles no informe de gastos. |
| **Viaxes e gasto** | [441256](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441256) | O saldo anticipado de efectivo non se actualiza cando se contabiliza un informe de gastos por liña. |
| **Viaxes e gasto** | [465396](https://fix.lcs.dynamics.com/Issue/Details/?bugId=465396) | O traballo **Actualizar información de pagamento** falla despois de inverter as liquidacións cando se liquidou unha factura con dúas ou máis transaccións de pagamento. |
| **Viaxes e gasto** | [472892](https://fix.lcs.dynamics.com/Issue/Details/?bugId=472892) | Hai un problema co cálculo da redución da comida do último día para a categoría de gastos de dietas. |
| **Viaxes e gasto** | [477714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=477714) | O informe **Tipo de gasto por empregado** non mostra gastos detallados se a primeira conexión dun usuario estaba no idioma es-MX. |
| **Viaxes e gasto** | [487516](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487516) | O pagamento do fornecedor por unha factura de informe de gastos está a usar unha conta de resumo incorrecta para contabilizar a liquidación. |
| **Viaxes e gasto** | [487531](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487531) | Cando un informe de gastos se contabiliza con **Permitir agrupar transaccións en función da conta de pagamento compensado** e **Corrección da data de contabilidade ao contabilizar** activados, as datas contables non se agrupan na táboa **Distribución contable**, o que afecta aos rexistros de impostos sobre vendas. |
| **Viaxes e gasto** | [488292](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488292) | A asignación de subcategorías de gastos elimínase cando Uso na caixa de verificación de gastos está desmarcada e logo se selecciona de novo. |
| **Viaxes e gasto** | [506175](https://fix.lcs.dynamics.com/Issue/Details/?bugId=506175) | Non se pode crear un informe de gastos entre empresas se o ID do proxecto se engade no nivel de cabeceira. |
| **Viaxes e gasto** | [509491](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509491) | Hai un problema cos pagamentos de gastos cando o importe do gasto é superior ao importe do adianto en efectivo. |
| **Viaxes e gasto** | [509556](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509556) | O campo **ID do proxecto** nun informe de gastos entre empresas está baleira se o rol de usuario está atribuído a unha organización específica. |
| **Viaxes e gasto** | [518186](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518186) | A categoría de gasto queda bloqueada ao engadir unha nova liña de gasto. |
| **Viaxes e gasto** | [520914](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520914) | Detallar as liñas do informe de gastos que xa están divididas da lugar a un vale de libro maior de Contas pendentes de pago\Xeral. Por mor da duplicación de **TRVEXPTRANS.SOURCEDOCUMENTLINE**, o Explorador de orixe de contabilidade tamén está interrompido. |
| **Viaxes e gasto** | [521768](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521768) | O índice engadido na táboa **TRVREQUISITIONLINE** para a que o cliente ten duplicados, causa un erro durante a actualización. |
| **Viaxes e gasto** | [525106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525106) | En Project Operations, o tempo non se pode crear nin aprobar con tarefas entre empresas en Dataverse. |

## <a name="regulatory-updates"></a>Actualizacións normativas

Para obter información sobre actualizacións normativas para aplicacións de Finance and Operations, vexa [Actualizacións normativas](/dynamics365/finance/localizations/regulatory-updates). Tamén pode iniciar sesión en LCS e ver as actualizacións normativas previstas usando a ferramenta de busca de problemas. A busca de problemas permítelle buscar por país, tipo de funcionalidade e lanzamento.


[!INCLUDE[footer-include](../includes/footer-banner.md)]