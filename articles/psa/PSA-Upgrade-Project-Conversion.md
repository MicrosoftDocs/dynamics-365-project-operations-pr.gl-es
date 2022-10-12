---
title: Cambios de características de Project Service Automation a Project Operations
description: Este artigo ofrece unha visión xeral dos cambios de funcións para Microsoft Dynamics 365 Project Service Automation a Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/03/2022
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
ms.openlocfilehash: 9869b3ad0fb6429484a26f367e06a0996f110ed8
ms.sourcegitcommit: a2d720ac6d7ddb20a0967fe87992a376b2478208
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/04/2022
ms.locfileid: "9621316"
---
# <a name="feature-changes-for-project-service-automation-to-project-operations"></a>Cambios de características de Project Service Automation a Project Operations

Despois de que un proxecto se actualice con éxito desde Microsoft Dynamics 365 Project Service Automation 3.X a Dynamics 365 Project Operations Lite, a edición de tarefas do proxecto na estrutura de descomposición do traballo da grella de tarefas (WBS) non é posible. Os clientes poderán revisar os WBS na grella de seguimento onde se engadiron novos campos para proporcionar todos os detalles relacionados coa tarefa. Para proxectos nos que se requiren edicións na WBS, pode converter selectivamente os proxectos elixibles ao novo proxecto para a experiencia de programación web.

## <a name="project-conversion-process"></a>Proceso de conversión do proxecto

Para converter un proxecto, siga estes pasos.

1. Abre a páxina principal do proxecto e selecciona **Converter** no panel de accións.
1. Na caixa de mensaxes de confirmación, seleccione **Ok** para iniciar a conversión do proxecto. Prodúcense as seguintes accións:

    1. Unha barra de mensaxes que aparece na páxina principal do proxecto indica: "A programación do proxecto estase a converter. Non podes facer cambios no proxecto ata que se complete a conversión".
    1. Estás redirixido á lista de proxectos.

    Despois de completar a conversión do proxecto, prodúcense as seguintes accións:

    1. O director do proxecto asignado recibe unha notificación no lado dereito da aplicación.
    1. Elimínase a barra de mensaxes que indica que a conversión está en curso.
    1. O **Horario** mostra a nova experiencia de programación con Project para a web. Calquera usuario que teña as licenzas e as funcións de seguranza adecuadas pode editar o WBS.
    1. O **Motor de programación** campo está actualizado a **Proxecto para a web**.
    1. O **Converter** elimínase do panel de accións.

> [!IMPORTANT]
> Non se permite a conversión masiva de proxectos. Calquera intento de actualizar un gran volume de proxectos ao mesmo tempo será limitado. Esta limitación axuda a garantir un alto rendemento para todos os clientes.

## <a name="manual-tasks-vs-automatic-tasks"></a>Tarefas manuais vs tarefas automáticas

Cando se actualiza un ambiente de Project Service Automation a Project Operations, todas as tarefas da WBS considéranse programadas automaticamente. O concepto de tarefas programadas manualmente non está dispoñible en Project para a web. Non obstante, pode definir o comportamento de programación preferido para os seus proxectos usando o [modo de programación](/project-management/scheduling-modes.md) configuración cando crea novos proxectos.

## <a name="restricted-operations-for-pre-conversion-projects"></a>Operacións restrinxidas para proxectos previos á conversión

Esta sección describe as diferenzas funcionais que pode esperar cando os proxectos non se converteron.

### <a name="copy-project"></a>Copiar proxecto

O **Copiar** A operación só se admite nos proxectos convertidos. Os proxectos actualizados non se poden copiar antes da conversión.

### <a name="move-project"></a>Mover proxecto

Un cambio na data de inicio dun proxecto non moverá proporcionalmente o inicio das tarefas a non ser que o proxecto fose convertido.

## <a name="frequently-asked-questions"></a>Preguntas máis frecuentes

### <a name="what-are-the-differences-between-converted-projects-and-new-projects-that-are-created-after-the-upgrade-has-been-completed"></a>Cales son as diferenzas entre os proxectos convertidos e os novos que se crean despois de completar a actualización?

Para os proxectos que se converten despois de actualizar o ambiente, establecerase unha bandeira que indicará que o calendario respecte só o calendario do proxecto. Este comportamento coincide co comportamento de Project Service Automation. Non obstante, a marca non se establecerá para proxectos novos que se creen despois da actualización. Polo tanto, o horario respectará o horario de traballo dos recursos cando estean asignados a unha tarefa.

### <a name="what-should-i-do-if-my-project-fails-to-be-converted"></a>Que debo facer se o meu proxecto non se converte?

Se o teu proxecto non se converte, o primeiro paso é revisar os rexistros de erros para identificar os problemas comúns relacionados co teu WBS. Se os rexistros non indican un erro específico no que poida tomar medidas, póñase en contacto con Atención ao cliente para que o seu caso poida ser revisado máis a fondo.

### <a name="how-are-business-closures-handled-in-project-for-the-web"></a>Como se xestionan os peches de empresas en Project for the web?

O proxecto para a web non respecta os peches de empresas que a empresa defina a nivel de organización. Non obstante, respectará outros tipos de días libres que se definan nun modelo de horario laboral determinado.

### <a name="what-are-the-limitations-of-project-for-the-web"></a>Cales son as limitacións de Project for the web?

Ver [Crear unha estrutura de desglose do traballo: Limitacións do proxecto](/project-management/create-wbs#project-limitations.md).

### <a name="can-i-expect-changes-to-my-cost-and-sales-estimates"></a>Podo esperar cambios nas miñas estimacións de custos e vendas?

En casos raros nos que se recalculan os contornos de asignación de recursos ou nos que se sitúan nun límite de data diferente ao do proxecto de orixe, é posible que vexa diferenzas nas estimacións de custos e vendas. Como parte do proceso de actualización, espérase que os clientes proben un conxunto representativo de proxectos de mostra, para que poidan comprender calquera posible cambio de programación.
