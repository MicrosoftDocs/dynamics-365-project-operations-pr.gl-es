---
title: Novidades ou cambios na versión 19 de actualización de Project Service Automation, V3
description: Este tema mostra as funcionalidades e correccións que están dispoñibles la versión 19 de actualización de Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 05/05/2020
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
ms.openlocfilehash: ecc923cccfad21985025ab9d8006aaff16afc25f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076085"
---
# <a name="project-service-automation-update-release-19-v3"></a>Versión 19 de actualización de Project Service Automation, V3

Comprácenos anunciar a última actualización da aplicación Project Service Automation para Dynamics 365. Esta versión inclúe algunhas melloras importantes na calidade, rendemento e facilidade de uso. Esta versión é compatible con Dynamics 365 9.x. Para actualizar a esta versión, visite a paxina de solucións do Centro de administración para Dynamics 365 en liña para instalar a actualización. Para obter máis información, consulte [Instalar, actualizar ou eliminar unha solución preferida](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)

Este tema mostra as funcionalidades e correccións que son novas ou modificadas para PSA V3, versión 19 de actualización. Esta versión ten un número de compilación de V3.10.30.41 e está xeralmente dispoñible a través dunha actualización automática en maio de 2020.

## <a name="update-release-19"></a>Versión 19 de actualización

### <a name="bug-fixes"></a>Correccións de erros

**Tempo e gasto**

Resolvéronse os seguintes problemas: 

- Os erros derivados das importacións de entradas de tempo non aparecen correctamente.
- A grade de entrada de tempo non admite o comportamento de campo **Só data**.
- Os recursos do proxecto non son capaces de crear un gasto cun proxecto.

**Xestión de proxectos**

Resolvéronse os seguintes problemas: 

-  A tarefa seguinte á secundaria causa unha estimación de esforzo incorrecta durante o cálculo de finalización (EAC).

**Sales**

Resolvéronse os seguintes problemas: 

- A acción **Calcular de novo** non funciona cos detalles da liña do contrato de gasto ou cos detalles da liña de oferta.
- **Actualizar prezos** falta para as estimacións de gastos.
-  Os clientes non poden seleccionar os motivos para o estado do contrato na páxina **Contrato de proxecto**.
- Os clientes experimentan un rendemento degradado ao crear unha lista de prezos personalizada a partir dunha oferta.
- Os clientes experimentan incoherencia cos valores predeterminados de **unidade** nas páxinas **Detalles da liña de oferta** e **Detalles da liña de contrato**.
- Se engade elementos da categoría de transacción non imputable a unha liña de contrato imputable, non se respectará o tipo de facturación **Non imputable** da categoría de transacción.
- Os clientes non poden usar os roles e a categoría engadidos recentemente nos contratos creados anteriormente.
- Os clientes experimentan un rendemento degradado. Recuperación innecesaria en PreValidateProjectTeamMemberUpdate.cs
- Os roles configurados como non imputables na lista **Categorías de recursos** deberían engadirse ao separador **Roles imputables** como **Non imputable** na liña de contrato dun proxecto.
- Os clientes poden experimentar un rendemento degradado ao crear un proxecto porque **GetBookableResourceIdFromUser** recupera todas as columnas de recursos reservables en vez de só o ID principal.
- Na entidade **Tipo de transacción** falta o complemento de actualización de validación previa para evitar que os usuarios introduzan **Unidades** e **Grupos de unidades** que non sexan válidos para os tipos de transacción.
- O paso **Eliminar** non funciona para a importación de entradas de tempo.