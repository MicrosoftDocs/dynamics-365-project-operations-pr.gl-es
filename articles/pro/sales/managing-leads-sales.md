---
title: Xestionar clientes potenciais (Pro)
description: Neste tema se proporciona información sobre a xestión de clientes potenciais baseados en proxectos (pro).
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 005e36811643b0b1e98a686792cf39125ae97949
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896324"
---
# <a name="manage-leads-pro"></a>Xestionar clientes potenciais (Pro)

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

Os clientes potenciais baseados en proxectos pódense xestionar e cualificar en Project Operations. O proceso de xestión de clientes potenciais inclúe a creación de clientes potenciais baseados en traballo e a cualificación deses clientes potenciais. 

## <a name="list-of-project-sales-leads"></a>Lista de clientes potenciais de vendas de proxecto

Na sección **Vendas**, no panel de navegación esquerdo, abra a páxina de lista **Clientes potenciais** para ver unha lista de todos os rexistros de clientes potenciais no sistema. A lista de clientes potenciais que se mostran están baseada no traballo e outros tipos de clientes potenciais que se poden crear se tamén ten Dynamics 365 Sales ou aplicacións de Dynamics 365 Field Service.

Pode crear unha vista filtrada para ver só clientes potenciais baseados en proxectos creando un filtro no valor **Tipo**. Por exemplo, pode seleccionar mostrar só clientes potenciais baseados en traballo.

## <a name="creating-a-new-lead-for-a-project-based-deal"></a>Creación dun novo cliente potencial para unha oferta baseada en proxecto

Cando se cualifica un cliente potencial baseado en proxecto, créanse unha oportunidade e unha conta. Unha oportunidade baseada en proxecto é o punto de partida para as actividades de busca de vendas na fase Oportunidade. As oportunidades baseadas en proxectos teñen capacidades únicas necesarias para vender traballos de proxectos. Estas capacidades inclúen:

- Métodos de facturación de tempo e material e prezo fixo
- Listas de prezos efectivos de varias datas para recursos humanos, gastos e material incorridos en proxectos.

Para que un cliente potencial cualificado cree automaticamente unha oportunidade, configure o atributo **Tipo** como **Baseado en traballo** cando cree o cliente potencial. Se escolle un tipo diferente, o cliente potencial non creará unha oportunidade baseada en proxecto cando estea cualificado. Se a oportunidade baseada en proxecto non se crea, as capacidades específicas do proxecto non estarán dispoñibles nos procesos de venda descendentes.

A seguinte táboa inclúe información importante sobre o campo para un cliente potencial e as implicacións posteriores deses campos.

| **Campo** | **Localización** | **Relevancia, finalidade e orientación** | **Impacto descendente** |
| --- | --- | --- | --- |
| Tema | Separador Xeral | Este campo de texto debe conter unha breve descrición do acordo. | O tema do cliente potencial será o predefinido como tema da oportunidade e o nome da oferta e do contrato do proxecto. |
| Tipo | Separador Xeral | Este campo de conxunto de opcións ten as seguintes opcións:</br>- Baseado en traballo (dispoñible só cando Project Operations están instalada)</br>- Baseado en elementos (dispoñible só cando Project Operations e Sales están instaladas)</br>- Baseado en mantemento de servizo (dispoñible cando se instala Field Service) | Cando o valor deste campo está establecido en **Baseado en traballo** no cliente potencial, o cliente está cualificado para crear unha oportunidade baseada en proxecto. É necesaria unha oportunidade baseada en proxecto para activar todas as extensións e funcionalidades específicas do proxecto no proceso de vendas descendentes para este acordo. |
| Nome | Separador Xeral | Nome do contacto do posible interesado | Cando o cliente potencial está cualificado, créanse unha conta, un contacto e unha oportunidade. O nome do contacto é o valor establecido aquí. |
| Apelidos | Separador Xeral | Apelido do contacto do posible interesado | Cando o cliente potencial está cualificado, créanse unha conta, un contacto e unha oportunidade. O apelido do contacto é o valor establecido aquí. |
| Empresa | Separador Xeral | Nome da empresa do cliente interesado | Cando o cliente potencial está cualificado, créanse unha conta, un contacto e unha oportunidade. O nome da conta creada é o valor establecido aquí. |
| Moeda | Separador Detalles | Moeda do cliente interesado | Cando o cliente potencial está cualificado, créanse unha conta, un contacto e unha oportunidade. A moeda da conta creada é o valor establecido aquí. |

## <a name="qualify-a-new-project-based-lead"></a>Cualificar un novo cliente potencial baseado en proxecto

Clientes potenciais que teñen o valor **Tipo** establecido en **Baseado en traballo** chámanse clientes potenciais baseados en proxectos. Cando se cualifica un cliente potencial baseado en proxecto, créase o seguinte:

- Unha conta que usa o campo **Empresa** do cliente potencial.
- Un rexistro de contacto asociado á conta baseado nos valores dos campos **Nome** e **Apelidos** do cliente potencial.
- Unha oportunidade baseada en proxecto que ten o campo **Tipo** definido como &quot;**Baseado en traballo**.

Para obter información máis detallada sobre a cualificación de clientes potenciais, consulte[Cualificar ou converter clientes potenciais](https://docs.microsoft.com/dynamics365/sales-enterprise/qualify-lead-convert-opportunity-sales).

## <a name="business-process-flow-for-project-based-deals"></a>Fluxo do proceso de negocio para ofertas baseadas en proxecto

Os seguintes fluxos do proceso de negocio son compatibles con ofertas baseadas en proxecto en Project Operations:

- Proceso de negocio de cliente potencial a oportunidade
- Proceso de vendas de oportunidade

O proceso de negocio de cliente potencial a oportunidade admite as seguintes fases:

| Nome da fase | Entidade asignada | Funcionalidade |
| --- | --- | --- |
| Cualificar | Cliente potencial | Cualifique o cliente potencial para crear unha conta, un contacto e unha oportunidade. |
| Desenvolver | Oportunidade | Desenvolva a oportunidade de engadir máis información sobre o traballo involucrado, as partes interesadas e a competencia. |
| Propor | Oportunidade | Desenvolva a proposta e obteña a aprobación do equipo de revisión interno. |
| Pechar | Oportunidade | Gañe a oportunidade para pechar o acordo. |
