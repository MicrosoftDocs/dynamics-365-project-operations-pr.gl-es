---
title: Rexístrese nas subscricións de previsualización de Project Operations para situacións de recursos/sen fornecemento
description: Este tema ofrece información sobre como subscribirse e despregar Project Operations para situacións baseadas en recursos/sen fornecemento.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4d35a8bf9e8a841b45808b26ae2587c5b7d99d72
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948862"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Rexístrese nas subscricións de previsualización de Project Operations para situacións de recursos/sen fornecemento

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Este tema explica como subscribirse á oferta de previsualización/socios e despregar o entorno de Project Operations para situacións baseadas en recursos/sen fornecemento.

## <a name="prerequisites"></a>Requisitos previos

- Recibirá un correo electrónico convidándolle a participar na previsualización. Pode solicitar unha previsualización no [sitio web de Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- O usuario que desprega a vprevisualización debe ter dereitos de administrador global de arrendatario de Azure.
- O despregamento dun ambiente de Finance require unha subscrición válida a Azure que se facturará por ambiente. Pode usar a subscrición existente das súas organizacións ou usar unha [Proba de Azure](https://azure.microsoft.com/en-us/free/) para comezar. O ambiente de CDS proporcionarase de balde por un período limitado de 30 días.

## <a name="subscribe"></a>Subscribir

Cando se aprobe a súa [solicitude de previsualización](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u), recibirá dúas ofertas de Microsoft por correo electrónico. Estas ofertas permítenlle despregar a previsualización de Project Operations:

- Dynamics 365 Project Operations – Proba de previsualización
- Proba de previsualización de Dynamics 365 for Finance and Operations

> [!IMPORTANT]
> Só unha persoa, o administrador do arrendatario, dunha organización precisa realizar esta tarefa. Se non es o subscritor desta versión, agarde a que a súa organización estea rexistrada e reciba as súas credenciais de usuario.

### <a name="dynamics-365-project-operations--preview-trial"></a>Dynamics 365 Project Operations – Proba de previsualización

1. Troque a primeira oferta, **Proba de Dynamics 365 Project Operations**, co URL fornecido no seo correo electrónico de benvida.

![Primeira oferta](./media/1FirstOffer.png)

2. Verifique que iniciou sesión como o usuario que pertence á organización que se subscribirá ao servizo.
3. Proceda co troco da oferta. 
4. Seleccione **Si, engadila á miña conta**.

![Trocar oferta](./media/2RedeemFirstOffer.png)

![Confirmar oferta](./media/3ConfirmFirstOffer.png)

![Oferta trocada](./media/4OfferSuccessfulyRedeemed.png)

### <a name="dynamics-365-finance-preview-trial"></a>Proba de previsualización de Dynamics 365 Finance

Repita os mesmos pasos coa segunda oferta do correo electrónico de benvida.

## <a name="assign-licenses"></a>Atribuír licenzas

> [!IMPORTANT]
> Necesitará acceso administrativo ao portal Office 365 da súa organización para completar os seguintes pasos.

1. Vaia a [Centro de administración de Microsoft 365](https://portal.office.com/) para atribuír licenzas aos seus usuarios.

![Portal de administración de Office](./media/5OfficeAdminPortal.png)

2. Na páxina **Usuarios activos**, seleccione os usuarios aos que desexa atribuír unha licenza.

![Atribuír licenzas](./media/6AssignLicenses.png)

3. Verifique que a licenza de Project Operations foi seleccionada e seleccione **Gardar cambios**. 

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

