---
title: Programar recursos para un proxecto
description: Como programar recursos para un proxecto en Project Service
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: f3b7ea1a2b81b86bedc85b77689145ba5afb579d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583122"
---
# <a name="schedule-resources-for-a-project-project-service"></a>Programar recursos para un proxecto (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Pode comprobar a dispoñibilidade de recursos para obter unha vista xeral de como están reservados os seus recursos, ou pode filtrar a visualización por cualificacións, equipo, localización e outras opcións.  
  
O panel de programación mostra a lista de recursos e a súa dispoñibilidade. Seleccionar un modo de visualización para mostrar dispoñibilidade por **Horas**, **Día**, **Semana** ou **Mes**.  
  
Antes de utilizar o panel de programación, é importante definilo. Para obter máis información, consulte [Configurar o panel de programación (Field Service ou Project Service Automation)](/dynamics365/field-service/configure-schedule-board).
  
Se está a usar unha versión máis antiga, para obter información sobre a dispoñibilidade de recursos, consulte [Ver dispoñibilidade de recursos](../psa/view-resource-availability.md).  

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
 [Guía do xestor de recursos](../psa/resource-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
