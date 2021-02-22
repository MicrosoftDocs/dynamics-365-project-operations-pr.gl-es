---
title: Novidades ou cambios na versión 26 de actualización de Project Service Automation, V3
ms.openlocfilehash: 849e7288ee91d3e9360c0b03f6b8b37ff29338e7
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643261"
---
<a name="project-service-automation-update-release-26-v3"></a>Versión 26 de actualización de Project Service Automation, V3
================================================

Comprácenos anunciar a última actualización da aplicación Project Service Automation para Dynamics 365. Esta versión inclúe algunhas melloras importantes na calidade, rendemento e facilidade de uso. Esta versión é compatible con Dynamics 365 9.x. Para actualizar a esta versión, visite a paxina de solucións do Centro de administración para Dynamics 365 en liña para instalar a actualización. Para obter máis información, consulte [Instalar, actualizar ou eliminar unha solución preferida](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)

Este tema mostra as funcionalidades e correccións que son novas ou modificadas para Project Service Automation, versión 26 de actualización, V3. Esta versión ten un número de compilación de V3.10.44.59 e está dispoñible xeralmente a través dunha actualización automática en decembro de 2020.

<a name="update-release-26"></a>Versión 26 de actualización
-----------------

### <a name="bug-fixes"></a>Correccións de erros

**Tempo e gasto**

Resolvéronse os seguintes problemas:

-   Os usuarios poden cambiar a tarefa nunha entrada de tempo aprobada/enviada.

-   Erro de "Referencia de obxecto non definida" ao gardar a entrada de tempo.

-   A importación de entradas de tempo a partir das atribucións de recursos crea entradas de tempo cos valores de data e hora incorrectos.

-   Cando se instalan Project Service Automation e a aplicación Field Service, o botón **Novo** móstrase dúas veces na barra de comandos para as entradas de tempo na aplicación Field Service.

-   As actualizacións das celas **Permitir unidade** e **Grupo de unidades** agora funcionan na grade **Estimacións de gastos**.

-   O formulario **Actualizar edición de entrada de tempo** inclúe **Liña de tempo**.

-   A aprobación do tempo para as entradas de tempo que non sexan do proxecto bloquea o sistema cando se busca un rol de responsable de aprobación de proxecto.

**Xestión de recursos**

Resolvéronse os seguintes problemas:

-   Engadiuse a validación no complemento **PostProjectCreate** para comprobar se hai un requisito principal antes de crealo.

-   O formulario de creación rápida **Membro do equipo do proxecto** produce unha excepción de referencia nula se se eliminan campos do formulario.

-   Xerar requisitos para 12 horas ao longo dun ano fallará.

-   Mellorouse a excepción de referencia nula da mensaxe de erro durante a creación de requisitos de recursos.

**Xestión de proxectos**

Resolvéronse os seguintes problemas:

-   Validación mellorada para abordar a excepción de referencia nula xerada no complemento **PreProjectUpdate**.

-   Os proxectos publicados polo complemento de escritorio Microsoft Project eliminan tarefas sen atribuír.

-   Engadiuse unha nova validación cando a referencia do proxecto dunha tarefa non é válida debido a unha excepción de referencia nula no complemento **PreValidateProjectTaskUpdate**.

-   A grade de membros do equipo non mostra atribucións distintas no rexistro de membros do equipo.

-   Engadíronse novas mensaxes de validación e erro debido a unha excepción de referencia nula no complemento **PreProjectTaskDelete**.

**Sales**

Resolvéronse os seguintes problemas:

-   Ao seleccionar unha liña baseada en proxecto en oferta ou contrato, o botón **Suxestión** só debería ser visible cando se selecciona unha liña baseada en produto asociada a un produto existente.

-   Separe o privilexio **Create_Product** do privilexio **Create_ProjectContract**.

-   A eliminación dunha liña de factura provoca un fallo de referencia nula en **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.