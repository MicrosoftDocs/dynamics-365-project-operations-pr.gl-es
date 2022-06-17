---
title: Novidades ou cambios en Project Operations, outubro de 2021 para escenarios abastecidos ou baseados na produción
description: Este artigo ofrece información sobre as actualizacións de calidade que están dispoñibles na versión de outubro de 2021 de Project Operations para escenarios abastecidos ou baseados na produción.
author: andchoi
ms.date: 11/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: ba88268e74269c774b41396a8b6574e5bab477b9
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933674"
---
# <a name="whats-new-or-changed-in-project-operations-october-2021-for-stockedproduction-based-scenarios"></a>Novidades ou cambios en Project Operations, outubro de 2021 para escenarios abastecidos ou baseados na produción

_**Aplícase a:** Project Operations para situacións baseadas en produción/con fornecemento_

Este artigo aplícase aos seguintes compoñentes e versións de Microsoft Dynamics 365 Project Operations:

- Xestión de proxectos e contabilidade nun entorno Dynamics 365 Finance versión 10.0.22
 
## <a name="quality-updates"></a>Actualizacións de calidade

| Área de funcionalidades | Número de referencia | Actualización de calidade |
|--------------|------------------|----------------|
| Xestión e contabilidade de proxectos | [557017](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557017) | O traballo do proxecto en proceso (WIP) e os importes dos ingresos acumulados non se reverten correctamente cando se publica unha factura de cliente entre empresas. |
| Xestión e contabilidade de proxectos | [558232](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558232) | O **Evitar o peche do proxecto se hai transaccións abertas** a funcionalidade non funciona. |
| Xestión e contabilidade de proxectos | [559271](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559271) | A clasificación de facturación nunha factura de texto gratuíto non enche automaticamente as dimensións dos proxectos cando esta función está activada. |
| Xestión e contabilidade de proxectos | [574013](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574013) | En escenarios que non sexan entre empresas, os importes do WIP e dos ingresos acumulados non se inverten correctamente cando se publica a factura do proxecto. |
| Xestión e contabilidade de proxectos | [577857](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577857) | Os valores de débito e crédito cámbianse cando o Microsoft Excel o complemento utilízase co diario de gastos do proxecto e co **Tipo de conta compensada** campo está configurado en **Proxecto**. |
| Xestión e contabilidade de proxectos | [577972](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577972) | O importe que se contabiliza nas transaccións do proxecto está sobreestimado nunha orde de compra do proxecto que inclúe artigos en existencia e que ten importes fiscais non deducibles cando **UseTax** está marcado. |
| Xestión e contabilidade de proxectos | [581216](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581216) | O sistema divide o importe entre os informes de perdas e ganancias do proxecto e os informes de WIP do proxecto. |
| Xestión e contabilidade de proxectos | [582065](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582065) | O inventario dispoñible é incorrecto despois de que se axuste un requisito de artigo devolto parcialmente. |
| Xestión e contabilidade de proxectos | [582682](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582682) | Os nomes dos recursos duplícanse en Project Operations cando se editan en Microsoft Project. |
| Xestión e contabilidade de proxectos | [583873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583873) | Os informes de gastos intercompañías que teñen custos de facturas de provedores pendentes de contas a pagar entre empresas publícanse primeiro no **Custo do proxecto WIP** tipo de publicación. Non obstante, durante o procesamento, os custos relacionados coa estimación publícanse no **Custo do proxecto** tipo de publicación en lugar do esperado **Custo entre empresas** tipo de publicación. |
| Xestión e contabilidade de proxectos | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Non se mostran os resultados de retención de provedores nas transaccións de gastos do proxecto. |
| Xestión e contabilidade de proxectos | [587453](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587453) | A folla de horas debe redondear o importe da transacción na moeda da transacción ata un número especificado de cifras decimais en todas as distribucións contables e as entradas xerais de asignación ao diario. |
| Xestión e contabilidade de proxectos | [589409](https://fix.lcs.dynamics.com/Issue/Details/?bugId=589409) | As cantidades de requisitos de elementos do proxecto actualízanse automaticamente cando se confirman os pedidos planificados. |
| Xestión e contabilidade de proxectos | [590206](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590206) | O número do comprobante, o saldo do provedor do tipo de transacción e o número de conta non se poden reverter na factura de prepago dunha orde de compra. |
| Xestión e contabilidade de proxectos | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | A factura do provedor interempresas rompe cando se activa a integración da factura do provedor. |
| Xestión e contabilidade de proxectos | [593335](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593335) | Cando crea un diario de gastos do proxecto, o importe do custo móstrase no **Crédito** campo. |
| Xestión e contabilidade de proxectos | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | As condicións de pago das facturas do proxecto non funcionan como se esperaba. |
| Xestión e contabilidade de proxectos | [593565](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593565) | Os vales de follas de horas poden reutilizarse cando a secuencia numérica se configura como continua. |
| Xestión e contabilidade de proxectos | [593652](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593652) | FRANCIA: O **Importe de retención manual** a lóxica non coincide co **Importe de retención automática** lóxica na proposta de factura do contrato do proxecto. |
| Xestión e contabilidade de proxectos | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Cando se libera a retención de provedores, a publicación do comprobante ten liñas adicionais incorrectas. |
| Xestión e contabilidade de proxectos | [596650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596650) | Cando o **Data da factura** campo no **Crear proposta de factura** cambiase a páxina, pode ocorrer o seguinte erro: "A referencia do obxecto non se estableceu nunha instancia dun obxecto". |
| Xestión e contabilidade de proxectos | [597679](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597679) | Prodúcese un erro ao tentar aprobar unha folla de horas desde o **TSLine** fluxo de traballo e hai unha política de follas de horas para o sábado e o domingo. |
| Xestión e contabilidade de proxectos | [597801](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597801) | Exclúese o tipo de partida do proxecto de saldo inicial **Resumos da transacción da proposta de factura** cando se calcule o total da factura da proposta de factura. |
| Xestión e contabilidade de proxectos | [597886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597886) | Se o custo de consumo dunha orde de produción do proxecto é 0 (cero), prodúcese o seguinte erro ao tentar estimar: "Intento dividir por cero". |
| Xestión e contabilidade de proxectos | [598706](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598706) | A aplicación móbil Project Timesheet para Android deixa de responder. O tema está relacionado con **TimeEntryDataManager ArgumentNullException**. |
| Xestión e contabilidade de proxectos | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | O diario de integración de Project Operations falla cando o publicas, porque a unha conta faltan dimensións. Non obstante, a conta á que lle faltan as dimensións non é a conta na que estás publicando. |
| Xestión e contabilidade de proxectos | [598929](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598929) | O **Ata a data** o filtro nas buscas non se borra cando se elimina do **Seleccione** cadro de diálogo no **Costo de publicación** páxina. |
| Xestión e contabilidade de proxectos | [599757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=599757) | **Restablecer toda a distribución** falla e mostra un erro para as follas de horas que se crean para un proxecto do **Só tempo** tipo. |
| Xestión e contabilidade de proxectos | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | O **Proxecto** a pestana non se pode editar nunha factura de provedor pendente cando se lle asigna a categoría de adquisición ao artigo. |
| Xestión e contabilidade de proxectos | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Falta o panel de navegación se non iniciaches sesión en Project Operations Dataverse. |
| Xestión e contabilidade de proxectos | [546467](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546467) | Para as transaccións de axuste de proxectos entre empresas, hai problemas na empresa de destino. |
| Xestión e contabilidade de proxectos | [563579](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563579) | Os custos comprometidos para un proxecto calculan a cantidade e o prezo de custo incorrectos se a orde de compra foi procesada por **Proceso de fin de ano da orde de compra** en Libro maior. |
| Xestión e contabilidade de proxectos | [581454](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581454) | Cando un pedido de produción de proxecto que ten pedidos de calidade se informa como rematado, ocorre o seguinte erro: "Non hai transacción virtual marcada con transacción de inventario". |
| Xestión e contabilidade de proxectos | [596408](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596408) | Cando se publica unha factura de contas a pagar relacionada co proxecto, prodúcese o seguinte erro: "O texto enumerado Proxecto - custo - artigo non existe". |
| Xestión e contabilidade de proxectos | [597237](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597237) | Os custos indirectos duplícanse cando acumulas ingresos manualmente. |
| Xestión e contabilidade de proxectos | [601198](https://fix.lcs.dynamics.com/Issue/Details/?bugId=601198) | A publicación de ingresos acumulados e WIP non produce transaccións. |
| Xestión e contabilidade de proxectos | [602095](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602095) | A activación do prezo pendente falla para unha partida de custo estándar cando existe unha orde de compra do proxecto recibida. |
| Xestión e contabilidade de proxectos | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | O valor WIP invertido dunha contabilización de factura difire do valor WIP publicado orixinal dunha entrada de tempo. |
| Xestión e contabilidade de proxectos | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Hai un problema de contabilización dos ingresos facturados do proxecto nos casos de retención aplicada nos que as transaccións do comprobante non se equilibran. |
| Xestión e contabilidade de proxectos | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | A creación dunha estimación despois de publicar unha proposta de factura bloquea a importación de liñas de corrección en Operacións do proxecto. |
| Xestión e contabilidade de proxectos | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Non debería ser posible a modificación dun rexistro de fito totalmente facturado. |
| Xestión e contabilidade de proxectos | [611389](https://fix.lcs.dynamics.com/Issue/Details/?bugId=611389) | Cando se utilizan cargos automáticos, non se pode publicar a factura do cliente entre empresas dunha folla de horas e móstrase unha mensaxe de erro. |
| Xestión e contabilidade de proxectos | [612991](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612991) | O enderezo dun subproxecto non está actualizado correctamente. |
| Xestión e contabilidade de proxectos | [613418](https://fix.lcs.dynamics.com/Issue/Details/?bugId=613418) | O prezo de custo dos requisitos dos artigos actualízase co prezo de compra dos pedidos de compra consolidados. |
| Xestión e contabilidade de proxectos | [614145](https://fix.lcs.dynamics.com/Issue/Details/?bugId=614145) | O custo publicado non é correcto despois de que se actualice o prezo de compra e o parámetro **Activar a xestión de cambios** está activado. |
| Viaxes e gasto | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Pódense ver todos os gastos dos usuarios cando busca unha categoría na aplicación móbil Expense. |
| Viaxes e gasto | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Os importes incorrectos en transaccións de provedores e transaccións de impostos sobre vendas publícanse a partir dun gasto que se creou a partir dunha transacción con tarxeta de crédito. |
| Viaxes e gasto | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Unha mensaxe de aviso irrelevante móstrase cando actualiza as páxinas do informe de gastos. |
| Viaxes e gasto | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | O aprobador provisional incorrecto úsase cando elimina un aprobador interino e despois volve enviar a través do fluxo de traballo. |
| Viaxes e gasto | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Prodúcese un erro de publicación relacionado coa configuración da quilometraxe. |
| Viaxes e gasto | [620773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620773) | A distribución non actualiza a entidade xurídica cando se engade de novo unha transacción non anexa ao informe de gastos sobre un gasto intercompañía. |

### <a name="regulatory-updates"></a>Actualizacións normativas

Para obter información acerca das actualizacións regulamentarias para as aplicacións Finance and Operations, consulte [Actualizacións normativas](/dynamics365/finance/localizations/regulatory-updates). Tamén podes iniciar sesión en Microsoft Dynamics Lifecycle Services (LCS) e use a ferramenta de busca de problemas para ver as actualizacións regulamentarias previstas. A busca de problemas permíteche buscar por país ou rexión, tipo de función e versión.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
