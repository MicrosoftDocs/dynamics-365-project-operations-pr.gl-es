---
title: Conceptos de estimación financeira
description: Este tema ofrece información sobre as estimacións financeiras de proxectos en Project Operations.
author: rumant
ms.date: 03/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 74b2499cc706e03658cadeb088df154100051cbc7cce386b2e4d50dbdb5c197f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6989189"
---
# <a name="financial-estimation-concepts"></a>Conceptos de estimación financeira

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

En Dynamics 365 Project Operations, pode estimar financeiramente os seus proxectos en dúas fases: 
1. Durante a fase de prevenda antes de gañar o acordo. 
2. Durante a fase de execución despois da creación do contrato do proxecto. 

Pode crear unha estimación financeira para o traballo baseado en proxectos usando calquera das seguintes 3 páxinas:
- A páxina **Liña de oferta**, usando os detalles da liña de oferta.  
- A páxina **Liña de contrato de proxecto**, usando os detalles da liña de contrato. 
- A páxina **Proxecto**, usando as páxinas do separador **Tarefas** ou **Estimacións de gastos**.

## <a name="use-a-project-quote-to-create-an-estimate"></a>Usar unha oferta de proxecto para crear unha estimación
Nunha oferta baseada en proxectos, pode usar a entidade **Detalle de liña de oferta** para estimar o traballo que é necesario para entregar un proxecto. Despois pode compartir esa estimación co cliente.

As liñas da oferta baseada en proxectos poden ter de cero a moitos detalles de liña de oferta. Os detalles de liña de oferta utilízanse para estimar tempo, gastos ou tarifas. Microsoft Dynamics 365 Project Operations non permite estimacións de materiais sobre os detalles de liña de oferta. Estas se chaman clases de transacción. Os importes de impostos estimados tamén se poden introducir nunha clase de transacción.

Ademais das clases de transacción, os detalles de liña de oferta teñen un tipo de transacción. Admítense dous tipos de transacción para detalles de liña de oferta: **Custo** e **Contrato do proxecto**.

## <a name="use-a-project-contract-to-create-an-estimate"></a>Usar un contrato de proxecto para crear unha estimación

Se utilizou unha oferta cando creou un contrato baseado en proxectos, a estimación que fixo para cada liña de oferta na oferta cópiase no contrato de proxecto. A estrutura dun contrato de proxecto é como a estrutura da oferta do proxecto que ten liñas, detalles de liña e programas de facturas.

As estimacións pódense facer directamente nun contrato de proxecto, como nunha oferta de proxecto. Para unha oferta de proxecto, a estimación faise mediante as liñas de contrato e os detalles de liña de contrato. Os detalles de liña de contrato tamén se poden xerar a partir dun plan de proxecto que se creou mediante o enfoque de estimación de abaixo cara arriba.

Os detalles de liña de contrato pódense utilizar para estimar tempo, gastos ou tarifas. Os importes de impostos estimados tamén se poden introducir nun detalle de liña de contrato.

As estimacións de materiais no se permiten nos detalles de liña de contrato.

## <a name="use-a-project-to-create-an-estimate"></a>Empregue un proxecto para crear unha estimación 

Pode estimar tempo e gastos en proxectos. Project Operations non admite estimacións de materiais ou taxas nos proxectos.

As estimacións de tempo xéranse cando vostede crea unha tarefa e identifica os atributos dun recurso xenérico que se require para realizar a tarefa. As estimacións de tempo xéranse a partir de tarefas de programación. As estimacións de tempo non se crean se vostede crea membros xenéricos do equipo fóra do contexto da programación.

As estimacións de gastos introdúcense na grade na páxina **Estimacións de gastos**.

Crear unha estimación para un proxecto considérase unha boa práctica porque vostede pode elaborar estimacións detalladas para traballo ou tempo e gastos en cada tarefa do plan do proxecto. A seguir, pode empregar esta estimación detallada para crear estimacións para cada liña de oferta e crear unha oferta máis crible para o cliente. Cando importa ou crea unha estimación detallada na liña de oferta usando o plan do proxecto, Project Operations importa os valores de vendas e os valores de custo destas estimacións. Despois da importación, pode ver as métricas de rendibilidade, marxes e viabilidade na oferta do proxecto.

## <a name="understanding-estimates"></a>Comprensión das estimacións

Utilice a seguinte táboa como guía para comprender a lóxica de negocio na fase de estimación.

| Escenario                                                                                                                                                                                                                                                                                                                                          | Rexistro da entidade                                                                                                                                                                                                       | Tipo de transacción | Clase de transacción | Información adicional                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|-------------|-----------------------------------------------------------------------------------|
| Cando necesite estimar o valor de vendas de tempo nunha oferta                                                                                                                                                                                                                                                                                    | Créase o rexistro de detalle de liña de oferta (QLD)                                                                                                                                                                               | Contrato do proxecto | Time        | O campo de orixe da transacción na fila QLD de vendas fai referencia a QLD de custo |
|                                                                                                                                                                                                                                                                                     | O sistema crea un segundo rexistro QLD para almacenar os valores de custo correspondentes. O sistema copia todos os campos non monetarios do QLD de vendas ao QLD de custo.                                                                                                                                                                               | Custo | Time        | O campo de orixe da transacción na fila de detalle de liña de oferta (QLD)de vendas fai referencia ao QLD de custo |
| Cando necesite estimar o valor de vendas de tempo nun contrato                                                                                                                                                                                                                                                                                 | Créase o rexistro de detalle de liña de contrato (CLD) do proxecto                                                                                                                                                                    | Contrato do proxecto | Time        | O campo de orixe da transacción na fila CLD de vendas fai referencia a CLD de custo      |
|                                                                                                                                                                                                                                                                                  | O sistema crea un segundo rexistro CLD para almacenar os valores de custo correspondentes. O sistema copia todos os campos non monetarios do CLD de vendas ao CLD de custo.                                                                                                                                                                    | Custo | Time        | O campo de orixe da transacción na fila CLD de vendas fai referencia a CLD de custo      |
| Cando o usuario describe un recurso nunha tarefa de proxecto                                                                                                                                                                                                                                                                                            | Créase un rexistro de liña de estimación para mostrar o valor de vendas da tarefa cando se crea unha tarefa con todas as dimensións de prezos necesarias. O rol e as unidades organizativas son as dimensións dos prezos | Contrato do proxecto | Tempo        |                                                                                   |
|     | Créase un rexistro de liña de estimación para mostrar o valor de custo da tarefa cando se crea unha tarefa con todas as dimensións de prezos necesarias. O sistema copia todos os campos non monetarios da liña de estimación de vendas ao á liña de estimación de custo. O rol e a unidade organizativa son as dimensións dos prezos tanto para custo como para taxas de facturación.                                                                                                                                                                                                                | Custo             | Tempo           |                                                                                   |



## <a name="customize-the-quote-line-detail-and-contract-line-detail-entities"></a>Personalizar as entidades de detalle de liña de oferta e detalle de liña de contrato

Se engadiu un campo personalizado no detalle de liña de oferta e quere que o sistema introduza o valor do campo como valor predefinido na liña de custo relacionada que crea, use as ferramentas de rexistro dos complementos **PreOperationContractLineDetailUpdate** e **PreOperationQuoteLineDetailUpdate**. Estes complementos deben rexistrarse de novo despois de que se cambie o detalle da liña de oferta ou detalle da liña de contrato. Siga estes pasos para completar o proceso:

1. Abra PluginRegistrationTool e conéctese á súa instancia en liña.
2. Seleccione **Buscar** e busque o complemento para actualizar.
3. Seleccione o complemento e, a seguir, na páxina principal, prema **Seleccionar**.
4. Seleccione o paso do complemento para actualizar, prema co botón dereito e logo seleccione **Actualizar**.
5. Na caixa de diálogo **Actualizar o paso existente**, no campo **Atributos de filtrado**, seleccione o botón de puntos suspensivos (**...**):
6. Na caixa de diálogo **Seleccionar atributos**, seleccione as caixas de verificación dos atributos personalizados.
7. Seleccione **Aceptar** para pechar a caixa de diálogo e logo seleccione **Actualizar paso**.
8. Repita os pasos do 1 ao 7 para o segundo complemento.
9. Peche **PluginRegistrationTool**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
