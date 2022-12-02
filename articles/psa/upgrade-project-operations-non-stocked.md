---
title: Actualizar de Project Service Automation a Project Operations
description: Este artigo ofrece unha visión xeral do proceso desde para actualizar de Microsoft Dynamics 365 Project Service Automation a Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/11/2022
ms.topic: article
ms.author: ruhercul
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
ms.openlocfilehash: ac2435c99f3aa9b2a6cdb08d7ce5f6628e7f6ac4
ms.sourcegitcommit: bea5f9b4066277344add1da3a1567ed56a0cfd31
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 11/02/2022
ms.locfileid: "9736664"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Actualizar de Project Service Automation a Project Operations

Estamos encantados de anunciar a segunda das tres fases para a actualización de Microsoft Dynamics 365 Project Service Automation a Microsoft Dynamics 365 Project Operations. Este artigo ofrece unha visión xeral para os clientes que se están embarcando nesta emocionante viaxe. 

O programa de entrega de actualizacións dividirase en tres fases.

| Entrega de actualizacións | Fase 1 (xaneiro de 2022) | Fase 2 (novembro de 2022) | Fase 3 (onda de abril de 2023)  |
|------------------|------------------------|---------------------------|---------------------------|
| Non depende da estrutura de subdivisión do traballo (WBS) dos proxectos | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Unha WBS está incluída nos límites actualmente admitidos de Project Operations | | :heavy_check_mark: | :heavy_check_mark: |
| Unha WBS fóra dos límites actualmente admitidos de Project Operations, incluído o soporte para Project Desktop Client | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>Funcionalidades do proceso de actualización 

Como parte do proceso de actualización, engadimos rexistros de actualizacións ao mapa do sitio para que os administradores poidan diagnosticar erros máis facilmente. Ademais da nova interface, engadiranse novas regras de validación para garantir a integridade dos datos despois dunha actualización. As seguintes validacións engadiranse ao proceso de actualización.

| Validacións | Fase 1 (xaneiro de 2022) | Fase 2 (novembro de 2022) | Fase 3  |
|-------------|------------------------|---------------------------|---------------------------|
| A WBS validarase contra violacións comúns da integridade dos datos (por exemplo, asignacións de recursos que están asociadas coa mesma tarefa principal pero que teñen proxectos principais). | | :heavy_check_mark: | :heavy_check_mark: |
| A WBS validarase contra os [límites coñecidos de Project for the Web](/project-for-the-web/project-for-the-web-limits-and-boundaries). | | :heavy_check_mark: | :heavy_check_mark: |
| A WBS validarase contra os límites coñecidos de Project Desktop Client. | |  | :heavy_check_mark: |
| Os recursos reservables e os calendarios de proxectos avaliaranse en función das excepcións comúns ás regras de calendario incompatibles. | | :heavy_check_mark: | :heavy_check_mark: |

Na fase 2, os clientes que se actualicen a Project Operations terán os seus proxectos existentes actualizados a unha experiencia de só lectura para a planificación do proxecto. Nesta experiencia de só lectura, a WBS completa estará visible na grade de seguimento. Para editar a WBS, os xestores de proxectos poden seleccionar [**Converter**](/PSA-Upgrade-Project-Conversion.md) na páxina principal do proxecto. A seguir, un proceso en segundo plano actualiza o proxecto para que admita a nova experiencia de programación de proxectos de Project for the Web. Esta fase é axeitada para clientes que teñan proxectos que encaixan dentro dos [límites coñecidos de Project for the Web](/project-for-the-web/project-for-the-web-limits-and-boundaries).

Na fase 3 engadirase soporte para Project Desktop Client, en beneficio dos clientes que queiran seguir editando os seus proxectos desde esa aplicación. Non obstante, se os proxectos existentes se converten á nova experiencia Project for the Web, o acceso ao complemento desactivarase para cada proxecto convertido.

## <a name="prerequisites"></a>Requisitos previos

Para ser elixible para a actualización da Fase 1, debes cumprir os seguintes criterios:

- O ambiente de destino non debe conter ningún rexistro na entidade **msdyn_projecttask**.
- As licenzas válidas de Project Operations deben asignarse a todos os usuarios activos. 
- Debe validar o proceso de actualización en polo menos un ambiente que non sexa de produción que conteña un conxunto de datos representativo que estea aliñado co seu ambiente de produción.
- O ambiente de destino debe actualizarse á versión 37 de actualización de Project Service Automation (V3.10.58.120) ou posterior.

Para ser elixible para a actualización da Fase 2, debe cumprir os seguintes criterios:

- As licenzas válidas de Project Operations deben asignarse a todos os usuarios activos. 
- Debe validar o proceso de actualización en polo menos un ambiente que non sexa de produción que conteña un conxunto de datos representativo que estea aliñado co seu ambiente de produción.
- O ambiente de destino debe actualizarse á versión 37 de actualización de Project Service Automation (V3.10.58.120) ou posterior.
- Os ambientes que conteñen tarefas (msdyn_projecttask) só son compatibles se o número total de tarefas por proxecto é 500 ou menos.

Os requisitos previos para a Fase 3 actualizaranse a medida que se aproxime a data de dispoñibilidade xeral.

## <a name="licensing"></a>Obtención de licenzas

Se ten licenzas activas para Project Service Automation, pode instalar e usar Project Operations, que inclúe todas as capacidades de Project Service Automation e moito máis. Deste xeito, pode probar as capacidades de Project Operations mentres continúa usando Project Service Automation na produción. Despois de que caduquen as licenzas de Project Service Automation, terá que pasar a Project Operations. Cando planifique esta transición, debe ter en conta o feito de que a licenza de Project Operations non inclúe unha licenza de Project Service Automation. Os clientes que teñan escenarios nos que implementaron Project Service Automation e necesitan seguir utilizando ou aumentando as súas licenzas para PSA mentres planean pasar a Project Operations, poden solicitar licenzas temporais de PSA en función das licenzas adquiridas por Project Operations. Emitirase unha licenza de Project Service Automation para unha licenza de Project Operations. Pódense solicitar licenzas de PSA temporais mediante esta ligazón: aka.ms/ineedpsa

## <a name="testing-and-refactoring-customizations"></a>Proba e refactorización de personalizacións

Como punto de partida, importe todas as personalizacións nun ambiente limpo de Project Operations (Lite) para confirmar que a importación se realiza correctamente e que as operacións comerciais se comportan como se esperaba.

Aquí ten algunhas cousas que debe ter en conta:

- A importación pode fallar porque faltan dependencias. Noutras palabras, as personalizacións fan referencia a campos ou outros compoñentes que foron eliminados en Project Operations. Neste caso, elimine estas dependencias do ambiente de desenvolvemento.
- Se as súas solucións non xestionadas e xestionadas inclúen compoñentes que non están personalizados, elimine eses compoñentes da solución. Por exemplo, cando personaliza a entidade **Proxecto**, engada só a cabeceira da entidade á súa solución. Non engada todos os campos. Se engadiu previamente todos os subcompoñentes, quizais teña que crear manualmente unha nova solución e engadirlle compoñentes relevantes.
- É posible que os formularios e as vistas non aparezan como se esperaba. Baixo algunhas circunstancias, se personalizou algún dos formularios ou vistas listados, as personalizacións poden impedir que as novas actualizacións en Project Operations teñan efecto. Para identificar estes problemas, recomendámoslle que faga unha revisión en paralelo dunha instalación limpa de Project Operations e dunha instalación de Project Operations que inclúa as súas personalizacións. Compare os formularios máis usados na súa empresa para confirmar que a súa versión do formulario aínda ten sentido e que non falta nada da versión limpa do formulario. Faga o mesmo tipo de revisión en paralelo para todas as vistas que personalizou.
- A lóxica empresarial pode fallar no tempo de execución. Dado que as referencias aos campos dos seus complementos non se validan no momento da importación, a lóxica empresarial pode fallar debido a referencias a campos que xa non existen e pode recibir unha mensaxe de erro que se asemella ao seguinte exemplo: "'Project' entity doesn't contain attribute with Name = 'msdyn_plannedhours' and NameMapping = 'Logical'." Neste caso, modifique as súas personalizacións para que utilicen os novos campos. Se usa clases de proxy xeradas automaticamente e referencias de tipo forte na lóxica do complemento, considere rexenerar eses proxies desde unha instalación limpa. Deste xeito, pode identificar facilmente todos os lugares onde os seus complementos dependen de campos obsoletos.

Despois de actualizar as súas personalizacións para importar correctamente Project Operations, pase aos seguintes pasos.

## <a name="end-to-end-testing-in-development-environments"></a>Probas de extremo a extremo en ambientes de desenvolvemento

### <a name="initiate-upgrade"></a>Iniciar actualización 

1. No centro de administración de Power Platform, busque e seleccione o seu ambiente. A seguir, nas aplicacións, busque e seleccione **Dynamics 365 Project Operations**.
2. Seleccione **Instalar** para iniciar a actualización. O centro de administración de Power Platform presentará esta instalación como unha nova instalación. Non obstante, detectarase a presenza dunha versión anterior de Project Service Automation e actualizarase a instalación existente.

    Despois de completar a actualización, o ambiente debería mostrar que Project Operations está instalado e que Project Service Automation non está instalado.

    En función da cantidade de datos do ambiente, a actualización podería tardar varias horas. O equipo principal que xestiona a actualización debe planificar en consecuencia e executar a actualización durante as horas non laborables. Nalgúns casos, se o volume de datos é grande, a actualización debería executarse durante a fin de semana. A decisión sobre a programación debe basearse nos resultados das probas en ambientes inferiores.

3. Actualice as solucións personalizadas segundo corresponda. Neste punto, implemente todos os cambios que fixo nas súas personalizacións na sección [Proba e refactorización de personalizacións](#testing-and-refactoring-customizations) deste artigo.
4. Vaia a **make.powerapps.com**, seleccione o seu ambiente no menú despregable na parte superior dereita do portal, seleccione **Solucións** no menú da esquerda, seleccione a solución **Compoñentes obsoletos de Project Operations** e **Desinstalar**.

    Esta solución é unha solución temporal que contén o modelo de datos existente e os compoñentes que están presentes durante a actualización. Ao eliminar esta solución, elimina todos os campos e compoñentes que xa non se usan. Deste xeito, axuda a simplificar a interface e facilita a integración e a extensión.
    
### <a name="upgrade-to-project-operations-lite"></a>Actualizar a Project Operations Lite

Os seguintes pasos describen o proceso de actualización e o rexistro de erros asociado:

1. **Verificación da versión de PSA:** Para instalar Project Operations, debe ter V3.10.58.120 ou superior.
1. **Validación previa:** Cando un administrador inicia unha actualización, o sistema executa unha operación de validación previa en cada entidade que é o núcleo da solución Project Operations. Este paso verifica que todas as referencias de entidades sexan válidas e garante que os datos relacionados coa WBS estean dentro dos límites publicados de Project for the Web.
1. **Actualización de metadatos:** Despois da validación previa con éxito, o sistema inicia cambios no esquema e crea unha solución de compoñentes obsoletos. Pode eliminar esta solución obsoleta despois de completar toda a refactorización necesaria das personalizacións. Este paso é a parte máis longa do proceso de actualización e pode tardar ata catro horas en completarse.
1. **Actualización de datos:** Despois de que se completen todos os cambios de esquema necesarios no paso de actualización de metadatos, os seus datos migráranse ao novo esquema e realízanse os cálculos predeterminados e os novos cálculos necesarios.
1. **Actualización do motor de programación do proxecto:** Despois da actualización de datos con éxito, o separador **Programación** da páxina principal etiquetárase como **Tarefas**. Cando un usuario selecciona este separador despois da actualización, diríxeselle á grade de seguimento para ver unha versión de só lectura da WBS. Para editar a WBS, debe iniciar o [proceso de conversión de programación](/PSA-Upgrade-Project-Conversion.md). Todos os proxectos sen WBS preexistente poden usar a nova experiencia de programación directamente, sen conversión.
 
### <a name="validate-common-scenarios"></a>Validar escenarios comúns

Cando valide as súas personalizacións específicas, recomendámoslle que revise tamén os procesos comerciais admitidos nas aplicacións. Estes procesos de negocio inclúen, entre outras cousas, a creación de entidades de vendas, como cotizacións e contratos, e a creación de proxectos que inclúan WBS e aprobación de datos reais.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Cambios importantes entre Project Service Automation e Project Operations

Esta sección ofrece un resumo dos principais cambios que pode esperar entre Project Service Automation e Project Operations.

### <a name="project-planning"></a>Planificación de proxectos

As capacidades de planificación de proxectos en Project Operations xa non dependen dunha combinación de lóxica do lado cliente e lóxica do servidor. No seu lugar, Project Operations usa Project for the Web como o seu principal motor de programación. Este cambio nas capacidades de programación permite varias funcións novas, como vistas de Panel e Gantt, planificación baseada en recursos, [elementos da lista de verificación de tarefas](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c) e modos de programación de proxectos. As novas capacidades de programación tamén están soportadas por un rico conxunto de novas [interfaces de programación de aplicacións (API)](../project-management/schedule-api-preview.md). Estas API están destinadas a garantir que ningunha operación programática para crear, actualizar ou eliminar unha entidade na WBS corrompe os campos calculados na programación.

### <a name="billing-and-pricing"></a>Facturación e prezos

Como parte dos investimentos continuos en Project Operations, hai dispoñibles varias capacidades novas en Facturación e prezos. Aquí van algúns exemplos:

- [Rexistro do uso do material en proxectos e tarefas de proxecto](../material/material-usage-log.md)
- [Xestión de subcontratos](../pro/subcontracting/managing-subcontracts-overview.md)
- [Contratos baseados en adiantos e retencións](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Estado de non superar o contrato e validacións](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Facturación baseada en tarefas

### <a name="resource-management"></a>Xestión de recursos

Project Operations ofrece soporte opcional para o asistente de programación Universal Resource Scheduling (URS). Esta nova experiencia será obrigatoria na onda de abril de 2023.

## <a name="frequently-asked-questions"></a>Preguntas máis frecuentes

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>Que tipos de implementación se admiten actualmente para a actualización?

| Código fonte                                                 | Destino                                                    | Progresión                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Project Service Automation                             | Despregamento de Project Operations Lite                        | Compatible               |
| Xestión e contabilidade de proxectos de Dynamics 365 Finance | Despregamento de Project Operations Lite                        | Actualmente non se admite |
| Xestión e contabilidade de proxectos de Finance              | Project Operations para escenarios baseados en recursos ou sen existencias     | Actualmente non se admite |
| Project Service Automation 3.x                         | Project Operations para escenarios baseados en recursos ou sen existencias     | Actualmente non se admite |
| Project for the Web (ambiente dedicado)            | Despregamento de Project Operations Lite                        | Actualmente non se admite |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>Como podo instalar Project Operations antes de que a ferramenta de actualización estea dispoñible?

Hai dúas opcións para instalar Project Operations antes de que a ferramenta de actualización estea dispoñible:

- Fornecer un novo ambiente.
- Despregar Project Operations por separado en calquera organización de vendas onde Project Service Automation non estea presente.

Se Project Service Automation está instalado nunha organización, pero non se utilizou, pódese desinstalar. Despois de eliminar completamente Project Service Automation, Project Operations pódese instalar na mesma organización.
