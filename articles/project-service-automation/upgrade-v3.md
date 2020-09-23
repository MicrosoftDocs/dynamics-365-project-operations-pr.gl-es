---
title: Consideracións sobre a actualización - Microsoft Dynamics 365 Project Service Automation versión 2.x ou 1.x a versión 3
description: Este tema proporciona información sobre as consideracións que debe ter en conta ao actualizar da versión 2.x ou 1.x á versión 3 de Project Service Automation.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 11/13/2018
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 3.x
author: JohnPBurrows
ms.assetid: e4fae2ea-9013-488e-a666-f7192dd42c0b
ms.author: john.burrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: ba710eb8c07df7dac97e8b911184c00b87b14548
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751420"
---
# <a name="upgrade-considerations---psa-version-2x-or-1x-to-version-3"></a>Consideracións sobre a actualización - PSA versión 2.x ou 1.x a versión 3
[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="project-service-automation-and-field-service"></a>Project Service Automation e Field service
Tanto Dynamics 365 Project Service Automation como Dynamics 365 Field Service usan a solución Universal Resourcing Scheduling (URS) para a planificación de recursos. Se ten na súa instancia tanto Project Service Automation como Field Service, debe planificar a actualización de ambas solucións á versión máis recente (versión 3.x para Project Service Automation, versión 8.x para Field Service). A actualización de Project Service Automation e Field Service instalará a última versión de URS, o que significa que é posible un comportamento incoherente se as solucións Project Service Automation e Field Service da mesma instancia non se actualizan á última versión.

## <a name="resource-assignments"></a>Atribucións de recursos
En Project Service Automation versión 2 e versión 1, as tarefas almacenábanse como tarefas secundarias (tamén chamadas tarefas de liña) na **Entidade tarefa**, e indirectamente relacionadas coa entidade **Atribución de recursos**. A tarefa de liña era visible na ventá emerxente de atribución en Work Breakdown Structure (WBS).

![Tarefas de liña no WBS en Project Service Automation versión 2 e versión 1](media/upgrade-line-task-01.png)

Na versión 3 de Project Service Automation, o esquema subxacente de atribución de recursos reservables a tarefas cambiou. A tarefa de liña quedou desfasada e hai unha relación directa 1:1 entre a tarefa no **Entidade tarefa** e o membro do equipo na entidade **Atribución de recursos**. As tarefas atribuídas a un membro do equipo de proxecto agora almacénanse directamente na entidade Atribución de recursos.  

Estes cambios afectan á actualización de calquera proxecto existente que teña atribucións de recursos para recursos reservables nomeados e recursos xenéricos nun equipo de proxecto. Este tema ofrece as consideracións que terá que ter en conta para os seus proxectos cando actualice á versión 3. 

### <a name="tasks-assigned-to-named-resources"></a>Tarefas atribuídas a recursos nomeados
Ao usar a entidade de tarefas subxacente, as tarefas da versión 2 e a versión 1 permitían aos membros do equipo retratar un rol distinto do seu rol definido por defecto. Por exemplo, a Beatriz Fervenza, a quen por defecto se atribuíu o rol de xestor de programas, podería atribuírselle unha tarefa co rol de programador. Na versión 3, o rol dun membro nomeado é sempre o predefinido, polo que calquera tarefa que se lle atribúa a Beatriz Fervenza usa o seu rol predefinido de xestor de programas.

Se atribuíu un recurso a unha tarefa fóra do seu rol predefinido na versión 2 e na versión 1, ao actualizar, atribuirase ao recurso nomeado o rol predefinido para todas as atribucións de tarefas, independentemente da atribución de roles na versión 2. Isto producirá diferenzas nas estimacións calculadas da versión 2 ou a versión 1 á versión 3 porque as estimacións calcúlanse en función do rol do recurso e non da atribución de tarefas de liña. Por exemplo, na versión 2, atribuíronse dúas tarefas a Rita Caramés. O rol na tarefa de liña para a tarefa 1 é programador e para a tarefa 2, xestor de programas. Rita Caramés ten o rol predefinido como xestor de programas.

![Varios roles atribuídos a un recurso](media/upgrade-multiple-roles-02.png)

Debido a que os roles do programador e do xestor de programas son diferentes, as estimacións de custos e vendas son as seguintes:

![Estimacións de custos dos roles de recursos](media/upggrade-cost-estimates-03.png)

![Estimacións de vendas dos roles de recursos](media/upgrade-sales-estimates-04.png)

Cando actualice á versión 3, as tarefas de liña substitúense por atribucións de recursos na tarefa do membro do equipo de recursos reservable. A atribución empregará o rol predefinido do recurso reservable. No seguinte gráfico, Rita Caramés, que ten un rol de xestor de programas, é o recurso.

![Atribucións de recursos](media/resource-assignment-v2-05.png)

Debido a que as estimacións están baseadas no rol predefinido do recurso, as estimacións de vendas e custos poden cambiar. Teña en conta que no seguinte gráfico xa non ve o rol **Programador** porque o rol se toma do rol predefinido do recurso reservable.

![Estimacións de custos dos roles predefinidos](media/resource-assignment-cost-estimate-06.png)
![Estimación de vendas dos roles predefinidos](media/resource-assignment-sales-estimate-07.png)

Despois de completar a actualización, pode editar o rol dun membro do equipo para que sexa distinto do asignado por defecto. Non obstante, se cambia un rol dos membros do equipo, cambiarase en todas as súas tarefas atribuídas porque aos membros do equipo xa non se lles poden atribuír varios roles na versión 3.

![Actualización dun rol de recurso](media/resource-role-assignment-08.png)

Isto tamén é válido para as tarefas de liña atribuídas a recursos nomeados cando cambia a unidade organizativa predefinida do recurso a outra unidade organizativa. Despois de completar a actualización da versión 3, a atribución empregará a unidade organizativa predefinida do recurso en lugar da fixada na tarefa de liña.

### <a name="tasks-assigned-to-generic-resources"></a>Tarefas atribuídas a recursos xenéricos
Na versión 2 e na versión 1, pode configurar o rol e a unidade organizativa para unha tarefa e logo usar a funcionalidade **Xerar equipo** para xerar recursos xenéricos en función dos atributos establecidos na tarefa. Na versión 3, vostede crea os membros do equipo xenérico con rol e unidade organizativa, e despois atribúe aos membros do equipo a tarefas.

Na versión 2 e na versión 1, os proxectos con recursos xenéricos poden estar en dous estados ou unha mestura de ambos a nivel de tarefa. Por exemplo, pode ter os seguintes escenarios:

- Tarefas con roles e unidades organizativas establecidas, pero non se xerou ningunha atribución de recursos afiliados.
- Tarefas coas atribucións de recursos de membros xenéricos do equipo atribuídas mediante a creación de recursos xenéricos utilizando a funcionalidade **Xerar equipo**.

Antes de comezar a actualización, recomendamos que xere de novo o equipo para cada proxecto que teña tarefas atribuídas a recursos xenéricos ou que aínda teña que executar o proceso de xeración do equipo.

Para tarefas atribuídas a membros do equipo xenérico que se xeraron con **Xerar equipo**, a actualización deixará o recurso xenérico no equipo e deixará a atribución a ese membro do equipo xenérico. Recomendamos que xere o requisito de recurso para o membro xenérico do equipo despois da actualización, pero antes de reservar ou enviar unha solicitude de recurso. Isto conservará as tarefas de unidades organizativas nos membros xenéricos do equipo que sexan diferentes da unidade organizativa contratante do proxecto.

Por exemplo, no proxecto Project Z, a unidade organizativa de contratación é Contoso US. No plan do proxecto, as tarefas de proba dentro da fase de implantación foron atribuídas co rol de consultor técnico e a unidade organizativa atribuída é Contoso India.

![Atribución da organización na fase de implantación](media/org-unit-assignment-09.png)

Despois da fase de implantación, a tarefa de proba de integración está atribuída ao rol de asesor técnico, pero o organización está definida en Contoso US.  

![Atribución de organización da tarefa de proba de integración](media/org-unit-generate-team-10.png)

Cando se xera un equipo para o proxecto, créanse dous membros xenéricos do equipo debido ás diferentes unidades organizativas nas tarefas. Atribuiranse ao asesor técnico 1 as tarefas de Contoso India e o consultor técnico 2 terá as tarefas de Contoso EUA.  

![Membros xenéricos do equipo xerados](media/org-unit-assignments-multiple-resources-11.png)

> [!NOTE]
> En Project Service Automation versión 2 e versión 1, o membro do equipo non mantén a unidade organizativa, que se mantén na tarefa de liña.

![Tarefas de liña en Project Service Automation versión 2 e versión 1](media/line-tasks-12.png)

Pode ver a unidade organizativa na vista de estimacións. 

![Estimacións da unidade organizativa](media/org-unit-estimates-view-13.png)
 
Cando a actualización está completa, a unidade organizativa da tarefa de liña que corresponde ao membro xenérico do equipo engádese ao membro xenérico do equipo e elimínase a tarefa de liña. Por iso recomendamos que antes de actualizar, xere ou xere de novo o equipo en cada proxecto que conteña recursos xenéricos.

Para tarefas atribuídas a un rol cunha unidade organizativa que difira da unidade organizativa do proxecto de contratación e non se xerou un equipo, a actualización creará un membro xenérico do equipo para o rol, pero usará a unidade de contratación do proxecto para a unidade organizativa do membro do equipo. Volvendo ao exemplo co Proxecto Z, isto significa que a unidade organizativa contratante Contoso EUA e as tarefas de proba do plan de proxecto dentro da fase de implantación foron atribuídas ao rol de asesor técnico e coa unidade organizativa atribuída a Contoso India. A tarefa de proba de integración que se completa despois da fase de implantación foi atribuída ao rol de asesor técnico. A unidade organizativa é Contoso EUA e non se xerou un equipo. A actualización creará un membro xenérico do equipo, un asesor técnico que teña as horas atribuídas das tres tarefas e unha unidade organizativa de Contoso EUA, a unidade organizativa contratante do proxecto.   
 
O cambio das diferentes unidades organizativas de recursos predefinidas en membros do equipo non xerados é o motivo polo que recomendamos que xere ou volva xerar o equipo en cada proxecto que conteña recursos xenéricos antes da actualización para que non se perdan as atribucións de unidades organizativas.

