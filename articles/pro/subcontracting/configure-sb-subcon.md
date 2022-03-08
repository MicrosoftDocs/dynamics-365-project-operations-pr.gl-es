---
title: Configurar Schedule Board para mostrar os traballadores contratados e a capacidade subcontratada
description: Este tema describe como configurar Schedule Board en Microsoft Dynamics 365 Project Operations para mostrar a capacidade de recursos subcontratados ao dotar de persoal as necesidades de recursos do proxecto.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: d645dee741a45dcb0219e4e4f58a329b7b873e10
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903655"
---
# <a name="configure-schedule-board-to-show-contract-workers-and-subcontracted-capacity"></a>Configurar Schedule Board para mostrar os traballadores contratados e a capacidade subcontratada 

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

Taboleiro de programación en Microsoft Dynamics 365 Project Operations pódese utilizar para buscar recursos de dúas formas:

- Busca xeral de recursos sen o contexto de ningún requisito específico de recursos baseados en proxectos.
- Busca de recursos específicos de requisitos onde o requisito do proxecto proporcionará o contexto para os recursos suxeridos.

Para notificar ao consello de programación da capacidade de recursos subcontratados e dos traballadores contratados, cómpre facer actualizacións na configuración do panel de programación. Estas actualizacións inclúen: 
- Actualiza a configuración do taboleiro de programación para a busca xeral de recursos.
- Actualiza a configuración do taboleiro de programación para a busca de recursos baseada en requisitos.

## <a name="update-schedule-board-settings-for-general-resource-search"></a>Actualiza a configuración do taboleiro de programación para a busca xeral de recursos
### <a name="update-filters-for-general-resource-search"></a>Actualiza os filtros para a busca xeral de recursos
Cando busque un recurso, os filtros dispoñibles no taboleiro de programación deben actualizarse para que tamén poida buscar recursos externos especificando algún ou todos os seguintes:
  - Tipo de traballador, se os recursos mostrados deben ser traballadores por contrato ou asalariados.
  - Empresa vendedora á que debe pertencer un recurso.
  - Recursos que pertencen a unha determinada subcontratación ou liña de subcontratación.
    
### <a name="update-retrieve-resource-query"></a>Actualizar a consulta de recursos de recuperación
A consulta utilizada para a busca tamén debe actualizarse para utilizar estes atributos de filtro adicionais. Use os seguintes pasos para actualizar a configuración do taboleiro de programación para a busca xeral de recursos:  
1. Aberto **Configuración do taboleiro de programación** para un Consello de Horarios específico.
2. Abre o **Configuración xeral** pestana e desprázate ata **Outras opcións**.
3. Na lista de configuracións desta sección, actualice o **Disposición do filtro** a **Disposición de filtro predeterminada para Project Operations Lite**.
4. Actualizar **Consulta de recursos de recuperación** a **Consulta de recursos de recuperación predeterminada para Project Operations Lite**.

![Actualiza a configuración do taboleiro de programación para a busca xeral de recursos](../media/BoardSettings.png)  

## <a name="update-schedule-board-settings-for-requirementbased-resource-search"></a>Actualiza a configuración do taboleiro de programación para a busca de recursos baseada en requisitos
### <a name="update-filters-for-requirement-specific-resource-search"></a>Actualiza os filtros para a busca de recursos específicos de requisitos 
Cando busque un recurso, os filtros dispoñibles no taboleiro de programación deben actualizarse para que tamén poida buscar recursos externos especificando algún ou todos os seguintes:
 - Tipo de traballador, se os recursos mostrados deben ser traballadores por contrato ou asalariados.
 - Empresa vendedora á que debe pertencer un recurso.
 - Recursos que pertencen a unha determinada subcontratación ou liña de subcontratación.

### <a name="update-retrieve-resource-query-for-requirement-specific-resource-search"></a>Actualiza a consulta de recursos de recuperación para a busca de recursos específicos de requisitos 
A consulta utilizada para a busca tamén debe actualizarse para utilizar estes atributos de filtro adicionais. Use os seguintes pasos para actualizar a configuración do taboleiro de programación para a busca de recursos baseada en requisitos:

1. Aberto **Configuración do taboleiro de programación** para un taboleiro de programación específico e, a continuación, seleccione **Abre a configuración predeterminada** para abrir a configuración para a busca específica de requisitos.
2. Abre o **Configuración xeral** pestana e desprázate ata **Outras opcións**.
3. Na lista de configuracións desta sección, actualice o **Disposición do filtro** a **Disposición de filtro predeterminada para Project Operations Lite**.
4. Actualizar **Consulta de recursos de recuperación** a **Consulta de recursos de recuperación predeterminada para Project Operations Lite**.
5. Abre o **Tipos de horarios** pestana e vai a **Proxecto**.
6. Baixo a configuración para **Proxecto**, actualizar **Consulta de recursos de recuperación do asistente de programación** a **Consulta de recursos de recuperación predeterminada para Project Operations Lite** e actualizar **Consulta de restricións de recuperación do asistente de programación** a **Consulta de restricións de recuperación predeterminada para Project Operations Lite**.

![Actualiza a configuración do taboleiro de programación para a busca de recursos baseada en requisitos](../media/SASettings.png)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]