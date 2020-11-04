---
title: Definir calendarios de proxectos
description: Este tema ofrece información sobre o uso dun calendario do proxecto para rastrexar a programación do proxecto.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 774399f2c02d8434c9c042c3a9f995792893bfce
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076306"
---
# <a name="define-project-calendars"></a>Definir calendarios de proxectos

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Para crear unha programación de proxecto, créase un modelo de calendario de proxecto que define o número de horas de traballo para adaptar por día na programación e os peches de empresa. Para crear un modelo de calendario de proxecto, asocie un modelo de traballo ao campo **Modelo de calendario** para o proxecto. Siga estes pasos para crear un modelo de traballo.

1. No panel de navegación esquerdo, seleccione **Recursos**. 
2. Na páxina de lista **Recursos** , abra un rexistro de usuario e, a seguir, seleccione **Mostrar horas laborables**.

  > [!NOTE]
  > Asegúrese de permitir ventás emerxentes na páxina do navegador. Isto permítelle ver as horas laborables establecidas para o recurso.
  
3. No separador **Vista mensual** , seleccione **Configurar**. Aparece unha lista de tres opcións: 

  - Nova programación semanal
  - Programación de traballo para un día
  - Tempo libre

4. Seleccione **Nova programación semanal** e logo configure as opcións para esta programación de recursos. Pode definir unha programación semanal recorrente, parámetros horarios diarios, peches de negocio e moito máis.
5. Estableza o intervalo de datas, seleccione **Gardar** e, a seguir, seleccione **Pechar**. 
6. Volva á páxina de lista **Recursos** e seleccione o recurso para o que estableceu as horas laborables. 
7. Seleccione **Establecer calendario como** para configurar o modelo de traballo. 
8. Na caixa de diálogo **Modelo de traballo** , introduza un nome para o modelo de traballo e, a seguir, seleccione **Aplicar**. 

Agora pode asociar o modelo de traballo a un modelo de calendario de proxecto.
