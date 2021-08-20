---
title: 'Novidades de xullo de 2021: despregamento de Project Operations lite'
description: Este tema ofrece información sobre as actualizacións de calidade dispoñibles na versión de xullo de 2021 do despregamento de Project Operations lite.
author: sigitac
ms.date: 07/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 8cff4c37e1c2df29041ef86cdcf05afa6093f890565a855024202e87fd533ea5
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009214"
---
# <a name="whats-new-july-2021---project-operations-lite-deployment"></a>Novidades de xullo de 2021: despregamento de Project Operations lite

_Aplícase a: Despregamento de Lite - acordo para facturación proforma_

Este tema aplícase aos seguintes compoñentes e versións de Dynamics 365 Project Operations:

  - Project Operations no ambiente de Dataverse versión 4.12.0.148 ou 4.12.0.152.

## <a name="quality-updates"></a>Actualizacións de calidade
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
