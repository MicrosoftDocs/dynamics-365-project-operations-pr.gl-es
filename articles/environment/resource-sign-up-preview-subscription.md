---
title: Rexístrese nas subscricións de previsualización de Project Operations para situacións de recursos/sen fornecemento
description: Este artigo ofrece información sobre como subscribirse e implementar Project Operations para escenarios baseados en recursos ou non almacenados.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3164add153d77a52f85c2aac442dcf90baa24440
ms.sourcegitcommit: 0d11377bf3ac74c80afbd2013775fcc9869f926a
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 12/10/2022
ms.locfileid: "9842013"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Rexístrese nas subscricións de previsualización de Project Operations para situacións de recursos/sen fornecemento

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_



Este artigo explica como subscribirse á oferta de proba e despregar o ambiente de Project Operations para situacións baseadas en recursos/sen fornecemento.

## <a name="prerequisites"></a>Requisitos previos
- O usuario que desprega a vprevisualización debe ter dereitos de administrador global de arrendatario de Azure. Pode crear un arrendatario durante o troco da primeira oferta. 
- O despregamento dun ambiente de Finance require unha subscrición válida a Azure que se facturará por ambiente. Pode usar a subscrición existente das súas organizacións ou usar unha [Proba de Azure](https://azure.microsoft.com/free/) para comezar. O ambiente de CDS proporcionarase de balde por un período limitado de 30 días.

> [!IMPORTANT]
> Só unha persoa, o administrador do arrendatario, dunha organización precisa realizar esta tarefa. Se non es o subscritor desta versión, agarde a que a súa organización estea rexistrada e reciba as súas credenciais de usuario.
> 
> As probas son de uso único no arrendatario. Só pode realizar unha proba unha vez. Recomendámoslle que cree un novo arrendatario para a proba.


### <a name="dynamics-365-project-operations-ce---preview-trial"></a>Dynamics 365 Project Operations (CE) - Proba da versión preliminar 

Antes de comezar, asegúrese de iniciar sesión nun explorador coa conta de traballo do usuario no arrendatario onde desexa a previsualización de Project Operations.

1. Troque o primeiro código de oferta, **Dynamics 365 Project Operations** aquí [Proba de Project Operations](https://aka.ms/try-po).
2. Confirme o seu pedido.

  Verá que a oferta de confirmación se trocou con éxito.

### <a name="dynamics-365-finance-preview-trial"></a>Proba da versión preliminar de Dynamics 365 Finance

Vaia a [Proba da versión preliminar de Dynamics 365 for Finance](https://aka.ms/trypoche) e repita os pasos da sección anterior coa oferta, Rexístrese para o ambiente aloxado na nube.  

## <a name="assign-licenses"></a>Atribuír licenzas

> [!IMPORTANT]
> Necesitará acceso administrativo ao portal Microsoft 365 da súa organización para completar os seguintes pasos.

1. Vaia a [Centro de administración de Microsoft 365](https://portal.office.com/) para atribuír as licenzas aos seus usuarios.

2. Na páxina **Usuarios activos**, seleccione os usuarios aos que desexa atribuír unha licenza.

3. Verifique que se seleccionou a licenza de **Dynamics 365 Project Operations** e seleccione **Gardar cambios**.

> [!NOTE]
> Non é necesario atribuír a oferta de proba de Finance a un usuario.

## <a name="start-a-new-project-in-lcs"></a>Iniciar un novo proxecto en LCS

Crear un novo proxecto LCS como se describe no artigo [Iniciar un novo proxecto en LCS](create-lcs-project.md)

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>Engadir unha subscrición a Azure a un proxecto de LCS

Para completar esta tarefa, siga os pasos do artigo [Engadir unha subscrición a Azure ao proxecto de LCS](resource-add-azure-subscription-lcs-project.md).

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>Despregar ambiente de demostración de Finance con Project Operations para situacións de recursos/sen fornecemento

Siga as indicacións do artigo [Proporcionar un novo ambiente](resource-provision-new-environment.md) para completar o despregamento. Use o tipo de despregamento de [ambiente de demostración](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) para a previsualización. 

## <a name="install-cds-setup-and-configuration-data"></a>Instalar os datos de configuración de CDS

Instale os datos configuración do CDS como se describe no artigo [Configurar e aplicar os datos de configuración en Common Data Service](resource-apply-pro-setup-config-data.md).
Complete este paso só despois de que se despregue o ambiente de demostración Finance e os datos de demostración estean listos.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
