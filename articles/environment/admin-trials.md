---
title: Rexistro para as probas de Project Operations
description: Este tema fornece información sobre como despregar unha proba de Dynamics 365 Project Operations.
author: ruhercul
ms.date: 10/04/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 1c8ae111acffb45fef1c2e6435849471ae331796
ms.sourcegitcommit: 05ee415093d152b5b9e1203c3db0ea7f0c5a75a5
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/04/2021
ms.locfileid: "7599211"
---
# <a name="sign-up-for-project-operations-trials"></a>Rexistro para as probas de Project Operations 

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento, despregamento de Lite - de acordo a facturación proforma, Project Operations para situacións baseadas en produción/con fornecemento_ 

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Este tema explica como subscribirse á oferta de asociado de versión preliminar e despregar un ambiente de Dynamics 365 Project Operations.

Coa nova proba de Project Operations, pode despregar automaticamente calquera dos tres escenarios de despregamento admitidos enchendo un cuestionario que recomenda o mellor enfoque de despregamento. Neste tema se proporciona información sobre como:

- Troque a súa oferta de proba.
- Inicie o aprovisionamento.
- Configure a escrita dual.
- Máis información acerca de Project Operations. 

A seguinte táboa describe os detalles da nova oferta de proba.

| **Elemento da oferta**               | **Detalles**                                  |
|------------------------------|----------------------------------------------|
| Tipo de oferta                   | Este tipo de oferta é o cliente potencial de administrador, polo que é necesario un administrador de arrendatarios para trocar. |
| Uso da oferta                    | Unha vez por arrendatario                          |
| Duración da oferta               | 30 días de calendario                             |
| Trocos por arrendatario       | 1                                            |
| Número de usuarios              | 25                                           |
| Extensión                    | 1 extensión, 30 días de calendario               |
| Número de ambientes de proba | 3                                            |


## <a name="admin-trial-details"></a>Detalles da proba de administrador
A seguinte táboa indica os detalles da proba e como se aplican a cada tipo de despregamento.

| **Elemento**                      | **Lite**                                     | **Materiais sen fornecemento** | **Materiais con fornecemento** |
|-------------------------------|----------------------------------------------|---------------------------|-----------------------|
| Datos de configuración proporcionados           | Si                                          | Si                       | Si (USSI)            |
| Datos transaccionais            | No                                           | No                        | No                    |
| Tempo de aprovisionamento en minutos  | 15                                           | 90                        | 30                    |
 
## <a name="prerequisites"></a>Requisitos previos
os seguintes requisitos previos son necesarios para despregar unha proba de Dynamics 365 Project Operations.

- Rexístrese para [Dynamics 365 Project Operations - Proba da versión preliminar](https://www.aka.ms/try-po).
- O usuario que desprega a vprevisualización debe ter dereitos de administrador global de arrendatario de Azure.

> [!IMPORTANT]
> Só unha persoa nunha organización, o administrador do arrendatario, precisa realizar esta tarefa. Se non es o subscritor desta versión, agarde a que a súa organización estea rexistrada e reciba as súas credenciais de usuario.

### <a name="dynamics-365-project-operations---preview-trial"></a>Dynamics 365 Project Operations - Proba da versión preliminar 

Antes de comezar, inicie sesión nun explorador coa conta de traballo do usuario no arrendatario onde desexa a versión preliminar de Project Operations.

1. Troque o primeiro código de oferta, **Dynamics 365 Project Operations - Proba de versión preliminar** pegándoo no URL do explorador.

    ![Trocar oferta](./media/16RedeemFirstOfferNew.png)

2. Confirme o seu pedido.

    ![Confirmar o pedido](./media/17ConfirmOrderNew.png)

  Verá que a oferta de confirmación se trocou con éxito.

   ![Confirmación](./media/18OrderConfirmationNew.png)

  Será redirixido ao [centro de administración de Power Platform](https://admin.powerplatform.microsoft.com/projectoperationstrial).

## <a name="questionnaire-and-provisioning"></a>Cuestionario e aprovisionamento

1.  Vaia ao [centro de administración de Power Platform](https://admin.powerplatform.com/projectoperationstrial) e encha o cuestionario.  
2.  Revise o tipo de despregamento recomendado e seleccione **Comezar a configuración** para iniciar o aprovisionamento.
3.  Revise os termos e condicións e, a seguir, seleccione **Iniciar**.

   Despois de iniciar o aprovisionamento, redirixiráselle á lista de ambientes do centro de administración de Power Platform. Mentres o aprovisionamento está en curso, o estado do seu ambiente é **Preparando instancia**.
 
  Cando se completa o aprovisionamento, o estado do seu ambiente é **Listo**. O aprovisionamento do ambiente inclúe o despregamento de datos de demostración.
 
4.  Seleccione o respectivo URL de Microsoft Dataverse e as aplicacións de Finance and Operations para validar o despregamento.

## <a name="configuring-dual-write"></a>Configuración da escrita dual
Só para despregamentos de materiais sen fornecemento, configure as súas asignacións de escrita dual. Para obter máis información, consulte [Versións de mapa de escrita dual de Project Operations](resource-dual-write-maps.md).

## <a name="assign-licenses"></a>Atribuír licenzas

Necesitará acceso administrativo ao portal de Microsoft 365 da súa organización para completar os seguintes pasos.

1. Vaia ao [Centro de administración de Microsoft 365](https://portal.office.com/) para atribuír as licenzas aos seus usuarios.

   ![Páxina de inicio do centro de administración](./media/14AdminPortal.png)

2. Na páxina **Usuarios activos**, seleccione os usuarios aos que desexa atribuír unha licenza.

   ![Atribuír licenzas](./media/15AssignLicenses.png)

3. Verifique que se seleccionou a licenza da **versión preliminar de Dynamics 365 Project Operations** e seleccione **Gardar cambios**.

## <a name="additional-resources"></a>Recursos adicionais

Os seguintes recursos proporcionan unha guía útil cando comeza a súa viaxe con Project Operations:

- [Serie de vídeo - Visión xeral de Project Operations, inclúe análises a fondo e folla de ruta](https://youtube.com/playlist?list=PLcakwueIHoT_LJ3Fr1tHnkPk5lioqE6uH)
- [Dynamics 365 Project Operations](/learn/modules/examine-dynamics-365-project-operations/)
- [Determinar o seu tipo de despregamento](determine-deployment-type.md)

## <a name="frequently-asked-questions"></a>Preguntas máis frecuentes

### <a name="what-if-i-require-alm-or-elm-for-my-finance-and-operations-apps-environment"></a>Que pasa se necesito ALM ou ELM para o meu ambiente de aplicacións de Finance and Operations?

- Para os socios que requiran capacidades de xestión do ciclo de vida do ambiente completo, consulte o documento [Solicitude de licenza de illamento de procesos para socios](https://experience.dynamics.com/requestlicense) para revisar a oferta para novos socios. 
- Para socios que buscan máis información sobre os dereitos de uso interno, consulte [Beneficios de nube e software de dereitos de uso interno (microsoft.com](https://partner.microsoft.com/membership/internal-use-software).

### <a name="can-i-extend-my-trial-beyond-30-days"></a>Podo prolongar a proba máis de 30 días?
Para ampliar a proba, complete os seguintes pasos.

1. No **Centro de administración de Microsoft 365**, vaia a **Facturación** > **Os seus produtos**.
2. Seleccione **Dynamics 365 Project Operations (CE) - Proba de versión preliminar**.
3. En **Data de caducidade**, seleccione **Ampliar data**.

### <a name="can-i-upgrade-from-the-lite-deployment-to-the-resourcenon-stocked-based-scenario-deployment"></a>Podo actualizar desde o despregamento lite ao despregamento de escenarios baseados en recursos/sen fornecemento?
Actualmente, non hai soporte para actualizar un ambiente desde unha versión básica a un despregamento sen fornecemento.

### <a name="can-i-access-lifecycle-services-lcs-for-my-finance-environments"></a>Podo acceder a Lifecycle Services (LCS) para os meus ambientes de Finance?  
Non. Para estas probas, o despregamento manéxase a través do Centro de administración de Power Platform. O acceso ao ambente de Finance está restrinxido.

### <a name="can-i-install-my-trial-on-an-existing-environment"></a>Podo instalar a proba nun ambiente existente?
Se ten un ambiente existente, poderá instalar o despregamento lite nun ambiente de Dataverse de vendas existente dende o Centro de administración de Power Platform.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
