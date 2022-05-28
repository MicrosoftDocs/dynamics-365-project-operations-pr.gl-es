---
title: Novidades ou cambios na versión 38 de actualización de Project Service Automation, V3
description: Este tema indica as funcionalidades e correccións dispoñibles na versión 38 de actualización de Microsoft Dynamics 365 Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 12/06/2021
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 16994535d57dc1d7fefbe6e892c154f52638c7c0
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598716"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-38-v3"></a>Novidades ou cambios na versión 38 de actualización de Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Comprácenos anunciar a última actualización da aplicación Microsoft Dynamics 365 Project Service Automation. Esta versión inclúe algunhas melloras importantes na calidade, rendemento e facilidade de uso. É compatible con Dynamics 365 9.x. Para actualizar esta versión, visite a páxina de solucións en liña do Centro de administración de Dynamics 365 e instale a actualización. Para obter máis información, consulte [Instalar, actualizar ou eliminar unha solución preferida](/power-platform/admin/install-remove-preferred-solution)

Este tema mostra as funcionalidades e correccións que son novas ou modificadas para Project Service Automation, versión 38 de actualización, V3. Esta versión ten un número de compilación de V3.10.59.117 e está dispoñible xeralmente a través dunha actualización automática en decembro de 2021.

## <a name="update-release-38"></a>Versión 38 de actualización

### <a name="bug-fixes"></a>Correccións de erros

Resolvéronse os seguintes problemas.

**Hora e gasto**

- Prodúcese unha excepción cando a lonxitude dos rexistros do conxunto de aprobación supera os 100.000 rexistros.
- Os usuarios non poden acceder a **Entrada horaria** reixa de O **Entrada horaria** páxina principal.
- O **Importación de entrada de hora** cadro de diálogo non mostra ningún texto cando non hai elementos aptos para importar.
- Os usuarios poden crear conxuntos de aprobación onde o **Estado de destino** campo está configurado en **Descoñecido**.

**Xestión de proxectos**

- Os contornos non se mostran correctamente nas asignacións de recursos para UTC(+09:30) e UTC(+10:00) cando comeza o horario de verán.
- O **Columna adicional** O campo para as estruturas de descomposición do traballo está oculto nalgúns lugares.
- O selector de datas para o control do calendario no **Tarefa do proxecto** a grella non está correctamente localizada para o chinés.

**Vendas**

- **Execución do contrato** e **Custo real do proxecto** os valores non coinciden cando os recursos reservables que teñen diferentes unidades de contratación e moedas envían entradas de tempo.
- Un fluxo de traballo personalizado para confirmar facturas automaticamente falla cando as facturas se importan como solución administrada. Móstrase a seguinte mensaxe: "Microsoft.Xrm.Sdk.InvalidPluginExecutionException Mensaxe: estado da factura non válido".
- Cando **Raíz** se selecciona como opción de resumo e o proxecto ten estimacións dunha mestura de clases de transaccións (por exemplo, unha combinación de estimacións de tempo, gastos e materiais), o sistema resume todas as clases de transaccións como unha única liña de tarifa.
- Nos escenarios nos que se engade unha liña de gasto antes de asociarse a unha liña de contrato cun proxecto, o prezo correcto non se introduce como valor predeterminado no **Actualizar prezo** campo.
- Non se permiten cantidades de vendas negativas **Proxecto** e **Tarefa** entidades.
