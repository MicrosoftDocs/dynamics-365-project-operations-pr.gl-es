---
title: Aplicación para móbil Project Timesheet
description: Este tema ofrece información sobre a aplicación para móbil Microsoft Dynamics 365 Project Timesheet. A aplicación para móbil Project Timesheet permite aos usuarios enviar e aprobar follas de control horario para proxectos no seu dispositivo móbil.
author: abruer
manager: AnnBe
ms.date: 04/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: b9cbd84ecb0d71a99982e158d7e0ea1e236fb369
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076305"
---
# <a name="project-timesheet-mobile-application"></a>Aplicación para móbil Project Timesheet

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Visión xeral

A aplicación para móbil Microsoft Dynamics 365 Project Timesheet permite aos usuarios enviar e aprobar follas de control horario para proxectos no seu dispositivo móbil (iPhone ou Android). Esta aplicación para móbil presenta a funcionalidade de folla de control horario que reside na área de xestión de proxectos e contabilidade de Dynamics 365 Finance, mellorando a produtividade e eficiencia dos usuarios, ademais de permitir a entrada e aprobación oportuna das follas de control horario do proxecto.

## <a name="download-and-install-the-mobile-app"></a>Descargar e instalar a aplicación móbil

Descargue e instale a aplicación para móbil Microsoft Dynamics 365 Project Timesheet para Android ou iPhone desde a tenda móbil do seu dispositivo.

## <a name="enable-the-app"></a>Activar a aplicación 

En Finanzas, a aplicación para móbil Project Timesheet debe estar activada. Para activar a funcionalidade, vaia a **Parámetros de xestión de proxectos e contabilidade \> Folla de control horario** e seleccione o parámetro **Activar Microsoft Dynamics 365 Project Timesheet**.

## <a name="sign-in-to-the-app"></a>Inicie sesión na aplicación

1.  Inicie a aplicación no seu dispositivo móbil.

2.  Introduza o seu URL de Finanzas.

3.  A primeira vez que inicie sesión, solicítaselle o seu nome de usuario e contrasinal. Introduza as súas credenciais.

4.  Iniciará sesión na súa empresa predefinida.

## <a name="submit-a-project-timesheet"></a>Enviar unha folla de control horario do proxecto

Pode crear e enviar unha folla de control horario do proxecto na aplicación. Pode basear unha nova folla de control horario en información dunha folla de control horario anterior, liñas gardadas ou atribucións de proxectos. Se está designado como delegado, tamén pode introducir unha folla de control horario para outro traballador. Para crear unha folla de control horario como delegado, seleccione o botón **Menú** e logo seleccione un nome de recurso.

A páxina de folla de control horario creará unha nova folla de control horario para o período da folla de control horario, segundo a data actual. Mostrarase a semana laboral. Se a folla de control horario abrangue varias semanas, pode seleccionar outra semana laboral nos separadores da semana laboral.
Se existe unha folla de control horario para a data actual, mostrarase. Se precisa crear unha nova folla de control horario nun período de folla de control horario diferente, seleccione o botón **Menú** e logo seleccione **Nova folla de control horario**.

Pode introducir a información do proxecto premendo a acción **Engadir tempo** ou a acción **Copiar tempo desde**. A acción **Copiar o tempo desde** copiará a información da liña do proxecto, pero non as horas. O menú **Copiar tempo desde** inclúe as seguintes opcións:

- **Copiar desde folla de control horario existente** - Copie as liñas da folla de control horario desde unha folla de control horario existente.

- **Copiar desde favorito** - Cree novas liñas de folla de control horario empregando as configuracións da folla de control horario que seleccionou como favoritos.

- **Copiar desde atribución** - Crear novas liñas de follas de control horario a partir de proxectos atribuídos.

A información do proxecto que se amosa depende dos parámetros móbiles que definiu na páxina **Parámetros de xestión de proxectos e contabilidade**.

No campo **Persoa xurídica**, seleccione a persoa xurídica para a que realizou o traballo do proxecto. O campo **Persoa xurídica** só está dispoñible se a compatibilidade coa folla de control horario entre empresas está activada para a súa persoa xurídica.

Seleccione o cliente que está asociado ao proxecto para a folla de control horario. Para o lanzamento inicial no Android, non se admite a entrada por cliente, xa que primeiro debe seleccionar o proxecto. Se seleccionou primeiro o proxecto, o campo **Cliente** énchese automaticamente.

No campo **Proxecto**, seleccione o proxecto para o que está introducindo o tempo. O campo **Cliente** énchese automaticamente.

As buscas de clientes e proxectos permiten a busca tanto en clientes como en proxectos.

Seleccione información nos campos **Categoría**, **Actividade**, **Propiedade da liña**, **Grupo do imposto sobre as vendas** e **Grupo do imposto sobre as vendas de artigos** segundo o requirido. Estes campos pódense anular.

O campo **Propiedade da liña** establecerase nun valor predefinido, baseado nos parámetros de xestión de proxectos e contabilidade. Cando os parámetros de proxecto/categoría e categoría/recurso están activados, o valor **Propiedade da liña** establecerase no valor predefinido que definiu para esta validación. Cando os parámetros proxecto/categoría e categoría/recurso non están activados, o valor **Propiedade da liña** será o predefinido segundo o campo **Activar propiedade de liña predefinida** na páxina **Parámetros de xestión de proxectos e contabilidade**. O valor **Propiedade da liña** pódese anular.

Seleccione un día para engadir tempo. Introduza o número de horas que traballou cada día.

Para engadir comentarios sobre as horas que está a introducir, prema **Engadir comentarios** e, a seguir, introduza comentarios para un público interno, público de clientes ou ambos.
Os xestores de proxectos poden ver os comentarios internos. Os comentarios dos clientes inclúense nas facturas.

Para gardar a liña como favorito, seleccione a caixa de verificación e prema **Gardar como favorito**.

A dimensión financeira e a compatibilidade con anexos non se proporcionan na aplicación para móbil.

Continúe engadindo liñas de proxecto segundo sexa necesario para completar a súa folla de control horario.

Prema **Enviar** para enviar a folla de control horario ao fluxo de traballo de aprobación.

## <a name="review-timesheets"></a>Revisar follas de control horario

No menú está dispoñible unha lista das follas de control horario que hai que revisar. Esta opción só está dispoñible se foi designado como responsable de aprobación de fluxo de traballo. Admítese a aprobación de cabeceira e de liña. A aprobación a nivel de liña ofrece a posibilidade de marcar unha ou máis liñas para a súa aprobación. Despois de revisar a información da folla de control horario, prema **Aprobar**, **Delegar** ou **Retornar** para continuar o fluxo de traballo.
