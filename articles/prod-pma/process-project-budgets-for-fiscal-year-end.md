---
title: Transferir orzamentos de proxecto ao finalizar o ano fiscal
description: Este artigo ofrece información sobre como transferir cantidades de orzamento restantes a exercicios futuros e crear detalles do rexistro de orzamento.
author: Yowelle
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 74b2831a19688636f5c4863036adf7043c80d49829737b56c131abb6998d6cb3
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007369"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a>Transferir orzamentos de proxecto ao finalizar o ano fiscal

[!include [banner](../includes/banner.md)]

Ao traballar nun proxecto de varios anos, pode que teña un orzamento restante ao final do ano fiscal. Pode transferir as cantidades orzamentarias restantes a un ano futuro e crear detalles do rexistro orzamentario para as cantidades nas contas do libro maior asociadas. Antes de transferir os importes restantes, revise e analice os importes restantes do orzamento.

## <a name="review-and-analyze-remaining-budget-amounts"></a>Revisar e analizar os importes do orzamento restantes

Complete os seguintes pasos para revisar os importes do orzamento de fin de ano para os proxectos, pero non transfira os importes.

1. Vaia a **Xestión e contabilidade de proxectos** > **Periódico** > **Orzamentos** > **Transferir orzamentos**. 
2. Na páxina **Proceso de transferencia do orzamento do proxecto**, no separador **Opcións de fin de ano**, verifique que a opción **Transferir os importes restantes do orzamento do proxecto** non está activada.
3. No separador **Parámetros**, no campo **Ano do orzamento do proxecto**, seleccione o ano fiscal para o que desexa ver o importe do orzamento restante. 
4. No campo **Ano fiscal de apertura**, seleccione o ano fiscal para o que desexa ver o importe do orzamento restante. 
5. No campo **A partir do modelo de previsión**, seleccione **Orzamento restante**. 
6. Para incluír proxectos que cumpran os criterios seleccionados e que non teñan orzamento restante, seleccione **Mostrar cero restante**.  
7. No separador **Seleccionar orzamentos**, seleccione **Recuperar todos os orzamentos** para cargar todos os orzamentos que coincidan cos criterios seleccionados e logo seleccione **Procesar**. 
8. Para deseñar unha consulta de base de datos que cargue un conxunto específico de orzamentos no panel, seleccione **Recuperar os orzamentos seleccionados**.

Para obter máis información sobre unha liña específica no panel, seleccione a liña e logo seleccione **Ver detalles do orzamento** ou **Ver contas**.

## <a name="carry-forward-remaining-budget-amounts"></a>Transferir os importes do orzamento restantes 

Cando procesa os importes do orzamento restantes, pode crear transaccións no libro maior para as cantidades que está transferindo. Para crear transaccións de libro maior, complete os pasos da sección [Transferir importes de orzamento e crear transaccións de libro maior](#carry-forward). 

> [!NOTE]
> As cantidades orzamentarias transfírense ao modelo de previsión seleccionado na páxina **Modelos de previsión** páxina como modelo de previsión de transferencia.  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a>Transferir importes orzamentarios e crear transaccións de libro maior

1.  Seleccione **Xestión e contabilidade de proxectos** > **Periódico** > **Orzamentos** > **Transferir orzamentos**. 
2. Na páxina **Proceso de transferencia orzamento do proxecto**, seleccione **Fin de ano** e, a seguir, active **Transferir os importes restantes do orzamento do proxecto** e **Crea entradas de rexistro de orzamento no libro maior**. 
3. No separador **Parámetros**, no grupo de campos **Parámetros do proxecto**, seleccione o seguinte:

   - **Ano do orzamento do proxecto**: Seleccione o ano fiscal para o que desexa ver os importes do orzamento restante. 
   - **Beneficios e perdas**: Cree transaccións de resultados no libro maior. 
   -  **WIP**: Cree transaccións de traballo en curso (WIP) no libro maior.
   -  **Nómina**: Cree transaccións de asignación de nóminas no libro maior. 

5. No grupo de campos **Libro maior**, forneza a seguinte información: 

   - No campo **Ano fiscal de apertura**, seleccione o ano fiscal ao que desexa transferir os importes do orzamento restante para os proxectos. O valor predefinido é un ano despois do valor no campo **Ano do orzamento do proxecto**.
   -  No campo **Período de transferencia**, seleccione o período para o que desexa crear os detalles do rexistro de orzamento no libro maior. Este é normalmente o primeiro período do ano fiscal de apertura.

6. No grupo de campos **Copiar de/a**, forneza a seguinte información:

   - No campo **A partir do modelo de previsión**, seleccione o modelo de previsión do orzamento do proxecto asociado cos importes orzamentarios restantes que desexa transferir para os proxectos. 
   - No campo **Ao modelo de orzamento de libro maior**, seleccione o modelo de orzamento do libro maior asociado aos importes orzamentarios que desexa transferir ao libro maior. 
   -  Seleccione **Transferir moeda de vendas** para usar a moeda de vendas do proxecto para as transaccións de libro maior que se crean ao transferir os importes orzamentarios dos proxectos. Cando a opción non está seleccionada, as transaccións utilizan a moeda de contabilidade. 
   -  Seleccione **Mostrar cero restante** para incluír proxectos que non teñan cantidades orzamentarias restantes, pero que cumpran os outros criterios que seleccione nos proxectos que se amosan no panel inferior.

7. No separador **Seleccionar orzamentos**, seleccione **Recuperar todos os orzamentos** para cargar todos os orzamentos que coincidan cos criterios seleccionados. Se prefire deseñar unha consulta de base de datos que cargue un conxunto específico de orzamentos do proxecto no panel, seleccione **Recuperar os orzamentos seleccionados**.
8. Para cada proxecto que desexe procesar, seleccione a opción ao comezo da liña do proxecto.

    > [!TIP]
    > Para seleccionar todos ou a maioría dos proxectos, seleccione a marca de verificación na esquina superior esquerda. Para excluír o procesamento de calquera proxecto, quite a marca de verificación dese proxecto.

9. Para transferir os importes do orzamento restantes para os proxectos seleccionados ao ano fiscal seleccionado e crear detalles do rexistro de orzamento no libro maior, seleccione **Procesar**.

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a>Transferir importes orzamentarios sen crear transaccións de libro maior

1. Vaia a **Xestión e contabilidade de proxectos** > **Periódico** > **Orzamentos** > **Transferir orzamentos**.
2. Na páxina **Proceso de transferencia do orzamento do proxecto**, no separador **Opcións de fin de ano**, seleccione **Transferir os importes restantes do orzamento do proxecto**.
3. No grupo **Parámetros**, no campo **Ano do orzamento do proxecto**, seleccione o ano fiscal para o que desexa ver os importes do orzamento restante.
4. No grupo **Copiar de/a**, forneza a seguinte información:

   - No campo **A partir do modelo de previsión**, seleccione o modelo de previsión do orzamento do proxecto asociado aos importes orzamentarios restantes que desexa transferir para os proxectos. 
   - Seleccione **Mostrar cero restante** ara incluír proxectos que non teñan importes de orzamento restante, pero que cumpran os outros criterios que seleccionou.
   - No grupo **Seleccionar orzamentos**, seleccione **Recuperar todos os orzamentos** para cargar todos os orzamentos que coincidan cos criterios seleccionados. Para deseñar unha consulta de base de datos que cargue un conxunto específico de orzamentos de proxecto no panel, seleccione **Recuperar os orzamentos seleccionados**.

5. Para cada proxecto que desexe procesar, seleccione a opción ao comezo da liña do proxecto. 
6. Seleccione **Proceso** para transferir os importes do orzamento restantes para os proxectos seleccionados ao ano fiscal seleccionado.



[!INCLUDE[footer-include](../includes/footer-banner.md)]