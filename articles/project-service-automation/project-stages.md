---
title: Fases do proxecto
description: Neste tema se proporciona información sobre as fases do proxecto.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 983c25a0-ed21-4151-a109-b385a88285fa
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 70aa057e127df7ba925e84f5d056a06a4cc8833e
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751360"
---
# <a name="project-stages"></a>Fases do proxecto 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

As fases do proxecto actualízanse para reflectir o estado do proxecto a medida que progresa. O fluxo do proceso de negocio por defecto actualiza automaticamente algunhas fases do proxecto, mentres que outras son actualizadas manualmente polo xestor de proxectos. 

No BPF por defecto defínense as seguintes etapas:

- Novo
- Oferta
- Planificar
- Entregar
- Completar
- Pechar 

## <a name="new"></a>Novo

Ao crear un proxecto, a fase do proxecto defínese como **Novo**. Se o proxecto se creou a partir dun modelo, pode que teña datos de programación, estimación e equipo. Se non, é só un esquema do proxecto e deben introducirse os compoñentes restantes.

## <a name="quote"></a>Oferta

Cando asocia un proxecto a unha oferta ou cando crea un proxecto a partir dunha oferta, a fase de proxecto está definida en **Oferta**, e as datas de inicio e fin estimadas tamén se actualizan. Mentres o proxecto está na fase de **Oferta**, o separador **Vendas** da páxina **Entidade do proxecto** mostra detalles da oferta.

## <a name="plan"></a>Planificar

Cando gaña unha oferta asociada a un proxecto, e o proxecto se move á fase **Contrato**, a fase do proxecto actualízase a **Planificar**. Mentres o proxecto está na fase **Planificar**, a páxina **Entidade do proxecto** mostra detalles do contrato.

## <a name="deliver"></a>Entregar

Cando o plan do proxecto estea finalizado e vostede estea listo para iniciar o proxecto, o xestor de proxectos debería actualizar a fase do proxecto a **Entregar** para demostrar que o proxecto comezou.

## <a name="complete"></a>Finalizar 

Cando o traballo para o proxecto estea rematado, o xestor de proxectos pode actualizar a fase a **Finalizar**. Ao actualizar a fase do proxecto a **Finalizar**, o xestor de proxectos indica que o traballo está finalizado ao 100 por cento, pero que o proxecto se mantén aberto para que se poida rexistrar calquera entrada de tempo ou gasto pendente.

## <a name="close"></a>Pechar

Cando todas as transaccións do proxecto estean rexistradas, o xestor de proxectos pode actualizar a fase a **Pechar**. Nese momento, non se poden rexistrar transaccións e o proxecto configúrase como só de lectura.
