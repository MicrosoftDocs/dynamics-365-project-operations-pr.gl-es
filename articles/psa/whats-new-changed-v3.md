---
title: Novidades ou cambios na versión 3 de Project Service Automation
description: Este tema fornece información sobre as novidades e as modificacións na versión 3 de Project Service Automation.
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 15925cb88cc413f9a23a25e89ddd29668e9171de
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581650"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3"></a>Novidades ou cambios na versión 3 de Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]



Este tema proporciona información sobre os cambios na interface de usuario (IU), funcionalidade e terminoloxía en Project Service Automation entre a versión 2 ou a versión 1 e a versión 3.

## <a name="project-scheduling"></a>Programación de proxecto
A programación do proxecto, que se coñecía como a estrutura de subdivisión do traballo (WBS) en versións anteriores, pasou a denominarse Programación e se accede a ela premendo o separador **Programación**. 

![Programación de proxecto.](media/psa-schedule-01.png)

O programa ten agora unha nova superficie para a interacción que é moderna e accesible. Non obstante, o motor de programación de Project Service Automation subxacente non cambiou. Os botóns de control da fita da grade de programación permiten interactuar coa programación de xeito similar á versión anterior de Project Service Automation. Outros cambios na programación:

- **Gráfico de Gantt** - O gráfico de Gantt xa non está presente. Unha nova visualización de Gannt regresará nunha futura actualización.
- **Cabeceiras de columnas** - Pode ocultar as cabeceiras de columna na grade premendo no indicador de abaixo xunto ao título da columna. 
- **Columnas** - Pode mostrar columnas ocultas premendo **Engadir columna**. 
- **Categoría de transacción** - A busca de **Categoría de transacción** engadiuse á grade de programación e móstrase por defecto. 
 
## <a name="project-templates"></a>Modelos de proxecto
Realizáronse os seguintes cambios na funcionalidade do modelo de proxecto.

### <a name="create-a-project-template"></a>Crear un modelo de proxecto 
Pode crear un modelo de proxecto na versión 3 similar á versións anteriores de Project Service Automation. O modelo pode conter só unha programación e a programación pode incluír tarefas, pero non son necesarias. Se a programación ten atribucións, só poden ser para recursos xenéricos. Pode xerar requisitos de recursos para recursos xenéricos, pero non se poden reservar con recursos reais no modelo. Non pode reservar un recurso real a un equipo nun modelo. 

### <a name="create-a-template-from-an-existing-template"></a>Crear un modelo a partir doutro xa existente
Cando crea un novo modelo de proxecto a partir dun modelo existente na versión 3 de Project Service Automation, ocorre o seguinte: 

- A programación do proxecto fonte cópiase no modelo. 
- Os recursos xenéricos cópianse no equipo e cópianse tamén as atribucións de recursos xenéricos. Non se copian os requisitos para os recursos xenéricos. 

### <a name="create-a-template-from-an-existing-project"></a>Crear un modelo a partir dun proxecto existente
Cando crea un novo modelo de proxecto a partir dun proxecto existente na versión 3 de PSA, ocorre o seguinte: 

- A programación do proxecto fonte cópiase no modelo. 
- Os recursos xenéricos cópianse no equipo e consérvanse as atribucións de recursos xenéricos. Non se copian os requisitos para os recursos xenéricos.    
- Os recursos nomeados, tanto os atribuídos como os non atribuídos, elimínanse do equipo e son substituídos por recursos xenéricos.
- Se está presente, elimínase a información do cliente. 
- Se está presente, elimínanse as referencias ás ofertas e contratos. 

### <a name="create-a-project-from-a-template"></a>Crear un proxecto a partir dun modelo
Na versión 3 de Project Service Automation, cando crea un novo proxecto a partir dun modelo, ocorre o seguinte:

- A programación, o equipo e as tarefas cópianse ao novo proxecto.   
- A data de inicio é a data de copia ou a data seleccionada polo usuario.   
- Para calquera membro xenérico do equipo con requisitos de recurso no modelo, os requisitos non se copian nin se xeran automaticamente. Terá que xeralos. 

## <a name="copy-a-project"></a>Copiar un proxecto
Na versión 3 de Project Service Automation, cando copia un proxecto, ocorre o seguinte: 

- A data estimada de inicio cópiase, pero pode modificarse.  
- Copíase o calendario do proxecto e as tarefas. 
- Cópianse os recursos xenéricos e as súas atribucións. Non se copian os requisitos de recursos para os recursos xenéricos. Terá que xeralos de novo. 
- Non se copian os recursos reais e as súas atribucións. Pola contra, son substituídos por recursos xenéricos. 
- Os datos reais non se copian no novo proxecto. 

## <a name="move-a-scheduled-project"></a>Mover un proxecto programado
Ao facer avanzar a programación do proxecto existente, sucede o seguinte: 

- As datas das tarefas móvense automaticamente para corresponder co período de movemento. 
- Os recursos xenéricos atribuídos seguen atribuídos.   
- Se se xeran antes de mover o proxecto, os requisitos para o recurso xenérico seguen sendo os mesmos e non se xeran automaticamente. Deberá xeralos de novo para reflectir as novas atribucións debido ao movemento de tarefas. 
- As tarefas sobre dos recursos reais cambian para corresponder co movemento da data da tarefa. As reservas de recursos reais non cambian. Deberá modificar as reservas mediante a vista de reconciliación. 
- Os recursos de equipo con reservas pero sen atribucións non cambian. 
- Os datos reais non se moven. 

## <a name="estimates"></a>Estimacións
As estimacións dividíronse en dous separadores, **Atribucións de recursos** e **Estimacións**. O separador **Atribucións de recursos** contén as estimacións de esforzo e mostra as atribucións de recursos para as tarefas nunha vista de fase de tempo. Pode editar as estimacións en función do que xerou o motor de programación.

![Separador de atribucións de recursos que mostra estimacións e atribucións de recursos para tarefas.](media/resource-assignments-tab-02.png)

O separador **Estimacións** mostra os custos e as cantidades de vendas para atribucións de recursos. Os importes son só de lectura. Os custos e os prezos de vendas derívanse das atribucións dos membros do equipo na programación. Isto significa que se ten unha tarefa sen ningunha atribución, a tarefa mostrarase na sección de non atribuídos. Isto tamén significa que sen **rol**, que é unha dimensión predefinida de prezos, non haberá custo nin vendas estimadas se ten un cliente ou un contrato/oferta asociado ao proxecto. 

![Separador Estimacións que mostra as cantidades de custos e vendas.](media/estimates-tab-03.png)
  
A categoría tamén é compatible coas tarefas na vista de programación. Agrupar por categoría na vista de fases de tempo das estimacións proporcionará unha mellor experiencia, especialmente cando tamén ten estimacións de gastos no seu proxecto. As estimacións de gastos introdúcense mediante unha grade nun separador independente. 

As estimacións de gastos poden introducirse na grade no separador **Estimacións de gastos**. 

![Separador estimacións de gastos que mostra a grade de estimacións de gastos.](media/expense-estimates-tab-04.png)

## <a name="resource-management"></a>Xestión de recursos
Na versión 3 de Project Service Automation, coa nova IU do cliente unificado e os cambios na relación entre reservas e atribucións, a dotación de persoal dun proxecto con recursos xenéricos ou reais cambiou drasticamente respecto á versión 2 e á versión 1. Non obstante, os conceptos de recursos reservables, tanto **reais** como **xenéricos** permanecen igual, do mesmo xeito que os membros do equipo, requisitos, atribucións e reservas.   

![Utilizar o selector de recursos.](media/resource-management-05.png)

### <a name="assign-a-real-bookable-resource"></a>Atribuír un recurso real reservable 
Na versión 3 de Project Service Automation, as reservas e as atribucións de tarefas non están tan estreitamente entrelazadas como nas versións anteriores de Project Service Automation. Pode empregar a grade do equipo para reservar un membro do equipo **real**, de xeito similar ao mercado.

Ao usar o selector de recursos na programación, pode seleccionar o membro do equipo creado na vista do equipo e despois atribuílo a tarefas. Pode seguir atribuíndolle tarefas, incluso superando as súas reservas. Use o separador **Conciliación** para conciliar membros do equipo que teñen diferenzas nas reservas e atribucións.

O selector de recursos mostrará os membros do equipo para o proxecto. Tamén pode usar o selector de recursos para buscar e ver recursos reservables que xa non forman parte do equipo do proxecto. Pode atribuílos a unha tarefa e pasarán a formar parte do equipo do proxecto. Terá que reservalos mediante o separador **Panel de programación** ou **Conciliación**.

### <a name="assign-a-generic-bookable-resource-on-a-task-and-project-team-and-then-fulfill-with-a-real-resource-via-schedule-board"></a>Atribución dun recurso que se pode reservar xenérico nunha tarefa e un equipo de proxecto e posterior cumprimento cun recurso real a través do panel de programación 
Na versión 3 de Project Service Automation, a funcionalidade de xeración de equipo non se usa para recursos xenéricos. No seu lugar, pode crear e atribuír directamente un recurso xenérico a partir da programación escribindo o nome do posto do recurso xenérico na cela de recursos da programación. Tamén pode seleccionar a icona de recurso na cela e, a seguir, mediante o selector de recursos, escribir o nome do recurso xenérico que desexe crear. Con ese procedemento, abrirase un panel de creación rápida que lle permitirá establecer o rol e a unidade organizativa do membro do equipo do recurso xenérico. Despois de crear o recurso, atribúese á tarefa e pode continuar atribuíndo ese recurso xenérico a outras tarefas na programación.    
 
Cando atribúa o recurso a todas as tarefas apropiadas, poderá xerar un requisito de recurso e logo cumprilo reservando directamente co **Panel de programación** ou enviando unha solicitude de recurso. Tamén pode engadir recursos xenéricos directamente á grade de membros do equipo. 

Os recursos xenéricos engádense ao equipo do proxecto sen requisitos de recursos e coas datas de inicio/finalización do proxecto ata que se xeren os requisitos de recursos. Para xerar un requisito, seleccione o recurso xenérico e prema **Xerar**. A ligazón de requisito agora móstrase e as horas requiridas encheranse coas horas atribuídas. Podes premer na ligazón para abrir e actualizar o requisito.
  
Cando a reserva estea completa e un recurso nomeado a cumpra totalmente, o recurso xenérico substituirase polo recurso nomeado e a atribución da programación actualizarase co recurso nomeado. 

Os recursos propostos para os requisitos agora almacénanse nun separador en lugar dunha sección separada.

### <a name="multiple-named-resources-fulfilling-a-generic-resource"></a>Múltiples recursos nomeados que cumpren un recurso xenérico
Cando se cumpre un requisito con varios recursos, o recurso xenérico permanece no equipo e atribúese á tarefa. Os membros do equipo nomeados que están reservados non son atribuídos como parte do posto. O xestor do proxecto pode atribuír o traballo segundo corresponda aos recursos reais.  A vista **Conciliación** proporciona unha subdivisión das reservas de distintos recursos en varias atribucións de tarefa. Isto non se fai de xeito automático porque en escenario máis complicados, como cando hai un paquete de tarefas que conforman o requisito, a intención de como o xestor de proxectos quere atribuír debe ser asumida. Debido a que o sistema non pode entender a intención, as suposicións probablemente serán diferentes do previsto e se produza un resultado incorrecto ou imprevisible. O resultado predicible é que o recurso xenérico permanece atribuído hasta que o xestor de proxectos atribúa recursos deliberadamente coa vista **Conciliación**.

### <a name="reconciliation"></a>Conciliación
O separador **Conciliación** mostra as reservas e todas as atribucións para cada membro do equipo do proxecto. A vista mostra horas en celas que poden representar puntos temporais de meses a días. Esta vista permite aos xestores de proxectos concilien as reservas dos membros do equipo e as súas atribucións para o seu equipo de proxecto. Isto é útil porque as reservas e as tarefas non están ligadas estritamente, o que permite unha maior flexibilidade á hora de planificar un proxecto. 

![Separador Conciliación que mostra as reservas e atribucións para os membros do equipo do proxecto.](media/resource-reconciliation-tab-06.png)

Para cada recurso, a vista selecciona a diferenza entre as reservas dun membro do equipo e un informe das súas atribucións de tarefas e mostra as seguintes dúas diferenzas que poden producirse coas reservas e atribucións nun proxecto: 

- **Escaseza de reservas** - A escaseza de reservas prodúcese cando un recurso ten máis atribucións que reservas. Debido a que non se reservou esta capacidade, un xestor de proxectos pode corrixir esta condición ampliando as reservas do recurso para cubrir o déficit. 
- **Exceso de reservas** - O exceso de reservas prodúcese cando se reservou un recurso para o proxecto pero non foi asignado a tarefas.  Isto podería ser aceptable se, por exemplo, o recurso foi reservado antes da atribución de tarefas. Non obstante, noutros casos, é posible que non estea previsto atribuír o recurso, y o xestor de proxecto debería considerar cancelar as reservas do recurso para permitir que a capacidade se use para outro proxecto. 

Cando teña atribucións de tarefas para un recurso sen reservas (escaseza de reservas), pode seleccionar a escaseza de reservas agregadas e premer en **Estender reserva**. Desde aquí, pode ver a reserva que é necesaria para atallar a escaseza do recurso e a súa dispoñibilidade. 
 
## <a name="time-and-expense"></a>Tempo e gasto
Esta sección ofrece información sobre os cambios no tempo, gasto e aprobación na versión 3 de Project Service Automation. Como parte da solución Dynamics 365 Project Service Automation, actualizouse a funcionalidade **Entrada de tempo** para aproveitar o marco da interface unificada. Isto permite a entrega dunha interface de usuario uniforme e coherente que segue un deseño sensible para una visualización óptima en calquera tamaño de pantalla ou dispositivo. 

### <a name="landing-page"></a>Páxina de destino
A experiencia de entrada de tempo personalizada non extensible quedou desfasada na versión 3. No seu lugar, agora hai unha experiencia de grade nativa extensible e accesible. Pode acceder á funcionalidade de entrada de tempo empregando o mapa do sitio á esquerda. Con ese cambio, xa non poderá introducir o tempo dunha semana á vez. No seu lugar, terá que crear unha entrada de tempo para cada día na grade. Despois de crear algunhas entradas de tempo, os usuarios poden crear entradas de tempo en masa coa función **Copiar** que se explica más adiante neste tema. 

![Páxina de destino da entrada de tempo.](media/time-entry-landing-page-07.png)
 
### <a name="create-new-time-entries"></a>Crear novas entradas de tempo 
Prema en **Novo** na fita para abrir unha páxina de creación rápida para a entrada de tempo onde introducir a duración en minutos, horas ou días. Para facer isto, simplemente comece a escribir h, m ou d xunto coa cantidade.  

![Creación rápida de entrada de tempo.](media/quick-create-time-entry-08.png)

Os campos de busca están apoiados por vistas do sistema. Por exemplo, despois de introducir a información do proxecto, o campo **Tarefa de proxecto** establécese de forma predefinida na vista **As miñas tarefas de proxecto abertas**. Para crear entradas de tempo para tarefas que non están atribuídas ao usuario, prema en **Cambiar vista** na busca e seleccione **Todas as tarefas de proxecto activas**. Una vez que se cree la entrada de tempo e se mostre na grade, poderá editar calquera valor de liña directamente na grade.  

### <a name="bulk-createcopy"></a>Creación/copia en masa 
Despois de crear unhas poucas entradas de tempo, pode usar a funcionalidade de copia para crear entradas de tempo adicionais en masa. Prema en **Copiar** para abrir a caixa de diálogo **Copiar**. En **Desde o período: data de inicio**, estableza o rango de datas desde o que se deben copiar os períodos de tempo. En **Ata o período: data de inicio**, especifique a data para la que se deben crear entradas de tempo. Prema en **Copiar** para copiar as entradas de tempo ao día correspondente da semana indicado en **Ata o período**. Por exemplo, a entrada de tempo do luns da semana pasada copiarase no luns da semana indicada en **Ata o período**. 

![Copiar entradas de tempo en masa.](media/bulk-copy-time-entry-09.png)
 
### <a name="import-data"></a>Importar datos 
Las atribucións e o intercambio seguen o mesmo padrón de interface de usuario, que permite ao usuario especificar o rango de datas desde o momento no que deben importarse as reservas. A seguir, debe elixir explicitamente as reservas que deben copiarse nas entradas de tempo **Borrador**. Na versión 3, xa non pode ver o padrón das entradas de tempo **Suxerido** na grade e o calendario.  

### <a name="change-in-calendar-control"></a>Cambio no control do calendario
Na versión 3, afastámonos do control de calendario personalizado e agora estamos usando o calendario de UC para mostrar as entradas de tempo para a semana. Con este calendario, pode ver o día, a semana e o mes. 

> [!NOTE]
> Unha limitación do calendario é que este control non admite accións en elementos de calendario individuais. Por exemplo, non poderá seleccionar un ou varios elementos do calendario e enviar ou eliminar eses elementos. Ao premer ni elemento do calendario, abrirase a páxina da entidade **Entrada de tempo** para accións adicionais. 

### <a name="extensibility"></a>Extensibilidade
**Captura de datos en campos personalizados só en entidades de entrada de tempo e gastos**: a entrada de tempo utiliza unha grade editable, unha grade de só lectura e controis de calendario desde a plataforma. Todos estes controis son nativos e, polo tanto, admitirán personalizacións. Na versión 3 de Project Service Automation, pode engadir campos personalizados adicionais, configurar campos de busca e facer copia de seguridade con vistas personalizadas. Tamén pode configurar unha lóxica de negocio personalizada baseada nos valores seleccionados en campos personalizados.  

**Captura de datos en campos personalizados na entrada de tempo y gastos e propagación a través de entidades que admiten o fluxo de envío e aprobación**: o procesamento típico das entradas de tempo móstrase no seguinte diagrama.

![Proceso de fluxo de entrada de tempo.](media/process-time-entries-10.png)

Se os requisitos de negocio estipulan que as entidades de tempo e gasto deben capturar dimensións de prezos personalizadas e propagar os valores establecidos por un recurso de tempo e entrada na dimensión de prezos personalizada a través de todas as entidades no gráfico anterior, consulte [Configuración de campos personalizados como dimensións de prezos](set-up-pricing-dimensions.md).

Para admitir os requisitos de negocio nos que as entidades de tempo y gastos deben capturar dimensións personalizadas que non sexan de prezos e propagar os valores, pode usar a configuración de dimensións de prezos e expresar as dimensións personalizadas como dimensións de prezos sen custo nin taxa de facturación. Outro escenario sería engadir un campo personalizado a cada unha das entidades, empregando o mesmo nome de campo en todas as entidades. Pódense crear complementos personalizados para relacionar rexistros nas entidades que participan no fluxo de envío/aprobación mediante a orixe da transacción e as entidades de conexión de transaccións.  

### <a name="delegate-time-and-expense-entry"></a>Delegar entrada de tempo ou gastos
A plataforma Common Data Service non admite que un usuario se faga pasar por outro, o que significa que na versión 3 de Project Service Automation non se admite a entrada delegada de tempo e gastos. Non obstante, os socios e clientes aproveitaron unha solución para permitir as experiencias de entrada de tempo delegadas na versión 3. Isto é só unha solución alternativa e incompleta, polo que é importante comprender as limitacións. Ademais, só debe usar este enfoque se as limitacións son aceptables . 

> [!IMPORTANT]
> O socio/cliente debe considerar esta información só como guía suxerida para a implantación personalizada. O equipo de produto non ofrecerá asistencia formal para esta funcionalidade a través de ningunha das nosas canles de asistencia.

### <a name="customization-details"></a>Detalles de personalización 
A personalización permítelle engadir **Recurso reservable** ás experiencias de creación e edición, o que permitirá que un usuario actúe como delegado ao cambiar o campo **Reserva de recursos** a outro usuario para o que se deben rexistrar as entradas de tempo e gastos. Os seguintes pasos tratan sobre a delegación de entrada de tempo. Aplícase a mesma información á delegación de entrada de gastos. 
 
1.  Asegúrese de que o usuario delegado teña acceso de seguridade global a proxectos e tarefas de proxecto. 
1.  Debido a que **Recurso reservable**, que é un campo da entidade **Entrada de tempo**, non se expón na páxina **Creación rápida**, terá que engadilo.

    ou

    Cree unha vista personalizada, que inclúa a columna **Recurso reservable**, para ver só as entradas de tempo creadas para o recurso. Publique as personalizacións no deseñador do módulo da aplicación para que esta vista apareza en **Selector de vistas** na páxina **Entradas de tempo**. Existen dous complementos que xestionan a configuración do administrador para as entradas de tempo que non son do proxecto:

    - PreValidateTimeEntryCreate
    - PreValidateTimeEntryUpdate
 
1. Cree un novo complemento para sobrescribir o campo **Xestor** no xestor do usuario atribuído no campo **Recurso reservable**. Use a mesma **Fase de execución** que o complemento fóra de banda (OOB) (prevalidación) e use unha **orde de execución** superior aos complementos OOB (maior que 1). Isto garantirá que o complemento personalizado se execute despois dos complementos OOB.  
 
### <a name="end-user-experience"></a>Experiencia de usuario final
1.  Cando cree unha entrada de tempo na páxina de creación rápida, introduza os detalles do Proxecto e a tarefa de Proxecto e logo elixa o usuario no campo **Recurso reservable** para quen deben rexistrarse entradas de tempo. 
2.  Por defecto, este campo está predefinido para o usuario conectado. Non obstante, posto que o usuario anulou este campo, agora se crea unha entrada de tempo para o **Recurso reservable** elixido.
3.  Cando envíe as entradas de tempo que creou para estes rexistros, as entradas poranse en fila para o responsable de aprobacións do proxecto como se esperaba. 
4.  Cando recupere as entradas de tempo creadas para o outro usuario, as entradas de tempo volverán a un estado de **Borrador** co campo **Recurso reservable** establecido para o outro usuario. 
5.  Opcionalmente, pode cambiar á vista personalizada para filtrar as entradas de tempo creadas para o outro usuario. 
 
### <a name="limitations"></a>Limitacións
A funcionalidade **Copiar** e **Importar** só funciona no contexto do usuario que iniciou sesión. Isto significa que non é posible copiar ou importar entradas de tempo creadas para o usuario que iniciou sesión como recurso reservable.

As entradas de tempo que non son para un proxecto dirixiranse para a súa aprobación ao xestor do recurso reservable solo se se completa o paso 4 na sección **Detalles da personalización** anterior. En caso contrario, as entradas de tempo que non sexan do proxecto para o outro usuario dirixiranse incorrectamente ao xestor do usuario que iniciou sesión. 

### <a name="other-changes"></a>Outros cambios 
Eliminouse a funcionalidade **Reservas e tarefas**. 

## <a name="multidimensional-pricing"></a>Prezos multidimensionais
Para maximizar a flexibilidade e cumprir cos diferentes requisitos de negocio, a versión 3 de Project Service Automation admite a aplicación discreta de conxuntos de dimensións de prezos a taxas de custo e facturación. Os valores de dimensión poden establecerse como predefinidos e, a seguir, propagarse a través do proceso de cálculo de custos e prezos desde a creación de perfís de recursos ata a entrada de tempo aos datos reais do proxecto. A configuración e modificación ou extensión específica do cliente aproveita a infraestrutura de personalización estándar.

Project Service Automation envíase cun conxunto predeterminado de dimensións de prezos e roles e unidades de recursos e permite a configuración de prezos e custos para cada combinación de roles e unidades organizativas.

Para os clientes de Project Service Automation que desexan continuar utilizando estes campos listos para usar como dimensións de prezos na versión 3, no haberá ningún cambio observable. Pode seguir usando Project Service Automation como sempre. Non obstante, se necesita fixar o prezo ou o custo dos seus recursos utilizando outros atributos adicionais, a versión 3 permítelle engadir as súas propias dimensións de prezos personalizadas a Project Service Automation. A extensión das dimensións de prezos personalizadas é unha experiencia de configuración complicada. 

## <a name="quotes-and-contracts"></a>Ofertas e contratos
Na versión 3 de Project Service Automation, os aspectos de configuración e xestión de ofertas e contratos cambiaron. As seguintes seccións proporcionan información máis detallada.

### <a name="set-up-chargeability-options"></a>Configuración de opcións de imputabilidade
Nas versións 1 e 2, a configuración de imputabilidade para roles e categorías para ofertas e contratos específicos realizouse mediante a vista **Imputabilidade** que estaba na navegación superior dunha liña de oferta ou unha liña de contrato. Aquí tamén se podían configurar os prezos para eses roles e categorías de gastos.

A partir da versión 3, a configuración das opcións de imputabilidade por rol e categoría de gastos realizarase a nivel de liña de oferta ou contrato. A configuración de prezos é independente da configuración de imputabilidade. Poderá atopar **Roles imputables** e **Categorías de gastos imputables** como separadores nas páxinas **Liña de oferta** e **Liña de contrato** sen ter que utilizar a barra de navegación superior.

![Roles imputables.](media/chargeable-12.png)
 
A configuración de Roles imputables e Categorías imputables tamén aproveita o control de grade editable listo para usar. Para cada función e categoría, as opcións admitidas para o tipo de facturación durante a fase de oferta e contrato non cambiaron desde as versións anteriores como **Imputable** e **Non imputable**. **Gratis** non é un tipo admitido durante a fase de oferta ou contrato. **Gratis** só se admite durante a aprobación de tempo ou gastos.  
 
### <a name="create-and-edit-custom-pricing-for-a-project-service-automation-quote-and-project-contract"></a>Creación e edición de prezos personalizados para unha oferta de Project Service Automation e un contrato de proxecto
Nas versións 1 e 2, o uso da lista de prezos personalizada para ofertas e contratos específicos realizouse mediante **Editar prezos** na vista **Imputabilidade**. A vista **Imputabilidade** atópase na navegación superior dunha liña de oferta ou unha liña de contrato. Aquí tamén era onde podía configurar opcións de imputabilidade para roles ou categorías de gastos.

A partir da versión 3, a creación e o uso dunha lista de prezos de proxecto personalizada nunha oferta e un contrato de proxecto de Project Service Automation separouse da configuración de imputabilidade. Os contratos de oferta de Project Service Automation e proxecto de Project Service Automation teñen un novo separador **Listas de prezos do proxecto**. Este separador mostra unha vista asociada de todas as listas de prezos do proxecto que se anexan á oferta ou ao contrato do proxecto de Project Service Automation. Para crear unha lista de prezos personalizada a partir dunha lista de prezos existente que xa está asociada á oferta ou contrato do proxecto, prema en **Crear prezos personalizados**. Isto creará unha copia de todas as listas de prezos asociadas e as anexará á oferta ou ao contrato. Agora pode abrir a lista de prezos e editar o prezo da categoría de gastos ou roles para que eses cambios de prezos só se apliquen a esta oferta ou contrato. 
  
O seguinte gráfico é de antes de que se creasen listas de prezos personalizadas.

![Antes das listas de prezos personalizadas.](media/before-custom-price-lists-13.png)

O seguinte gráfico é de despois de que se creasen listas de prezos personalizadas.

![Despois listas de prezos personalizadas.](media/after-custom-price-lists-14.png)

> [!NOTE]
> Pode producirse un pequeno retraso entre cando preme en **Crear prezos personalizados** e cando se crea a lista de prezos personalizada. Recomendamos actualizar a grade en lugar de premer varias veces. Creouse unha lista de prezos personalizada se o nome da lista de prezos asociada ten o nome de oferta ou o nome do contrato do proxecto anexo.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
