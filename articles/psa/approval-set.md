---
title: Conxuntos de aprobacións
description: Este tema ofrece información sobre o conxunto de aprobacións, as solicitudes e os subconxuntos desas operacións.
author: stsporen
manager: tfehr
ms.date: 05/28/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: ac73313420029ece740d0bdb9c21c7abaa9defc6
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116869"
---
# <a name="approval-sets"></a>Conxuntos de aprobacións

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Os conxuntos de aprobacións agrupan solicitudes de aprobación do grupo en subconxuntos de operacións máis pequenos. Esta agrupación permite que as aprobacións sexan procesadas en orde por Proxecto e permite reintentar e secuenciar. A agrupación mellora a fiabilidade e a rastrexabilidade do procesamento de aprobacións para grandes volumes de aprobacións.

Os conxuntos de aprobacións indican o estado global de procesamento dos seus rexistros relacionados. Cando un rexistro de aprobación se procesa usando un conxunto de aprobacións, o rexistro pasa de **Enviado** a **Aprobado**, e está desvinculado do conxunto de aprobacións. Se un rexistro falla cando se somete a aprobación, o rexistro permanecerá nun estado de **Enviado** e o conxunto de aprobacións márcase como erro. O conxunto de aprobacións rexistra a mensaxe de erro do fallo.

## <a name="processing-approvals-and-approval-sets"></a>Tramitación de aprobacións e conxuntos de aprobacións
As aprobacións que están na fila para o procesamento son visibles na vista **Aprobacións de procesamento**. O sistema tenta procesar todas as entradas varias veces de xeito asíncrono, o que inclúe tentar de novo unha aprobación se fallaron os intentos anteriores.

O campo **Vida útil do conxunto de aprobacións** rexistra o número de intentos que quedan para procesar o conxunto antes de que se marque como erro.

## <a name="failed-approvals-and-approval-sets"></a>Aprobacións e conxuntos de aprobacións con erros
A vista **Aprobacións con erros** mostra todas as aprobacións que requiren a intervención do usuario. Abra os rexistros de conxuntos de aprobacións asociados para identificar a causa do fallo.
Seleccionar **Tentar de novo** engade ao reconto de vida útil do conxunto de aprobacións, traslada o conxunto de aprobacións a un estado de **Procesando** e tenta procesar os rexistros restantes.

## <a name="configure-approval-sets"></a>Configurar conxuntos de aprobacións

###  <a name="enable-the-approval-sets-feature"></a>Activar a funcionalidade de Conxuntos de aprobacións
Antes de activar a funcionalidade de Conxuntos de aprobacións, comprobe que non hai aprobacións procesándose actualmente.

- Vaia á páxina **Parámetros do proxecto** e seleccione **Control de funcionalidades** > **Activar aprobacións modernas**.

### <a name="turn-off-the-approval-sets-feature"></a>Desactivar a funcionalidade de Conxuntos de aprobacións
Antes de desactivar a funcionalidade de Conxuntos de aprobación, comprobe que non hai aprobacións procesándose actualmente.

- Vaia á páxina **Parámetros do proxecto** e seleccione **Control de funcionalidades** > **Desactivar aprobacións modernas**.

### <a name="configuring-the-asynchronous-threshold"></a>Configuración do limiar asíncrono 
Cando se crean conxuntos de aprobacións, o procesamento móvese a un segundo plano cando o número de rexistros seleccionado para a aprobación supera o limiar indicado. Use o campo **Limiar asíncrono** para configurar cando o proceso de aprobación debe executarse de xeito síncrono ou asíncrono.
Os valores válidos son:

  - Cero: Todas as solicitudes deben procesarse de forma asíncrona. 
  - Números superiores a cero: As aprobacións só se procesan de xeito asíncrono cando o número de aprobacións enviado supera este valor.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
