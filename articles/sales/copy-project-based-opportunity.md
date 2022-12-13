---
title: Copiar oportunidades do proxecto
description: Este artigo ofrece información sobre como copiar oportunidades baseadas en proxecto en Project Operations.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0fe29918e14a944de7277639f752ad53513a7589
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 12/05/2022
ms.locfileid: "9826126"
---
# <a name="copy-project-opportunities"></a>Copiar oportunidades do proxecto

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_


As oportunidades do proxecto pódense copiar facilmente para crear novas oportunidades de proxecto. 

1. Vaia á páxina de lista **Oportunidades de proxecto** e seleccione unha oportunidade da lista. Ou abra a páxina de detalles dunha oportunidade específica. 
2. En calquera das dúas páxinas, seleccione **Copiar**. Abrirase unha páxina de diálogo que contén a seguinte información de campo. Dependendo dos valores seleccionados neste diálogo, o proceso de copia pode cambiar.

    | **Campo** | **Descrición** | **Impacto descendente** |
    | --- | --- | --- |
    | Tema | Introduza o tema relevante da oportunidade de destino. Cando se abra o diálogo, o sistema configurarao co tema da oportunidade de destino con **copia** anexa a el. | Non hai ningún impacto descendente para este campo. |
    | Conta | Fai referencia á empresa ou ao rexistro da conta do cliente. Cando se abra o diálogo, o sistema configurarao na conta da oportunidade de orixe. | Este campo é o cliente principal na oportunidade. |
    | Unidade de contratación | A unidade organizativa que é responsable da entrega dos proxectos asociados a esta oferta. Cando se abra o diálogo, o sistema configurarao na unidade de contratación da oportunidade de orixe. | A unidade contratante é a división da empresa que executa os proxectos despois de pechar a oferta. Cada unidade de contratación ten unha moeda e esta moeda úsase para informar dos custos estimados e reais incorridos durante o proxecto. |
    | Moeda | A moeda na que se realizan as transaccións da oferta. Cando se abra a páxina de diálogo, o sistema configurarao na moeda da oportunidade de orixe. | A moeda úsase para predefinir unha lista de prezos e crear estimacións financeiras na oferta. Finalmente, a moeda úsase para facturar ao cliente cando se gaña a oferta. |
    | Copiar prezos | Un valor Si/Non que indica se se deben copiar os prezos da oportunidade da oportunidade de orixe. | Se se selecciona **Si**, as listas de prezos cópianse desde a oportunidade de orixe ata a oportunidade de destino. Se se selecciona **Non**, as listas de prezos predefínense en función das últimas listas de prezos que se configuraron. |

3. Seleccione **Aceptar**. O sistema crea unha copia da oportunidade de proxecto en función dos parámetros seleccionados e ábrese a nova oportunidade de proxecto.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
