---
title: Resolver problemas de traballo na grade de tarefas
description: Este tema ofrece a información de solución de problemas necesaria cando se traballa na grade de tarefas.
author: ruhercul
ms.date: 04/05/2022
ms.topic: article
ms.product: ''
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: ee80363cf6f9a65a91be43a84434d37f02511f26
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8596416"
---
# <a name="troubleshoot-working-in-the-task-grid"></a>Resolver problemas de traballo na grade de tarefas 


_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento, despregamento de Lite: facturación proforma, Project for the Web_

A grade Tarefa aproveitada por Dynamics 365 Project Operations é un iframe aloxado dentro de Microsoft Dataverse. Como resultado deste uso, débense cumprir requisitos específicos para garantir que a autenticación e a autorización funcionan correctamente. Este tema describe os problemas frecuentes que poden afectar a capacidade de representar a grade ou xestionar tarefas na estrutura de subdivisión do traballo (WBS).

Os problemas frecuentes son:

- O separador **Tarefa** da grade Tarefa está baleiro.
- Ao abrir o proxecto, o proxecto non se carga e a interface de usuario (IU) queda atascada no indicador de progreso.
- Administración de privilexios para **Project for the Web**.
- Os cambios non se gardan cando crea, actualiza ou elimina unha tarefa.

## <a name="issue-the-task-tab-is-empty"></a>Problema: o separador Tarefa está baleiro

### <a name="mitigation-1-enable-cookies"></a>Mitigación 1: Activar as cookies

Project Operations require que se activen as cookies de terceiros para representar a estrutura de subdivisión do traballo. Cando as cookies de terceiros non estean activadas, no canto de ver tarefas, verá unha páxina en branco cando seleccione o separador **Tarefas** guía na páxina **Proxecto**.

Para os navegadores Microsoft Edge ou Google Chrome, os seguintes procedementos describen como actualizar a configuración do seu explorador para activar as cookies de terceiros.

#### <a name="microsoft-edge"></a>Microsoft Edge

1. Abra o explorador Edge.
2. Na esquina superior dereita, seleccione a icona de **puntos suspensivos** (...) e seleccione **Configuración**.
3. En **Cookies e permisos do sitio**, seleccione **Cookies e datos do sitio**.
4. Desactive **Bloquear cookies de terceiros**.
5. Actualice o explorador. 

#### <a name="google-chrome"></a>Google Chrome

1. Abra o explorador Chrome.
2. Na esquina superior dereita, seleccione os tres puntos verticais e logo seleccione **Configuración**.
3. En **Privacidade e seguridade**, seleccione **Cookies e outros datos do sitio**.
4. Seleccione **Permitir todas as cookies**.
5. Actualice o explorador. 

> [!NOTE]
> Se bloquea as cookies de terceiros, bloquearanse todas as cookies e os datos doutros sitios, aínda que o sitio estea permitido na súa lista de excepcións.

### <a name="mitigation-2-validate-the-pex-endpoint-has-been-correctly-configured"></a>Mitigación 2: Validar que o extremo PEX se configurou correctamente

Project Operations requiren que un parámetro do proxecto faga referencia ao extremo de PEX. Este extremo é necesario para comunicarse co servizo que se usa para representar a estrutura de subdivisión do traballo. Se o parámetro non está activado, recibirá o erro "O parámetro do proxecto non é válido". Para actualizar o extremo PEX, complete os seguintes pasos.

1. Engada o campo **Extremo PEX** á páxina **Parámetros do proxecto**.
2. Identifique o tipo de produto que está a usar. Este valor úsase cando se establece o extremo PEX. Ao recuperalo, o tipo de produto xa está definido no extremo PEX. Manteña ese valor.
3. Actualice o campo co valor seguinte: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=<id>&type=2`. A seguinte táboa ofrece o parámetro de tipo que se debe usar en función do tipo de produto.

      | **Tipo de produto**                     | **Tipo de parámetro** |
      |--------------------------------------|--------------------|
      | Project for the Web na organización predefinida   | tipo=0             |
      | Project for the Web na organización nomeada de CDS | tipo=1             |
      | Project Operations                   | tipo=2             |

4. Elimine o campo da páxina **Parámetros do proxecto**.

### <a name="mitigation-3-sign-in-to-projectmicrosoftcom"></a>Mitigación 3: inicie sesión en project.microsoft.com
No teu Microsoft Edge navegador, abra unha nova pestana, vai a project.microsoft.com e inicie sesión usando o rol de usuario que está a usar para acceder a Operacións do proxecto.

## <a name="issue-the-project-doesnt-load-and-the-ui-is-stuck-on-the-spinner"></a>Problema: O proxecto non se carga e a interface de usuario está atascada no indicador de progreso

Para os efectos da autenticación, as ventás emerxentes deben estar activadas para que se cargue a grade Tarefa. Se as ventás emerxentes non están activadas, a pantalla quedará atascada no indicador de progreso de carga. A seguinte gráfica mostra a URL cunha etiqueta emerxente bloqueada na barra de enderezos, o que fai que o indicador de progreso quede atascado intentando cargar a páxina. 

   ![Indicador de progreso atascado e bloqueo de ventá emerxente.](media/popupsblocked.png)

### <a name="mitigation-1-enable-pop-ups"></a>Mitigación 1: Activar as ventás emerxentes

Cando o seu proxecto está atascado no indicador de progreso, é posible que as ventás emerxentes non estean activadas.

#### <a name="microsoft-edge"></a>Microsoft Edge

Hai dúas formas de activar as ventás emerxentes no explorador Edge.

1. No seu explorador Edge, seleccione a notificación na parte superior dereita do explorador.
2. Seleccione **Permitir sempre ventás emerxentes e redireccionamentos desde** o ambiente de Dataverse específico.
 
     ![Ventás emerxentes bloqueadas.](media/enablepopups.png)

Como alternativa, pode realizar un dos seguintes pasos.

1. Abra o explorador Edge.
2. Na esquina superior dereita, seleccione so **puntos suspensivos** (...) e logo seleccione **Configuración** > **Permisos do sitio** > **Ventás emerxentes e redireccionamentos**.
3. Desactive **Ventás emerxentes e redireccionamentos** para bloquear ventás emerxentes ou actíveo para permitir ventás emerxentes no seu dispositivo.
4. Despois de activar as ventás emerxentes, actualice o explorador. 

#### <a name="google-chrome"></a>Google Chrome
1. Abra o explorador Chrome.
2. Desprácese ata unha páxina onde as ventás emerxentes estean bloqueadas.
3. Na barra de enderezos, seleccione **Ventá emerxente bloqueada**.
4. Seleccione a ligazón para a ventá emerxente que queira ver.
5. Despois de activar as ventás emerxentes, actualice o explorador. 

> [!NOTE]
> Para ver sempre as ventás emerxentes do sitio, seleccione **Permitir sempre as ventás emerxentes e redireccionamentos desde [sitio]** e logo seleccione **Feito**.

## <a name="issue-3-administration-of-privileges-for-project-for-the-web"></a>Problema 3: Administración de privilexios para Project for the Web

Project Operations depende dun servizo de programación externo. O servizo require que un usuario teña asignadas varios roles que lle permitan ler e escribir a entidades relacionadas co WBS. Estas entidades inclúen tarefas do proxecto, atribucións de recursos e dependencias de tarefas. Se un usuario non pode representar o WBS cando navega ata o separador **Tarefas**, probablemente sexa porque **Proxecto** para **Project Operations** non está activado. Un usuario pode recibir un erro de rol de seguranza ou un erro relacionado cunha denegación de acceso.

### <a name="mitigation-1-validate-the-application-user-and-end-user-security-roles"></a>Mitigación 1: Validar os roles de seguranza do usuario da aplicación e do usuario final

1. Vaia a **Configuración** > **Seguranza** > **Usuarios** > **Usuarios da aplicación**.  

   ![Lector de aplicacións.](media/applicationuser.jpg)
   
2. Prema dúas veces no rexistro de usuario da aplicación para verificar:

     - O usuario ten acceso ao proxecto. Pode facelo verificando que o usuario ten o rol de seguranza **Xestor de proxectos**.
     - O usuario da aplicación Microsoft Project existe e está configurado correctamente.
 
3. Se este usuario non existe, cree un novo rexistro de usuario. 
4. Seleccione **Novos usuarios**, cambie o formulario de entrada a **Usuario da aplicación** e, a seguir, engada o **ID de solicitude**.

   ![Detalles do usuario da aplicación.](media/applicationuserdetails.jpg)


## <a name="issue-4-changes-arent-saved-when-you-create-update-or-delete-a-task"></a>Problema 4: Os cambios non se gardan cando crea, actualiza ou elimina unha tarefa

Cando fai unha ou máis actualizacións de WBS, os cambios fallan e non se gardan. Prodúcese un erro na grade de programación cunha mensaxe que di: "Non se puido gardar o cambio recente que fixo".

### <a name="mitigation-1-validate-the-license-assignment"></a>Mitigación 1: Validar a atribución da licenza

1. Verifique que ao usuario se lle asignou a licenza correcta e que o servizo está activado nos detalles dos plans de servizo da licenza.  
2. Verifique que o usuario pode abrir **project.microsoft.com**.
    
### <a name="mitigation-2-validation-configuration-of-the-project-application-user"></a>Mitigación 2: Configuración de validación do usuario da aplicación do proxecto
1. Verifique que se creou o usuario da aplicación do proxecto.
2. Aplique ao usuario os seguintes roles de seguranza:
  
  - Usuario de Dataverse ou usuario de base
  - Sistema de Project Operations
  - Sistema do proxecto
  - Sistema de escrita dual en Project Operations. Este rol é necesario para a situación de despregamento baseado en recursos/sen fornecemento de Project Operations.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
