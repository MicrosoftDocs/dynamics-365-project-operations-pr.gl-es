---
title: Pechar ofertas baseadas en proxecto
description: Este artigo ofrece información sobre o peche de ofertas en Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7b35417d4258a1e837fdf7a61bbcc303ec04a900
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824214"
---
# <a name="close-project-based-quotes"></a>Pechar ofertas baseadas en proxecto

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Pódese pechar unha cotización dun proxecto como **gañado** ou **perdida**. 

## <a name="close-a-quote-as-won"></a>Pechar unha oferta como gañada

Ao pechar unha oferta de proxecto como Gañada, o estado da oferta establecerase en **Pechada** e o motivo para o estado establecido en **Gañada**. Pechar as ofertas fai que sexan de só lectura e se crea un borrador do contrato do proxecto con toda a información da oferta. Debido a que non se pode volver abrir unha oferta pechada, antes de pechar unha oferta, un diálogo de confirmación confirmará os cambios.

O contrato do proxecto creado a partir dunha oferta de proxecto tamén está dispoñible no módulo de xestión e contabilidade de proxectos de Project Operations. Se un contrato de proxecto non está asociado a un proxecto en ningunha das súas liñas, este contrato de proxecto ponse a disposición como un contrato de proxecto inactivo e faise activo en canto un proxecto se asigna a polo menos unha das súas liñas de contrato.

Se a oferta se anexa a unha oportunidade, calquera outra oferta de proxecto da oportunidade péchase automaticamente como Perdida.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Impacto financeiro de pechar unha oferta como Gañada

Se houbo datos reais por tempo rexistrados nun proxecto mentres aínda está anexado a un borrador de oferta, só se rexistra o custo do tempo ou do gasto. Despois de pechar a oferta como Gañada, a aplicación refactorizará os custos revertendo os datos reais de custos máis antigos e creando novos datos reais de custos. A aplicación procesará estes custos reais en función do método de facturación da liña de contrato do proxecto asociado. Se os datos reais de custos fan referencia a unha liña de contrato de tempo e material, o sistema creará automaticamente os correspondentes datos reais de vendas non facturados para cando se peche a oferta e se cree o contrato do proxecto. Se os datos reais de custos fan referencia a unha liña de contrato de prezo fixo, a aplicación deixará de procesar os datos reais de custos en función das regras de facturación dividida para os clientes do contrato do proxecto.

Todos os datos reais reprocesados están dispoñibles no módulo de xestión e contabilidade do proxecto para que o contable do proxecto poida revisalos, actualizalos e contabilizalos no libro maior. 

## <a name="close-a-quote-as-lost"></a>Pechar unha oferta como Perdida

Ao pechar unha oferta de proxecto como Perdida, establecerase o estado en **Pechada** e motivo para o estado en **Perdida**. Pechar a oferta fai que sexa só de lectura. Debido a que non se pode volver abrir unha oferta pechada, antes de pechar unha oferta, un diálogo de confirmación confirmará os cambios.

Se a oferta proxecto pechada como Perdida ten un proxecto referenciado nalgunha das súas liñas, ese proxecto tamén se marcará como Pechado e cancelaranse as reservas de recursos a partir dese día.

> [!NOTE]
> En Project Operations, pechar unha oferta como Gañada ou Perdida non afectará a ese estado da Oportunidade, que permanecerá aberta ata que se peche manualmente.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
