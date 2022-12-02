---
title: Eliminar unha estimación de proxecto
description: Este artigo ofrece información sobre como eliminar unha estimación do proxecto unha vez finalizado.
author: Yowelle
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: de54659f9e69daf1566f86bec16436c19eeacf49
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932202"
---
# <a name="eliminate-a-project-estimate"></a>Eliminar unha estimación de proxecto

[!include [banner](../includes/banner.md)]

As estimacións de proxecto fornecen a visualización financeira para o traballo estimado e programado para un proxecto. Para traballar con estimacións dun proxecto, debe anexalo a un proxecto de estimación. Un proxecto de estimación baséase sempre nun proxecto existente, pero moitos proxectos poden referirse a un único proxecto de estimación. Só se poden anexar proxectos de prezo fixo e de investimento para estimar proxectos, e estes proxectos deben pertencer ao mesmo grupo de proxectos que o proxecto de estimación.

Para eliminar un proxecto de estimación, debe estar completo. Os seguintes pasos explican como eliminar unha estimación.

1. Vaia a **Xestión e contabilidade de proxectos** > **Todos os proxectos** e abra o proxecto. 
2. No separador **Xestionar**, seleccione **Estimacións** e na páxina **Estimación** seleccione **Eliminar**.
3. Na páxina **Eliminar estimación** no separador **Xeral**, configure as seguintes opcións:

   - **Código do período**: Seleccione o código do período para escoller os proxectos de estimación axeitados. 
   - **Data da estimación**: Seleccione a data da estimación axeitada para a eliminación.
   - **Eliminar con advertencias de WIP**: Active esta opción para proporcionar unha notificación cando se elimine unha estimación asociada a un traballo en curso (WIP). Cando esta opción non está activada, a eliminación non pode continuar se existen transaccións non estimadas. 
   > [!NOTE]
   > Esta opción só está dispoñible cando se aplica a eliminación a un proxecto de estimación. Non está dispoñible se está a usar anotacións periódicas. Esta configuración funciona coa configuración do separador **Estimación** na páxina **Parámetros do proxecto**, no grupo de campos **Permitir a eliminación cando existen transaccións non estimadas**.
   - **Establecer a fase como Finalizada**: Active esta opción para establecer a fase do proxecto de estimación en **Finalizada** despois de executar a eliminación.
   - **Imprimir lista de estimacións**: Seleccione a información que se incluirá cando se imprima a lista de estimacións.
   - **Mostrar Infolog**: Active esta opción para amosar o Infolog.
   - **Data de contabilización**: Elixa a data de contabilización no libro maior da estimación.

4.  Seleccione **Aceptar**.
5. Despois de completar o proceso de eliminación, o proxecto de estimación eliminado móstrase cun valor negativo. 

Se non pretendía eliminar unha estimación, pode seleccionar a estimación eliminada e seleccionar **Inverter eliminación**.   


[!INCLUDE[footer-include](../includes/footer-banner.md)]