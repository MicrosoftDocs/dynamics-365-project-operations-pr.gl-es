---
title: Rexistrarse para unha subscrición de previsualización - lite
description: Este tema ofrece información sobre como subscribirse e despregar o despregamento de Project Operations lite - de acordo a facturación proforma.
author: sigitac
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4de51277e5a08690cc16497e3916f40498b39fb8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997419"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>Rexistrarse para unha subscrición de previsualización - lite 

Este tema explica como subscribirse á oferta de versión preliminar para socios e o despregamento de Dynamics 365 Project Operations lite: de acordo a facturación proforma.

> [!NOTE]
> Este proceso cambiará nas próximas versións de Project Operations.

## <a name="prerequisites"></a>Requisitos previos

- Recibirá un correo electrónico convidándolle a participar na previsualización. Pode solicitar unha previsualización no [sitio web de Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- O usuario que desprega a vprevisualización debe ter dereitos de administrador global de arrendatario de Azure.
- Revise todos os termos e condicións.

## <a name="subscribe"></a>Subscribir

Cando reciba unha aprobación de [solicitude de previsualización](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u), recibirá dúas ofertas de Microsoft por correo electrónico. Estas ofertas permítenlle despregar a previsualización de Project Operations:

- Dynamics 365 Project Operations (CRM) - Proba de previsualización
- Office 365 Project Operations - Proba de previsualización

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

## <a name="assign-licenses"></a>Atribuír licenzas

> [!IMPORTANT]
> Necesitará acceso administrativo ao portal de Microsoft 365 da súa organización para completar os seguintes pasos.


1. Vaia a [Centro de administración de Microsoft 365](https://portal.office.com/) para atribuír as licenzas aos seus usuarios.

![Páxina de inicio do centro de administración](./media/14AdminPortal.png)

2. Na páxina **Usuarios activos**, seleccione os usuarios aos que desexa atribuír unha licenza.

![Atribuír licenzas](./media/15AssignLicenses.png)

3. Verifique que están seleccionadas as licenzas de **Versión preliminar de Dynamics 365 Project Operations (CRM)** e **Office 365 Project Operations - Versión preliminar**. 
4. Seleccione **Gardar as modificacións**.

## <a name="create-a-new-cds-environment"></a>Crear un novo ambiente de CDS

1. Proporcione un novo ambiente de implantación de CDS de Project Operations seguindo as instrucións do tema, [Modelo de despregamento de CDS](lite-deployment.md). Cando seleccione o tipo de ambiente, asegúrese de usar **Proba (baseada en subscrición)**.
![Novo ambiente](./media/19CreateEnvironment.png)

2. Seleccione a configuración **Activar as aplicacións de Dynamics 365** e deixe **Despregar automaticamente estas aplicacións** en branco.  
3. Seleccione **Gardar** para crear o ambiente.

![Engadir base de datos](./media/20CreateEnvironment1.png)

4. Despois de crear o ambiente, instale a solución **Microsoft Dynamics 365 Project Operations**. 

![Instalar solución](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>Instalar unha configuración de CDS e configurar datos de demostración

Instale a configuración de CDS e configure os datos de demostración seguindo as instrucións do tema, [Aplicar os datos de instalación e configuración da demostración](lite-apply-demo-setup-config-data.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]