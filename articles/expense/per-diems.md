---
title: Dietas
description: Este tema ofrece información sobre as regras das dietas que se usan na xestión de gastos.
author: suvaidya
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 192164094231fa2da47806cd9c2ccaba8321c83a1464fc8724fa0d0a7618660f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986399"
---
# <a name="per-diems"></a>Dietas

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_


A dieta é un subsidio que se paga a un traballador que viaxa por traballo. En xestión de gastos, pode crear regras de dietas para varias situacións de viaxe. As taxas das dietas poden basearse na época do ano, na localización da viaxe ou en ambas. Cando crea unha regra de dietas, pode especificar que se reterá unha porcentaxe da taxa de dietas se un traballador recibe comidas ou servizos de cortesía. Tamén pode establecer un número mínimo e máximo de horas que a taxa de dietas se pode aplicar ás viaxes dun traballador.

## <a name="configuration"></a>Configuración 

1. Para engadir localizacións de dietas, vaia a **Configuración** > **Cálculos e códigos** > **Localizacións de dietas**.
2. Para cada unha das localizacións engadidas anteriormente, seleccione unha taxa de dietas e a moeda que sexa válida entre unha data específica de inicio e fin para hotel, comidas e outros gastos. Os tipos e as moedas diarios configúranse en **Configuración** > **Cálculos e códigos** > **Dietas**.
3. Na páxina **Localizacións de dietas**, configure os niveis de taxa de dietas. Os niveis de taxa de dietas permítenlle definir a porcentaxe de división dun subsidio diario para gastos de hotel, comida e outros. 
4. Para especificar a redución da porcentaxe das comidas para o almorzo, o xantar ou a cea, actualice os campos da páxina **Parámetros de xestión de gastos** no separador **Dietas**. 
    
## <a name="submit-expenses-using-per-diem"></a>Enviar os gastos usando as dietas
Para enviar gastos utilizando dietas, use a categoría de gasto **Dietas** cando cree un informe de gastos. Introduza a **Dietas desde a data**, **Dietas ata a data** e **Localización de dietas**. A cantidade calcularase en función das taxas de dietas para a localización seleccionada e a redución de comidas calcularase en función dos niveis de taxas de dietas.


[!INCLUDE[footer-include](../includes/footer-banner.md)]