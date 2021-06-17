---
title: Engadir unha subscrición a Azure a un proxecto de LCS
description: Este tema ofrece información sobre como conectar a súa subscrición a Azure a un proxecto LCS.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6daa86d453ec5022cdd75dff0394c8818292406c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000614"
---
# <a name="add-an-azure-subscription-to-an-lcs-project"></a>Engadir unha subscrición a Azure a un proxecto de LCS

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Os ambientes aloxados na nube deben despregarse mediante unha subscrición a Azure existente. Este tema explica como conectar a súa subscrición a Azure existente a un proxecto LCS. 

## <a name="grant-admin-consent"></a>Outorgar o consentimento de administrador

1. No seu proxecto LCS, na sección **Ambientes**, seleccione **Configuración de Microsoft Azure**.

![Configuración de Microsoft Azure](./media/1MicrosoftAzureSettings.png)

2. Na páxina **Configuración do proxecto**, no separador **Conectores de Azure**, seleccione **Autorizar**. Isto permite despregar ambientes neste proxecto.

![Conectores de Azure](./media/2AzureConnectors.png)

3. Seleccione **Autorizar** de novo para proporcionar o consentimento do administrador.

![Outorgar o consentimento de administrador](./media/3GrantAdminConsent.png)

4. Acepte a solicitude de permisos.

![Aceptar a solicitude de permisos](./media/4AcceptPermissionRequest.png)

A autorización xa está completa. 

![Autorización realizada correctamente](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a>Proporcionar acceso a Dynamics Deployment Services para a súa subscrición a Azure

1. Vaia a [Facturación de Microsoft Azure](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) e seleccione a súa subscrición. Dynamics Deployment Services precisa acceder a esta subscrición para poder despregar ambientes.

![Detalles da subscrición a Azure](./media/6AzureSubscription.png)

2. Seleccione **Control de acceso (IAM)** no panel de navegación e logo seleccione **Engadir atribución de roles**.
3. No control deslizante do lado dereito, seleccione **Rol de colaborador** e na lista que aparece busque e seleccione **Dynamics Deployment Services**. 
4. Seleccione **Gardar**.

![Acceso á subscrición](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a>Engadir un conector de subscrición a un proxecto LCS

1. No seu proxecto LCS, na páxina **Configuración de Microsoft Azure**, seleccione **Engadir** para engadir un novo conector.
2. Introduza o seu ID de subscrición a Azure. Pode atopar o seu ID de subscrición a Azure no [Portal de Azure](https://ms.portal.azure.com/), en **Configuración** na parte inferior esquerda da pantalla.
3. No campo **Configurar para usar Azure Resource Manager**, seleccione **Si**.
4. Asegúrese de que o dominio do arrendatario AAD da subscrición a Azure coincida coa subscrición a Azure que posúe o dominio que está a usar e seleccione **Seguinte**.
5. Na pantalla **Configuración de Microsoft Azure**, seleccione **Seguinte** para confirmar. Se recibe un erro nesta pantalla, volva á sección [Proporcionar acceso a Dynamics Deployment Services para a subscrición a Azure](#provide) neste tema e asegúrese de que completou todos os pasos.
6. Descargue o certificado de xestión de Azure a un cartafol local do seu ordenador. Solicite ao administrador da subscrición a Azure que cargue o certificado no Azure Management Portal seleccionando a subscrición e dirixíndose a **Configuración** > **Certificados de xestión**. Este certificado permite a LCS comunicarse con Azure no seu nome. Podes omitir este paso se o seu usuario ten acceso á subscrición.
7. Seleccione **Seguinte**.
8. Seleccione a rexión de Azure na que desexa despregar e seleccione un centro de datos que estea preto do lugar onde desexa usar este sistema.
9.  Seleccione **Conectar**.

Conectou correctamente a súa subscrición a Azure. Agora pode despregar ambientes aloxados na nube de Dynamics 365 Finance.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
