---
title: Actualizar os atributos do complemento con novas dimensións de prezos
description: Este tema fornece información sobre como actualizar os atributos do complemento para as dimensións de prezos.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 54b87a993929edbf89ef48741ba0a06c6c42ec4e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004619"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a>Actualizar os atributos do complemento con novas dimensións de prezos

Este tema fornece información sobre como actualizar os atributos do complemento para as dimensións de prezos.

> [!NOTE]
> Este tema só é aplicable ás funcionalidades de oferta e contrato en Dynamics 365 Project Operations.

## <a name="prerequisites"></a>Requisitos previos
Antes de completar os pasos deste tema, debe ter completado os procedementos dos seguintes temas:

  - [Crear campos e entidades personalizados](create-custom-fields-entities-pricing-dimensions.md) 
  - [Engadir campos personalizados á configuración de prezos e ás entidades transaccionais ](add-custom-fields-price-setup-transactional-entities.md)
  - [Configurar campos personalizados como dimensións de prezos](set-up-custom-fields-pricing-dimensions.md). 
  
Se non completou eses procedementos, compléteos e despois volva a este tema.

## <a name="register-a-plug-in"></a>Rexistrar un complemento
Cando se crea un detalle de liña de oferta na páxina **Liña de oferta** dunha liña de oferta do proxecto, o sistema crea dúas liñas de estimación. Unha liña é para o lado de custo da estimación e a outra liña é para o lado de vendas. Isto é o mesmo para as liñas de contrato do proxecto.

Cando faga unha modificación da cantidade ou dun campo do lado do custo, este cambio farase tamén no lado das vendas. Isto é posible porque os complementos PreOperation de Quotelinedetail e as entidades de detalle de liña de contrato conectan atributos específicos do lado do custo co lado de vendas da transacción. Se precisa que se fagan cambios nos valores das dimensións de prezos do lado de vendas tamén no lado do custo, deberán volver rexistrarse os seguintes complementos despois de facer cambios na dimensión de prezos.

Estes son os complementos para actualizar e volver rexistrar:

- PreOperationContractLineDetailUpdate - **Actualiza msdyn_orderlinetransaction**
- PreOperationQuoteLineDetailUpdate - **Actualiza msdyn_quotelinetransaction**

Complete os seguintes pasos para actualizar e volver rexistrar os complementos.

1. Abra **PluginRegistrationTool** e conécteo ao seu ambiente de Project Operations Dataverse.
2. Seleccione **Buscar** e escriba as primeiras letras do complemento que se vai actualizar.
3. Despois de atopar o complemento, seleccióneo e logo seleccione **Seleccionar en formulario principal**.
4. Seleccione o paso **Update msdyn_orderlinetransaction**, prema co botón dereito e logo seleccione **Actualizar**.
5. Na páxina de diálogo **Actualizar**, seleccione os puntos suspensivos (**...**) nos atributos de filtrado.
6. Ábrese a ventá de atributos de filtrado e ofrece unha lista de todos os atributos da entidade e as dimensións de prezos. Marque as caixas de verificación dos atributos de dimensión de prezos.
7. Seleccione **Aceptar** para pechar a páxina e logo seleccione **Actualizar paso**.
8. Repita os pasos do 2 ao 7 para o segundo complemento, **PreOperationQuoteLineDetail**. Para este complemento, debe actualizar o paso **Actualización de msdyn_quotelinetransaction**.
9. Peche **PluginRegistrationTool**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]