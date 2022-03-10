---
title: Modelos de proxecto
description: Este tema fornece información sobre como usar modelos de proxecto para a configuración rápida do proxecto.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 34df8ed9a8baff949097af1b95da56bfe9a4240c213896fafd5c7dcfcf580b6c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7002509"
---
# <a name="project-templates"></a>Modelos de proxecto 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Un modelo de proxecto é un marco predefinido que axuda a iniciar con rapidez e facilidade un proxecto. Pode usar un modelo predefinido para crear un novo proxecto cun só clic. En canto aos proxectos, debe definir os requisitos previos para os modelos de proxectos. Debe definir un calendario de proxecto para cada modelo de proxecto, e os roles e listas de prezos deben ser predefinidos na organización, de xeito que os compoñentes do modelo teñan datos útiles.

Un modelo de proxecto consta de tres compoñentes: un calendario, estimacións do proxecto e membros do equipo do proxecto.

## <a name="schedule"></a>Programar

Unha programación nun modelo de proxecto ten o mesmo conxunto de elementos que unha programación nun proxecto. Pode crear unha xerarquía de tarefas, asociar roles a tarefas, definir atributos de programación e definir dependencias. Unha programación nun modelo de proxecto tamén admite modos de tarefas para cada tarefa. Polo tanto, admite o motor de programación. Debe asociar un calendario de proxecto ao proxecto. Ao crear unha programación de traballo, non hai ningunha diferenza entre un modelo de proxecto e un proxecto.

## <a name="project-estimates"></a>Estimacións do proxecto

As estimacións dun proxecto nun modelo de proxecto funcionan da mesma forma que as estimacións dun proxecto. Non obstante, os custos e os prezos de venda extráense das listas de prezos e custos por defecto que se definen nos parámetros.

## <a name="creating-a-project-from-a-template"></a>Creación dun proxecto a partir dun modelo
 
Hai varios xeitos de crear un proxecto a partir dun modelo de proxecto:

- Ao crear un proxecto desde unha oferta, pode seleccionar un modelo de proxecto na caixa de diálogo **Creación rápida: Proxecto**.

> ![Caixa de diálogo Creación rápida: Proxecto.](media/project-11.png)

- Cando cree un proxecto seleccionando **Novo proxecto**, a páxina **Proxecto** aparece antes de gardar o rexistro. No campo **Escoller un modelo**, seleccione un dos modelos de proxecto predefinidos na organización.
- Use **Crear proxecto a partir dun modelo** na páxina **Entidade de modelo**.

## <a name="copying-components-of-template-to-project"></a>Copiar compoñentes do modelo a un proxecto

Cando copia os compoñentes dun modelo de proxecto nun proxecto, poden ocorrer algunhas anulacións, dependendo da configuración do proxecto.

### <a name="copying-the-schedule"></a>Copiar a programación

Ao copiar a programación a partir dun modelo de proxecto, se o proxecto ten un calendario de proxecto diferente ao do modelo, as horas de traballo do calendario do proxecto aplicaranse á programación de tarefas. Deste xeito, a programación axústase segundo o calendario de respaldo do proxecto. De forma similar, a primeira tarefa na programación colle a data de inicio do proxecto, e a programación do resto da xerarquía actualízase segundo a duración e as dependencias especificadas no modelo. 

### <a name="copying-project-estimates"></a>Copiar estimacións do proxecto 

Cando copia entre liñas de estimación do proxecto, as listas de prezos actualízanse. Para a lista de prezos de custos, estas actualizacións baséanse na unidade propietaria do proxecto. Para a lista de prezos de vendas, baséanse no cliente. Para proxectos que están asociados a unha entidade de vendas, o custo unitario e os prezos de vendas determínanse segundo estas listas de prezos.

### <a name="copying-a-project-team"></a>Copiar un equipo de proxecto

Ao copiar o equipo de proxecto a partir do modelo de proxecto, os recursos xenéricos está tamén se copian, xunto cos coñecementos e habilidades definidos no modelo. As atribucións de recursos xenéricas tamén se manteñen igual que no modelo de proxecto. Os recursos nomeados non son compatibles cos modelos de proxecto.


[!INCLUDE[footer-include](../includes/footer-banner.md)]