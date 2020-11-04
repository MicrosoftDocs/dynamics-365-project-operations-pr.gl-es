---
title: Configuración de proxecto
description: Neste tema se proporciona información sobre a configuración de xestión de proxectos.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: c9b8659f3b7ee81d2e21ef52743debd521fa9bb9
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076295"
---
# <a name="project-settings"></a>Configuración de proxecto

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Use os seguintes axustes para acceder ás funcións de planificación de proxectos.

## <a name="work-template"></a>Modelo de traballo

Para crear unha programación de proxecto, créase un modelo de calendario de proxecto que define o número de horas de traballo para adaptar por día na programación e os peches de empresa. Para crear un modelo de calendario de proxecto, asocie un modelo de traballo ao campo **Modelo de calendario** para o proxecto. Siga estes pasos para crear un modelo de traballo.

1. En PSA, no panel de navegación esquerdo, prema **Recursos**. 
2. Na páxina de lista **Recursos** , abra un rexistro de usuario e, a seguir, seleccione **Mostrar horas laborables**.

  > [!NOTE]
  > Asegúrese de permitir ventás emerxentes na páxina do navegador. Isto permítelle ver as horas laborables establecidas para o recurso.
  
3. No separador **Vista mensual** , prema **Configurar**. Aparece unha lista de tres opcións: 

  - Nova programación semanal
  - Programación de traballo para un día
  - Tempo libre

> ![Configurar opcións](media/project-13.png)

4. Seleccione **Nova programación semanal** e logo configure as opcións para esta programación de recursos. Pode definir unha programación semanal recorrente, parámetros horarios diarios, peches de negocio e moito máis.
5. Estableza o intervalo de datas, seleccione **Gardar** e, a seguir, prema **Pechar**. 
6. Volva á páxina de lista **Recursos** e seleccione o recurso para o que estableceu as horas laborables. 
7. Seleccione **Establecer calendario como** para configurar o modelo de traballo. 
8. Na caixa de diálogo **Modelo de traballo** , introduza un nome para o modelo de traballo e, a seguir, seleccione **Aplicar**. 

Agora pode asociar o modelo de traballo a un modelo de calendario de proxecto.

## <a name="resource-roles"></a>Roles do recurso

O termo *rol de recurso* refírese a un conxunto de habilidades, competencias e certificacións que unha persoa debe ter para realizar un conxunto específico de tarefas nun proxecto. PSA permítelle determinar o custo e facturar o tempo dun recurso en función do rol ao que estea asociado o recurso. Cada organización debe configurar estes roles empregando a navegación á esquerda no menú de **Project Service**.

Cada organización debe configurar estes roles na páxina **Categorías de recurso activas**. Para abrir esta páxina, no panel de navegación da esquerda, seleccione **Roles de recursos**.

## <a name="price-lists"></a>Listas de prezos

As listas de prezos permítenlle establecer o custo e os prezos de vendas para roles de recursos, categorías de gasto, produtos e outros elementos dunha organización. Antes de establecer estimacións financeiras para o traballo que se deben entregar para un proxecto, debería crear unha lista de custos e prezos de vendas de seguridade. Na sección de parámetros, tamén debe configurar unha lista de custos e prezos de vendas predefinida que se aplica a todos os proxectos creados na organización. Na páxina **Parámetros do proxecto activos** , asegúrese de configurar unha lista de prezos de vendas e custos predefinida.
