---
title: Resolver problemas de traballo na grade de tarefas
description: Este tema ofrece a información de solución de problemas necesaria cando se traballa na grade de tarefas.
author: ruhercul
ms.date: 01/19/2021
ms.topic: article
ms.product: ''
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: a15a4752de7537b3f60d5ee3269c846257a1fe4a
ms.sourcegitcommit: 72fa1f09fe406805f7009fc68e2f3eeeb9b7d5fc
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/09/2021
ms.locfileid: "6213398"
---
# <a name="troubleshoot-working-in-the-task-grid"></a>Resolver problemas de traballo na grade de tarefas 

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Este tema describe como solucionar problemas que pode atopar ao traballar coa xestión de custos.

## <a name="enable-cookies"></a>Activar cookies

Project Operations require que se activen as cookies de terceiros para renderizar a estrutura de subdivisión do traballo. Cando as cookies de terceiros non estean activadas, no canto de ver tarefas, verá unha páxina en branco cando seleccione o separador **Tarefas** guía na páxina **Proxecto**.

![Separador en branco cando as cookies de terceiros non están activadas](media/blankschedule.png)


### <a name="workaround"></a>Outros métodos
Para os navegadores Microsoft Edge ou Google Chrome, os seguintes procedementos describen como actualizar a configuración do seu explorador para activar as cookies de terceiros.

#### <a name="microsoft-edge"></a>Microsoft Edge

1. Abra o explorador Edge.
2. Na esquina superior dereita, seleccione a icona de **puntos suspensivos** (...) e seleccione **Configuración**.
3. En **Cookies e permisos do sitio**, seleccione **Cookies e datos do sitio**.
4. Desactive **Bloquear cookies de terceiros**.

#### <a name="google-chrome"></a>Google Chrome

1. Abra o explorador Chrome.
2. Na esquina superior dereita, seleccione os tres puntos verticais e logo seleccione **Configuración**.
3. En **Privacidade e seguridade**, seleccione **Cookies e outros datos do sitio**.
4. Seleccione **Permitir todas as cookies**.

> [!IMPORTANT]
> Se bloquea as cookies de terceiros, bloquearanse todas as cookies e os datos doutros sitios, aínda que o sitio estea permitido na súa lista de excepcións.

## <a name="pex-endpoint"></a>Extremo de PEX

Project Operations requiren que un parámetro do proxecto faga referencia ao extremo de PEX. Este extremo é necesario para comunicarse co servizo usado para renderizar a estrutura de subdivisión do traballo. Se o parámetro non está activado, recibirá o erro "O parámetro do proxecto non é válido". 

### <a name="workaround"></a>Outros métodos
 ![Campo Extremo PEX no parámetro do proxecto](media/projectparameter.png)

1. Engada o campo **Extremo PEX** á páxina **Parámetros do proxecto**.
2. Actualice o campo co valor seguinte: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=/<id>&type=2`
3. Elimine o campo da páxina **Parámetros do proxecto**.

## <a name="privileges-for-project-for-the-web"></a>Privilexios para o proxecto para a web

Project Operations depende dun servizo de programación externo. O servizo require que un usuario teña varios roles atribuídos para ler e escribir a entidades relacionadas coa estrutura de subdivisión do traballo. Estas entidades inclúen tarefas do proxecto, atribucións de recursos e dependencias de tarefas. Se un usuario non pode renderizar a estrutura de subdivisión do traballo cando vai ao separador **Tarefas**, probablemente sexa porque o proxecto para Project Operations non se activou. Un usuario pode recibir un erro de rol de seguranza ou un erro relacionado cunha denegación de acceso.


## <a name="workaround"></a>Outros métodos

1. Vaia a **Configuración > Seguridade > Usuarios > Usuarios da aplicación**.  

   ![Lector de aplicacións](media/applicationuser.jpg)
   
2. Prema dúas veces no rexistro de usuario da aplicación para verificar o seguinte:

 - O usuario ten acceso ao proxecto. Esta verificación normalmente faise asegurándose de que o usuario ten o rol de seguranza **Xestor de proxectos**.
 - O usuario da aplicación Microsoft Project existe e está configurado correctamente.
 
3. Se este usuario non existe, pode crear un novo rexistro de usuario. Seleccione **Novos usuarios**. Cambie o formulario de entrada a **Usuario da aplicación** e, a seguir, engada o **ID de aplicación**.

   ![Detalles do usuario da aplicación](media/applicationuserdetails.jpg)

4. Verifique que ao usuario se lle asignou a licenza correcta e que o servizo está activado nos detalles dos plans de servizo da licenza.
5. Verifique que o usuario pode abrir project.microsoft.com.
6. Verifique a través dos parámetros do proxecto que o sistema apunta ao extremo correcto do proxecto.
7. Verifique que se crea o usuario da aplicación do proxecto.
8. Aplique ao usuario os seguintes roles de seguranza:

  - Usuario de Dataverse
  - Sistema de Project Operations
  - Sistema do proxecto

## <a name="error-when-updating-the-work-breakdown-structure"></a>Erro ao actualizar a estrutura de subdivisión do traballo

Cando se fai unha ou máis actualizacións na estrutura de subdivisión do traballo, os cambios finalmente fallan e non se gardan. Prodúcese un erro na grade de programación indicando que "Non se puideron gardar os cambios recentes que fixo".

### <a name="workaround"></a>Outros métodos

1. Verifique que ao usuario se lle asignou a licenza correcta e que o servizo está activado nos detalles dos plans de servizo da licenza.
2. Verifique que o usuario pode abrir project.microsoft.com.
3. Verifique que o sistema apunta ao extremo correcto do proxecto.
4. Verifique que se creou o usuario da aplicación do proxecto.
5. Aplique ao usuario os seguintes roles de seguranza:
  
  - Usuario de Dataverse ou usuario de base
  - Sistema de Project Operations
  - Sistema do proxecto
  - Sistema de escritura dual de Project Operations (Este rol é necesario se está a despregar o escenario baseado en recursos/sen fornecemento de Project Operations).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
