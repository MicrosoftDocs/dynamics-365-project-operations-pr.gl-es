---
title: Visión xeral da utilización de recursos
description: Este artigo ofrece información sobre a utilización de recursos en Project Operations.
author: ruhercul
ms.date: 11/05/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 5fbba4c9feaf3b26fba3423e160b09c58e049c70
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918494"
---
# <a name="resource-utilization-overview"></a>Visión xeral da utilización de recursos

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Os recursos poden ter unha utilización facturable obxectivo. Esta utilización obxectivo defínese como un atributo no rol predefinido dun recurso ou establécese no rexistro do recurso reservable individual. Os cálculos de utilización baséanse nas horas reais que os recursos comunicaron mediante entradas de tempo aprobadas.

Para o cálculo da utilización úsanse as seguintes fórmulas:

  - Utilización facturable = (Horas reais imputables) ÷ (Capacidade do recurso).
  - Utilización non facturable = Tempo real con ID de tipo de facturación = Non imputable, Gratuíto ou Non dispoñible ÷ Capacidade do recurso
  - Interno = Tempo real sen contrato de vendas ÷ Capacidade do recurso
  - Capacidade do recurso = Horas laborables do recurso - Fóra de oficina - Días non laborables

Podes atopar a vista **Utilización de recursos** no panel **Recursos**.

Cada cela da grade representa a porcentaxe de utilización facturable do recurso nun período, como un día, unha semana ou un mes. Para o color das celas úsanse as seguintes fórmulas:

  - **Verde**: utilización facturable > = utilización de destino de recursos
  - **Amarelo**: utilización de destino – 20 < = utilización facturable < utilización de destino
  - **Vermello**: utilización facturable < utilization de destino – 20

Debido a que a vista **Utilización de recursos** está baseada no panel de programación, pode empregar as capacidades de filtrado do panel de programación para filtrar os seus resultados.

A grade require que estableza unha utilización obxectivo no rol ou o recurso individual. Para configurar isto, vaia a **Recursos** > **Roles de recursos**.

Ademais, debe atribuírse un rol predefinido a cada recurso reservable. Vaia a **Recursos** > **Recursos**. No separador **Project Service**, verifique se está definido un rol de recurso e que o campo **É predefinido** está configurado en **Si**. Pode engadir roles adicionais cando **É predefinido** = **Non**. O rol cando **É predefinido** = **Si** úsase para avaliar a utilización do recurso fronte ao obxectivo para ese rol.

No separador **Project Service**, tamén pode configurar unha utilización obxectivo individual para o recurso. A seguir, o cálculo de utilización usa esa utilización obxectivo para avaliar o obxectivo do recurso no canto do obxectivo do rol predefinido do recurso.

A utilización móstrase só para un recurso só se ese recurso ten un tempo imputable acordado durante o período que se amosa na grade.


[!INCLUDE[footer-include](../includes/footer-banner.md)]