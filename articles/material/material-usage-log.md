---
title: Rexistrar o uso do material en proxectos e tarefas de proxecto
description: Este tema ofrece información sobre como rexistrar o uso de material en proxectos e tarefas de proxecto.
author: rumant
ms.date: 03/31/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3c739d7fabb96a845eaf139fcc9eab21247b0860
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001559"
---
# <a name="record-material-usage-on-projects-and-project-tasks"></a>Rexistrar o uso do material en proxectos e tarefas de proxecto

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Cando un equipo de proxecto traballa mediante tarefas nun proxecto, consumen ou utilizan materiais. Un rexistro de uso de material ofrece un xeito de rexistrar este uso para que poida ser aprobado polo xestor do proxecto e, finalmente, facturado ao cliente. 

Para rexistrar o uso do catálogo ou materiais fóra de catálogo e envialos ao responsable de aprobacións, siga estes pasos: 

1. No panel de navegación, seleccione **Uso de material** e, a seguir, seleccione **Novo**.
2. Na páxina **Uso de material novo** páxina, introduza a información de uso do material requirida e logo seleccione **Gardar**.

A seguinte táboa ofrece información sobre os campos da páxina **Rexistro de uso de material**. 

| **Campo** | **Descrición** | **Impacto descendente** |
| --- | --- | --- |
| Descripción | Unha descrición do uso específico do material. | Non hai ningún impacto descendente para este campo. |
| Data | A data na que se prevé usar o material. | Non hai ningún impacto descendente para este campo. |
| Project | Unha lista de proxectos activos. | A selección dun proxecto para un rexistro de uso de material afecta ao campo **Tarefa** para amosar só as tarefas que están no proxecto. |
| Tarefa | Unha lista de tarefas para o proxecto, incluídas as tarefas de resumo e nó folla. | A selección dunha tarefa para un rexistro de uso de material afecta ao custo real do material e ás vendas reais de material para unha tarefa. Se este campo está baleiro, o custo e as vendas de uso de material correspondentes rastréxanse e resúmense só a nivel do proxecto. |
| Seleccionar produto | Especifique se este uso de material é para un produto **Existente** (catálogo) ou un produto **Fóra de catálogo**. | Este campo determina o tipo de produto. |
| Produto | O ID do produto do catálogo de produtos. Cando selecciona un ID de produto, o valor do campo **Seleccionar produto** actualízase automaticamente a **Produto existente**. O ID úsase para recuperar os prezos de custo e venda da lista de prezos. | Non hai ningún impacto descendente para este campo. |
| Descrición do produto fóra de catálogo | Un campo de texto para escribir o nome do produto. Este campo está dispoñible cando selecciona un produto **Fóra de catálogo** no campo **Seleccionar produto**.| Non hai ningún impacto descendente para este campo. |
| Recurso reservable| Recurso que usou este material no proxecto. O valor predefinido para este campo é o recurso reservable do usuario que iniciou sesión, pero pódese cambiar para rexistrar o uso en nome doutros membros do equipo do proxecto. | Non hai ningún impacto descendente para este campo. |
| Grupo de unidades | O valor predefinido neste campo provén do grupo de unidades configurado como predefinido no produto de catálogo. Pode actualizar este campo para seleccionar outro grupo de unidades. | Non hai ningún impacto descendente para este campo. |
| Unidade | O valor por defecto deste campo é a unidade predefinida do produto seleccionado. Pode actualizar este campo para seleccionar outra unidade. | Cambiar a unidade dá lugar a nun prezo unitario e un custo predefinidos diferentes. |
| Importe | A cantidade do produto que se usou no proxecto ou na tarefa do proxecto. | Non hai ningún impacto descendente para este campo. |
| Custo da unidade | O custo unitario do produto seleccionado e a combinación de unidades establecidas na lista de prezos de custo aplicable | O custo unitario móstrase sempre na moeda de custo do proxecto. Se non hai un custo unitario para a combinación do produto e a unidade na lista de prezos, o custo unitario será por defecto 0,00. |
| Custo total | O importe do custo que se calcula como cantidade de \* custo unitario.| O importe do custo móstrase sempre na moeda de custo do proxecto. |


## <a name="submit-material-usage-for-review-and-approval"></a>Enviar o uso do material para a súa revisión e aprobación 
Despois de capturar todo o uso do material e cando estea listo para que o aproben, debe enviar a información de uso para a súa revisión.

1. Vaia a **Rexistro de uso de material** e seleccione unha ou máis entradas. Ou seleccione todos os rexistros de uso de material empregando a caixa de verificación da cabeceira.
2. Seleccione **Enviar**. O sistema procesa as entradas seleccionadas e logo crea solicitudes de aprobación de uso de material.

## <a name="recall-a-material-usage-log"></a>Retirar un rexistro de uso de material

Cando sexa necesario, pode retirar o uso de material enviado. O tempo necesario para retirar unha entrada de uso de material depende da fase de aprobación.  Se o responsable de aprobacións aínda non aprobou a entrada, a recuperación pode producirse inmediatamente. Non obstante, se a entrada xa foi aprobada, solicítaselle ao responsable de aprobacións que aprobe a recuperación e reverta as transaccións.

1. Vaia a **Uso de material** e na lista de rexistros de uso de material, seleccione o uso de material que desexa retirar.
2. Seleccione **Recuperar**. Se aínda non se aprobou a entrada de uso de material, o sistema retírao inmediatamente. Se a entrada de material xa foi aprobada, créase unha solicitude de retirada para notificar ao responsable de aprobacións que desexa retirar o uso de material. A seguir, o responsable de aprobacións confirmará que se pode facer a reversión e devolverase a entrada.

## <a name="delete-a-material-usage-log"></a>Eliminar un rexistro de uso de material

Pode eliminar os rexistros de uso de material que non se enviaron. Para eliminar un rexistro de uso de material que xa foi enviado, primeiro debe retiralo.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
