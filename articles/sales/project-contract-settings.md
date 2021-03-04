---
title: Configuración de contrato de proxecto
description: Este tema ofrece información sobre os campos que afectan ás liñas de contrato e a información sobre o contrato que se resume en todos os elementos de liña.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2f29e396f8d30a5c5648b5c9937f1f20fbf72e89
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181135"
---
# <a name="project-contract-settings"></a>Configuración de contrato de proxecto

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Este tema ofrece información sobre campos que se aplican a todo o contrato do proxecto, incluídos os axustes que afectan a todas as liñas de contrato. Tamén se inclúe información sobre o contrato que se resume en todos os elementos de liña para impulsar os KPIs do contrato do proxecto.

A seguinte táboa indica os campos de información resumida nun contrato de proxecto que son exclusivos de Dynamics 365 Project Operations ou teñen algúns cambios importantes no comportamento respecto dos pedidos de vendas de Dynamics 365 Sales.

| Campo | Localización | Descripción | Impacto descendente |
| --- | --- | --- | --- |
| Tipo | Separador **Resumo** (oculto) | Este é un campo de conxunto de opcións coas seguintes opcións:</br>- **Baseado en traballo** (dispoñible só cando Project Operations están instalada)</br>- **Baseado en elementos** (dispoñible só cando Project Operations e Sales están instaladas)</br>- **Baseado en mantemento de servizo** (dispoñible cando se instala Dynamics 365 Field Service) | En Project Operations, o valor deste campo é por defecto **Baseado no traballo** e clasifica o contrato como un contrato baseado en proxecto. Un contrato debería basearse no proxecto para activar todas as extensións e funcionalidades específicas do proxecto. |
| Empresa propietaria | Separador **Resumo** | A entidade legal que contabiliza os custos e ingresos que derivados dos proxectos asociados a este contrato de proxecto. Cando se crea un contrato a partir dunha oferta, este campo copiase desde o campo correspondente na oferta. | A empresa propietaria equivale ao concepto de entidade legal no módulo **Xestión e contabilidade de proxectos** de Project Operations. Todos os custos e ingresos derivados deste proxecto contabilízanse no libro maior da empresa propietaria. |
| Cliente | Separador **Resumo** | A referencia á empresa ou ao rexistro da conta do cliente. Cando se crea un contrato a partir dunha oferta, este campo copiase desde o campo correspondente na oferta. | A moeda do contrato de proxecto está predefinida en función da moeda do cliente. A moeda pódese cambiar antes de gardar o contrato. |
| Xestor de contas | Separador **Resumo** | O nome do xestor da conta para este acordo. Cando se crea un contrato a partir dunha oferta, este campo copiase desde o campo correspondente na oferta. | O xestor de contas é o responsable de xestionar a relación co cliente a través durante a realización do proxecto. Baseada no rexistro de recursos reservables ligado ao xestor de contas, a unidade de contratación é a predefinida no contrato de proxecto. |
| Unidade de contratación | Separador **Resumo** | A unidade organizativa que é responsable da entrega dos proxectos asociados a este contrato. Cando se crea un contrato a partir dunha oferta, este campo copiase desde o campo correspondente na oferta. | A unidade contratante é a división da empresa que executa os proxectos. Cada unidade de contratación ten unha moeda e esta moeda úsase para informar dos custos estimados e reais incorridos durante o proxecto. |
| Lista de prezos de produtos | Separador **Resumo** | Esta é a lista de prezos que se usa para predefinir os prezos nas liñas de contrato baseado en produto. A lista despregable de opcións deste campo mostra unha lista de listas de prezos onde a moeda da lista de prezos coincide coa moeda do contrato. Cando se crea un contrato a partir dunha oferta, este campo copiase desde o campo correspondente na oferta. No contrato de proxecto, este campo está predefinido no rexistro da conta pero se pode cambiar. | Non hai ningunha relevancia descendente para este campo. |
| Moeda | Separador **Resumo** | A moeda empregada para informar do valor deste acordo e a moeda na que se facturará ao cliente. Cando se crea un contrato a partir dunha oferta, este campo copiase desde o campo correspondente na oferta. No contrato de proxecto, este campo está predefinido no rexistro da conta pero se pode cambiar. | Despois de gardar un contrato, este campo xa non se pode editar. Este campo utilízase para predefinir as listas de prezos de produtos e proxectos do contrato. A moeda do contrato utilízase para facer coincidir a moeda da lista de prezos. |
| Límite non superable | Separador **Resumo** | Este campo indica o límite negociado do valor final que o cliente aceptou para este acordo. | O límite avalíase durante a execución e é aplicable a todos os elementos de liña e proxectos asociados a este acordo. |
| Data de entrega solicitada | Separador **Resumo** | Cando se crea un contrato a partir dunha oferta de proxecto, este campo copiase desde o campo correspondente na oferta de proxecto. | Esta data úsase como data de finalización para xerar programacións de facturas. |

Os seguintes KPI están dispoñibles no separador **Execución do contrato** dun contrato de proxecto.

| Campo | Localización | Descripción |
| --- | --- | --- |
| Valor do contrato | Contrato xeral | O valor total do contrato do proxecto. |
| Importe facturado | Contrato xeral | A suma dos importes de todas as facturas correspondentes a este contrato. |
| Custo incorrido | Contrato xeral | A suma de todos os datos reais de custo rexistrados en todos os proxectos asociados ao contrato. |
| Marxe bruta | Contrato xeral | Importe facturado - Custo incorrido ata a data/importe facturado |
| Marxe prevista | Contrato xeral | (Valor do contrato - Custos estimados) / Valor do contrato Custos estimados = A suma de todos os custos estimados en todos os proxectos asignados ao contrato.|
| Valor do contrato | Liñas baseadas en proxecto | O valor da liña de contrato. |
| Importe facturado | Liñas baseadas en proxecto | Para a liña de contrato de prezo fixo: A suma dos importes de todos os datos reais de fitos de vendas facturadas contra esta liña de contrato en varias facturas creadas para este contrato. Para a liña de contrato de tempo e material: A suma dos importes de todos os datos reais de fitos de vendas facturadas imputables contra esta liña de contrato en varias facturas creadas para este contrato. |
| Custo incorrido | Liñas baseadas en proxecto | A suma de todos os datos reais de custo rexistrados en todos os proxectos asociados á liña de contrato. |
| Marxe bruta | Liñas baseadas en proxecto | (Importe facturado - Custo incorrido ata a data) / Importe facturado |
| Marxe prevista | Liñas baseadas en proxecto | (Importe da liña do contrato en moeda base - Custos estimados para a liña do contrato en moeda base) / Importe da liña do contrato en moeda base |
| Custo incorrido | Detalle dunha liña baseada en proxecto | Tempo: A suma do importe dos datos reais de custo de tempo rexistrados para este rol no proxecto asignado á liña de contrato. Gastos: A suma do importe dos datos reais de custo de todos os gastos rexistrados para esta categoría no proxecto asignado á liña de contrato. |
| Cantidade rexistrada | Detalle dunha liña baseada en proxecto | Tempo: toda a cantidade de tempo dos datos reais de custo de tempo para un rol no proxecto que está asignado a esta liña de contrato. Gastos: Todas as cantidades para esta categoría de gasto nos datos reais de custo de gasto no proxecto asígnanse a esta liña de contrato. |
| Importe facturado | Detalle dunha liña baseada en proxecto | Para unha liña de contrato de prezo fixo, este campo déixase en branco no nivel de detalle e só se mostra no nivel de liña de contrato. Para unha liña de contrato de tempo e material, os cálculos complétanse no nivel de detalles. Os detalles mostran a suma do importe de todas as liñas de ingresos facturados contra esta liña de contrato que son imputables. |
| Cantidade facturada | Detalle dunha liña baseada en proxecto | Para unha liña de contrato de prezo fixo, este campo déixase en branco no nivel de detalle e só se mostra no nivel de liña de contrato. Para unha liña de contrato de tempo e material, os cálculos complétanse no nivel de detalles para tempo e gastos. Tempo: A suma das horas de todas as liñas de ingresos facturados para este rol contra esta liña de contrato que son imputables. Gastos: Todas as cantidades para esta categoría de gasto nos datos reais de custo de gasto no proxecto asígnanse a esta liña de contrato. |
| Valor do contrato | Liñas baseadas en produto | O valor da liña de contrato desta liña de contrato baseada en produto. |
| Importe facturado | Liñas baseadas en produto | A suma dos importes de todas as liñas de facturación contra esta liña de contrato baseado en produtos en varias facturas creadas para este contrato. |
| Custo incorrido | Liñas baseadas en produto | A suma de todos os datos reais de custo para a liña de contrato baseado en produto. |
| Marxe bruta | Liñas baseadas en proxecto | Importe facturado - Custo incorrido ata a data/importe facturado |
| Marxe prevista | Liñas baseadas en produto | (Valor da liña de contrato - Custos estimados para a liña de contrato) / Valor da liña de contrato |


[!INCLUDE[footer-include](../includes/footer-banner.md)]