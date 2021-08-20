---
title: Copiar listas de prezos
description: Este tema ofrece información sobre como copiar listas de prezos en Project Operations.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ad09bdce563a48843b3ed96e7aaabd9c0d5960336b9e1c74fddb9b61f760f4cd
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003724"
---
# <a name="copy-price-lists"></a>Copiar listas de prezos

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Podes crear copias das listas de prezos en Dynamics 365 Project Operations. Por exemplo, pode crear listas de prezos para o próximo ano usando unha lista de prezos do ano actual.  Ou pode copiar unha lista de prezos para as taxas de factura e os prezos de venda a partir das listas de prezos para custo. 

Para facer unha copia da lista de prezos, complete os seguintes pasos.

1. Abra a lista de prezos da que queira facer unha copia e seleccione **Copiar**.
2. Insira a información necesaria para copiar a lista de prezos. A seguinte táboa mostra consideracións que hai que ter en conta ao introducir información.

| Campo | Descripción | Impacto descendente |
| --- | --- | --- |
| Nome | O nome da lista de prezos de orixe con **-copia** anexo. | A lista de prezos inclúe este valor en todas as páxinas da lista e opcións despregables. |
| Contexto | Introduza o contexto que desexe para a lista de prezos obxectivo. | Unha lista de prezos que ten o contexto establecido en **Custo** utilízase para buscar o prezo para as estimacións de custos e os datos reais de custo. Unha lista de prezos que ten o contexto establecido en **Vendas** utilízase para buscar o prezo para as estimacións de vendas e os datos reais de vendas. Só as listas de prezos que teñen o contexto establecido en **Vendas** poden anexarse a unha lista de prezos do proxecto para un cliente, ofertas ou un contrato. |
| Data de inicio | A data de inicio do período no que esta lista de prezos está vixente. | Xunto con **Data de finalización**, este campo úsase para determinar que lista de prezos é aplicable para unha determinada estimación ou liña de datos reais. |
| Data de finalización | A data de finalización do período no que esta lista de prezos está vixente. | Xunto con **Data de inicio**, este campo úsase para determinar que lista de prezos é aplicable para unha determinada estimación ou liña de datos reais. |
| Moeda | A moeda da lista de prezos de orixe. Isto pódese modificar. | Cando se cambia isto, todas as liñas de prezos resultantes para man de obra, gasto e artigos do catálogo de produtos convértense á moeda da lista de prezos obxectivo durante a copia. |
| Unidade de tempo | A moeda da lista de prezos de orixe. Isto pódese modificar. | Cando se cambia isto, todas as liñas de prezos resultantes para man de obra convértense á unidade da lista de prezos obxectivo durante a copia. Utilízase a conversión da configuración da unidade para a unidade de tempo da lista de prezos de orixe e a unidade de tempo da lista de prezos obxectivo. |
| Descripción | Unha descrición da lista de prezos de orixe con **-copia** anexo. Este é un campo de texto e permítelle ter unha descrición de varias liñas da lista de prezos. | Este campo móstrase nas vistas **Asociado** na lista de prezos en varias entidades que teñen listas de prezos relacionadas. |

3. Garde a lista de prezos. 

## <a name="update-a-price-list-by-applying-a-mark-up-to-all-the-prices"></a>Actualice unha lista de prezos aplicando un aumento a todos os prezos

1. Nos separadores **Rol**, **Categoría** e **Elemento da lista de prezos** dunha lista de prezos, pode seleccionar **Actualizar prezos** para aplicar un sobreprezo para todos os prezos da subgrade. 
2. Na páxina de diálogo que se abre, introduza un aumento. Tamén pode introducir unha porcentaxe de aumento negativa para reducir os prezos nunha porcentaxe determinada. 
3. Seleccione **Aceptar** na páxina de diálogo e logo verifique que os prezos da subgrade reflicten os cambios que realizou.


[!INCLUDE[footer-include](../includes/footer-banner.md)]