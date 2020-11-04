---
title: Crear ofertas de proxectos a partir de oportunidades
description: Neste tema se proporciona información sobre o a creación dunha oferta de proxecto a partir dunha oportunidade.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 606098473db479d0015e3a7a3c01a3d3b6de9db1
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076044"
---
# <a name="create-project-quotes-from-opportunities"></a>Crear ofertas de proxectos a partir de oportunidades

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Pódense crear ofertas a partir das oportunidades do proxecto das seguintes formas:

- Desde o separador **Ofertas** na páxina **Oportunidade de proxecto**
- Desde o fluxo do proceso de vendas de oportunidade
- Actualizando a referencia de oportunidade nunha oferta existente

## <a name="from-the-quotes-tab-of-the-project-opportunity-page"></a>Desde o separador Ofertas da páxina Oportunidade de proxecto

Para crear unha oferta de proxecto a partir dunha oportunidade, complete os pasos seguintes.

1. Abra a páxina **Oportunidade de proxecto** e seleccione o separador **Ofertas**. 
2. Na subgrade **Ofertas** , seleccione **+** para crear unha nova oferta de proxecto baseada na oportunidade. Todas as liñas da oportunidade e as listas de prezos do proxecto relacionadas cópianse á nova oferta desde a oportunidade.

## <a name="from-the-opportunity-sales-process-flow"></a>Desde o fluxo do proceso de vendas de oportunidade

Para crear unha oferta desde o fluxo do proceso de vendas da oportunidade, complete os pasos seguintes.

1. Desde o fluxo do proceso de vendas de Oportunidade, abra Oportunidade.
2. Seleccione a fase **Cualificar**. 
3. Seleccione **Seguinte** e logo seleccione **+ Crear** para crear unha nova oferta. A maior parte da información sobre o separador **Resumo** desta nova oferta será a da oportunidade por defecto. 
4. Introduza a información necesaria que falta ou actualice os valores predefinidos segundo sexa necesario no separador **Resumo** ,
5. Seleccione **Gardar**. A nova oferta créase e asóciase á oportunidade. Agora pode ver a información da oferta no separador **Ofertas** da páxina **Oportunidade**. 

   O proceso de vendas de Oportunidade pasa á seguinte fase, **Propoñer**.


## <a name="by-updating-the-opportunity-reference-on-an-existing-quote"></a>Actualizando a referencia de oportunidade nunha oferta existente

Unha oferta existente pódese vincular a unha oportunidade. Complete os seguintes pasos para actualizar a información de oportunidade sobre unha oferta existente.

1. Abra a páxina **Oferta** e seleccione o separador **Resumo**.
2. No campo **Oportunidade** , seleccione a oportunidade que desexa ligar á oferta. Pode ver a oferta na grade **Ofertas** da oportunidade. 
3. Usando o proceso de vendas de Oportunidade, a oportunidade pódese pasar á seguinte fase, **Propoñer**. 

   Cando traslade unha oportunidade a esta fase, pode seleccionar esta oferta nunha lista de ofertas asociadas a esta oportunidade. Se selecciona esta oferta, indica que seguirá adiante con ela.

   Todas as outras ofertas asociadas á oportunidade aínda estarán dispoñibles e estarán activas ata que se gañe unha delas. Pode mover o proceso de venda á etapa anterior **Cualificar** e escoller outra cita para seguir adiante con ela.
