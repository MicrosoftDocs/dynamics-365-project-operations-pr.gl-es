---
title: Aplicación de gastos para móbiles
description: Este tema ofrece información sobre a área de traballo móbil de xestión de gastos.
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 88251552a937f0a3a066e08b87dbd5f7b73c46c69776fbc788d37cc21fe73541
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993194"
---
# <a name="mobile-expense-app"></a>Aplicación de gastos para móbiles

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Este tema ofrece información sobre a área de traballo móbil de **Xestión de gastos**. Esta área de traballo permite aos usuarios capturar e cargar un recibo para que poidan anexalo a un informe de gastos máis tarde. Os usuarios tamén poden crear rapidamente unha liña de gasto mediante un recibo anexo e crear e xestionar os seus informes de gastos. Ademais, os responsables de aprobacións poden usar a área de traballo móbil **Xestión de gastos** para ver os informes de gastos que se lles atribúan e aprobar ou rexeitar eses informes de gastos.

Esta área de traballo móbil está pensada para ser usada xunto coa aplicación móbil Dynamics 365 Unified Ops.

Moitas organizacións requiren que se anexe unha copia dun recibo a un informe de gastos relacionados con viaxes ou negocios que un empregado presenta para o seu reembolso. A área de traballo móbil **Xestión de gastos** permite aos usuarios crear rapidamente novas liñas de gasto no dispositivo móbil que escollan usando unha foto anexada dun recibo. Como alternativa, os usuarios poden capturar unha foto dun recibo e despois anexala a un informe de gastos máis tarde. Os empregados tamén poden crear e xestionar os seus informes de gastos e despois envialos para a súa aprobación e reembolso mediante o seu dispositivo móbil.

En concreto, a área de traballo móbil **Xestión de gastos** permite aos usuarios realizar estas tarefas:

- Faga unha foto dun recibo. Cargue a foto do recibo e anéxea a un informe de gastos máis tarde.
- Cargue un ficheiro como recibo capturado. Despois pode anexar ese ficheiro a un informe de gastos máis tarde.
- Cree unha nova liña de gastos usando un recibo anexado. Despois pode engadir o elemento da liña a un informe de gastos máis tarde e envialo para a súa aprobación e reembolso.

Tamén pode utilizar estas funcionalidades:

- Cree un novo informe de gastos.
- Anexe transaccións con tarxeta de crédito e outros gastos creados previamente a un informe de gastos.
- Cree novos gastos para un informe de gastos.
- Anexe un recibo a calquera gasto para un informe de gastos, tomando unha foto do recibo ou cargando un ficheiro como recibo capturado.
- Dependendo da política de gastos da empresa, engada a lista de convidados a un gasto.
- Dependendo da política de gastos da empresa, detalle os gastos.
- Envíe un informe de gastos para a súa aprobación e reembolso.
- Aprobe ou rexeite os informes de gastos dos que sexa responsable de aprobación.

## <a name="prerequisites"></a>Requisitos previos
Os requisitos varían segundo a versión que se despregou para a súa organización.

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Requisitos previos se usa Dynamics 365 Finance 
Se se despregou Finanzas para a súa organización, o administrador do sistema debe publicar a área de traballo móbil **Xestión de gastos**. 

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
<td>Implemente KB 4019015.</td>
<td>Administrador do sistema</td>
<td>KB 4019015 é unha actualización de X++ ou unha revisión de metadatos que contén a área de traballo móbil <strong>Xestión de gastos</strong>. Para implementar KB 4019015, o administrador do sistema debe seguir estes pasos.
<ol>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Descargar actualizacións de Lifecycle Services</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Instale a corrección de metadatos</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Cree un paquete despregable</a> que contén os modelos <strong>ApplicationSuite</strong> e <strong>ExpenseMobile</strong> e logo cargue o paquete despregable a LCS.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Aplique o paquete despregable</a>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Publique a área de traballo móbil <strong>Xestión de gastos</strong>.</td>
<td>Administrador do sistema</td>
<td>Consulte <a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Publicar unha área de traballo móbil</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-dynamics-365-unified-ops-mobile-app"></a>Descargue e instale a aplicación móbil Dynamics 365 Unified Ops
Descargue e instale a aplicación móbil Dynamics 365 Unified Ops:

- [Para teléfonos Android](https://go.microsoft.com/fwlink/?linkid=850662)
- [Para iPhones](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Inicie sesión na aplicación móbil.
1. Inicie a aplicación no seu dispositivo móbil.
2. Introduza o seu URL de Dynamics 365.
4. A primeira vez que inicie sesión, solicítaselle o seu nome de usuario e contrasinal. Introduza as súas credenciais.
5. Despois de iniciar sesión, móstranse as áreas de traballo dispoñibles para a súa empresa. Se o administrador do sistema publica unha nova área de traballo máis tarde, terá que actualizar a lista de áreas de traballo móbiles.

## <a name="capture-a-receipt-by-using-the-expense-management-mobile-workspace"></a>Capturar un recibo usando a área de traballo móbil de xestión de gastos

1. No seu dispositivo móbil, abra a área de traballo móbil **Xestión de gastos**.
2. Seleccione **Capturar recibo**.
3. Seleccione **Facer foto** ou **Escoller imaxe**.
4. Siga un destes pasos:

   - Se seleccionou **Facer foto**, siga estes pasos:

      1. Irá á cámara do seu dispositivo móbil para que poida facer unha foto do recibo. 
      2. Cando remate de facer unha foto, seleccione **Aceptar** para aceptar a foto.
      3. Opcional: Introduza un nome para a foto e introduza calquera nota.

    - Se seleccionou **Escoller imaxe**, siga estes pasos:

        1. Seleccione unha imaxe da lista.
        2. Opcional: Introduza un nome para a imaxe e introduza calquera nota.

5. Seleccione **Feito**.

## <a name="quickly-enter-expenses-by-using-the-expense-management-mobile-workspace"></a>Introduza rapidamente os gastos usando a área de traballo móbil de xestión de gastos

1. No seu dispositivo móbil, abra a área de traballo móbil **Xestión de gastos**.
2. Seleccione **Entrada rápida de gasto**.
3. Seleccione a categoría do gasto. Verá unha lista das categorías de gasto cargadas na súa aplicación para o seu uso sen conexión. Por defecto, cárganse 50 elementos, pero un programador pode cambiar este número. Para obter máis información, os programadores deben consultar [Plataforma móbil](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Se a súa categoría non está na lista, seleccione **Buscar** para facer unha busca en liña. Busque por categoría de gasto ou cambie á busca por tipo de gasto.
4. Introduza a data de transacción do gasto.
5. Opcional: Introduza o comerciante para o gasto.
6. Introduza o importe do gasto.
7. Seleccione a moeda do gasto. Verá unha lista dos códigos de moedas cargados na súa aplicación para o seu uso sen conexión. Por defecto, cárganse 400 moedas, pero un programador pode cambiar este número. Para obter máis información, os programadores deben consultar [Plataforma móbil](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Se a súa moeda non está na lista, seleccione **Buscar** para facer unha busca en liña. Busque por moeda ou cambie á busca por nome.
8. Seleccione **Facer foto** ou **Escoller imaxe**.
9. Siga un destes pasos:

    - Se seleccionou **Facer foto**, irá á cámara do seu dispositivo móbil para que poida facer unha foto do recibo. Cando remate de facer unha foto, seleccione **Aceptar** para aceptar a foto.
    - Se seleccionou **Escoller imaxe**, seleccione unha imaxe da lista.

10. Seleccione **Feito**.

## <a name="approve-an-expense-report-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Aprobe un informe de gastos mediante a área de traballo móbil de xestión de gastos (se usa a actualización de xullo de 2017)

1. No seu dispositivo móbil, abra a área de traballo móbil **Xestión de gastos**.
2. **Aprobacións de gastos** mostra o número de informes de gastos que se lle atribúen para a súa aprobación. O número actualízase aproximadamente cada 30 minutos. Seleccione **Aprobacións de gastos**.

    Móstrase a lista de informes de gastos que se lle atribúen para a súa aprobación.
    
3. Seleccione un informe de gastos para ver os detalles do gasto.
4. Seleccione un gasto para ver os seus detalles. A información que se mostra para un gasto inclúe o recibo, o convidado e os detalles.
5. De volta na páxina **Informe de gastos**, seleccione aprobar ou rexeitar o informe de gastos.
6. Introduza calquera comentario para a acción de aprobación.
7. Seleccione **Feito**.

## <a name="create-a-new-expense-report-and-submit-it-for-approval-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Crear un novo informe de gastos e envíeo para a súa aprobación mediante a área de traballo móbil de xestión de gastos (se usa a actualización de xullo de 2017)

1. No seu dispositivo móbil, abra a área de traballo móbil **Xestión de gastos**.
2. Seleccione **Entrada de gasto**.
3. Seleccione **Novo informe** ou seleccione un informe de gastos existente na lista.
4. Para novos informes de gastos, introduza a finalidade e calquera información adicional dispoñible. Esta información varía, dependendo da forma na que se configure a xestión de gastos para a súa empresa.
5. Seleccione **Feito**.
6. Para engadir gastos existentes, como transaccións con tarxeta de crédito, ao informe de gastos, seleccione **Anexar**.
7. Seleccione un ou máis gastos da lista.
8. Seleccione **Feito**.
9. Para engadir un novo gasto ao informe de gastos, seleccione **Novo gasto**.
10. Seleccione a categoría do gasto. Verá unha lista das categorías de gasto cargadas na súa aplicación para o seu uso sen conexión. Por defecto, cárganse 50 elementos, pero un programador pode cambiar este número. Para obter máis información, os programadores deben consultar [Plataforma móbil](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Se a súa categoría non está na lista, seleccione **Buscar** para facer unha busca en liña. Busque por categoría de gasto ou cambie á busca por tipo de gasto.
11. Opcional: Introduza o comerciante para o gasto.
12. Introduza a data de transacción do gasto.
13. Introduza o importe do gasto.
14. Seleccione a moeda do gasto. Verá unha lista dos códigos de moedas cargados na súa aplicación para o seu uso sen conexión. Por defecto, cárganse 400 moedas, pero un programador pode cambiar este número. Para obter máis información, os programadores deben consultar [Plataforma móbil](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Se a súa moeda non está na lista, seleccione **Buscar** para facer unha busca en liña. Busque por moeda ou cambie á busca por nome.
15. Seleccione **Feito**.
16. Para engadir máis detalles ao gasto, seleccione **Engadir máis detalles**. Os campos dispoñibles dependen da configuración de xestión de gastos para a súa empresa.
17. Se a política da empresa require un recibo do gasto, seleccione **Recibos** e siga estes pasos:

    1. Seleccione **Capturar recibo** ou **Anexar recibo**.
    2. Siga un destes pasos:

        - Se seleccionou **Capturar recibo**, siga estes pasos:

            1. Seleccione **Facer foto** ou **Escoller imaxe**.
            2. Siga un destes pasos:

                - Se seleccionou **Facer foto**, siga estes pasos:

                    1. Irá á cámara do seu dispositivo móbil para que poida facer unha foto do recibo. Cando remate de facer unha foto, seleccione **Aceptar** para aceptar a foto.
                    2. Opcional: Introduza un nome para a foto e introduza calquera nota.

                - Se seleccionou **Escoller imaxe**, siga estes pasos:

                    1. Seleccione unha imaxe da lista.
                    2. Opcional: Introduza un nome para a imaxe e introduza calquera nota.

            3.  Seleccione **Feito**.

        - Se seleccionou **Anexar recibo**, siga estes pasos:

            1.  Seleccione unha ou máis imaxes da lista.
            2.  Seleccione **Feito**.

    3. Seleccione o botón **Atrás** para volver aos detalles do gasto.

18. Se a política da empresa require convidados para o gasto, seleccione **Convidados** e siga estes pasos:

    1. Seleccione **Convidado**, **Convidados anteriores** ou **Compañeiros de traballo**.
    2. Siga un destes pasos:

        - Se seleccionou **Convidado**, siga estes pasos:

            1. Introduza o nome do convidado.
            2. Opcional: Introduza a organización e/ou o país do convidado.
            3. Opcional: Introduza o cargo do convidado.
            4. Seleccione **Feito**.

        - Se seleccionou **Convidados anteriores**, siga estes pasos:

            1. Seleccione un ou máis convidados anteriores da lista. Verá unha lista de convidados anteriores que engadiu a informes de gastos anteriores que se cargan na súa aplicación para o seu uso sen conexión. Por defecto, cárganse 50 elementos, pero un programador pode cambiar este número. Para obter máis información, os programadores deben consultar [Plataforma móbil](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Se o seu convidado anterior non está na lista, seleccione **Buscar** para facer unha busca en liña. Busque por nome ou cambie á busca por organización, país ou cargo.
            2. Seleccione **Feito**.

        - Se seleccionou **Compañeiros de traballo**, siga estes pasos:

            1. Seleccione un ou máis compañeiros de traballo da lista. Verá unha lista dos compañeiros de traballo cargados na súa aplicación para o seu uso sen conexión. Por defecto, cárganse 50 elementos, pero un programador pode cambiar este número. Para obter máis información, os programadores deben consultar [Plataforma móbil](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Se o seu compañeiro de traballo non está na lista, seleccione **Buscar** para facer unha busca en liña. Busque por nome ou cambie á busca por empresa ou cargo.
            2. Seleccione **Feito**.

    3. Seleccione o botón **Atrás** para volver aos detalles do gasto.

19. Se a política da empresa require que se detalle o gasto, seleccione **Detallar** e siga estes pasos:

    1. Selecciona a primeira data para detallar.
    2. Seleccione **Engadir detalles**.
    3. Seleccione a subcategoría para detallar o gasto. Verá unha lista das subcategorías de gasto cargadas na súa aplicación para o seu uso sen conexión. Por defecto, cárganse 50 elementos, pero un programador pode cambiar este número. Para obter máis información, os programadores deben consultar [Plataforma móbil](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Se a súa subcategoría non está na lista, seleccione **Buscar** para facer unha busca en liña. Busque por nome da subcategoría de gastos.
    4. Introduza o importe da transacción para detallala.
    5. Se é necesario, edite a data da transacción.
    6. Seleccione **Feito**.
    7. Repita os pasos anteriores ata que remate de engadir todos os detalles para a data seleccionada.
    8. Para os días adicionais, pode seleccionar **Copiar ao día seguinte** para copiar os detalles ao día seguinte. Como alternativa, pode seleccionar a data para detallar e despois engadir detalles como fixo na primeira data.
    9. Despois de rematar de detallar o gasto, seleccione o botón **Atrás** para volver aos detalles do gasto.

20. Seleccione o botón **Atrás** para volver á páxina **Informe de gastos**.
21. Repita os pasos anteriores ata que remate de engadir todos os gastos.
22. Seleccione **Enviar**.
23. Introduza calquera comentario para o responsable de aprobacións.
24. Seleccione **Feito**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]