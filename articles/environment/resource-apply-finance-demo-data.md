---
title: Aplicar os datos de demostración de Project Operations a un ambiente aloxado na nube de Finance
description: Este tema explica como aplicar datos de demostración de Project Operations a un ambiente aloxado na nube de Dynamics 365 Finance.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b9af6c71b61840f4ffdf2892d8e7e5bbf0f8df67
ms.sourcegitcommit: 91ad491e94a421f256a378b0f4b26ed48c67bc93
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/22/2020
ms.locfileid: "4096620"
---
# <a name="apply-project-operations-demo-data-to-a-finance-cloud-hosted-environment"></a><span data-ttu-id="62bf6-103">Aplicar os datos de demostración de Project Operations a un ambiente aloxado na nube de Finance</span><span class="sxs-lookup"><span data-stu-id="62bf6-103">Apply Project Operations demo data to a Finance Cloud-hosted environment</span></span>

<span data-ttu-id="62bf6-104">_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_</span><span class="sxs-lookup"><span data-stu-id="62bf6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="62bf6-105">Este tema só é aplicable a Microsoft Dynamics 365 Finance versión 10.0.13 e só se pode executar nun ambiente aloxado na nube.</span><span class="sxs-lookup"><span data-stu-id="62bf6-105">This topic is only applicable only Microsoft Dynamics 365 Finance version 10.0.13 and can be performed only on a Cloud-hosted environment.</span></span> <span data-ttu-id="62bf6-106">Complete os pasos deste tema **ANTES** de aplicar actualizacións de calidade ao ambiente.</span><span class="sxs-lookup"><span data-stu-id="62bf6-106">Complete the steps in this topic **BEFORE** you apply quality updates to the environment.</span></span>

1. <span data-ttu-id="62bf6-107">No seu proxecto LCS, abra a páxina **Detalles do ambiente**.</span><span class="sxs-lookup"><span data-stu-id="62bf6-107">In your LCS project, open the **Environment details** page.</span></span> <span data-ttu-id="62bf6-108">Teña en conta que inclúe os detalles necesarios para conectarse ao ambiente mediante o protocolo de escritorio remoto (RDP).</span><span class="sxs-lookup"><span data-stu-id="62bf6-108">Notice that it includes the details needed to connect to the environment by using Remote Desktop Protocol (RDP).</span></span>

![Detalles do ambiente de ](./media/1EnvironmentDetails.png)

<span data-ttu-id="62bf6-110">O primeiro conxunto de credenciais resaltadas son as credenciais da conta local e conteñen unha hiperligazón á conexión de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="62bf6-110">The first set of highlighted credentials are the local account credentials and contain a hyperlink to the remote desktop connection.</span></span> <span data-ttu-id="62bf6-111">As credenciais inclúen o nome de usuario e o contrasinal do administrador do entorno.</span><span class="sxs-lookup"><span data-stu-id="62bf6-111">The credentials include the environment admin username and password.</span></span> <span data-ttu-id="62bf6-112">O segundo conxunto de credenciais úsase para iniciar sesión en SQL Server neste ambiente.</span><span class="sxs-lookup"><span data-stu-id="62bf6-112">The second set of credentials are used to log in to SQL Server in this environment.</span></span>

2. <span data-ttu-id="62bf6-113">Conéctese ao ambiente a través da hiperligazón en **Contas locais** e use as **Credenciais da conta local** para autenticar.</span><span class="sxs-lookup"><span data-stu-id="62bf6-113">Remote to the environment by the hyperlink in **Local Accounts** , and use the **Local Account credentials** to authenticate.</span></span>
3. <span data-ttu-id="62bf6-114">Vaia a **Servizos de Información en Internet** > **Agrupacións de aplicacións** > **AOSService** e deteña o servizo.</span><span class="sxs-lookup"><span data-stu-id="62bf6-114">Go to **Internet Information Services** > **Application Pools** > **AOSService** and stop the service.</span></span> <span data-ttu-id="62bf6-115">Está detendo o servizo neste momento para poder continuar e substituír a base de datos SQL.</span><span class="sxs-lookup"><span data-stu-id="62bf6-115">You are stopping the service at this point so that you can continue to replace the SQL database.</span></span>

![Deter AOS](./media/2StopAOS.png)

4. <span data-ttu-id="62bf6-117">Vaia a **Servizos** e deteña os dous elementos seguintes:</span><span class="sxs-lookup"><span data-stu-id="62bf6-117">Go to **Services** and stop the following two items:</span></span>

- <span data-ttu-id="62bf6-118">Microsoft Dynamics 365 Unified Operations: Servizo de xestión de lotes</span><span class="sxs-lookup"><span data-stu-id="62bf6-118">Microsoft Dynamics 365 Unified Operations: Batch Management Service</span></span>
- <span data-ttu-id="62bf6-119">Microsoft Dynamics 365 Unified Operations: Marco de importación e exportación de datos</span><span class="sxs-lookup"><span data-stu-id="62bf6-119">Microsoft Dynamics 365 Unified Operations: Data Import Export Framework</span></span>

![Deter servizos](./media/3StopServices.png)

5. <span data-ttu-id="62bf6-121">Abra Microsoft SQL Server Management Studio.</span><span class="sxs-lookup"><span data-stu-id="62bf6-121">Open Microsoft SQL Server Management Studio.</span></span> <span data-ttu-id="62bf6-122">Inicie sesión coas credenciais do servidor SQL e use o usuario e o contrasinal axdbadmin da páxina **Detalles de ambientes** de LCS.</span><span class="sxs-lookup"><span data-stu-id="62bf6-122">Log in with SQL server credentials and use the axdbadmin user and password from the LCS **Environments details** page.</span></span>

![SQL Server Management Studio](./media/4SSMS.png)

6. <span data-ttu-id="62bf6-124">No explorador de obxectos, vaia a **Bases de datos** e localice **AXDB**.</span><span class="sxs-lookup"><span data-stu-id="62bf6-124">In Object Explorer, **Databases** and locate **AXDB**.</span></span> <span data-ttu-id="62bf6-125">Substituirá a base de datos por unha nova base de datos situada no [Centro de descargas](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip).</span><span class="sxs-lookup"><span data-stu-id="62bf6-125">You will replace database with a new database that is located in the [Download Center](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip).</span></span> 
7. <span data-ttu-id="62bf6-126">Copie o ficheiro zip na VM á que está conectado de forma remota e extraia o contido do ficheiro zip.</span><span class="sxs-lookup"><span data-stu-id="62bf6-126">Copy the zip file to the VM you are remoted into and extract zip contents.</span></span>
8. <span data-ttu-id="62bf6-127">En SQL Server Management Studio, prema dúas veces en **AxDB** e logo seleccione **Tarefas** > **Restaurar** > **Base de datos**.</span><span class="sxs-lookup"><span data-stu-id="62bf6-127">In SQL Server Management Studio, right-click **AxDB** , and then select **Tasks** > **Restore** > **Database**.</span></span>

![Restaurar base de datos](./media/5RestoreDatabase.png)

9. <span data-ttu-id="62bf6-129">Seleccione **Dispositivo de orixe** e navegue ata o ficheiro extraído do zip que copiou.</span><span class="sxs-lookup"><span data-stu-id="62bf6-129">Select **Source Device** and navigate to the file extracted from zip you copied.</span></span>

![Dispositivos de orixe](./media/6SourceDevice.png)

10. <span data-ttu-id="62bf6-131">Seleccione **Opcións** e, a seguir, seleccione **Sobrescribir a base de datos existente** e **Pechar as conexións existentes coa base de datos de destino**.</span><span class="sxs-lookup"><span data-stu-id="62bf6-131">Select **Options** , and then select **Overwrite the existing database** and **Close existing connections to destination database**.</span></span> 
11. <span data-ttu-id="62bf6-132">Seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="62bf6-132">Select **OK**.</span></span>

![Restaurar configuración](./media/7RestoreSetting.png)

<span data-ttu-id="62bf6-134">Recibirá a confirmación de que a restauración de AXDB tivo éxito.</span><span class="sxs-lookup"><span data-stu-id="62bf6-134">You will receive confirmation that the AXDB restore was successful.</span></span> <span data-ttu-id="62bf6-135">Despois de recibir esta confirmación, pode pechar SQL Services Management Studio.</span><span class="sxs-lookup"><span data-stu-id="62bf6-135">After you receive this confirmation, you can close SQL Services Management Studio.</span></span>

12. <span data-ttu-id="62bf6-136">Volva a **Servizos de Información en Internet** > **Agrupacións de aplicacións** > **AOSService** e inicie AOSService.</span><span class="sxs-lookup"><span data-stu-id="62bf6-136">Go back to **Internet Information Services** > **Application Pools** > **AOSService** and start the AOSService.</span></span>
13. <span data-ttu-id="62bf6-137">Vaia a **Servizos** e inicie os dous servizos que detivo antes.</span><span class="sxs-lookup"><span data-stu-id="62bf6-137">Go to **Services** and start the two services you stopped earlier.</span></span>

14. <span data-ttu-id="62bf6-138">Localice a ferramenta AdminUserProvisioning nesta VM.</span><span class="sxs-lookup"><span data-stu-id="62bf6-138">Locate the AdminUserProvisioning tool on this VM.</span></span> <span data-ttu-id="62bf6-139">Mire en K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.</span><span class="sxs-lookup"><span data-stu-id="62bf6-139">Look under, K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.</span></span>
15. <span data-ttu-id="62bf6-140">Execute o ficheiro .ext usando o seu enderezo de usuario no campo **Enderezo de correo electrónico**.</span><span class="sxs-lookup"><span data-stu-id="62bf6-140">Run the .ext file using your user address in the **Email Address** field.</span></span> 
16. <span data-ttu-id="62bf6-141">Seleccione **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="62bf6-141">Select **Submit**.</span></span>

![Fornecemento de usuario administrador:](./media/8AdminUserProvisioning.png)

<span data-ttu-id="62bf6-143">Isto tarda un par de minutos en completarse.</span><span class="sxs-lookup"><span data-stu-id="62bf6-143">This takes a couple of minutes to complete.</span></span> <span data-ttu-id="62bf6-144">Debería recibir unha mensaxe de confirmación de que o usuario administrador se actualizou correctamente.</span><span class="sxs-lookup"><span data-stu-id="62bf6-144">You should receive a confirmation message that the Admin user was successfully updated.</span></span>

17. <span data-ttu-id="62bf6-145">Por último, execute o símbolo do sistema como administrador e execute iisreset</span><span class="sxs-lookup"><span data-stu-id="62bf6-145">Lastly, run Command Prompt as Administrator and perform iisreset</span></span>

![Restablecemento de IIS](./media/9IISReset.png)

18. <span data-ttu-id="62bf6-147">Peche a sesión de escritorio remoto e use a páxina **Detalles do ambiente** para iniciar sesión no ambiente e confirmar que funciona como se esperaba.</span><span class="sxs-lookup"><span data-stu-id="62bf6-147">Close the remote desktop session and use the LCS **Environment details** page to log in to the environment to confirm it is working as expected.</span></span>

![Finance and Operations](./media/10FinanceAndOperations.png)
