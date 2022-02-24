---
title: Configurar e aplicar datos de configuración en Common Data Service
description: Este tema ofrece información sobre como configurar e aplicar os datos de configuración en Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7742e81316b217066f9f3b8d5c23aa64f1a7efc4
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642226"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a>Configurar e aplicar datos de configuración en Common Data Service 

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a>Requisitos previos

Antes de comezar a configurar datos en Common Data Service (CDS), deben cumprirse os seguintes requisitos previos:

1.  Proporcionar un ambiente de CDS e un ambiente de Dynamics 365 Finance ambiente para Project Operations.
2.  A información da entidade legal de Dynamics 365 Finance compártese co ambiente de CDS. Isto significa que a entidade **Empresa** en CDS ten os seguintes rexistros da empresa:
  - THPM
  - USPM
  - GBPM

## <a name="install-setup-and-configuration-data"></a>Instale os datos de configuración

1. Descargue, desbloquee e descomprima o ficheiro [Paquete de datos de instalación e configuración](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).
2. Vaia ao cartafol descomprimido e execute o ficheiro executable, *DataMigrationUtility*.
3. Na páxina 1 do Asistente de migración de configuración (CMT) de Common Data Service, seleccione **Importar datos** e logo seleccione **Continuar**.

![Migración da configuración](./media/1ConfigurationMigration.png)

4. Na páxina 2 do asistente de CMT, seleccione **Microsoft 365** como o **Tipo de despregamento**.
5. Seleccione as caixas de verificación **Mostrar unha lista das organizacións dispoñibles** e **Mostrar avanzado**.
6. Seleccione a rexión do seu arrendatario, introduza as súas credenciais e seleccione **Iniciar sesión**.

![Inicio de sesión de configuración](./media/2ConfigurationSignin.png)

7. Na páxina 3, na lista de organizacións do arrendatario, seleccione a que organización desexa importar os datos de demostración e seleccione **Iniciar sesión**.
8. Na páxina 4, seleccione o ficheiro zip, *SampleSetupAndConfigData* do cartafol descomprimido.

![Selección de ficheiro Zip](./media/3ZipFile.png)

![Seleccionar un ficheiro](./media/4SelectAFile.png)

9. Despois de seleccionar o ficheiro zip, seleccione **Importar datos**.

![Datos de importación](./media/5ImportData.png)

10. A importación executarase durante aproximadamente de dous a dez minutos segundo a velocidade da rede. Cando finalice a importación, saia do asistente de CMT. 
11. Comprobe se a súa organización ten datos nas seguintes 19 entidades:

  - Moeda
  - Unidade organizativa
  - Contacto
  - Grupo fiscal
  - Grupo de clientes
  - Unidade
  - Grupo de unidades
  - Lista de prezos
  - Lista de prezos do parámetro do proxecto
  - Frecuencia da factura
  - Categoría de recursos reservables
  - Categoría da transacción
  - Categoría de gasto
  - Prezo do rol
  - Prezo da categoría da transacción
  - Característica
  - Recurso reservable
  - Asociación de categorías de recursos reservables
  - Característica de recursos reservables

![Completar importación](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a>Actualiza as configuracións de Project Operations

1. Vaia ao ambiente de CE. Podes atopalo abrindo o [Centro de administración de Power Platform](https://admin.powerplatform.microsoft.com/environments), seleccionando o ambiente e logo seleccionando **Ambiente aberto**. 

![Abrir ambiente](./media/7OpenEnvironment.png)

2. Vaia a **Proxectos** > **Recursos** e logo seleccione **Novo** para crear un recurso reservable para o seu usuario.

![Recursos reservables](./media/8BookableResources.png)

3. No separador **Xeral**, seleccione o seu usuario administrador. Verifique que o fuso horario coincide co fuso no que se atopa. 

![Novo recurso reservable](./media/9NewBookableResource.png)

4. No separador **Programación**, no campo **Empresa**, escolla a empresa **USPM** e seleccione **Gardar**. 

![Separador de programación](./media/10SchedulingTab.png)

5. Prema o separador **Horas de traballo**.  

![Horas laborables](./media/11WorkHours.png)

6. Prema dúas veces en calquera valor do calendario e seleccione **Editar** > **Todos os eventos da serie**. 

![Calendario de traballo](./media/12WorkCalendar.png)

7. Cambie as horas de traballo a un día de traballo de oito (8) horas, marque as fins de semana como días non laborables e asegúrese de que o fuso horario coincida co seu. 
8. Seleccione **Gardar e pechar**.

![Actualizar calendario](./media/13UpdateCalendar.png)

9. Vaia a **Configuración** > **Modelos de calendario** e seleccione **Novo**.
 
 ![Modelos de calendario](./media/14CalendarTemplates.png)
 
 10. Insira un nome, seleccione o recurso do modelo que creou e logo seleccione **Gardar**. 
 
 ![Gardar modelo de calendario](./media/15SaveCalendarTemplate.png)
 
 11. Vaia a **Parámetros** e faga dobre clic no rexistro. 
 
 ![Parámetros do proxecto](./media/16ProjectParameters.png)
 
12. Actualice os seguintes campos:

 - **Empresa predefinida**: USPM
 - **Unidade organizativa predefinida**: Contoso Robotics Global
 - **Frecuencia de facturas**: Sétimo e último día
 - **Modelo de horas de traballo**: Cambie ao modelo que creou.

13. Seleccione **Gardar**. 

![Parámetros do proxecto actualizados](./media/17UpdatedProjectParameters.png)
