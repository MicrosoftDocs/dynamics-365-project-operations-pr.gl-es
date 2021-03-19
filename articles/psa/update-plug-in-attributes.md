---
title: Actualizar os atributos do complemento para incluír novas dimensións de prezos
description: Este tema fornece información sobre a actualización dos atributos do complemento para as dimensións de prezos.
author: Rumant
manager: kfend
ms.custom: ''
ms.date: 11/19/2018
ms.topic: article
ms.service: project-operations
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 958646c9e06a15e265bc0caa8b0f3eb9f79fc347
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281791"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a>Actualizar os atributos do complemento para incluír novas dimensións de prezos

[!include [banner](../includes/psa-now-project-operations.md)]

> [!NOTE]
> Se non está a usar as funcións de ofertas e contratación de Project Service Automation (PSA), pode omitir este tema.

Este tema asume que completou os procedementos nos temas [Crear campos e entidades personalizados](create-custom-fields-entities.md), [Engadir campos personalizados a configuración de prezos e entidades transaccionais](field-references.md) e [Configurar campos personalizados como dimensións de prezos](set-up-pricing-dimensions.md). Se non completou eses procedementos, volva e compléteos e despois volva a este tema.

Cando se crea un detalle de liña de oferta na páxina **Liña de oferta** para unha liña de oferta do proxecto, o sistema crea dúas liñas de estimación en segundo plano: unha liña para o lado de custo da estimación e outra para o lado de vendas. Isto é o mesmo para as liñas de contrato do proxecto.

Cando faga unha modificación da cantidade ou dun campo do lado do custo, este cambio propagarase ao lado das vendas. Isto é posible debido aos seguintes complementos que deben volver rexistrarse despois dun cambio nas dimensións de prezos.

- PreOperationContractLineDetailUpdate - Actualizacións **msdyn_orderlinetransaction**.
- PreOperationQuoteLineDetailUpdate - Actualizacións **msdyn_quotelinetransaction**.

Os pasos seguintes explican o proceso de rexistro dos complementos.

1. Abra **PluginRegistrationTool** e conéctese á súa instancia en liña.
2. Prema **Buscar** e busque o complemento para actualizar.

 ![Captura de pantalla da árbore de busca](media/PRT-1.png)

3. Despois de atopar o complemento, seleccióneo e logo prema **Seleccionar en formulario principal**.

4. Seleccione o paso do complemento para actualizar, prema co botón dereito e logo seleccione **Actualizar**.

 ![Captura de pantalla do complemento para actualizar](media/PRT-2.png)
 
5. Na ventá de actualización, prema nos puntos suspensivos (**...**) nos atributos de filtrado.

 ![Captura de pantalla de información de configuración do paso existente Actualizar](media/PRT-3.png)
 
6. Seleccione as caixas de verificación do atributo de prezos

 ![Captura de pantalla que mostra a selección da caixa de verificación para os atributos de prezos](media/PRT-4.png)

7. Prema **Aceptar** para pechar a páxina e logo seleccione **Actualizar paso**.

 ![Captura de pantalla que mostra o botón "Actualizar paso"](media/PRT-5.png)
 
8. Repita este proceso para o segundo complemento, **PreOperationQuoteLineDetail - Actualización de msdyn_quotelinetransaction**.

9. Peche a ferramenta de rexistro de complementos.



[!INCLUDE[footer-include](../includes/footer-banner.md)]