---
title: Aplicar datos de instalación e configuración da demostración
description: Este tema ofrece información sobre como aplicar os datos de instalación e configuración da demostración para Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 42e02f393e89d20b2a462645f519a3792bee8f2f
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948857"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations-lite-deployment---deal-to-proforma-invoicing"></a>Aplique os datos de instalación e configuración da demostración para o despregamento de Project Operations lite: oferta para facturación proforma

_**Despregamento de Lite - oferta para facturación proforma_

1. Descargue o [Paquete de datos mestres](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip). 
2. Vaia ao cartafol *ProjOpsDemoDataSetupAndMaster - Integrated CMT* e execute o ficheiro executable, *DataMigrationUtility*.
3. Na páxina 1 do Asistente de migración de configuración (CMT) de Common Data Service, seleccione **Importar datos** e logo seleccione **Continuar**.

![Migración da configuración](./media/1ConfigurationMigration.png)

4. Na páxina 2 do asistente de CMT, seleccione **Office 365** como o **Tipo de despregamento**.
5. Seleccione as caixas de verificación **Mostrar unha lista das organizacións dispoñibles** e **Mostrar avanzado**.
6. Seleccione a rexión do seu arrendatario, introduza as súas credenciais e logo seleccione **Iniciar sesión**.

![Inicio de sesión de configuración](./media/2ConfigurationSignin.png)

7. Na páxina 3, na lista de organizacións do arrendatario, seleccione a que organización desexa importar os datos de demostración e logo seleccione **Iniciar sesión**.
8. Na páxina 4, seleccione o ficheiro zip *MasterAndSetupData* desde o cartafol desempaquetado, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.

![Ficheiro ZIP](./media/3ZipFile.png)

![Seleccionar un ficheiro](./media/4SelectAFile.png)

9. Despois de seleccionar o ficheiro zip, seleccione **Importar datos**.

![Importar datos](./media/5ImportData.png)

10. A importación executarase durante aproximadamente de dous a dez minutos segundo a velocidade da rede. Cando finalice, saia do asistente de CMT. 
11. Comprobe se a súa organización ten datos nas seguintes 20 entidades:

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
- Detalle da frecuencia da factura
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
