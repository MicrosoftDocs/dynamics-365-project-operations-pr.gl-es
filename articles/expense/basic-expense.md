---
title: Entrada de gasto (lite)
description: Este tema ofrece información sobre como traballar coa entrada de gastos nun despregamento lite.
author: stsporen
manager: AnnBe
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d87094882751f0751a8d9d539fa4cdcfc6b7b0d7
ms.sourcegitcommit: 16c442258ba24c79076cf5877a0f3c1f51a85f61
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 11/20/2020
ms.locfileid: "4590944"
---
# <a name="expense-entry-lite"></a>Entrada de gasto (lite)

_**Aplícase a:** Despregamento de Lite - acordo para facturación proforma_

A xestión básica ou lite de gastos é a capacidade de rexistrar gastos simples. Pode rexistrar os gastos contra un proxecto e logo o responsable de aprobacións do proxecto revisaraos e aprobaraos.

Para obter máis información sobre as capacidades de gasto en Dynamics 365 Project Operations, consulte [Visión xeral dos gastos](expense-overview.md).

## <a name="capture-a-basic-expense"></a>Capta un gasto básico

Pode capturar os seus gastos para poder envialos ao responsables de aprobacións.

1. Vaia a **Gastos** e seleccione **Novo**.
2. Na páxina **Novo gasto**, introduza a información do gasto requirida e seleccione **Gardar**.

## <a name="submit-a-basic-expense"></a>Enviar un gasto básico

Despois de rematar de capturar todos os seus gastos e cando estea listo para facer que os aproben, debe envialos.

1. Vaia a **Gastos** e seleccione un gasto. Ou seleccione todos os gastos empregando a caixa de verificación da cabeceira.
2. Seleccione **Enviar**. O sistema procesa as entradas seleccionadas e logo crea solicitudes de aprobación de gastos.

## <a name="add-an-attachment"></a>Engadir un anexo

É posible que deba proporcionar ao responsable de aprobación documentación adicional sobre o seu gasto. Pode anexar un recibo na liña de tempo da entrada de gasto. Seleccione **Editar** e na sección **Liña de tempo** seleccione a icona de clip para anexar o recibo.

## <a name="recall-a-basic-expense"></a>Recuperar un gasto básico

Cando envíe un gasto por erro, pode recuperalo. O tempo necesario para recuperar unha entrada de gasto depende da súa fase de aprobación.  Se o responsable de aprobacións aínda non aprobou a entrada, a recuperación pode producirse inmediatamente. Non obstante, se a entrada xa foi aprobada, solicítaselle ao responsable de aprobacións que aprobe a recuperación e reverta as transaccións.

1. Vaia a **Gastos** e, a seguir, na lista de gastos, seleccione o gasto que desexa recuperar.
2. Seleccione **Recuperar**. Se aínda non se aprobou a entrada de gasto, o sistema o recupera inmediatamente. Se a entrada de gasto xa se aprobou, créase unha solicitude de recuperación para notificar ao responsable de aprobacións de que desexa reverter o gasto. A seguir, o responsable de aprobacións confirmará que se pode facer a reversión e devolverase a entrada.

## <a name="delete-a-basic-expense"></a>Eliminar un gasto básico

Pódense eliminar os gastos que aínda non se enviaron. Para eliminar un gasto xa enviado, primeiro debe recuperalo.

## <a name="see-also"></a>Consulte tamén

- [Visión xeral das aprobacións](../approvals/approvals-overview.md)
