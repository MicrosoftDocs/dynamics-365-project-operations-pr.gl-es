---
title: Pechar ofertas
description: Este tema ofrece información sobre o peche dunha oferta en Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cc3b2cdeb1ac46b7d927c1f96e94e9154d3eebf8
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076053"
---
# <a name="close-quotes"></a>Pechar ofertas 

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

Unha oferta de proxecto pódese pechar como gañada ou perdida. As operacións de activar e revisar en ofertas non se admiten en Microsoft Dynamics 365 Project Operations, polo que se pode pechar un borrador de oferta.

## <a name="close-a-quote-as-won"></a>Pechar unha oferta como gañada

Ao pechar unha oferta de proxecto como Gañada, pecharase a oferta co estado establecido en Pechada e o motivo para o estado establecido en Gañada. Pechar a oferta fai que a oferta de proxecto sexa de só lectura e se crea un borrador do contrato do proxecto que contén a información da oferta. Debido a que non se pode volver abrir unha oferta pechada, aparece un diálogo de confirmación antes de que se fagan os cambios xa que non se pode volver abrir unha oferta pechada e os cambios son irreversibles.

Se a oferta se anexa a unha oportunidade, calquera outra oferta de proxecto da oportunidade péchase automaticamente como Perdida.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Impacto financeiro de pechar unha oferta como Gañada

Se houbo datos reais por tempo rexistrados nun proxecto mentres aínda está anexado a un borrador de oferta, só se rexistra o custo do tempo ou do gasto. Despois de pechar a oferta como Gañada, a aplicación refactorizará os custos revertendo os datos reais de custos máis antigos e creando novos datos reais de custos. A aplicación procesará estes custos reais en función do método de facturación da liña de contrato do proxecto asociado. Se os datos reais de custos fan referencia a unha liña de contrato de tempo e material, o sistema creará automaticamente os correspondentes datos reais de vendas non facturados para cando se peche a oferta e se cree o contrato do proxecto. Se os datos reais de custos fan referencia a unha liña de contrato de prezo fixo, a aplicación deixará de procesar os datos reais de custos en función das regras de facturación dividida para os clientes do contrato do proxecto.

## <a name="closing-a-quote-as-lost"></a>Peche dunha oferta como perdida:

Ao pechar unha oferta de proxecto como Perdida, establecerase o estado en Pechada e motivo para o estado en Perdida. O peche da oferta fai que a oferta de proxecto sexa de só lectura. Debido a que non se pode volver abrir unha oferta pechada, antes de pechar unha oferta, un diálogo de confirmación confirmará os cambios.

Se a oferta proxecto pechada como Perdida ten un proxecto referenciado nalgunha das súas liñas, ese proxecto tamén se marcará como Pechado e cancelaranse as reservas de recursos a partir dese día.

> [!NOTE]
> En Project Operations, pechar unha oferta como Gañada ou Perdida non afectará a ese estado da Oportunidade, que permanecerá aberta ata que se peche manualmente.
