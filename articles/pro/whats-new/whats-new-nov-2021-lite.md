---
title: Novidades de novembro de 2021 - Despregamento de Project Operations lite
description: Este artigo ofrece información sobre as actualizacións de calidade que están dispoñibles na versión de novembro de 2021 do despregamento de Project Operations lite.
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 947e7f6183ddeef3ab9a88d140331956bbcf23bd
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913802"
---
# <a name="whats-new-november-2021---project-operations-lite-deployment"></a>Novidades de novembro de 2021 - Despregamento de Project Operations lite

_Aplícase a: Despregamento de Lite - acordo para facturación proforma_

Este artigo aplícase aos seguintes compoñentes e versións de Microsoft Dynamics 365 Project Operations:

- Project Operations nun ambiente de Dataverse versión 4.26.0.145, 4.26.0.148, 4.26.0.150, 4.26.0.155
  
## <a name="features-included-in-this-release"></a>Funcionalidades incluídas nesta versión

As seguintes funcionalidades están incluídas nesta versión:

- As interfaces de programación de aplicacións (API) de programación de proxectos agora admiten a posibilidade de crear e eliminar depósitos de proxectos

## <a name="quality-updates"></a>Actualizacións de calidade

### <a name="project-operations-in-dataverse"></a>Project Operations en Dataverse

| Área de funcionalidades | Número de referencia | Actualización de calidade |
| --- | --- | --- |
| Facturación e prezos | 2358236 | A corrección da factura debe permitir correccións que teñan liñas de prezo cero. |
| Xestión de recursos | 2410072 | Permitir a configuración dun recurso que está atribuído á tarefa como xestor do proxecto. |
| Facturación e prezos | 2430234 | Corrixir un problema de cálculo do rendemento dos custos. |
| Tempo e gasto | 2436978 | Permitir que se introduza o tempo en formato hh:mm. |
| Facturación e prezos | 2448623 | Permitir que as listas de prezos se actualicen despois de asociarse a unha unidade organizativa. |
| Tempo e gasto | 2460396 | Permitir que se elimine unha entrada de tempo borrando a cela. |
| Facturación e prezos | 2467386 | Permitir que se elimine un proxecto que teña unha tarefa, mesmo cando a tarefa estea asociada a unha oferta gañada. |
| Tempo e gasto | 2461744 | A vista **A miña aprobación con erros** só contén aprobacións de proxectos na fase **Enviado**. |
| Tempo e gasto | 2464082 | Elimina a ligazón das aprobacións do proxecto ao conxunto de aprobacións cando coincida cun estado de destino. |
| Tempo e gasto | 2468108 | O traballo de programación non debe establecer un estado **Procesando** para o conxunto de aprobacións. |
| Tempo e gasto | 2471503 | Eliminar os conxuntos de aprobacións que teñan sete días de antigüidade. |
| Facturación e prezos | 2480687 | A referencia da liña de oferta non debe eliminarse cando se crea un fito de liña de oferta. |
