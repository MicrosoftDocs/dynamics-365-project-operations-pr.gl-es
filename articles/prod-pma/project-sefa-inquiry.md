---
title: Lista de gastos de investigación de subvencións federais
description: Este tema ofrece información sobre a programación de gastos de investigación de subvencións federais.
author: velofog
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: johnmichalak
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: andchoi
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: b88c97f3dcb1020ccf17788256990485580f6964
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/04/2022
ms.locfileid: "8684456"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a>Lista de gastos de investigación de subvencións federais

[!include [banner](../includes/banner.md)]

Segundo a Circular A-133 da Oficina de Xestión e Orzamentos, as axencias que reciben fondos federais están suxeitas a requisitos de auditoría, que tamén se coñecen como auditorías únicas. O proceso de auditoría úsase para informar de forma recorrente sobre os ingresos e gastos das subvencións federais. Unha parte do informe único de auditoría inclúe a programación de gastos de subvencións federais (SEFA).

A programación de gastos de investigación de subvencións federais inclúe o título e número do Catálogo de asistencia doméstica federal (CFDA), o número da subvención, o ano da subvención, o nome da axencia federal que proporciona os fondos e o nome da entidade intermediaria. A investigación é por un período específico. Normalmente, ese período é o mesmo que o período dos estados financeiros, que é un ano fiscal.

A consulta inclúe subvencións que teñen datas de proxección no intervalo de datas seleccionado. A columna **Axencia outorgante** na columna da investigación mostra o cliente da subvención ou, para unha subvención a través de intermediario, a axencia outorgante. Para unha subvención a través de intermediario, a columna **Axencia intermediaria** mostra o cliente da subvención. Se subvención non é través de intermediario, a columna **Axencia intermediaria** está en branco.

## <a name="set-up-the-cfda-clusters"></a>Configure os clústeres CFDA

Debe configurar os clústeres de CFDA que se poidan asociar aos números CFDA na programación de gastos de investigación de subvencións federais.

1. Vaia a **Xestión e contabilidade de proxectos \> Configurar \> Subvencións \> Catálogo de clústeres de asistencia doméstica federal**.
2. Seleccione **Novo** para crear un clúster de CFDA.
3. Escriba o nome do clúster.
4. Seleccione **Gardar** para gardar as modificacións.

## <a name="set-up-cfda-numbers"></a>Configurar os números de CFDA

Debe configurar os números de CFDA que se poidan engadir ás subvencións e incluír na programación de gastos de investigación de subvencións federais.

1. Vaia a **Xestión e contabilidade de proxectos \> Configurar \> Subvencións \> Catálogo de números de asistencia doméstica federal**.
2. Seleccione **Novo** para crear un número de CFDA.
3. Na columna **Número**, introduza o número de CFDA.
4. Prema a tecla **Separador**.
5. Na columna **Descrición**, introduza o título de CFDA.
6. Prema a tecla **Separador**.
7. Opcional: No campo **Clúster de programas**, engada o clúster de CFDA axeitado.
8. Seleccione **Gardar** para gardar as modificacións.

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a>Configurar subvencións para a programación de gastos de investigación de subvencións federais

1. Vaia a **Xestión e contabilidade de proxectos \> Subvencións \> Subvencións** e seleccione unha subvención existente.
2. No separador rápido **Configurar**, no campo **Catálogo de asistencia doméstica federal**, atribúa o número CFDA. O número CFDA da subvención determina o clúster de CFDA para a presentación de informes.
3. No separador rápido **Información de contacto**, introduza a información do outorgante seguindo estes pasos:

    1. No campo **Cliente da subvención**, introduza o cliente responsable da subvención. Para unha subvención existente, é posible que esta información xa estea introducida.
    2. Indique se o cliente da subvención é o financiador. Se o cliente da subvención é o financiador, deixe a caixa de verificación **Intermediario** sen marcar. Se outro cliente é o financiador e o cliente da subvención é responsable do gasto e rastrexo do diñeiro, seleccione a caixa de verificación **Intermediario**.

4. Se seleccionou a caixa de verificación **Intermediario** no paso anterior, no campo **Axencia outorgante**, introduza o cliente que proporcionou a subvención. A axencia outorgante e o cliente outorgante non poden ser o mesmo cliente.

Aquí ten un exemplo de subvención a través de intermediario:

O goberno federal financiou un proxecto de infraestrutura para un estado. O goberno federal deu o diñeiro ao estado para gastalo. Neste caso, o goberno federal é a axencia outorgante e o estado é o cliente da subvención.

> [!NOTE] 
> Cando active a funcionalidade por primeira vez, introduciranse os números CFDA iniciais empregando os números existentes nas subvencións.

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a>Excluír as subvencións dos informes SEFA en función do tipo de subvención

1. Vaia a **Xestión e contabilidade de proxectos \> Configurar \> Subvencións \> Tipos de subvencións**.
2. No separador rápido **Información predefinida**, seleccione a caixa de verificación **Excluír da programación de gastos de subvencións federais**.
3. Seleccione **Gardar** para gardar as modificacións.

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a>Execute a programación gastos de investigación de subvencións federais

1. Vaia a **Xestión e contabilidade de proxectos \> Investigacións e informes \> Investigación de subvención \> Programación de gastos de subvencións federais**.
2. Na sección **Parámetros**, siga estes pasos:

    1. No campo **Intervalo de datas**, seleccione o código para o intervalo de datas. Alternativamente, nos campos **A partir da data** e **Ata a data**, defina o intervalo de datas.
    2. Opcional: Para incluír só as transaccións facturadas como ingresos na investigación, configure a opción **Incluír só os ingresos facturados** en **Si**.

## <a name="columns"></a>Columnas

A programación de gastos de investigación de subvencións federais inclúe as seguintes columnas:

- Nome do clúster do catálogo de asistencia doméstica federal
- Axencia outorgante
- Axencia intermediaria
- Nome da subvención
- ID da subvención
- ID da solicitude de subvención
- Catálogo de asistencia doméstica federal
- Recibos
- Gastos


[!INCLUDE[footer-include](../includes/footer-banner.md)]