---
title: Rexístrese nas subscricións de previsualización de Project Operations para situacións de recursos/sen fornecemento
description: Este tema ofrece información sobre como subscribirse e despregar Project Operations para situacións baseadas en recursos/sen fornecemento.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a6dfa51f59119834230b7c9f8859a9d85eaae999
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642954"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Rexístrese nas subscricións de previsualización de Project Operations para situacións de recursos/sen fornecemento

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Este tema explica como subscribirse á oferta de previsualización/socios e despregar o entorno de Project Operations para situacións baseadas en recursos/sen fornecemento.

## <a name="prerequisites"></a>Requisitos previos

- Recibirá un correo electrónico convidándolle a participar na previsualización. Pode solicitar unha previsualización no [sitio web de Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- O usuario que desprega a vprevisualización debe ter dereitos de administrador global de arrendatario de Azure.
- O despregamento dun ambiente de Finance require unha subscrición válida a Azure que se facturará por ambiente. Pode usar a subscrición existente das súas organizacións ou usar unha [Proba de Azure](https://azure.microsoft.com/en-us/free/) para comezar. O ambiente de CDS proporcionarase de balde por un período limitado de 30 días.

## <a name="subscribe"></a>Subscribir

Cando se aprobe a súa [solicitude de previsualización](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u), recibirá tres ofertas de Microsoft por correo electrónico. Estas ofertas permítenlle despregar a previsualización de Project Operations:

- Dynamics 365 Project Operations (CRM) - Proba de previsualización
- Office 365 Project Operations - Proba de previsualización
- Dynamics 365 Finance - Proba de previsualización

> [!IMPORTANT]
> Só unha persoa, o administrador do arrendatario, dunha organización precisa realizar esta tarefa. Se non es o subscritor desta versión, agarde a que a súa organización estea rexistrada e reciba as súas credenciais de usuario.

### <a name="dynamics-365-project-operations-crm---preview-trial"></a>Dynamics 365 Project Operations (CRM) - Proba de previsualización 

Antes de comezar, asegúrese de iniciar sesión nun explorador coa conta de traballo do usuario no arrendatario onde desexa a previsualización de Project Operations.

1. Troque o primeiro código de oferta, **Dynamics 365 Project Operations (CRM) - Proba de previsualización** pegándoo no URL do explorador.

![Trocar oferta](./media/16RedeemFirstOfferNew.png)

2. Confirme o seu pedido.

![Confirmar o pedido](./media/17ConfirmOrderNew.png)

Verá que a oferta de confirmación se trocou con éxito.

![Confirmación](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a>Office 365 Project Operations - Proba de previsualización

Repita os mesmos pasos que co primeiro código de oferta. Asegúrese de engadir o segundo código de oferta usando a mesma conta de usuario que se usou co primeiro código de oferta.

### <a name="dynamics-365-finance-preview-trial"></a>Proba de previsualización de Dynamics 365 Finance

Repita os mesmos pasos coa última oferta do correo electrónico de benvida.

## <a name="assign-licenses"></a>Atribuír licenzas

> [!IMPORTANT]
> Necesitará acceso administrativo ao portal de Microsoft 365 da súa organización para completar os seguintes pasos.

1. Vaia a [Centro de administración de Microsoft 365](https://portal.office.com/) para atribuír as licenzas aos seus usuarios.

![Páxina de inicio do centro de administración](./media/14AdminPortal.png)

2. Na páxina **Usuarios activos**, seleccione os usuarios aos que desexa atribuír unha licenza.

![Atribuír licenzas](./media/15AssignLicenses.png)

3. Verifique que a licenza de **Dynamics 365 Project Operations (CRM) Previsualización** e **Office 365 Project Operations - Previsualización** seleccionáronse e seleccione **Gardar cambios**.

> [!NOTE]
> Non é necesario atribuír a oferta de proba de Finance a un usuario.

## <a name="start-a-new-project-in-lcs"></a>Iniciar un novo proxecto en LCS

Crear un novo proxecto LCS como se describe no tema [Iniciar un novo proxecto en LCS](create-lcs-project.md)

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>Engadir unha subscrición a Azure a un proxecto de LCS

Para completar esta tarefa, siga os pasos do tema [Engadir unha subscrición a Azure ao proxecto de LCS](resource-add-azure-subscription-lcs-project.md).

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>Despregar ambiente de demostración de Finance con Project Operations para situacións de recursos/sen fornecemento

Siga as indicacións do tema [Proporcionar un novo ambiente](resource-provision-new-environment.md) para completar o despregamento. Use o tipo de despregamento de [ambiente de demostración](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) para a previsualización. 

## <a name="install-cds-setup-and-configuration-data"></a>Instalar os datos de configuración de CDS

Instale os datos configuración do CDS como se describe no tema [Configurar e aplicar os datos de configuración en Common Data Service](resource-apply-pro-setup-config-data.md).
Complete este paso só despois de que se despregue o ambiente de demostración de Finance e os datos de demostración en FO estean listos.
