---
title: Actualizar a páxina de inicio
description: Este tema mostra onde atopar información importante sobre as funcións novas e modificadas en Dynamics 365 Project Service Automation e o proceso para actualizar á versión máis recente.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 05/30/2019
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 for Project Service 3.x
author: rumant
ms.assetid: c92d0849-e40c-4a56-9719-34030fbf5991
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 55f544636f39fc4faae06fdd512f859800bb7b44
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751421"
---
# <a name="upgrade-home-page"></a>Actualizar a páxina de inicio

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a>Actualizar da versión 2.x ou 1.x á versión 3.x de PSA

### <a name="new-instances"></a>Novas instancias

A partir do 17 de maio de 2019, cando se selecciona Project Service Automation durante a subministración dunha nova instancia, a versión 3.x instálase por defecto.

### <a name="existing-instances"></a>Instancias existentes

Anteriormente, os clientes que tiñan unha instancia da versión 2.x de PSA e necesitaban actualizar á versión 3.x, que é a versión de PSA baseada na interface de cliente unificada (UCI) de PSA, debían contactar co Soporte técnico de Microsoft e proporcionar os detalles da súa instancia, de xeito que o servizo de asistencia puidese habilitar a instancia para a actualización á versión 3.x. A partir do 1 de marzo de 2020, os clientes que teñan unha instancia da versión 2.x de PSA e precisen actualizar á versión 3.x, poderán actualizar as súas instancias directamente desde o portal de administración sen ter que contactar co Soporte técnico de Microsoft.  

> [!NOTE]
> A versión 3.x de PSA inclúe cambios significativos. Foi creada no marco Interface unificada para axudar a proporcionar unha experiencia de usuario mellorada. A aplicación rediseñada ofrece unha interface de usuario (IU) uniforme e segue principios de deseño sensibles para unha visualización óptima en calquera tamaño de pantalla ou dispositivo. Houbo outros cambios ao longo da aplicación. Algunhas das áreas que foron modificadas inclúen fixación de prezos, reservas e atribución de recursos, tempo, gastos e aprobacións.

Antes de comezar o proceso de actualización, recomendámoslle que realice as seguintes tarefas:

- Verifique se Dynamics 365 Field Service e Project Service Automation están instalados na instancia identificada. Se se instalan ambas solucións, ten que planificar a actualización antes de continuar co uso regular da instancia.
- Revise coidadosamente os seguintes temas. O coñecemento e a comprensión dos cambios entre versións axudaranlle co proceso de actualización. Estes temas fornecen información sobre os cambios importantes en PSA, xunto con consideracións e recomendacións para planificar a súa actualización á versión 3.x.

    - [Novidades ou cambios na versión 3 de Project Service Automation](whats-new-changed-v3.md)
    - [Consideracións sobre a actualizaciñon - Project Service Automation versión 2.x ou 1.x a versión 3](upgrade-v3.md)

- Actualice a súa instancia de illamento de procesos para avaliar os cambios na súa instalación antes de actualizar a súa instancia de produción.

Despois de revisar os temas mencionados anteriormente e estar preparado para actualizar a PSA versión 3.x ou a versión baseada en UCI, envíe unha solicitude ao servizo de asistencia de Microsoft para que a actualización estea dispoñible desde o centro de administración. Na súa solicitude, indique os detalles da súa instancia.

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a>Versións máis antigas de PSA (versión PSA 2.x) nunha instancia de nova creación

A partir do 17 de maio de 2019, todas as novas instancias terán UCI como cliente predefinido. Para o aliñamento con este cambio, PSA versión 3.x e Field Service versión 8.x subministraranse por defecto, porque estas versións están deseñadas para funcionar co cliente UCI.

A partir do 1 de marzo de 2020, os clientes de Dynamics PSA xa non poderán crear novos ambientes con versións máis antigas de PSA, por exemplo PSA versión 2.x ou inferior. Calquera novo ambiente consistirá en obter só a versión 3.x de PSA.

> [!NOTE]
> Para obter a mellor experiencia cando usa versións máis antigas das aplicacións Field Service e PSA, vaia á páxina **Configuración do sistema** e para o campo **Usar a nova Interface unificada (recomendado)**, seleccione **Non** xa que estas versións non están deseñadas para cargarse correctamente en UCI. Despois de desactivar UCI, pode abrir e executar estas versións de Field Service e PSA empregando o antigo cliente web. Para obter instrucións sobre como desactivar o cliente UCI, consulte [Activar só a Interface unificada](../admin/enable-unified-interface-only.md).
