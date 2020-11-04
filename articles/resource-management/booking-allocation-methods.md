---
title: Métodos de atribución de reservas
description: Este tema ofrece información sobre como funcionan os métodos de asignación de reservas en Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: c2a964c18c7eae61c5a0239da3b18da31b6ad574
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076082"
---
# <a name="booking-allocation-methods"></a>Métodos de atribución de reservas

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Tanto si engade un membro do equipo directamente a un proxecto no separador **Equipo** ou se reserva un recurso a un proxecto ou requisito no panel de programación, hai diferentes médotos de reserva de atribucións que pode utilizar. Este tema explica como funciona cada método e que tipo de método pode provocar saturación de recursos.

## <a name="booking-allocation-methods"></a>Métodos de atribución de reservas

Pode utilizar seis métodos de asignación de reservas:

- [Capacidade completa](#full)
- [Capacidade restante](#remaining)
- [Capacidade da porcentaxe](#percentage)
- [Horas de distribución uniforme](#evenly)
- [Horas da carga frontal](#front)
- [Ningún](#none)

### <a name="full-capacity"></a><a name="full"></a>Capacidade completa 
O método de Capacidade completa reserva a capacidade completa do recurso para as datas desde e ata especificadas. Por exemplo, se un recurso ten un calendario definido para traballar oito horas por día, cinco días por semana, definir unha data de inicio e de fin que cubra cinco días laborables reservará o recurso para 40 horas. A reserva faise independentemente da capacidade restante do recurso. Se un recurso xa está reservado durante ese período noutros proxectos, as horas 40 resérvanse como horas adicionais, o que pode provocar saturacións.

### <a name="remaining-capacity"></a><a name="remaining"></a>Capacidade restante
O método de capacidade restante só está dispoñible cando reserva directamente nun proxecto con panel de programación. Este método reserva a capacidade dispoñible do recurso dentro do rango de datas especificado. Por exemplo, se un recurso ten unha capacidade de 40 horas de traballo por semana e xa se reservou 10 horas, a reserva para a mesma semana ten como resultado a reserva das restantes 30 horas de capacidade para esa semana.

### <a name="percentage-capacity"></a><a name="percentage"></a>Capacidade da porcentaxe
O método de Capacidade porcentual reserva unha porcentaxe da capacidade do recurso para as datas desde e ata especificadas. Por exemplo, se un recurso ten un calendario definido para traballar oito horas por día, cinco días por semana, definir unha data de inicio e de fin que cubra cinco días laborables ao 50 % de capacidade reservará o recurso para 20 horas. As reservas individuais por día esténdense da mesma forma durante o período, por exemplo catro horas por día neste exemplo. A reserva faise independentemente da capacidade restante do recurso. Se o recurso xa está reservado durante ese período noutros proxectos, as horas 20 resérvanse como horas adicionais, o que pode provocar saturacións.

### <a name="evenly-distribute-hours"></a><a name="evenly"></a>Horas de distribución uniforme
O método de Distribuír uniformemente as horas reserva o recurso para un número de horas especificado, e distribúe o tempo de forma similar por día sobre as datas desde e ata especificadas. Por exemplo, se reserva un recurso para 20 horas durante un período de cinco días, este método distribúe as 20 horas uniformemente en catro horas por día. A reserva faise independentemente da capacidade restante do recurso. Se o recurso xa está reservado durante ese período noutros proxectos, as horas 20 resérvanse como horas adicionais, o que pode provocar saturacións.

### <a name="front-load-hours"></a><a name="front"></a>Horas da carga frontal
O método de Carga frontal de horas reserva o recurso para un número de horas especificado, con carga frontal das horas por día sobre as datas desde e ata especificadas. A carga frontal consume a capacidade dispoñible do recurso por orde "o primeiro consume primeiro". Por exemplo, se a programación do traballo do recurso é de oito horas por día, cinco días por semana, e non ten ningunha reserva actual, reservar o recurso por 20 horas durante un período de cinco días de traballo resulta no seguinte padrón de reserva diaria: 

|                           |    Día 1    |    Día 2    |    Día 3    |    Día 4    |    Día 5    |    Total    |
|---------------------------|-------------|-------------|-------------|-------------|-------------|-------------|
|    **Reservas existentes**    |    0        |    0        |    0        |    0        |    0        |    0        |
|    **Nova reserva**          |    8        |    8        |    4        |    0        |    0        |    20       |

O método de carga frontal considera as reservas existentes e a capacidade dispoñible. Por exemplo, se o mesmo recurso xa ten horas 20 de reservas en semana laboral, as novas reservas consumen a capacidade restante da seguinte maneira:

|                     | Día 1 | Día 2 | Día 3 | Día 4 | Día 5 | Total |
|---------------------|-------|-------|-------|-------|-------|-------|
| **Reservas existentes** | 8     | 8     | 4     | 0     | 0     | 20    |
| **Nova reserva**       | 0     | 0     | 4     | 8     | 8     | 20    |

Debido a que xa considerou a capacidade dispoñible, é posible que reciba unha mensaxe de erro se o recurso non ten capacidade restante pode que poida absorber a reserva. Con este método, non é posible a saturación.

### <a name="none"></a><a name="none"></a>Ningún
O método Ningún só está dispoñible cando reserva do separador **Equipo** dentro dun proxecto. Este método engade o recurso como membro do equipo ao proxecto, pero non crea ningunha reserva que absorba a capacidade do recurso. Este método úsase cando se engade o membro do equipo xestor de proxecto predefinido ao crear un proxecto. O usuario xestor de proxecto que creou o proxecto engádese por defecto ao proxecto, de forma que o rexistro da entidade de proxecto ten un propietario e hai un aprobador no proxecto. Debido a que este usuario non ten ningunha reserva, se desexa reservar o recurso pode eliminalo e, a seguir, volver a engadilo utilizando un método de atribución diferente, ou engadir o recurso a tarefas e, a seguir, utilizar **Estender reservas** no separador **Conciliación** para crear reservas para as atribucións.

## <a name="allocation-methods-that-lead-to-overbooking"></a>Métodos de atribución que provocan saturación
En resumen, os seguintes métodos de atribución conducen a saturación se o recurso xa está comprometido noutros projects (ou para outros pedidos de traballo ou entidades programables):

- Capacidade completa
- Capacidade da porcentaxe
- Horas de distribución uniforme

Ao utilizar un destes tres métodos de atribución, non será notificado de que o recurso está saturado. Para corrixir a saturación, ten que utilizar o panel de programación.
