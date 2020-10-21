---
title: Fornecer un novo ambiente
description: Este tema ofrece información sobre como fornecer un novo ambiente de Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 45700371c50e3b5a840df45fc24fa8a5b4584b61
ms.sourcegitcommit: 87b7a8d793c19c50f3765b8d788cde24a6a0ca24
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949360"
---
# <a name="provision-a-new-environment"></a>Fornecer un novo ambiente

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Este tema ofrece información sobre como fornecer un novo ambiente de Dynamics 365 Project Operations para situacións baseadas en recursos/sen fornecemento.

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a>Activar o fornecemento automatizado de Project Operations nun proxecto de LCS

Siga os pasos seguintes para activar o fluxo de fornecemento automatizado de Project Operations para o seu proxecto de LCS.

1. Vaia a [LCS](https://lcs.dynamics.com/v2) e seleccione o mosaico **Xestión da funcionalidade de previsualización**.
2. Na lista **Funcionalidade de previsualización**, seleccione **Project Operations** e seleccione **Funcionalidade de previsualización activada** para activar Project Operations.

> [!NOTE]
> Este paso só se realiza unha vez por proxecto de LCS.

## <a name="provision-a-project-operations-environment"></a>Fornecer un ambiente de Project Operations

1. Abra un novo despregamento de Dynamics 365 Finance [ambiente de demostración](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) ou [ambiente de illamento de procesos/produción](https://docs.microsoft.com/edynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure). 
2. Consulte o asistente de **Fornecemento de ambientes**. 

> [!IMPORTANT]
> Asegúrese de que a versión da aplicación seleccionada sexa 10.0.13 ou superior.

3. Para fornecer Project Operations, en **Configuración avanzada**, seleccione **Common Data Service**. 
4. Active a **Configuración de Common Data Service** seleccionando **Si** e logo introduza información nos campos obrigatorios:

  - Nome
  - Rexión
  - Linguaxe
  - Moeda
 
5. No campo **Modelo de Common Data Service**, seleccione **Project Operations** 

6. Seleccionar o tipo de ambiente para o seu despregamento. Unha proba baseada en subscrición permitiralle despregar un ambiente de CDS durante 30 días. 

![Configuración de despregamento](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> Seleccione **Acepto** para aceptar os termos do servizo e logo seleccione **Feito** para volver á configuración de despregamento.

![Consentimento de despregamento](./media/2DeploymentConsent.png)

7. Complete os restantes campos obrigatorios no asistente e confirme o despregamento. O tempo de subministración do ambiente varía segundo o tipo de ambiente. A subministración pode levar ata seis horas.

  Despois de completar correctamente o despregamento, o ambiente mostrarase como **Despregado**.

8. Para confirmar que o ambiente se implantou correctamente, seleccione **Iniciar sesión** e inicie sesión no ambiente para confirmar.

![Detalles do ambiente de ](./media/3EnvironmentDetails.png)

## <a name="apply-project-operations-finance-demo-data-optional-step"></a>Aplicar datos de demostración de Project Operations Finance (paso opcional)

Aplique os datos de demostración de Project Operations Finance á versión de servizo 10.0.13 do ambiente aloxado na nube como se describe [neste artigo](resource-apply-finance-demo-data.md).

## <a name="apply-updates-to-the-finance-environment"></a>Aplicar actualizacións ao ambiente de Finance

Project Operations require un ambiente de Finance coa versión da aplicación **10.0.13 (10.0.569.20009)** ou superior.

É posible que teña que aplicar actualizacións de calidade ao seu ambiente de Finance para recibir esta versión.

1. En LCS, na páxina **Detalles do ambiente**, na sección **Actualizacións dispoñibles**, seleccione **Ver actualización**.

![Ver actualizacións](./media/5ViewUpdates.png)

2. Na páxina **Actualizacións binarias**, seleccione **Gardar paquete.**

![Gardar paquete](./media/6SavePackage.png)

3. Prema **Seleccionar todos** e logo seleccione **Gardar paquete**.

![Revisar e gardar actualizacións](./media/7ReviewAndSaveUpdates.png)

4. Introduza un nome e unha descrición do paquete e seleccione **Gardar**. Dependendo da conexión a Internet, este proceso pode levar algún tempo.

![Cargar o paquete á biblioteca de activos](./media/8UploadPackageToAssetsLibrary.png)

5. Despois de gardar o paquete, seleccione **Feito** e garde este paquete na biblioteca de activos do seu proxecto de LCS.

Gardar e validar o paquete pode levar uns 15 minutos.

6. Para aplicar a actualización, navegue ata a páxina **Detalles do ambiente** páxina en LCS e seleccione **Manter** > **Aplicar actualizacións**.

![Manter ambientes](./media/9MaintainEnvironment.png)

7. Na lista de actualizacións seleccione o paquete que creou e seleccione **Aplicar**.

![Aplicar actualizacións](./media/10ApplyUpdates.png)

O servizo do ambiente levará algún tempo. Despois de completalo, o ambiente volverá a un estado despregado.

![Ambiente despregado](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a>Establecer unha conexión de escrita dual 

1. No seu proxecto de LCS, vaia á páxina **Detalles do ambiente**.
2. En **Información do ambiente de Common Data Service**, seleccione **Ligazón a CDS para aplicacións**.
3. Despois de completar a ligazón, seleccione **Ligazón a CDS para aplicacións** de novo. Redixiráselle a escrita dual en Finance.

![Ligazón a CDS](./media/12LinktoCDS.png)

4. Seleccione **Aplicar solución** para acceder ás entidades que serán asignadas na integración.

![Aplicar solucións](./media/13ApplySolutions.png)

5. Seleccione ambas solucións, **Mapa de entidades de escrita dual de Dynamics 365 Finance and Operations** e **Mapas de entidades de escrita dual de Dynamics 365 Project Operations** e, a seguir, seleccione **Aplicar**.

![Confirmar solucións](./media/14ConfirmSolutions.png)

Despois de aplicar as solucións, as entidades de escrita dual aplícanse ao ambiente.

![Aplicación de solucións](./media/15ApplyingSolutions.png)

Despois de aplicar as entidades, todas as asignacións dispoñibles aparecen no ambiente.

![Mapas de escrita dual](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a>Actualice as entidades de datos despois da actualización

1. En Finance, vaia á área de traballo **Xestión de datos**.

![Área de traballo de xestión de datos](./media/16DataManagement.png)

2. Seleccione o mosaico **Parámetros marco**.

![Parámetros do marco](./media/17FrameworkParameters.png)

3. Na páxina **Configuración de entidades**, seleccione **Actualizar lista de entidades**.

![Actualizar lista de entidades](./media/18RefreshEntityList.png)

A actualización tardará aproximadamente 20 minutos. Recibirá unha alerta cando remate.

![Actualizar confirmación](./media/19RefreshConfirmation.png)

## <a name="run-project-operations-dual-write-maps"></a>Executar mapas de escrita dual en Project Operations

1. No seu proxecto de LCS, vaia á páxina **Detalles do ambiente**.
2. En **Información do ambiente de Common Data Service**, seleccione **Ligazón a CDS para aplicacións.** Despois de seleccionar a ligazón, redirixiráselle á lista de entidades nas asignacións.
3. Inicie os mapas segundo se describe na seguinte táboa. Asegúrese de seguir a secuencia como aparece na lista.

| **Asignación de entidades** | **Actualizar entidade** | **Sincronización inicial** | **Padrón para a sincronización inicial** | **Executar requisitos previos** | **Sincronización inicial de requisitos previos** |
| --- | --- | --- | --- | --- | --- |
| **Roles de recursos do proxecto para todas as empresas (bookableresourcecategories)** | No | Si | Common Data Service | No | N\A |
| **Entidades legais (cdm\_companies)** | No | Si | Aplicacións de Finance and Operations | No | N\A |
| **Datos reais de integración de Project Operations (msdyn\_actuals)** | No | No | N\A | Si | No |
| **Liñas de contrato de proxecto (salesorderdetails)** | No | No | N\A | No | No |
| **Entidade de integración para as relacións de transaccións do proxecto (msdyn\_transactionconnections)** | No | No | N\A | No | N\A |
| **Fitos da liña de contrato de integración de Project Operations (msdyn\_contractlinesscheduleofvalues)** | No | No | N\A | No | N\A |
| **Entidade de integración de Project Operations para estimacións de gastos (msdyn\_estimateslines)** | No | No | N\A | No | N\A |
| **Entidade de integración de Project Operations para estimacións de horas (msdyn\_resourceassignments)** | No | No | N\A | No | N\A |
| **Entidade de exportación de gastos de proxecto de integración de Project Operations (msdyn\_expenses)** | Si | No | N\A | No | N\A |
| **Entidade de integración de Project Operations para estimacións de horas (msdyn\_resourceassignments)** | Si | No | N\A | No | N\A |

4. Para actualizar a entidade, seleccione o nome do mapa e logo seleccione **Actualizar entidades**. 
5. Proceda coa execución do mapa despois de completar a actualización.

![Actualizar mapa](./media/20RefreshMapping.png)

Antes de activar o seguinte mapa, verifique que o mapa da táboa estea en estado de **Execución**. A execución de mapas cun maior número de requisitos previos pode levar moito tempo.

Para executar un mapa con requisitos previos, active o conmutador **Mostrar mapas de entidades relacionadas**. Se a táboa indica **Sincronización inicial de requisitos previos** é **Non**, verifique que o indicador **Sincronización inicial** está **Desactivado** en todos os mapas de requisitos previos antes de executalo.

![Executar mapa](./media/21RunMap.png)

6. Valide que todos os mapas relacionados co proxecto están en estado de execución.

![Todos os mapas en execución](./media/22AllMapsRunning.png)

O seu ambiente de Project Operations agora está subministrado e configurado.
