---
title: Novidades ou cambios en Project Operations, xullo de 2021, para situacións baseadas en produción/con fornecemento
description: Este artigo ofrece información sobre as actualizacións de calidade dispoñibles na versión de xullo de 2021 de Project Operations para escenarios abastecidos ou baseados na produción.
author: andchoi
ms.date: 07/01/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: df9a68c5a12e6aec140867eb1db3d88279c05795
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933628"
---
# <a name="whats-new-or-changed-in-project-operations-july-2021-for-stockedproduction-based-scenarios"></a>Novidades ou cambios en Project Operations, xullo de 2021, para situacións baseadas en produción/con fornecemento

_**Aplícase a:** Project Operations para situacións baseadas en produción/con fornecemento_

Este artigo aplícase ao seguinte Dynamics 365 Project Operations compoñentes e versións:

- Xestión de proxectos e contabilidade no entorno Dynamics 365 Finance versión 10.0.20
 
### <a name="quality-updates"></a>Actualizacións de calidade
                                                                                                                                                                                  
| Área de funcionalidades                      | Número de referencia| Actualización de calidade                                                                                                                                                                          |
|-----------------------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Xestión e contabilidade de proxectos | [485394](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485394) | Os rexistros de compromiso de custos dunha solicitude de compra bórranse en canto se libera o pedido de compra da emisión da solicitude de compra.                                                                           |
| Xestión e contabilidade de proxectos | [529602](https://fix.lcs.dynamics.com/Issue/Details/?bugId=529602) | A validación do orzamento prodúcese dúas veces nunha solicitude de compra. Esta duplicación significa que non se pode pechar a solicitude e non se crea o pedido de compra correspondente.                                                                                                                        |
| Xestión e contabilidade de proxectos | [539439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539439) | A regra de facturación **Porcentaxe para facturar sobre** non se puido completar a regra de facturación por mor dun problema de redondeo.                                                                              |
| Xestión e contabilidade de proxectos | [540023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540023) | Cando axusta a transacción e a porcentaxe ten decimais, o custo e o prezo de venda non se axustan correctamente.                                      |
| Xestión e contabilidade de proxectos | [540927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540927) | O explorador de fontes de contabilidade mostra horas para unha única liña de folla de tempo para varias liñas de folla de tempo con actividades diferentes.                                      |
| Xestión e contabilidade de proxectos | [541471](https://fix.lcs.dynamics.com/Issue/Details/?bugId=541471) | As vistas gardadas e a personalización dos detalles da liña de folla de tempo fan que o sistema abra sempre os detalles da primeira folla de tempo da lista cando intenta abrir unha folla de tempo.  |
| Xestión e contabilidade de proxectos | [548677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548677) | O nodo raíz do proxecto desaparece e os rexistros da estrutura de subdivisión do traballo elimínanse despois da importación.                                                                                             |
| Xestión e contabilidade de proxectos | [548999](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548999) | Cando os elementos se reciben e se emiten parcialmente desde o requisito do elemento, o sistema actualiza o saldo de consumo orzamentario incorrecto. |
| Xestión e contabilidade de proxectos | [550959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550959) | Os pedidos de compra de retención de proxectos non mostran os totais correctamente no panel **Totais** ou a grade **Factura pendente**.                                                                  |
| Xestión e contabilidade de proxectos | [554593](https://fix.lcs.dynamics.com/Issue/Details/?bugId=554593) | Ao pechar o inventario, os axustes dos custos das partidas do proxecto contabilízanse na conta de saldo en lugar da conta de resultados.                                                            |
| Xestión e contabilidade de proxectos | [557394](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557394) | Un vale de transacción publicado por un proxecto e un vale estimado utilizan USD como divisa de contabilidade pero o importe mostra o que sería o equivalente en CAD.              |
| Xestión e contabilidade de proxectos | [560140](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560140) | Os custos comprometidos cun requisito de artigo e pedido de compra son erróneos no proceso de facturación da orde de compra coa recepción parcial do produto e a facturación parcial.       |
| Xestión e contabilidade de proxectos | [560567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560567) | O axuste do proxecto non actualiza o importe das vendas correctamente con custos indirectos.                                                                                    |
| Xestión e contabilidade de proxectos | [561137](https://fix.lcs.dynamics.com/Issue/Details/?bugId=561137) | Na táboa **Folla de tempo** falta unha relación definida coa vista **Traballador/Recurso**.                                                                                   |
| Xestión e contabilidade de proxectos | [563330](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563330) | Non se puido encher o campo **Número de actividade** cando o selecciona no menú despregable para unha folla de tempo entre empresas.                                                                 |
| Xestión e contabilidade de proxectos | [563840](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563840) | Non pode engadir un campo personalizado **Propósito** ou **Descrición da actividade** ás seguintes páxinas: **Transacción contabilizada do proxecto**, **Creación de proposta de factura** ou **Proposta de factura**.  |
| Xestión e contabilidade de proxectos | [566348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566348) | Proporciónase un control da data de entrega incorrecto cando crea requisitos de elementos mediante a xestión de datos (**ProjSalesItemRequirementEntity**).                                              |
| Xestión e contabilidade de proxectos | [566544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566544) | Cando selecciona un ID de contrato de proxecto en Finance, o ambiente integrado de Project Operations abre a páxina para crear un novo rexistro en lugar de abrir o contrato de proxecto existente.                                                                                                                 |
| Xestión e contabilidade de proxectos | [567300](https://fix.lcs.dynamics.com/Issue/Details/?bugId=567300) |  A etiqueta "@SYS4083080" ("Non se pode atopar un rexistro único de traballador correspondente aos valores introducidos") non está traducida ao danés.                                |
| Xestión e contabilidade de proxectos | [569901](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569901) | O campo **Grupo do imposto sobre as vendas** non se pode editar nunha proposta de factura.                                                                               |
| Xestión e contabilidade de proxectos | [557049](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557049) | O custo comprometido esaxérase cos importes fiscais non deducibles.                                                                                                    |
| Xestión e contabilidade de proxectos | [565080](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565080) | Publicar unha folla de tempo entre empresas con varios proxectos e diferentes dimensións financeiras xera valores inesperados no libro maior.                             |
| Xestión e contabilidade de proxectos | [567962](https://fix.lcs.dynamics.com/Issue/Details/?bugId=567962) | As liñas de proposta de factura están duplicadas debido a varias instancias do proceso periódico, **Importar desde transición** executándose ao mesmo tempo.                                      |
| Xestión e contabilidade de proxectos | [571339](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571339) | Produciuse un erro na contabilización da proposta de factura da nota de crédito, polo que as transaccións do vale non se saldan.    |
| Xestión e contabilidade de proxectos | [573567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573567) | Os custos comprometidos no proxecto convértense en incorrectos despois de liberar as facturas pendentes en espera.                                                                             |
| Xestión e contabilidade de proxectos | [573886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573886) | Non pode crear unha nota de crédito para un pedido de venda do proxecto cando o imposto está nunha moeda diferente á moeda da empresa.                                      |
| Xestión e contabilidade de proxectos | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | A eliminación dun contrato tamén elimina o enderezo asociado ao cliente.                                                                                     |
| Xestión e contabilidade de proxectos | [585811](https://fix.lcs.dynamics.com/Issue/Details/?bugId=585811) | Non se pode contabilizar unha proposta de factura que resulte dunha corrección negativa da transacción de tempo.                                                                    |
| Viaxes e gasto                  | [532075](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532075) | O imposto calcúlase de forma diferente nos informes de gastos.                                                                                                                  |
| Viaxes e gasto                  | [546450](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546450) | A actualización da versión **DB72_Expense.updateTrvExpTransProjTransId ()** non permite a **trvExpTrans.ReferenceDataAreaId** crear a nova secuencia numérica.                    |
| Viaxes e gasto                  | [568805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568805) | A cantidade arquivada non aparece co campo obrigatorio.                                                                                                             |
| Viaxes e gasto                  | [568831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568831) | Melloras no rendemento de anexar un gasto ao informe de gastos mediante a interface de usuario de novo deseño de gastos.                                                            |
| Viaxes e gasto                  | [570790](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570790) | Pode eliminar os informes de gastos contabilizados.                                                                                           |
| Viaxes e gasto                  | [571317](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571317) | A mensaxe de política de gastos móstrase varias veces.                                                                                                       |
| Viaxes e gasto                  | [573969](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573969) | O campo **Método de pagamento** está incluído no panel **Novo gasto**.                                                                                                      |
| Viaxes e gasto                  | [523557](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523557) | A ferramenta **Restablecer o estado do documento de gastos** debería restablecer o estado do informe de gastos a **Borrador** se non se atopou o fluxo de traballo. 

### <a name="regulatory-updates"></a>Actualizacións normativas
Para obter información acerca das actualizacións regulamentarias para as aplicacións Finance and Operations, consulte [Actualizacións normativas](/dynamics365/finance/localizations/regulatory-updates). Tamén pode iniciar sesión en Lifecycle Services (LCS) e ver as actualizacións regulamentarias previstas usando a ferramenta de busca de problemas. A busca de problemas permítelle buscar por país, tipo de funcionalidade e lanzamento.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
