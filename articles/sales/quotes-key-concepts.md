---
title: Ofertas - Conceptos clave
description: Este tema ofrece información sobre as ofertas e as ofertas de vendas dispoñibles en Project Operations.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 8a1b5152b76cbcdfb5160a0af78eceec2c42b9a13dfc76701b6ad935318c7ba8
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997874"
---
# <a name="concepts-unique-to-project-based-quotes"></a>Conceptos exclusivos de ofertas baseadas en proxecto

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

En Dynamics 365 Project Operations, hai dous tipos de ofertas: ofertas de proxecto e ofertas de vendas. Os dous tipos de ofertas difiren das seguintes formas:

- **Grades para os elementos de liña**: Na oferta de vendas, só hai unha grade para elementos de liña. Nunha oferta de proxecto, hai dúas grades para os elementos de liña. Unha grade é para liñas de proxectos e a outra é para liñas de produtos.
- **Activación e revisións**: As ofertas de vendas admiten a activación e revisións. Estes procesos non se admiten nunha oferta de proxecto.
- **Pedidos anexados**: Pode anexar varios pedidos a unha oferta de vendas. Só se pode anexar un contrato de proxecto a unha oferta de proxecto.
- **Gañar unha oferta**: Cando gaña unha oferta de vendas, a oportunidade relacionada pode permanecer aberta. Despois de gañar unha oferta de proxecto, a oportunidade relacionada péchase.
- **Campos e conceptos**: Unha oferta de vendas non inclúe algúns campos e conceptos que se inclúen nunha oferta de proxecto. Os campos inclúen **Unidade contratante**, **Xestor de conta** e **Facturar ao nome de contacto**.  
- **Tipo**: As ofertas de vendas e as ofertas de proxecto tamén se identifican por un campo baseado en conxunto de opcións, **Tipo**. Para unha oferta de vendas, este campo ten o valor **Baseado en elementos**. Para unha oferta de proxecto, ten o valor **Baseado en traballo**.

Este tema centrase nos detalles das ofertas de proxecto.

Unha oferta de proxecto en Project Operations pode ter varios elementos ou liñas de oferta. De feito, unha oferta de proxecto ten dúas grades para os elementos de liña. Unha grade é para liñas baseadas en proxectos que permiten estimacións detalladas. A outra grade é para liñas baseadas en produtos que empregan un prezo de unidade simple e un enfoque baseado na cantidade.

- **Baseado en proxectos**: O valor ofertado determínase despois de estimar canto traballo é necesario. Pode estimar o traballo a un nivel alto, directamente como detalles de liña debaixo de cada liña de oferta ou baseándose en estimacións, usando un proxecto e un plan de proxecto. As liñas de ofertas baseadas en proxectos só se atopan en ofertas baseadas en proxectos creadas mediante Project Operations. Este tipo de liña de oferta é un formulario personalizado das liñas de oferta fóra de catálogo dispoñibles en Microsoft Dynamics 365 Sales.

- **Baseada en produtos**: A cantidade (valor ofertado) determínase en función da cantidade de unidades vendidas e do prezo de venda unitario do produto. O produto nunha liña baseada en produtos pode proceder dun catálogo de produtos en Sales ou pode ser un produto que defina vostede. Este tipo de liña de oferta tamén está dispoñible en ofertas baseadas en proxectos creadas mediante Project Operations.

O importe dunha oferta é o total das liñas baseadas en produtos e as liñas baseadas en proxectos.

> [!NOTE]
> As ofertas e liñas de oferta non son necesarias en Project Operations. Pode iniciar o proceso do proxecto cun contrato de proxecto (proxecto vendido). Non obstante, sempre se require unha oportunidade, independentemente de se comece cunha oferta ou un contrato de proxecto.

## <a name="project-based-quote-lines"></a>Liñas de oferta baseadas en proxecto

Unha liña de oferta baseada en proxectos en Project Operations ten os seguintes métodos de facturación:

- Hora e material
- Prezo fixo

### <a name="time-and-material"></a>Tempo e material

O método de facturación de tempo e material baséase no consumo. Cando seleccione este método de facturación, factúrase ao cliente cando o proxecto incorra en custos. As facturas créanse nunha frecuencia periódica baseada en datas. Durante o proceso de vendas, o valor indicado dun compoñente de tempo e material só proporciona ao cliente unha estimación do custo final. O fornecedor non se compromete a completar o proxecto con exactamente o valor ofertado. Os compoñentes de tempo e material aumentan o risco do cliente. Os clientes poden querer negociar cláusulas adicionais de valores máximos para minimizar o seu risco. Project Operations non admite a configuración de cláusulas de valores máximos.

### <a name="fixed-price"></a>Prezo fixo

No método de facturación de prezos fixos, un vendedor comprométese a entregar o proxecto cun custo fixo ao cliente. Factúrase ao o valor ofertado da liña de oferta de prezo fixo, independentemente dos custos nos que o vendedor incorra para entregar esa liña de oferta. O valor da liña de oferta de prezo fixo factúrase dunha das seguintes formas: 

- Como importe total ao inicio ou ao final do proxecto ou cando se alcanza un fito do proxecto. 
- Con unha frecuencia baseada en datas de prazos iguais do valor fixo na liña de oferta. Estes prazos coñécense como fitos periódicos.
- En prazos que teñen un valor monetario que está aliñado co avance do traballo ou fitos específicos que se conseguen no proxecto. Neste caso, o valor de cada prazo pode variar, pero todos deberán sumarse ao valor fixo na liña de oferta.

Project Operations admite os tres tipos de programas de facturas para liñas de oferta de prezo fixo.

## <a name="transaction-classification"></a>Clasificación da transacción

As organizacións de servizos profesionais normalmente ofertan e facturan aos seus clientes mediante a clasificación dos custos. Os custos están representados polas seguintes clasificacións de transaccións:

- **Tempo**: Esta clasificación representa o custo do tempo de traballo ou recursos humanos nun proxecto.
- **Gasto**: Esta clasificación representa todos os demais tipos de gastos nun proxecto. Debido a que os gastos poden clasificarse de maneira xeral, a maioría das organizacións crean subcategorías, como viaxes, aluguer de vehículos, hotel ou material de oficina.
- **Tarifa**: Esta clasificación representa gastos xerais, penalizacións e outros elementos que se cobran ao cliente. 
- **Imposto**: Esta clasificación representa os importes de impostos que os usuarios engaden mentres introducen gastos.
- **Transacción de material**: Esta clasificación representa os datos reais das liñas de produtos nunha factura de proxecto confirmada.
- **Fito**: Esta clasificación é utilizada pola lóxica de facturación de prezo fixo en PSA.

Unha ou máis destas clasificacións de transaccións poden asociarse a cada liña de oferta. Despois de gañar unha oferta, a asignación entre a clasificación da transacción e a liña de oferta transfírese á liña de contrato.
  
Por exemplo, unha oferta podería conter as dúas liñas de oferta seguintes: 

- Traballo de consultoría que emprega un método de facturación de tempo e material onde sexan aplicables clasificacións de transaccións de tempo e tarifas. Por exemplo, as transaccións de tempo e tarifa para o exemplo de proxecto **Aplicación de Dynamics AX** factúrase ao cliente en función do tempo e os materiais que se usen. 
- Gastos de viaxe relacionados que empregan un método de facturación de prezo fixo. Por exemplo, todos os gastos de viaxe para o exemplo de proxecto **Aplicación de Dynamics AX** factúranse a un valor monetario fixo.

> [!NOTE]
> A combinación de clasificacións de proxectos e transaccións de **Tempo**, **Gasto**, e **Tarifa** asociados a unha liña de oferta ou liña de contrato debe ser única. Se a mesma combinación de clase de proxecto e transacción está asociada a máis dunha liña de contrato ou liña de oferta, Project Operations non funcionará correctamente.

## <a name="billing-types"></a>Tipos de facturación

O campo **Tipo de facturación** define o concepto de imputabilidade. É un conxunto de opcións que ten os seguintes valores posibles:

- **Imputable**: O custo que acumula este rol/categoría é un custo directo que impulsa a execución do proxecto e o cliente pagará por este traballo. O pago pódese administrar como un arranxo de tempo e material ou de prezo fixo. Non obstante, o empregado que dedique este tempo recibirá o crédito correspondente pola súa utilización facturable.
- **Non Imputable**: O custo que acumula este rol/categoría considérase un custo directo que impulsa a execución do proxecto, aínda que o cliente non recoñece este feito en non pagará por este traballo. Ao empregado que dedique este tempo non se lle acreditará una utilización facturable por iso.
- **Gratuíto**: O custo que acumula este rol/categoría considérase un custo directo que impulsa a execución do proxecto e o cliente recoñece este feito. Ao empregado que dedique este tempo acreditaráselle una utilización facturable por iso. Non obstante, este custo non se cobra ao cliente.
- **Non dispoñible**: Os custos nos que se incorre en proxectos internos que non requiren o rastrexo de ingresos rastréxanse mediante esta opción.

## <a name="invoice-schedule"></a>Programa de facturas

Un programa de facturas é unha serie de datas nas que se produce a facturación dun proxecto. Opcionalmente pode crear un programa de facturas nunha liña de oferta. Cada liña de oferta pode ter o seu propio programa de facturas. Para crear un programa de facturas, ten que proporcionar os seguintes valores de atributo:

- Unha data de inicio da facturación 
- Unha data de entrega que representa a data de finalización da facturación do proxecto
- Unha frecuencia das facturas

Estes tres valores de atributo utilízanse para xerar un conxunto de datas provisional para establecer a facturación.

## <a name="invoice-frequency"></a>Frecuencia das facturas

A frecuencia de facturas é unha entidade que almacena valores de atributo que axudan a expresar a frecuencia de creación de facturas. Os seguintes atributos expresan ou definen a entidade de frecuencia de facturas:

- **Período**: Admítense períodos mensuais, quincenais e semanais. 
- **Execucións por período**: Para períodos semanais e quincenais, pode definir só unha execución por período. Para períodos mensuais, pode definir entre unha e catro execucións por período. 
- **Días de execución**: Os días nos que debe executarse a facturación. Pode configurar este atributo de dúas maneiras:
  - **Días laborables**: Por exemplo, pode especificar que a facturación se executa todos os luns ou cada dous luns. Os clientes que deban establecer a facturación para que se execute un día laborable poderán preferir este tipo de configuración. 
  - **Días de calendario**: Por exemplo, pode especificar que a facturación se execute os días 7 e 21 de cada mes. Algunhas organizacións poden preferir este tipo de configuración, porque axuda a garantir que a facturación se execute segundo un programa fixo cada mes.
  
### <a name="invoice-schedule-for-a-fixed-price-quote-line"></a>Programa de facturas para unha liña de oferta de prezo fixo

Para unha liña de oferta de prezo fixo, pode empregar a grade **Programa de facturas** para crear fitos de facturación que sexan iguais ao valor da liña de oferta.

- Para crear fitos de facturación divididos equitativamente, seleccione unha frecuencia de facturas, insira a data de inicio da facturación na liña de oferta e seleccione **Data de finalización solicitada** para a oferta na sección **Resumo** do encabezado da oferta. A continuación, seleccione **Xerar fitos periódicos** para crear fitos divididos equitativamente en función da frecuencia de facturas seleccionada. 
- Para crear un fito de facturación de cantidade global, cree un fito e, a seguir, introduza o valor da liña de oferta como importe do fito.
- Para crear fitos de facturación baseados en tarefas específicas no plan do proxecto, cree un fito e asígneo ao elemento de programación do proxecto na IU de fitos de facturación.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
