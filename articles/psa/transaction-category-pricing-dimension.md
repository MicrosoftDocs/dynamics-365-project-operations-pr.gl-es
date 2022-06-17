---
title: Use a categoría de transacción como dimensión de prezos
description: Este artigo ofrece información sobre o uso dunha categoría de transacción como dimensión de prezos.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 1a1c2dc17c2092e5364d90e7efc1f13aee80703e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915734"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>Use a categoría de transacción como dimensión de prezos

[!include [banner](../includes/psa-now-project-operations.md)]

Este artigo mostra como usar unha categoría de transacción como dimensión de prezos. Antes de comezar, se aínda non creou unha solución de dimensión de prezos, necesitará crear unha nova. Se xa ten unha solución de dimensión de prezos, pode facer os seus cambios nesa solución. Se non creou unha nova solución de dimensións de prezos para a súa organización, complete os procedementos da páxina [Crear campos e entidades personalizados](create-custom-fields-entities.md) artigo.

## <a name="add-transaction-category-to-forms-and-views"></a>Engadir a categoría de transacción a formularios e vistas
Para facer a categoría de transacción visible na IU na solución de dimensión de prezos, necesitará percorrer todos os formularios e vistas das entidades clave de Project Service e engadir estes campos aos formularios e vistas desas entidades.
A seguinte táboa é unha lista completa de formularios listos para usar, listados por entidade, que terán que ser actualizados cos novos campos. Se hai vistas ou formularios adicionais nas súas personalizacións nestas entidades, engada os novos campos a eles tamén.

|  Entidade        | Formularios     |Visualizacións        |
| ------------------------------|---------------------------------|----------------------------------|
|  Prezo do rol|• Información |• Prezos de categorías de recursos activos<br> • Visualización asociada do prezo da categoría de recursos|
|  Sobreprezo de rol|• Información|• Sobreprezo de rol activo<br>• Vista asociada a sobreprezo de rol|
|  Detalle da liña da oferta|• Información do proxecto<br>• Creación rápida do proxecto|• Detalles da liña de oferta activos<br>• Detalles da liña de oferta combinados<br>• Visualización asociada de detalles da liña de oferta|
|  Detalle da liña de contrato do proxecto|• Información do proxecto<br>• Creación rápida do proxecto|• Detalles de liña de contrato combinados<br>• Detalles activos da liña de contrato<br>• Visualización asociada aos detalles da liña de contrato|
|  Tarefa do proxecto|• Información<br>• Novo formulario||
|  Membro do equipo do proxecto|• Información<br>• Novo formulario|• Membros do equipo de proxecto activos<br>• Membros do equipo do proxecto<br>• Visualización asociada de membros do equipo de proxecto|
|  Entrada de tempo|• Información<br>• Crear entrada de tempo|• As miñas entradas de tempo por data<br>• As miñas entradas de tempo desta semana<br>• Entradas de tempo para aprobar|
|  Liña de diario|• Información<br>• Creación rápida|• Liñas de diario activas<br>• Visualización asociada da liña de diario|
|  Detalle da liña da factura|• Información<br>• Creación rápida|• Detalles da liña de factura activos<br>• Transaccións de facturas imputables<br>• Transaccións de facturas complementarias<br>• Visualización asociada de detalles da liña de factura<br>• Transacción de facturas non imputables|
|  Real|• Información<br>• Datos reais activos|• Visualización asociada dos datos reais|

## <a name="set-up-transaction-category-as-a-pricing-dimension"></a>Configurar unha categoría de transacción como dimensión de prezos

1. Na interface web, vaia a **Project Service** > **Configuración** > **Parámetros**. 
2. Na páxina **Parámetros**, no separador **Dimensións de prezos baseados na cantidade**, observe que a grade do separador mostra os rexistros da entidade **Dimensións de prezos**.
3. Engada **Categoría de transaccións** a esta lista e configure os campos **Aplicable ao custo** e **Aplicable á venda** en **Si**.
4. No capo **Tipo de dimensión**, seleccione **Baseado na cantidade** e, seguir, seleccione a prioridade para a **Categoría de transacción** relacionada co custo e as vendas.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
