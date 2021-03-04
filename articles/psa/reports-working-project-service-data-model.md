---
title: Traballo co modelo de datos de Project Service Automation
description: Este tema fornece información sobre como traballar co modelo de datos.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: d8c212ef2c9fd9dcd6be0b8f0a31aa5a948176bc
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147651"
---
# <a name="working-with-the-project-service-automation-data-model"></a>Traballo co modelo de datos de Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]
[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Service Automation estende outras entidades de aplicacións e introduce as súas propias entidades no modelo de datos de Common Data Service. Este tema describe algunhas das entidades que atopará en escenarios típicos de informes de PSA.

## <a name="reporting-on-opportunities"></a>Informes sobre oportunidades

Project Service Automation estende a entidade **Oportunidade** de Dynamics 365 Sales engadindo campos que permiten escenarios baseados en proxectos. Estes campos identifícanse cun nome de esquema prefixado con **msdyn\_**. Un novo campo importante para informar sobre as oportunidades de PSA é **Tipo de pedido**. Un valor de **Baseado no traballo** para este campo indica que a oportunidade é unha oportunidade de PSA. Outros campos que se engadiron á entidade inclúen **Organización contratante**, que capta a organización que está a manter a oportunidade, e **Xestor de contas**, que capta o nome do xestor de contas que é o responsable da oportunidade.

A entidade **Liña de oportunidade** tamén inclúe campos relacionados co Project Service. **Método de facturación** indica se a liña de oportunidade debe facturarse por tempo ou por materiais ou con prezo fixo e **Proxecto** captura o nome do proxecto que está apoiando a oportunidade. Outros campos dos que pode informar capturan os custos e os importes do orzamento do cliente para o elemento de liña.

## <a name="reporting-on-quotes"></a>Informes sobre ofertas

PSA amplía a entidade **Oferta** de Vendas engadindo campos relacionados co proxecto. **Tipo de pedido** distingue as ofertas de PSA das ofertas que non son de PSA. Un valor de **Baseado en traballo** para este campo indica que a oferta é unha oferta de PSA. Outros campos que poden ser relevantes para informar sobre ofertas de PSA inclúen campos de cantidade, como **Custos imputables**, **Custos non imputables**, **Marxe bruta**, **Estimacións** e **Orzamento**. Outros campos útiles indican se a oferta é rendible, se se completará antes do prazo e se cumpre as expectativas orzamentarias do cliente.

PSA tamén amplía a entidade **Liña de oferta** de Vendas. Un campo que PSA engade é **Método de facturación**, que indica como se facturará a liña de oferta (tempo e materiais ou prezo fixo). Outros campos que se engadiron á entidade capturan o proxecto relacionado que apoia a liña de oferta, facturación, custo e orzamento.

PSA tamén engade novas entidades relacionadas coas ofertas ao modelo de datos de Dynamics 365. Aquí van algúns exemplos:

- **Detalle da liña de oferta** - Esta entidade contén os detalles da estimación do proxecto da liña de oferta. Ten dous rexistros para cada liña de oferta. Un rexistro almacena custo e os detalles de custo e custo da liña de oferta, e outro rexistro almacena o importe das vendas e os detalles das vendas da liña de oferta.
- **Programación de facturas da liña de oferta** - Esta entidade contén a programación de facturación da liña de oferta. Esta programación xérase en función da frecuencia de facturación atribuída á liña de oferta.
- **Fito de liña de oferta** - Esta entidade contén os fitos de facturación das liñas de oferta de prezo fixo.
- **Subdivisión de análise da liña de oferta** - Esta entidade contén os detalles financeiros da liña de oferta. Estes detalles poden ser útiles para informar de importes de vendas ofertadas e custo estimado por varias dimensións.

Outras entidades que PSA engade ás ofertas son **Lista de prezos do proxecto da liña de oferta**, **Categoría de recursos de liña de oferta** e **Categoría de transacción de liña de oferta**.

![Diagrama que mostra a oferta, a liña de oferta e as relacións do proxecto](media/PS-Reporting-image2.png "Diagrama que mostra a oferta, a liña de oferta e as relacións do proxecto")

## <a name="reporting-on-project-contracts"></a>Informes sobre contratos do proxecto

PSA amplía a entidade **Pedido** de Vendas que se emprega cando se rexistran contratos de proxecto. Engade un campo novo importante, **Tipo de pedido**, que identifica o contrato como un contrato de proxecto de PSA en lugar dun pedido de vendas. Un valor de **Baseado no traballo** para este campo indica que o pedido é un contrato de proxecto de PSA. Outros campos novos que se engaden á entidade **Pedido** capturan detalles sobre os custos, o estado do contrato de PSA e a organización propietaria do contrato.

PSA tamén amplía a entidade **Liña de pedido de vendas**. Entre os campos que engade están os campos que capturan o método de facturación (tempo e materiais ou prezo fixo), os importes do orzamento do cliente e o proxecto subxacente.

PSA tamén engade novas entidades deseñadas para contratos de proxecto. Aquí van algúns exemplos:

- **Detalle da liña de contrato do proxecto** - Esta entidade contén os detalles de nivel de liña que se acumulan ao importe da liña de contrato. Estes poden ser tan detallados como as liñas xeradas a partir dunha programación de proxecto a nivel de tarefa.
- **Programación de facturas da liña de contrato** - Esta entidade contén a programación de facturación que se xera en función da frecuencia de facturas asignada á liña de contrato.
- **Fito de contrato** - Esta entidade contén os fitos de facturación para liñas de contrato que teñen un prazo de facturación de prezo fixo.

Outras entidades que PSA engade aos contratos son **Lista de prezos do proxecto da liña de contrato do proxecto**, **Categoría de recursos de liña de contrato do proxecto** e **Categoría de transacción de liña de contrato do proxecto**.

![Diagrama que mostra o pedido, a liña de pedido e as relacións do proxecto](media/PS-Reporting-image3.png "Diagrama que mostra o pedido, a liña de pedido e as relacións do proxecto")

## <a name="reporting-on-projects"></a>Informes sobre proxectos

A entidade **Proxectos** e as entidades relacionadas son exclusivas de PSA. **Proxecto** é a entidade de primeiro nivel que se emprega para capturar o traballo e o custo das operacións. Este é unha lista das entidades relacionadas:

- **Membro do equipo de proxecto** - Esta entidade contén detalles sobre os recursos reservables asignados ao proxecto. Estes recursos poden ser recursos xenéricos reservables ou poden ser recursos nomeados reservables que son introducidos polo xestor do proxecto ou xerados a partir da programación do proxecto.
- **Tarefa do proxecto** - Esta entidade contén as tarefas que compoñen o plan ou a programación do proxecto.
- **Atribución de recursos** - Esta entidade contén a atribución de tarefas para o recurso reservable.
- **Requisito de recursos** - Esta entidade contén os requisitos para todos os membros do equipo de recursos xenéricos.
- **Estimación** e **Liña de estimación** - Estas entidades teñen unha relación de cabeceira/liña e conteñen estimacións de gastos para o proxecto. As estimacións das tarefas almacénanse na entidade **Estimación de recursos**.

![Diagrama que mostra o requisito de recursos e as relacións do proxecto](media/PS-Reporting-image4.png "Diagrama que mostra o requisito de recursos e as relacións do proxecto")

## <a name="reporting-on-resources"></a>Informes sobre recursos

Os recursos do proxecto utilizan as entidades **Recurso reservable** de Universal Resource Scheduling (URS) que se comparten con outras aplicacións, como Microsoft Dynamics 365 Field Service. Esta é unha lista das entidades que podería ter que empregar cando informe sobre os recursos do proxecto:

- **Recurso reservable** - Esta entidade representa o usuario, contacto, recurso xenérico, conta, grupo ou equipo que se emprega no equipo do proxecto.
- **Características dos recursos reservables** - Esta entidade inclúe as habilidades, certificacións ou educación do recurso. As características poden ter valores de clasificación definidos polo modelo de clasificación.
- **Categoría de recurso reservable** - Esta entidade representa o rol do recurso reservable.
- **Reservas de recursos reservables** - Esta entidade representa o tempo que está reservado nos proxectos para o recurso. Cada reserva ten unha entidade de cabeceira e entidades de liña, e cada liña ten un estado que representa o estado da reserva.

![Diagrama que mostra as relacións de características de recursos reservables](media/PS-Reporting-image5.png "Diagrama que mostra as relacións de características de recursos reservables")

## <a name="reporting-on-actual-transactions"></a>Informes sobre transaccións reais

Cando aproba unha folla de control horario ou un gasto ou factura un contrato en PSA, a transacción comercial captúrase na entidade **Dato real**. Esta entidade pode servir de base para case todos os informes relacionados con financiamento en PSA. A entidade **Dato real** captura as transaccións de custo e vendas para o evento comercial. Tamén captura moitos atributos relevantes.

Cando estea a traballar coa entidade **Dato real**, é importante que entenda que transacción ou transaccións se rexistran na entidade e cando se rexistran as transaccións. Este é o fluxo típico cando se traballa con entradas de tempo (o fluxo para as entradas de gasto é similar):

1. Cando se garda a entrada de tempo, non se crean rexistros na entidade **Dato real**.
2. Cando se envía a entrada de tempo, non se crean rexistros na entidade **Dato real**.
3. Cando se aproba a entrada de tempo, créase un rexistro na entidade **Dato real** e tamén se pode crear un segundo rexistro. O primeiro rexistro almacena o custo da entrada do tempo. O segundo rexistro almacena o importe das vendas sen facturar da entrada de tempo. O segundo rexistro depende de que o proxecto teña un cliente, unha oferta ou unha liña de contrato atribuída.

    | Data do documento | Tipo de transacción | Clase de transacción | Cliente         | Contrato   | Recurso     | Rol do recurso | Tipo de facturación | Cantidade | Prezo por unidade | Importe |
    |---------------|------------------|-------------------|------------------|------------|--------------|---------------|--------------|----------|------------|--------|
    | 2/3/18        | Custo             | Time              | Casa de esquí alpino | CRM alpino | Rita Caramés | Xestor de proxectos   | Imputable   | 8.0      | 50.00      | 400.00 |
    | 2/3/18        | Vendas sen facturar   | Time              | Casa de esquí alpino | CRM alpino | Rita Caramés | Xestor de proxectos   | Imputable   | 8.0      | 100.00     | 800.00 |

    Estes dous rexistros son rexistros separados pero relacionados. Non son débitos nin créditos.

4. Se un contrato está asociado ao proxecto, cando se factura a entrada de tempo, créanse dous rexistros máis na entidade **Dato real**. En primeiro lugar, créase un importe negativo para o rexistro de vendas sen facturar. Este rexistro inverte esencialmente a venda sen facturar. En segundo lugar, créase unha transacción para a venda facturada. Unha vez máis, estes rexistros son rexistros separados pero relacionados, non débitos e créditos.

    | Data do documento | Tipo de transacción | Clase de transacción | Cliente         | Contrato   | Recurso     | Rol do recurso | Tipo de facturación | Cantidade | Prezo por unidade | Importe   |
    |---------------|------------------|-------------------|------------------|------------|--------------|---------------|--------------|----------|------------|----------|
    | 2/4/18        | Vendas sen facturar   | Time              | Casa de esquí alpino | CRM alpino | Rita Caramés | Xestor de proxectos   | Imputable   | - 8,0    | 100.00     | - 800,00 |
    | 2/4/18        | Vendas facturadas     | Time              | Casa de esquí alpino | CRM alpino | Rita Caramés | Xestor de proxectos   | Imputable   | 8.0      | 100.00     | 800.00   |

A entidade **Orixe da transacción** rexistra a orixe do rexistro **Dato real** e a entidade **Conexión de transaccións** rexistra os rexistros relacionados para o rexistro **Dato real**. Adicionalmente, o rexistro **Dato real** contén referencias ao proxecto, contrato de proxecto (pedido), recurso reservable e cliente.

![Diagrama que mostra a conexión da transacción, a orixe e as relacións reais](media/PS-Reporting-image6.png "Diagrama que mostra a conexión da transacción, a orixe e as relacións reais")


[!INCLUDE[footer-include](../includes/footer-banner.md)]