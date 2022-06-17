---
title: Rexistrarse para unha subscrición de previsualización - lite
description: 'Este artigo ofrece información sobre como subscribirse e implementar a implementación de Project Operations Lite: xestionar a facturación proforma.'
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 6953956c0b3401a6c64ee597f966ba4a4c0d07b5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921254"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>Rexistrarse para unha subscrición de previsualización - lite 

Este artigo explica como subscribirse á oferta de proba e implementar Dynamics 365 Project Operations implementación lite: tramitar a facturación proforma.

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
> Necesitará acceso administrativo ao portal Microsoft 365 da súa organización para completar os seguintes pasos.


1. Ir a [Microsoft 365 centro de administración](https://portal.office.com/) para asignar as licenzas aos seus usuarios.
2. Na páxina **Usuarios activos**, seleccione os usuarios aos que desexa atribuír unha licenza.
3. Verifique que a licenza de **Dynamics 365 Project Operations** está seleccionada. 
4. Seleccione **Gardar as modificacións**.

## <a name="create-a-new-dataverse-environment"></a>Crear un novo ambiente de Dataverse

1. Proporcionar un novo proxecto Operacións Dataverse ambiente de implantación seguindo as instrucións do artigo, [Dataverse modelo de implantación](lite-deployment.md). Cando seleccione o tipo de ambiente, asegúrese de usar **Proba (baseada en subscrición)**.

  ![Novo ambiente.](./media/19CreateEnvironment.png)

2. Seleccione a configuración **Activar as aplicacións de Dynamics 365** e deixe **Despregar automaticamente estas aplicacións** en branco.  
3. Seleccione **Gardar** para crear o ambiente.

  ![Engada a base de datos.](./media/20CreateEnvironment1.png)

4. Despois de crear o ambiente, instale a solución **Microsoft Dynamics 365 Project Operations**. 

![Instale a solución.](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>Instalar unha configuración de CDS e configurar datos de demostración

Instala a configuración de CDS e configura os datos de demostración seguindo as instrucións do artigo, [Aplicar datos de configuración e configuración de demostración](lite-apply-demo-setup-config-data.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
