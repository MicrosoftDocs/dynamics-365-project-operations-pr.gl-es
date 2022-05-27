---
title: Prezos de proxecto
description: Este tema fornece información sobre como funcionan os prezos en Dynamics 365 Project Service Automation.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/11/2019
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
ms.reviewer: johnmichalak
ms.openlocfilehash: c9a5e1ef52eec99ee580258b5dd6db9823cdb4cb
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8576452"
---
# <a name="project-pricing"></a>Prezos de proxecto 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation amplía a entidade Lista de prezos en Dynamics 365 Sales. 

## <a name="key-entities"></a>Entidades clave

Unha lista de prezos inclúe información ofrecida por catro entidades diferentes:

- **Lista de prezos** - Esta entidade almacena información sobre contexto, moeda, efectividade de data e unidade de tempo para o tempo de prezos. O contexto mostra se a lista de prezos expresa taxas de custo ou taxas de vendas. 
- **Moeda** - Esta entidade almacena a moeda dos prezos na lista de prezos. 
- **Data** - Esta entidade úsase cando o sistema intenta introducir un prezo por defecto nunha transacción. O prezo PSA selecciona a lista de prezos que ten efectividade de data que inclúe a data da transacción. Se os prezos de PSA atopan que máis dunha lista de prezos que é efectiva para a data da transacción está anexada á oferta, contrato ou unidade organizativa relacionada, entón ningún prezo será predefinido. 
- **Tempo** - Esta entidade almacena a unidade de tempo para a que se expresan os prezos, como taxas diarias ou horarias. 

A entidade Lista de prezos ten tres táboas relacionadas que almacenan os prezos:

  - **Prezo de rol** - Esta táboa almacena unha taxa para a combinación de valores de rol e unidade organizativa e úsase para establecer prezos baseados en roles para os recursos humanos.
  - **Prezo da categoría de transacción** - Esta táboa almacena os prezos por categoría de transacción e úsase para configurar prezos de categoría de gasto.
  - **Elementos da lista de prezos** - Esta táboa almacena os prezos dos produtos do catálogo.

> ![Configuración de prezos utilizando a lista de prezos.](media/basic-guide-12.png)
 
A lista de prezos é un cartón de tarifas. Un cartón de tarifas é unha combinación da entidade Lista de prezos e as filas relacionadas nas táboas de Prezo de rol, Prezo de categoría de transacción e Elementos da lista de prezos.

## <a name="resource-roles"></a>Roles do recurso

O termo *rol de recurso* refírese a un conxunto de habilidades, competencias e certificacións que unha persoa debe ter para realizar un conxunto específico de tarefas nun proxecto.

O tempo de recursos humanos soe ofertarse en función do rol que un recurso cumpre nun proxecto específico. Para o tempo de recursos humanos, PSA admite o custo e a facturación baseados no rol dos recursos. Pode fixarse o prezo do tempo en calquera unidade do grupo de unidades **Tempo**.

O grupo de unidades **Tempo** créase cando se instala PSA. Ten unha unidade predefinida de **Hora**. Non pode eliminar, cambiar o nome ou editar os atributos do grupo de unidades **Tempo** ou a unidade **Hora**. Non obstante, pode engadir outras unidades ao grupo de unidades **Tempo**. Se tenta eliminar o grupo de unidades **Tempo** ou a unidade **Hora**, pode causar fallos na lóxica de negocio de PSA.

> ![Configuración dos prezos por rol.](media/basic-guide-13.png)
 
## <a name="transaction-categories-and-expense-categories"></a>Categorías de transaccións e categorías de gasto

Normalmente factúranse ao cliente os gastos de viaxe e outros gastos nos que incorren os consultores do proxecto. PSA admite a fixación de prezos de categorías de gasto mediante listas de prezos. Os gastos de avións, hoteis e aluguer de vehículos son exemplos de categorías de gasto. Cada liña da lista de prezos para gastos especifica os prezos para unha categoría de gasto específica. Para a fixación de prezos de categorías de gasto, PSA admite os seguintes tres métodos:

- **A custo** - O custe do gasto factúrase ao cliente e non se aplica ningún sobreprezo.
- **Porcentaxe de sobreprezo** - A porcentaxe sobre o custo real factúrase ao cliente. 
- **Prezo por unidade** - Establécese un prezo de facturación para cada unidade da categoría de gasto. A cantidade que se factura ao cliente calcúlase en función do número de unidades de gasto que informa o consultor. Quilometraxe usa o método de prezo por unidade. Por exemplo, a categoría de gasto de quilometraxe pódese configurar para 30 dólares estadounidenses (USD) por día ou 2 USD por milla. Cando un consultor informa de quilometraxe nun proxecto, o importe a facturar calcúlase en función do número de millas que informou o consultor.

> ![Configuración de prezos para categorías de gasto.](media/basic-guide-14.png)
 
## <a name="project-sales-pricing-and-overrides"></a>Prezos de vendas e anulacións do proxecto

Para as ofertas e contratos de proxectos, a lista de prezos dun proxecto ten un padrón de anulación de prezos diferente do que ten unha lista de prezos de produtos. Nunha liña de oferta baseada en catálogo de produtos, pode anular o prezo aos roles e categorías directamente na liña de oferta, porque cada liña de oferta apunta exactamente a un elemento do catálogo. Non obstante, nunha liña de oferta baseada en proxectos, non pode anular o prezo aos roles e categorías directamente na liña de oferta. Para permitir os dous patróns de anulación distintos, PSA introduciu unha nova asociación de lista prezos, a lista de prezos do proxecto.

> [!NOTE]
> Recomendamos que teña unha lista de prezos independente para os recursos do proxecto e os elementos do seu catálogo, debido ás diferenzas de comportamento entre ambas cando anula os prezos.

Cada unha das seguintes entidades pode ter unha ou varias listas de prezos de vendas asociadas para os prezos de proxectos:

- Cliente (conta) 
- Oportunidade 
- Oferta 
- Contrato do proxecto

A asociación destas entidades cunha lista de prezos está indicada polas listas de prezos do proxecto. Pode asociar unha ou varias listas de prezos ás entidades de vendas Cliente, Oportunidade, Oferta e Contrato de Proxecto.

Non se introduce automaticamente unha lista de prezos do proxecto predefinida nun rexistro de clientes. Non obstante, pode anexar manualmente unha lista de prezos do proxecto ao rexistro de clientes. Non obstante, debe anexar manualmente unha lista de prezos do proxecto só cando teña un acordo de prezos personalizado co cliente. 

Cando unha lista de prezos do proxecto está anexada a unha entidade de vendas, PSA valida a seguinte información:

- A lista de prezos ten un contexto de **Vendas** 
- A moeda da lista de prezos coincide coa moeda do cliente. 

No contrato do proxecto, PSA usa a seguinte orde de precedencia para establecer automaticamente as listas de prezos de proxecto relacionadas:

1. Oferta
2. Oportunidade
3. Cliente 
4. Configuración global para PSA

Cando se introduce de xeito predeterminado unha lista de prezos do proxecto, PSA valida que a moeda coincide coa moeda do cliente e que as listas de prezos por defecto que se introduciron teñen un contexto de **Vendas**.

Pode asociar varias listas de prezos ás entidades de vendas Cliente, Oportunidade, Oferta e Contrato de Proxecto. Esta capacidade admite prezos predefinidos específicos da data para un contrato de proxecto de longa duración, onde pode requirir máis dunha lista de prezos para dar conta das actualizacións de prezos que se producen por mor da inflación. Non obstante, se as listas de prezos que asocie á entidade Cliente, Oportunidade, Oferta ou Contrato de proxecto teñen efectividade de datas superpostas, os prezos por defecto poderían ser incorrectos. Polo tanto, ten que asegurarse de que as listas de prezos do proxecto que teñan data de superposición non estean asociadas a esas entidades.

### <a name="deal-specific-price-overrides"></a>Anulación de prezos específicos da operación

En PSA, pode crear anulacións específicas de operacións para os prezos seleccionados nas listas de prezos do proxecto que se introducen de xeito predefinido nunha oferta ou nun contrato de proxecto.

Por defecto, un contrato de proxecto sempre recibe unha copia da lista de prezos de venda principal en lugar dunha ligazón directa a ela. Este comportamento axuda a garantir que os acordos de prezos que se realizan cun cliente para unha declaración de traballo (SOW) non cambian se cambia a lista de prezos principal.

Non obstante, nunha oferta, pode usar unha lista de prezos principal. Alternativamente, pode copiar unha lista de prezos principal e editala para crear unha lista de prezos personalizada que se aplica só a esa oferta. Para crear unha nova lista de prezos específica dunha oferta, na páxina **Oferta**, seleccione **Crear prezos personalizados**. Pode acceder á lista de prezos de proxecto específica da oferta só desde a oferta. 

Cando crea unha lista de prezos de proxecto personalizada, só se copian os compoñentes do proxecto da lista de prezos. Noutras palabras, unha nova lista de prezos creada como unha copia da lista de prezos de proxecto existente que se anexa na oferta, e esta nova lista de prezos só ten prezos de rol relacionados e os prezos da categoría de transacción.

> ![Visualización e configuración de prezos personalizados para un contrato de proxecto.](media/basic-guide-15.png)
  
## <a name="tracking-costs"></a>Rastrexo dos custos

PSA rastrexa os custos do uso de tempo de recursos humanos nos proxectos. Tamén rastrexa os custos para outros gastos nos que se incorre durante o proxecto, como os gastos de viaxe.

Do mesmo xeito que as taxas de facturación, as taxas de custos dos recursos humanos tamén se establecen mediante listas de prezos. Aquí están as principais diferenzas no comportamento da lista de prezos de custo e da lista de prezos de vendas:

- Non se pode anular a taxa de custo dun recurso nun proxecto, contrato ou oferta específicos. Non obstante, as taxas de facturación poden anularse segundo a operación se se realizan cambios específicos na natureza da operación. 

- A seguinte orde úsase para resolver unha lista de prezos de custo:

    1. A lista de prezos de custos que se anexa á unidade organizativa.
    2. A lista de prezos de custos que se anexa aos parámetros de Project Service. Debido a que se poden anexar listas de prezos en moitas moedas diferentes aos parámetros de Project Service, PSA fai unha equivalencia entre a moeda da unidade organizativa contratante do proxecto, o contrato ou a oferta e a moeda da lista de prezos de custos.
    3. Para os gastos, os métodos de prezos a custo e de sobreprezo sobre custo non se aplican ás listas de prezos de custos. Aínda que se utilicen estes métodos de prezos nas liñas de lista de prezos de custos para configurar os custos da categoría de transaccións, o sistema non os ignora e non se introduce ningún prezo de custo por defecto.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
