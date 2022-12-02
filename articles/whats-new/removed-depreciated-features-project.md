---
title: Funcionalidades eliminadas ou obsoletas en Dynamics 365 Project Operations
description: Este artigo describe as funcionalidades que se eliminaron ou que están previstas para eliminar de Dynamics 365 Project Operations.
author: sigitac
ms.date: 03/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: f0fbaed028db11d8fb1551d304a40543faf35b0d
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028327"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-project-operations"></a>Funcionalidades eliminadas ou obsoletas en Dynamics 365 Project Operations

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento, despregamento de Lite - de acordo a facturación proforma e Project Operations para situacións baseadas en produción/con fornecemento_

Este artigo describe as funcionalidades que se eliminaron ou que están previstas para eliminar de Dynamics 365 Project Operations.

- Unha funcionalidade *eliminada* xa non está dispoñible no produto.
- Unha funcionalidade *obsoleta* non está en desenvolvemento activo e pode eliminarse nunha futura actualización.

Esta lista está destinada a axudarlle a considerar estas eliminacións e obsolescencias para a súa propia planificación.

> [!NOTE]
> Pódese atopar información detallada sobre obxectos en aplicacións de finanzas e operacións nos [**Informes técnicos de referencia**](/dynamics/s-e/global/axtechrefrep_61). Pode comparar as diferentes versións destes informes para coñecer os obxectos que cambiaron ou se eliminaron en cada versión das aplicacións de finanzas e operacións.

## <a name="features-removed-or-deprecated-in-the-project-operations-march-2022-release"></a>Funcionalidades eliminadas ou obsoletas en Project Operations versión de marzo de 2022

### <a name="project-management-and-accounting-always-create-adjustment-transaction-parameter"></a>Parámetro de xestión e contabilidade de proxectos "Crear sempre transacción de axuste"

| &nbsp; | &nbsp; |
|--------|--------|
| **Motivo da obsolescencia/eliminación** | As transaccións de axuste son necesarias para fins de auditoría. Despois de quedar obsoleto, este parámetro ocultarase. O sistema sempre creará transaccións de axuste, tal e como o fai actualmente cando o parámetro está configurado en **Si**. |
| **Substituído por outra funcionalidade?** | No |
| **Áreas de produtos afectadas** | Aplicación |
| **Opción de despregamento** | Project Operations para situacións baseadas en produción/con fornecemento |
| **Estado** | Obsoleto: O 1 de marzo de 2023, ocultaremos o parámetro e cambiaremos o comportamento do sistema para que se creen sempre transaccións de axuste. |

### <a name="project-management-and-accounting-use-adjustment-date-as-new-project-date-parameter"></a>Parámetro "Usar data de axuste como nova data do proxecto" de Xestión e contabilidade de proxectos

| &nbsp; | &nbsp; |
|--------|--------|
| **Motivo da obsolescencia/eliminación** | Este parámetro utilizouse orixinalmente para permitir axustes cando se pechaba un período fiscal. Non obstante, xa non é necesario, porque a data contable da transacción pódese cambiar á primeira data do período aberto, se está configurada. Non se debe cambiar a data do proxecto, porque representa a data na que se produciu a transacción. |
| **Substituído por outra funcionalidade?** | No |
| **Áreas de produtos afectadas** | Aplicación |
| **Opción de despregamento** | Project Operations para situacións baseadas en produción/con fornecemento |
| **Estado** | Obsoleto: O 1 de marzo de 2023, ocultaremos o parámetro e cambiaremos o comportamento do sistema para que a data do proxecto nunca se cambie nos axustes. |

### <a name="resource-request-workflow-in-project-operations-for-stockedproduction-based-scenarios"></a>Fluxo de traballo de solicitude de recursos en Project Operations para situacións baseadas en produción/con fornecemento

| &nbsp; | &nbsp; |
|--------|--------|
| **Motivo da obsolescencia/eliminación** | Obsoleto debido ao baixo uso e ás limitacións do volume de transaccións. |
| **Substituído por outra funcionalidade?** | No |
| **Áreas de produtos afectadas** | Aplicación |
| **Opción de despregamento** | Project Operations para situacións baseadas en produción/con fornecemento |
| **Estado** | Obsoleto: O 1 de marzo de 2023 desactivaremos a opción de solicitar recursos para o proxecto mediante o fluxo de traballo. |

### <a name="project-invoice-proposal-page-without-header-and-lines-views"></a>Páxina de proposta de factura do proxecto sen vistas de cabeceira e liñas

| &nbsp; | &nbsp; |
|--------|--------|
| **Motivo da obsolescencia/eliminación** | Obsoleto debido ás melloras na páxina que se introduciron xunto coa tecla de función **Usar os formularios de proposta de factura e diario de factura do proxecto coa vista de Cabeceira e Liñas**. |
| **Substituído por outra funcionalidade?** | Si |
| **Áreas de produtos afectadas** | Aplicación |
| **Opción de despregamento** | Project Operations para situacións baseadas en produción/con fornecemento; Project Operations para situacións baseadas en recursos/sen fornecemento |
| **Estado** | Obsoleto: O 1 de marzo de 2023 desactivaremos a páxina anterior (antiga) e activaremos a tecla de función **Usar os formularios de proposta de factura e diario de factura do proxecto coa vista de Cabeceira e Liñas** por defecto. |

## <a name="features-removed-or-deprecated-in-the-project-operations-december-2021-release"></a>Funcionalidades eliminadas ou obsoletas en Project Operations versión de decembro de 2021

### <a name="collaboration-workspaces"></a>Áreas de traballo de colaboración

[Crear ou vincular unha área de traballo de colaboración (proxecto)](/dynamicsax-2012/appuser-itpro/create-or-link-to-a-collaboration-workspace-project)

| &nbsp; | &nbsp; |
|--------|--------|
| **Motivo da obsolescencia/eliminación** | Obsoleto debido ao pouco uso. Os clientes que usan Project Operations para situacióins baseadas en recursos/sen fornecemento poden aproveitar [Colaboración con Office Groups](../project-management/collaboration-groups.md). |
| **Substituído por outra funcionalidade?** | No |
| **Áreas de produtos afectadas** | Aplicación  |
| **Opción de despregamento** | Project Operations para situacións baseadas en produción/con fornecemento |
| **Estado** | Obsoleto: O 1 de decembro de 2022 temos previsto deixar de admitir as áreas de traballo de colaboración. |
