---
title: Rexistrarse para unha subscrición de previsualización
description: Este tema ofrece información sobre como subscribirse e despregar o despregamento de Project Operations lite - de acordo a facturación proforma.
author: sigitac
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a9c1432e8971eeb7918e23e00be9989294335f49
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948859"
---
# <a name="sign-up-for-a-preview-subscription-for-lite-deployment--deal-to-proforma-invoicing"></a>Rexístrese para obter unha subscrición de previsualización do despregamento lite - de acordo a facturación proforma

Este tema explica como subscribirse á oferta de previsualización e despregar o despregamento de Dynamics 365 Project Operations lite - de acordo a facturación proforma.

> [!NOTE]
> Este proceso cambiará nas próximas versións de Project Operations.

## <a name="prerequisites"></a>Requisitos previos

- Recibirá un correo electrónico convidándolle a participar na previsualización. Pode solicitar unha previsualización no [sitio web de Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- O usuario que desprega a vprevisualización debe ter dereitos de administrador global de arrendatario de Azure.
- O usuario que despregue a previsualización necesitará un número de teléfono e unha tarxeta de crédito válida. Durante o rexistro, non haberá cargos na tarxeta durante seis meses. Despois de seis meses, debe cancelar a subscrición. 
- Revise todos os termos e condicións.

## <a name="subscribe"></a>Subscribir

Cando reciba unha aprobación de [solicitude de previsualización](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u), recibirá dúas ofertas de Microsoft por correo electrónico. Estas ofertas permítenlle despregar a previsualización de Project Operations:

- Proba de previsualización de Dynamics 365 Customer Service – código de un só uso
- Dynamics 365 Project Operations – proba de previsualización

### <a name="dynamics-365-customer-service-paid-offer"></a>Oferta pagada de Dynamics 365 Customer Service

1. Usando unha ventá do explorador InPrivate/Incognito, trocará o primeiro código de oferta para Dynamics 365 Customer Service. Para rexistrarse no servizo de atención ao cliente, necesitará:

- Un número de teléfono
- Unha tarxeta de crédito. Cando se rexistre, non haberá cargos na tarxeta durante seis meses. Despois de seis meses, debe cancelar a subscrición.
- Revise todos os termos e condicións.

2. Proporcione a súa información de contacto.

![Información sobre o contacto](./media/1ContactInformation.png)

3. Proporcione os novos datos do arrendatario.

![Crear ID de usuario](./media/2CreateUserID.png)

4. Verifique a súa identidade, garde o seu novo ID de usuario e logo seleccione **Instalar**.

![Gardar información](./media/3SaveInfo.png)

5. Complete o rexistro da tarxeta de crédito e revise todos os termos e condicións. 

![Completar tarxeta de crédito](./media/4CompleteCreditCard.png)

![Comprobación de tarxeta de crédito](./media/5CreditCardCheckout.png)

![Gardar pedido](./media/6SaveOrder.png)

![Confirmación de tarxeta de crédito](./media/7Confirmation.png)

## <a name="cancel-the-dynamics-365-customer-service-enterprise-offer"></a>Cancelar a oferta de empresa de Dynamics 365 Customer Service

A oferta de empresa de Dynamics 365 Customer Service e gratis durante seis meses. A oferta renovarase á tarifa completa ao final do período de seis meses. Para cancelar antes da data de renovación, siga as instrucións que se mostran a continuación. 

> [!NOTE]
> Despois de completar estes pasos, xa non poderá usar o ambiente de previsualización pública de Project Operations.

1. Vaia ao [Portal de administración](https://admin.microsoft.com/), e en **Facturación**, seleccione **Os seus produtos**.

![Portal de administración, páxina Os seus produtos](./media/8AdminPortal.png)

2. Seleccione a **Oferta de empresa de Dynamics 365 Customer Service**.

![Cancelar subscrición](./media/9CancelSubscription.png)

3. Seleccione **Configuración** > **Accións** > **Cancelar subscrición**.
4. No formulario **Cancelación da subscrición**, introduza información nos campos obrigatorios.
5. Seleccione **Cancelar** > **Subscrición.**

### <a name="dynamics-365-project-operations--preview-trial"></a>Dynamics 365 Project Operations – Proba de previsualización

1. Troque a segunda oferta, Proba de operacións de Dynamics 365 Project co URL fornecido no correo electrónico de benvida.

![Trocar oferta 2](./media/10RedeemOffer2.png)

2. Verifique que iniciou sesión como o usuario que pertence á mesma organización que se subscribiu usando o primeiro código de oferta e, a seguir, proceda a trocar a oferta. 
3. Seleccione **Si, engadila á miña conta**.

![Engadir á conta](./media/11AddToAccount.png)

![Pantalla Probar agora](./media/12TryNow.png)

![Detalles do pedido](./media/13Confirmation.png)

## <a name="assign-licenses"></a>Atribuír licenzas

> [!IMPORTANT]
> Necesitará acceso administrativo ao portal Office 365 da súa organización para completar os seguintes pasos.

1. Vaia a [Centro de administración de Microsoft 365](https://portal.office.com/) para atribuír as licenzas aos seus usuarios.

![Páxina de inicio do centro de administración](./media/14AdminPortal.png)

2. Na páxina **Usuarios activos**, seleccione os usuarios aos que desexa atribuír unha licenza.

![Atribuír licenzas](./media/15AssignLicenses.png)

3. Verifique que a licenza de **Customer Service Enterprise** e **Project Operations** se seleccionou e seleccione **Gardar cambios**.

## <a name="create-a-new-cds-environment"></a>Crear un novo ambiente de CDS

Proporcione un novo ambiente de implantación de CDS de Project Operations seguindo as instrucións do tema, [Modelo de despregamento de CDS](lite-deployment.md).

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>Instalar unha configuración de CDS e configurar datos de demostración

Instale a configuración de CDS e configure os datos de demostración seguindo as instrucións do tema, [Aplicar os datos de instalación e configuración da demostración](lite-apply-demo-setup-config-data.md).
