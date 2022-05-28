---
title: Previsións e orzamentos de proxectos
description: Microsoft Dynamics 365 Finance ofrece previsións e orzamentos de proxectos para xestionar e controlar os seus proxectos.
author: Yowelle
ms.date: 10/25/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ForecastModel, ProjYearEndProcess
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 23501
ms.assetid: 4e6d1384-19a2-4232-b3f3-d2590c218bd7
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 15731010877b5d62329867e878f624149e74f761
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/04/2022
ms.locfileid: "8684548"
---
# <a name="project-forecasts-and-budgets"></a>Previsións e orzamentos de proxectos

[!include [banner](../includes/banner.md)]

Hai dous xeitos de xestionar e controlar os seus proxectos: previsións de proxectos e orzamentos de proxectos. 

Utilice as previsións de proxectos se a súa organización ten unha perspectiva operativa e se centra nos ingresos e custos derivados de transaccións específicas. Utilice os orzamentos de proxectos se a súa organización se centra máis nas cantidades financeiras. 

Tanto as previsións como os orzamentos de proxectos utilizan modelos de previsión para manter os importes das transaccións proxectadas. 

Cada método ten as súas vantaxes. Debería considerar os seguintes puntos antes de seleccionar un método para a súa organización.

|   Método de atribución       |           Previsións de proxectos            |        Orzamentos de proxectos                           |
|---------------------------|------------------------------------------|----------------------------------------------------|
| **Asignación de períodos**     | Non pode asignar transaccións de xeito explícito a un período fiscal. Pola contra, a previsión e o control da previsión baséanse na vida do proxecto. Debido a que as previsións están baseadas nunha data específica, debe deducir o período a partir da data. | Non pode asignar transaccións a todo o proxecto ou a un período fiscal. Se asigna a un período, podes trasladar as cantidades non utilizadas ao seguinte período fiscal. |
| **Visualización de transaccións**  | Pode visualizar as transaccións nos formularios de previsións, onde pode ver as previsións para toda a empresa e para todos os proxectos, independentemente da xerarquía. Para centrarse nun proxecto concreto, debe filtrar os datos.                                       | Pode ver as transaccións orzamentadas para unha única xerarquía do proxecto. Polo tanto, pode ver os detalles das transaccións dun proxecto principal ou dos seus subproxectos.                 |
| **Variables das transaccións** | Cando introduce as transaccións previstas, pode usar todos os atributos que existen para unha transacción real. Isto permite obter máis detalles na previsión. Por exemplo, pode introducir detalles sobre cantidades, traballadores, artigos ou propiedades da liña.         | Cando introduce os detalles do orzamento, só pode usar cantidades, categorías e actividades.                    |
| **Seguranza**              | A previsión baséase nas transaccións que introduce nos formularios de previsión e non implica ningún mecanismo de control de procesos. Calquera traballador que teña permisos para un formulario de previsión pode revisar a información sen aprobación.                                        | O orzamento utiliza o sistema de fluxo de traballo, que habilita a xestión de cambios e lle permite gardar un historial das revisións.         |
| **Tipos de entrada**           | As entradas de transaccións de previsión baséanse no número de unidades e nos custos e prezos unitarios de venda.  | Os detalles do orzamento baséanse en cantidades, que se dividen entre custos e ingresos.                                          |
| **Modelos de previsión**       | Debido a que cada previsión debe estar asociada a un modelo, pode crear varios modelos de previsión e tamén configurar submodelos.           | O orzamento do proxecto limita os modelos de previsión que se utilizan para o orzamento. Menos modelos de previsión poden axudar a aumentar a coherencia nas proxeccións.                           |
| **Excesos de custos**         | Só pode permitir ou non permitir a entrada de transaccións que causarán un exceso de custos.   | O orzamento de proxectos ofrece opcións de control adicionais para os usuarios. Pode permitir avisos e excesos.                    |
| **Control**               | O control da previsión realízase mediante a redución da previsión. Os importes reais réstanse dos saldos previstos das transaccións sen ningún rexistro de auditoría. Isto pode facer máis difícil rastrexar onde se produciron as transaccións reais.                   | No control do orzamento do proxecto, as cantidades reais réstanse das cantidades do orzamento restante. Isto permite un rexistro de auditoría máis claro.                                   |

## <a name="project-forecasts"></a>Previsións de proxectos
Cando usa as previsións de proxectos, pode introducir transaccións de previsión en formularios de previsión para cada tipo de transacción. Todos os atributos dispoñibles para unha transacción real pódense usar para unha transacción de previsión, por exemplo, rendibilidade de liña, atributos de liña, traballadores ou descricións. Tamén pode proxectar canto tempo despois de incorrer nun custo facturará a un cliente. 

As transaccións de previsións de proxectos baséanse en unidades e cantidades. 

Debe asociar cada previsión de proxecto a un modelo de previsión. Cando introduce unha transacción de previsión, suxírese automaticamente un modelo de previsión. O modelo de previsión actúa como contedor para as transaccións de previsión. 

Pode designar modelos de previsión como submodelos para un modelo. Isto permítelle predicir por rexión, período de tempo ou departamento. Pode copiar as transaccións previstas nun modelo para crear un novo modelo e tamén pode transferir as transaccións ao libro maior xeral. Debido a que existe unha relación individual entre unha previsión e un modelo, cada modelo de previsión constitúe un orzamento separado para un proxecto. 

Os modelos de previsión poden usar a redución de previsión como mecanismo de control para proxectos. Na redución da previsión, as transaccións reais reducen os saldos das transaccións de previsión. Non obstante, debido a que a redución de previsión aplícase ao proxecto máis alto da xerarquía, ofrece unha visión limitada dos cambios na previsión. Por exemplo, se un traballador está asociado a un subproxecto, as transaccións reais do traballador contabilízanse no proxecto principal. Isto pode dificultar o rastrexo dos cambios, porque non pode determinar facilmente que transacción en que subproxecto provocou unha redución do importe da previsión. Polo tanto, é unha boa idea crear unha copia dun modelo de previsión para usar na redución de previsión. A seguir, pode empregar informes para ver o previsto inicialmente. 

Pode revisar, copiar, eliminar ou transferir as previsións de proxectos a un orzamento de libro maior xeral. Non obstante, non hai control de procesos. Calquera traballador que teña permiso para un formulario de previsión pode facer revisións sen revisar.

-   **Revisar** - Pode revisar unha transacción de previsión nos mesmos formularios onde se realizaron as entradas orixinais.
-   **Copiar ou eliminar** - Cando copia transaccións de previsión, copia as liñas de transacción dun modelo de previsión a outro modelo de previsión. Cando elimina unha previsión, elimina as transaccións de previsión dun modelo de previsión. Para limitar as transaccións de previsión que se copian ou eliminan, seleccione tipos e datas de transacción específicos. Isto permítelle copiar ou eliminar só partes específicas dunha previsión.
-   **Transferir** - Cando transfire unha previsión de proxecto a un orzamento de libro maior xeral, transfire as transaccións de previsión dun modelo de previsión a un orzamento de libro maior xeral. Pode sobrescribir as transaccións transferidas previamente no orzamento do libro maior xeral ao que transfira a previsión do seu proxecto.

## <a name="project-budgets"></a>Orzamentos de proxectos
O orzamento de proxectos é un método máis sinxelo que a previsión, aínda que se integra cos modelos de previsión. Utiliza un formulario de entrada único para obter detalles e revisións do orzamento orixinal e permite proxeccións baseadas só na cantidade, categoría ou actividade. 

No orzamento do proxecto, todos os orzamentos e revisións orixinais deben enviarse a un fluxo de traballo do proxecto para a súa aprobación. Os fluxos de traballo ofrecen un maior control sobre o proceso e crean un rexistro do historial de cambios. 

O orzamento de proxectos aseméllase ao orzamento de libro maior xeral, pero é máis rápido e fácil de configurar. Moitas das opcións do orzamento de libro maior xeral, como secuencias numéricas ou moeda, non teñen por que configurarse por separado para os proxectos.

Os orzamentos de proxectos asócianse automaticamente a dous modelos de previsión, un para o orzamento orixinal e outro para o orzamento restante. Polo tanto, os informes baseados en modelos de previsión poden empregar datos de orzamento. Cando se compromete un orzamento de proxecto, o sistema crea transaccións de previsión baseadas nos modelos asociados, que se usan con fins de realización de informes e control.

## <a name="forecast-models"></a>Modelos de previsión
Os modelos de previsión teñen unha xerarquía de capa única. Isto significa que unha previsión de proxecto debe asociarse a un modelo de previsión.

Se usa a previsión de proxectos, pode identificar modelos como submodelos. Despois pode crear previsións departamento, período de tempo ou rexión Por exemplo, pode crear un modelo de previsión para un ano e despois crear submodelos para as previsións rexionais do nordeste, sueste, noroeste e suroeste que envíen os xefes rexionais. Ao seleccionar diferentes opcións nos informes dispoñibles, pode ver información por predición total ou por submodelo.





[!INCLUDE[footer-include](../includes/footer-banner.md)]