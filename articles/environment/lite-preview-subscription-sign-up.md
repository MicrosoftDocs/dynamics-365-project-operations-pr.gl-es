---
title: Rexistrarse para unha subscrición de previsualización - lite
description: Este tema ofrece información sobre como subscribirse e despregar o despregamento de Project Operations lite - de acordo a facturación proforma.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2b5a65f5e29915c349d40400ebbf3e4923b36a67
ms.sourcegitcommit: 52b26950bb3b1596ad81aa4ff91745ee9615d1b0
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334780"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>Rexistrarse para unha subscrición de previsualización - lite 

Este tema explica como subscribirse á oferta de proba e despregar Dynamics 365 Project Operations lite: acordo para facturación proforma.

> [!NOTE]
> Este proceso cambiará nas próximas versións de Project Operations.

## <a name="prerequisites"></a>Requisitos previos
- O usuario que desprega a vprevisualización debe ter dereitos de administrador global de arrendatario de Azure. Pode crear un arrendatario durante o troco da primeira oferta.

> [!IMPORTANT]
> Só unha persoa, o administrador do arrendatario, dunha organización precisa realizar esta tarefa. Se non es o subscritor desta versión, agarde a que a súa organización estea rexistrada e reciba as súas credenciais de usuario.
> 
> As probas son de uso único no arrendatario. Só pode realizar unha proba unha vez. Recomendámoslle que cree un novo arrendatario para a proba.

### <a name="dynamics-365-project-operations-trial"></a>Proba de Dynamics 365 Project Operations 

Antes de comezar, asegúrese de iniciar sesión nun explorador coa conta de traballo do usuario no arrendatario onde desexa a previsualización de Project Operations.

1. Vaia a [Proba de Project Operations](https://aka.ms/try-po) para trocar o primeiro código de oferta, **Dynamics 365 Project Operations**.
2. Confirme o seu pedido.

  Verá que a oferta de confirmación se trocou con éxito.

## <a name="assign-licenses"></a>Atribuír licenzas

> [!IMPORTANT]
> Necesitará acceso administrativo ao portal de Microsoft 365 da súa organización para completar os seguintes pasos.


1. Vaia a [Centro de administración de Microsoft 365](https://portal.office.com/) para atribuír as licenzas aos seus usuarios.
2. Na páxina **Usuarios activos**, seleccione os usuarios aos que desexa atribuír unha licenza.
3. Verifique que a licenza de **Dynamics 365 Project Operations** está seleccionada. 
4. Seleccione **Gardar as modificacións**.

## <a name="create-a-new-dataverse-environment"></a>Crear un novo ambiente de Dataverse

1. Proporcione un novo ambiente de despregamento de Project Operations Dataverse seguindo as instrucións do tema, [Modelo de despregamento de Dataverse](lite-deployment.md). Cando seleccione o tipo de ambiente, asegúrese de usar **Proba (baseada en subscrición)**.

  ![Novo ambiente](./media/19CreateEnvironment.png)

2. Seleccione a configuración **Activar as aplicacións de Dynamics 365** e deixe **Despregar automaticamente estas aplicacións** en branco.  
3. Seleccione **Gardar** para crear o ambiente.

  ![Engadir base de datos](./media/20CreateEnvironment1.png)

4. Despois de crear o ambiente, instale a solución **Microsoft Dynamics 365 Project Operations**. 

![Instalar solución](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>Instalar unha configuración de CDS e configurar datos de demostración

Instale a configuración de CDS e configure os datos de demostración seguindo as instrucións do tema, [Aplicar os datos de instalación e configuración da demostración](lite-apply-demo-setup-config-data.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
