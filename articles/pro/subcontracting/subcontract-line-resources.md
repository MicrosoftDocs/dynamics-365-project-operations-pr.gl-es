---
title: Recursos da liña de subcontrato
description: Este tema explica como especificar os recursos dedicados que o provedor proporciona para unha liña de subcontrato específica para tempo.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4a929b985a51ab49d3e34ce4a5c277af4c05c216
ms.sourcegitcommit: d507a75a19c992a9421e4f3605162a2faa84a445
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 09/27/2021
ms.locfileid: "7558455"
---
# <a name="subcontract-line-resources"></a>Recursos da liña de subcontrato

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

En Dynamics 365 Project Operations, un fornecedor pode especificar os recursos que se utilizarán para subministrar a capacidade de recursos que se está a mercar na liña de subcontrato para tempo.

## <a name="create-subcontract-line-resources"></a>Crear recursos da liña de subcontrato

Para crear recursos da liña de subcontrato, complete os seguintes pasos.

1. No panel de navegación, seleccione **Subcontratos** e abra o subcontrato co que desexa traballar.
2. Abra a liña de subcontrato do tempo no que desexa especificar os recursos do fornecedor.
3. No separador **Recursos da liña de subcontrato**, na subgrade, seleccione **+ Novo recurso da liña de subcontrato**.
4. Na páxina **Novo recurso de liña de subcontrato**, introduza a información requirida e logo seleccione **Gardar e pechar**.

A seguinte táboa explica os campos do recurso de liña de subcontrato.

| Campo | Descripción | Impacto funcional |
| ----- | ----------- | ----------------- |
| Recurso reservable | Seleccione un recurso reservable do tipo **Traballador por contrato** que desexa empregar como recurso na liña de subcontrato.| Se non creou un recurso reservable para o traballador contratado, deixe este campo baleiro. Crearase un recurso reservable cando garde o rexistro.  |
| Contacto | Pode crear o seu recurso de liña de subcontrato a partir dun contacto existente. Use a busca para ver a lista de contactos activos no sistema. Seleccione un contacto para o fornecedor deste subcontrato. Se o contacto que seleccionou non é un contacto válido para o fornecedor do subcontrato, non se gardará o rexistro de recursos da liña de subcontrato.| Se non hai ningún recurso reservable para o contacto seleccionado, o sistema crea un recurso reservable para o contacto seleccionado antes de crear o recurso de liña de subcontrato. |
| Usuario | Pode crear un recurso de liña de subcontrato seleccionando un usuario activo. Use a busca para ver a lista de usuarios activos no sistema.| Se non hai ningún recurso reservable para o usuario seleccionado, o sistema crea un recurso reservable para o usuario seleccionado antes de que se cree o recurso de liña de subcontrato. |
| Data de inicio | A data na que comezará a tarefa do traballador subcontratado.| Se se reserva este recurso para un período anterior a este rango de datas, producirase unha advertencia. |
| Data de finalización | A data na que finaliza a tarefa do traballador subcontratado.| Se se reserva este recurso para un período posterior a este rango de datas, producirase unha advertencia. |
| Esforzo | O número total de horas de esforzo que o traballador contratado pasará nesta liña de subcontrato.| Se se reserva este recurso máis alá do esforzo asignado neste subcontrato, producirase un aviso. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
