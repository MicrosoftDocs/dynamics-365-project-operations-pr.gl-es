---
title: Moeda
description: Este tema ofrece información sobre como engadir e eliminar tipos de moeda en Project Operations.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: a20b4518954cce755555b95cc7fd9e6efb1a7322
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591816"
---
# <a name="currency"></a>Moeda

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_



As divisas determinan os prezos dos produtos no catálogo de produtos e o custo das transaccións, como os pedidos de vendas. Se os seus clientes se atopan en diferentes localizacións xeográficas, engada as súas moedas para xestionar as súas transaccións. Engada as moedas máis adecuadas para as súas necesidades empresariais actuais e futuras  

> [!NOTE]
> Se o seu ambiente é un ambiente de Common Data Service, está no centro de administración de Power Platform e selecciona a páxina **Moedas** (**Ambientes** > [seleccionar ambiente] > **Configuración** > **Empresa** > **Moedas**), a páxina estará en branco. Isto é porque a configuración dunha moeda non é compatible con ambientes de Common Data Service

## <a name="add-a-currency"></a>Engadir unha moeda  
Antes de comezar este procedemento, verifique que o seu rol de seguranza inclúe permisos de administrador do sistema. 

1. No centro de administración de Power Platform, seleccione un ambiente. 
2. Seleccione **Configuración** > **Empresa**.
3. Escolla **Moedas**.  
4. Seleccione **Nova**.  
5. Encha a información necesaria.  


   |          Campo          |                                                                                                                                                                                                                                                                                                                                                                            Descrición                                                                                                                                                                                                                                                                                                                                                                            |
   |-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |    **Tipo de moeda**    | - **Sistema**: Seleccione esta opción se desexa utilizar moedas dispoñibles en aplicacións baseadas en modelos en Dynamics 365. Para buscar unha moeda, seleccione **Buscar**. Cando selecciona un código de moeda **Nome de Moeda** e **Símbolo Monetario** engádense automaticamente para a moeda seleccionada.<br />- **Personalizado**: Seleccione esta opción se desexa engadir unha moeda que non está dispoñible en aplicacións baseadas en modelos en Dynamics 365. Neste caso, introduza manualmente os valores de **Código de Moeda**, **Precisión de Moeda**, **Nome de Moeda**, **Símbolo Monetario**, e **Conversión de Moeda**. |
   |    **Código de moeda**    |                                                                                                                                                                                                                                                                                                                                            Formulario breve para a moeda. Por exemplo, **USD** para dólares de Estados Unidos.                                                                                                                                                                                                                                                                                                                                            |
   | **Precisión de moeda**  |                                                                                                                                                                                  Introduza o número de decimais que desexa usar para a moeda.  Pode engadir un valor de entre 0 e 4. **Nota:** Se definiu un valor de precisión na caixa de diálogo **Configuración do Sistema**, ese valor aparecerá aquí.                                                                                                                                                                                  |
   |    **Nome da moeda**    |                                                                                                                                                                                                                                         Se seleccionou un código de moeda da lista de moedas dispoñibles en aplicacións baseadas en modelos en Dynamics 365, o nome de moeda para o código de seleccionados móstrase aquí. Se seleccionou **Personalizado** como o tipo de moeda, introduza o nome da moeda.                                                                                                                                                                                                                                          |
   |   **Símbolo monetario**   |                                                                                                                                                                                                                                                                      Se seleccionou un código de moeda da lista de moedas dispoñibles, o símbolo da moeda seleccionada móstrase aquí. Se seleccionou **Personalizado** como o tipo de moeda, introduza o símbolo da moeda nova.                                                                                                                                                                                                                                                                       |
   | **Conversión de moeda** |                                                                                                                                                                                                                                     Escriba o valor da moeda seleccionada en relación cun dólar de Estados Unidos. Este é o importe en que a moeda seleccionada converte á moeda base. **Importante:** Asegúrese de que actualiza este valor coa frecuencia necesaria para evitar cálculos inexacto nas súas transaccións.                                                                                                                                                                                                                                      |


6. Cando finalice, na barra de comandos, seleccione **Gardar** ou **Gardar e pechar**.  

   > [!TIP]
   >  Para editar unha moeda, seleccione a moeda e, a seguir, introduza ou seleccione os novos valores.  

## <a name="delete-a-currency"></a>Eliminar unha moeda  

1. No centro de administración de Power Platform, seleccione un ambiente. 
2. Seleccione **Configuración** > **Empresa**.
3. Escolla **Moedas**.  
4. Na lista de moedas mostradas, seleccione a moeda para eliminar.  
5. Seleccione **Eliminar**.  
6. Confirme a eliminación.  

> [!IMPORTANT]
>  Non pode eliminar as moedas que están a ser utilizadas por outros rexistros, só pode desactivalas. A desactivación dos rexistros de moeda non elimina a información monetaria almacenada nos rexistros existentes, tales como oportunidades ou pedidos. No entanto, non poderá seleccionar a moeda desactivada para novas transaccións.  


[!INCLUDE[footer-include](../includes/footer-banner.md)]