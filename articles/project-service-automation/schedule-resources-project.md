---
title: Programar recursos para un proxecto
description: Como programar recursos para un proxecto en Project Service
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 4935567d-9318-4f7c-9c02-c584a78b7841
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: d9767e324b3caec4b5f9723347537dbe97ea34fb
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751459"
---
# <a name="schedule-resources-for-a-project-project-service"></a>Programar recursos para un proxecto (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Pode comprobar a dispoñibilidade de recursos para obter unha vista xeral de como están reservados os seus recursos, ou pode filtrar a visualización por cualificacións, equipo, localización e outras opcións.  
  
O panel de programación mostra a lista de recursos e a súa dispoñibilidade. Seleccionar un modo de visualización para mostrar dispoñibilidade por **Horas**, **Día**, **Semana** ou **Mes**.  
  
Antes de utilizar o panel de programación, é importante definilo. Para obter máis información, consulte [Configurar o panel de programación (Field Service ou Project Service Automation)](../field-service/configure-schedule-board.md).
  
Se está a usar unha versión máis antiga, para obter información sobre a dispoñibilidade de recursos, consulte [Ver dispoñibilidade de recursos](../project-service/view-resource-availability.md).  

> [!IMPORTANT]
>  Para utilizar a funcionalidade de reserva do panel de programación, xeocodificación e servizos de localización, cómpre activar mapas.  
> 
> 1. No menú principal, seleccione **Programación de recursos** > **Administración**.  
> 2. Prema **Parámetros de programación**.  
> 3. Abra o rexistro e desprácese cara abaixo ata a sección **Resource Scheduling Optimization**.  
> 4. No campo **Conectar a asignacións**, escolla **Si**.  
> 5. Acepte os termos e garde o rexistro.  
> 6. No menú principal, seleccione **Project Service** > **Panel de Programación**. Existen varias maneiras de programar manualmente un requisito de reserva. Elixa o método que mellor lle convén.
  
## <a name="find-available-resources"></a>Atopar recursos dispoñibles

1.  Na lista de **Requisitos da reserva**, prema co botón secundario nunha reserva sen programar e escolla unha das seguintes opcións:  
  
- Elixa **Localizar dispoñibilidade-Recursos Actuais** para localizar un recurso dispoñible na lista do panel de programación.  
- Elixa **Elixa Localizar dispoñibilidade-Todos os recursos** para localizar un recurso dispoñible nos recursos do sistema  
   > [!NOTE]
   >  Ao facer isto, os filtros mostrarán opcións para o requirimento da reserva seleccionada.  
  
2. Cando vexa un intervalo dispoñible, prema co botón secundario no intervalo de tempo do panel de programación e escolla **Reservar aquí**. Tamén pode arrastrar e soltar o requirimento da reserva no intervalo de tempo dispoñible.  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a>Reservar un recurso utilizando a visualización diaria e buscar quen non está completamente reservado
  
1.  No panel de programación, seleccione **Modo de Visualización** e seleccione **Días**.  
  
    Mostra unha visualización de grade de cantas horas non está reservado un recursopor día e que días están libres.  
  
2.  Prema no nome do recurso que desexa reservar e, a seguir, seleccione **Reservar**.  
  
3.  Na caixa de diálogo **Reserva de Recurso (crear)**, escolla o proxecto para o que desexa reservar o recurso xunto co método de reserva e horas de inicio e fin.  
  
4.  Cando finalice, seleccione **Reservar**.  
  
## <a name="view-to-the-schedule-board"></a>Ver o panel de programación
  
1.  Seleccione un requisito de reserva sen programar da lista na parte inferior.  
  
2.  Arrastre o requisito de reserva ata un intervalo de tempo ou recurso dispoñible no panel de programación.  
  
3.  Cando finalice, seleccione **Reservar**.  
  
### <a name="additional-resources"></a>Recursos adicionais  
 [Guía do xestor de recursos](../project-service/resource-manager-guide.md)
