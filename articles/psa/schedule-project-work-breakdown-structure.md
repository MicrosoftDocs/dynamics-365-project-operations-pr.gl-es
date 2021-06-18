---
title: Programar un proxecto coa estrutura de subdivisión do traballo
description: Como programar un proxecto coa estrutura de subdivisión do traballo (Project Service)
author: ruhercul
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
ms.openlocfilehash: 027bcbc8995ed39af78c7ff9b1028f401c3b0d4d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008579"
---
# <a name="schedule-a-project-with-a-work-breakdown-structure-project-service"></a>Programar un proxecto coa estrutura de subdivisión do traballo (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Unha programación de proxecto communica que traballo é necesario levar a cabo, que recursos van realizar o traballo e o intervalo temporal que se precisa para concluír o traballo. A programación de proxecto reflicte todo o traballo asociado coa entrega do proxecto a tempo. Un dos primeiros pasos da fase de inicio do proxecto é facer unha programación de proxecto. Para establecer unha programación de proxecto, ten que crear unha estrutura de subdivisión de traballo.  
  
 Crear unha estrutura de proxecto cunha estrutura de subdivisión de traballo, axuda a:  
  
- Dividir o traballo en tarefas manexables  
  
- Estimar o tempo necesario para finalizar unha tarefa  
  
- Definir as dependencias de tarefa e duración de tarefa  
  
- Determinar os roles necesarios para completar cada tarefa  
  
  A programación de proxecto na estrutura de subdivisión do traballo ten unha aparencia familiar, así como unha gráfica interactiva de Gantt.  
  
## <a name="create-a-work-breakdown-structure-for-a-project"></a>Crear unha estrutura de subdivisión do traballo para un proxecto  
 Cree unha estrutura de subdivisión do traballo para representar a secuencia de tarefas nun proxecto. A estrutura de subdivisión do traballo inclúe tarefas, requirimentos para cada tarefa e a información de ingresos e custos. Na estrutura de subdivisión do traballo, pode engadir:  
  
-   A secuencia de tarefas nunha xerarquía  
  
-   Outras tarefas que debe completar para poder iniciar unha tarefa  
  
-   A data inicial, a data final, e a duración dunha tarefa  
  
-   O número de horas necesarias para unha tarefa  
  
-   Os coñecementos e educación necesarios para un traballador  
  
-   Os traballadores que están atribuídos a unha tarefa  
  
-   Os ingresos e custos estimados  
  
## <a name="task-types"></a>Tipos de tarefa  
Usará os seguintes tipos de tarefas ao crear a estrutura de subdivisión do traballo:  

| | | 
|---------------------------------------|-----------------------------------------------------------------| 
| **Nó de raíz de proxecto** | Tarefa de resumo de nivel superior para o proxecto. Todas as outras tarefas de proxecto créanse nela. O nome da tarefa de raíz é o nome de proxecto. O esforzo, as datas e a duración do nó de raíz están baseados nos valores na xerarquía de abaixo. Non se poden editar os nós de propiedades ou eliminar o nó de raíz. | 
| **Tarefas de resumo ou contedor** | Unha tarefa de resumo é unha tarefa con subtarefas. Unha tarefa de resumo non ten un esforzo de traballo ou custo propio. O esforzo de traballo e o custo son un resumo das subtarefas. Pode modificar o nome dunha tarefa de resumo, mais non pode cambiar o esforzo, as datas ou a duración, porque eses calcúlanse automaticamente. Ao eliminar unha tarefa de resumo elimínase a tarefa e todas as subtarefas.|  
| **Tarefas de nó folla** | As tarefas nó follas representan o traballo máis detallado no proxecto. Ten un esforzo estimado, varios recursos planificados, datas de inicio e fin planificadas e unha duración.|

  
## <a name="task-hierarchy"></a>Xerarquía de tarefas  
 Ten as seguintes opcións ao crear unha xerarquía de tarefa:  
  
- **Engadir tarefa**.   Pode engadir unha tarefa nunha posición que escolla na xerarquía de tarefa. Se non selecciona unha posición, a nova tarefa aparece no fin.  
  
- **Aplicar sangría á tarefa**.   Aplicar sangría a unha tarefa para torna a que está enriba secundaria.  
  
- **Eliminar sangría dunha tarefa**   Elimine a sangría dunha tarefa para facer para que deixe de ser unha subtarefa da súa tarefa primaria orixinal.  
  
- **Mover para arriba e mover para abaixo**.   Mova tarefas arriba ou abaixo na xerarquía da tarefa primaria. Mover unha tarefa arriba ou baixo non ten efecto no seu esforzo, custo, datas ou duración.  
  
## <a name="task-attributes"></a>Atributos de lista  
 O nome dunha tarefa describe o traballo que precisa ser concluído. Pode utilizar varios atributos de tarefas para describir a programación e os requirimentos de persoal para a tarefa.  
  
### <a name="schedule-attributes"></a>Programar atributos

 - Atribuír valores a **Horas de esforzo**, **Número de recursos**, **Data de Inicio**, **Data de Fin** e **Duración** para determinar a programación para a tarefa. 
 - **Esforzo** é a estimación de horas que leva concluír a tarefa.
 - **Número de recursos** é unha estimación que o xestor de proxecto pon na tarefa para axudar a crear a mellor programación posible. 
 - **Duración** (en días) indica o número de días laborables que levará concluír a tarefa.  
  
### <a name="staffing-attributes"></a>Atributos de persoal

 - **Rol**, **Unidade da organización de recursos**, **Número de recursos** e **Recursos** describen os requisitos de persoal da tarefa. 
 - **Rol** describe o tipo de recurso necesario para realizar a tarefa. 
 - **Unidade de organización de recursos** indica a unidade da organización da que vén o persoal dos recursos para esa tarefa; isto tamén afecta a estiamción de vendas e custo, xa que se ten en conta para determinar o prezo de venda da unidade para o recurso. 
 - **Recursos** mantén un recurso xenérico ou un recurso con nome cando se atopa un.  
  
## <a name="task-dependencies"></a>Dependencias de tarefa  
 Pode crear relacións de predecesor entre unha ou varias tarefas na estrutura de subdivisión de traballo. Pode definir un ou máis valores para o campo predecesor nas tarefas para indicar as tarefas das que dependerá. Cando atribúe un valor predecesor a unha tarefa, a tarefa só pode iniciarse cando todas as tarefas predecesoras conclúan. Definir este dependencia nunha tarefa levará a recalcular a data de inicio planificada da tarefa como o último fin de todos os predecesores. Os impactos relacionados cos predecesores nunha programación non están limitados polo modo de tarefa definido na tarefa.  
  
## <a name="task-mode"></a>Modo de tarefa  
 O modo de tarefa é unha dos factores importante que determinan tarefas de nó folla de programación. Hai dous modos de tarefa para cada tarefa: modo automático e modo de programación manual.  
  
-   **Programación automática**.   Cando establece o modo de tarefa a Programada automaticamente, o motor de programación de tarefas usa as regras de programación nos seguintes atributos de tarefa para determinar a programación para a tarefa:  
  
    -   Predecesores  
  
    -   Esforzo  
  
    -   Número de recursos  
  
    -   Datas de inicio e de fin  
  
-   **Regras de programación**.   A data de inicio dunha tarefa de nó folla que non teña predecesores ten por defecto a data de inicio da programación do proxecto. A duración dunha tarefa de nó folla calcúlase sempre como o número de días laborables entre as datas de inicio e fin. Cando unha tarefa automaticamente está programada, o motor de programación segue as regras seguintes:  
  
    -   As datas de inicio e fin dunha tarefa sempre deben ser días laborables segundo o calendario de programación do proxecto  
  
    -   A data de inicio dunha tarefa que teña predecesores ten por defecto a última data de fin dos seus predecesores  
  
    -   Esforzo = Número de persoas * Duración * horas nun día laborable estándar do calendario de proxecto  
  
-   **Programación manual**.   Nalgúns casos, é posible que desexe afastarse destas regras. Nestes casos, pode definir que o modo de tarefas para a tarefa se programe manualmente. Isto fai que o motor de programación non calcule os valores para outros atributos de programación. Configurar os predecesores nas tarefas sempre afecta a data de comezo da tarefa dependente.  
  
## <a name="create-a-work-breakdown-structure"></a>Crear unha estrutura de subdivisión do traballo  
  
1.  Vaia a **Project Service > Proxectos**.  
  
2.  Prema no proxecto no que quere traballar.  
  
3.  Na barra da parte superior da pantalla, seleccione a frecha cara abaixo ao lado do nome do proxecto e, a seguir, prema Estrutura de subdivisión do traballo.  
  
4.  Para engadir unha tarefa, prema **Engadir Tarefa**. Complete os campos para a tarefa e, a seguir, prema en **Gardar**.  
  
5.  Continúe a engadir tarefas até que conclúa a estrutura de subdivisión do traballo. Ao crear a estrutura de subdivisión do traballo, pode realizar o seguinte para organizar as súas tarefas:  
  
    -   Seleccione unha tarefa e prema **Aplicar sangría** para movela a outra tarefa ou prema Eliminar sangría para movela un nivel.  
  
    -   Seleccione unha tarefa e prema **Mover para arriba** ou **Mover para abaixo** para movela cara arriba ou cara a abaixo na lista.  
  
    -   Prema **Ocultar Gantt** para ocultar a gráfica de Gantt e prema **Mostrar Gantt** para mostrala de novo.  
  
    -   Seleccione outro período de tempo para a gráfica de Gantt en **Escala de Tempo**.  
  
6.  Para engadir os roles especificados na estrutura de subdivisión do traballo aos membros do equipo do proxecto, prema **Xerar equipo de proxecto**.  
  
7.  Prema **Gardar** na parte inferior dereita da pantalla cando remate as modificacións.  
  
### <a name="see-also"></a>Consulte tamén  
 [Guía do xestor de proxectos](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]