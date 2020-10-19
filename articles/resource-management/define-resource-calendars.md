---
title: Definir calendarios de recursos
description: Este tema ofrece información sobre como definir os calendarios de horas de traballo para recursos en Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: ab39d7e5dc2d8c01ed49ca0f1a4d1691aaf15637
ms.sourcegitcommit: 396e0fea2f1598a5313cb0128eca4fe0bb5aade9
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961860"
---
# <a name="define-resource-calendars"></a>Definir calendarios de recursos

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Cada recurso reservable que traballa nun proxecto debe ter un calendario de horas de traballo para definir a súa dispoñibilidade. As horas de traballo dun recurso pódense definir de dúas maneiras: 

   - Definir regras de calendario individuais para un recurso
   - Aplicar un modelo de calendario existente para o recurso

## <a name="define-a-resources-working-hours"></a>Definir as horas de traballo dun recurso

1. No menú **Recursos**, seleccione **Recursos**.
2. Na vista de grade, seleccione o **Recurso reservable** aplicable.
3. Na páxina **Detalles do recurso**, seleccione o separador **Horas de traballo**. Por defecto, o calendario de recursos reservables é o horario de traballo do modelo de horas de traballo por defecto definido para a organización.
4. Para actualizar as horas de traballo, prema co botón dereito na data de inicio da regra de calendario proposta que se definirá. Use o menú de regras de calendario para definir unha regra de calendario para un día específico, o resto da serie ou todo o calendario.
5. Despois de seleccionar a opción, pode definir:

    - O día da semana onde se aplicarán as horas de traballo.
    - As horas de traballo de cada día.
    - O fuso horario local da regra de calendario.
    - Se é o caso, tamén se pode especificar o tempo non laborable para a regra.

## <a name="applying-a-calendar-template-to-a-resource"></a>Aplicación dun modelo de calendario a un recurso

1. No menú **Recursos**, seleccione **Recursos**.
2. Na vista de grade, seleccione ata 25 **Recursos reservables** para actualizar.
3. Seleccione **Establecer calendario** e un diálogo solicitaralle unha lista de modelos de horas de traballo dispoñibles.
4. Seleccione o modelo que desexe usar e, a seguir, seleccione **Aplicar**.
