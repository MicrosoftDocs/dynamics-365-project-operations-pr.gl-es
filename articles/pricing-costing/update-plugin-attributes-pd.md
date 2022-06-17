---
title: Actualizar os atributos do complemento con novas dimensións de prezos
description: Este artigo ofrece información sobre como actualizar os atributos do complemento para as dimensións de prezos.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2ae502fea533d9f199ef5ee1cc85b623f08cbd84
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920012"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a>Actualizar os atributos do complemento con novas dimensións de prezos

Este artigo ofrece información sobre como actualizar os atributos do complemento para as dimensións de prezos.

> [!NOTE]
> Este artigo só é aplicable ás características de cotización e contrato en Dynamics 365 Project Operations.

## <a name="prerequisites"></a>Requisitos previos
Antes de completar os pasos deste artigo, debes completar os procedementos dos seguintes artigos:

  - [Crear campos e entidades personalizados](create-custom-fields-entities-pricing-dimensions.md) 
  - [Engadir campos personalizados á configuración de prezos e ás entidades transaccionais ](add-custom-fields-price-setup-transactional-entities.md)
  - [Configurar campos personalizados como dimensións de prezos](set-up-custom-fields-pricing-dimensions.md). 
  
Se non completaches eses procedementos, complétaos e despois volve a este artigo.

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