---
title: Novidades ou cambios en Project Operations, setembro de 2021 para escenarios abastecidos ou baseados na produción
description: Este tema ofrece información sobre as actualizacións de calidade que están dispoñibles na versión de setembro de 2021 de Project Operations para escenarios abastecidos ou baseados na produción.
author: andchoi
ms.date: 11/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: 24de8626199a3ed56bb6703b78d746ff7a43a089
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582018"
---
# <a name="whats-new-or-changed-in-project-operations-september-2021-for-stockedproduction-based-scenarios"></a>Novidades ou cambios en Project Operations, setembro de 2021 para escenarios abastecidos ou baseados na produción

_**Aplícase a:** Project Operations para situacións baseadas en produción/con fornecemento_

Este tema aplícase aos seguintes compoñentes e versións de Microsoft Dynamics 365 Project Operations:

- Xestión de proxectos e contabilidade nun entorno Dynamics 365 Finance versión 10.0.21
 
## <a name="quality-updates"></a>Actualizacións de calidade

| Área de funcionalidades | Número de referencia | Actualización de calidade |
|---|---|---|
| Xestión e contabilidade de proxectos | [412077](https://fix.lcs.dynamics.com/Issue/Details/?bugId=412077) | Se o rol de xestor de compras ten acceso a unha persoa xurídica, tamén terá acceso a todos os proxectos de todas as persoas xurídicas. |
| Xestión e contabilidade de proxectos | [537214](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537214) | Prodúcese un problema de redondeo do imposto sobre o valor engadido (IVE) mentres se liquida unha nota de crédito contra unha factura orixinal do proxecto. |
| Xestión e contabilidade de proxectos | [538002](https://fix.lcs.dynamics.com/Issue/Details/?bugId=538002) | Use un orzamento de proxecto alternativo para a verificación do orzamento. |
| Xestión e contabilidade de proxectos | [546265](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546265) | O **Prezo de venda hora** o grupo de prezos non se calcula na estrutura de desglose do traballo para as cotizacións do proxecto. |
| Xestión e contabilidade de proxectos | [555604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=555604) | A eliminación da estimación falla cando o **Activa a moeda do contrato do proxecto para o cálculo da estimación** a función está activada. |
| Xestión e contabilidade de proxectos | [563523](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563523) | A factorización do imposto de vendas por cantidade engádese ao importe do prezo de venda cando se utiliza o imposto de uso no grupo de impostos sobre vendas do diario de gastos do proxecto. |
| Xestión e contabilidade de proxectos | [564701](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564701) | O imposto condicional non se calcula correctamente para o último pago cando se aplica a retención de provedores e o prepago ás facturas de pedidos de compra. |
| Xestión e contabilidade de proxectos | [565642](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565642) | O rastrexo de axuste non funciona para os diarios de saldo de inicio. |
| Xestión e contabilidade de proxectos | [568814](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568814) | **Dotación de revisión do orzamento do proxecto por período** está dividido en todos os períodos orzamentarios. Cando se envía a asignación, o rexistro non se borra. |
| Xestión e contabilidade de proxectos | [569250](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569250) | As publicacións de traballo en proceso (WIP) no libro maior teñen un importe incorrecto. |
| Xestión e contabilidade de proxectos | [570731](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570371) | A aprobación do diario de horas do proxecto non funciona. |
| Xestión e contabilidade de proxectos | [571391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571391) | O prezo de venda do axuste do proxecto non se actualiza cos custos indirectos cando non se marca o límite de financiamento. |
| Xestión e contabilidade de proxectos | [575831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575831) | Non se pode crear un requisito de artigo cando se factura a cabeceira da táboa de vendas e se finaliza a orde de compra de apoio para as liñas existentes. |
| Xestión e contabilidade de proxectos | [578036](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578036) | O importe de retención dunha regra de facturación que teña un fito para un proxecto diferente non se publica no ID do proxecto correspondente que se seleccionou para o fito. Pola contra, publícase co primeiro proxecto. |
| Xestión e contabilidade de proxectos | [578327](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578327) | Cando selecciones **Conxunto de dimensións financeiras** nunha proposta de factura, prodúcese o seguinte erro: "Non se pode emitir o obxecto do tipo "Dinámica.AX .Application.FormIntControl' para escribir 'Dinámica.AX .Application.FormStringControl'." |
| Xestión e contabilidade de proxectos | [581167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581167) | O **Factura do proxecto** informe salta liñas. |
| Xestión e contabilidade de proxectos | [581489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581489) | Prodúcese un erro ao calcular o control de custos dun proxecto de investimento. |
| Xestión e contabilidade de proxectos | [590357](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590357) | O **ProxTable:: InitFromCustTable - canDeletePostalAddress** método provoca un problema de rendemento. |
| Xestión e contabilidade de proxectos | [592493](https://fix.lcs.dynamics.com/Issue/Details/?bugId=592493) | A mensaxe de erro debería ser máis clara que "Erro inesperado". |
| Xestión e contabilidade de proxectos | [598810](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598810) | O traballo por lotes de publicación de facturas do proxecto procesa e publica a proposta de factura aínda que non se xerasen as liñas de factura. |
| Xestión e contabilidade de proxectos | [574282](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574282) | Prodúcese un problema de redondeo cando se desactiva a clave de configuración da licenza do sector público. Xérase un custo ou prezo de venda incorrecto nas horas da folla de horas para contratos que teñen varias fontes fundacionais. |
| Xestión e contabilidade de proxectos | [577598](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577598) | O prezo de venda do proxecto nunha orde de compra do proxecto facturado calcúlase incorrectamente cando o modelo de prezo de venda **Ratio de cotización**. |
| Xestión e contabilidade de proxectos | [580784](https://fix.lcs.dynamics.com/Issue/Details/?bugId=580784) | O sistema non considera os días activos intermedios cando calcula a taxa de traballo efectiva dun empregado. |
| Xestión e contabilidade de proxectos | [584054](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584054) | Prodúcese un erro de publicación na folla de horas entre empresas debido ao seguinte erro de validación: "Ningún socio comercial está configurado para a persoa xurídica". |
| Xestión e contabilidade de proxectos | [586303](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586303) | A descrición dunha orde de compra que ten unha categoría de gasto non se recupera na lista de transaccións do proxecto publicada. |
| Xestión e contabilidade de proxectos | [590349](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590349) | Hai unha conversión incorrecta nos diarios de artigos que se publican nun proxecto. |
| Xestión e contabilidade de proxectos | [557294](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557294) | Podes confirmar unha orde de compra aínda que se supere o límite de financiamento. |
| Xestión e contabilidade de proxectos | [574162](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574162) | O **Corrección/Cancelar factura** a sección dunha factura de texto libre desaparece cando se selecciona un ID de proxecto. |
| Xestión e contabilidade de proxectos | [575425](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575425) | Hai problemas de rendemento cando se publica unha proposta de factura dun proxecto desde un pedido de venda do proxecto que inclúe un artigo en existencia. |
| Xestión e contabilidade de proxectos | [575939](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575939) | Non se poden publicar as facturas de compra do proxecto porque se produce o seguinte erro: "Chamouse incorrectamente á función AccDistProcessorProjectExtension.createForProjectRevenueLine". |
| Xestión e contabilidade de proxectos | [578970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578970) | Actualización para a creación de traballos por lotes de estimación do proxecto para soportar a execución de varias subtarefas. |
| Xestión e contabilidade de proxectos | [584519](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584519) | Non se pode actualizar o estado dunha folla de horas **Borrador** cando o fluxo de traballo está atrapado nun **Cancelado** estado. |
| Xestión e contabilidade de proxectos | [584757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584757) | Os importes de retención non se calculan na proposta de factura da nota de crédito se existen varias liñas. |
| Xestión e contabilidade de proxectos | [586034](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586034) | Cando tentas cambiar o importe dunha factura xerada a partir dunha orde de compra, prodúcese o seguinte erro: "As transaccións do comprobante non se equilibran segundo XX/XX/XXXX. (divisa de contabilidade: 0,00 - divisa de informes: 0,01)". |
| Xestión e contabilidade de proxectos | [588714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588714) | Hai un problema de rendemento cando unha proposta de factura de proxecto se publica en modo por lotes, debido á unión con **Entrada da conta xeral do xornal**. |
| Xestión e contabilidade de proxectos | [588851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588851) | Hai problemas de rendemento cando se publica unha folla de horas. |
| Xestión e contabilidade de proxectos | [590535](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590535) | A xerarquía de estimacións de custos da estrutura de desglose do traballo non se aliña correctamente despois de que todas as tarefas se expandan ou despois de que unha única tarefa se expanda manualmente. |
| Xestión e contabilidade de proxectos | [593663](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593663) | O modelo de Excel de cotización do proxecto non se pode engadir ao **Abrir en Excel** menú. |
| Xestión e contabilidade de proxectos | [596669](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596669) | O número exento de impostos para unha persoa xurídica non está incluído na factura do proxecto impresa. |
| Xestión e contabilidade de proxectos | [597563](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597563) | Non se actualizan datos financeiros no erro da unidade de inventario cando se axusta un proxecto en relación ás liñas de crédito. |
| Xestión e contabilidade de proxectos | [598109](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598109) | Despois de aplicar KB 461935, non pode publicar estimacións se cambia a secuencias numéricas continuas. |
| Xestión e contabilidade de proxectos | [598688](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598688) | **TimeEntryDataManager** provoca a aplicación móbil da folla de horas do proxecto para Android para deixar de responder. |
| Xestión e contabilidade de proxectos | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | O valor WIP invertido dunha contabilización de factura difire do valor WIP publicado orixinalmente da entrada de hora. |
| Xestión e contabilidade de proxectos | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Nos casos de retención aplicada, as transaccións dun vale non se equilibran cando se contabilizan os ingresos facturados dun proxecto. |
| Xestión e contabilidade de proxectos | [603320](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603320) | Cando o **Mellora do rendemento da programación de recursos do proxecto** función está activada, os valores decimais están redondeados incorrectamente pola dispoñibilidade e capacidade dos recursos. |
| Xestión e contabilidade de proxectos | [607324](https://fix.lcs.dynamics.com/Issue/Details/?bugId=607324) | Cando o **Crea estimacións do proxecto usando varias tarefas por lotes** función está activada, a creación de estimacións nun lote que ten varias subtarefas só funciona para o período actual. |
| Viaxes e gasto | [551911](https://fix.lcs.dynamics.com/Issue/Details/?bugId=551911) | Ignorase unha política de solicitude de viaxe e apróbase o fluxo de traballo sen erros. |
| Viaxes e gasto | [563752](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563752) | <p>A aplicación Mobile Expense non garda a seguinte información na liña de gasto:</p><ul><li>ID do proxecto</li><li>Se o gasto é facturable</li><li>O número da actividade</li></ul> |
| Viaxes e gasto | [569458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569458) | O **Adxuntos recibos** campo está configurado en **Si** aínda que non se xunte ningún recibo á liña de gasto. |
| Viaxes e gasto | [571334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571334) | Prodúcese un erro ao cambiar a categoría de gasto a **Persoal**. |
| Viaxes e gasto | [572783](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572783) | Non podes anexar un recibo e editar o gasto dos pais despois de que unha transacción con tarxeta de crédito se divide nun gasto persoal. |
| Viaxes e gasto | [574252](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574252) | A política de gastos para transaccións entre empresas que teñan un ID de proxecto non funciona correctamente. |
| Viaxes e gasto | [574489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574489) | Falta a información da data publicada para os informes de gastos publicados. |
| Viaxes e gasto | [574504](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574504) | Hai problemas cos métodos de pago na aplicación móbil Expense. |
| Viaxes e gasto | [584799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584799) | Unha solicitude de viaxe que se crea para un traballador pode utilizarse para o informe de gastos doutro traballador antes da data do delegado. |
| Viaxes e gasto | [586023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586023) | Cando crea un gasto, os cambios nos valores da dimensión financeira non se actualizan correctamente no nivel de distribución contable no **Xestión de gastos** espazo de traballo. |
| Viaxes e gasto | [586081](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586081) | O estado de aprobación da liña de gasto principal non está sincronizado co estado de aprobación do fluxo de traballo da liña detallada. |
| Viaxes e gasto | [590544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590544) | Prodúcese un erro se publica un informe de gastos e se activa a recuperación de impostos. |
| Viaxes e gasto | [564851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564851) | Un delegado non pode eliminar os documentos de gastos dun empregado cesado. |
| Viaxes e gasto | [587306](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587306) | A eliminación dunha liña de gasto leva máis tempo do esperado e afecta o rendemento. |
| Viaxes e gasto | [600455](https://fix.lcs.dynamics.com/Issue/Details/?bugId=600455) | **TrvExpTrans** provoca un orfo **Impostos non comprometidos** gravar, porque só **SourceDocumentLine** está eliminado. |
| Viaxes e gasto | [609918](https://fix.lcs.dynamics.com/Issue/Details/?bugId=609918) | **ReleaseUpdateDB72_Expense.updateTrvExpTransProjTransId()** non honra **trvExpTrans.ReferenceDataAreaId** para crear a nova secuencia numérica. |

## <a name="regulatory-updates"></a>Actualizacións normativas

Para obter información acerca das actualizacións regulamentarias para as aplicacións Finance and Operations, consulte [Actualizacións normativas](/dynamics365/finance/localizations/regulatory-updates). Tamén podes iniciar sesión en Microsoft Dynamics Lifecycle Services (LCS) e use a ferramenta de busca de problemas para ver as actualizacións regulamentarias previstas. A busca de problemas permíteche buscar por país ou rexión, tipo de función e versión.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
