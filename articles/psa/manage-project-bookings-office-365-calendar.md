---
title: Xestionar proxectos e reservas no seu calendario de Office 365
description: Como xestionar proxectos e reservas no seu calendario de Office 365
author: ruhercul
manager: kfend
ms.service: project-operations
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
- D365PS
- ProjectOperations
ms.openlocfilehash: 1df4864ca8dbf6948ca88a7c82a6c0a676e3bd53
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275041"
---
# <a name="manage-projects-and-bookings-in-your-calendar-project-service"></a>Xestionar proxectos e reservas no seu calendario (Project Service)

> [!Note]
> DESFASADO: Esta funcionalidade está en desuso e xa non está dispoñible.

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 

Ver os compromisos persoais, as reservas de traballo nos proxectos e as atribucións de pedidos de traballo de Field Service usando o calendario de [!INCLUDE[pn_office_365](../includes/pn-office-365.md)].  
  
 Con todo nun só lugar, é fácil xestionar o día. As reunións, compromisos, reservas e tarefas están dispoñibles no seu calendario de [!INCLUDE[pn_office_365](../includes/pn-office-365.md)].  
  
 Se está a usar [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], tamén pode introducir os compromisos persoais na visualización de entrada de tempo de Project Service Isto permite que os xestores de proxectos e recursos saiban a súa dispoñibilidade para proxectos. Tamén aforra tempo porque non ten que introducir información sobre os seus compromisos persoais dúas veces. Pode importar os compromisos persoais desde calendario á visualización de entrada de tempo en Project Service.  
  
 O calendario sincronizará as reservas de pedidos de traballo e proxecto a partir de hoxe e durante as próximas catro semanas. Esta configuración non se pode modificar.  
  
 A sincronización só se admite dunha forma, de PSA ao calendario de [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]. Pode sincronizar na orde inversa. 
  
 Para obter infomación sobre como utilizar o seu calendario de [!INCLUDE[pn_office_365](../includes/pn-office-365.md)], consulte [Calendario de Outlook na web para empresas](https://support.office.com/article/Calendar-in-Outlook-on-the-web-for-business-5219c457-d1fe-4c2f-9032-1a816b88e936).  
  
## <a name="setup"></a>Configuración  
 Antes de poder ver e xestionar as súas reservas no seu calendario de [!INCLUDE[pn_office_365](../includes/pn-office-365.md)], debe configurar algunhas cousas.  
  
- Deberá ter credenciais de administrador global ou administrador do sistema de [!INCLUDE[pn_office_365](../includes/pn-office-365.md)].  
  
- O seu administrador terá que configurar o perfil de servidor de correo electrónico e cada usuario deberá configurar a súa caixa de correo. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Configurar o procesamento de correo electrónico a través da sincronización no servidor](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/admin/set-up-server-side-synchronization-of-email-appointments-contacts-and-tasks)  
  
## <a name="turn-on-synchronization-for-your-organization-admin-task"></a>Activar a sincronización para a súa organización (tarefa de administrador)  
  
1.  No menú principal, prema en **Configuración** > **Administración**.  
  
2.  Prema **Configuración do sistema**.  
  
3.  Prema o separador **Sincronización**.  
  
4.  En **Seleccione se desexa activar a sincronización da reserva de recursos con**, marque **Sincronizar a reserva de recursos con Outlook**.  
  
## <a name="turn-on-synchronization-for-your-user-profile-user-task"></a>Activar a sincronización para o seu perfil de usuario (tarefa de usuario)  
  
1.  Prema o botón **Configuración**  na esquina superior dereita da pantalla.  
  
2.  Prema **Opcións**.  
  
3.  Prema o separador **Sincronización**.  
  
4.  En **Sincronización da reserva de recursos con Outlook**, marque **Sincronización da reserva de recursos con Outlook**.  
  
## <a name="import-your-personal-appointments-user-task"></a>Importar os seus compromisos persoais (tarefa de usuario)  
 Pode importar os compromisos persoais desde calendario á visualización de entrada de tempo en Project Service Automation.  
  
1. Abra o calendario de [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] e prema **Importar datos**.  
  
2. Na pantalla de Filtros, seleccione **Compromisos de Exchange** e, a seguir, prema en **Aplicar**.  
  
3. O sistema extraerá compromisos na visualización de entrada de tempo como entradas suxeridas na semana actual. Para engadir entradas noutra semana, prema **Anterior** ou **Seguinte**.  
  
4. Seleccione o compromiso que desexe engadir á visualización de entrada de tempo en Project Service Automation.  
  
5. Na caixa emerxente **Entrada de tempo**, seleccione as opcións apropiadas para converter o compromiso nunha visualización de entrada de tempo en Project Service Automation.  
  
6. Prema **Gardar**.  
  
### <a name="see-also"></a>Consulte tamén  
 [Guía de tempo, gasto e colaboración](../psa/time-expense-collaboration-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]