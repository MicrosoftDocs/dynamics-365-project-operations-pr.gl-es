---
title: Propoñer recursos do proxecto
description: Este tema fornece información sobre como propoñer recursos de proxecto.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: bdb0dcb2-4421-4ee1-b97d-89a8cdefbd8d
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 3a7f7c15c3c7a3c39f2b7b9eeb88b9cf0cfdc220
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751464"
---
# <a name="propose-project-resources"></a>Propoñer recursos do proxecto

Os xestores de recursos poden propoñer un recurso ao xestor de proxectos empregando unha solicitude de recursos.

1. Na grade de solicitudes ou na propia solicitude, seleccione **Buscar recursos**.
2. Na páxina **Asistente de programación**, seleccione o recurso e, a seguir, no panel **Crear reserva de recursos**, no campo **Estado da reserva**, seleccione **Reservar**.

    ![Recurso proposto seleccionado](media/Resource-Management-image62.png)

Prodúcense as seguintes actualizacións de estado:

- Na páxina **Asistente de programación**, os indicadores de estado actualízanse para indicar que a reserva é unha proposta, non unha reserva dura.

    ![Indicadores de estado para a reserva proposta na páxina de Asistente de programación](media/Resource-Management-image63.png)

- Na solicitude do recurso, o estado cambia a **Necesita revisión**.

    ![Estado de solicitude de recurso cambiado a Necesita revisión.](media/Resource-Management-image64.png)

- No separador **Equipo** do proxecto, o valor **Estado da solicitude** do membro xenérico do equipo, o valor cambiase a **Necesita revisión**.

    ![Estado da solicitude de membro xenérico de equipo cambiado a Necesita revisión no separador Equipo](media/Resource-Management-image48.png)

O responsable do proxecto pode aceptar ou rexeitar a proposta.

Cando os xestores de recursos procesan solicitudes de recursos, poden empregar calquera dos seguintes enfoques:

- Propoñer múltiples recursos para satisfacer a demanda se non se dispón dun recurso único para cumprir as horas requiridas. As horas propostas divídense entre varios recursos que poden satisfacer as horas requiridas. Neste escenario, as horas non se poden solapar.
- Propoñer menos recursos dos necesarios. Neste escenario, a capacidade do recurso proposta é inferior ás horas requiridas que o solicitante especificou. Polo tanto, cando o solicitante acepta os recursos propostos, créase un requisito de recursos non cumpridos para capturar a demanda restante.
- Reserve múltiples recursos para satisfacer a demanda se non dispón dun recurso único para rematar o traballo.
- Reserve menos recursos dos necesarios. Neste escenario, as horas reservadas son menos que as horas requiridas. O sistema guíalle para que propoña recursos en lugar de reservas para que o solicitante poida verificar e rastrexar da demanda restante.

## <a name="billable-utilization"></a>Utilización facturable

Os recursos poden ter unha utilización facturable obxectivo. Esta utilización obxectivo defínese como un atributo no rol predefinido dun recurso ou establécese no rexistro do recurso reservable individual. Os cálculos de utilización baséanse nas horas reais que os recursos comunicaron mediante entradas de tempo aprobadas.

Para o cálculo da utilización úsanse as seguintes fórmulas:

- Utilización facturable = (Horas reais imputables) ÷ (Capacidade do recurso).
- Utilización non facturable = Tempo real con ID de tipo de facturación = Non imputable, Gratuíto ou Non dispoñible ÷ Capacidade do recurso
- Interno = Tempo real sen contrato de vendas ÷ Capacidade do recurso
- Capacidade do recurso = Horas laborables do recurso - Fóra de oficina - Días non laborables

Podes atopar a vista **Utilización de recursos** no panel **Recursos**.

![Visualización da utilización de recursos](media/Resource-Management-image65.png)

Cada cela da grade representa a porcentaxe de utilización facturable do recurso nun período, como un día, unha semana ou un mes. Para o color das celas úsanse as seguintes fórmulas:

- **Verde:** Utilización facturable \>= Utilización obxectivo de recursos
- **Amarelo:** Utilización de recursos – 20 \<= Utilización facturable \< Utilización objectivo
- **Vermello:** Utilización facturable \< Utilización obxectivo – 20

Debido a que a vista **Utilización de recursos** está baseada no panel de programación, pode empregar as capacidades de filtrado do panel de programación para filtrar os seus resultados.

A grade require que estableza unha utilización obxectivo no rol ou o recurso individual. Para configurar isto, vaia a **Recursos** \> **Roles de recursos**.

Ademais, debe atribuírse un rol predefinido a cada recurso reservable. Vaia a **Recursos** \> **Recursos**. No separador **Project Service**, verifique se está definido un rol de recurso e que o campo **É predefinido** para el está configurado en **Si**. Pode engadir roles adicionais cando **É predefinido = Non**. O rol cando **É predefinido = Si** úsase para avaliar a utilización do recurso fronte ao obxectivo para ese rol.

![Rol predefinido establecido](media/Resource-Management-image67.png)

No separador **Project Service**, tamén pode configurar unha utilización obxectivo individual para o recurso. A seguir, o cálculo de utilización usa esa utilización obxectivo para avaliar o obxectivo do recurso no canto do obxectivo do rol predefinido do recurso.

A utilización móstrase para un recurso só se ese recurso ten un tempo imputable acordado durante o período que se amosa na grade.

## <a name="resource-availability"></a>Dispoñibilidade de recursos

É fundamental que os xestores de recursos poidan ver a dispoñibilidade de recursos e actualizar as reservas. Nalgúns casos, non hai unha demanda formal (solicitude de recursos), pero un xestor de recursos debe responder a unha demanda non planificada que chega por canles como un correo electrónico, chamada telefónica ou mensaxe instantánea. Os xestores de recursos usan o panel de programación para actualizar recursos e reservas.

As horas laborables do recurso serven como base para calcular a dispoñibilidade dun recurso. As reservas de recursos consumen a capacidade dos recursos.

![Panel de programación](media/Resource-Management-image68.png)

O panel de programación usa cores e sombreados para amosar reservas, dispoñibilidade e saturacións, e tamén o estado das reservas. Un axuste da configuración do panel de programación permítelle mostrar unha lenda.

Se aparece unha frecha apuntando á dereita xunto a un recurso reservable individual no panel de programación, pódese ampliar o recurso para mostrar detalles do traballo no que está reservado o recurso.

![Engadir o recurso reservable expandido no panel de programación](media/Resource-Management-image69.png)

Debido a que Dynamics 365 Project Service Automation usa o motor de Universal Resource Scheduling, se tamén ten Dynamics 365 Field Service instalado, pode ver os detalles das reservas de recursos para proxectos, pedidos de traballo e calquera outra entidade á que estendeu a programación.

![Detalles de reservas de recursos para proxectos e pedidos de traballo](media/Resource-Management-image70.png)

Para ver máis detalles sobre un recurso individual, prema co botón dereito sobre el para abrir a tarxeta do recurso.

![Tarxeta de recurso](media/Resource-Management-image71.png)
