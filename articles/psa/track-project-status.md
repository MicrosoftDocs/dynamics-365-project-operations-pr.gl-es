---
title: Rastrexar o estado dun proxecto
description: Como rastrexar o estado dun proxecto en Project Service
author: ruhercul
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
ms.openlocfilehash: 70d07c98bd9432712e939445dbf867b96642f5ba
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076218"
---
# <a name="track-a-projects-status-project-service"></a>Rastrexar o estado dun proxecto (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Utilice a [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] para rastrexar o progreso do proxecto dun cliente.  

A medida que o compromiso progresa, as fases do proxecto actualízanse para reflectir a fase do compromiso:  


|              |                                                                                                                                                                                                                                                                                                  |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   **Novo**    | Ao crear un proxecto, a fase está definida en **Nova**. Se creou o proxecto a partir dun modelo, nesta fase o proxecto pode ter unha programación, estimacións e datos de equipo. En caso contrario, será o esquema do proxecto e terá que introducir o resto dos compoñentes do proxecto manualmente. |
|  **Oferta**   |      Cando asocia un proxecto a unha oferta ou crea un proxecto a partir dunha oferta, a fase de proxecto está definida en **Oferta** , e as datas de inicio e fin estimadas tamén se actualizan. Cando o proxecto está en fase de oferta, móstranse detalles da oferta no separador **Sales** na páxina **Proxecto**.      |
|   **Planificar**   |                                     Cando gaña unha oferta asociada a un proxecto, e cando o compromiso progresa á fase de contrato, a fase de proxecto actualízase a **Planificar**. A información do contrato aparece no separador **Sales** na páxina **Proxecto**.                                      |
| **Completada** |                    Cando conclúa o traballo de proxecto, pode cambiar a fase a **Concluído**. Cando a fase de proxecto está definida en concluído, enténdese que o traballo está o 100% concluído pero o proxecto queda aberto para entradas de tempo ou gastos pendentes de ser rexistradas.                     |
|  **Pechar**   |           Cando todas as transaccións están rexistradas no proxecto e non espera máis, pode manualmente configurar a fase a **Pechar**. Cando o proxecto está definido como **Pechar** , non pode rexistrar máis transaccións no proxecto e o proxecto será só de lectura.           |

## <a name="to-track-a-projects-status"></a>Para rastrexar o estado dun proxecto  

1.  Vaia a **Project Service > Proxectos**.  

2.  Prema no proxecto no que quere traballar.  

3.  Na barra da parte superior da pantalla, seleccione a frecha cara abaixo ao lado do nome do proxecto e, a seguir, prema **Rastrexar proxecto**.  

4.  Seleccione **Rastrexo de esforzo** ou **Rastrexo de custo** na lista despregable enriba da lista de tarefas.  

5.  Prema dúas veces nunha tarefa para editala. Tamén pode mover ou redimensionar as barras na gráfica Gantt para modificar a hora e o progreso dunha tarefa.  

### <a name="see-also"></a>Consulte tamén  
 [Guía do xestor de proxectos](../psa/project-manager-guide.md)
