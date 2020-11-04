---
title: Copiar oportunidades baseadas en proxecto
description: Este tema ofrece información sobre como copiar oportunidades baseadas en proxecto en Project Operations.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 89f5a63581f36b30634bdd302a6d360d6b5e75bd
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076071"
---
# <a name="copy-project-based-opportunities"></a>Copiar oportunidades baseadas en proxecto

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_


As oportunidades do proxecto pódense copiar facilmente para crear novas oportunidades de proxecto. 

1. Vaia á páxina de lista **Oportunidades de proxecto** e seleccione unha oportunidade da lista. Ou abra a páxina de detalles dunha oportunidade específica. 
2. En calquera das dúas páxinas, seleccione **Copiar**. Abrirase unha páxina de diálogo que contén a seguinte información de campo. Dependendo dos valores seleccionados neste diálogo, o proceso de copia pode cambiar.

    | **Campo** | **Relevancia, finalidade e orientación** | **Impacto descendente** |
    | --- | --- | --- |
    | Tema | Introduza o tema relevante da oportunidade de destino. Cando se abra o diálogo, o sistema configurarao co tema da oportunidade de destino con **copia** anexa a el. | Non hai ningún impacto descendente para este campo. |
    | Conta | Fai referencia á empresa ou ao rexistro da conta do cliente. Cando se abra o diálogo, o sistema configurarao na conta da oportunidade de orixe. | Este campo é o cliente principal na oportunidade. |
    | Unidade de contratación | A unidade organizativa que é responsable da entrega dos proxectos asociados a esta oferta. Cando se abra o diálogo, o sistema configurarao na unidade de contratación da oportunidade de orixe. | A unidade contratante é a división da empresa que executa os proxectos despois de pechar a oferta. Cada unidade de contratación ten unha moeda e esta moeda úsase para informar dos custos estimados e reais incorridos durante o proxecto. |
    | Moeda | A moeda na que se realizan as transaccións da oferta. Cando se abra a páxina de diálogo, o sistema configurarao na moeda da oportunidade de orixe. | A moeda úsase para predefinir unha lista de prezos e crear estimacións financeiras na oferta. Finalmente, a moeda úsase para facturar ao cliente cando se gaña a oferta. |
    | Copiar prezos | Un valor Si/Non que indica se se deben copiar os prezos da oportunidade da oportunidade de orixe. | Se se selecciona **Si** , as listas de prezos cópianse desde a oportunidade de orixe ata a oportunidade de destino. Se se selecciona **Non** , as listas de prezos predefínense en función das últimas listas de prezos que se configuraron. |

3. Seleccione **Aceptar**. O sistema crea unha copia da oportunidade de proxecto en función dos parámetros seleccionados e ábrese a nova oportunidade de proxecto.