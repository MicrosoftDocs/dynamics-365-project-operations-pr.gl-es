---
title: Conceptos clave de ofertas de proxecto
description: Este tema ofrece información sobre el uso de las ofertas de proxecto en Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 64d2fd9bab9452d71e8cd194fbab70edadf00b93
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896279"
---
# <a name="project-quote-key-concepts"></a>Conceptos clave de ofertas de proxecto

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_


Os seguintes son conceptos clave que hai que ter en conta antes de comezar a empregar ofertas de proxecto en Dynamics 365 Project Operations:

## <a name="contracting-unit"></a>Unidade de contratación

A unidade de contratación representa a división ou práctica propietaria da entrega do proxecto. Pode configurar custos de recursos para cada unidade de contratación. Cando especifique o custo do recurso para un recurso na unidade de contratación, tamén poderá configurar diferentes taxas de custo para os recursos que esta unidade de contratación toma en préstamo ou doutra división ou prácticas dentro da empresa. Denomínanse prezos de transferencia, préstamos de recursos ou prezos de intercambio. Cando configura o custo de pedir prestados recursos a outras divisións, tamén pode optar por configurar eses tipos de custo na moeda da división prestamista.

## <a name="cost-currency"></a>Moeda de custo

A moeda de custo en Project Operations é a moeda na que se informa dos custos. Esta moeda derívase da moeda anexa ao campo **Unidade de contratación** na oferta, o contrato e o proxecto. Os custos poden rexistrarse en calquera moeda cun proxecto. Non obstante, hai unha conversión de moeda desde os custos de moeda rexistrados ata a moeda de custo do proxecto.

Debido a que os tipos de cambio da plataforma CDS non poden ser efectivos nunha data, os totais en pantalla do custo poden cambiar co paso do tempo se actualiza os tipos de cambio de moeda. Non obstante, os custos rexistrados na base de datos permanecen inalterados porque os importes almacénanse na moeda na que se incorreron.

## <a name="sales-currency"></a>Moeda das vendas

A moeda das vendas en Project Operations é a moeda na que se rexistran e mostran os importes de vendas estimados e reais. Tamén é a moeda na que se factura ao cliente polo acordo. Nunha oferta de proxecto, a moeda de venda predefinida no rexistro do cliente ou da conta e pódese cambiar cando se crea a oferta. Despois de gardar a oferta, a moeda das vendas non se pode cambiar. As listas de prezos de produtos e proxectos están predefinidas en función da moeda de vendas da oferta.

A diferenza dos custos, os valores das vendas só se poden rexistrar na moeda das vendas.

## <a name="billing-method"></a>Método de facturación

Os proxectos normalmente teñen modelos de contratación baseados en taxas e consumo fixos. Isto represéntase en Project Operations como **Método de facturación** e ten dous valores, tempo e material e prezo fixo.

- **Tempo e material:** Trátase dun modelo de contrato baseado no consumo onde cada custo incorrido está avalado polos ingresos correspondentes. Cando estime ou incorra en máis custos, tamén aumentarán as vendas estimadas e reais correspondentes. Pode especificar límites non superables nas liñas de oferta que teñan este método de facturación. Isto limitará os ingresos reais. Os ingresos estimados non se ven afectados polos límites non superables.
- **Prezo fixo:** Este é un modelo de contrato de taxa fixa que indica que os valores de vendas serán independentes dos custos incorridos. O valor das vendas é fixo e non cambia cando estime incorra en máis custos.

## <a name="project-price-lists"></a>Listas de prezos de proxectos

As listas de prezos do proxecto son listas de prezos que se utilizan para os prezos predefinidos, non as taxas de custo, por tempo, gastos e outros compoñentes relacionados co proxecto. Pode haber varias listas de prezos e cada lista pode ter a súa propia data de vixencia para cada oferta de proxecto. A superposición das datas de vixencia das listas de prezos de proxecto non se admite en Project Operations.

## <a name="product-price-lists"></a>Listas de prezos de produtos

As listas de prezos dos produtos son listas de prezos que se utilizan para os prezos predefinidos, non as taxas de custo, para as liñas baseadas en produto nunha oferta. Só hai unha lista de prezos de produtos por oferta.

## <a name="transaction-classes"></a>Clases de transacción

Project Operations admite catro tipos de clases de transacción:

- Tempo
- Gasto
- Material
- Cota

Os valores de custos e vendas pódense estimar e incorrer nas clases de transaccións de tempo, gastos e material. A taxa é unha clase de transacción só con ingresos.

## <a name="work-entities-and-billing-entities"></a>Entidades de traballo e entidades de facturación

As entidades que representan o traballo son proxectos e tarefas. As entidades que representan a facturación son as liñas de oferta e as liñas de contrato. Pode vincular diferentes entidades de traballo a opcións de facturación asociándoas con liñas de oferta ou contrato.

## <a name="multi-customer-deals"></a>Ofertas de varios clientes

As ofertas de varios clientes prodúcense cando hai máis dun cliente ao que facturar. Entre os exemplos máis habituais están os seguintes:

- **Empresas OEM e os seus socios:** Os socios e revendedores venden un produto con servizos de valor engadido. Esta é normalmente unha situación na que durante un acordo concreto cun cliente, o OEM ofrécese a financiar unha parte do proxecto. 

- **Proxectos do sector público:** Varios departamentos dun goberno local acordan financiar un proxecto e se lles factura de acordo cunha división previamente acordada. Por exemplo, un distrito escolar e a cidade ou o departamento do goberno local acordan financiar a construción dunha piscina.

## <a name="invoice-schedules"></a>Programacións de facturas

As programacións de facturas son específicos de cada liña de oferta e tamén son opcionais. As programacións de facturas créanse en función de certas datas de inicio e finalización e frecuencia de facturación. As programacións de facturas úsanse na fase do contrato cando se configura o proceso de creación automática de facturas. Na fase de oferta, as programacións son opcionais. Cando se crean programacións de facturas na fase **Oferta**, cópianse no contrato do proxecto que se crea cando se gaña unha oferta do proxecto.

## <a name="changes-from-dynamics-365-sales-quote"></a>Cambios da oferta de Dynamics 365 Sales:

As ofertas de Project Operations baséanse nas ofertas de Dynamics 365 Sales. Non obstante, hai algunhas diferenzas importantes na funcionalidade que debe ter en conta:

- As accións **Revisar** e **Activar** non son compatibles.
- As ofertas de Project Operations teñen dous tipos de liñas diferentes. Unha é para proxectos e a outra é para produtos.
- As ofertas de Project Operations teñen os seus propios elementos de formulario e IU regras de negocio, lóxica empresarial nos complementos e scripts do cliente que as diferencian das ofertas de Sales.

Por estes motivos, non se recomenda empregar indistintamente unha oferta de Sales e unha oferta de Project Operations.
