---
title: Xestionar estimacións de ingresos
description: Este tema ofrece información sobre como traballar con estimacións de ingresos para proxectos.
author: sigitac
ms.date: 11/04/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e3cbaff18d8bd4d6f6a7577bba25b3e843b1757e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013845"
---
# <a name="manage-revenue-estimates"></a>Xestionar estimacións de ingresos

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Pode crear, calcular, contabilizar, reverter ou eliminar estimacións de ingresos. Pode facelo manualmente ou mediante un proceso periódico. Este tema ofrece información sobre como traballar con estimacións de ingresos para proxectos.

### <a name="manage-revenue-estimates-manually"></a>Xestionar estimacións de ingresos manualmente

No proxecto de estimación de ingresos a prezo fixo ou na páxina **Consulta de estimación** (**Xestión e contabilidade de proxectos** > **Informes e consultas** > **Consultas e informes de estimacións**), seleccione **Estimacións**.

### <a name="manage-revenue-estimates-using-a-periodic-process"></a>Xestionar estimacións de ingresos mediante un proceso periódico

Vaia a **Xestión e contabilidade de proxectos** > **Periódico** > **Estimacións** e seleccione o proceso correspondente.

## <a name="create-a-revenue-estimate"></a>Crear unha estimación de ingresos

Complete os seguintes pasos para crear unha estimación de ingresos. 

1. Vaia a **Xestión e contabilidade de proxectos** > **Periódico** > **Estimacións**.
2. Seleccione **Nova**. Na páxina **Creación de estimación**, seleccione os seguintes parámetros:

   - **Código do período**: Este código determina a frecuencia coa que se publican as estimacións.
   - **Data da estimación**: Data na que se procesa a estimación.
   - **Continua**: Marque esta caixa de verificación para crear estimacións só se se contabilizaron estimacións no período anterior ou se a estimación é a primeira estimación que se creou. Se non se selecciona, créanse estimacións aínda que non se contabilizasen no período anterior.
   - **Método de custo para completar**: Defina como estimar o traballo restante do proxecto. Para obter máis información, consulte [Métodos de custo para completar](cost-complete-methods.md).
   - **Método de finalización**: Seleccione un método de finalización entre as seguintes opcións:
     - **Automático**: A porcentaxe de finalización calcúlase automaticamente e baséase nas liñas de custo incluídas no cálculo. O modelo de custo define as liñas de custo incluídas.
     - **Manual**: A porcentaxe de finalización é igual á porcentaxe de finalización da última estimación. Despois de crear a estimación, pode cambiar o **Cálculo manual** na páxina **Estimacións**.
     - **Do modelo de custo**: Unha combinación dos métodos automático e manual. Esta opción configúrase automaticamente ou manualmente, dependendo do valor predefinido no modelo de custo.
   - **Modelo de previsión**: Seleccione un modelo de previsión para a estimación.
   - **Imprimir lista de estimacións**: Crea e amosa unha lista de estimacións. A lista contén o estado da función actual. Pode imprimir calquera aviso sobre a estimación no informe. As seguintes condicións provocan que aparezan avisos na lista de estimacións:
     - Unha porcentaxe de finalización superior ao 100 por cento.
     - Unha porcentaxe de finalización inferior ao cero por cento.
     - Unha cantidade negativa na columna **Por completar**.
     - Unha estimación sen importe do contrato correspondente.
     - Unha estimación sen estimación de custo anexa.
   - **Mostrar Infolog**: Seleccione esta opción para recibir unha mensaxe que conteña información sobre os proxectos estimados que se procesaron cando se executou o traballo.


## <a name="post-wip-or-accruals"></a>Contabilizar WIP ou acumulacións

Despois de avaliar as estimacións, estas se manteñen, diminúen ou aumentan. Despois pode publicar o WIP cando traballes co principio de avaliación **Contrato rematado** ou contabilizar as acumulacións cando traballe co principio de avaliación **Porcentaxe completada**.
  
O estado do período da estimación cambia de **Creado** a **Contabilizado**.

## <a name="reverse-wip-or-accruals"></a>Reverter WIP ou acumulacións

Use a opción de reverter para recoñecer o WIP ou as acumulacións xa contabilizados e logo cree estimacións para o período.

> [!NOTE]
> Para reverter un período que se atopa entre outros períodos, reverta os períodos de estimación necesarios e logo volva contabilizalos. Como todos os períodos posteriores dependen das estimacións do período anterior, non omita ningún período.

## <a name="eliminate-the-estimate-project-and-finish-the-project"></a>Eliminar o proxecto de estimación e finalizar o proxecto

O último paso no proceso de estimación é eliminar o proxecto de estimación e finalizar o proxecto de prezo fixo cando a porcentaxe de finalización alcance o 100 por cento.

Ocorre o seguinte cando executa a eliminación:

- Para un proxecto de prezo fixo cun contrato finalizado, os valores de WIP saen das contas de saldo e contabilízanse nas contas de resultados.
- Para un proxecto de prezo fixo cunha porcentaxe de finalización, as acumulacións elimínanse das contas de resultados.

A estimación cambia o estado a **Eliminado**.

> [!NOTE]
> En casos especiais, a porcentaxe pode estenderse máis alá do 100 por cento. Cando isto ocorre, reduza a porcentaxe de finalización empregando o **Establecer o custo para completar en cero** para chegar ao 100 por cento.

## <a name="reverse-elimination"></a>Reverter eliminación

1. Vaia a **Xestión e contabilidade de proxectos** > **Periódico** > **Estimacións** > **Reverter eliminación**. 
2. No panel de acción, no separador **Proceso**, no grupo **Manter**, seleccione **Estimación**. 
3. Seleccione **Reverter eliminación**.

Use esta páxina para reverter todas as eliminacións cunha data de estimación especificada e cun estado de estimación de **Eliminado**. O estado da transacción cambia despois de seleccionar os campos apropiados.

Isto tamén cambia automaticamente o estado do proxecto a **En proceso** se a fase do proxecto está configurada como finalizada. O estado da estimación do período do proxecto volve a **Contabilizado**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]