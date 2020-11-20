---
title: Visión xeral da conciliación de recursos
description: Este tema fornece información sobre garantir que as reservas e atribucións de recursos a proxectos estean aliñadas.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 574afac3bf5d1f6e5e13d8c61aa1ace6188f4008
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4125716"
---
# <a name="resource-reconciliation-overview"></a>Visión xeral da conciliación de recursos

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Para os membros do equipo, as reservas e atribucións están emparelladas libremente. Noutras palabras, os recursos poden ter atribucións pero sen reservas ou poden ter reservas pero sen atribucións. O ideal sería que as reservas e atribucións estivesen aliñadas, de xeito que os recursos teñan capacidade comprometida para realizar as atribucións de tarefas. Non obstante, as reservas poden estar baseadas na dispoñibilidade e os calendarios de tarefas poderían cambiar a medida que o proxecto continúe. Polo tanto, o emparellamento libre de reservas e atribucións proporciona flexibilidade.

O separador **Conciliación** do formulario **Proxecto** permite aos xestores de proxectos concilien as reservas dos membros do equipo e as súas atribucións para os equipos de proxecto.

O separador **Conciliación** tamén mostra reservas e atribucións ata o nivel da tarefa individual para cada membro do equipo. As horas móstranse en celas que representan períodos de tempo desde meses ata días.

O separador tamén mostra un total neto global do proxecto, xunto cunha columna **Total**.

Para cada recurso, o separador calcula a diferenza entre as reservas do membro do equipo e un resumo das atribucións do membro do equipo. O ideal sería que esta diferenza fose 0 (cero). Noutras palabras, non debería haber ningunha diferenza entre reservas e atribucións. As diferenzas están coloreadas e sombreadas para chamar a atención sobre dúas condicións:

- **Escaseza de reservas** - A escaseza de reservas prodúcese cando un recurso ten máis atribucións que reservas. Debido a que non se reservou esta capacidade, un xestor de proxectos podería querer corrixir esta condición ampliando as reservas do recurso para cubrir o déficit.
- **Exceso de reservas** - O exceso de reservas prodúcese cando se reservou un recurso para o proxecto pero non foi asignado a tarefas. Esta condición pode ser aceptable nos casos en que o recurso foi reservado para o proxecto antes de que se producise a atribución de tarefas. Non obstante, noutros casos, non está previsto atribuír tarefas ao recurso. Nestes casos, o xestor do proxecto debería considerar a cancelación das reservas do recurso, de xeito que a capacidade poida utilizarse para outro proxecto.

Nalgúns casos, cando ve o tempo a un nivel superior ao nivel de día (por exemplo, a nivel de mes), pode que vexa unha diferenza neta de cero para un recurso (noutras palabras, reservas = atribucións). Non obstante, se ve o tempo a nivel de semana, é posible que vexa que hai atribucións de cero horas e reservas de 40 horas na primeira semana, pero atribucións de 40 horas e reservas de cero horas na segunda semana. En xeral, as reservas e atribucións conciliaranse, pero difiren dunha semana a outra.

Cando vexa o tempo a niveis máis altos, as celas do separador **Conciliación** ten un indicador para informar de que hai diferenzas a niveis máis baixos. Ao premer dúas veces nunha cela, pode facer zoom para ver a diferenza. A seguir, pode premer co botón dereito para facer zoom. Ao seleccionar un recurso e despois usar o control **Seguinte diferenza** na barra de ferramentas da rede, pode ir á seguinte diferenza entre reservas e atribucións para ese recurso. Pode entón usar o control **Diferencia anterior** para volver. Tamén pode desactivar o indicador de diferenzas e o comportamento de navegación en **Configuración**.


Se ten atribucións de tarefas para un recurso pero non ten reservas, na páxina **Proxectos**, no separador **Conciliación**, seleccione a escaseza de reservas e logo seleccione **Estender a reserva**. Aparece a caixa de diálogo **Estender reserva** e mostra a reserva que é necesaria para resolver a escaseza do recurso. Tamén amosa as reservas existentes do recurso en todos os proxectos ou outras entidades programables. Se selecciona **Aceptar** para crear a reserva para o recurso, independentemente da dispoñibilidade dese recurso, pode causar un exceso de reservas.

O xestor de proxectos ou xestor de recursos pode utilizar o panel de programación para xestionar calquera situación na que un recurso estea sobrecargado fóra da súa capacidade.

