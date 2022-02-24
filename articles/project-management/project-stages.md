---
title: Fases do proxecto
description: Este tema ofrece información sobre as fases do proxecto dispoñibles en Microsoft Dynamics Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: aa3d692a46165b01eafbd7619578cead8dd912d6
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127471"
---
# <a name="project-stages"></a>Fases do proxecto

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

As fases do proxecto están deseñadas para reflectir o estado do proxecto a medida que progresa. Pódense utilizar as personalizacións para actualizar automaticamente as fases con fluxos de proceso de negocio, Power Automate ou extensións de complementos.

No fluxo do proceso de negocio por defecto defínense as seguintes etapas:

- Nova
- Oferta
- Plan
- Entregar
- Completado
- Pechar 

## <a name="new"></a>Nova

Ao crear un proxecto, a fase do proxecto defínese como **Novo**. Se o proxecto se creou a partir dun modelo, pode que teña datos de programación, estimación e equipo. Se non, é un esquema do proxecto e deben introducirse os compoñentes restantes.

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

