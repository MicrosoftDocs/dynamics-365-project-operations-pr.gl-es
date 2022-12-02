---
title: Novidades de xullo de 2021 - Project Operations para situacións baseadas en recursos/sen fornecemento
description: Este artigo ofrece información sobre as actualizacións de calidade dispoñibles na versión de xullo de 2021 de Project Operations para situacións baseadas en recursos/sen fornecemento.
author: sigitac
ms.date: 07/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: c004a6adc265f8f02fc557700d9b88a174c221c4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931696"
---
# <a name="whats-new-july-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades de xullo de 2021 - Project Operations para situacións baseadas en recursos/sen fornecemento

*Aplícase a: Project Operations para situacións baseadas en recursos/sen fornecemento*

Este artigo aplícase aos seguintes compoñentes e versións de Dynamics 365 Project Operations:

   - Project Operations no ambiente de Microsoft Dataverse versión 4.12.0.148 ou 4.12.0.152.
   - Xestión e contabilidade de proxectos en ambientes de aplicacións de Dynamics 365 Finance versión 10.0.20.

## <a name="features-included-in-this-release"></a>Funcionalidades incluídas nesta versión

As seguintes funcionalidades están incluídas nesta versión:

- Posibilidade de que administradores vexan rexistros de PSS e rexistros de conxunto de operacións no menú de configuración. Os rexistros almacénanse durante 90 días.

## <a name="project-operations-dual-write-maps-updates"></a>Actualizacións de mapas de escrita dual en Project Operations

Non hai actualizacións para mapas de escrita dual de Project Operations nesta versión.

Para obter unha lista actual e versións dos mapas de escrita dual de Project Operations, consulte [Versións de mapa de escrita dual de Project Operations](../environment/resource-dual-write-maps.md).

Execute sempre a última versión do mapa no seu ambiente e active todos os mapas de táboa relacionados mentres actualiza a súa solución de Project Operations Dataverse solución e a versión da solución de Finance. É posible que certas funcionalidades e capacidades non funcionen correctamente se a última versión do mapa non está activada. Pode ver a versión activa do mapa na páxina **Escrita dual** na columna **Versión**. Active unha nova versión do mapa seleccionando **Versións do mapa de táboas**, seleccionando a última versión e logo gardando a versión seleccionada. Se personalizou un mapa de táboa listo para usar, aplique de novo os cambios. Para obter máis información, consulte [Xestión do ciclo de vida da aplicación](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se ten algún problema ao iniciar o mapa, siga as instrucións da sección [Problema de columnas da táboa que faltan nos mapas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) na guía de resolución de problemas de escrita dual.

## <a name="quality-updates"></a>Actualizacións de calidade

### <a name="project-operations-on-dataverse"></a>Project Operations en Dataverse

| **Área de funcionalidades**              | **Número de referencia** | **Actualización de calidade**                                                                                                                                                                                             |
|-------------------------------|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Facturación e prezos           | 2224046              | O campo **Clase de transacción** pódese editar no separador **Detalles da liña de oferta**, pero está bloqueado se está a traballar desde a páxina **Detalles da liña de oferta**.                                                                     |
| Facturación e prezos           | 2224400              | A acción **Pechar oferta como gañada** falla cando unha oferta non ten fitos de data.                                                                                                                                    |
| Facturación e prezos           | 2234089              | Cando introduce manualmente unha descrición do produto, bórrase despois de introducir unha cantidade para unha estimación de material.                                                                                                                         |
| Facturación e prezos           | 2234100              | A grade **Configuración da facturación de tarefas** non inclúe a columna **Material** e o seu valor no separador **Facturación de tarefas** do proxecto.                                                                                                       |
| Facturación e prezos           | 2277409              | O identificador do produto non está dispoñible no detalle da liña de contrato para unha liña de tipo de material.                                                                                                                                        |
| Facturación e prezos           | 2281728              | A creación dunha liña de contrato avalía de novo os datos reais innecesariamente provocando aumentos significativos no volume de datos, o que repercute no rendemento.                                                                                |
| Facturación e prezos           | 2298668              | As liñas de diario asociadas a un gasto recuperado e eliminado non se eliminan.                                                                                                                                     |
| Facturación e prezos           | 2300192              | Cando varios usuarios están editando unha factura, é posible que se cree un novo detalle de liña de factura nunha factura confirmada.                                                                                   |
| Facturación e prezos           | 2301569              | As facturas non se poden corrixir se se aplicou o importe de retención \$0.                                                                                                                                        |
| Facturación e prezos           | 2307965              | Aparecerá un erro se se crea un prezo de categoría con valores que faltan.                                                                                                                           |
| Facturación e prezos           | 2326870              | Prodúcese un erro en **Microsoft.Dynamics.ProjectService.Plugins.PostInvoiceLineDelete** se **producttypecode** ñe nulo.                                                                            |
| Facturación e prezos           | 2332732              | Prodúcese un erro se se crea un fito da liña de contrato sen unha liña de pedido.                                                                                                                |
| Planificación e rastrexo de proxectos | 2181094              | A API de programación de proxectos agora admite rexistros de PSS e rexistros de conxunto de operacións que se almacenan durante 90 días.                                                                                                                  |
| Planificación e rastrexo de proxectos | 2254201              | A etiqueta de **Modo de programación** actualízase con detalles que describen a lóxica predefinida.                                                                                                                                      |
| Planificación e rastrexo de proxectos | 2300252              | A caché de respostas **openProject** actualízase e inclúe ao propietario do token na clave de caché, **base Url**, e **Segment Url** así que **Request Url** sempre se pode volver crear se o ficheiro **base Url** cambia. |
| Planificación e rastrexo de proxectos | 2301312              | **msdyn_membershipstatus** foi eliminado da vista **Membro do equipo do proxecto**.                                                                                                                                        |
| Planificación e rastrexo de proxectos | 2302759              | Os produtos obtéñense innecesariamente nos separadores **Asignacións de recursos**, **Estimacións** e **Estimacións de gastos**.                                                                                                        |
| Planificación e rastrexo de proxectos | 2308050              | **CopyProject** falla co erro "Erro ao obter o token para falar co servizo remoto".                                                                                                                           |
| Planificación e rastrexo de proxectos | 2322650              | A vista **Lista de tarefas do proxecto** actualizouse para amosar a data da tarefa por defecto.                                                                                                            |
| Planificación e rastrexo de proxectos | 2327266              | **CopyProject** xera o erro "A clave non se atopou no dicionario" ao copiar estimacións.                                                                                                      |
| Planificación e rastrexo de proxectos | 2328123              | **CopyProject** xera o erro "Erro ao obter o token para falar co servizo remoto".                                                                                                                          |
| Planificación e rastrexo de proxectos | 2336258              | **CopyProject** copia incorrectamente os nomes de posición dos recursos.                                                                                                                                                 |
| Facturación e prezos           | 2224476              | O campo **Recurso reservable** non é o predeterminado correctamente para o usuario conectado na páxina **Uso do material**.                                                                                                            |
| Xestión de recursos           | 2277249              | Prodúcese un erro cando se actualiza un requisito de recursos non baseado en proxectos.                                                                                                            |
| Xestión de recursos           | 2323869              | A utilización dos recursos non recoñece correctamente os recursos filtrados.                                                                                                                                             |
| Tempo e gasto              | 2176538              | Aplícanse os operadores de filtro incorrectos ao control **Entrada de tempo**.                                                                                                                                                   |
| Tempo e gasto              | 2177462              | Se elimina unha entrada de tempo na grade non se actualiza o estado dos botóns **Enviar**, **Recuperar**, **Eliminar** e **Editar entrada** como se esperaba.                                                                                        |
| Tempo e gasto              | 2299985              | **TimeEntriesImportFromResourceAssignment** non mantén a hora de inicio/fin dos contornos da atribución.                                                                                                  |
| Tempo e gasto              | 2318426              | Despois de enviar unha entrada de tempo, aínda se poden editar os campos bloqueados.                                                                                                                                   |
| Tempo e gasto              | 2323749              | Prodúcese un erro cando se crea un gasto a partir do separador **Relacionado** dun recurso reservable.                                                                                                      |
| Tempo e gasto              | 2327678              | Cando crea unha entrada de tempo desde o separador **Relacionado** dun recurso reservable, o recurso principal non se pasa ao control de entrada de tempo.                                                                            |
| Xeral                       | 2296857              | Rastrexo do progreso para traballos de longa duración.                                                                                                                                                                        |
| Xeral                       | 2253682              | A solución de escrita dual de Project Operations non se debería instalar cando o núcleo de escrita dual está instalado nun ambiente sen a solución de orquestración de escrita dual.                                                |
| Xeral                       | 2316420              | O aprovisionamento principal de Project Service falla se cambia a unidade de negocio do usuario da aplicación.                                                                                                                     |
| Xeral                       | 2376405              | Solucionouse un problema de actualización causado polo editor (a actualización de calidade está dispoñible na versión 4.12.0.152)                                                                                                                     |
### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Xestión e contabilidade de proxectos en Dynamics 365 Finance

| Área de funcionalidades                      | Número de referencia | Actualización de calidade                                                                                                                                                                                                                                                                                                                |
|-----------------------------------|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Xestión e contabilidade de proxectos | 4620267          | Non se poden personalizar formularios para engadir un campo **Propósito** ás páxinas **Transacción contabilizada do proxecto**, **Creación de proposta de factura** e **Proposta de factura**.                                                                                                                                                                                         |
| Xestión e contabilidade de proxectos | 4613449          | Cando selecciona un ID de contrato de proxecto en Finance, o ambiente integrado de Project Operations abre a páxina para crear un novo rexistro en lugar da páxina para os contratos de proxecto xa creados.                                                                                                                                           |
| Xestión e contabilidade de proxectos | 4614445          | No despregamento de escenarios integrados de Project Operations, non pode editar o campo **Grupo do imposto sobre as vendas** da proposta de factura importada desde a transición. O grupo de impostos sobre vendas de artigos debería ser editable para unha proposta de factura aberta de todo tipo de transaccións, incluídas conta, horas, gastos, taxas e artigos. |
| Xestión e contabilidade de proxectos |                  | Non se pode contabilizar unha proposta de factura que resulte dunha corrección negativa da transacción de tempo.                                                                                                                                                                                                                                              |
| Xestión e contabilidade de proxectos |                  | As liñas de proposta de factura están duplicadas debido a varios procesos periódicos de **Importar desde transición** executándose ao mesmo tempo.                                                                                                                                                                                                                |

