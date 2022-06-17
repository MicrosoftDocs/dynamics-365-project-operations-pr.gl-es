---
title: Reinvención dos informes de gastos
description: Este artigo ofrece información sobre a experiencia rediseñado e reimaxinado para a entrada do informe de gastos.
author: ryansandness
ms.date: 06/14/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2019-6-30
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 09322d7a59ae91f64dfa63b00f035178d7ca6444
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920978"
---
# <a name="redesigned-expense-reports"></a>Reinvención dos informes de gastos

Rediseñouse a entrada do informe de gastos para simplificar o proceso de completar os informes de gastos e diminuír o tempo necesario. Estes son os principais compoñentes da nova experiencia de gastos:

- Unha nova área de traballo de xestión de gastos que lle permite acceder aos gastos do seu delegado.
- Unha nova experiencia de correspondencia de recibos para amosar mellor os recibos a nivel de cabeceira e simplificar o proceso de anexar recibos ás liñas de gasto.
- Unha nova grade de só lectura que lle permite ver moitas máis liñas de gasto e columnas de datos adicionais. Agora pode ver todas as liñas detalladas e divididas, xunto cos seus gastos matriz.
- Un panel simplificado para editar gastos.
- Redeseñáronse as mensaxes de erro, advertencia e política para garantir que vostede teña o contexto correcto para comprender o problema e como resolvelo. Microsoft eliminou moitas mensaxes que aparecían antes de que os usuarios tivesen a oportunidade de completar as súas tarefas e resolver os problemas, como a mensaxe de itemización incompleta.
- Unha nova páxina para especificar que campos require a súa organización, que campos son opcionais e que campos non deben ser capturados. Esta páxina axudara a reducir o número de campos que deben definir os usuarios.
- Un novo aspecto para os informes de gastos, de xeito que os informes xa non parecen deseñados para contables.

Para activar a nova experiencia, use a área de traballo **Xestión de funcionalidades** para activar a funcionalidade **Reinvención dos informes de gastos**. Ao activar esta funcionalidade, prodúcense as seguintes accións:

- A área de traballo de gastos existente substitúese pola nova área de traballo.
- Engádese un novo elemento de menú para a visibilidade do campo de gastos.
- Non se eliminan elementos de menú existentes para informes de gastos (a páxina existente) nin campos do informe de gastos.
- Os fluxos de traballo e as aprobacións aínda o levarán á páxina de informes de gastos existente.

## <a name="new-features"></a>Novas funcionalidades

| Nova funcionalidade | Descripción |
|---|----|
| Visibilidade do campo de gasto | Unha nova páxina de configuración permítelle especificar que campos deben desactivarse para unha organización, que campos deben ser obrigatorios e que campos son recomendables. |
| Campos obrigatorios | A nova configuración sinxela permítelle crear algúns campos necesarios sen ter que empregar o marco de políticas. |
| Campos opcionais | Engádese unha segunda páxina para campos opcionais. Deste xeito, aos empregados non se sentirán como se debesen establecer os campos, senón que os campos xa son facilmente accesibles. |
| Engadir recibos non anexados | A capacidade de engadir recibos non anexados ao informe de gastos é máis visible desde a área de traballo e no informe de gastos. |
| Mellora da mensaxería | Hai unha mellor visibilidade das liñas de gasto que teñen advertencias ou erros. |
| Redución de mensaxes na barra de mensaxes| Reduciuse o número de mensaxes de Infolog e fíxxose un esforzo para evitar que aparezan mensaxes duplicadas en moitos casos. |
| Accións comúns agrupadas | A interface limpouse coa adición dun novo botón de accións para a maioría das accións comúns a nivel de liña e a adición dun botón de puntos suspensivos (...) para a cabeceira e outras accións menos frecuentes. |
| Nova área de traballo para aumentar a visibilidade | A nova área de traballo unifica funcións e ligazóns que permiten aos usuarios moverse a diferentes áreas. |
| Engadir os gastos e recibos existentes durante a creación de gastos | Cando crea informes de gastos, pode engadir todos os gastos e recibos ou algúns seleccionados. |
| Calculadora de taxa de cambio | Engádese unha calculadora de taxas de cambio que lle permite calcular a taxa de cambio das transaccións multimoeda. |
| Gardar e engadir novas liñas de gasto | Os botóns **Gardar** e **Novo** están dispoñibles cando se introducen novos gastos para axudarlle a introducir rapidamente as liñas de gastos. |
| Mellor visibilidade en liñas divididas e detalladas | As liñas detalladas e divididas engádense directamente á lista de gastos para aumentar a visibilidade e axudarlle a determinar facilmente se hai erros de política ou outros erros. |
| Amosar recibos durante a itemización | Os recibos pódense mostrar durante a itemización. |

A versión inicial céntrase en situacións de entrada de gastos. Calquera situación de revisión ou aprobación do informe de gastos seguirá utilizando a páxina de entrada de gastos existente.

As seguintes funcionalidades están presentes na páxina existente pero aínda non están na nova páxina. Estas funcións volveranse introducir nas próximas versións:

- Aprobacións
- Aprobacións de contas pendentes de pagamento e capacidade para editar a contabilidade
- Varios puntos de entrada
- Integración de solicitude de viaxe
- Entidade de datos para a visibilidade do campo de gasto
- Entrada para gastos de dietas
- Fluxo de traballo a nivel de liña
- Apoio provisional para responsables de aprobacións…
- Itemización avanzada


[!INCLUDE[footer-include](../includes/footer-banner.md)]