---
title: Desempeño da API de programación de proxectos
description: Este artigo ofrece información sobre os puntos de referencia de rendemento das API de programación do proxecto e identifica as mellores prácticas para un uso óptimo.
author: ruhercul
ms.date: 11/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1ee1bd8e4412ee1d10f445628c5dc87cc9fa91d3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911180"
---
# <a name="project-schedule-api-performance"></a>Desempeño da API de programación de proxectos

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento, despregamento de Lite: facturación proforma, Project for the Web_

Este artigo ofrece información sobre os puntos de referencia de rendemento das interfaces de programación de aplicacións (API) de programación do proxecto e identifica as mellores prácticas para un uso optimizado.

## <a name="project-scheduling-service"></a>Servizo de programación de proxectos
O servizo de programación de proxectos é un servizo de varios arrendatarios que se executa en Microsoft Azure. Está deseñado para mellorar a interacción proporcionando unha experiencia rápida e fluída cando os usuarios traballan en proxectos. Esta mellora conséguese aceptando solicitudes de cambio, procesándoas e devolvendo inmediatamente o resultado. O servizo persiste de forma asíncrona en Dataverse e non impide que os usuarios realicen outras operacións.

As API de programación de proxectos dependen do servizo de programación de proxectos para executar solicitudes que se describen con máis detalle en seccións posteriores deste artigo.

As API de programación do proxecto están deseñadas para funcionar coas seguintes entidades de estrutura de subdivisión do traballo (WBS):

  - Project
  - Tarefa do proxecto
  - Dependencia da tarefa do proxecto
  - Membro do equipo do proxecto
  - Atribución do recurso
  
Admítense tanto os campos listos para usar como personalizados. A menos que se indique o contrario, admítense todas as operacións comúns, como crear, actualizar e eliminar. Para obter máis información, consulte [Usar as API de programación do proxecto para realizar operacións e programar entidades](schedule-api-preview.md).

Como parte das API de programación do proxecto, engadiuse un patrón de unidade de traballo. Este patrón coñécese como OperationSet e pódese utilizar cando se deben procesar varias solicitudes nunha soa transacción.

A seguinte ilustración mostra o fluxo que experimentará un asociado cando se utilice esta función.

![Dataverse e fluxo do servizo de programación de proxectos.](./media/dataverse-project-scheduling-service-flow.png)

**Paso 1**: Un cliente realiza unha chamada de API a un extremo de protocolo de datos abertos (OData) en Dataverse para crear un OperationSet.

**Paso 2**: Despois de crear o novo OperationSet, devólvese un valor de **OperationSetId**.

**Paso 3**: O cliente usa o valor **OperationSetId** valor para realizar outra solicitude de API de programación de proxectos. O resultado é unha solicitude de creación, actualización ou eliminación nunha entidade de programación. Cando se fai esta solicitude, realízase a validación dos metadatos. Se a validación falla, a solicitude finaliza e devólvese un erro.

**Pasos 4a-4c**: Estes pasos representan a fase ACEPTAR. O cliente chama á API **ExecuteOperationSetV1**, que envía todos os cambios ao servizo de programación de proxectos nun lote. O servizo de programación de proxectos executa as súas propias validacións nas solicitudes do lote. Calquera erro de validación desfai o lote e devolve unha excepción ao autor de chamada. Se o servizo de programación de proxectos acepta o lote con éxito, o estado de OperationSet actualízase para reflectir o feito de que o servizo de programación de proxectos está a procesar OperationSet.

**Paso 5**: Este paso representa é a fase PERSISTIR. O servizo de programación de proxectos escribe o lote de forma asíncrona en Dataverse nunha transacción. Se a operación de escritura ten éxito, OperationSet márcase como **Completado**. Calquera erro desfai a transacción e o lote, e o OperationSet márcase como **Errado**.

## <a name="performance-methodology"></a>Metodoloxía de actuación
O tempo de execución defínese como o tempo desde a chamada ata a API **ExecuteOperationSetV1** ata que o servizo de programación de proxectos remate de escribir a Dataverse. Todas as operacións execútanse en conxunto 2200 veces e infórmase das medicións do tempo de execución de P99. Mídense as operacións de rexistro único e en masa.

Para unha operación de rexistro único, OperationSet contén unha solicitude. Para operacións masivas, contén 20, 50 ou 100 solicitudes. Cada tamaño masivo comunícase por separado.

Estas operacións execútanse nun despregamento de UR 15 Project Operations Lite en América do Norte.

## <a name="results"></a>Resultados
### <a name="create-operations"></a>Crear operacións
#### <a name="single-record-create-operations"></a>Operacións de creación de rexistro único
A seguinte táboa mostra os tempos de execución para a creación dun rexistro único. Os tempos están en segundos.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Tipo de&nbsp;&nbsp;&nbsp;rexistro</th>
    <th class="tg-0lax" colspan="2">Tempo</th>
  </tr>
  <tr>
    <th class="tg-0lax">Campos obrigatorios</th>
    <th class="tg-0lax">Todos os campos admitidos</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Project</td>
    <td class="tg-0lax">2.5</td>
    <td class="tg-0lax">3.78</td>
  </tr>
  <tr>
    <td class="tg-0lax">Tarefa</td>
    <td class="tg-0lax">8.82</td>
    <td class="tg-0lax">9.34</td>
  </tr>
  <tr>
    <td class="tg-0lax">Atribución</td>
    <td class="tg-0lax">9.19</td>
    <td class="tg-0lax">9.19</td>
  </tr>
  <tr>
    <td class="tg-0lax">Membro do equipo</td>
    <td class="tg-0lax">0.84</td>
    <td class="tg-0lax">4.2</td>
  </tr>
  <tr>
    <td class="tg-0lax">Dependencia</td>
    <td class="tg-0lax">8.84</td>
    <td class="tg-0lax">8.84</td>
  </tr>
</tbody>
</table>

#### <a name="bulk-create-operations"></a>Operacións de creación en masa
A seguinte táboa mostra os tempos de execución para a creación de moitos rexistros. En concreto, Microsoft mediu os tempos de execución para a creación de 20, 50 e 100 rexistros nun único OperationSet. Os tempos están en segundos.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="3">Tipo de&nbsp;&nbsp;&nbsp;rexistro</th>
    <th class="tg-0lax" colspan="6">Tempo</th>
  </tr>
  <tr>
    <th class="tg-0lax" colspan="2">20 rexistros</th>
    <th class="tg-0lax" colspan="2">50 rexistros</th>
    <th class="tg-0lax" colspan="2">100 rexistros</th>
  </tr>
  <tr>
    <th class="tg-0lax">Campos obrigatorios</th>
    <th class="tg-0lax">Todos os campos admitidos</th>
    <th class="tg-0lax">Campos obrigatorios</th>
    <th class="tg-0lax">Todos os campos admitidos</th>
    <th class="tg-0lax">Campos obrigatorios</th>
    <th class="tg-0lax">Todos os campos admitidos</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Tarefa</td>
    <td class="tg-0lax">19.92</td>
    <td class="tg-0lax">38.35</td>
    <td class="tg-0lax">36.67</td>
    <td class="tg-0lax">99.13</td>
    <td class="tg-0lax">116.77</td>
    <td class="tg-0lax">174.06</td>
  </tr>
  <tr>
    <td class="tg-0lax">Atribución</td>
    <td class="tg-0lax">13.94</td>
    <td class="tg-0lax">13.94</td>
    <td class="tg-0lax">43.95</td>
    <td class="tg-0lax">43.95</td>
    <td class="tg-0lax">69.38</td>
    <td class="tg-0lax">69.38</td>
  </tr>
  <tr>
    <td class="tg-0lax">Dependencia</td>
    <td class="tg-0lax">30.04</td>
    <td class="tg-0lax">30.04</td>
    <td class="tg-0lax">77.82</td>
    <td class="tg-0lax">77.82</td>
    <td class="tg-0lax">176.89</td>
    <td class="tg-0lax">176.89</td>
  </tr>
</tbody>
</table>

> [!NOTE] 
> As operacións de creación masiva nas entidades **Proxecto** e **Membro do equipo** non están incluídas nesta táboa, porque o tempo de execución para esas operacións aseméllase ao tempo de execución cando a API para crear un único rexistro se chama varias veces. Estas API execútanse inmediatamente en Dataverse.

A seguinte ilustración mostra un gráfico dos tempos de execución para as entidades **Tarefa**, **Atribución** e **Dependencia** cando se crean 20, 50 e 100 rexistros e se utilizan todos os campos admitidos.

![Cree un gráfico de tempo de execución de rexistro.](./media/create-record-execution-time.png)

### <a name="update-operations"></a>Actualizar operacións
#### <a name="single-record-update-operations"></a>Operacións de actualización de rexistro único
A seguinte táboa mostra os tempos de execución para as actualizacións dun rexistro único. Os tempos están en segundos.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Tipo de&nbsp;&nbsp;&nbsp;rexistro</th>
    <th class="tg-0lax" colspan="2">Tempo</th>
  </tr>
  <tr>
    <th class="tg-0lax">Campos obrigatorios </th>
    <th class="tg-0lax">Todos os campos admitidos</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Project</td>
    <td class="tg-0lax">9.53</td>
    <td class="tg-0lax">13.91</td>
  </tr>
  <tr>
    <td class="tg-0lax">Tarefa</td>
    <td class="tg-0lax">8.82</td>
    <td class="tg-0lax">9.91</td>
  </tr>
  <tr>
    <td class="tg-0lax">Membro do equipo</td>
    <td class="tg-0lax">9</td>
    <td class="tg-0lax">8.96</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> As operacións de actualización nas entidades **Atribucións de recursos** e **Dependencia da tarefa do proxecto** non se admiten.

#### <a name="bulk-update-operations"></a>Operacións de actualización en masa
A seguinte táboa mostra os tempos de execución para as actualizacións de moitos rexistros. En concreto, Microsoft mediu os tempos de execución para as actualizacións de 20, 50 e 100 rexistros nun único OperationSet. Os tempos están en segundos.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="3">Tipo de&nbsp;&nbsp;&nbsp;rexistro</th>
    <th class="tg-0lax" colspan="6">Tempo</th>
  </tr>
  <tr>
    <th class="tg-0lax" colspan="2">20 rexistros</th>
    <th class="tg-0lax" colspan="2">50 rexistros</th>
    <th class="tg-0lax" colspan="2">100 rexistros</th>
  </tr>
  <tr>
    <th class="tg-0lax">Campos obrigatorios</th>
    <th class="tg-0lax">Todos os campos admitidos</th>
    <th class="tg-0lax">Campos obrigatorios</th>
    <th class="tg-0lax">Todos os campos admitidos</th>
    <th class="tg-0lax">Campos obrigatorios</th>
    <th class="tg-0lax">Todos os campos admitidos</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Tarefa</td>
    <td class="tg-0lax">8.91</td>
    <td class="tg-0lax">38.71</td>
    <td class="tg-0lax">20.92</td>
    <td class="tg-0lax">87.13</td>
    <td class="tg-0lax">36.68</td>
    <td class="tg-0lax">190.34</td>
  </tr>
  <tr>
    <td class="tg-0lax">Membro do equipo</td>
    <td class="tg-0lax">20.52</td>
    <td class="tg-0lax">26.06</td>
    <td class="tg-0lax">41.93</td>
    <td class="tg-0lax">44.51</td>
    <td class="tg-0lax">38.63</td>
    <td class="tg-0lax">66.53</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> As operacións de actualización nas entidades **Atribucións de recursos** e **Dependencia da tarefa do proxecto** non se admiten.

A seguinte ilustración mostra un gráfico dos tempos de execución para as entidades Tarefa e Membro do equipo cando se actualizan 20, 50 e 100 rexistros e se utilizan todos os campos admitidos.

![Actualice un gráfico de tempo de execución de rexistro.](./media/update-record-execution-time.png)

### <a name="delete-operations"></a>Eliminar operacións
#### <a name="single-record-delete-operations"></a>Operacións de eliminación de rexistro único
A seguinte táboa mostra os tempos de execución para a eliminación dun rexistro único. Os tempos están en segundos.

| Tipo de rexistro | Tempo  |
|-------------|-------|
| Tarefa        | 20.12 |
| Atribución  | 10.86 |
| Membro do equipo | 12.52 |
| Dependencia  | 20.89 |

> [!NOTE]
> As operacións de eliminación na entidade **Proxecto** nn se admiten.

#### <a name="bulk-delete-operations"></a>Operacións de eliminación en masa
A seguinte táboa mostra os tempos de execución para a eliminación de moitos rexistros. En concreto, Microsoft mediu os tempos de execución para a eliminación de 20, 50 e 100 rexistros nun único OperationSet. Os tempos están en segundos.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Tipo de&nbsp;&nbsp;&nbsp;rexistro</th>
    <th class="tg-0lax" colspan="3">Tempo</th>
  </tr>
  <tr>
    <th class="tg-0lax">20 rexistros</th>
    <th class="tg-0lax">50 rexistros</th>
    <th class="tg-0lax">100 rexistros</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Tarefa</td>
    <td class="tg-0lax">20.91</td>
    <td class="tg-0lax">67.43</td>
    <td class="tg-0lax">71.96</td>
  </tr>
  <tr>
    <td class="tg-0lax">Atribución</td>
    <td class="tg-0lax">11.75</td>
    <td class="tg-0lax">25.79</td>
    <td class="tg-0lax">47.66</td>
  </tr>
  <tr>
    <td class="tg-0lax">Membro do equipo</td>
    <td class="tg-0lax">9.78</td>
    <td class="tg-0lax">39.73</td>
    <td class="tg-0lax">24.33</td>
  </tr>
  <tr>
    <td class="tg-0lax">Dependencia</td>
    <td class="tg-0lax">24.61</td>
    <td class="tg-0lax">54.9</td>
    <td class="tg-0lax">109.16</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> As operacións de eliminación na entidade **Proxecto** nn se admiten.

A seguinte ilustración mostra un gráfico dos tempos de execución para as entidades **Tarefa**, **Atribución** e **Membro do equipo** e **Dependencia** cando se eliminan 20, 50 e 100 rexistros e se utilizan todos os campos admitidos.

![Elimine un gráfico de tempo de execución de rexistro.](./media/delete-record-execution-time.png)

## <a name="observations"></a>Observacións
Para cada operación de rexistro, a API **ExecuteOperationSet** tarda uns 800 milisegundos en enviar unha solicitude ao servizo de programación de proxectos. O servizo de programación de proxectos tarda uns cinco segundos en procesar a carga útil e chamar a Dataverse. O resto do tempo de execución úsase executando a lóxica empresarial e escribindo datos na base de datos en Dataverse.

Cando se crean, actualizan ou eliminan 100 rexistros, a API **ExecuteOperationSet** tarda uns tres segundos en enviar a solicitude ao servizo de programación de proxectos. O servizo de programación de proxectos tarda uns cinco segundos en procesar as solicitudes e chamar a Dataverse. As operacións masivas deben pagar a **Imposto do servizo de programación de proxectos** unha vez, para todos os rexistros de OperationSet. Polo tanto, as operacións masivas teñen un tempo medio de execución significativamente menor que as operacións de rexistro único.

## <a name="scenarios"></a>Escenarios
A seguinte táboa mostra os tempos de execución nos que se usan as API de programación de proxectos para lograr situacións específicas. Os tempos están en segundos.

| Escenario                                                                   | Tempo  |
|----------------------------------------------------------------------------|-------|
| Cree un proxecto que teña 40 tarefas.                                      | 36.01 |
| Cree un proxecto que teña 40 tarefas e 20 dependencias.                  | 38.11 |
| Cree un proxecto que teña 40 tarefas e 30 atribucións.                   | 60.17 |
| Cree un proxecto que teña 40 tarefas, 20 dependencias e 30 atribucións. | 60.27 |

## <a name="best-practices"></a>Recomendacións
Segundo os resultados da situación anterior, as API funcionan mellor nas seguintes condicións:

  - Agrupe tantas operacións como sexa posible. O tempo de execución medio para operacións masivas é mellor que o tempo de execución medio para operacións de rexistro único. Canto menor sexa o número de OperationSets en uso, máis rápido será o tempo medio de execución.
  - Defina só os atributos mínimos que son necesarios para lograr a súa situación. Sexa selectivo sobre os tipos de campos non obrigatorios incluídos nunha solicitude de OperationSet. Os campos que conteñan claves estranxeiras ou campos de resumo afectarán negativamente ao rendemento.
