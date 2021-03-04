---
title: Estimacións
description: Este tema fornece información sobre as estimacións en Dynamics 365 Project Service Automation.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 1/31/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 2fa81067ad6e7c291b9ad9468db051e8f6187da9
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5151431"
---
# <a name="estimates"></a>Estimacións

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Nunha oferta baseada en proxectos, pode usar a entidade de detalle de liña Oferta para estimar o traballo que é necesario para entregar un proxecto. Despois pode compartir esa estimación co cliente.

As liñas da oferta baseada en proxectos non teñen que ter detalles de liña de oferta. Alternativamente, poden ter moitos detalles da liña de oferta. Os detalles de liña de oferta utilízanse para estimar tempo, gastos ou tarifas. PSA non permite estimacións de materiais sobre os detalles de liña de oferta. Estas se chaman clases de transacción. Os importes de impostos estimados tamén se poden introducir nunha clase de transacción.

Ademais das clases de transacción, os detalles de liña de oferta teñen un tipo de transacción. PSA admite dous tipos de transacción para detalles de liña de oferta: **Custo** e **Contrato do proxecto**.

## <a name="estimate-by-using-a-contract"></a>Estimar mediante un contrato

Se utilizou unha oferta de PSA cando creou un contrato baseado en proxectos, a estimación que fixo para cada liña de oferta na oferta cópiase no contrato de proxecto. A estrutura dun contrato de proxecto é como a estrutura da oferta do proxecto que ten liñas, detalles de liña e programas de facturas.

As estimacións pódense facer directamente nun contrato de proxecto, como nunha oferta de proxecto. Para unha oferta de proxecto, a estimación faise mediante as liñas de contrato e os detalles de liña de contrato. Os detalles de liña de contrato tamén se poden xerar a partir dun plan de proxecto que se creou mediante o enfoque de estimación de abaixo cara arriba.

Os detalles de liña de contrato pódense utilizar para estimar tempo, gastos ou tarifas. Os importes de impostos estimados tamén se poden introducir nun detalle de liña de contrato.

PSA non permite estimacións de materiais sobre os detalles de liña de contrato.

Os procesos que se admiten nun contrato de proxecto son a creación e confirmación de facturas. A creación de facturas crea un borrador dunha factura baseada en proxecto que inclúe todos os datos reais de vendas sen facturar ata a data actual.

A confirmación fai que o contrato sexa só de lectura e cambie o seu estado de **Borrador** a **Confirmado**. Despois de realizar esta acción, non pode desfacela. Dado que esta acción é permanente, é unha mellor práctica manter o contrato nun estado de **Borrador**.

As únicas diferenzas entre os borradores de contrato e os contratos confirmados son o seu estado e o feito de que os borradores de contrato se poden editar mentres que os contratos confirmados non poden editarse. A creación de facturas e o rastrexo de datos reais pódense realizar tanto nos borradores de contrato como nos contratos confirmados.

PSA non admite a modificación de pedidos en contratos ou proxectos.

## <a name="estimating-projects"></a>Estimación de proxectos

Pode estimar tempo e gastos en proxectos. PSA non permite estimacións de materiais ou tarifas nos proxectos.

As estimacións de tempo xéranse cando vostede crea unha tarefa e identifica os atributos dun recurso xenérico que se require para realizar a tarefa. As estimacións de tempo xéranse a partir de tarefas de programación. As estimacións de tempo non se crean se vostede crea membros xenéricos do equipo fóra do contexto da programación.

As estimacións de gastos introdúcense na grade na páxina **Estimacións**.

## <a name="understanding-estimation"></a>Comprensión da estimación

Utilice a seguinte táboa como guía para comprender a lóxica de negocio na fase de estimación.

| Escenario                                                                                                                                                                                                                                                                                                                                          | Rexistro de entidades                                                                                                                                                                                                       | Tipo de transacción | Clase de transacción | Información adicional                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|-------------|-----------------------------------------------------------------------------------|
| Cando necesite estimar o valor de vendas de tempo nunha oferta                                                                                                                                                                                                                                                                                    | Créase o rexistro de detalle de liña de oferta (QLD)                                                                                                                                                                               | Contrato do proxecto | Time        | O campo de orixe da transacción na fila QLD de vendas fai referencia a QLD de custo |
|                                                                                                                                                                                                                                                                                     | O sistema crea un segundo rexistro QLD para almacenar os valores de custo correspondentes. O sistema copia todos os campos non monetarios do QLD de vendas ao QLD de custo.                                                                                                                                                                               | Custo | Time        | O campo de orixe da transacción na fila de detalle de liña de oferta (QLD)de vendas fai referencia ao QLD de custo |
| Cando necesite estimar o valor de vendas de tempo nun contrato                                                                                                                                                                                                                                                                                 | Créase o rexistro de detalle de liña de contrato (CLD) do proxecto                                                                                                                                                                    | Contrato do proxecto | Time        | O campo de orixe da transacción na fila CLD de vendas fai referencia a CLD de custo      |
|                                                                                                                                                                                                                                                                                  | O sistema crea un segundo rexistro CLD para almacenar os valores de custo correspondentes. O sistema copia todos os campos non monetarios do CLD de vendas ao CLD de custo.                                                                                                                                                                    | Custo | Time        | O campo de orixe da transacción na fila CLD de vendas fai referencia a CLD de custo      |
| Cando o usuario describe un recurso nunha tarefa de proxecto                                                                                                                                                                                                                                                                                            | Créase un rexistro de liña de estimación para mostrar o valor de vendas da tarefa cando se crea unha tarefa con todas as dimensións de prezos necesarias. O rol e as unidades organizativas son as dimensións dos prezos de OOB Project Service | Contrato do proxecto | Time        |                                                                                   |
|     | Créase un rexistro de liña de estimación para mostrar o valor de custo da tarefa cando se crea unha tarefa con todas as dimensións de prezos necesarias. O sistema copia todos os campos non monetarios da liña de estimación de vendas ao á liña de estimación de custo. O rol e a unidade organizativa son as dimensións dos prezos de OOB PSA tanto para custo como para taxas de facturación.                                                                                                                                                                                                                | Custo             | Time           |                                                                                   |



## <a name="customizing-the-quote-line-detail-and-contract-line-detail-entities"></a>Personalización das entidades de detalle de liña de oferta e detalle de liña de contrato

Se engadiu un campo personalizado no detalle de liña de oferta e quere que o sistema introduza o valor do campo como valor predefinido na liña de custo relacionada que crea, use as ferramentas de rexistro dos complementos PreOperationContractLineDetailUpdate e PreOperationQuoteLineDetailUpdate. Estes complementos deben rexistrarse de novo despois de que se cambie o detalle da liña de oferta ou detalle da liña de contrato. Siga estes pasos para completar o proceso:

1. Abra PluginRegistrationTool e conéctese á súa instancia en liña.
2. Seleccione **Buscar** e busque o complemento para actualizar.

    ![Caixa de diálogo de árbore de busca](media/basic-guide-19.png)

3. Seleccione o complemento e, a seguir, na páxina principal, seleccione **Seleccionar**.
4. Seleccione o paso do complemento para actualizar, prema co botón dereito e logo seleccione **Actualizar**.

    ![Selección dun paso no complemento](media/basic-guide-20.png)

5. Na caixa de diálogo **Actualizar o paso existente**, no campo **Atributos de filtrado**, seleccione o botón de puntos suspensivos (**...**):
 
    ![Actualizar a caixa de diálogo de Paso existente](media/basic-guide-21.png)

6. Na caixa de diálogo **Seleccionar atributos**, seleccione as caixas de verificación dos atributos personalizados.

    ![Seleccionar a caixa de diálogo Atributos](media/basic-guide-22.png)

7. Seleccione **Aceptar** para pechar a caixa de diálogo e logo seleccione **Actualizar paso**.
 
    ![Actualizar o botón Paso](media/basic-guide-23.png)

8. Repita os pasos do 1 ao 7 para o segundo complemento.
9. Peche PluginRegistrationTool.


[!INCLUDE[footer-include](../includes/footer-banner.md)]