---
title: Conceptos exclusivos de ofertas baseadas en proxecto
description: Este artigo ofrece información sobre presupostos de proxectos en Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/02/2022
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 89867cfbe92f47d58b16da40b62d3d9dd6a15b64
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824325"
---
# <a name="concepts-unique-to-project-based-quotes"></a>Conceptos exclusivos de ofertas baseadas en proxecto

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Antes de comezar a utilizar as comiñas do proxecto en Microsoft Dynamics 365 Project Operations, debes ter en conta os seguintes conceptos clave.

## <a name="owning-company"></a>Empresa propietaria

A empresa propietaria representa a persoa xurídica propietaria da entrega do proxecto. O cliente da cotización debe ser un cliente válido desa persoa xurídica nas aplicacións de finanzas e operacións. A moeda da empresa propietaria e a moeda da unidade de contratación seleccionada nunha cotización baseada no proxecto deben coincidir.

## <a name="contracting-unit"></a>Unidade de contratación

Unha unidade de contratación representa a división ou práctica propietaria da entrega do proxecto. Pode configurar custos de recursos para cada unidade de contratación. Cando especifica os custos de recursos para un recurso nunha unidade de contratación, pode configurar diferentes taxas de custo para os recursos dos que a unidade de contratación toma préstamos ou para outras divisións ou prácticas da empresa. Estes tipos de custo denomínanse prezos de transferencia, préstamo de recursos ou prezos de cambio. Cando configuras o custo dos recursos de préstamo doutras divisións, podes configurar as taxas de custo na moeda da división de préstamos.

## <a name="cost-currency"></a>Moeda de custo

A moeda de custo en Operacións do proxecto é a moeda na que se informan os custos. Esta moeda derívase da moeda que está anexa ao campo **Unidade de contratación** na cotización, contrato e proxecto. Os custos dun proxecto pódense rexistrar en calquera moeda. Non obstante, hai unha conversión de moeda da moeda na que se rexistraron os custos á moeda de custo do proxecto.

Dado que os tipos de cambio da Dataverse plataforma non poden ser efectivos para a data, os totais de custo en pantalla poden cambiar co paso do tempo se actualizas os tipos de cambio de moeda. Non obstante, os custos que se rexistran na base de datos permanecen inalterados, porque os importes almacénanse na moeda na que se incorreron.

## <a name="sales-currency"></a>Moeda das vendas

A moeda de vendas en Project Operations é a moeda na que se rexistran e mostran os importes de vendas estimados e reais. Tamén é a moeda na que se factura ao cliente polo acordo. Para unha cotización de proxecto, establécese unha moeda de vendas predeterminada a partir do rexistro do cliente ou da conta e pódese cambiar cando se crea a cotización. Non obstante, a moeda de vendas non se pode cambiar despois de gardar a cotización. As listas de prezos predeterminadas de produtos e proxectos establécense en función da moeda de vendas da cotización.

A diferenza dos custos, os valores de vendas pódense rexistrar **só** na moeda de vendas.

## <a name="billing-method"></a>Método de facturación

Os proxectos adoitan ter modelos de contratación a tarifa fixa e baseados no consumo. En Operacións do proxecto, o modelo de contratación dun proxecto está representado polo método de facturación. O método de facturación ten dous valores: tempo e material e prezo fixo.

- **Tempo e material** – Un modelo de contratación baseado no consumo no que cada custo que se incorre está respaldado polos ingresos correspondentes. Cando estime ou incorra en máis custos, tamén aumentarán as vendas estimadas e reais correspondentes. Pode especificar límites non superables nas liñas de oferta que teñan este método de facturación. Deste xeito, pode limitar os ingresos reais. Os ingresos estimados non se ven afectados polos límites de non exceder.
- **Prezo fixo** – Un modelo de contratación de tarifa fixa no que os valores das vendas son independentes dos custos nos que se incorre. O valor das vendas é fixo e non cambia cando estime ou incorra en máis custos.

## <a name="project-price-lists"></a>Listas de prezos de proxectos

As listas de prezos do proxecto son listas de prezos que se usan para introducir prezos predeterminados, non taxas de custo, para o tempo, os gastos e outros compoñentes relacionados co proxecto. Pode haber varias listas de prezos e cada lista pode ter a súa propia data de vixencia para cada oferta de proxecto. Project Operations non admite a superposición de datas de vixencia para as listas de prezos do proxecto.

## <a name="product-price-lists"></a>Listas de prezos de produtos

As listas de prezos dos produtos son listas de prezos que se usan para introducir prezos predeterminados, non taxas de custo, para as liñas baseadas en produtos nunha cotización. Só hai unha lista de prezos de produtos por cotización.

## <a name="transaction-classes"></a>Clases de transacción

Project Operations admite catro tipos de clases de transacción:

- Tempo
- Gasto
- Material
- Cota

Os valores de custo e de vendas pódense estimar e producirse en **Tempo**, **Gasto** e **Material** clases de transacción. **As tarifas** é unha clase de transacción só con ingresos.

## <a name="work-entities-and-billing-entities"></a>Entidades de traballo e entidades de facturación

Proxectos e Tarefas son entidades que representan o traballo. As liñas de cotización e as liñas de contrato son entidades que representan a facturación. Pode vincular diferentes entidades de traballo ás opcións de facturación asociándoas con liñas de cotización ou liñas de contrato.

## <a name="multi-customer-deals"></a>Ofertas de varios clientes

As ofertas multicliente prodúcense cando hai máis dun cliente por factura. Aquí tes algúns exemplos típicos:

- **As empresas fabricantes de equipos orixinais (OEM) e os seus socios** – Os socios e revendedores venden un produto que inclúe servizos de valor engadido. Durante un acordo cun cliente, o OEM adoita ofrecer financiar parte do proxecto.
- **Proxectos do sector público** – Varios departamentos dun goberno local acordan financiar un proxecto e factúranse segundo unha división previamente acordada. Por exemplo, un distrito escolar e a cidade ou o departamento do goberno local acordan financiar a construción dunha piscina.

## <a name="invoice-schedules"></a>Programacións de facturas

Os calendarios de facturas son específicos para cada liña de cotización e son opcionais. Os calendarios de facturas créanse en función de datas específicas de inicio e finalización e unha frecuencia de factura. Utilízanse durante a fase do contrato, cando se configura o proceso de creación automática de facturas. Durante a fase de cotización, os calendarios de facturas son opcionais. Se se crean durante a fase de cotización, cópiase no contrato do proxecto que se crea cando se gaña unha cotización do proxecto.

## <a name="differences-from-dynamics-365-sales-quotes"></a>Diferenzas coas cotizacións de Dynamics 365 Sales

Os presupostos de Project Operations baséanse nos presupostos de Dynamics 365 Sales. Non obstante, hai algunhas diferenzas importantes na funcionalidade que debe ter en conta:

- As cotizacións de Project Operations teñen dous tipos diferentes de liñas: unha para proxectos e outra para produtos.
- Os presupostos de Project Operations teñen a súa propia páxina e elementos de interface de usuario (UI), regras comerciais, lóxica empresarial en complementos e scripts do lado do cliente que os diferencian dos presupostos de vendas.
- En Vendas, pode anexar varios pedidos a unha única cotización de vendas. En Operacións do proxecto, só pode anexar un contrato de proxecto a unha cotización do proxecto.
- Cando gañas unha cotización de vendas, a oportunidade relacionada pode permanecer aberta. Despois de gañar unha oferta de proxecto, a oportunidade relacionada péchase.
- Unha cotización de venda non inclúe algúns campos e conceptos que inclúe unha cotización do proxecto. Os campos inclúen **Unidade contratante**, **Xestor de conta** e **Facturar ao nome de contacto**.
- Os presupostos de venda e de proxecto identifícanse co campo conxunto de opcións-based **Tipo** . Para unha cotización de venda, o valor deste campo é **Baseado en artigos**. Para unha cotización de proxecto, o valor é **Baseado no traballo**.

Debido a estas diferenzas, non recomendamos que utilices os presupostos de vendas e os presupostos de operacións de proxectos de xeito intercambiable.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
