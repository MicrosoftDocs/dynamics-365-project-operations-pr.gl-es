---
title: Aplicar os datos de demostración a un ambiente aloxado na nube de Finance
description: Este artigo explica como aplicar datos de demostración de Project Operations a un ambiente aloxado na nube de Dynamics 365 Finance.
author: sigitac
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 793b1a01f3bf692bb9f4c2d9abad9a44b110544a
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029895"
---
# <a name="apply-demo-data-to-a-finance-cloud-hosted-environment"></a>Aplicar os datos de demostración a un ambiente aloxado na nube de Finance

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

> [!IMPORTANT]
> Este artigo só é aplicable a Microsoft Dynamics 365 Finance versión 10.0.13 e só se pode executar nun ambiente aloxado na nube. Complete os pasos deste artigo **ANTES** de aplicar actualizacións de calidade ao ambiente.

1. No seu proxecto LCS, abra a páxina **Detalles do ambiente**. Teña en conta que inclúe os detalles necesarios para conectarse ao ambiente mediante o protocolo de escritorio remoto (RDP).

![Detalles do ambiente.](./media/1EnvironmentDetails.png)

O primeiro conxunto de credenciais resaltadas son as credenciais da conta local e conteñen unha hiperligazón á conexión de escritorio remoto. As credenciais inclúen o nome de usuario e o contrasinal do administrador do entorno. O segundo conxunto de credenciais úsase para iniciar sesión en SQL Server neste ambiente.

2. Conéctese ao ambiente a través da hiperligazón en **Contas locais** e use as **Credenciais da conta local** para autenticar.
3. Vaia a **Servizos de Información en Internet** > **Agrupacións de aplicacións** > **AOSService** e deteña o servizo. Está detendo o servizo neste momento para poder continuar e substituír a base de datos SQL.

![Deter AOS.](./media/2StopAOS.png)

4. Vaia a **Servizos** e deteña os dous elementos seguintes:

- Microsoft Dynamics 365 Unified Operations: Servizo de xestión de lotes
- Microsoft Dynamics 365 Unified Operations: Marco de importación e exportación de datos

![Deter servizos.](./media/3StopServices.png)

5. Abra Microsoft SQL Server Management Studio. Inicie sesión coas credenciais do servidor SQL e use o usuario e o contrasinal axdbadmin da páxina **Detalles de ambientes** de LCS.

![SQL Server Management Studio.](./media/4SSMS.png)

6. No explorador de obxectos, vaia a **Bases de datos** e localice **AXDB**. Substituirá a base de datos por unha nova base de datos situada no [Centro de descargas](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip). 
7. Copie o ficheiro zip na VM á que está conectado de forma remota e extraia o contido do ficheiro zip.
8. En SQL Server Management Studio, prema dúas veces en **AxDB** e logo seleccione **Tarefas** > **Restaurar** > **Base de datos**.

![Restaurar base de datos.](./media/5RestoreDatabase.png)

9. Seleccione **Dispositivo de orixe** e navegue ata o ficheiro extraído do zip que copiou.

![Dispositivos de orixe.](./media/6SourceDevice.png)

10. Seleccione **Opcións** e, a seguir, seleccione **Sobrescribir a base de datos existente** e **Pechar as conexións existentes coa base de datos de destino**. 
11. Seleccione **Aceptar**.

![Restaurar configuración.](./media/7RestoreSetting.png)

Recibirá a confirmación de que a restauración de AXDB tivo éxito. Despois de recibir esta confirmación, pode pechar SQL Services Management Studio.

12. Volva a **Servizos de Información en Internet** > **Agrupacións de aplicacións** > **AOSService** e inicie AOSService.
13. Vaia a **Servizos** e inicie os dous servizos que detivo antes.

14. Localice a ferramenta AdminUserProvisioning nesta VM. Mire en K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.
15. Execute o ficheiro .ext usando o seu enderezo de usuario no campo **Enderezo de correo electrónico**. 
16. Seleccione **Enviar**.

![Fornecemento de usuario administrador.](./media/8AdminUserProvisioning.png)

Isto tarda un par de minutos en completarse. Debería recibir unha mensaxe de confirmación de que o usuario administrador se actualizou correctamente.

17. Por último, execute o símbolo do sistema como administrador e execute iisreset

![Restablecemento de IIS.](./media/9IISReset.png)

18. Peche a sesión de escritorio remoto e use a páxina **Detalles do ambiente** para iniciar sesión no ambiente e confirmar que funciona como se esperaba.

![Finanzas e operacións.](./media/10FinanceAndOperations.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]