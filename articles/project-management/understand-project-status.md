---
title: Comprender o estado do proxecto
description: Este tema ofrece información sobre o estado atribuído aos proxectos en Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fc9b107507008fd2381d3669552d754d2c867a7f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286471"
---
# <a name="understand-project-status"></a>Comprender o estado do proxecto

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_


A sección **Estado** da páxina **Entidade do proxecto** ofrece un resumo da saúde dun proxecto en función do custo e do esforzo.


## <a name="status-summary-fields"></a>Campos resumo do estado

- O campo **Estado xeral do proxecto** é un campo editable que amosa o estado xeral do proxecto. Este campo emprega codificación de cores, como verde, amarelo e vermello, para indicar un risco crecente. 
- O campo **Comentarios** permítelle ao xestor de proxectos introducir comentarios específicos sobre o estado. 
- O campo **Estado actualizado o** non é editable. O valor deste campo é unha marca de tempo que indica cando se actualizou por última vez o estado.
- Os campos **Rendemento de programación** e **Rendemento de custos** defínense a partir da grade de rastrexo. Cando a varianza de programación e custo para o nó raíz na vista **Rastrexo do esforzo** é positiva, estes campos actualízanse a **Adiantado**. Cando o calendario e a varianza de custos para o nó raíz son negativos, estes campos configúranse en **Atrasado**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]