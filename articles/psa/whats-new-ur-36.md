---
title: Novidades ou cambios na versión 36 de actualización de Project Service Automation, V3
description: Este tema indica as funcionalidades e correccións dispoñibles na versión 36 de actualización de Microsoft Dynamics 365 Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/06/2021
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
ms.openlocfilehash: 108c75598dc7dd3dd0cdb9ce68e30423d051a4cf
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586664"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-36-v3"></a>Novidades ou cambios na versión 36 de actualización de Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Comprácenos anunciar a última actualización da aplicación Microsoft Dynamics 365 Project Service Automation. Esta versión inclúe algunhas melloras importantes na calidade, rendemento e facilidade de uso. É compatible con Dynamics 365 9.x. Para actualizar esta versión, visite a páxina de solucións en liña do Centro de administración de Dynamics 365 e instale a actualización. Para obter máis información, consulte [Instalar, actualizar ou eliminar unha solución preferida](/power-platform/admin/install-remove-preferred-solution)

Este tema mostra as funcionalidades e correccións que son novas ou modificadas para Project Service Automation, versión 36 de actualización, V3. Esta versión ten un número de compilación de V3.10.57.152 e está dispoñible xeralmente a través dunha autoactualización desde outubro de 2021.

## <a name="update-release-36"></a>Versión 36 de actualización

### <a name="bug-fixes"></a>Correccións de erros

Resolvéronse os seguintes problemas.

**Xeral**
- O noe de campo **Modelo de hora de traballo predefinido** está traducido incorrectamente na páxina **Parámetros do proxecto**.
- Os complementos asíncronos non tratan correctamente as excepcións relacionadas con **SharedVariableService**.

**Tempo e gasto**
- Cando faltan liñas de diario ou o usuario non ten os privilexios correctos para ler as liñas de diario, prodúcese un erro incorrecto cando se cancelan as aprobacións do proxecto.
- Os usuarios non poden cancelar unha aprobación cando unha entrada de gasto ou tempo teña máis dunha aprobación de proxecto asociada.
- **Ausencia** e **Vacacións** están incorrectamente traducidos para o idioma chinés nunha busca na páxina de creación rápida de **Entrada de tempo**.

**Xestión de recursos**
- O usuario non pode buscar recursos no **Asistente de programación** cando o modo de vista está configurado en **Día**, **Semana** ou **Mes**.
- Permítese incorrectamente que os recursos xenéricos teñan nomes de posición baleiros. 
- O peche dun contrato como perdido non cancela futuras reservas.

**Vendas**
- Cando un ambiente ten un gran volume de produtos, o rendemento degrádase na grade **Estimación de materiais**.
- Ao crear un proxecto a partir dun modelo, a moeda do proxecto non é a unidade de contratación do xestor de proxectos respectivo.
- As cantidades reais non sempre coinciden co reflectido no proxecto debido, ou as cantidades vólvense negativas en escenarios específicos de recuperación.
- Prodúcese un erro ao asociar un proxecto creado a partir dun modelo de proxecto a unha liña de contrato.
- Os usuarios poden eliminar unha liña de contrato cos fitos **Listo para facturar** e **Factura creada**. Non se debería permitir isto.
- Cando se importan estimacións dun proxecto, a immputabildade detallada da liña de oferta establécese incorrectamente cando a facturación baseada en tarefas está activada para a liña de oferta.
- Cando engade un fito de facturación a prezo fixo, o fito non se reflicte na subgrade de fito ata que a páxina se actualice.
- Xérase unha excepción de referencia nula cando crea un contrato de proxecto cun nome de oferta que é nulo.
- As tarefas en modo manual onde a moeda do proxecto é diferente da moeda do recurso dan lugar a estimacións de prezos incorrectas.
- Os usuarios non poden recuperar unha transacción que se corrixiu con éxito mediante unha factura correctiva.
- As categorías de transaccións desactivadas aparecen na grade **Estimacións de gastos**.



