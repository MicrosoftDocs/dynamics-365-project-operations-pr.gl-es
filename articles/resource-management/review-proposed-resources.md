---
title: Revisar os recursos propostos
description: Este tema fornece información sobre como propoñer recursos de proxecto.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 212b80a7fde8368eedd7572dd5f9278cc53fae98
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897359"
---
# <a name="review-proposed-resources"></a>Revisar os recursos propostos

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Os xestores de recursos poden propoñer un recurso ao xestor de proxectos empregando unha solicitude de recursos.

1. Na grade de solicitudes ou na propia solicitude, seleccione **Buscar recursos**.
2. Na páxina **Asistente de programación**, seleccione o recurso e, a seguir, no panel **Crear reserva de recursos**, no campo **Estado da reserva**, seleccione **Reservar**.

Prodúcense as seguintes actualizacións de estado:

- Na páxina **Asistente de programación**, os indicadores de estado actualízanse para indicar que a reserva é unha proposta, non unha reserva dura.
- Na solicitude do recurso, o estado cambia a **Necesita revisión**.
- No separador **Equipo** do proxecto, o valor **Estado da solicitude** do membro xenérico do equipo, o valor cambiase a **Necesita revisión**.

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

Cada cela da grade representa a porcentaxe de utilización facturable do recurso nun período, como un día, unha semana ou un mes. Para o color das celas úsanse as seguintes fórmulas:

- **Verde:** Utilización facturable \>= Utilización obxectivo de recursos
- **Amarelo:** Utilización de recursos – 20 \<= Utilización facturable \< Utilización objectivo
- **Vermello:** Utilización facturable \< Utilización obxectivo – 20

Debido a que a vista **Utilización de recursos** está baseada no panel de programación, pode empregar as capacidades de filtrado do panel de programación para filtrar os seus resultados.

A grade require que estableza unha utilización obxectivo no rol ou o recurso individual. Para configurar isto, vaia a **Recursos** \> **Roles de recursos**.

Ademais, debe atribuírse un rol predefinido a cada recurso reservable. Vaia a **Recursos** \> **Recursos**. No separador **Project Service**, verifique se está definido un rol de recurso e que o campo **É predefinido** para el está configurado en **Si**. Pode engadir roles adicionais cando **É predefinido = Non**. O rol cando **É predefinido = Si** úsase para avaliar a utilización do recurso fronte ao obxectivo para ese rol.

No separador **Project Service**, tamén pode configurar unha utilización obxectivo individual para o recurso. A seguir, o cálculo de utilización usa esa utilización obxectivo para avaliar o obxectivo do recurso no canto do obxectivo do rol predefinido do recurso.

A utilización móstrase para un recurso só se ese recurso ten un tempo imputable acordado durante o período que se amosa na grade.

## <a name="resource-availability"></a>Dispoñibilidade de recursos

É fundamental que os xestores de recursos poidan ver a dispoñibilidade de recursos e actualizar as reservas. Nalgúns casos, non hai unha demanda formal (solicitude de recursos), pero un xestor de recursos debe responder a unha demanda non planificada que chega por canles como un correo electrónico, chamada telefónica ou mensaxe instantánea. Os xestores de recursos usan o panel de programación para actualizar recursos e reservas.

As horas laborables do recurso serven como base para calcular a dispoñibilidade dun recurso. As reservas de recursos consumen a capacidade dos recursos.

O panel de programación usa cores e sombreados para amosar reservas, dispoñibilidade e saturacións, e tamén o estado das reservas. Un axuste da configuración do panel de programación permítelle mostrar unha lenda.

Se aparece unha frecha apuntando á dereita xunto a un recurso reservable individual no panel de programación, pódese ampliar o recurso para mostrar detalles do traballo no que está reservado o recurso.

Debido a que Dynamics 365 Project Operations usa o motor de Universal Resource Scheduling, se tamén ten Dynamics 365 Field Service instalado, pode ver os detalles das reservas de recursos para proxectos, pedidos de traballo e calquera outra entidade á que estendeu a programación.

Para ver máis detalles sobre un recurso individual, prema co botón dereito sobre el para abrir a tarxeta do recurso.

