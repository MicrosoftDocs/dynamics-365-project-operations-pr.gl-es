---
title: Crear e confirmar diarios de corrección
description: Este tema fornece información sobre como crear e confirmar un diario de corrección.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: c15db854e3d130150ad7afc707a126b37c57f62d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582801"
---
# <a name="create-and-confirm-correction-journals"></a>Crear e confirmar diarios de corrección

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

En ocasións, é posible que se introduza incorrectamente unha entrada de tempo ou gasto. Por exemplo, un consultor pode seleccionar a data incorrecta cando crea unha entrada de tempo ou pode seleccionar o proxecto incorrecto cando introduce un gasto. Se un consultor non pode actualizar as entradas enviadas, un administrador back-end pode corrixir directamente os datos reais dun proxecto.

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

 
## <a name="correct-approved-expense-entries"></a>Corrixir as entradas de gasto aprobadas

Realice os seguintes pasos para corrixir unha ou varias entradas de gasto. 

1. Na zona **Vendas**, no panel de navegación esquerdo, baixo **Transaccións**, seleccione **Gastos aprobados**.

2. Na lista **Gastos aprobados**, seleccione o proxecto que desexa corrixir e logo seleccione **Corrixir entradas**. Crearase automaticamente un novo diario de corrección, co tipo asignado de **Corrección de gasto**. 

3. Na páxina **Novo diario**, introduza unha **Descrición** para a corrección, e no separador **Corrección de gasto**, na sección **Novos valores para gastos**, seleccione os campos de datos que desexa corrixir para as liñas de gasto seleccionadas. Por exemplo, pode atribuír o gasto a outro **Proxecto** ou corrixir **Categoría de gasto**, **Data de gasto** ou **Recurso reservable**.

4. Seleccione **Previsualización**. Na caixa de diálogo, seleccione **Aceptar**. 

5. Verifique as correccións no separador **Liñas de diario**. Pode ver unha lista dos datos reais orixinais relacionados coas entradas de gasto seleccionadas que foron invertidas e as liñas correspondentes corrixidas que se crearon.

6. Se os valores corrixidos son os esperados, seleccione **Confirmar**. Na caixa de diálogo, seleccione **Aceptar.** Se os valores non se amosan como se espera, seleccione **Cancelar** para volver á lista **Gastos aprobados**. Repita os pasos do 2 ao 5. 

7. Despois de confirmar o diario de correccións, volve ao proxecto ou proxectos que actualizou para ver os cambios.

8. Na páxina do proxecto, na **Reais** ficha, revisa o **Vista asociada real** lista. Aparecerán as entradas orixinais e as entradas corrixidas.


## <a name="correct-approved-material-usage-logs"></a>Corrixir os rexistros de uso do material aprobado

Complete os seguintes pasos para corrixir unha ou máis entradas do rexistro de uso de material.

1. No **Vendas** área, no panel de navegación esquerdo, debaixo **Transaccións**, seleccione **Reais**.

2. No **Reais** lista, use filtros de columna para seleccionar **Material** clase de transacción, para que só se mostren os datos reais dos materiais. Use outros filtros de columna para limitar aínda máis os datos reais que se mostran. Despois de atopar o conxunto desexado de datos reais, seleccione os reais e, a continuación, seleccione **Entradas correctas**. Créase automaticamente un novo diario de correccións e o **Corrección material** se asigna o tipo.

3. No **Novo Xornal** páxina, na **Descrición** campo, introduza unha descrición para a corrección. Despois, no **Corrección material** ficha, na **Novos valores para os materiais** sección, seleccione os campos de datos para corrixir para as liñas de material seleccionadas. Por exemplo, pode asignar o material a outro proxecto ou corrixir o produto, a data do material ou o subcontrato.

4. Seleccione **Previsualización**. A continuación, no cadro de diálogo, seleccione **Ok**.

5. No **Liñas do xornal** ficha, verifique as correccións. Podes ver unha lista dos reais orixinais que están relacionados coas entradas de materiais seleccionadas que foron invertidas e as liñas correspondentes corrixidas que foron creadas.

6. Se os valores corrixidos son os esperados, seleccione **Confirmar**. A continuación, no cadro de diálogo, seleccione **Ok**. Se os valores non son os esperados, seleccione **Cancelar** para volver ao **Reais** lista. A continuación, repita os pasos do 2 ao 5.

7. Despois de confirmar o diario de correccións, volve ao proxecto ou proxectos que actualizou para ver os cambios.

8. Na páxina do proxecto, na **Reais** ficha, revisa o **Vista asociada real** lista. Aparecerán as entradas orixinais e as entradas corrixidas.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
