---
title: Novidades de maio de 2021 - Project Operations para situacións baseadas en recursos/sen fornecemento
description: Este tema ofrece información sobre as actualizacións de calidade dispoñibles na versión de maio de 2021 de Project Operations para situacións baseadas en recursos/sen fornecemento.
author: sigitac
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 07ae18faef6acb9d64b889bbfdba89de0c96a453
ms.sourcegitcommit: d48dce64f6c5b16db3250096715c9d9f92a81971
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/20/2021
ms.locfileid: "6083924"
---
# <a name="whats-new-may-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades de maio de 2021 - Project Operations para situacións baseadas en recursos/sen fornecemento

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Este tema aplícase aos seguintes compoñentes e versións de Dynamics 365 Project Operations:

- Project Operations no ambiente de Dynamics 365 Dataverse versión 4.10.0.186
- Xestión e contabilidade de proxectos en ambientes de aplicacións de Finance and Operations versión 10.0.18

## <a name="features-included-in-this-release"></a>Funcionalidades incluídas nesta versión

As seguintes funcionalidades están incluídas nesta versión:

- [Modos de programación](../project-management/scheduling-modes.md): Os xestores de proxectos poden definir se un proxecto debe ser xestionado usando un modo de programación de duración fixa, traballo fixo ou unidades fixas.
- [Configurar a quilometraxe empregando niveis de taxa de quilometraxe](../expense/set-up-mileage.md): Actualice os niveis de taxa de quilometraxe para os informes de gastos dos empregados.

## <a name="project-operations-dual-write-maps-updates"></a>Actualizacións de mapas de escrita dual en Project Operations

A seguinte lista mostra os mapas de escrita dual que foron modificados ou engadidos na versión de Project Operations de maio de 2021.

| Asignación de entidades | Versión actualizada | Comentarios |
| --- | --- | --- |
| Orixe de financiamento do proxecto (msdyn\_projectcontractsplitbillingrules) | 1.0.0.2 | Sincronización das condicións de pagamento do cliente do contrato do proxecto. |
| Proposta de factura de proxecto V2 (facturas) | 1.0.0.3 | Sincronización das condicións de pagamento da factura proforma. |
| Entidade de exportación de liñas de facturas do fornecedor do proxecto de integración de Project Operations (msdyn\_projectvendorinvoicelines) | 1.0.0.1 | Actualizacións de calidade |
| Proxectos V2 (msdyn\_projects) | 1.0.0.2 | Actualizacións de calidade |

Execute sempre a última versión do mapa no seu ambiente e activar todos os mapas de táboa relacionados mentres actualiza a súa solución de Project Operations Dataverse e a versión da solución de aplicacións de Finance and Operations. É posible que certas funcionalidades e capacidades non funcionen correctamente se a última versión do mapa non está activada. Pode ver a versión activa do mapa na columna **Versión** columna na páxina **Escrita dual**. Para activar unha nova versión do mapa, seleccione **Versións do mapa de táboa**, seleccione a versión máis recente e logo garde a versión seleccionada. Se personalizou un mapa de táboa listo para usar, aplique de novo os cambios. Para obter máis información, consulte [Xestión do ciclo de vida da aplicación](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management.md).

Se ten algún problema ao iniciar o mapa, siga as instrucións da sección [Problema de falta de columnas da táboa nos mapas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades.md#missing-table-columns-issue-on-maps) da guía de resolución de problemas de escrita dual.

## <a name="quality-updates"></a>Actualizacións de calidade

### <a name="project-operations-on-dataverse"></a>Project Operations en Dataverse

| **Área de funcionalidades** | **Número de referencia** | **Actualización de calidade** |
| --- | --- | --- |
| Facturación e prezos | 2227635 | Os valores dos campos **Grupo de unidades** e **Unidade** son os predefinidos do produto na grade **Estimacións de material**. |
| Facturación e prezos | 2234127 | O campo **ID de tarefa** campo agora intégrase correctamente nos datos reais do proxecto de Dataverse cando se publica unha factura do fornecedor. |
| Facturación e prezos | 2235564 | Ao gardar a liña de diario garántese que a moeda mostrada na entrada da liña de diario coincida coa moeda predefinida na liña despois de gardar. |
| Facturación e prezos | 2246671 | Converter unha transacción en non imputable durante a facturación inverte o rexistro de vendas sen facturar orixinal e crea un novo rexistro de vendas sen facturar como non imputable. |
| Facturación e prezos | 2264042 | Non se debe bloquear a corrección de facturas válidas se hai un detalle de corrección de facturas que non é válido no ambiente. |
| Facturación e prezos | 2146367 | A asignación de escrita dual de cabeceira de factura do proxecto amplíase para incluír condicións de pagamento. |
|   Xestión de oportunidades | 2086888 | Non engada roles e categorías que estean desactivadas antes de copiar unha oferta a roles e categorías imputables dunha nova oferta copiada. |
|   Xestión de oportunidades | 2234376 | Os campos de só lectura están gris na grade **Estimacións de material**. |
|   Xestión de oportunidades | 2238337 | Pódese gardar unha oferta baseada nun contacto aínda que non estea asociada a unha lista de prezos do proxecto. |
|   Xestión de oportunidades | 2239810 | Pechar unha oferta perdida tamén pecha o proxecto asociado e cancela as reservas. |
| Planificación e rastrexo de proxectos | 2099559 | Engadíronse validacións adicionais para o estado do sistema antes de que se abra a grade **Tarefas do proxecto**. |
| Planificación e rastrexo de proxectos | 2178987 | Solucionouse un erro transitorio que se producía ao seleccionar **Seguinte fase** na páxina **Proxecto**. |
| Xestión de recursos | 2224817 | A funcionalidade para ampliar as reservas é o estado de reserva correcto. |
| Entrada de tempo | 2202476 | A páxina **Entrada de tempo** agora usa o control de grade de reacción e resolve problemas como o aliñamento incorrecto da grade. |
| Entrada de tempo | 2223377 | A entrada de tempo está oculta na sección **Relacionado** na páxina **Recurso reservable** para evitar confusións coa usabilidade. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Xestión e contabilidade de proxectos en Dynamics 365 Finance

| Área de funcionalidades | Número de referencia | Actualización de calidade |
| --- | --- | --- |
| Xestión e contabilidade de proxectos | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | Project Operations para situacións baseadas en recursos: Non pode converter unha oferta a gañada por un erro de integración. |
| Xestión e contabilidade de proxectos | [546604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546604) | Project Operations: Aparece unha mensaxe de erro cando intenta asociar unha liña de contrato a un ID de proxecto debido á comprobación de liñas de contrato e tipos de transacción superpostos. |
| Xestión e contabilidade de proxectos | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | **ProjCDSProjectContractEntity** define o enderezo da factura da orixe de financiamento dun cliente diferente. |
| Viaxes e gasto | [480451](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480451) | Pode producirse un erro de contabilización relacionado coa configuración da quilometraxe. |
| Viaxes e gasto | [522084](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522084) | A funcionalidade **Dividir a persoal** non funciona para as transaccións de gastos en moeda estranxeira. |
| Viaxes e gasto | [523938](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523938) | Os valores do menú despregable da categoría de gasto mostran categorías incorrectas para os delegados independentemente de se son un recurso. |
| Viaxes e gasto | [539266](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539266) | Non pode gardar un informe de gastos entre empresas por mor dun erro de **Validación de recursos/categorías**. |
| Viaxes e gasto | [532610](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532610) | O cálculo da taxa de quilometraxe incorrecto na contabilización de informes de gastos ten liñas divididas. |
| Viaxes e gasto | [537404](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537404) | Non pode publicar un informe de gastos entre empresas cando se inclúa o imposto sobre as vendas e o tipo de conta compensada no método de pagamento é **Traballador**. |
| Viaxes e gasto | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | A entidade de datos **TrvRequisitionLine** de reversión e o índice único están asociados. |
| Viaxes e gasto | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | O informe de gastos admite a creación e actualización de liñas de documentos de orixe. |
| Viaxes e gasto | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | Un diario de contabilidade auxiliar incorrecto móstrase nunha situación entre empresas se o imposto sobre as vendas se contabiliza na entidade legal de destino. |
| Viaxes e gasto | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | Project Operations: A estimación de gastos non se elimina de Finance cando se elimina de Dataverse. |
| Viaxes e gasto | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | Cando a categoría de gasto non é unha categoría de proxecto, as dimensións financeiras que están seleccionadas na páxina **Gastos** non se copian no informe de gastos. |
