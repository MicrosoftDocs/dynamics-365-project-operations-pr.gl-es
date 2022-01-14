---
title: Actualiza de Project Service Automation a Project Operations
description: Este tema ofrece unha visión xeral do proceso desde o que se actualiza Microsoft Dynamics 365 Project Service Automation a Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/05/2022
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
ms.openlocfilehash: 9363fd5a06b6b1ba023961b03228e13a53a82002
ms.sourcegitcommit: 5789766efae1e0cb513ea533e4f9ac1e553158a5
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 01/10/2022
ms.locfileid: "7954291"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Actualiza de Project Service Automation a Project Operations

Estamos encantados de anunciar a primeira das tres fases para a actualización Microsoft Dynamics 365 Project Service Automation a Dynamics 365 Project Operations. Este tema ofrece unha visión xeral para os clientes que se están embarcando nesta emocionante viaxe. Os temas futuros incluirán consideracións para os desenvolvedores e detalles sobre as melloras das funcións. Non só proporcionarán orientación para axudarche a preparar a túa actualización a Project Operations, senón que tamén explicarán o que podes esperar despois de actualizar.

O programa de entrega de actualizacións dividirase en tres fases.

| Actualizar a entrega | Fase 1 (xaneiro de 2022) | Fase 2 (Onda de abril de 2022) | Fase 3 (Onda de abril de 2022) |
|------------------|------------------------|---------------------------|---------------------------|
| Non depende da estrutura de desagregación do traballo (WBS) dos proxectos | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| O WBS dentro dos límites actualmente soportados das operacións do proxecto | | :heavy_check_mark: | :heavy_check_mark: |
| O WBS fóra dos límites actualmente compatibles de Project Operations, incluído o soporte para o cliente de escritorio de Project | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>Funcións do proceso de actualización 

Como parte do proceso de actualización, engadimos rexistros de actualizacións ao mapa do sitio, para que os administradores poidan diagnosticar erros máis facilmente. Ademais da nova interface, engadiranse novas regras de validación para garantir a integridade dos datos despois dunha actualización. As seguintes validacións engadiranse ao proceso de actualización.

| Validacións | Fase 1 (xaneiro de 2022) | Fase 2 (Onda de abril de 2022) | Fase 3 (Onda de abril de 2022) |
|-------------|------------------------|---------------------------|---------------------------|
| O WBS validarase contra violacións comúns da integridade dos datos (por exemplo, asignacións de recursos que están asociadas coa mesma tarefa principal pero que teñen proxectos principais). | | :heavy_check_mark: | :heavy_check_mark: |
| O WBS validarase contra o [límites coñecidos de Project for the Web](/project-for-the-web/project-for-the-web-limits-and-boundaries). | | :heavy_check_mark: | :heavy_check_mark: |
| O WBS validarase contra os límites coñecidos do cliente de escritorio do proxecto. | | :heavy_check_mark: | :heavy_check_mark: |
| Os recursos reservables e os calendarios de proxectos avaliaranse en función das excepcións comúns ás regras de calendario incompatibles. | | :heavy_check_mark: | :heavy_check_mark: |

Na fase 2, os clientes que se actualicen a Project Operations terán os seus proxectos existentes actualizados a unha experiencia de só lectura para a planificación do proxecto. Nesta experiencia de só lectura, o WBS completo estará visible na grella de seguimento. Para editar a WBS, os xestores de proxectos poden seleccionar **Converter** na principal **Proxectos** páxina. A continuación, un proceso en segundo plano actualizará o proxecto para que admita a nova experiencia de programación de proxectos de Project for the Web. Esta fase é axeitada para clientes que teñan proxectos que encaixan dentro do [límites coñecidos de Project for the Web](/project-for-the-web/project-for-the-web-limits-and-boundaries).

Na fase 3, engadirase soporte para o cliente de escritorio de Project, en beneficio dos clientes que queiran seguir editando os seus proxectos desde esa aplicación. Non obstante, se os proxectos existentes se converten á nova experiencia Proxecto para a web, desactivarase o acceso ao complemento para cada proxecto convertido.

## <a name="prerequisites"></a>Requisitos previos

Para ser elixible para a actualización da fase 1, un cliente debe cumprir os seguintes criterios:

- O ambiente de destino non debe conter ningún rexistro no **msdyn_projecttask** entidade.
- As licenzas válidas de Project Operations deben asignarse a todos os usuarios activos do cliente. 
- O cliente debe validar o proceso de actualización en polo menos un ambiente que non sexa de produción que teña un conxunto de datos representativo que estea aliñado cos datos de produción.
- O ambiente de destino debe actualizarse á versión 38 de actualización de Project Service Automation ou posterior.

Os requisitos previos para as fases 2 e 3 actualizaranse a medida que se aproximen as datas xerais de dispoñibilidade.

## <a name="licensing"></a>Obtención de licenzas

Se tes licenzas activas para Project Service Automation, podes instalar e usar Project Operations, que inclúe todas as capacidades de Project Service Automation e moito máis. Deste xeito, podes probar as capacidades de Project Operations mentres continúas usando Project Service Automation na produción. Despois de que caduquen as licenzas de Project Service Automation, terás que pasar a Project Operations. Cando planifiques esta transición, debes ter en conta o feito de que a licenza de Project Operations non inclúe unha licenza de Project Service Automation.

## <a name="testing-and-refactoring-customizations"></a>Proba e refactorización de personalizacións

Como punto de partida, importe todas as personalizacións nun ambiente limpo de Project Operations (lite) para confirmar que a importación se realiza correctamente e que as operacións comerciais se comportan como se esperaba.

Aquí tes algunhas cousas que debes ter en conta:

- A importación pode fallar por falta de dependencias. Noutras palabras, as personalizacións fan referencia a campos ou outros compoñentes que foron eliminados en Operacións do proxecto. Neste caso, elimine estas dependencias do contorno de desenvolvemento.
- Se as túas solucións non xestionadas e xestionadas inclúen compoñentes que non están personalizados, elimina eses compoñentes da solución. Por exemplo, cando personaliza o **Proxecto** entidade, engade só a cabeceira da entidade á súa solución. Non engada todos os campos. Se engadiches previamente todos os subcompoñentes, quizais teñas que crear manualmente unha nova solución e engadirlle os compoñentes relevantes.
- É posible que os formularios e as vistas non aparezan como inesperados. Baixo algunhas circunstancias, se personalizou algún dos formularios ou vistas listados, as personalizacións poden impedir que as novas actualizacións en Project Operations teñan efecto. Para identificar estes problemas, recomendámosche que fagas unha revisión en paralelo dunha instalación limpa de Project Operations e dunha instalación de Project Operations que inclúa as túas personalizacións. Compara os formularios máis utilizados na túa empresa para confirmar que a túa versión do formulario aínda ten sentido e que non falta nada da versión limpa do formulario. Fai o mesmo tipo de revisión en paralelo para todas as vistas que personalizaches.
- A lóxica empresarial pode fallar no tempo de execución. Dado que as referencias aos campos dos seus complementos non se validan no momento da importación, a lóxica empresarial pode fallar debido a referencias a campos que xa non existen e pode recibir unha mensaxe de erro que se asemella ao seguinte exemplo: "'Proxecto' a entidade non contén atributo con Nome = 'msdyn_plannedhours' e NameMapping = 'Lóxico'." Neste caso, modifica as túas personalizacións para que utilicen os novos campos. Se usas clases de proxy xeradas automaticamente e referencias de tipos fortes na lóxica do complemento, considera rexenerar eses proxies desde unha instalación limpa. Deste xeito, pode identificar facilmente todos os lugares onde os seus complementos dependen de campos obsoletos.

Despois de actualizar as túas personalizacións para importar correctamente as operacións do proxecto, pasa aos seguintes pasos.

## <a name="end-to-end-testing-in-lower-environments"></a>Probas de extremo a extremo en ambientes inferiores

### <a name="run-the-upgrade-in-production"></a>Executa a actualización en produción

1. No Power Platform centro de administración, busque e seleccione o seu entorno. Despois, nas aplicacións, busque e seleccione **Dynamics 365 Project Operations**.
2. Seleccione **Instalar** para iniciar a actualización. O Power Platform O centro de administración presentará esta instalación como unha nova instalación. Non obstante, detectarase a presenza dunha versión anterior de Project Service Automation e actualizarase a instalación existente.

    Despois de completar a actualización, o ambiente debería mostrar que Project Operations está instalado e que Project Service Automation non está instalado.

    > [!NOTE]
    > Dependendo da cantidade de datos do contorno, a actualización pode levar varias horas. O equipo principal que xestiona a actualización debe planificar en consecuencia e executar a actualización durante as horas non laborables. Nalgúns casos, se o volume de datos é grande, a actualización debería executarse durante a fin de semana. A decisión sobre a programación debería basearse nos resultados das probas en ambientes inferiores.

3. Actualiza as solucións personalizadas segundo corresponda. Neste punto, implementa os cambios que fixeches nas túas personalizacións no ficheiro [Proba e refactorización de personalizacións](#testing-and-refactoring-customizations) sección deste tema.
4. Ir a **Configuración** \> **Solucións**, e seleccione para desinstalar **Operacións do proxecto Compoñentes obsoletos** solución.

    Esta solución é unha solución temporal que contén o modelo de datos existente e os compoñentes que están presentes durante a actualización. Ao eliminar esta solución, elimina todos os campos e compoñentes que xa non se utilizan. Deste xeito, axudas a simplificar a interface e facilita a integración e a extensión.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Principais cambios entre Project Service Automation e Project Operations

Esta sección ofrece un resumo dos principais cambios que pode esperar entre Project Service Automation e Project Operations.

### <a name="project-planning"></a>Planificación de proxectos

As capacidades de planificación de proxectos en Project Operations xa non dependen dunha combinación de lóxica do lado cliente e lóxica do servidor. Pola contra, Project Operations usa Project for the Web como motor de programación. Este cambio nas capacidades de programación permite varias funcións novas, como vistas de Board e Gantt, planificación baseada en recursos, [elementos da lista de verificación de tarefas](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c), e modos de programación de proxectos. As novas capacidades de programación tamén están soportadas por un rico conxunto de novas [interfaces de programación de aplicacións (API)](../project-management/schedule-api-preview.md). Estas API están destinadas a garantir que ningunha operación programática para crear, actualizar ou eliminar unha entidade no WBS corrompe os campos calculados na programación.

## <a name="billing-and-pricing"></a>Facturación e prezos

Como parte dos investimentos continuos en Operacións do proxecto, hai dispoñibles varias capacidades novas en Facturación e prezos. Aquí van algúns exemplos:

- [Rexistrar o uso do material en proxectos e tarefas do proxecto](../material/material-usage-log.md)
- [Xestión de subcontratación](../pro/subcontracting/managing-subcontracts-overview.md)
- [Contratos baseados en adiantos e retencións](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Estado de non exceder do contrato e validacións](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Facturación baseada en tarefas

## <a name="frequently-asked-questions"></a>Preguntas máis frecuentes

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>Que tipos de implementación se admiten actualmente para a actualización?

| Código fonte                                                 | Destino                                                    | Progresión                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Project Service Automation                             | Implementación de Project Operations Lite                        | Compatible               |
| Dynamics 365 Finance Xestión de proxectos e contabilidade | Implementación de Project Operations Lite                        | Non é compatible actualmente |
| Xestión de proxectos financeiros e contabilidade              | Project Operations para escenarios baseados en recursos ou sen existencias     | Non é compatible actualmente |
| Xestión de proxectos financeiros e contabilidade              | Project Operations para situacións baseadas en recursos/sen fornecemento | Non é compatible actualmente |
| Project Service Automation 3.x                         | Project Operations para escenarios baseados en recursos ou sen existencias     | Non é compatible actualmente |
| Proxecto para a Web (entorno dedicado)            | Implementación de Project Operations Lite                        | Non é compatible actualmente |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>Como podo instalar Project Operations antes de que a ferramenta de actualización estea dispoñible?

Hai dúas opcións para instalar Project Operations antes de que a ferramenta de actualización estea dispoñible:

- Proporcionar un novo ambiente.
- Implementa Project Operations por separado en calquera organización de vendas onde Project Service Automation non estea presente.

> [!NOTE]
> Se Project Service Automation está instalado nunha organización, pero non se utilizou, pódese desinstalar. Despois de eliminar completamente Project Service Automation, Project Operations pódese instalar na mesma organización.
