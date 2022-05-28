---
title: Liñas de oportunidade baseadas en proxecto
description: Este tema ofrece información sobre como traballar con liñas de oportunidade baseadas en proxecto.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: cceb175210f7b597d682e9e4e910c79280211293
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600924"
---
# <a name="project-based-opportunity-lines"></a>Liñas de oportunidade baseadas en proxecto

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_


As liñas de oportunidade baseada en proxecto só están dispoñibles en oportunidades baseadas en proxecto. Os rexistros de oportunidade baseada en proxecto teñen o campo **Tipo** definido como **Baseado en traballo**.

As liñas de oportunidade baseada en proxecto son os elementos de liña que se entregarán ao cliente mediante un proxecto. Non obstante, un proxecto non pode estar ligado a unha liña de oportunidade baseada en proxecto. Os proxectos pódense vincular a elementos de liña da fase **Oferta** en adiante porque normalmente a oportunidade ocorre nunha fase inicial dun acordo. A determinación de cantos proxectos se empregarán para entregar o traballo ao cliente é unha decisión que se toma máis tarde na fase de vendas. Use a fase de oportunidade para identificar os compoñentes de entrega discreta para o cliente. As decisións sobre o número real de proxectos empregados para entregar estes compoñentes pódense aprazar ata que se coñeza máis información sobre o traballo en si.

Abaixo amósanse os campos dunha liña de oportunidade baseada en proxecto:

| **Campo** | **Localización** | **Descrición** | **Impacto descendente** |
| --- | --- | --- | --- |
| Tipo de produto | Separador Xeral (oculto) | Este é un campo de conxunto de opcións. Se ten instalado Dynamics 365 Operations, unha das opcións dispoñibles é **Servizo baseado en proxecto**.  | O valor deste campo establécese en **Servizo baseado en proxecto** cando crea a liña de oportunidade baseada en proxecto desde a grade de liñas baseadas en proxecto na Oportunidade. <br> Se cambia ou anula este valor, a funcionalidade do proxecto non se activará nos seus elementos de liña baseada en proxecto. |
| Oportunidade | Separador Xeral | Este campo é de só lectura e fai referencia ao rexistro principal de Oportunidade ao que pertence este elemento de liña. | Non hai ningún impacto descendente deste campo. |
| Nome | Separador Xeral | Este é un campo de texto editable que se pode usar para dar unha identidade curta a esta elemento de liña | Este valor transfírese á liña de oferta cando cree unha oferta a partir desta oportunidade |
| Orzamento do cliente | Separador Xeral | Este campo de moeda editable pode usarse para rastrexar o importe que o cliente está disposto a gastar para este elemento de liña. | Este valor transfírese ao campo correspondente da liña de oferta cando cree unha oferta a partir desta oportunidade |
| Método de facturación | Separador Xeral | Este campo editable ten os seguintes valores posibles:</br>- Tempo e material</br>- Prezo fixo | Este valor transfírese ao campo correspondente da liña de oferta cando cree unha oferta a partir desta oportunidade. Despois de crear a liña de oferta, o campo bloquéase e non se pode cambiar. Atribúa este valor de campo coa maior precisión posible. Se precisa cambiar o valor deste campo na liña de oferta, elimine e cree de novo a liña de oferta. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]