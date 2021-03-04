---
title: Crear un equipo de proxecto
description: Este tema fornece información sobre como crear e xestionar equipos de proxecto.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kdwns
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a7eb9101352afd27b527bf6b8acc6f92198f44ea
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076297"
---
# <a name="create-a-project-team"></a>Crear un equipo de proxecto

[!include [banner](../includes/banner.md)]

Para usar os roles que se configuraron previamente nun proxecto, un xestor de proxectos debe asociar os roles ao proxecto. Pódense asignar varios roles para un proxecto. Para evitar confusións, estas funcións etiquétanse automaticamente durante a reserva. Por exemplo, se o xestor de proxectos require tres enxeñeiros de software, tres roles de enxeñeiro de software que teñen **enxeñeiro de software 1** , **enxeñeiro de software 2** e **enxeñeiro de software 3** como etiquetas que se xeran automaticamente. Se previamente se definiron as características do rol, aplícanse como filtro durante as buscas dun recurso. Pódense engadir características adicionais segundo sexa necesario para mellorar a busca.

A configuración da visualización tamén se pode personalizar para visualizar mellor a dispoñibilidade de recursos. Hai opcións para amosar a dispoñibilidade horaria, diaria, semanal, mensual, trimestral e anual. Tamén hai unha opción para amosar a capacidade dispoñible e restante de recursos. Esta opción é útil para a xestión do tempo cando estima o tempo dispoñible para actividades ou a dispoñibilidade de recursos.

O xestor de proxectos pode seleccionar un rol na páxina e despois, se hai un recurso dispoñible que se axuste ao requisito, seleccionar reservar un recurso para cubrir o rol. Teña en conta que non ten que reservar os recursos neste momento da fase de planificación. Cando crea unha WBS, pode substituír roles por recursos de persoal para o proxecto. Se as funcións substitúense por recursos con persoal na WBS, a configuración de recursos actualiza automaticamente a listaxe e a programación do equipo do proxecto.

[![Listaxe do equipo do proxecto que inclúe roles e recursos reais](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

O xestor do proxecto ten varias opcións para reservar un recurso para un proxecto, como **Capacidade restante** , **Capacidade total** , **Porcentaxe de capacidade** e **Especificar horas**. Estas opcións de reserva pódense cancelar en calquera momento se cambian as atribucións de recursos. Admítense dous tipos de reserva:

- **Reserva dura** - Aprobouse e confirmouse a reserva de recursos para traballar no compromiso durante o tempo especificado.
- **Reserva branda** - A reserva de recursos estableceuse provisionalmente para traballar no compromiso durante o tempo especificado.

O seguinte procedemento explica como crear un equipo de proxecto:

## <a name="create-a-project-team"></a>Crear un equipo de proxecto

1. Na páxina de lista **Todos os proxectos** , seleccione un proxecto e logo seleccione **Editar**.
2. No separador **Equipo do proxecto e programación** , no campo **Data de finalización da programación** , introduza a data de inicio da programación máis un mes. Por exemplo, se a data de inicio da programación é o 24 de xuño de 2017 (24/06/2017), introduza **24/07/2017**.
3. Seleccione **Engadir**.
4. No panel **Engadir roles ao proxecto** , no campo **Rol** , seleccione **Xestor de proxectos principal**.
5. Seleccione **Competencias requiridas**.
6. Na páxina **Elixir características** , as características que configurou previamente para o rol de xestor de proxectos principal se seleccionan de xeito predefinido. Seleccione **Aceptar**.
7. Na páxina **Engadir funcións ao proxecto** , no campo **Número de recursos** , introduza **1**.
8. No campo **Recurso** , a busca mostra todos os recursos que teñen as competencias requiridas. Seleccione **Daniel Goldschmidt** e, a seguir, seleccione **Crear**.
9. Na páxina **Proxecto** , seleccione **Engadir**.
10. No panel **Engadir roles ao proxecto** , no campo **Rol** , seleccione **Membro do equipo**. No campo **Número de recursos** , introduza **5**.
11. Seleccione **Crear**.
12. Na páxina **Proxectos** , seleccione **Encher recurso**.

## <a name="monitor-project-teams"></a>Supervisar os equipos do proxecto
1. Na páxina **Todos os proxectos** , seleccione a ligazón **ID de proxecto** para o proxecto **Fase 2 de actualización de XYZ**.
2. No separador rápido **Equipo do proxecto e programación** , verifique que os recursos do proxecto que aparecen na lista son correctos.


[!INCLUDE[footer-include](../includes/footer-banner.md)]