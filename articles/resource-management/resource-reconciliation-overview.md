---
title: Visión xeral da conciliación de recursos
description: Este artigo ofrece información que o axudará a garantir que as reservas de recursos e as atribucións para proxectos estean aliñadas.
author: ruhercul
ms.date: 01/08/2021
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: eaad9187f08be810d730f5a8ca6411ecee85bbc4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926314"
---
# <a name="resource-reconciliation-overview"></a>Visión xeral da conciliación de recursos

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Para os membros do equipo, as reservas e atribucións están emparelladas libremente. Noutras palabras, os recursos poden ter atribucións e sen reservas ou poden ter reservas e sen atribucións. O ideal sería que as reservas e atribucións estivesen aliñadas, de xeito que os recursos teñan capacidade comprometida para realizar as atribucións de tarefas. Non obstante, as reservas poden estar baseadas na dispoñibilidade e os calendarios de tarefas poderían cambiar a medida que o proxecto continúe. Polo tanto, o emparellamento libre de reservas e atribucións proporciona flexibilidade.

O separador **Conciliación** da páxina **Proxectos** permite aos xestores de proxectos concilien as reservas dos membros do equipo e as súas atribucións para os equipos de proxecto.

O separador **Conciliación** mostra reservas e atribucións ata o nivel da tarefa individual para cada membro do equipo. As horas amósanse en celas que representan períodos de tempo desde meses ata días. O separador tamén mostra un total neto global do proxecto, xunto cunha columna **Total**.

Para cada recurso, o separador **Conciliación** calcula a diferenza entre as reservas do membro do equipo e un resumo das atribucións do membro do equipo. O ideal sería que esta diferenza fose 0 (cero). Noutras palabras, non debería haber ningunha diferenza entre reservas e atribucións. As diferenzas están coloreadas e sombreadas para chamar a atención sobre dúas condicións:

- **Escaseza de reservas** - A escaseza de reservas prodúcese cando un recurso ten máis atribucións que reservas. Debido a que non se reservou a capacidade, o xestor de proxectos podería querer corrixir esta condición ampliando as reservas do recurso para cubrir o déficit.
- **Exceso de reservas** - O exceso de reservas prodúcese cando se reservou un recurso para o proxecto pero non foi asignado a tarefas. Esta condición pode ser aceptable nos casos en que o recurso foi reservado para o proxecto antes de que se producise a atribución de tarefas. Non obstante, noutros casos, onde non hai ningún plan para atribuír o recurso a tarefas, o xestor do proxecto debería considerar a posibilidade de cancelar as reservas do recurso. Deste xeito, a capacidade pode usarse para outro proxecto.

Nalgúns casos, cando ve o tempo a un nivel superior ao nivel de día (por exemplo, a nivel de mes), pode que vexa unha diferenza neta de cero para un recurso (noutras palabras, reservas é igual a atribucións). Non obstante, se ve o tempo a nivel de semana, é posible que vexa que hai atribucións de cero horas e reservas de 40 horas na primeira semana, pero atribucións de 40 horas e reservas de cero horas na segunda semana. En xeral, as reservas e atribucións conciliaranse, pero difiren dunha semana a outra.

Cando vexa o tempo a niveis máis altos, as celas no separador **Conciliación** ten un indicador para informar de que hai diferenzas a niveis máis baixos. Ao premer dúas veces nunha cela, pode facer zoom para ver a diferenza. A seguir, pode seleccionar e manter premido (ou premer o botón dereito) para facer zoom. Ao seleccionar un recurso e despois usar o control **Seguinte diferenza** na barra de ferramentas da rede, pode ir á seguinte diferenza entre reservas e atribucións para ese recurso. Pode entón usar o control **Diferencia anterior** para volver. Tamén pode desactivar o indicador de diferenzas e o comportamento de navegación en **Configuración**.

Se ten atribucións de tarefas para un recurso pero non ten reservas, seleccione a escaseza de reservas e logo seleccione o separador **Conciliación** da páxina **Proxectos** e logo seleccione **Estender a reserva**. A caixa de diálogo **Estender reserva** que aparece mostra a reserva que é necesaria para resolver a escaseza do recurso. A caixa de diálogo tamén amosa as reservas existentes do recurso en todos os proxectos ou outras entidades programables. Se selecciona **Aceptar** para crear a reserva para o recurso, independentemente da dispoñibilidade dese recurso, pode causar un exceso de reservas.

As reservas que se crean a través da acción **Estender reserva** está asociada ao requisito principal do proxecto. Cando se inicia unha extensión, non se pode determinar o requisito específico que debe estenderse, porque o recurso pode estar asociado a máis dun requisito para o proxecto.

O xestor de proxectos ou xestor de recursos pode utilizar o panel de programación para xestionar calquera situación na que un recurso estea sobrecargado fóra da súa capacidade.


[!INCLUDE[footer-include](../includes/footer-banner.md)]