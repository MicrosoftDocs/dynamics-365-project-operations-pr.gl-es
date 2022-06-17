---
title: Novidades de novembro de 2021 - Project Operations para situacións baseadas en recursos/sen fornecemento
description: Este artigo ofrece información sobre as actualizacións de calidade dispoñibles na versión de novembro de 2021 de Project Operations para escenarios baseados en recursos ou non almacenados.
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d5b58965f728321cc30d4e476b0dacf621fdec71
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932892"
---
# <a name="whats-new-november-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades de novembro de 2021 - Project Operations para situacións baseadas en recursos/sen fornecemento

*Aplícase a: Project Operations para situacións baseadas en recursos/sen fornecemento*

Este artigo aplícase aos seguintes compoñentes e versións de Microsoft Dynamics 365 Project Operations:

- Operacións do proxecto en a Dataverse versión do entorno 4.26.0.145, 4.26.0.148, 4.26.0.150, 4.26.0.155
- Xestión de proxectos e contabilidade nun entorno Dynamics 365 Finance versión 10.0.22

## <a name="features-included-in-this-release"></a>Funcionalidades incluídas nesta versión

As seguintes funcionalidades están incluídas nesta versión:

- As interfaces de programación de aplicacións (API) de programación de proxectos agora admiten a capacidade de crear e eliminar depósitos de proxectos.

## <a name="project-operations-dual-write-maps-updates"></a>Actualizacións de mapas de escrita dual en Project Operations

Non hai actualizacións para mapas de escrita dual de Project Operations nesta versión. Para obter unha lista actual e versións dos mapas de escrita dual de Project Operations, consulte [Versións de mapa de escrita dual de Project Operations](/dynamics365/project-operations/environment/resource-dual-write-maps).

Executa sempre a versión máis recente do mapa no teu entorno e activa todos os mapas de táboas relacionados mentres actualizas as operacións do teu proxecto Dataverse solución e versión de solución financeira. Algunhas funcións e capacidades poden non funcionar correctamente se a última versión do mapa non está activada. Pode ver a versión activa do mapa na columna **Versión** columna na páxina **Escrita dual**. Para activar unha nova versión do mapa, seleccione **Versións do mapa de táboa**, seleccione a versión máis recente e logo garde a versión seleccionada. Se personalizou un mapa de táboas listo para usar, volve aplicar os cambios. Para obter máis información, consulte [Xestión do ciclo de vida da aplicación](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se atopas algún problema ao iniciar o mapa, siga as instrucións da páxina [Faltan columnas da táboa nos mapas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) sección da guía de solución de problemas de escritura dual.

## <a name="quality-updates"></a>Actualizacións de calidade

### <a name="project-operations-in-dataverse"></a>Operacións do proxecto en Dataverse

| Área de funcionalidades | Número de referencia | Actualización de calidade |
| --- | --- | --- |
| Facturación e prezos | 2240080 | O **Termos de pago** o campo non debe estar duplicado na factura pro forma. |
| Facturación e prezos | 2358236 | A corrección da factura debe permitir correccións que teñan liñas de prezo cero. |
| Xestión de recursos | 2410072 | Permitir a configuración dun recurso que está asignado á tarefa como xestor de proxecto. |
| Facturación e prezos | 2430234 | Corrixir un problema de cálculo do rendemento dos custos. |
| Tempo e gasto | 2436978 | Permitir que se introduza o tempo en formato hh:mm. |
| Facturación e prezos | 2448623 | Permitir que as listas de prezos se actualicen despois de asociarse a unha unidade organizativa. |
| Tempo e gasto | 2460396 | Permitir que se elimine unha entrada de tempo limpando a cela. |
| Facturación e prezos | 2467386 | Permitir que se elimine un proxecto que teña unha tarefa, mesmo cando a tarefa estea asociada cunha cotización gañada. |
| Tempo e gasto | 2461744 | O **A miña aprobación fallida** a vista só contén aprobacións de proxectos na vista **Enviado** etapa. |
| Tempo e gasto | 2464082 | Elimina a ligazón das aprobacións do proxecto ao conxunto de aprobación cando coincida cun estado de destino. |
| Tempo e gasto | 2468108 | O traballo de programación non debe establecer a **Procesamento** estado para o conxunto de aprobación. |
| Tempo e gasto | 2471503 | Elimina os conxuntos de aprobación que teñan sete días de antigüidade. |
| Facturación e prezos | 2480687 | A referencia da liña de cotización non debe eliminarse cando se crea un marco de liña de cotización. |

### <a name="project-management-and-accounting-in-finance"></a>Xestión de proxectos e contabilidade en Finanzas

| Área de funcionalidades | Número de referencia | Actualización de calidade |
| --- | --- | --- |
| Xestión e contabilidade de proxectos | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Os importes de provedores retidos nas transaccións de gastos do proxecto non se mostran na lista de transaccións. |
| Xestión e contabilidade de proxectos | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | A factura do provedor interempresas rompe cando se activa a integración da factura do provedor. |
| Xestión e contabilidade de proxectos | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | As condicións de pago das facturas do proxecto non funcionan como se esperaba. |
| Xestión e contabilidade de proxectos | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Cando se libera a retención de provedores, a publicación do comprobante ten liñas adicionais incorrectas. |
| Xestión e contabilidade de proxectos | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Cando se publica o diario de integración de Project Operations, falla porque faltan dimensións para unha conta na que non se publica. |
| Xestión e contabilidade de proxectos | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | O **Proxecto** a pestana non se pode editar nunha factura de provedor pendente cando se lle asigna a categoría de adquisición ao artigo. |
| Xestión e contabilidade de proxectos | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Falta o panel de navegación se non iniciaches sesión en Project Operations Dataverse. |
| Xestión e contabilidade de proxectos | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Cando publicas ingresos dunha factura de proxecto nun caso de retención aplicado, prodúcese un problema porque as transaccións do comprobante non se equilibran. |
| Xestión e contabilidade de proxectos | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | A creación dunha estimación despois de publicar unha proposta de factura bloquea as liñas de corrección da importación. |
| Xestión e contabilidade de proxectos | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Non debería ser posible a modificación dun rexistro de fito totalmente facturado. |
| Viaxes e gasto | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Todos os informes de gastos son visibles cando buscas unha categoría na aplicación móbil Expense. |
| Viaxes e gasto | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Os importes incorrectos en transaccións de provedores e transaccións de impostos sobre vendas publícanse a partir dun gasto que se crea a partir dunha transacción con tarxeta de crédito. |
| Viaxes e gasto | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Prodúcese un aviso irrelevante ao actualizar o **Informe de gastos** páxina. |
| Viaxes e gasto | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | O aprobador provisional incorrecto úsase cando elimina un aprobador interino e despois volve enviar un informe de gastos a través do fluxo de traballo. |
| Viaxes e gasto | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Prodúcese un erro de publicación relacionado coa configuración da quilometraxe. |
