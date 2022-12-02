---
title: Conxuntos de aprobacións
description: Este artigo explica como traballar con conxuntos de aprobacións, solicitudes e os subconxuntos desas operacións.
author: stsporen
ms.date: 02/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: ca205073edbce2b399aab3ae273d635c8af96765
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 09/16/2022
ms.locfileid: "9524914"
---
# <a name="approval-sets"></a>Conxuntos de aprobacións

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Os conxuntos de aprobacións agrupan solicitudes de aprobación do grupo en subconxuntos de operacións máis pequenos. Esta agrupación permite procesar as aprobacións por proxecto, nunha orde específica e permite reintentar e secuenciar. Agrupar as solicitudes de aprobación mellora a fiabilidade e rastrexabilidade do procesamento de aprobacións para grandes volumes de aprobacións.

Os conxuntos de aprobacións indican o estado global de procesamento dos seus rexistros relacionados. Cando un rexistro de aprobación se procesa usando un conxunto de aprobacións, o rexistro pasa de **Enviado** a **Aprobado**, e xa non está ligado ao conxunto de aprobacións. Se un rexistro falla cando se somete a aprobación, o rexistro permanecerá nun estado de **Enviado** e o conxunto de aprobacións márcase como erro. O conxunto de aprobacións rexistra a mensaxe de erro do fallo.

## <a name="processing-approvals-and-approval-sets"></a>Tramitación de aprobacións e conxuntos de aprobacións
As aprobacións que están na fila para o procesamento son visibles na vista **Aprobacións de procesamento**. O sistema procesa todas as entradas varias veces de xeito asincrónico, incluíndo reintentar unha aprobación se fallaron os intentos anteriores.

O campo **Vida útil do conxunto de aprobacións** rexistra o número de intentos que quedan para procesar o conxunto antes de que se marque como erro.

Os conxuntos de aprobación son procesados mediante a activación periódica baseada nun **Fluxo de nube** denominado **Project Service: programar de forma recorrente os conxuntos de aprobacións do proxecto**. Isto atópase na **Solución** denominada **Project Operations**. 

Asegúrese de que o fluxo estea activado completando os seguintes pasos.

1. Como administrador, inicie sesión en [flow.microsoft.com](https://powerautomate.microsoft.com).
2. Na esquina superior dereita, cambie ao ambiente que usa para Dynamics 365 Project Operations.
3. Seleccione **Solucións** para enumerar as solucións que están instaladas no ambiente.
4. Na lista de solucións, seleccione **Project Operations**.
5. Cambie o filtro de **Todos** a **Fluxos de nube**.
6. Verifique que o fluxo **Project Service: programar de forma recorrente os conxuntos de aprobacións do proxecto** está configurado en **Activado**. Se non está, seleccione o fluxo e logo seleccione **Activar**.
7. Verifique que o procesamento se produce cada cinco minutos revisando a lista de **Traballos do sistema** na zona de **Configuración** do seu ambiente de Project Operations Dataverse.

## <a name="failed-approvals-and-approval-sets"></a>Aprobacións e conxuntos de aprobacións con erros
A vista **Aprobacións con erros** indica todas as aprobacións que requiren a intervención do usuario. Abra os rexistros de conxuntos de aprobacións asociados para identificar a causa do fallo.
Seleccionar **Tentar de novo** engade ao reconto de vida útil do conxunto de aprobacións, traslada o conxunto de aprobacións a un estado de **Procesando** e tenta procesar os rexistros restantes.

## <a name="configure-approval-sets"></a>Configurar conxuntos de aprobacións

### <a name="enable-the-approval-sets-feature"></a>Activar a funcionalidade de Conxuntos de aprobacións
Antes de activar a funcionalidade de Conxuntos de aprobacións, comprobe que non hai aprobacións procesándose actualmente. Despois de activar esta función, non se pode desactivar.

- Vaia á páxina **Parámetros do proxecto** e seleccione **Control de funcionalidades** > **Activar aprobacións modernas**.

### <a name="configuring-the-asynchronous-threshold"></a>Configuración do limiar asíncrono 
Cando se crean conxuntos de aprobacións, o procesamento móvese a un segundo plano cando o número de rexistros seleccionado para a aprobación supera o limiar indicado. Use o campo **Limiar asíncrono** para configurar cando o proceso de aprobación debe executarse de xeito síncrono ou asíncrono. Seleccione un dos seguintes valores:

  - Cero: Todas as solicitudes deben procesarse de forma asíncrona. 
  - Números superiores a cero: As aprobacións só se procesan de xeito asíncrono cando o número de aprobacións enviado supera este valor.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
