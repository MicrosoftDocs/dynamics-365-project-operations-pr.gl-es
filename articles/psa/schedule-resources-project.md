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
ms.openlocfilehash: db69348aac96cbfaaa865228c9230cbda4b1e784
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076338"
---
# <a name="schedule-resources-for-a-project-project-service"></a><span data-ttu-id="70dc4-103">Programar recursos para un proxecto (Project Service)</span><span class="sxs-lookup"><span data-stu-id="70dc4-103">Schedule resources for a project (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="70dc4-104">Pode comprobar a dispoñibilidade de recursos para obter unha vista xeral de como están reservados os seus recursos, ou pode filtrar a visualización por cualificacións, equipo, localización e outras opcións.</span><span class="sxs-lookup"><span data-stu-id="70dc4-104">You can check resource availability to get an overall view of how booked your resources are, or you can filter the view by skills, team, location, and other options.</span></span>  
  
<span data-ttu-id="70dc4-105">O panel de programación mostra a lista de recursos e a súa dispoñibilidade.</span><span class="sxs-lookup"><span data-stu-id="70dc4-105">The schedule board shows list of resources and their availability.</span></span> <span data-ttu-id="70dc4-106">Seleccionar un modo de visualización para mostrar dispoñibilidade por **Horas** , **Día** , **Semana** ou **Mes**.</span><span class="sxs-lookup"><span data-stu-id="70dc4-106">Select a view mode to show availability by **Hours** , **Day** , **Week** , or **Month**.</span></span>  
  
<span data-ttu-id="70dc4-107">Antes de utilizar o panel de programación, é importante definilo.</span><span class="sxs-lookup"><span data-stu-id="70dc4-107">Before you use the schedule board, it’s important to set it up.</span></span> <span data-ttu-id="70dc4-108">Para obter máis información, consulte [Configurar o panel de programación (Field Service ou Project Service Automation)](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board).</span><span class="sxs-lookup"><span data-stu-id="70dc4-108">For more information, see [Configure the schedule board (Field Service or Project Service Automation)](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board).</span></span>
  
<span data-ttu-id="70dc4-109">Se está a usar unha versión máis antiga, para obter información sobre a dispoñibilidade de recursos, consulte [Ver dispoñibilidade de recursos](../psa/view-resource-availability.md).</span><span class="sxs-lookup"><span data-stu-id="70dc4-109">If you are using an older version, for resource availability, see [View resource availability](../psa/view-resource-availability.md).</span></span>  

> [!IMPORTANT]
>  <span data-ttu-id="70dc4-110">Para utilizar a funcionalidade de reserva do panel de programación, xeocodificación e servizos de localización, cómpre activar mapas.</span><span class="sxs-lookup"><span data-stu-id="70dc4-110">To use the schedule board booking functionality, geocoding, and location services, you need to turn on maps.</span></span>  
> 
> 1. <span data-ttu-id="70dc4-111">No menú principal, seleccione **Programación de recursos** > **Administración**.</span><span class="sxs-lookup"><span data-stu-id="70dc4-111">On the main menu, select **Resource Scheduling** > **Administration**.</span></span>  
> 2. <span data-ttu-id="70dc4-112">Prema **Parámetros de programación**.</span><span class="sxs-lookup"><span data-stu-id="70dc4-112">Click **Scheduling parameters**.</span></span>  
> 3. <span data-ttu-id="70dc4-113">Abra o rexistro e desprácese cara abaixo ata a sección **Resource Scheduling Optimization**.</span><span class="sxs-lookup"><span data-stu-id="70dc4-113">Open record and scroll down to the **Resource Scheduling Optimization** section.</span></span>  
> 4. <span data-ttu-id="70dc4-114">No campo **Conectar a asignacións** , escolla **Si**.</span><span class="sxs-lookup"><span data-stu-id="70dc4-114">On the **Connect to Maps** field, choose **Yes**.</span></span>  
> 5. <span data-ttu-id="70dc4-115">Acepte os termos e garde o rexistro.</span><span class="sxs-lookup"><span data-stu-id="70dc4-115">Accept terms and save the record.</span></span>  
> 6. <span data-ttu-id="70dc4-116">No menú principal, seleccione **Project Service** > **Panel de Programación**.</span><span class="sxs-lookup"><span data-stu-id="70dc4-116">On the main menu, select **Project Service** > **Schedule board**.</span></span> <span data-ttu-id="70dc4-117">Existen varias maneiras de programar manualmente un requisito de reserva.</span><span class="sxs-lookup"><span data-stu-id="70dc4-117">From here, there are several ways to manually schedule a booking requirement.</span></span> <span data-ttu-id="70dc4-118">Elixa o método que mellor lle convén.</span><span class="sxs-lookup"><span data-stu-id="70dc4-118">Choose the method that works for you.</span></span>
  
## <a name="find-available-resources"></a><span data-ttu-id="70dc4-119">Atopar recursos dispoñibles</span><span class="sxs-lookup"><span data-stu-id="70dc4-119">Find available resources</span></span>

1.  <span data-ttu-id="70dc4-120">Na lista de **Requisitos da reserva** , prema co botón secundario nunha reserva sen programar e escolla unha das seguintes opcións:</span><span class="sxs-lookup"><span data-stu-id="70dc4-120">From the **Booking Requirement** list, right-click an unscheduled booking and choose one of the following:</span></span>  
  
- <span data-ttu-id="70dc4-121">Elixa **Localizar dispoñibilidade-Recursos Actuais** para localizar un recurso dispoñible na lista do panel de programación.</span><span class="sxs-lookup"><span data-stu-id="70dc4-121">Choose **Find availability - Current Resources** to find an available resource from the list on the schedule board.</span></span>  
- <span data-ttu-id="70dc4-122">Elixa **Elixa Localizar dispoñibilidade-Todos os recursos** para localizar un recurso dispoñible nos recursos do sistema</span><span class="sxs-lookup"><span data-stu-id="70dc4-122">Choose **Find availability - All Resources** , to find an available resource from resources in the system</span></span>  
   > [!NOTE]
   >  <span data-ttu-id="70dc4-123">Ao facer isto, os filtros mostrarán opcións para o requirimento da reserva seleccionada.</span><span class="sxs-lookup"><span data-stu-id="70dc4-123">When you do this, the filters will show options for the selected booking requirement.</span></span>  
  
2. <span data-ttu-id="70dc4-124">Cando vexa un intervalo dispoñible, prema co botón secundario no intervalo de tempo do panel de programación e escolla **Reservar aquí**.</span><span class="sxs-lookup"><span data-stu-id="70dc4-124">When you see an available slot, right-click the time slot on the schedule board and choose **Book Here**.</span></span> <span data-ttu-id="70dc4-125">Tamén pode arrastrar e soltar o requirimento da reserva no intervalo de tempo dispoñible.</span><span class="sxs-lookup"><span data-stu-id="70dc4-125">Or, drag and drop the booking requirement to the available time slot.</span></span>  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a><span data-ttu-id="70dc4-126">Reservar un recurso utilizando a visualización diaria e buscar quen non está completamente reservado</span><span class="sxs-lookup"><span data-stu-id="70dc4-126">Book a resource using the daily view and find who’s under-booked</span></span>
  
1.  <span data-ttu-id="70dc4-127">No panel de programación, seleccione **Modo de Visualización** e seleccione **Días**.</span><span class="sxs-lookup"><span data-stu-id="70dc4-127">On the schedule board, select **View Mode** and select **Days**.</span></span>  
  
    <span data-ttu-id="70dc4-128">Mostra unha visualización de grade de cantas horas non está reservado un recursopor día e que días están libres.</span><span class="sxs-lookup"><span data-stu-id="70dc4-128">This shows a grid view of how many hours a resource is booked per day and which days they are free.</span></span>  
  
2.  <span data-ttu-id="70dc4-129">Prema no nome do recurso que desexa reservar e, a seguir, seleccione **Reservar**.</span><span class="sxs-lookup"><span data-stu-id="70dc4-129">Click the name of the resource you want to book, and then select **Book**.</span></span>  
  
3.  <span data-ttu-id="70dc4-130">Na caixa de diálogo **Reserva de Recurso (crear)** , escolla o proxecto para o que desexa reservar o recurso xunto co método de reserva e horas de inicio e fin.</span><span class="sxs-lookup"><span data-stu-id="70dc4-130">On the **Resource booking (create)** dialog box, choose the project that you want to book the resource for along with booking method and start and end times.</span></span>  
  
4.  <span data-ttu-id="70dc4-131">Cando finalice, seleccione **Reservar**.</span><span class="sxs-lookup"><span data-stu-id="70dc4-131">When you’re done, select **Book**.</span></span>  
  
## <a name="view-to-the-schedule-board"></a><span data-ttu-id="70dc4-132">Ver o panel de programación</span><span class="sxs-lookup"><span data-stu-id="70dc4-132">View to the schedule board</span></span>
  
1.  <span data-ttu-id="70dc4-133">Seleccione un requisito de reserva sen programar da lista na parte inferior.</span><span class="sxs-lookup"><span data-stu-id="70dc4-133">Select an unscheduled booking requirement from the list at the bottom.</span></span>  
  
2.  <span data-ttu-id="70dc4-134">Arrastre o requisito de reserva ata un intervalo de tempo ou recurso dispoñible no panel de programación.</span><span class="sxs-lookup"><span data-stu-id="70dc4-134">Drag the booking requirement to an available resource/time slot on the schedule board.</span></span>  
  
3.  <span data-ttu-id="70dc4-135">Cando finalice, seleccione **Reservar**.</span><span class="sxs-lookup"><span data-stu-id="70dc4-135">When you're done, select **Book**.</span></span>  
  
### <a name="additional-resources"></a><span data-ttu-id="70dc4-136">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="70dc4-136">Additional resources</span></span>  
 [<span data-ttu-id="70dc4-137">Guía do xestor de recursos</span><span class="sxs-lookup"><span data-stu-id="70dc4-137">Resource manager guide</span></span>](../psa/resource-manager-guide.md)
