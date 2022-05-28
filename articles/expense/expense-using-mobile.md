---
title: Aplicación de gastos para móbiles
description: Este tema ofrece información sobre a área de traballo móbil de xestión de gastos.
author: suvaidya
ms.date: 11/15/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 14bd76df5f058d2af9f77990471a0a173fe8c15d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588918"
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

## <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Requisitos previos se usas Dynamics 365 Finance

Se se despregou Finanzas para a súa organización, o administrador do sistema debe publicar a área de traballo móbil **Xestión de gastos**. 

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

## <a name="approve-an-expense-report-by-using-the-expense-management-mobile-workspace"></a>Aproba un informe de gastos mediante o espazo de traballo móbil Xestión de gastos

1. No seu dispositivo móbil, abra a área de traballo móbil **Xestión de gastos**.
2. **Aprobacións de gastos** mostra o número de informes de gastos que se lle atribúen para a súa aprobación. O número actualízase aproximadamente cada 30 minutos. Seleccione **Aprobacións de gastos**.

    Móstrase a lista de informes de gastos que se lle atribúen para a súa aprobación.

3. Seleccione un informe de gastos para ver os detalles do gasto.
4. Seleccione un gasto para ver os seus detalles. A información que se mostra para un gasto inclúe o recibo, o convidado e os detalles.
5. De volta na páxina **Informe de gastos**, seleccione aprobar ou rexeitar o informe de gastos.
6. Introduza calquera comentario para a acción de aprobación.
7. Seleccione **Feito**.

## <a name="create-a-new-expense-report-and-submit-it-for-approval-by-using-the-expense-management-mobile-workspace"></a>Crea un novo informe de gastos e envíao para a súa aprobación mediante o espazo de traballo móbil Xestión de gastos

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

            3. Seleccione **Feito**.

        - Se seleccionou **Anexar recibo**, siga estes pasos:

            1. Seleccione unha ou máis imaxes da lista.
            2. Seleccione **Feito**.

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

## <a name="frequently-asked-questions"></a>Preguntas máis frecuentes

### <a name="why-doesnt-the-expense-mobile-app-enter-the-payment-method-by-default"></a>Por que a aplicación móbil Expense non introduce o método de pago de forma predeterminada?

As organizacións poden personalizar **Método de pago predeterminado** configuración para cada categoría de gasto tal como se crea. Ademais, cando configure os métodos de pago, pode configurar o **Método de pago predeterminado** campo a **Só importar**.

Cando **Só importar** está habilitado para un método de pago, o método de pago non se introduce de forma predeterminada. Estará en branco nas categorías de gastos nas que estea configurado este método de pago. Este comportamento é consistente tanto na experiencia web como na experiencia móbil.
    
Cando **Só importar** non está habilitado para un método de pago, o valor definido introdúcese de forma predeterminada para as categorías de gastos nas que este método de pago está configurado. Non obstante, hai un problema coñecido polo que o valor predeterminado non se introduce na aplicación móbil Expense. Para solucionar este problema, selecciona manualmente un método de pago antes de gardar o informe de gastos. 

### <a name="why-cant-i-add-or-edit-financial-dimensions-in-the-expense-mobile-app"></a>Por que non podo engadir ou editar dimensións financeiras na aplicación móbil Expense?

Non se admite a entrada de dimensións e distribucións. Para evitar esta limitación, pode configurar estes campos de forma predeterminada na aplicación móbil configurando as dimensións financeiras predeterminadas por proxecto ou empregado.

### <a name="why-do-i-sometimes-see-a-synchronization-error-in-the-expense-mobile-app"></a>Por que ás veces vexo un erro de sincronización na aplicación móbil Expense?

Se as liñas de gasto non cumpren os requisitos da política e o usuario envía o informe de gastos sen abordar a advertencia da política, os datos móbiles non se sincronizan co servidor e prodúcese un erro de sincronización. Todos os informes de gastos que se envíen despois de que se produza un fallo de sincronización permanecerán nun estado de erro e provocarán máis fallos de sincronización. A única forma de solucionar esta situación é eliminar manualmente as notificacións de sincronización. Solucionouse este problema interrompendo o envío de informes de gastos cando non se abordaron os avisos de políticas, para evitar os erros de sincronización.

### <a name="why-isnt-project-and-category-validation-correctly-reflected-in-the-expense-mobile-app"></a>Por que a validación de proxectos e categorías non se reflicte correctamente na aplicación móbil Expense?

Actualmente non se admite esta validación. Non obstante, pode engadirse soporte no futuro. 

### <a name="what-document-types-are-supported-in-the-expense-mobile-app"></a>Que tipos de documentos son compatibles coa aplicación móbil Expense?

A aplicación móbil Expense só admite imaxes. Actualmente non admite PDF nin outros documentos.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
