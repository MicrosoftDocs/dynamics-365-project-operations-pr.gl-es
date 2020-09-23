---
title: Usar o recurso reservable como dimensión de prezos
description: Este tema fornece información sobre o uso dun recurso reservable como dimensión de prezos.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 1d147827-dc55-48a5-b3f6-d8b00bd1c7f7
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 999f7575d1777077376ba74933654b90fcc504c3
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751395"
---
# <a name="use-bookable-resource-as-a-pricing-dimension"></a>Usar o recurso reservable como dimensión de prezos
Este tema fornece información sobre o uso dun recurso reservable como dimensión de prezos. Antes de comezar, se aínda non creou unha solución de dimensión de prezos, necesitará crear unha nova. Se xa ten unha solución de dimensión de prezos, pode facer os seus cambios nesa solución. Se non creou unha nova solución de dimensión de prezos para a súa organización, complete os procedementos do tema [Crear campos e entidades personalizados](create-custom-fields-entities.md).

## <a name="add-bookable-resource-to-forms-and-views"></a>Engadir un recurso reservable a formularios e vistas
Para facer os campos visibles na IU na solución de dimensión de prezos, necesitará percorrer todos os formularios e vistas das entidades clave de Project Service e engadir estes campos aos formularios e vistas desas entidades.
A seguinte táboa é unha lista completa de formularios listos para usar, listados por entidade, que terán que ser actualizados. Se hai vistas ou formularios adicionais nas súas personalizacións nestas entidades, engada os novos campos a eles tamén.
Abra o explorador de solucións para a solución de dimensión de prezos e logo prema en **Publicar todas as personalizacións**.


|   Entidade        | Formularios   |Visualizacións        |
| ------------------------------|---------------------------------|----------------------------------|
|  Prezo do rol|• Información |• Prezos de categorías de recursos activos<br> • Visualización asociada do prezo da categoría de recursos|
|  Sobreprezo de rol|• Información|• Sobreprezo de rol activo<br>• Vista asociada a sobreprezo de rol|
|  Detalle da liña da oferta|• Información do proxecto<br>• Creación rápida do proxecto|• Detalles da liña de oferta activos<br>• Detalles da liña de oferta combinados<br>• Visualización asociada de detalles da liña de oferta|
|  Detalle da liña de contrato do proxecto|• Información do proxecto<br>• Creación rápida do proxecto|• Detalles de liña de contrato combinados<br>• Detalles activos da liña de contrato<br>• Visualización asociada aos detalles da liña de contrato|
|  Membro do equipo do proxecto|• Información<br>• Novo formulario|• Membros do equipo de proxecto activos<br>• Membros do equipo do proxecto<br>• Visualización asociada de membros do equipo de proxecto|
|  Entrada de tempo|• Información<br>• Crear entrada de tempo|• As miñas entradas de tempo por data<br>• As miñas entradas de tempo desta semana<br>• Entradas de tempo para aprobar|
|  Liña de diario|• Información<br>• Creación rápida|• Liñas de diario activas<br>• Visualización asociada da liña de diario|
|  Detalle da liña da factura|• Información<br>• Creación rápida|• Detalles da liña de factura activos<br>• Transaccións de facturas imputables<br>• Transaccións de facturas complementarias<br>• Visualización asociada de detalles da liña de factura<br>• Transacción de facturas non imputables|
|  Real|• Información<br>• Datos reais activos|• Visualización asociada dos datos reais|

## <a name="set-up-bookable-resource-as-a-pricing-dimension"></a>Configurar o recurso reservable como dimensión de prezos

1. Na interface web, vaia a **Project Service** > **Configuración** > **Parámetros**. Na páxina **Parámetro**, no separador **Dimensións de prezos baseados na cantidade**, observe que a grade do separador mostra os rexistros da entidade de dimensións de prezos. 
2. Engada **Recurso reservable** a esta lista de dimensións de prezos como **msdyn_bookableresource**. 
3. Indique o contexto no que o recurso reservable funciona como dimensión de prezos e estableza os valores de **Aplicable ao custo** e **Aplicable ás vendas**.
4. No campo **Tipo de dimensión**, seleccione **Baseado na cantidade**. 
5. Seleccione a prioridade de custo e vendas para o recurso reservable. Normalmente, cando se inclúe como unha dimensión de prezos, un recurso reservable ten a prioridade máis alta, polo que establecer isto como **1** (ou **0** dependendo de como conte a prioridade) aseguraría ese comportamento.

## <a name="set-up-pricing-dimension-field-names"></a>Configurar nomes de campo de dimensións de prezos

Cando o nome de campo dunha dimensión de prezos na táboa **Prezo de rol** é diferente do seu nome de campo en calquera das outras entidades onde ten que funcionar a fixación de prezos predefinidos, o rexistro de dimensión de prezos debe ser informado dos diferentes nomes.    
Para o recurso reservable, a entidade **Membros do equipo do proxecto** ten un nome de campo lixeiramente diferente (**msdyn_bookableresourceid**) do da entidade **Prezo de rol** (**msdyn_bookableresource**). O rexistro da dimensión de prezos para **msydn_bookableresource** debe ser informado disto. 
1. Para facelo, prema dúas veces na fila na grade **Dimensións dos prezos** para abrir a páxina de dimensións de **msdyn_bookableresource**.
2. Na páxina de dimensión, no separador **Relacionado**, prema **Nomes de campo da dimensión de prezos**.

 ![Separador de nomes de campo de dimensión de prezos](media/PD-fieldname.png)

4. Na vista asociada que se abre, prema en **Engadir novo nome de campo da dimensión de prezos**.

 ![Engadir novos nomes de campo de dimensión de prezos](media/Add-NewPD-fieldname.png)


Isto abre a páxina **Novo nome de campo da dimensión de prezos** para **msdyn_bookableresource**. 

5. Engada **msdyn_projectteam** ao campo **Nome lóxico da entidade** e **msdyn_bookableresourceid** ao campo **Nome de campo**. Garde o rexistro.

 ![Novo formulario de nome de campo de dimensión de prezos](media/PD-fieldname-Added.png)
