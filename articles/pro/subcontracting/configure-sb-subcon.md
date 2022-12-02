---
title: Configurar o panel de programación para mostrar os traballadores contratados e a capacidade subcontratada
description: Este artigo describe como configurar o panel de programación en Microsoft Dynamics 365 Project Operations para mostrar a capacidade de recursos subcontratados ao dotar de persoal os requisitos de recursos do proxecto.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 355691b63f437de789afab499369afcdf87e6d3d
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/11/2022
ms.locfileid: "9262214"
---
# <a name="configure-schedule-board-to-show-contract-workers-and-subcontracted-capacity"></a>Configurar o panel de programación para mostrar os traballadores contratados e a capacidade subcontratada 

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

O panel de programación en Microsoft Dynamics 365 Project Operations pódese utilizar para buscar recursos de dúas formas:

- Busca xeral de recursos sen o contexto de ningún requisito específico de recursos baseados en proxectos.
- Busca de recursos específicos de requisitos onde o requisito do proxecto proporcionará o contexto para os recursos suxeridos.

Para notificar ao panel de programación a capacidade de recursos subcontratados e de traballadores contratados, cómpre facer actualizacións na configuración do panel de programación. Entre estas actualizacións inclúense: 
- Actualizar a configuración do panel de programación para a busca xeral de recursos.
- Actualizar a configuración do panel de programación para a busca de recursos baseados en requisitos.

## <a name="update-schedule-board-settings-for-general-resource-search"></a>Actualizar a configuración do panel de programación para a busca xeral de recursos
### <a name="update-filters-for-general-resource-search"></a>Actualizar os filtros para a busca xeral de recursos
Cando busque un recurso, os filtros dispoñibles no panel de programación deben actualizarse para que tamén poida buscar recursos externos especificando algún ou todos os seguintes:
  - Tipo de traballador, se os recursos mostrados deben ser traballadores por contrato ou empregados.
  - Empresa fornecedora á que debe pertencer un recurso.
  - Recursos que pertencen a unha determinada subcontratación ou liña de subcontratación.
    
### <a name="update-retrieve-resource-query"></a>Actualizar Recuperar consulta de recursos
A consulta utilizada para a busca tamén debe actualizarse para utilizar estes atributos de filtro adicionais. Use os seguintes pasos para actualizar a configuración do panel de programación para a busca xeral de recursos:  
1. Abra **Configuración do panel de programación** para un panel de programación específico.
2. Abra o separador **Configuración xeral** e desprácese ata **Outras configuracións**.
3. Na lista de configuracións desta sección, actualice o **Deseño filtro** a **Deseño de filtro predefinido para Project Operations Lite**.
4. Actualice **Recuperar consulta recursos** a **Recuperar consulta de recursos predefinida para Project Operations Lite**.

![Actualizar a configuración do panel de programación para a busca xeral de recursos](../media/BoardSettings.png)  

## <a name="update-schedule-board-settings-for-requirementbased-resource-search"></a>Actualizar a configuración do panel de programación para a busca de recursos baseados en requisitos
### <a name="update-filters-for-requirement-specific-resource-search"></a>Actualizar os filtros para a busca de recursos específicos do requisito 
Cando busque un recurso, os filtros dispoñibles no panel de programación deben actualizarse para que tamén poida buscar recursos externos especificando algún ou todos os seguintes:
 - Tipo de traballador, se os recursos mostrados deben ser traballadores por contrato ou empregados.
 - Empresa fornecedora á que debe pertencer un recurso.
 - Recursos que pertencen a unha determinada subcontratación ou liña de subcontratación.

### <a name="update-retrieve-resource-query-for-requirement-specific-resource-search"></a>Actualizar Recuperar consulta de recursos para a busca de recursos específicos de requisitos 
A consulta utilizada para a busca tamén debe actualizarse para utilizar estes atributos de filtro adicionais. Use os seguintes pasos para actualizar a configuración do panel de programación para a busca de recursos baseada nos requisitos:

1. Abra **Configuración do panel de programación** para un panel de programación específico e, a segir, seleccione **Abrir configuración predefinida** para abrir a configuración para a busca específica de requisitos.
2. Abra o separador **Configuración xeral** e desprácese ata **Outras configuracións**.
3. Na lista de configuracións desta sección, actualice o **Deseño filtro** a **Deseño de filtro predefinido para Project Operations Lite**.
4. Actualice **Recuperar consulta recursos** a **Recuperar consulta de recursos predefinida para Project Operations Lite**.
5. Abra o separador **Tipos de programación** e vaia a **Proxecto**.
6. Baixo a configuración para **Proxecto**, actualice **Recuperar consulta de recursos do asistente de programación** a **Recuperar consulta de recursos predefinida para Project Operations Lite** e actualice **Recuperar consulta de restricións do asistente de programación** a **Recuperar consulta de restricións predefinida para Project Operations Lite**.

![Actualizar a configuración do panel de programación para a busca de recursos baseados en requisitos](../media/SASettings.png)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
