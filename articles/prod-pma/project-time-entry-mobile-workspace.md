---
title: Área de traballo móbil de entrada de tempo do proxecto
description: Este artigo ofrece información sobre o espazo de traballo móbil de entrada de tempo do proxecto. Esta área de traballo permite aos usuarios introducir e aforrar tempo nun proxecto usando o seu dispositivo móbil.
author: Yowelle
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: a163e32dae0231b5d71d1de2dbb473593b989164
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919536"
---
# <a name="project-time-entry-mobile-workspace"></a>Área de traballo móbil de entrada de tempo do proxecto

[!include [banner](../includes/banner.md)]

Este artigo ofrece información sobre o **Entrada do tempo do proxecto** espazo de traballo móbil. Esta área de traballo permite aos usuarios introducir e aforrar tempo nun proxecto usando o seu dispositivo móbil.

Esta área de traballo móbil está pensada para ser usada xunto coa aplicación móbil Dynamics 365 Unified Ops. 

## <a name="overview"></a>Visión xeral
Como parte do seu traballo diario, os recursos do proxecto adoitan estar no sitio ou viaxando. A área de traballo móbil **Entrada do tempo do proxecto** permite aos usuarios introducir o seu tempo facturable ou non facturable dun proxecto no dispositivo móbil que elixan. Polo tanto, os recursos do proxecto poden rexistrar as entradas de tempo en calquera momento e en calquera lugar. Tamén poden ver as entradas de tempo que xa se rexistraron. 

Especificamente, na área de traballo móbil **Entrada de tempo do proxecto**, os usuarios poden realizar estas tarefas:

-   Para calquera data seleccionada, introducir o número de horas que dedicou a unha tarefa específica.
-   Buscar por nome do proxecto ou cliente para atopar o proxecto para o que se introduce o tempo.
-   Especificar a categoría e a actividade do tempo que dedicou.
-   Rexistrar o tempo como facturable ou non facturable para o proxecto.
-   Opcionalmente, introducir os comentarios internos ou externos.

## <a name="prerequisites"></a>Requisitos previos
Os requisitos previos son diferentes segundo a versión de Microsoft Dynamics 365 que se despregou para a súa organización.

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Requisitos previos se usas Dynamics 365 Finance
Se se despregou Finanzas para a súa organización, o administrador do sistema debe publicar a área de traballo móbil **Entrada do tempo do proxecto**. Para obter instrucións, consulte [Publicar unha área de traballo móbil](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace).

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a>Requisitos previos se usa a versión 1611 coa actualización da plataforma 3 ou posterior
Se se despregou a versión 1611 coa actualización da plataforma 3 ou posterior para a súa organización, o administrador do sistema debe cumprir os seguintes requisitos previos. 

<table>
<thead>
<tr class="header">
<th>Requisito previo</th>
<th>Rol</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">

<td>Implemente KB 4018050.</td>
<td>Administrador do sistema</td>
<td>KB 4018050 é unha actualización de X++ ou unha revisión de metadatos que contén a área de traballo móbil <strong>Entrada do tempo do proxecto</strong>. Para implementar KB 4018050, o administrador do sistema debe seguir estes pasos.
<ol>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Descargue a corrección de metadatos desde Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Instale a corrección de metadatos</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Cree un paquete despregable</a> que contén os modelos <strong>ApplicationSuite</strong> e <strong>ProjectMobile</strong> e logo cargue o paquete despregable a LCS.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Aplique o paquete despregable</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td>Publique a área de traballo móbil <strong>entrada de tempo do proxecto</strong>.</td>
<td>Administrador do sistema</td>
<td>Consulte <a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Publicar unha área de traballo móbil</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Descargar e instalar a aplicación móbil

Descarga e instala a aplicación móbil Finance and Operations:

-   [Para teléfonos Android](https://go.microsoft.com/fwlink/?linkid=850662)
-   [Para iPhones](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Inicie sesión na aplicación móbil.
1.  Inicie a aplicación no seu dispositivo móbil.
2.  Introduza o seu URL de Dynamics 365.
3.  A primeira vez que inicie sesión, solicítaselle o seu nome de usuario e contrasinal. Introduza as súas credenciais.
4.  Despois de iniciar sesión, móstranse as áreas de traballo dispoñibles para a súa empresa. Teña en conta que se o administrador do sistema publica unha nova área de traballo máis tarde, terá que actualizar a lista de áreas de traballo móbiles.

[![Tire para actualizar.](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a>Introducir o tempo empregando a área de traballo móbil de entrada de tempo do proxecto
1.  No seu dispositivo móbil, seleccione a área de traballo **Entrada de tempo do proxecto**.
2.  Seleccione **Entrada de tempo**. Amósanse as datas do calendario da semana actual.
3.  Para unha data seleccionada, seleccione **Accións** &gt; **Nova entrada**.
4.  Introduza o número de horas para rexistrar.
5.  Seleccione o proxecto para a entrada de tempo. Unha lista mostra os proxectos cargados na súa aplicación para o seu uso sen conexión. Por defecto, cárganse 50 elementos, pero un programador pode cambiar este número. Para obter máis información, consulte [Plataforma móbil](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).
6.  Se o seu proxecto non está na lista, seleccione **Buscar**. Busque por nome ou cambie á busca por nome do proxecto ou por cliente.
7.  Seleccione unha categoría. Unha lista mostra as categorías cargadas na súa aplicación para o seu uso sen conexión. Por defecto, cárganse 50 elementos, pero un programador pode cambiar este número. Para obter máis información, consulte [Plataforma móbil](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).
8.  Se a súa categoría non está na lista, seleccione **Buscar**. Busque por categoría ou cambie á busca por nome de categoría.
9.  Seleccione unha actividade. Unha lista mostra as actividades cargadas na súa aplicación para o seu uso sen conexión. Por defecto, cárganse 50 elementos, pero un programador pode cambiar este número. Para obter máis información, consulte [Plataforma móbil](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).
10. Se a súa actividade non está na lista, seleccione **Buscar**. Busca por número de actividade ou cambia á busca por finalidade.

11. Seleccione a propiedade de liña.
12. Opcional: Introduza os comentarios internos e externos.
13. Seleccione **Feito**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]