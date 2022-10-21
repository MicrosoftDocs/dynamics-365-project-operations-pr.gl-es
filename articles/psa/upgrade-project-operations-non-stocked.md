---
title: Actualizar de Project Service Automation a Project Operations
description: Este artigo ofrece unha visión xeral do proceso desde o que se actualiza Microsoft Dynamics 365 Project Service Automation a Dynamics 365 Project Operations.
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
ms.openlocfilehash: 2d7b372cac391fab7a81ac6ac5d2ea6d12977b5c
ms.sourcegitcommit: 9de444ae0460c8d15c77d225d0c0ad7f8445d5fc
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/18/2022
ms.locfileid: "9686973"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Actualizar de Project Service Automation a Project Operations

Estamos encantados de anunciar a segunda das tres fases para a actualización Microsoft Dynamics 365 Project Service Automation a Microsoft Dynamics 365 Project Operations. Este artigo ofrece unha visión xeral para os clientes que se están embarcando nesta emocionante viaxe. 

O programa de entrega de actualizacións dividirase en tres fases.

| Actualizar a entrega | Fase 1 (xaneiro de 2022) | Fase 2 (novembro 2022) | Fase 3 (Onda de abril de 2023)  |
|------------------|------------------------|---------------------------|---------------------------|
| Non depende da estrutura de desagregación do traballo (WBS) dos proxectos | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Un WBS dentro dos límites actualmente soportados das operacións do proxecto | | :heavy_check_mark: | :heavy_check_mark: |
| Un WBS fóra dos límites actualmente compatibles de Project Operations, incluíndo soporte para o cliente de escritorio de Project | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>Actualizar as características do proceso 

Como parte do proceso de actualización, engadimos rexistros de actualizacións ao mapa do sitio para que os administradores poidan diagnosticar erros máis facilmente. Ademais da nova interface, engadiranse novas regras de validación para garantir a integridade dos datos despois dunha actualización. As seguintes validacións engadiranse ao proceso de actualización.

| Validacións | Fase 1 (xaneiro de 2022) | Fase 2 (novembro 2022) | Fase 3  |
|-------------|------------------------|---------------------------|---------------------------|
| O WBS validarase contra violacións comúns da integridade dos datos (por exemplo, asignacións de recursos que están asociadas coa mesma tarefa principal pero que teñen proxectos principais). | | :heavy_check_mark: | :heavy_check_mark: |
| O WBS validarase contra o [límites coñecidos de Project for the Web](/project-for-the-web/project-for-the-web-limits-and-boundaries). | | :heavy_check_mark: | :heavy_check_mark: |
| O WBS validarase contra os límites coñecidos do cliente de escritorio do proxecto. | |  | :heavy_check_mark: |
| Os recursos reservables e os calendarios de proxectos avaliaranse en función das excepcións comúns ás regras de calendario incompatibles. | | :heavy_check_mark: | :heavy_check_mark: |

Na fase 2, os clientes que se actualicen a Project Operations terán os seus proxectos existentes actualizados a unha experiencia de só lectura para a planificación do proxecto. Nesta experiencia de só lectura, o WBS completo estará visible na grella de seguimento. Para editar a WBS, os xestores de proxectos poden seleccionar [**Converter**](/PSA-Upgrade-Project-Conversion.md) na páxina principal do proxecto. A continuación, un proceso en segundo plano actualiza o proxecto para que admita a nova experiencia de programación de proxectos de Project for the Web. Esta fase é axeitada para clientes que teñan proxectos que encaixan dentro do [límites coñecidos de Project for the Web](/project-for-the-web/project-for-the-web-limits-and-boundaries).

Na fase 3 engadirase soporte para o cliente de escritorio de Project, en beneficio dos clientes que queiran seguir editando os seus proxectos desde esa aplicación. Non obstante, se os proxectos existentes se converten á nova experiencia Proxecto para a web, o acceso ao complemento desactivarase para cada proxecto convertido.

## <a name="prerequisites"></a>Requisitos previos

Para ser elixible para a actualización da Fase 1, debes cumprir os seguintes criterios:

- O ambiente de destino non debe conter ningún rexistro no **msdyn_projecttask** entidade.
- As licenzas válidas de Project Operations deben asignarse a todos os usuarios activos. 
- Debe validar o proceso de actualización en polo menos un ambiente que non sexa de produción que conteña un conxunto de datos representativo que estea aliñado co seu ambiente de produción.
- O ambiente de destino debe actualizarse á versión 37 de actualización de Project Service Automation (V3.10.58.120) ou posterior.

Para ser elixible para a actualización da Fase 2, debes cumprir os seguintes criterios:

- As licenzas válidas de Project Operations deben asignarse a todos os usuarios activos. 
- Debe validar o proceso de actualización en polo menos un ambiente que non sexa de produción que conteña un conxunto de datos representativo que estea aliñado co seu ambiente de produción.
- O ambiente de destino debe actualizarse á versión 37 de actualización de Project Service Automation (V3.10.58.120) ou posterior.
- Os ambientes que conteñen tarefas (msdyn_projecttask) só son compatibles se o número total de tarefas por proxecto é 500 ou menos.

Os requisitos previos para a Fase 3 actualizaranse a medida que se aproxime a data de dispoñibilidade xeral.

## <a name="licensing"></a>Obtención de licenzas

Se tes licenzas activas para Project Service Automation, podes instalar e usar Project Operations, que inclúe todas as capacidades de Project Service Automation e moito máis. Despois podes probar as capacidades de Project Operations nun ambiente separado mentres continúas usando Project Service Automation na produción. Despois de que caduquen as licenzas de Project Service Automation, terás que pasar a Project Operations. Cando planifiques esta transición, debes ter en conta o feito de que a licenza de Project Operations non inclúe unha licenza de Project Service Automation.

## <a name="testing-and-refactoring-customizations"></a>Proba e refactorización de personalizacións

Como punto de partida, importe todas as personalizacións nun ambiente limpo de Operacións do proxecto (Lite) para confirmar que a importación se realiza correctamente e que as operacións comerciais se comportan como se esperaba.

Aquí tes algunhas cousas que debes ter en conta:

- A importación pode fallar porque faltan dependencias. Noutras palabras, as personalizacións fan referencia a campos ou outros compoñentes que foron eliminados en Operacións do proxecto. Neste caso, elimine estas dependencias do contorno de desenvolvemento.
- Se as túas solucións non xestionadas e xestionadas inclúen compoñentes que non están personalizados, elimina eses compoñentes da solución. Por exemplo, cando personaliza o **Proxecto** entidade, engade só a cabeceira da entidade á súa solución. Non engada todos os campos. Se engadiches previamente todos os subcompoñentes, quizais teñas que crear manualmente unha nova solución e engadirlle compoñentes relevantes.
- É posible que os formularios e as vistas non aparezan como se esperaba. Baixo algunhas circunstancias, se personalizou algún dos formularios ou vistas listados, as personalizacións poden impedir que as novas actualizacións en Project Operations teñan efecto. Para identificar estes problemas, recomendámosche que fagas unha revisión en paralelo dunha instalación limpa de Project Operations e dunha instalación de Project Operations que inclúa as túas personalizacións. Compara os formularios máis usados na túa empresa para confirmar que a túa versión do formulario aínda ten sentido e que non falta nada da versión limpa do formulario. Fai o mesmo tipo de revisión en paralelo para todas as vistas que personalizaches.
- A lóxica empresarial pode fallar en tempo de execución. Dado que as referencias aos campos dos seus complementos non se validan no momento da importación, a lóxica empresarial pode fallar debido a referencias a campos que xa non existen e pode recibir unha mensaxe de erro que se asemella ao seguinte exemplo: "'Proxecto' a entidade non contén atributo con Nome = 'msdyn_plannedhours' e NameMapping = 'Lóxico'." Neste caso, modifica as túas personalizacións para que utilicen os novos campos. Se usas clases de proxy xeradas automaticamente e referencias de tipos fortes na lóxica do complemento, considera rexenerar eses proxies desde unha instalación limpa. Deste xeito, pode identificar facilmente todos os lugares onde os seus complementos dependen de campos obsoletos.

Despois de actualizar as túas personalizacións para importar correctamente as operacións do proxecto, pasa aos seguintes pasos.

## <a name="end-to-end-testing-in-development-environments"></a>Probas de extremo a extremo en contornos de desenvolvemento

### <a name="initiate-upgrade"></a>Iniciar actualización 

1. No Power Platform centro de administración, busque e seleccione o seu entorno. Despois, nas aplicacións, busque e seleccione **Dynamics 365 Project Operations**.
2. Seleccione **Instalar** para iniciar a actualización. O Power Platform o centro de administración presentará esta instalación como unha nova instalación. Non obstante, detectarase a presenza dunha versión anterior de Project Service Automation e actualizarase a instalación existente.

    Despois de completar a actualización, o ambiente debería mostrar que Project Operations está instalado e que Project Service Automation non está instalado.

    Dependendo da cantidade de datos do contorno, a actualización pode levar varias horas. O equipo principal que xestiona a actualización debe planificar en consecuencia e executar a actualización durante as horas non laborables. Nalgúns casos, se o volume de datos é grande, a actualización debería executarse durante a fin de semana. A decisión sobre a programación debe basearse nos resultados das probas en ambientes inferiores.

3. Actualiza as solucións personalizadas segundo corresponda. Neste punto, implementa todos os cambios que fixeches nas túas personalizacións no ficheiro [Proba e refactorización de personalizacións](#testing-and-refactoring-customizations) sección deste artigo.
4. Ir a **Configuración** \> **Solucións**, e seleccione para desinstalar **Operacións do proxecto Compoñentes obsoletos** solución.

    Esta solución é unha solución temporal que contén o modelo de datos existente e os compoñentes que están presentes durante a actualización. Ao eliminar esta solución, elimina todos os campos e compoñentes que xa non se usan. Deste xeito, axudas a simplificar a interface e facilita a integración e a extensión.
    
### <a name="upgrade-to-project-operations-lite"></a>Actualiza a Project Operations Lite

Os seguintes pasos describen o proceso de actualización e o rexistro de erros asociado:

1. **Verificación da versión de PSA:** Para instalar Project Operations, debes ter V3.10.58.120 ou superior.
1. **Validación previa:** Cando un administrador inicia unha actualización, o sistema executa unha operación de validación previa en cada entidade que é o núcleo da solución Project Operations. Este paso verifica que todas as referencias de entidades sexan válidas e garante que os datos relacionados coa WBS estean dentro dos límites publicados de Project for the Web.
1. **Actualización de metadatos:** Despois da validación previa exitosa, o sistema inicia cambios no esquema e crea unha solución de compoñentes obsoletos. Podes eliminar esta solución obsoleta despois de completar toda a refactorización necesaria das personalizacións. Este paso é a parte máis longa do proceso de actualización e pode tardar ata catro horas en completarse.
1. **Actualización de datos:** Despois de que se completen todos os cambios de esquema necesarios no paso de actualización de metadatos, os teus datos migráranse ao novo esquema e realízanse os predeterminados e os recálculos necesarios.
1. **Actualización do motor de programación do proxecto:** Despois da actualización de datos exitosa, o **Horario** a pestana da páxina principal reetiquetárase **Tarefas**. Cando un usuario selecciona esta pestana despois da actualización, diríxese a que vaia á grella de seguimento para ver unha versión de só lectura do WBS. Para editar a WBS, deben iniciar a programación [proceso de conversión](/PSA-Upgrade-Project-Conversion.md). Todos os proxectos sen WBS preexistente poden usar a nova experiencia de programación directamente, sen conversión.
 
### <a name="validate-common-scenarios"></a>Validar escenarios comúns

Cando valides as túas personalizacións específicas, recomendámosche que revises tamén os procesos comerciais admitidos nas aplicacións. Estes procesos de negocio inclúen, pero non se limitan a, a creación de entidades de vendas, como cotizacións e contratos, e a creación de proxectos que inclúan WBS e aprobación de reais.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Principais cambios entre Project Service Automation e Project Operations

Esta sección ofrece un resumo dos principais cambios que pode esperar entre Project Service Automation e Project Operations.

### <a name="project-planning"></a>Planificación de proxectos

As capacidades de planificación de proxectos en Project Operations xa non dependen dunha combinación de lóxica do lado cliente e lóxica do servidor. Pola contra, Project Operations usa Project for the Web como motor de programación. Este cambio nas capacidades de programación permite varias funcións novas, como vistas de Board e Gantt, planificación baseada en recursos, [elementos da lista de verificación de tarefas](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c), e modos de programación de proxectos. As novas capacidades de programación tamén están soportadas por un rico conxunto de novas [interfaces de programación de aplicacións (API)](../project-management/schedule-api-preview.md). Estas API están destinadas a garantir que ningunha operación programática para crear, actualizar ou eliminar unha entidade no WBS corrompe os campos calculados na programación.

### <a name="billing-and-pricing"></a>Facturación e prezos

Como parte dos investimentos continuos en Operacións do proxecto, hai dispoñibles varias capacidades novas en Facturación e prezos. Aquí van algúns exemplos:

- [Rexistrar o uso do material en proxectos e tarefas do proxecto](../material/material-usage-log.md)
- [Xestión de subcontratación](../pro/subcontracting/managing-subcontracts-overview.md)
- [Contratos baseados en adiantos e retencións](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Estado de non exceder do contrato e validacións](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Facturación baseada en tarefas

### <a name="resource-management"></a>Xestión de recursos

Project Operations ofrece soporte opcional para Universal Resource Scheduling (URS) axudante de planificación e consello. Esta nova experiencia será obrigatoria na onda de abril de 2023.

## <a name="frequently-asked-questions"></a>Preguntas máis frecuentes

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>Que tipos de implementación se admiten actualmente para a actualización?

| Código fonte                                                 | Destino                                                    | Progresión                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Project Service Automation                             | Implementación de Project Operations Lite                        | Compatible               |
| Dynamics 365 Finance Xestión de proxectos e contabilidade | Implementación de Project Operations Lite                        | Non é compatible actualmente |
| Xestión de proxectos financeiros e contabilidade              | Project Operations para escenarios baseados en recursos ou sen existencias     | Non é compatible actualmente |
| Project Service Automation 3.x                         | Project Operations para escenarios baseados en recursos ou sen existencias     | Non é compatible actualmente |
| Proxecto para a Web (entorno dedicado)            | Implementación de Project Operations Lite                        | Non é compatible actualmente |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>Como podo instalar Project Operations antes de que a ferramenta de actualización estea dispoñible?

Hai dúas opcións para instalar Project Operations antes de que a ferramenta de actualización estea dispoñible:

- Proporcionar un novo ambiente.
- Implementa Project Operations por separado en calquera organización de vendas onde Project Service Automation non estea presente.

Se Project Service Automation está instalado nunha organización, pero non se utilizou, pódese desinstalar. Despois de eliminar completamente Project Service Automation, Project Operations pódese instalar na mesma organización.
