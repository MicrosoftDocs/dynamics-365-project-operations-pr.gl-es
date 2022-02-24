---
title: Información resumida sobre unha oferta de proxecto - lite
description: Este tema ofrece información sobre a información e a configuración que se aplican e afectan ás ofertas do proxecto. (Sales)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0a7fb3419536ca3a595ec339b971e32c11f9671e
ms.sourcegitcommit: df30839484ef278675c5c712af0f7ba66ed9cdd3
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 03/17/2021
ms.locfileid: "5663991"
---
# <a name="header-details-for-project-quotes"></a>Detalles da cabeceira para ofertas de proxecto

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

Este artigo explica a información que se aplica a unha oferta de proxecto. Isto inclúe a configuración que afecta a todas as liñas de oferta e información sobre a oferta que se resume en todos os elementos de liña para impulsar os KPI da oferta de proxecto.

A seguinte táboa indica os campos de información resumida dunha oferta de proxecto que son exclusivos de Dynamics 365 Project Operations ou teñen algúns cambios importantes no comportamento das ofertas de Dynamics 365 Sales.

| **Campo** | **Localización** | **Descrición** | **Impacto descendente** |
| --- | --- | --- | --- |
| Tipo | Separador Resumo (oculto) | Este campo de conxunto de opcións ten as seguintes opcións:</br>- Baseado en traballo (dispoñible só cando Project Operations están instalada)</br>- Baseado en elementos (dispoñible só cando Project Operations e Sales están instaladas)</br>- Baseado en mantemento de servizo (dispoñible cando se instala Dynamics 365 Field Service) | Cando usa a aplicación Project Operations, o valor deste campo configúrase automaticamente en **Baseado en traballo**. Isto clasifica a oferta como unha oferta baseada en proxecto. Unha oferta debería basearse no proxecto para activar todas as extensións e funcionalidades específicas do proxecto. |
| Cliente | Separador de resumo | Referencia á empresa ou ao rexistro da conta do cliente. Cando se crea unha oferta a partir dunha oportunidade, este campo copiase desde o campo correspondente na oportunidade. | A moeda da oferta de proxecto está predefinida en función da moeda do cliente. Non obstante isto se pode cambiar despois de gardar a oferta. |
| Xestor de contas | Separador de resumo | O nome do xestor da conta para este acordo. Cando se crea unha oferta a partir dunha oportunidade, este campo copiase desde o campo correspondente na oportunidade. | O xestor de contas é o responsable de xestionar a relación co cliente a través durante a realización deste proxecto. Baseada no rexistro de recursos reservables ligado ao xestor de contas, a unidade de contratación é a predefinida na oferta de proxecto. |
| Unidade de contratación | Separador de resumo | A unidade de organización que se encarga da entrega do proxecto ou proxectos asociados a esta oferta. Cando se crea unha oferta a partir dunha oportunidade, este campo copiase desde o campo correspondente na oportunidade. | A unidade de contratación é a división da empresa que executará os proxectos despois de pechar o acordo. Cada unidade de contratación ten unha moeda e esta moeda úsase para informar dos custos estimados e reais incorridos durante a execución do proxecto. |
| Lista de prezos de produtos | Separador de resumo | Esta é a lista de prezos que se usa para predefinir os prezos nas liñas de oferta baseada en produto. A lista de opcións deste campo mostra unha lista de listas de prezos onde a moeda da lista de prezos coincide coa moeda da oferta. Cando se crea unha oferta a partir dunha oportunidade, este campo copiase desde o campo correspondente na oportunidade. Este campo da oportunidade está predefinido no rexistro da conta pero se pode cambiar. | Cando se gaña a oferta, o valor do campo se copia ao contrato de proxecto que se crea. |
| Moeda | Separador de resumo | Isto indica a moeda que se usará para informar do valor deste acordo. Tamén é a moeda na que se facturará ao cliente se se gaña o acordo. Cando se crea unha oferta a partir dunha oportunidade, este campo copiase desde o campo correspondente na oportunidade. Este campo da oportunidade está predefinido no rexistro da conta pero o usuario o pode cambiar. | Despois de gardar unha oferta, este campo xa non se pode editar. Se utiliza para predefinir as listas de prezos de produtos e proxectos da oferta. A moeda da oferta utilízase para facer coincidir a moeda da lista de prezos. |
| Límite non superable | Separador de resumo | Isto indica o límite negociado do valor final que o cliente acepta para este acordo. | Este límite avalíase durante a execución e é aplicable a todos os elementos de liña e proxectos asociados a este acordo. |
| Data de entrega solicitada | Separador de resumo | Cando se crea unha oferta a partir dunha oportunidade, este campo copiase desde o campo correspondente na oportunidade. | Esta data úsase como data de finalización para xerar programacións de facturas. |

Abaixo amósanse os separadores e os KPI dispoñibles nunha oferta de proxecto que son exclusivos de Project Operations ou que teñen algúns cambios importantes no comportamento respecto ás ofertas de Sales:

| **Campo** | **Localización** | **Descrición** |
| --- | --- | --- |
| Análise da rendibilidade | Separador na oferta | O separador mostra os seguintes indicadores:</br>- Custo imputable total</br></br>- Custo non imputable total</br>- Ingresos totais</br>- Ingresos totais (base)</br>- Marxe bruto</br>- Marxe bruto axustado|
| Comparación coas expectativas do cliente | Separador na oferta | Este separador mostra os seguintes indicadores:</br>- Finalización estimada</br>- Finalización solicitada</br>- Orzamento do cliente</br>- Valor da oferta |
| Análise da oferta | Separador na oferta | Este separador resume os seguintes KPI principais para unha oferta de proxecto</br>- Comparación coas expectativas dos clientes respecto ao orzamento e á programación</br>- Marxe bruto</br>- Marxe bruto axustado |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
