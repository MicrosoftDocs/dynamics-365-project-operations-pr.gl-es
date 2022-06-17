---
title: Novidades ou cambios na versión 25 de actualización de Project Service Automation, V3
description: Este artigo enumera as funcións e correccións dispoñibles na actualización de Project Service Automation, versión 25, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
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
ms.openlocfilehash: 2330c7dc5d2dfb148d5c7fb9a5ce643fded84dde
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922542"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a>Novidades ou cambios na versión 25 de actualización de Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Comprácenos anunciar a última actualización da aplicación Project Service Automation para Dynamics 365. Esta versión inclúe algunhas melloras importantes na calidade, rendemento e facilidade de uso. Esta versión é compatible con Dynamics 365 9.x. Para actualizar a esta versión, visite a paxina de solucións do Centro de administración para Dynamics 365 en liña para instalar a actualización. Para obter máis información, consulte [Instalar, actualizar ou eliminar unha solución preferida](/power-platform/admin/install-remove-preferred-solution)

Este artigo enumera as funcións e as correccións que son novas ou modificadas para Project Service Automation V3, actualización da versión 25. Esta versión ten un número de compilación de V 3.10.43.76 e xeralmente está dispoñible mediante unha actualización automática en outubro de 2020.

## <a name="update-release-25"></a>Versión 25 de actualización

### <a name="bug-fixes"></a>Correccións de erros

**Tempo e gasto**

Corrixiuse o seguinte problema:

- O gráfico de entrada de tempo que mostra datos adicionais baseados nun intervalo demasiado grande que se recupera.

**Xestión de recursos**

Corrixiuse o seguinte problema:

- Engadiuse o código de Package Deployer para omitir a importación de parches de Universal Resource Scheduling se xa existe un parche de versión superior.

**Xestión de proxectos**

Resolvéronse os seguintes problemas:

- Corrixíronse as discrepancias de redondeo e taxa de cambio que dan lugar a nun custo planificado incorrecto na grade de rastrexo do proxecto.
- Admite a capacidade de amosar dúas ou máis grades de reacción no formulario **Proxecto**.
- Proporciona validación para abordar a posibilidade de atribuír unha tarefa máis tarde da data de finalización do calendario, o que da lugar a un erro na atribución de recursos.
- Mellorouse a xestión de erros para tratar a excepción de referencia nula xerada a partir do seguinte:

    - Complemento **PreValidateProjectTeamMemberCreate**
    - **PreValidateProjectTaskCreate** cando se crea unha tarefa de proxecto sen un proxecto asociado
    - Complemento **PreProjectTeamMemberCreate**
    - Complemento **PostProjectTeamMemberDelete**
    - Complemento **PreValidateProjectTaskDelete**

**Sales**

Resolvéronse os seguintes problemas:

- Mellorouse a xestión de erros para tratar excepcións de referencia nula xeradas a partir de **Copiar proxecto: Xestión de recursos Axuda de estimacións**.
- **Non está listo para facturar** no **Traballo pendente de facturación de tempo e material** non borra o estado de facturación.
- Corrixiuse o etiquetado incorrecto dos botóns de **Prezos** do separador **Prezo de rol** e **Artigos de catálogo**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
