---
title: Pechar unha oferta - lite
description: Este tema ofrece información sobre o peche dunha oferta en Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8ae5e14220ffecab5bcfa016d8d18e6ccfbc5b04be9a4e66cee26f8885125d31
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994319"
---
# <a name="close-a-quote---lite"></a>Pechar unha oferta - lite

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

Unha oferta de proxecto pódese pechar como gañada ou perdida. Pódese pechar un borrador de oferta porque as operacións Activar e Revisar de ofertas non son compatibles con Microsoft Dynamics 365 Project Operations.

## <a name="close-a-quote-as-won"></a>Pechar unha oferta como gañada

Cando pecha unha oferta de proxecto como Gañada, o estado establécese en Pechada e o motivo para o estado é Gañada. Pechar a oferta fai que a oferta de proxecto sexa de só lectura e se crea un borrador do contrato do proxecto que contén a información da oferta. Debido a que non se pode volver abrir unha oferta pechada, un diálogo de confirmación confirmará os seus cambios.

Se a oferta se anexa a unha oportunidade, calquera outra oferta de proxecto da oportunidade péchase automaticamente como Perdida.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Impacto financeiro de pechar unha oferta como Gañada

Se hai algún dato real nun proxecto mentres aínda está anexo a un borrador de oferta, só se rexistra o custo do tempo ou do gasto. Despois de pechar a oferta como Gañada, a aplicación refactorizará os custos revertendo os datos reais de custos máis antigos e creando novos datos reais de custos. A aplicación procesará estes custos reais en función do método de facturación da liña de contrato do proxecto asociado. Se os datos reais de custo fan referencia a unha liña de contrato de tempo e material, créanse as vendas sen facturar correspondentes cando se pecha a oferta e se crea o contrato do proxecto. Se os datos reais de custo fan referencia a unha liña de contrato de prezo fixo, a aplicación deixará de reprocesar os custos reais baseados nas regras de facturación divididas para os clientes do contrato do proxecto.

## <a name="closing-a-quote-as-lost"></a>Peche dunha oferta como perdida:

Cando pecha unha oferta de proxecto como Perdida, o estado establécese en Pechada e o motivo para o estado é Perdida. O peche da oferta fai que a oferta de proxecto sexa de só lectura. Debido a que non se pode volver abrir unha oferta pechada, antes de pechar unha oferta, un diálogo de confirmación confirmará os cambios.

Se a oferta do proxecto pechada como Perdida fai referencia a un proxecto nalgunha das súas liñas, ese proxecto tamén se marcará como Pechado. Cancélanse as reservas de recursos a partir dese día.

> [!NOTE]
> En Project Operations, pechar unha oferta como Gañada ou Perdida non afectará a ese estado da Oportunidade, que permanecerá aberta ata que se peche manualmente.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]