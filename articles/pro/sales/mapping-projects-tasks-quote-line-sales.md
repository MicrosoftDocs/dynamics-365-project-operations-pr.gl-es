---
title: Asignar proxectos e tarefas a unha liña de oferta baseada en proxecto
description: Este artigo ofrece información sobre como asignar proxectos e tarefas a unha liña de tarefas baseada en proxectos.
author: rumant
ms.date: 10/05/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 8971a334bd19f0ef106f88034a1abbb3c338de22
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917160"
---
# <a name="map-projects-and-tasks-to-a-project-based-quote-line"></a>Asignar proxectos e tarefas a unha liña de oferta baseada en proxecto

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Nas liñas de oferta baseada en proxecto, pode asignar as tarefas específicas dun proxecto que xa está asociado a unha liña de oferta.

Cando asigna tarefas a unha liña de oferta, os seguintes elementos que definiu na liña de oferta só se aplicarán a esas tarefas:

- Método de facturación
- Opcións de imputabilidade
- Límites non superables
- Clientes

Por exemplo, pode que teña un proxecto onde unha fase é de prezo fixo e as outras fases son de tempo e materiais. Neste caso, pode asociar a primeira fase e todas as tarefas secundarias á liña de oferta desa fase cun método de facturación de prezo fixo. Despois pode asociar todas as outras fases á liña de oferta baseada en tempo e materiais.

## <a name="associate-tasks-to-project-based-quote-lines"></a>Asociar tarefas a liñas de oferta baseada en proxecto

Pode asociar tarefas con liñas de oferta desde os seguintes lugares:

- Páxina **Proxecto** > separador **Facturación de tarefas** (óptima)
- Páxina **Liña de oferta** > separador **Tarefas imputables** 

### <a name="from-the-project-page"></a>Desde a páxina do proxecto.

A páxina **Proxecto** ofrece a experiencia óptima para asociar tarefas ás liñas de oferta. Podes usar esta páxina para seleccionar varias tarefas e asocialas todas, ademais das tarefas secundarias, á liña de oferta seleccionada.

1. No separador **Xeral** dunha liña de oferta baseada en proxecto, verifique que o campo **Proxecto** está cuberto.
2. No campo **Tarefas incluídas**, seleccione **Só tarefas seleccionadas**.
3. Garde a liña de oferta baseada en proxecto. Cando o formulario se actualiza, aparece o separador **Tarefas imputables**.
4. No separador **Xeral**, seleccione a ligazón para o proxecto desde o campo **Proxecto**.
5. Na páxina **Proxecto**, seleccione o separador **Facturación de tarefas**.
6. Na segunda grade, que se aplica á configuración de facturación específica da tarefa, seleccione unha ou máis tarefas e logo seleccione **Asociar liñas de oferta**.
7. Na páxina de diálogo que aparece, seleccione unha liña de oferta que mostre as liñas de oferta baseada en proxecto da oferta.
8. No campo **Tipo de facturación**, indique se estas tarefas son imputables ou non imputables.
9. Seleccione a caixa de verificación para indicar se a asociación debe incluír as tarefas secundarias das tarefas seleccionadas. Ao marcar a caixa asociaranse as tarefas secundarias das tarefas seleccionadas á liña de oferta.
10. Seleccione **Aceptar** para pechar a caixa de diálogo.

### <a name="from-the-quote-line-page"></a>Desde a páxina da liña de oferta

Pode asociar as tarefas do proxecto ás liñas de oferta desde o separador **Tarefas imputables** na páxina **Liña de oferta**.

>[!NOTE]
>O lugar ideal para asociar tarefas de proxecto a liñas de oferta está no separador **Facturación de tarefas** na páxina **Proxecto**. Se asocia as tarefas desde o separador **Tarefas imputables** na páxina **Liña de oferta**, debe asociar manualmente cada proxecto.

1. No separador **Xeral** dunha liña de oferta baseada en proxecto, verifique que hai un proxecto seleccionado no campo **Proxecto**.
2. No campo **Tarefas incluídas**, seleccione **Só tarefas seleccionadas**.
3. Garde a liña de oferta baseada en proxecto. Cando o formulario se actualiza, aparece o separador **Tarefas imputables**.
4. No separador **Tarefas imputables**, seleccione **Engadir unha tarefa de liña de oferta**.
5. Na páxina **Tarefa de liña de oferta**, no campo **Tarefas**, seleccione a tarefa e no campo **Tipo de facturación**, seleccione **Gardar**. 
6. Peche a páxina. A tarefa seleccionada agora está asociada á liña de oferta.

## <a name="disassociate-tasks-from-projectbased-quote-lines"></a>Desvincular tarefas das liñas de oferta baseada en proxecto

### <a name="from-the-project-page"></a>Desde a páxina do proxecto.

Este método ofrece a experiencia óptima para desvincular tarefas das liñas de oferta. Pode seleccionar varias tarefas e desvinculalas todas, ademais das tarefas secundarias, da liña de oferta seleccionada.

1. No separador **Xeral** dunha liña de oferta baseada en proxecto, no campo **Proxecto**, seleccione unha ligazón de proxecto.
2. Na páxina **Proxecto**, seleccione o separador **Facturación de tarefas**.
3. Na segunda grade, que se aplica á configuración de facturación específica da tarefa, seleccione unha ou máis tarefas e logo seleccione **Desvincular liñas de oferta**.
4. Na páxina de diálogo que aparece, seleccione unha liña de oferta.
5. Seleccione a caixa de verificación para indicar se a asociación debe eliminarse tamén das tarefas secundarias das tarefas seleccionadas. Ao marcar a caixa tamén se desvincularán as tarefas secundarias das tarefas seleccionadas á liña de oferta.
6. Seleccione **Aceptar**. Unha mensaxe de advertencia infórmalle de que se elimina esta asociación, poderíanse reverter os datos reais rexistrados previamente na tarefa. 
7. Seleccione **Aceptar** para continuar e eliminar a asociación entre a tarefa e a liña de oferta baseada en proxecto.

### <a name="from-the-quote-line-page"></a>Desde a páxina da liña de oferta

Tamén pode desvincular as tarefas do proxecto das liñas de oferta desde o separador **Tarefas imputables** na páxina **Liña de oferta**.

1. No separador **Tarefas imputables**, seleccione **Eliminar unha tarefa de liña de oferta**.
2. Seleccione **Aceptar**. Unha mensaxe de advertencia infórmalle de que se elimina esta asociación, poderíanse reverter os datos reais rexistrados previamente na tarefa. 
3. Seleccione **Aceptar** para continuar e eliminar a asociación entre a tarefa e a liña de oferta baseada en proxecto.

>[!NOTE]
> Este procedemento non elimina a tarefa do proxecto. Só elimina a asociación de tarefas da liña de oferta baseada en proxecto.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]