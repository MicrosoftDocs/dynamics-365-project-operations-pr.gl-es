---
title: Actualizar Project Operations no seu ambiente de Finance
description: Este tema ofrece información sobre como actualizar Project Operations no seu ambiente de Dynamics 365 Finance.
author: ruhercul
manager: tfehr
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d68296ec59f0bd58f848154c90e02c58f275ab12
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291977"
---
# <a name="update-project-operations-in-your-finance-environment"></a>Actualizar Project Operations no seu ambiente de Finance

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_


Este tema ofrece información sobre como actualizar Dynamics 365 Project Operations no seu ambiente de Dynamics 365 Finance. Hai tres procedementos necesarios para actualizar Project Operations á actualización 5 (UR5):

- [Importar o paquete ao seu proxecto de previsualización](#import)
- [Aplicar a actualización](#apply)
- [Actualizar o seu ambiente de Dataverse](#update)

## <a name="import-the-package-into-your-lcs-project"></a><a name="import"></a>Importar o paquete ao seu proxecto de LCS

1. Iniciar sesión en [Lifecycle Services (LCS)](https://lcs.dynamics.com/) como propietario do proxecto ou xestor do ambiente.
2. Na lista de proxectos, seleccione o seu proxecto de LCS.
3. Na páxina **Proxecto**, no grupo **Ambientes**, abra o ambiente que desexe actualizar.
4. Verifique que o ambiente se está a executar. Se non se inicia, inicie o ambiente.
5. Na sección **Nova versión** en **Actualizacións dispoñibles**, seleccione **Ver actualización** para 10.0.15.

![Botón de ver actualización](media/view-update.png)

6. Na páxina **Actualizacións binarias**, seleccione **Gardar paquete**.
7. Na páxina **Revisar e gardar actualizacións**, seleccione **Gardar paquete**.
8. No panel **Gardar paquete na biblioteca de activos** que se abre, introduza o nome do paquete e logo seleccione **Gardar paquete**.
9. Cando LCS remate de gardar o paquete, actívase o botón **Feito**. Seleccione **Feito**. LCS verificará o paquete. A verificación pode levar uns minutos ou ata unha hora.


## <a name="apply-the-package-update"></a><a name="apply"></a>Aplicar a actualización do paquete

1. En LCS, na páxina **Detalles do ambiente**, seleccione **Manter** > **Aplicar actualizacións**.
2. Na lista, seleccione o paquete que gardou anteriormente e logo seleccione **Solicitar**.
3. Seleccione **Si** para confirmar que desexa despregar o paquete.

![Caixa de diálogo de confirmar o despregamento do paquete](media/confirm-package-deployment.png)

4. Seleccione **Si** para confirmar que desexa actualizar a aplicación.

![Caixa de diálogo de confirmar a actualización da aplicación](media/confirm-application-update.png)

Comezará o despregamento e a actualización da aplicación. 

Na páxina **Detalles do ambiente**, na esquina superior dereita, o estado do ambiente actualizarase a **Mantemento**. En aproximadamente dúas horas, a actualización estará completa. A información da versión da aplicación actualizarase a **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** e o estado do ambiente actualizarase a **Despregado**.


## <a name="update-your-dataverse-environment"></a><a name="update"></a>Actualizar o seu ambiente de Dataverse

1. Inicie sesión no [Centro de administración de Power Platform](https://admin.powerplatform.com/).
2. Na lista, busque e abra o ambiente que utilizou para instalar Project Operations.
3. Na páxina **Ambientes**, seleccione **Recurso** > **Aplicacións de Dynamics 365**.
4. Na lista, localice **Microsoft Dynamics 365 Project Operations**, e na columna **Estado**, seleccione **Actualización dispoñible**.
5. Seleccione a caixa de verificación **Acepto as condicións do servizo** e logo seleccione **Actualizar**. Instalarase a versión máis recente da solución.

Despois de completar a instalación, terá instalada a versión 4.5.0.134.

## <a name="configure-new-features"></a>Configurar novas funcionalidades

### <a name="enable-dual-write-mapping"></a>Activar a asignación de escrita dual

Despois de completar a actualización nos ambiente de Finance e Dataverse, pode activar as asignacións de escritura dual requiridas. Complete os seguintes procedementos para activar as asignacións de escritura dual.

- [Actualice a configuración de seguridade no ambiente de Customer Engagement](#security)
- [Actualizar entidades de datos](#refresh)
- [Actualizar e executar as asignacións de escritura dual](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a>Actualizar a configuración de seguridade no ambiente de Dataverse

As seguintes actualizacións dos privilexios de seguridade para entidades son necesarias como parte da actualización a UR5.

1. No seu ambiente de Dataverse, vaia a **Configuración**, e no grupo **Sistema**, seleccione **Seguridade**.

![Configuración de ambientes de Dataverse](media/Picture21.png)

2. Seleccionar **Roles de seguranza**.
3. Na lista de roles, seleccione **usuario de aplicación de escritura dual** e seleccione o separador **Entidades personalizadas**. 
4. Comprobe que o rol ten os permisos de **Ler** e **Anexar a** para:

      - **Tipo de taxa de cambio de divisas**
      - **Gráfica de contas** 
      - **Calendario fiscal** 
      - **Libro maior**

5. Despois de actualizar o rol de seguranza, vaia a **Configuración** > **Seguridade** > **Equipos**. Verifique que o rol **usuario de aplicación de escritura dual** se aplicou ao equipo. 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a>Actualizar as entidades de datos desde a actualización

1. No seu ambiente de Finance, abra a área de traballo **Xestión de datos** e logo abra a páxina **Parámetros marco**.
2. No separador **Configuración da entidade**, seleccione **Actualizar lista de entidades**.
3. Seleccione **Pechar** para confirmar a actualización da entidade.

 > [!NOTE]
 > Este proceso pode tardar aproximadamente 20 minutos en completarse. Recibirá unha notificación cando remate a actualización.

### <a name="update-dual-write-mappings"></a><a name="run"></a>Actualizar asignacións de escrita dual

1. Na área de traballo **Xestión de datos**, seleccione **Escritura dual**.
2. Seleccione **Aplicar solucións**, seleccione ambas solucións da lista e logo seleccione **Aplicar**.
3. Na páxina **Escritura dual**, seleccione os seguintes mapas da táboa e logo seleccione **Parar**.

    - **Datos reais de integración de Project Operations (msdyn_actuals)**
    - **Categorías de gastos do proxecto de integración de Project Operations (msdyn_expensecategories)**
    - **Entidade de exportación de gastos do proxecto de datos reais de integración de Project Operations (msdyn_expensecategories)**

4. Na páxina **Versión do mapa de táboas**, aplique unha nova versión do mapa a cada unha das tres entidades.
5. Na páxina **Escritura dual**, seleccione executar para reiniciar os mapas.
6. Na lista de mapas, seleccione o papa de **Libro maior (msdyn_ledgers)** con todos os requisitos previos e seleccione a caixa de verificación **Sincronización inicial**. 
7. No campo **Padrón para a sincronización inicial**, seleccione **aplicacións de Finance and Operations** e logo seleccione **Executar**.
 
 ![Sincronización de mapa de libro maior](media/DW6.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]