---
title: Tipos de fases de proxecto
description: Este artigo ofrece información sobre as fases do proxecto.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 06/19/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 8d772acce152b08c7986739ac557818e6f97d0fe
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919058"
---
# <a name="project-stage-types"></a>Tipos de fases de proxecto 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

As fases do proxecto están deseñadas para reflectir o estado do proxecto a medida que progresa. Pódense utilizar as personalizacións para actualizar automaticamente as fases con fluxos de proceso de negocio, Power Automate ou extensións de complementos.

No BPF por defecto defínense as seguintes etapas:

- Nova
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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
