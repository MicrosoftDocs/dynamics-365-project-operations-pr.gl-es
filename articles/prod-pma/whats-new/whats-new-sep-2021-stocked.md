---
title: Novidades e cambios en Project Operations de setembro 2021 para situacións baseadas en produción/con fornecemento
description: Este artigo ofrece información sobre as actualizacións de calidade que están dispoñibles na versión de setembro de 2021 de Project Operations para situacións baseadas en produción/con fornecemento.
author: andchoi
ms.date: 11/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: be0f397df4a3e1973e1f5546e43b2cf9578950a0
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029850"
---
# <a name="whats-new-or-changed-in-project-operations-september-2021-for-stockedproduction-based-scenarios"></a>Novidades e cambios en Project Operations de setembro 2021 para situacións baseadas en produción/con fornecemento

_**Aplícase a:** Project Operations para situacións baseadas en produción/con fornecemento_

Este artigo aplícase aos seguintes compoñentes e versións de Microsoft Dynamics 365 Project Operations:

- Xestión e contabilidade de proxectos nun ambiente de aplicacións de Dynamics 365 Finance versión 10.0.21
 
## <a name="quality-updates"></a>Actualizacións de calidade

| Área de funcionalidades | Número de referencia | Actualización de calidade |
|---|---|---|
| Xestión e contabilidade de proxectos | [412077](https://fix.lcs.dynamics.com/Issue/Details/?bugId=412077) | Se o rol de xestor de compras ten acceso a unha persoa xurídica, tamén obtén acceso a todos os proxectos de todas as persoas xurídicas. |
| Xestión e contabilidade de proxectos | [537214](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537214) | Prodúcese un problema de redondeo do imposto sobre o valor engadido (IVE) mentres se liquida unha nota de crédito contra unha factura orixinal do proxecto. |
| Xestión e contabilidade de proxectos | [538002](https://fix.lcs.dynamics.com/Issue/Details/?bugId=538002) | Use un orzamento de proxecto alternativo para a verificación do orzamento. |
| Xestión e contabilidade de proxectos | [546265](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546265) | O grupo de prezos **Prezo de venda hora** non se calcula na estrutura de subdivisión do traballo para as cotizacións do proxecto. |
| Xestión e contabilidade de proxectos | [555604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=555604) | A eliminación da estimación falla cando a funcionalidade **Activar a moeda do contrato do proxecto para o cálculo da estimación** está activada. |
| Xestión e contabilidade de proxectos | [563523](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563523) | A factorización do imposto sobre as vendas por cantidade engádese ao importe do prezo de venda cando se usa o imposto de uso no grupo de impostos sobre vendas do diario de gastos do proxecto. |
| Xestión e contabilidade de proxectos | [564701](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564701) | O imposto condicional non se calcula correctamente para o último pagamento cando se aplicou a retención do fornecedor e o prepagamento a facturas de pedido de compra. |
| Xestión e contabilidade de proxectos | [565642](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565642) | O rastrexo de axustes non funciona para os diarios de saldo de inicio. |
| Xestión e contabilidade de proxectos | [568814](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568814) | **Dotación de revisión do orzamento do proxecto por período** divídese en todos os períodos orzamentarios. Cando se envía a asignación, o rexistro non se borra. |
| Xestión e contabilidade de proxectos | [569250](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569250) | As contabilizacións de traballo en proceso (WIP) no libro maior teñen unha cantidade incorrecta. |
| Xestión e contabilidade de proxectos | [570731](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570371) | A aprobación do diario de horas do proxecto non funciona. |
| Xestión e contabilidade de proxectos | [571391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571391) | O prezo de venda do axuste do proxecto non se actualiza cos custos indirectos cando non se marca o límite de financiamento. |
| Xestión e contabilidade de proxectos | [575831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575831) | Non se pode crear un requisito de artigo cando se factura a cabeceira da táboa de vendas e se finaliza a orde de compra de respaldo das liñas existentes. |
| Xestión e contabilidade de proxectos | [578036](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578036) | O importe de retención dunha regra de facturación que ten un fito para un proxecto diferente non se publica no ID do proxecto correspondente que se seleccionou para o fito. Pola contra, contabilízase co primeiro proxecto. |
| Xestión e contabilidade de proxectos | [578327](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578327) | Cando seleccione **Conxunto de dimensión financeira** nunha proposta de factura, prodúcese o seguinte erro: "Non se pode emitir o obxecto do tipo "Dynamics.AX.Application.FormIntControl' para escribir 'Dynamics.AX.Application.FormStringControl'." |
| Xestión e contabilidade de proxectos | [581167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581167) | O informe **Factura de proxecto** omite liñas. |
| Xestión e contabilidade de proxectos | [581489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581489) | Prodúcese un erro ao calcular o control de custos dun proxecto de investimento. |
| Xestión e contabilidade de proxectos | [590357](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590357) | O método **ProjTable::InitFromCustTable - canDeletePostalAddress** causa un problema de rendemento. |
| Xestión e contabilidade de proxectos | [592493](https://fix.lcs.dynamics.com/Issue/Details/?bugId=592493) | A mensaxe de erro debería ser máis clara que "Erro inesperado". |
| Xestión e contabilidade de proxectos | [598810](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598810) | O traballo por lotes de contabilización de facturas do proxecto procesa y contabiliza a proposta de factura incluso se as liñas de factura non se xeraron. |
| Xestión e contabilidade de proxectos | [574282](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574282) | Prodúcese un problema de redondeo cando se desactiva a clave de configuración da licenza do sector público. Xérase un custo ou prezo de venda incorrecto nas horas da folla de control horario para contratos que teñen varias fontes de financiamento. |
| Xestión e contabilidade de proxectos | [577598](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577598) | O prezo de venda do proxecto nun pedido de compra do proxecto facturado calcúlase incorrectamente cando o modelo de prezo de venda é **Proporción de contribución**. |
| Xestión e contabilidade de proxectos | [580784](https://fix.lcs.dynamics.com/Issue/Details/?bugId=580784) | O sistema non considera os días activos intermedios cando calcula a taxa de traballo efectiva dun empregado. |
| Xestión e contabilidade de proxectos | [584054](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584054) | Prodúcese un erro de contabilización na folla de control horario entre empresas debido ao seguinte erro de validación: "Ningún socio comercial está configurado para a persoa xurídica". |
| Xestión e contabilidade de proxectos | [586303](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586303) | A descrición dun pedido de compra que ten unha categoría de gasto non se recupera na lista de transaccións do proxecto publicada. |
| Xestión e contabilidade de proxectos | [590349](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590349) | Hai unha conversión incorrecta nos diarios de elementos que se publican nun proxecto. |
| Xestión e contabilidade de proxectos | [557294](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557294) | Pode confirmar un pedido de compra aínda que se supere o límite de financiamento. |
| Xestión e contabilidade de proxectos | [574162](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574162) | A sección **Corrección/Cancelar factura** dunha factura de texto libre desaparece cando se selecciona un ID de proxecto. |
| Xestión e contabilidade de proxectos | [575425](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575425) | Hai problemas de rendemento cando se publica unha proposta de factura dun proxecto desde un pedido de venda do proxecto que inclúe un artigo en existencias. |
| Xestión e contabilidade de proxectos | [575939](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575939) | Non se contabilizar publicar as facturas de compra do proxecto porque se produce o seguinte erro: "Chamouse incorrectamente á función AccDistProcessorProjectExtension.createForProjectRevenueLine". |
| Xestión e contabilidade de proxectos | [578970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578970) | Actualización da creación de traballos por lotes de estimación de proxectos para soportar a execución de múltiples subtarefas. |
| Xestión e contabilidade de proxectos | [584519](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584519) | Non se pode actualizar o estado dunha folla de control horario a **Borrador** cando o fluxo de traballo está atrapado nun estado **Cancelado**. |
| Xestión e contabilidade de proxectos | [584757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584757) | Os importes de retención non se calculan na proposta de factura da nota de crédito se hai varias liñas. |
| Xestión e contabilidade de proxectos | [586034](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586034) | Cando tenta cambiar o importe dunha factura xerada a partir dun pedido de compra, prodúcese o seguinte erro: "As transaccións do vale non se equilibran segundo XX/XX/XXXX. (divisa de contabilidade: 0,00 - divisa de informes: 0,01)". |
| Xestión e contabilidade de proxectos | [588714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588714) | Hai un problema de rendemento cando unha proposta de factura de proxecto se publica en modo por lotes, debido á unión con **GeneralJournalAccountEntryl**. |
| Xestión e contabilidade de proxectos | [588851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588851) | Hai problemas de rendemento cando se publica unha folla de control horario. |
| Xestión e contabilidade de proxectos | [590535](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590535) | A xerarquía de estimacións de custos da estrutura de subdivisión do traballo non está aliñada correctamente despois de que todas as tarefas se expandan ou despois de que unha única tarefa se expanda manualmente. |
| Xestión e contabilidade de proxectos | [593663](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593663) | O modelo de Excel de cotización do proxecto non se pode engadir ao menú **Abrir en Excel**. |
| Xestión e contabilidade de proxectos | [596669](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596669) | O número de exención fiscal dunha persoa xurídica non se inclúe na factura impresa do proxecto. |
| Xestión e contabilidade de proxectos | [597563](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597563) | Non se actualizan os datos financeiros no erro da unidade de inventario cando se axusta un proxecto en relación coas liñas de crédito. |
| Xestión e contabilidade de proxectos | [598109](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598109) | Despois de aplicar KB 461935, non pode publicar estimacións se cambia a secuencias numéricas continuas. |
| Xestión e contabilidade de proxectos | [598688](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598688) | **TimeEntryDataManager** provoca a aplicación móbil da folla de control horario do proxecto para Android para deixar de responder. |
| Xestión e contabilidade de proxectos | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | O valor WIP invertido da contabilización de facturas é diferente do valor WIP contabilizado orixinalmente da entrada de tempo. |
| Xestión e contabilidade de proxectos | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Nos casos de retencións aplicadas, as transacción dun comprobante non cadran cando se contabilizan os ingresos facturados dun proxecto. |
| Xestión e contabilidade de proxectos | [603320](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603320) | Cando a funcionalidade **Mellora do rendemento da programación de recursos do proxecto** está activada, os valores decimais están redondeados incorrectamente para a dispoñibilidade e capacidade dos recursos. |
| Xestión e contabilidade de proxectos | [607324](https://fix.lcs.dynamics.com/Issue/Details/?bugId=607324) | Cando a funcionalidade **Crear estimacións do proxecto usando varias tarefas por lotes** está activada, a creación de estimacións nun lote que ten varias subtarefas só funciona para o período actual. |
| Viaxes e gasto | [551911](https://fix.lcs.dynamics.com/Issue/Details/?bugId=551911) | Ignórase unha política de solicitude de viaxe e o fluxo de traballo se aproba sen erros. |
| Viaxes e gasto | [563752](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563752) | <p>A aplicación Mobile Expense non garda a seguinte información na liña de gasto:</p><ul><li>O ID do proxecto</li><li>Se o gasto é facturable</li><li>O número da actividade</li></ul> |
| Viaxes e gasto | [569458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569458) | O campo **Recibos anexados** está definido como **Si** aínda que a liña de gastos non teña un recibo anexado. |
| Viaxes e gasto | [571334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571334) | Aparece un erro cando tenta cambiar a categoría de gasto a **Persoal**. |
| Viaxes e gasto | [572783](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572783) | Non se pode anexar un recibo e editar o gasto principal despois de dividir unha transacción de tarxeta de crédito a un gasto persoal |
| Viaxes e gasto | [574252](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574252) | A política de gastos para transaccións entre empresas que teñen un ID de proxecto non funciona correctamente. |
| Viaxes e gasto | [574489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574489) | Falta a información da data de contabilzación para os informes de gastos contabilizados. |
| Viaxes e gasto | [574504](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574504) | Na aplicación para móbil Expense hai problemas de métodos de pago. |
| Viaxes e gasto | [584799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584799) | Unha solicitude de viaxe que se crea para un traballador pode usarse para o informe de gastos doutro traballador antes da data do delegado. |
| Viaxes e gasto | [586023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586023) | Cando se crea un gasto, os cambios de valores de dimensión financeira non se actualizan correctamente a nivel de distribución contable na área de traballo **Xestión de gastos**. |
| Viaxes e gasto | [586081](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586081) | O estado de aprobación da liña de gasto principal non se sincroniza co estado de aprobación do fluxo de traballo detallado da liña. |
| Viaxes e gasto | [590544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590544) | Prodúcese un erro se contabiliza un informe de gastos e se activa a recuperación de impostos. |
| Viaxes e gasto | [564851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564851) | Un delegado non pode eliminar os documentos de gastos dun empregado cesado. |
| Viaxes e gasto | [587306](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587306) | A eliminación dunha liña de gasto leva máis tempo do esperado e afecta ao rendemento. |
| Viaxes e gasto | [600455](https://fix.lcs.dynamics.com/Issue/Details/?bugId=600455) | **TrvExpTrans** causa un rexistro **TaxUncommitted** orfo, porque só se elimina **SourceDocumentLine**. |
| Viaxes e gasto | [609918](https://fix.lcs.dynamics.com/Issue/Details/?bugId=609918) | **ReleaseUpdateDB72_Expense.updateTrvExpTransProjTransId()** non permite a **trvExpTrans.ReferenceDataAreaId** crear a nova secuencia numérica. |

## <a name="regulatory-updates"></a>Actualizacións normativas

Para obter información sobre actualizacións normativas para aplicacións de finanzas e operacións, vexa [Actualizacións normativas](/dynamics365/finance/localizations/regulatory-updates). Tamén pode iniciar sesión en Microsoft Dynamics Lifecycle Services (LCS) e usar a ferramenta de busca de problemas para ver as actualizacións regulamentarias previstas. A busca de problemas permítelle buscar por país ou rexión, tipo de funcionalidade e lanzamento.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
