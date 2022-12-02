---
title: Novidades ou cambios na versión 38 de actualización de Project Service Automation, V3
description: Este artigo indica as funcionalidades e correccións dispoñibles na versión 38 de actualización de Microsoft Dynamics 365 Project Service Automation, V3.
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
ms.openlocfilehash: ccc08cd0bc365bd4761424a4c0ceac91985e7c89
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915183"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-38-v3"></a>Novidades ou cambios na versión 38 de actualización de Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Comprácenos anunciar a última actualización da aplicación Microsoft Dynamics 365 Project Service Automation. Esta versión inclúe algunhas melloras importantes na calidade, rendemento e facilidade de uso. É compatible con Dynamics 365 9.x. Para actualizar esta versión, visite a páxina de solucións en liña do Centro de administración de Dynamics 365 e instale a actualización. Para obter máis información, consulte [Instalar, actualizar ou eliminar unha solución preferida](/power-platform/admin/install-remove-preferred-solution)

Este artigo mostra as funcionalidades e correccións que son novas ou modificadas para Project Service Automation, versión 38 de actualización, V3. Esta versión ten un número de compilación de V3.10.59.117 e está dispoñible xeralmente a través dunha actualización automática en decembro de 2021.

## <a name="update-release-38"></a>Versión 38 de actualización

### <a name="bug-fixes"></a>Correccións de erros

Resolvéronse os seguintes problemas.

**Hora e gasto**

- Prodúcese unha excepción cando a lonxitude dos rexistros do conxunto de aprobacións supera os 100.000 rexistros.
- Os usuarios non poden acceder á grade **Entrada de tempo** da páxina principal de **Entrada de tempo**.
- A caixa de diálogo **Importación de entradas de tempo** non mostra ningún texto cando non hai elementos aptos para importar.
- Os usuarios poden crear conxuntos de aprobacións onde o campo **Estado de destino** está configurado como **Descoñecido**.

**Xestión de proxectos**

- Os contornos non se mostran correctamente nas atribucións de recursos para UTC(+09:30) e UTC(+10:00) cando comeza o horario de verán.
- O campo **Columna adicional** para as estruturas de subdivisión do traballo está oculto nalgúns lugares.
- O selector de datas para o control do calendario na grade **Tarefa de proxecto** non está correctamente localizada para o chinés.

**Vendas**

- Os valores de **Execución do contrato** e **Custo real do proxecto** non coinciden cando os recursos reservables que teñen diferentes unidades de contratación e moedas envían entradas de tempo.
- Un fluxo de traballo personalizado para confirmar facturas automaticamente falla cando as facturas se importan como solución administrada. Móstrase a seguinte mensaxe: "Microsoft.Xrm.Sdk.InvalidPluginExecutionException Message: estado da factura non válido".
- Cando **Raíz** se selecciona como opción de resumo e o proxecto ten estimacións dunha mestura de clases de transaccións (por exemplo, unha combinación de estimacións de tempo, gastos e materiais), o sistema resume todas as clases de transaccións como unha única liña de tarifa.
- En situacións nas que se engade unha liña de gasto antes de asociarse a unha liña de contrato cun proxecto, o prezo correcto non se introduce como valor predefinido no campo **Actualizar prezo**.
- Non se permiten cantidades de vendas negativas nas entidades **Proxecto** e **Tarefa**.
