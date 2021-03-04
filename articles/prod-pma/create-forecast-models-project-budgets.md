---
title: Crear modelos de previsión para orzamentos de proxecto
description: Este tema describe como crear un modelo de previsión para os orzamentos restantes.
author: Yowelle
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 32a436d240f5535ff15f8bc3b8ba9be2d1d4da17
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076268"
---
# <a name="create-forecast-models-for-project-budgets"></a>Crear modelos de previsión para orzamentos de proxecto 

[!include [banner](../includes/banner.md)]

Este tema describe como crear un modelo de previsión para os orzamentos restantes. Un proxecto suxeito a control orzamentario utiliza dous tipos de orzamentos: o orixinal e o restante. Cando cree un orzamento do proxecto, debe especificar os modelos de previsión de orzamento orixinais e restantes que se crearon na páxina **Modelos de previsión**. Os orzamentos do proxecto baseados nos modelos especificados créanse cando confirma o orzamento do proxecto.

> [!NOTE]
> Un modelo de previsión que se usa para o control do orzamento non pode ter un submodelo nin ser usado como submodelo.

1. Seleccione **Xestión e contabilidade de proxectos** > **Configuración** > **Previsións**  > **Modelos de previsión**.
2. Seleccione **Novo** para crear un novo modelo de previsión e, a seguir, escriba un número de identificación e un nome de modelo para o novo modelo. 
3. Configure a opción **Detido** en **Si** para evitar cambios nas liñas de previsión do modelo de previsión. 
4. Se as liñas de previsión coas que se asocia o modelo deberían xerar previsións de fluxo de efectivo no libro maior, configure **Incluír nas previsións de fluxo de caixa** en **Si.** 
5. Para usar a data do proxecto como data de factura, configure **Previsión da data da factura** en **Si**. 
6. No campo **Tipo de orzamento** , seleccione un dos seguintes tipos de modelos:

   - **Orzamento orixinal** : Use os importes do orzamento orixinal confirmados cando se crea e aproba o orzamento inicial.
   - **Orzamento restante** : Use os importes do orzamento restante durante a vida do proxecto. Os saldos deste modelo de previsión redúcense por transaccións reais e aumentan ou diminúen por revisións orzamentarias.
   - **Transferir** : Use os importes do orzamento transferidos para o proxecto. A transferencia é un proceso opcional que se pode executar para transferir cantidades orzamentarias non utilizadas dun ano fiscal a outro.

7. Defina as seguintes opcións segundo sexa necesario:

   - Active **Previsión de data de factura** para usar a data do proxecto como data da factura.
   - Active **Previsión con WIP** para predicir en función do traballo en curso (WIP) e logo seleccionar o tipo de WIP. 
   - Pode manter o valor predefinido **Tipo de orzamento** como **Ningún** ou introduza un novo tipo. O tipo de orzamento non se pode cambiar despois de cambiar un rexistro.     
    > [!NOTE]
    > Se cambia o tipo de orzamento predefinido, as demais opcións non estarán dispoñibles para actualizacións e non pode volver usar este modelo de previsión. 
   


 



[!INCLUDE[footer-include](../includes/footer-banner.md)]