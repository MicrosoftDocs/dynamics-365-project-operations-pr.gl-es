---
title: Liñas de oportunidade baseada en proxecto - lite
description: Este artigo ofrece información sobre liñas de oportunidade baseadas en proxectos. (Pro)
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 8b5a8fc32ca903d7da2e090137bed358b364902a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914262"
---
# <a name="project-based-opportunity-lines---lite"></a>Liñas de oportunidade baseada en proxecto - lite

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

As liñas de oportunidade baseada en proxecto só están dispoñibles en oportunidades baseadas en proxecto. Os rexistros de oportunidade baseada en proxecto teñen o campo **Tipo** definido como **Baseado en traballo**.

As liñas de oportunidade baseada en proxecto son os elementos de liña que se entregarán ao cliente mediante un proxecto. Non obstante, un proxecto non pode estar ligado a unha liña de oportunidade baseada en proxecto. Os proxectos pódense vincular a elementos de liña da fase **Oferta** en adiante porque normalmente a oportunidade está nunha fase inicial do ciclo de vida dun acordo. A determinación de cantos proxectos se empregarán para entregar o traballo ao cliente é unha decisión que se toma máis tarde na fase de vendas. Pode usar a fase de oportunidade para identificar os compoñentes de entrega discreta para o cliente. As decisións sobre o número real de proxectos empregados para entregar estes compoñentes pódense aprazar ata que se coñeza máis información sobre o traballo en si.

Abaixo amósanse os campos dunha liña de oportunidade baseada en proxecto:

| **Campo** | **Localización** | **Descrición** | **Impacto descendente** |
| --- | --- | --- | --- |
| Tipo de produto | Separador Xeral (oculto) | Pode seleccionar unha das seguintes opcións:</br>- Servizo baseado en proxectos (dispoñible só cando Dynamics 365 Project Operations está instalado)</br>- Produto (dispoñible só cando Project Operations e Dynamics 365 Sales están instaladas) | O valor deste campo establécese en **Servizo baseado en proxecto** cando crea unha liña de oportunidade baseada en proxecto desde a grade de liñas baseadas en proxecto na Oportunidade. <br> Se cambia ou anula este valor, a funcionalidade do proxecto non se activará nos seus elementos de liña baseada en proxecto. |
| Oportunidade | Separador Xeral | Este campo é de só lectura e fai referencia ao rexistro principal de Oportunidade ao que pertence este elemento de liña. | Non hai ningún impacto descendente deste campo. |
| Nome | Separador Xeral | Este é un campo de texto editable que se pode usar para dar unha identidade curta ao elemento de liña. | Este valor transfírese á liña de oferta cando cree unha oferta a partir desta oportunidade. |
| Orzamento do cliente | Separador Xeral | Este campo de moeda editable pode usarse para rastrexar o importe que o cliente está disposto a gastar para este elemento de liña. | Este valor transfírese ao campo correspondente da liña de oferta cando cree unha oferta a partir desta oportunidade. |
| Método de facturación | Separador Xeral | Este campo editable ten os seguintes valores posibles:</br>- Tempo e material</br>- Prezo fixo | Este valor transfírese ao campo correspondente da liña de oferta cando cree unha oferta a partir desta oportunidade. Despois de crear a liña de oferta, o campo bloquéase e non se pode cambiar. Atribúa este valor de campo coa maior precisión posible. Se precisa cambiar o valor deste campo na liña de oferta, elimine e cree de novo a liña de oferta. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]