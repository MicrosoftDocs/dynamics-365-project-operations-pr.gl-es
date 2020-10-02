---
title: Crea estimacións nunha liña de oferta
description: Este tema ofrece información sobre como crear unha estimación nunha liña de oferta para un proxecto.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e841ab7c37e0b348a4d1570123a5aea00ede0047
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898485"
---
# <a name="create-estimates-on-a-quote-line"></a>Crea estimacións nunha liña de oferta

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Nunha oferta baseada en proxectos, pode usar a entidade de detalle de liña Oferta para estimar o traballo que é necesario para entregar un proxecto. Despois pode compartir esa estimación co cliente.

As liñas da oferta baseada en proxectos non teñen que ter detalles de liña de oferta. Alternativamente, poden ter moitos detalles da liña de oferta. Os detalles de liña de oferta utilízanse para estimar tempo, gastos ou tarifas. Dynamics 365 Project Operations non permite estimacións de materiais sobre os detalles de liña de oferta. Estas se chaman clases de transacción. Os importes de impostos estimados tamén se poden introducir nunha clase de transacción.

Ademais das clases de transacción, os detalles de liña de oferta teñen un tipo de transacción. Hai dous tipos de transacción para detalles de liña de oferta, **Custo** e **Contrato do proxecto**.

## <a name="estimate-by-using-a-contract"></a>Estimar mediante un contrato

Se utilizou unha oferta de Project Operations cando creou un contrato baseado en proxectos, a estimación que fixo para cada liña de oferta na oferta cópiase no contrato de proxecto. A estrutura dun contrato de proxecto é como a estrutura da oferta do proxecto que ten liñas, detalles de liña e programas de facturas.

As estimacións pódense facer directamente nun contrato de proxecto, como nunha oferta de proxecto. Para unha oferta de proxecto, a estimación faise mediante as liñas de contrato e os detalles de liña de contrato. Os detalles de liña de contrato tamén se poden xerar a partir dun plan de proxecto que se creou mediante o enfoque de estimación de abaixo cara arriba.

Os detalles de liña de contrato pódense utilizar para estimar tempo, gastos ou tarifas. Os importes de impostos estimados tamén se poden introducir nun detalle de liña de contrato.

As estimacións de materiais no se permiten nos detalles de liña de contrato.

Os procesos que se admiten nun contrato de proxecto son a creación e confirmación de facturas. A creación de facturas crea un borrador dunha factura baseada en proxecto que inclúe todos os datos reais de vendas sen facturar ata a data actual.

A confirmación fai que o contrato sexa só de lectura e cambie o seu estado de **Borrador** a **Confirmado**. Despois de realizar esta acción, non pode desfacela. Dado que esta acción é permanente, é unha mellor práctica manter o contrato nun estado de **Borrador**.

As únicas diferenzas entre os borradores de contrato e os contratos confirmados son o seu estado e o feito de que os borradores de contrato se poden editar mentres que os contratos confirmados non poden editarse. A creación de facturas e o rastrexo de datos reais pódense realizar tanto nos borradores de contrato como nos contratos confirmados.

Non se admite a modificación de pedidos en contratos ou proxectos.

## <a name="estimating-projects"></a>Estimación de proxectos

Pode estimar o tempo e os gastos en proxectos, pero non os materiais ou as taxas.

As estimacións de tempo xéranse cando vostede crea unha tarefa e identifica os atributos dun recurso xenérico que se require para realizar a tarefa. As estimacións de tempo xéranse a partir de tarefas de programación. As estimacións de tempo non se crean se vostede crea membros xenéricos do equipo fóra do contexto da programación.

As estimacións de gastos introdúcense na grade na páxina **Estimacións**.

## <a name="understand-estimation"></a>Comprender a estimación

Utilice a seguinte táboa como guía para comprender a lóxica de negocio na fase de estimación.

| Escenario                                                                                                                                                                                                                                                                                                                                          | Rexistro de entidades                                                                                                                                                                                                       | Tipo de transacción | Clase de transacción | Información adicional                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|-------------|-----------------------------------------------------------------------------------|
| Cando necesite estimar o valor de vendas de tempo nunha oferta                                                                                                                                                                                                                                                                                    | Créase o rexistro de detalle de liña de oferta (QLD)                                                                                                                                                                               | Contrato do proxecto | Time        | O campo de orixe da transacción na fila QLD de vendas fai referencia a QLD de custo |
|                                                                                                                                                                                                                                                                                     | O sistema crea un segundo rexistro QLD para almacenar os valores de custo correspondentes. O sistema copia todos os campos non monetarios do QLD de vendas ao QLD de custo.                                                                                                                                                                               | Custo | Time        | O campo de orixe da transacción na fila de detalle de liña de oferta (QLD)de vendas fai referencia ao QLD de custo |
| Cando necesite estimar o valor de vendas de tempo nun contrato                                                                                                                                                                                                                                                                                 | Créase o rexistro de detalle de liña de contrato (CLD) do proxecto                                                                                                                                                                    | Contrato do proxecto | Time        | O campo de orixe da transacción na fila CLD de vendas fai referencia a CLD de custo      |
|                                                                                                                                                                                                                                                                                  | O sistema crea un segundo rexistro CLD para almacenar os valores de custo correspondentes. O sistema copia todos os campos non monetarios do CLD de vendas ao CLD de custo.                                                                                                                                                                    | Custo | Time        | O campo de orixe da transacción na fila CLD de vendas fai referencia a CLD de custo      |
| Cando o usuario describe un recurso nunha tarefa de proxecto                                                                                                                                                                                                                                                                                            | Créase un rexistro de liña de estimación para mostrar o valor de vendas da tarefa cando se crea unha tarefa con todas as dimensións de prezos necesarias. O rol e as unidades organizativas son as dimensións dos prezos | Contrato do proxecto | Tempo        |                                                                                   |
|     | Créase un rexistro de liña de estimación para mostrar o valor de custo da tarefa cando se crea unha tarefa con todas as dimensións de prezos necesarias. O sistema copia todos os campos non monetarios da liña de estimación de vendas ao á liña de estimación de custo. O rol e a unidade organizativa son as dimensións dos prezos tanto para custo como para taxas de facturación.                                                                                                                                                                                                                | Custo             | Tempo           |                                                                                   |



## <a name="customize-the-quote-line-detail-and-contract-line-detail-entities"></a>Personalizar as entidades de detalle de liña de oferta e detalle de liña de contrato

Se engadiu un campo personalizado no detalle de liña de oferta e quere que o sistema introduza o valor do campo como valor predefinido na liña de custo relacionada que crea, use as ferramentas de rexistro dos complementos PreOperationContractLineDetailUpdate e PreOperationQuoteLineDetailUpdate. Estes complementos deben rexistrarse de novo despois de que se cambie o detalle da liña de oferta ou detalle da liña de contrato. Siga estes pasos para completar o proceso:

1. Abra PluginRegistrationTool e conéctese á súa instancia en liña.
2. Seleccione **Buscar** e busque o complemento para actualizar.
3. Seleccione o complemento e, a seguir, na páxina principal, seleccione **Seleccionar**.
4. Seleccione o paso do complemento para actualizar, prema co botón dereito e logo seleccione **Actualizar**.
5. Na caixa de diálogo **Actualizar o paso existente**, no campo **Atributos de filtrado**, seleccione o botón de puntos suspensivos (**...**):
6. Na caixa de diálogo **Seleccionar atributos**, seleccione as caixas de verificación dos atributos personalizados.
7. Seleccione **Aceptar** para pechar a caixa de diálogo e logo seleccione **Actualizar paso**.
8. Repita os pasos do 1 ao 7 para o segundo complemento.
9. Peche PluginRegistrationTool.
