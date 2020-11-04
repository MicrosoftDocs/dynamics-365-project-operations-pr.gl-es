---
title: Correccións en masa de datos reais creadas por entradas aprobadas de tempo e gasto
description: Este tema explica como un administrador pode facer correccións sinxelas ou en masa ás entradas de tempo ou gasto aprobadas previamente se a facturación non está completa.
author: rumant
manager: AnnBe
ms.date: 04/02/2020
ms.topic: article
ms.service: dynamics-ax-applications
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
search.app:
- ProjectOperations
ms.openlocfilehash: 6d6c03cc74d47ca3ae7c2bd7d0aa0720bb2f3c01
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076308"
---
# <a name="bulk-corrections-of-actuals-created-by-approved-time-and-expense-entries"></a>Correccións en masa de datos reais creadas por entradas aprobadas de tempo e gasto

De cando en vez pode introducirse unha entrada de tempo ou gasto incorrectamente. Por exemplo, un consultor pode seleccionar a data incorrecta ao crear unha entrada de tempo ou pode traspor os números ao ingresar un gasto. Se un consultor non pode realizar as actualizacións das entradas enviadas, un administrador pode corrixir directamente a entrada para un proxecto.

Para completar os procedementos neste tema, necesitará permisos de administrador.

## <a name="correct-approved-time-entries"></a>Corrixir as entradas de tempo aprobadas     

Realice os seguintes pasos para corrixir as entradas de tempo individuais ou múltiples para un proxecto.

1. Na zona **Vendas** , seleccione **Transaccións** e logo seleccione **Tempo aprobado**. 

2. Na lista **Tempo aprobado** , localice e seleccione unha ou varias entradas de tempo aprobadas para corrixir. Pode usar o filtro para localizar entradas relacionadas. Por exemplo, pode filtrar un ID de proxecto e seleccionar todas as entradas de tempo aprobadas con ese ID de proxecto.

3. Seleccione **Corrixir entradas**. Créase automaticamente un novo diario de corrección, co tipo asignado **Corrección de tempo**. As entradas que seleccionou engádense ao diario. 

4. Na páxina **Novo diario** , introduza unha **Descrición** do diario de corrección e, a seguir, seleccione o separador **Correccións de entradas de tempo**.  
5. Na sección **Novos valores para entradas de tempo** , actualice os campos coa información correcta segundo sexa necesario. Por exemplo, pode cambiar o proxecto asignado ou o recurso reservable.

6. Seleccione **Previsualización**. Na caixa de diálogo, seleccione **Aceptar**. No separador **Liñas de diario** , pode ver unha lista dos datos reais orixinais relacionados coas entradas de tempo seleccionadas que foron invertidas e as liñas correspondentes corrixidas que se crearon. Se hai que facer correccións adicionais, repita os pasos 5 e 6. 

> [!NOTE]
> Todos os datos reais corrixidos terán os mesmos valores que seleccionou na sección **Novos valores das entradas de tempo**.

7. Se as correccións aparecen como se espera, seleccione **Confirmar**. Na caixa de diálogo, seleccione **Aceptar**.

8. Volva á zona **Vendas** , seleccione **Proxectos** e, a seguir, abra o proxecto para o que acaba de actualizar as entradas de tempo. 

9. Na páxina **Proxectos** , no separador **Datos reais** , vexa os cambios que fixo. 

> [!NOTE]
> Se o separador **Datos reais** non é visible, seleccione **Relacionado** > **Datos reais**.  

10. Na lista **Vista asociada de datos reais** , pode ver que as entradas de tempo orixinais que foron invertidas aínda están na lista, do mesmo xeito que as entradas de tempo corrixidas correspondentes. 

Por exemplo, na seguinte gráfica, hai dúas partidas cunha cantidade de 8,00 que teñen débitos na columna Importe. Ademais, hai dúas partidas cunha cantidade de -8,00 que amosan importes cobrados na columna Importe. Estas correccións poñen a cantidade en cero.

![Lista de visualización asociada dos datos reais](https://github.com/MicrosoftDocs/dynamics-365-customer-engagement-pr/blob/bulk-corrections-actuals-created-by-approved-time-expense-entries.md/time-actuals.png)
 
## <a name="correct-approved-expense-entries"></a>Corrixir as entradas de gasto aprobadas

Realice os seguintes pasos para corrixir unha ou varias entradas de gasto. 

1. Na zona **Vendas** , no panel de navegación esquerdo, baixo **Transaccións** , seleccione **Gastos aprobados**.

2. Na lista **Gastos aprobados** , seleccione o proxecto que desexa corrixir e logo seleccione **Corrixir entradas**. Crearase automaticamente un novo diario de corrección, co tipo asignado de **Corrección de gasto**. 

3. Na páxina **Novo diario** , introduza unha **Descrición** para a corrección, e no separador **Corrección de gasto** , na sección **Novos valores para gastos** , seleccione os campos de datos que desexa corrixir para as liñas de gasto seleccionadas. Por exemplo, pode atribuír o gasto a outro **Proxecto** ou corrixir **Categoría de gasto** , **Data de gasto** ou **Recurso reservable**.

4. Seleccione **Previsualización**. Na caixa de diálogo, seleccione **Aceptar**. 

5. Verifique as correccións no separador **Liñas de diario**. Pode ver unha lista dos datos reais orixinais relacionados coas entradas de gasto seleccionadas que foron invertidas e as liñas correspondentes corrixidas que se crearon.

6. Se os valores corrixidos son os esperados, seleccione **Confirmar**. Na caixa de diálogo, seleccione **Aceptar.** Se os valores non se amosan como se espera, seleccione **Cancelar** para volver á lista **Gastos aprobados**. Repita os pasos do 2 ao 5. 

> [!NOTE]
> Os datos reais corrixidos terán os mesmos valores que seleccionou na sección **Novos valores dos gastos**.

7. Despois de confirmar o diario de correccións, desprácese ata o proxecto ou proxectos que actualizou para ver os seus cambios.  

8. Na páxina do proxecto, no separador **Datos reais** , revise a **Visualización asociada dos datos reais**. Aparecerán as entradas orixinais e as entradas corrixidas. O seguinte gráfico mostra os importes orixinais das entradas de gastos e os correspondentes importes corrixidos das entradas de gastos. 

![Datos reais de gastos](https://user-images.githubusercontent.com/60806505/77122219-4cd52900-69fa-11ea-8349-ccd2ffebf640.png)
