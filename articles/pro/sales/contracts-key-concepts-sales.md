---
title: Contratos de proxecto - Conceptos clave - lite
description: Este tema fornece información sobre os conceptos clave de contratos de proxecto.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ce37c9dd18fd01e599e8766389e42c066e182547
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177059"
---
# <a name="project-contracts---key-concepts---lite"></a>Contratos de proxecto - Conceptos clave - lite

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

Este tema fornece os conceptos clave que hai que ter en conta antes de comezar a empregar contratos de proxecto en Dynamics 365 Project Operations:

## <a name="contracting-unit"></a>Unidade de contratación

A unidade de contratación representa a división ou práctica propietaria da entrega do proxecto. Pode configurar custos de recursos para cada unidade de contratación. Cando especifique o custo do recurso para un recurso, tamén poderá configurar diferentes taxas de custo para os recursos. Esta unidade contratante toma prestados estes recursos doutra división ou prácticas dentro da empresa. As taxas de custo para os recursos denomínanse prezos de transferencia, préstamos de recursos ou prezos de intercambio. Cando configura as taxas de custo de pedir prestados recursos a outras divisións, utilice a moeda da división prestamista.

## <a name="cost-currency"></a>Moeda de custo

A moeda de custo é a moeda na que se informa dos custos na pantalla. Esta moeda derívase da moeda anexa ao campo **Unidade de contratación** no contrato e o proxecto. Os custos poden rexistrarse en calquera moeda cun proxecto. Non obstante, hai unha conversión de moeda desde a moeda na que se rexistraron os custos ata a moeda de custo do proxecto cando se mostra na pantalla.

Debido a que os tipos de cambio da plataforma Common Data Service (CDS) non poden ser efectivos nunha data, os totais en pantalla do custo poden cambiar co paso do tempo se actualiza os tipos de cambio de moeda. Non obstante, os custos tal como están rexistrados na base de datos permanecen inalterados porque os importes almacénanse na moeda na que se incorreron.

## <a name="sales-currency"></a>Moeda das vendas

A moeda das vendas en Project Operations é a moeda na que se rexistran e mostran os importes de vendas estimados e reais. A moeda de vendas tamén é a moeda na que se factura ao cliente polo acordo. Nun contrato de proxecto, a moeda de venda predefinida no rexistro do cliente ou da conta e pódese cambiar cando se crea o contrato. Cando se crea un contrato pechando unha oferta como gañada, a moeda do contrato é por defecto a moeda da oferta.

Cando crea un contrato de proxecto desde cero, o campo **Moeda de vendas** non se pode editar. As listas de prezos de produtos e proxectos están predefinidas en función desta moeda do contrato.

A diferenza dos custos, os valores das vendas só se poden rexistrar na moeda de vendas.

## <a name="billing-method"></a>Método de facturación

Normalmente hai dous tipos de modelos de contratación para proxectos: de taxa fixa e baseados no consumo. Estes modelos represéntanse en Project Operations como métodos de facturación con dous posibles valores:

- Tempo e material: Un modelo de contratación baseado no consumo onde cada custo incorrido está avalado polos ingresos correspondentes. Cando estime ou incorra en máis custos, tamén aumentarán as vendas estimadas e reais correspondentes. Especifique os límites non superables nas liñas de contrato que teñan este método de facturación que limita os ingresos reais. Os ingresos estimados non se ven afectados polos límites non superables.
- Prezo fixo: Un modelo de contratación de taxa fixa que indica que os valores de vendas serán independentes dos custos incorridos. O valor das vendas é fixo e non cambia cando estime ou incorra en máis custos.

## <a name="project-price-lists"></a>Listas de prezos de proxecto

As listas de prezos de proxecto son listas de prezos que se utilizan para os prezos predefinidos, non as taxas de custo, por tempo, gastos e outros compoñentes relacionados co proxecto. Pode haber varias listas de prezos. Cada lista de prezos ten a súa propia data de vixencia para cada contrato de proxecto. A superposición das datas de vixencia das listas de prezos de proxecto non se admite en Project Operations.

Cando se crea un contrato de proxecto ao gañar unha oferta de proxecto, as listas de prezos do proxecto cópianse co nome e a data do contrato incluídos. A copia desta información constitúe un prezo personalizado para os compoñentes do proxecto neste contrato de proxecto.

## <a name="product-price-lists"></a>Listas de prezos de produtos

As listas de prezos dos produtos se utilizan para os prezos predefinidos, non as taxas de custo, para as liñas baseadas en produto nun contrato. Só hai unha lista de prezos de produtos por contrato.

## <a name="transaction-classes"></a>Clases de transacción

Project Operations admite catro tipos de clases de transacción:

- Tempo
- Gasto
- Material
- Cota

Os valores de custos e vendas pódense estimar e incorrer nas clases de transaccións de tempo, gastos e material. A taxa é unha clase de transacción só con ingresos.

## <a name="work-entities-and-billing-entities"></a>Entidades de traballo e entidades de facturación

As entidades que representan o traballo son proxectos e tarefas. As entidades que representan aspectos de facturación son liñas de contrato. Pode vincular diferentes entidades de traballo a opcións de facturación vinculándoas a liñas de contrato.

## <a name="multi-customer-deals"></a>Ofertas de varios clientes

As ofertas de varios clientes teñen máis dun cliente ao que facturar nun acordo. Os exemplos comúns inclúen:

- Empresas OEM e os seus socios: Os socios e revendedores venden un produto con algúns servizos de valor engadido, normalmente implicando un acordo concreto cun cliente. O OEM ofrece financiar unha parte do proxecto. 

- Proxectos do sector público: Varios departamentos dun goberno local acordan financiar un proxecto e se lles factura de acordo cunha división previamente acordada. Por exemplo, un distrito escolar e o goberno local acordan financiar a construción dunha piscina.

## <a name="invoice-schedules"></a>Programacións de facturas

As programacións de facturas son específicas de cada liña de contrato e son necesarias para que a facturación automática funcione. As programacións de facturas créanse en función de certas datas de inicio e finalización e frecuencia de facturación. As programacións úsanse na fase do contrato cando se configura o proceso de creación automática de facturas. Cando se crea un contrato de proxecto a partir dunha oferta, a programación de facturas cópiase no contrato de proxecto a partir da oferta.

## <a name="changes-from-the-dynamics-365-sales-contract"></a>Cambios do contrato de Dynamics 365 Sales

Os contratos en Project Operations baséanse nos contratos de Dynamics 365 Sales. Non obstante, hai algunhas desviacións importantes na funcionalidade que debe ter en conta:

- Os contratos de Project Operations teñen dous tipos diferentes de liñas, unha para proxectos e outra para produtos.
- Os contratos de Project Operations teñen os seus propios elementos de formulario e IU regras de negocio, lóxica empresarial nos complementos e scripts do cliente que as diferencian dos contratos de Sales.

Por estes motivos, non debe usar indistintamente un contrato de vendas e un contrato de proxecto.
