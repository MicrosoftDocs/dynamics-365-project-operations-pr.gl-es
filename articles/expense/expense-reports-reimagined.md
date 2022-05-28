---
title: Informes de gastos reimaxinados (contén vídeo)
description: Este tema explica a experiencia redeseñada e reinterpretada para a entrada do informe de gastos.
author: suvaidya
ms.date: 12/16/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 562ec3701a607ed95f663f3e0846d044b3bf504e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586940"
---
# <a name="expense-reports-reimagined"></a>Os informes de gastos reinventáronse

A entrada do informe de gastos redeseñouse para simplificar o proceso e reducir o tempo necesario para completar un informe. Estes son os principais compoñentes da nova experiencia de gastos:

- Unha nova área de traballo de xestión de gastos que lle permite acceder aos gastos do seu delegado.
- Unha nova experiencia de correspondencia de recibos para amosar mellor os recibos a nivel de cabeceira e simplificar o proceso de anexar recibos ás liñas de gasto.
- Unha nova grade de só lectura que lle permite ver moitas máis liñas de gasto e outras columnas de datos. Agora pode ver todas as liñas detalladas e divididas, xunto cos seus gastos matriz.
- Un panel simplificado para editar gastos.
- Redeseñáronse as mensaxes de erro, advertencia e política para proporcionar o contexto correcto e a comprensión do problema e como resolvelo. Eliminamos varias das mensaxes que aparecían antes de que os usuarios puidesen completar as súas tarefas e solucionar os problemas.
- Unha nova páxina para especificar os campos obrigatorios, os campos opcionais e os campos que non deben incluírse. Esta páxina axuda a reducir o número de campos que se deben definir.
- Un novo aspecto para os informes de gastos, de xeito que os informes xa non parecen deseñados para contables.

Para activar a nova experiencia, use a área de traballo **Xestión de funcionalidades** para activar a funcionalidade **Novo deseño da área de traballo de informes de gastos**. Ao activar esta funcionalidade, prodúcense as seguintes accións:

- A área de traballo de gastos existente substitúese pola nova área de traballo.
- Engádese un novo elemento de menú para a visibilidade do campo de gastos.
- Non se eliminan elementos de menú existentes para informes de gastos (a páxina existente) nin campos do informe de gastos.
- Os fluxos de traballo e as aprobacións aínda o levarán á páxina de informes de gastos existente.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4IQFM]

## <a name="new-features"></a>Novas funcionalidades

| Nova funcionalidade | Descripción |
|---|----|
| Visibilidade do campo de gasto | Unha nova páxina de configuración permítelle especificar que campos se deben desactivar para unha organización. Tamén pode especificar os campos que se requiren e os campos recomendados. |
| Campos obrigatorios | A nova configuración sinxela permítelle crear algúns campos necesarios sen ter que empregar o marco de políticas. |
| Campos opcionais | Engádese unha segunda páxina para campos opcionais. Deste xeito, aos empregados non se sentirán como se debesen establecer os campos, senón que os campos xa son facilmente accesibles. |
| Engadir recibos non anexados | A capacidade de engadir recibos non anexados ao informe de gastos é máis visible desde a área de traballo e no informe de gastos. |
| Mellora da mensaxería | Hai unha mellor visibilidade das liñas de gasto que teñen advertencias ou erros. |
| Redución de mensaxes na barra de mensaxes| Reduciuse o número de mensaxes de Infolog e fíxxose un esforzo para evitar que aparezan mensaxes duplicadas en moitos casos. |
| Accións comúns agrupadas | A interface limpouse coa adición dun novo botón de accións para a maioría das accións comúns a nivel de liña e a adición dun botón de puntos suspensivos (...) para a cabeceira e outras accións menos frecuentes. |
| Nova área de traballo para aumentar a visibilidade | A nova área de traballo unifica funcións e ligazóns que permiten aos usuarios moverse a diferentes áreas. |
| Engadir os gastos e recibos existentes durante a creación de gastos | Cando crea informes de gastos, pode engadir todos os gastos ou seleccionar os gastos non anexados. Os gastos non anexados son gastos que se importaron da fonte da tarxeta de crédito corporativa ou gastos creados manualmente polo usuario pero que non se anexaron a un informe de gastos.|
| Calculadora de taxa de cambio | Engádese unha calculadora de taxas de cambio que lle permite calcular a taxa de cambio das transaccións multimoeda. |
| Gardar e engadir novas liñas de gasto | Os botóns **Gardar** e **Novo** están dispoñibles cando se introducen novos gastos para axudarlle a introducir rapidamente as liñas de gastos. |
| Mellor visibilidade en liñas divididas e detalladas | As liñas detalladas e divididas engádense directamente á lista de gastos para aumentar a visibilidade e axudarlle a determinar facilmente se hai algún erro. |
| Ver detalles da subcategoría en liñas detalladas | As liñas detalladas dun gasto principal amosan as etiquetas da subcategoría no informe de gastos. A itemización permítelle revisar os detalles granulares dunha ollada.|
|Desglose rapidamente os gastos recorrentes | O espazo de traballo de gastos reimaxinado ofrece a posibilidade de detallar os gastos recorrentes rapidamente engadindo a subcategoría, a data de inicio e a cantidade. A cantidade refírese ao número de veces que se repite a carga nun período continuo. |
| Amosar recibos durante a itemización | Os recibos pódense mostrar durante a itemización. |
| Selección de adianto en efectivo | Seleccione un ou máis adiantos en efectivo para realizar unha única transacción de gasto. |
| Saldo de adiantos en efectivo | Revise o saldo de adiantos en efectivo en tempo real cando cree unha entrada de gasto fronte a adiantos en efectivo aprobados e pagados. |

A versión inicial céntrase en situacións de entrada de gastos. Calquera situación de revisión ou aprobación do informe de gastos seguirá utilizando a páxina de entrada de gastos existente.


As seguintes funcionalidades non son compatibles no redeseño da área de traballo de informes de gastos, pero están previstas para futuras versións: 

- Integración de solicitude de viaxe
- Entrada de gastos de dietas
- Apoio provisional para responsables de aprobacións…
- Capacidade para ver o historial do fluxo de traballo


[!INCLUDE[footer-include](../includes/footer-banner.md)]
