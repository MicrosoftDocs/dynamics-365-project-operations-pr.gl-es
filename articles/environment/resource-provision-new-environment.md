---
title: Fornecer un novo ambiente
description: Este artigo ofrece información sobre como proporcionar un novo ambiente de Project Operations.
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 9cc3dafd6a2b6f92b585643c5d43ab52a3faf59e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931604"
---
# <a name="provision-a-new-environment"></a>Fornecer un novo ambiente

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_



Este artigo ofrece información sobre como proporcionar un novo Dynamics 365 Project Operations ambiente para escenarios baseados en recursos/non abastecidos.

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a>Activar o fornecemento automatizado de Project Operations nun proxecto de LCS

Siga os pasos seguintes para activar o fluxo de fornecemento automatizado de Project Operations para o seu proxecto de LCS.

1. Vaia a [LCS](https://lcs.dynamics.com/v2) e seleccione o mosaico **Xestión da funcionalidade de previsualización**.
2. Na lista **Funcionalidade de previsualización**, seleccione **Funcionalidade Project Operations** e, a seguir, seleccione **Funcionalidade de previsualización activada** para activar Project Operations.

   > [!NOTE]
   > Este paso só se realiza unha vez por proxecto de LCS.

## <a name="provision-a-project-operations-environment"></a>Fornecer un ambiente de Project Operations

1. Abre un novo Dynamics 365 Finance [ambiente de demostración](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) ou [entorno sandbox/produción](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) despregamento. 
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

     ![Configuración de despregamento.](./media/1DeploymentSettings.png)

    > [!IMPORTANT]
    > Seleccione **Acepto** para aceptar os termos do servizo e logo seleccione **Feito** para volver á configuración de despregamento.
    >
    >![Consentimento de despregamento.](./media/2DeploymentConsent.png)

7. Opcional - Aplique datos de demostración ao ambiente. Vaia a **Configuración avanzada**, seleccione **Personalizar a configuración da base de datos SQL** e estableza **Especificar un conxunto de datos para a base de datos de aplicacións** en **Demostración**.
8. Complete os restantes campos obrigatorios no asistente e confirme o despregamento. O tempo para fornecer o ambiente varía segundo o tipo de ambiente. A subministración pode levar ata seis horas.

   Despois de completar correctamente o despregamento, o ambiente mostrarase como **Despregado**.

9. Para confirmar que o ambiente se despregou correctamente, seleccione **Iniciar sesión** e inicie sesión no ambiente para confirmar.

    ![Detalles do ambiente.](./media/3EnvironmentDetails.png)

## <a name="apply-updates-to-the-finance-environment"></a>Aplicar actualizacións ao ambiente de Finance

Project Operations require un ambiente de Finance coa versión da aplicación **10.0.13 (10.0.569.20009)** ou superior.

É posible que teña que aplicar actualizacións de calidade ao seu ambiente de Finance para recibir esta versión.

1. En LCS, na páxina **Detalles do ambiente**, na sección **Actualizacións dispoñibles**, seleccione **Ver actualización**.

    ![Vexa as actualizacións.](./media/5ViewUpdates.png)

2. Na páxina **Actualizacións binarias**, seleccione **Gardar paquete.**

    ![Gardar paquete.](./media/6SavePackage.png)

3. Prema **Seleccionar todos** e logo seleccione **Gardar paquete**.

    ![Revise e garde as actualizacións.](./media/7ReviewAndSaveUpdates.png)

4. Introduza un nome e unha descrición do paquete e seleccione **Gardar**. Dependendo da conexión a Internet, este proceso pode levar algún tempo.

    ![Cargue o paquete á biblioteca de activos.](./media/8UploadPackageToAssetsLibrary.png)

5. Despois de gardar o paquete, seleccione **Feito** e garde este paquete na biblioteca de activos do seu proxecto de LCS.

   Gardar e validar o paquete pode levar uns 15 minutos.

6. Para aplicar a actualización, navegue ata a páxina **Detalles do ambiente** páxina en LCS e seleccione **Manter** > **Aplicar actualizacións**.

    ![Manteña os ambientes.](./media/9MaintainEnvironment.png)

7. Na lista de actualizacións seleccione o paquete que creou e seleccione **Aplicar**.

    ![Aplique as actualizacións.](./media/10ApplyUpdates.png)

   O servizo do ambiente levará algún tempo. Despois de completalo, o ambiente volverá a un estado despregado.

    ![Ambiente despregado.](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a>Establecer unha conexión de escrita dual 

1. No seu proxecto de LCS, vaia á páxina **Detalles do ambiente**.
2. En **Información do ambiente de Common Data Service**, seleccione **Ligazón a CDS para aplicacións**.
3. Despois de completar a ligazón, seleccione **Ligazón a CDS para aplicacións** de novo. Redixiráselle a escrita dual en Finance.

    ![Ligazón a CDS.](./media/12LinktoCDS.png)

4. Seleccione **Aplicar solución** para acceder ás entidades que serán asignadas na integración.

    ![Aplique as solucións.](./media/13ApplySolutions.png)

5. Seleccione ambas solucións, **Dynamics 365 Finance and Operations Mapa de entidades de escritura dual** e **Dynamics 365 Project Operations Mapas de entidades de escritura dual** e, a continuación, seleccione **Solicitar**.

    ![Confirme as solucións.](./media/14ConfirmSolutions.png)

    Despois de aplicar as solucións, as entidades de escrita dual aplícanse ao ambiente.

    ![Aplicación de solucións.](./media/15ApplyingSolutions.png)

    Despois de aplicar as entidades, todas as asignacións dispoñibles aparecen no ambiente.

    ![Mapas de escrita dual.](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a>Actualice as entidades de datos despois da actualización

1. En Finance, vaia á área de traballo **Xestión de datos**.

    ![Área de traballo de xestión de datos.](./media/16DataManagement.png)

2. Seleccione o mosaico **Parámetros marco**.

    ![Parámetros do marco.](./media/17FrameworkParameters.png)

3. Na páxina **Configuración de entidades**, seleccione **Actualizar lista de entidades**.

    ![Actualice a lista de entidades.](./media/18RefreshEntityList.png)

A actualización tardará aproximadamente 20 minutos. Recibirá unha alerta cando remate.

  ![Confirmación de actualización.](./media/19RefreshConfirmation.png)

## <a name="update-security-settings-on-project-operations-on-dataverse"></a>Actualizar a configuración de seguridade en Project Operations en Dataverse

1. Vaia a Project Operations no seu Dataverse ambiente. 
2. Vaia a **Configuración** > **Seguranza** > **Roles de seguranza**. 
3. Na páxina **Roles de seguranza**, na lista de roles, seleccione **usuario de aplicación de escritura dual** e seleccione o separador **Entidades personalizadas**.  
4. Comprobe que o rol ten permisos de **Lectura** e **Anexar a** para as seguintes entidades:
      
      - **Tipo de taxa de cambio de divisas**
      - **Gráfica de contas**
      - **Calendario fiscal**
      - **Libro maior**
      - **Empresa**
      - **Gasto**

5. Despois de actualizar o rol de seguranza, vaia a **Configuración** > **Seguridade** > **Equipos** e seleccione o equipo predefinido na vista de equipo **Propietario de empresa local**.
6. Seleccione **Xestionar roles** e comprobe que o privilexio de seguranza **usuario de aplicación de escritura dual** se aplica a este equipo.

## <a name="run-project-operations-dual-write-maps"></a>Executar mapas de escrita dual en Project Operations

1. No seu proxecto de LCS, vaia á páxina **Detalles do ambiente**.
2. En **Información do ambiente de Common Data Service**, seleccione **Ligazón a CDS para aplicacións.** Despois de seleccionar a ligazón, redirixiráselle á lista de entidades nas asignacións.
3. Inicie os mapas. Para obter máis información, consulte [Versións de mapa de escrita dual de Project Operations](resource-dual-write-maps.md#project-operations-dual-write-maps)
4. Valide que todos os mapas relacionados co proxecto están en estado de execución.

    ![Todos os mapas en execución.](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a>Aplicar os datos de configuración en CDS para Project Operations (opcional)

Se aplicou datos de demostración ao ambiente de Finance, consulte [Configurar e aplicar os datos de configuración en Common Data Service para Project Operations](resource-apply-pro-setup-config-data.md) para aplicar datos de demostración ao ambiente de CDS.


O seu ambiente de Project Operations agora está subministrado e configurado. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
