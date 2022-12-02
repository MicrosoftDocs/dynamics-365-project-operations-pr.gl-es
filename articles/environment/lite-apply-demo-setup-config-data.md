---
title: Aplicar datos de instalación e configuración da demostración - lite
description: Este artigo ofrece información sobre como aplicar os datos de instalación e configuración da demostración para Project Operations.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 9a3a99c326b7ebbdfa859c3298b35e910af0eb2a
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 09/07/2022
ms.locfileid: "9409988"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a>Aplicar a configuración de demostración e os datos de configuración para Project Operations - lite 

_**Despregamento de Lite - oferta para facturación proforma_



## <a name="prerequisites"></a>Requisitos previos

Antes de comezar a configuración, debe ter un ambiente de Dataverse subministrado para Dynamics 365 Project Operations.


## <a name="instructions"></a>Instrucións

1. Descargue o [Paquete de datos mestres](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip). 
2. Desprácese ata o cartafol *ProjOpsSampleSetupData - CE only CMT* e execute o ficheiro executable, *DataMigrationUtility*.
3. Na páxina 1 do Asistente de migración de configuración (CMT) de Common Data Service, seleccione **Importar datos** e logo seleccione **Continuar**.

    ![Migración da configuración.](./media/1ConfigurationMigration.png)

4. Na páxina 2 do asistente de CMT, seleccione **Microsoft 365** como o **Tipo de despregamento**.
5. Seleccione as caixas de verificación **Mostrar unha lista das organizacións dispoñibles** e **Mostrar avanzado**.
6. Seleccione a rexión do seu arrendatario, introduza as súas credenciais e logo seleccione **Iniciar sesión**.

   ![Inicio de sesión de configuración.](./media/2ConfigurationSignin.png)

7. Na páxina 3, na lista de organizacións do arrendatario, seleccione a que organización desexa importar os datos de demostración e logo seleccione **Iniciar sesión**.
8. Na páxina 4, seleccione o ficheiro zip *SampleSetupAndConfigData* dende o cartafol desempaquetado, *ProjOpsSampleSetupData - CE only CMT*.

   ![Ficheiro ZIP.](./media/3ZipFile.png)

   ![Seleccione un ficheiro.](./media/4SelectAFile.png)

9. Despois de seleccionar o ficheiro zip, seleccione **Importar datos**.

   ![Importe datos.](./media/5ImportData.png)

10. A importación executarase durante aproximadamente de dous a dez minutos segundo a velocidade da rede. Cando finalice, saia do asistente de CMT. 
11. Comprobe se a súa organización ten datos nas seguintes 18 entidades:

    -   Moeda
    -   Conta
    -   Unidade organizativa
    -   Contacto
    -   Unidade
    -   Grupo de unidades
    -   Lista de prezos
    -   Lista de prezos do parámetro do proxecto 
    -   Frecuencia da factura
    -   Categoría de recursos reservables
    -   Categoría da transacción
    -   Categoría de gasto
    -   Prezo do rol
    -   Prezo da categoría da transacción
    -   Característica
    -   Recurso reservable
    -   Asociación de categorías de recursos reservables
    -   Característica de recursos reservables

    ![Complete a importación.](./media/6CompleteImport.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
