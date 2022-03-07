---
title: Integración de Microsoft Project Client
description: Planificar e manter un programa de proxectos pode ser complexo, polo que os xestores de proxectos precisan empregar ferramentas que os axuden a xestionar esta tarefa. A integración con Microsoft Project Client proporciona apoio para abrir e xestionar unha estrutura de subdivisión do traballo do proxecto.
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 8ef34bc984510f23ab77cc1710c06abbcf80f721703685d696fea28eeaddd732
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988019"
---
# <a name="microsoft-project-client-integration"></a>Integración de Microsoft Project Client

[!include [banner](../includes/banner.md)]

Planificar e manter un programa de proxectos pode ser complexo, polo que os xestores de proxectos precisan empregar ferramentas que os axuden a xestionar esta tarefa. A integración con Microsoft Project Client proporciona apoio para abrir e xestionar unha estrutura de subdivisión do traballo do proxecto. O xestor do proxecto pode publicar os cambios de novo na estrutura de subdivisión do traballo do proxecto de Dynamics 365 Finance.

> [!NOTE]
> Se está a usar a actualización de xullo (versión 10.0.4), debe instalar KB 4054797 e 4055884.

## <a name="configure-the-microsoft-project-client-add-in"></a>Configurar o suplemento Microsoft Project Client
Para activar a integración con Microsoft Project Client, é necesario instalar o suplemento Microsoft Dynamics 365 na aplicación Microsoft Project do cliente do usuario. Isto faise abrindo o **espazo de traballo de xestión de proxectos**.

• Prema **Configurar o suplemento do cliente do proxecto** desde a sección **Ligazóns** > **Configuración** da área de traballo.

• Prema **Abrir** e, a seguir, prema **Executar** cando se lle solicite.

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a>Abrir e editar un borrador de estrutura de subdivisión do traballo existente en Microsoft Project Client
Se un proxecto en Dynamics 365 Finance xa ten unha estrutura de subdivisión do traballo creada, a estrutura de subdivisión do traballo pódese abrir na aplicación Microsoft Project Client se a estrutura de subdivisión de traballo está nun estado de borrador. Para abrir desde a páxina **Proxecto**, prema a ligazón **Abrir en Microsoft Project** desde o separador **Planificar**. Esta páxina tamén se pode abrir desde a aplicación Microsoft Project Client premendo **Abrir** no separador **Microsoft Dynamics 365**. Seleccione **Persoa xurídica** e **Proxecto** na lista.

> [!NOTE]
> Se está a usar Internet Explorer como explorador, terá que premer **Gardar** para abrir manualmente desde a localización á que se descargou o ficheiro. Ou prema **Gardar e abrir** para abrir o ficheiro en Microsoft Project Client. Non cambie o nome do ficheiro cando o garde.

Antes de facer ningunha edición no ficheiro usando Microsoft Project Client, debe comprobalo. Prema **Comprobar** no separador **Microsoft Dynamics 365**. Isto evitará que outros usuarios editen a estrutura de subdivisión do traballo desde Finanzas ao mesmo tempo. Para publicar a estrutura de subdivisión do traballo despois de completar as edicións, prema **Rexistrar** no separador **Microsoft Dynamics 365**.

Se un equipo do proxecto xa se engadiu ao proxecto en Finanzas, a lista de recursos encherase cos membros do equipo. Se aínda non se engadiu un equipo de proxecto ao proxecto, pode seleccionar recursos e crear o equipo dentro de Microsoft Project Client premendo o botón **Recursos** no separador **Microsoft Dynamics 365**. 

Os seguintes datos sincronizaranse de novo con Finanzas como parte do proceso de rexistro:

•   Nome da tarefa

•   Data de inicio

•   Data de finalización

•   Predecesores

•   Nomes de recursos

•   Categoría

•   Categoría do recurso

•   Horas laborables

•   Notas

•   Prioridade

> [!NOTE]
> Se engade outras columnas ao seu ficheiro de Microsoft Project Client, non se gardarán no ficheiro e non se amosarán cando se abra de novo o ficheiro.

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Crear a estrutura de subdivisión do traballo para un proxecto existente usando Microsoft Project Client
Para crear unha nova estrutura de subdivisión do traballo usando Microsoft Project Client, siga estes pasos:


1.  Abra Microsoft Project Client.

2.  No separador **Microsoft Dynamics 365**, prema **Abrir**.

3.  Seleccione a **Persoa xurídica** para o proxecto.

4.  Seleccione o **Proxecto**.

5.  Prema **Consultar** no separ **Microsoft Dynamics 365**.

6.  Cando estea listo para publicalo en Finanzas, prema **Rexistrar** no separador **Microsoft Dynamics 365**.

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Substituír a estrutura de subdivisión do traballo existente para un proxecto existente usando Microsoft Project Client
Para crear unha nova estrutura de subdivisión do traballo usando Microsoft Project Client e substituír unha estrutura de subdivisión do traballo existente por un proxecto existente, siga estes pasos:

1.  Abra Microsoft Project Client.

2.  Crear o programa en Microsoft Project Client.

3.  No separador **Microsoft Dynamics 365**, prema **Gardar cambios** > **Substituír o proxecto existente**.

4.  Seleccione a **Persoa xurídica** para o proxecto.

5.  Seleccione o **Proxecto**.

6.  Prema **Aceptar**.

## <a name="create-a-new-project-from-within-microsoft-project-client"></a>Crear un novo proxecto desde dentro de Microsoft Project Client


1.  Abra Microsoft Project Client.

2.  Crear o programa en Microsoft Project Client.

3.  No separador **Microsoft Dynamics 365**, prema **Gardar cambios** > **Gardar a novo proxecto**.

4.  Seleccione a **Persoa xurídica** para o proxecto.

5.  Introduza o **ID do proxecto**, se é necesario.

6.  Introduza o **nome de proxecto**.

7.  Seleccione o **Tipo de proxecto**, **Grupo do proxecto** e o **ID do contrato do proxecto**. Como alternativa, pode crear un novo contrato de proxecto premendo **Novo**.

8.  Seleccione o **Calendario** que se usará para os recursos.

11. Prema en **Aceptar**.

> [!NOTE]
> O complemento Project Client non admite os seguintes caracteres no formato de ID do proxecto:
> 
>   - Guión baixo
>   - Punto
>   - Barra espazadora
>   - Barra

[!INCLUDE[footer-include](../includes/footer-banner.md)]
