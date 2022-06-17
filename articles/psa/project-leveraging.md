---
title: Proxectos e estimacións de vendas
description: Este artigo ofrece información sobre como aproveitar a programación e as estimacións no proceso de vendas.
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 957c2337cce3b3bf65a0bfef7c1aee6a730971fc
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925394"
---
# <a name="sales-estimates-and-projects"></a>Proxectos e estimacións de vendas

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Durante o proceso de vendas, pode crear estimacións de vendas ligando un proxecto a unha oferta de vendas. Deste xeito, pode producirse unha estimación determinista durante o proceso de vendas, para aproveitar as capacidades de programación e estimación de proxectos. Se a venda continúa, pódese empregar a programación que se empregou con fins de estimación de vendas como base para o refinamento adicional do plan do proxecto.

## <a name="linking-a-project-to-a-quote-line"></a>Ligar un proxecto a unha liña de oferta

Cando crea unha liña de oferta baseada en proxectos, pode crear un proxecto novo ou asociar un proxecto existente na páxina **Liña de oferta**. 

> ![Formulario de liña de oferta.](media/project-8.png)
 
Cando crea un novo proxecto a partir dos detalles da liña de oferta, pode aproveitar os modelos de proxecto. Os modelos de proxectos son proxectos modelo que representan plans de proxecto estándar e estimacións financeiras típicas dunha organización. Tamén poden representar copias de plans de proxectos e estimacións de proxectos pasados.

> ![Detalles da liña da oferta.](media/project-9.png)
  
Cando cree o proxecto desde unha oferta, o proxecto asóciase automaticamente á liña de oferta.

## <a name="components-of-estimates-in-a-project"></a>Compoñentes das estimacións nun proxecto

Unha programación permítelle dividir o traballo en tarefas, manter unha xerarquía de tarefas, determinar que recursos son necesarios para completar unha tarefa e atribuír unha estimación do esforzo que se require para completar unha tarefa.

Pode definir o esforzo de traballo e programar estimacións mediante os campos do separador **Programación** da páxina **Proxecto**. Debido a que unha lista de prezos está asociada ao proxecto, as estimacións financeiras calcúlanse mediante os prezos de custos e vendas definidos na lista de prezos.

## <a name="importing-estimates-from-a-project-into-a-quote"></a>Importación de estimacións dun proxecto a unha oferta

Despois de definir as estimacións do proxecto, pode importalas na liña de oferta. Na páxina **Detalles de liña de oferta**, seleccione **Importación das estimacións** na fita para resumir as estimacións do proxecto por tipo de transacción, rol ou nivel de tarefa.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
