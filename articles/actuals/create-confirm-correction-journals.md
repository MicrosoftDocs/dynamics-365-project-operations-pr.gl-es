---
title: Crear e confirmar diarios de corrección
description: Este tema fornece información sobre como crear e confirmar un diario de corrección.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: f12cdba286a9e29e2c4eb4041effbe779cba65f3562684d625b21bc3bae809d6
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986714"
---
# <a name="create-and-confirm-correction-journals"></a>Crear e confirmar diarios de corrección

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

De cando en vez pode introducirse unha entrada de tempo ou gasto incorrectamente. Por exemplo, un consultor pode seleccionar a data incorrecta ao crear unha entrada de tempo ou pode traspor os números ao ingresar un gasto. Se un consultor non pode realizar as actualizacións das entradas enviadas, un administrador pode corrixir directamente a entrada para un proxecto.

Para completar os procedementos neste tema, necesitará permisos de administrador.

## <a name="correct-approved-time-entries"></a>Corrixir as entradas de tempo aprobadas     

Realice os seguintes pasos para corrixir as entradas de tempo individuais ou múltiples para un proxecto.

1. Na zona **Vendas**, seleccione **Transaccións** e logo seleccione **Tempo aprobado**. 

2. Na lista **Tempo aprobado**, localice e seleccione unha ou varias entradas de tempo aprobadas para corrixir. Pode usar o filtro para localizar entradas relacionadas. Por exemplo, pode filtrar un ID de proxecto e seleccionar todas as entradas de tempo aprobadas con ese ID de proxecto.

3. Seleccione **Corrixir entradas**. Créase automaticamente un novo diario de corrección, co tipo asignado **Corrección de tempo**. As entradas que seleccionou engádense ao diario. 

4. Na páxina **Novo diario**, introduza unha **Descrición** do diario de corrección e, a seguir, seleccione o separador **Correccións de entradas de tempo**.  

5. Na sección **Novos valores para entradas de tempo**, actualice os campos coa información correcta segundo sexa necesario. Por exemplo, pode cambiar o proxecto asignado ou o recurso reservable.

6. Seleccione **Previsualización**. Na caixa de diálogo, seleccione **Aceptar**. No separador **Liñas de diario**, pode ver unha lista dos datos reais orixinais relacionados coas entradas de tempo seleccionadas que foron invertidas e as liñas correspondentes corrixidas que se crearon. Se hai que facer correccións adicionais, repita os pasos 5 e 6. 

> [!NOTE]
> Todos os datos reais corrixidos terán os mesmos valores que seleccionou na sección **Novos valores das entradas de tempo**.

7. Se as correccións aparecen como se espera, seleccione **Confirmar**. Na caixa de diálogo, seleccione **Aceptar**.

8. Volva á zona **Vendas**, seleccione **Proxectos** e, a seguir, abra o proxecto para o que acaba de actualizar as entradas de tempo. 

9. Na páxina **Proxectos**, no separador **Datos reais**, vexa os cambios que fixo. 

> [!NOTE]
> Se o separador **Datos reais** non é visible, seleccione **Relacionado** > **Datos reais**.  

10. Na lista **Vista asociada de datos reais**, pode ver que as entradas de tempo orixinais que foron invertidas aínda están na lista, do mesmo xeito que as entradas de tempo corrixidas correspondentes. 

Por exemplo, na seguinte gráfica, hai dúas partidas cunha cantidade de 8,00 que teñen débitos na columna Importe. Ademais, hai dúas partidas cunha cantidade de -8,00 que amosan importes cobrados na columna Importe. Estas correccións poñen a cantidade en cero.

 
## <a name="correct-approved-expense-entries"></a>Corrixir as entradas de gasto aprobadas

Realice os seguintes pasos para corrixir unha ou varias entradas de gasto. 

1. Na zona **Vendas**, no panel de navegación esquerdo, baixo **Transaccións**, seleccione **Gastos aprobados**.

2. Na lista **Gastos aprobados**, seleccione o proxecto que desexa corrixir e logo seleccione **Corrixir entradas**. Crearase automaticamente un novo diario de corrección, co tipo asignado de **Corrección de gasto**. 

3. Na páxina **Novo diario**, introduza unha **Descrición** para a corrección, e no separador **Corrección de gasto**, na sección **Novos valores para gastos**, seleccione os campos de datos que desexa corrixir para as liñas de gasto seleccionadas. Por exemplo, pode atribuír o gasto a outro **Proxecto** ou corrixir **Categoría de gasto**, **Data de gasto** ou **Recurso reservable**.

4. Seleccione **Previsualización**. Na caixa de diálogo, seleccione **Aceptar**. 

5. Verifique as correccións no separador **Liñas de diario**. Pode ver unha lista dos datos reais orixinais relacionados coas entradas de gasto seleccionadas que foron invertidas e as liñas correspondentes corrixidas que se crearon.

6. Se os valores corrixidos son os esperados, seleccione **Confirmar**. Na caixa de diálogo, seleccione **Aceptar.** Se os valores non se amosan como se espera, seleccione **Cancelar** para volver á lista **Gastos aprobados**. Repita os pasos do 2 ao 5. 

> [!NOTE]
> Os datos reais corrixidos terán os mesmos valores que seleccionou na sección **Novos valores dos gastos**.

7. Despois de confirmar o diario de correccións, desprácese ata o proxecto ou proxectos que actualizou para ver os seus cambios.  

8. Na páxina do proxecto, no separador **Datos reais**, revise a **Visualización asociada dos datos reais**. Aparecerán as entradas orixinais e as entradas corrixidas. O seguinte gráfico mostra os importes orixinais das entradas de gastos e os correspondentes importes corrixidos das entradas de gastos. 




[!INCLUDE[footer-include](../includes/footer-banner.md)]