---
title: Novidades e cambios en Project Operations de outubro 2021 para situacións baseadas en produción/con fornecemento
description: Este artigo ofrece información sobre as actualizacións de calidade que están dispoñibles na versión de outubro de 2021 de Project Operations para situacións baseadas en produción/con fornecemento.
author: andchoi
ms.date: 11/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: aa36199c9e7b0a70307c5e9fb163d82554f6be16
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029941"
---
# <a name="whats-new-or-changed-in-project-operations-october-2021-for-stockedproduction-based-scenarios"></a>Novidades e cambios en Project Operations de outubro 2021 para situacións baseadas en produción/con fornecemento

_**Aplícase a:** Project Operations para situacións baseadas en produción/con fornecemento_

Este artigo aplícase aos seguintes compoñentes e versións de Microsoft Dynamics 365 Project Operations:

- Xestión e contabilidade de proxectos nun ambiente de aplicacións de Dynamics 365 Finance versión 10.0.22
 
## <a name="quality-updates"></a>Actualizacións de calidade

| Área de funcionalidades | Número de referencia | Actualización de calidade |
|--------------|------------------|----------------|
| Xestión e contabilidade de proxectos | [557017](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557017) | O traballo en proceso (WIP) do proxecto e os importes dos ingresos acumulados non se reverten correctamente cando se publica unha factura de cliente entre empresas. |
| Xestión e contabilidade de proxectos | [558232](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558232) | A funcionalidade **Evitar o peche do proxecto se hai transaccións abertas** non funciona. |
| Xestión e contabilidade de proxectos | [559271](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559271) | A clasificación de facturación nunha factura de texto libre non enche automaticamente as dimensións dos proxectos cando esta función está activada. |
| Xestión e contabilidade de proxectos | [574013](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574013) | En situacións non entre empresas, os importes de WIP e ingresos acumulados non se reverten correctamente cando se contabiliza unha factura de proxecto. |
| Xestión e contabilidade de proxectos | [577857](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577857) | Os valores de débito e crédito cámbianse cando o complemento Microsoft Excel se usa co diario de gastos do proxecto e o campo **Tipo de conta compensada** configurado como **Proxecto**. |
| Xestión e contabilidade de proxectos | [577972](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577972) | O importe que se contabiliza nas transaccións do proxecto está sobreestimado nun pedido de compra do proxecto que inclúe artigos en existencias e que ten importes fiscais non deducibles cando **Imposto de uso** está marcado. |
| Xestión e contabilidade de proxectos | [581216](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581216) | O sistema divide o importe entre os informes de perdas e ganancias do proxecto e os informes de WIP do proxecto. |
| Xestión e contabilidade de proxectos | [582065](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582065) | O inventario dispoñible é incorrecto despois de que se axuste un requisito de artigo devolto parcialmente. |
| Xestión e contabilidade de proxectos | [582682](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582682) | Os nomes dos recursos duplícanse en Project Operations cando se editan en Microsoft Project. |
| Xestión e contabilidade de proxectos | [583873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583873) | Os informes de gastos entre empresas que teñen custos de facturas de fornecedores pendentes de contas pendentes de pago entre empresas contabilízanse primeiro no tipo **Custo de WIP do proxecto**. Non obstante, durante o procesamento, os custos relacionados coa estimación contabilízanse no tipo **Custo do proxecto** en lugar do tipo esperado **Custo entre empresas**. |
| Xestión e contabilidade de proxectos | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Non se mostran os resultados de retención de fornecedores nas transaccións de gastos do proxecto. |
| Xestión e contabilidade de proxectos | [587453](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587453) | A folla de control horario debe redondear o importe da transacción na moeda da transacción ata un número especificado de cifras decimais en todas as distribucións contables e as entradas de asignación do diario xeral. |
| Xestión e contabilidade de proxectos | [589409](https://fix.lcs.dynamics.com/Issue/Details/?bugId=589409) | As cantidades de requisitos dos elementos do proxecto actualízanse automaticamente cando se confirman os pedidos planificados. |
| Xestión e contabilidade de proxectos | [590206](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590206) | O número do comprobante, o saldo do fornecedor do tipo de transacción e o número de conta non se poden reverter na factura de prepago dun pedido de compra. |
| Xestión e contabilidade de proxectos | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | A factura do fornecedor entre empresas rompe cando se activa a integración da factura do fornecedor. |
| Xestión e contabilidade de proxectos | [593335](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593335) | Cando se crea un diario de gastos do proxecto, o importe do custo móstrase no campo **Crédito**. |
| Xestión e contabilidade de proxectos | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | As condicións de pagamento das facturas do proxecto non funcionan como se esperaba. |
| Xestión e contabilidade de proxectos | [593565](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593565) | Os vales de follas de control horario poden reutilizarse cando a secuencia numérica está configurada como continua. |
| Xestión e contabilidade de proxectos | [593652](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593652) | FRANCIA: A lóxica **Importe de retención manual** non coincide coa lóxica **Cantidade de retención automática** na proposta de factura do contrato do proxecto. |
| Xestión e contabilidade de proxectos | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Cando se libera a retención de fornecedores, a contabilización do vale ten liñas adicionais incorrectas. |
| Xestión e contabilidade de proxectos | [596650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596650) | Cando se cambia o campo **Data da factura** na páxina **Crear proposta de factura**, pode ocorrer o seguinte erro: "A referencia de obxecto non está definida nunha instancia dun obxecto". |
| Xestión e contabilidade de proxectos | [597679](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597679) | Prodúcese un erro ao tentar aprobar unha folla de control horario desde o fluxo de traballo **TSLine** e hai unha política de follas de control horario para o sábado e o domingo. |
| Xestión e contabilidade de proxectos | [597801](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597801) | Exclúese o tipo de partida do proxecto de saldo inicial **Resumos das transaccións da proposta de factura** cando se calcule o total da factura da proposta de factura. |
| Xestión e contabilidade de proxectos | [597886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597886) | Se o custo de consumo dun pedido de produción do proxecto é 0 (cero), prodúcese o seguinte erro ao tentar estimar: "Intentouse dividir por cero". |
| Xestión e contabilidade de proxectos | [598706](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598706) | A aplicación Project Timesheet Mobile para Android deixa de responder. O tema está relacionado con **TimeEntryDataManager ArgumentNullException**. |
| Xestión e contabilidade de proxectos | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | O diario de integración de Project Operations falla ao contabilizalo porque faltan dimensións para unha conta. Non obstante, a conta á que lle faltan as dimensións non é a conta na que está a contabilizar. |
| Xestión e contabilidade de proxectos | [598929](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598929) | O filtro **ToDate** nas buscas non se borra cando se elimina da caixa de diálogo **Seleccionar** na páxina **Contabilizar custo**. |
| Xestión e contabilidade de proxectos | [599757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=599757) | **Restablecer toda a distribución** falla e mostra un erro para as follas de control horario que se crean para un proxecto de tipo **Só tempo**. |
| Xestión e contabilidade de proxectos | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | O separador **Proxecto** non é editable nunha factura de fornecedor pendente cando a categoría de adquisición se atribúe ao elemento. |
| Xestión e contabilidade de proxectos | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Falta o panel de navegación se non iniciou sesión en Project Operations Dataverse. |
| Xestión e contabilidade de proxectos | [546467](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546467) | Para as transaccións de axuste de proxectos entre empresas, hai problemas na empresa de destino. |
| Xestión e contabilidade de proxectos | [563579](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563579) | Os custos comprometidos para proxecto calculan a cantidade e o prezo de custo incorrectos se o pedido de compra foi procesado mediante o **Proceso de fin de ano do pedido de compra** no libro maior. |
| Xestión e contabilidade de proxectos | [581454](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581454) | Cando un pedido de produción de proxecto que ten pedidos de calidade se informa como rematado, ocorre o seguinte erro: "Non hai transacción virtual marcada con transacción de inventario". |
| Xestión e contabilidade de proxectos | [596408](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596408) | Cando se publica unha factura de contas pendentes de pago relacionada co proxecto, prodúcese o seguinte erro: "O texto enumerado Proxecto - custo - elemento non existe". |
| Xestión e contabilidade de proxectos | [597237](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597237) | Os custos indirectos duplícanse cando se acumulan ingresos manualmente. |
| Xestión e contabilidade de proxectos | [601198](https://fix.lcs.dynamics.com/Issue/Details/?bugId=601198) | A contabilización de ingresos acumulados e WIP non produce transaccións. |
| Xestión e contabilidade de proxectos | [602095](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602095) | A activación do prezo pendente falla para un elemento de custo estándar cando existe un pedido de compra do proxecto recibida. |
| Xestión e contabilidade de proxectos | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | O valor WIP invertido dunha contabilización de facturas é diferente do valor WIP contabilizado orixinal dunha entrada de tempo. |
| Xestión e contabilidade de proxectos | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Existe un problema de contabilización dos ingresos facturados polo proxecto nos casos de retencións aplicadas nos que as transaccións nos vales non cadran. |
| Xestión e contabilidade de proxectos | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | A creación dunha estimación despois de publicar unha proposta de factura bloquea a importación de liñas de corrección en Project Operations. |
| Xestión e contabilidade de proxectos | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Non debería ser posible a modificación dun rexistro de fito totalmente facturado. |
| Xestión e contabilidade de proxectos | [611389](https://fix.lcs.dynamics.com/Issue/Details/?bugId=611389) | Cando se utilizan cargos automáticos, non se pode publicar a factura do cliente entre empresas dunha folla de control horario e móstrase unha mensaxe de erro. |
| Xestión e contabilidade de proxectos | [612991](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612991) | O enderezo dun subproxecto non está actualizado correctamente. |
| Xestión e contabilidade de proxectos | [613418](https://fix.lcs.dynamics.com/Issue/Details/?bugId=613418) | O prezo de custo dos requisitos dos artigos actualízase co prezo de compra dos pedidos de compra consolidados. |
| Xestión e contabilidade de proxectos | [614145](https://fix.lcs.dynamics.com/Issue/Details/?bugId=614145) | O custo publicado non é correcto despois de que se actualice o prezo de compra e se active o parámetro **Activar a xestión de cambios**. |
| Viaxes e gasto | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Todos os gastos do usuario se poden ver ao buscar unha categoría na aplicación móbil Expense. |
| Viaxes e gasto | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Os importes incorrectos das transaccións do fornecedor e do imposto sobre as vendas contabilízanse a partir dun gasto que se creou a partir dunha transacción con tarxeta de crédito. |
| Viaxes e gasto | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Móstrase unha mensaxe de aviso irrelevante ao actualizar as páxinas de informe de gastos. |
| Viaxes e gasto | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | O responsable de aprobacións provisional incorrecto úsase cando elimina o responsable de aprobacións provisional e despois volve enviar a través do fluxo de traballo. |
| Viaxes e gasto | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Prodúcese un erro de contabilización que está relacionado coa configuración da quilometraxe. |
| Viaxes e gasto | [620773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620773) | A distribución non actualiza a persoa xurídica cando se engade de novo unha transacción non anexa ao informe de gastos nun gasto entre empresas. |

### <a name="regulatory-updates"></a>Actualizacións normativas

Para obter información sobre actualizacións normativas para aplicacións de finanzas e operacións, vexa [Actualizacións normativas](/dynamics365/finance/localizations/regulatory-updates). Tamén pode iniciar sesión en Microsoft Dynamics Lifecycle Services (LCS) e usar a ferramenta de busca de problemas para ver as actualizacións regulamentarias previstas. A busca de problemas permítelle buscar por país ou rexión, tipo de funcionalidade e lanzamento.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
