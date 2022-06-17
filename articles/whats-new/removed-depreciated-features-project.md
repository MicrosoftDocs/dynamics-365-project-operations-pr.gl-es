---
title: Funcións eliminadas ou obsoletas en Dynamics 365 Project Operations
description: Este artigo describe funcións que se eliminaron ou que se planearon eliminar de Dynamics 365 Project Operations.
author: sigitac
ms.date: 03/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: df9d8a40fa853e72416e64846bf59748815048be
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921484"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-project-operations"></a>Funcións eliminadas ou obsoletas en Dynamics 365 Project Operations

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento, despregamento de Lite - de acordo a facturación proforma e Project Operations para situacións baseadas en produción/con fornecemento_

Este artigo describe funcións que se eliminaron ou que se planearon eliminar de Dynamics 365 Project Operations.

- Unha funcionalidade *eliminada* xa non está dispoñible no produto.
- Unha funcionalidade *obsoleta* non está en desenvolvemento activo e pode eliminarse nunha futura actualización.

Esta lista está destinada a axudarlle a considerar estas eliminacións e obsolescencias para a súa propia planificación.

> [!NOTE]
> Pódese atopar información detallada sobre obxectos nas aplicacións de Finanzas e Operacións na páxina [**Informes técnicos de referencia**](/dynamics/s-e/global/axtechrefrep_61). Podes comparar as diferentes versións destes informes para coñecer os obxectos que cambiaron ou se eliminaron en cada versión das aplicacións Finance and Operations.

## <a name="features-removed-or-deprecated-in-the-project-operations-march-2022-release"></a>Funcións eliminadas ou obsoletas na versión Project Operations de marzo de 2022

### <a name="project-management-and-accounting-always-create-adjustment-transaction-parameter"></a>Parámetro de xestión e contabilidade de proxectos "Crear sempre transacción de axuste".

| &nbsp; | &nbsp; |
|--------|--------|
| **Motivo da obsolescencia/eliminación** | As transaccións de axuste son necesarias para fins de auditoría. Despois da desuso, este parámetro ocultarase. O sistema sempre creará transaccións de axuste, tal e como o fai actualmente cando o parámetro está configurado **Si**. |
| **Substituído por outra funcionalidade?** | No |
| **Áreas de produtos afectadas** | Aplicación |
| **Opción de despregamento** | Operacións do proxecto para escenarios de produción/stock |
| **Estado** | Obsoleto: ata o 1 de marzo de 2023, ocultaremos o parámetro e cambiaremos o comportamento do sistema para que se creen sempre transaccións de axuste. |

### <a name="project-management-and-accounting-use-adjustment-date-as-new-project-date-parameter"></a>Xestión de proxectos e contabilidade Parámetro "Usar data de axuste como nova data do proxecto".

| &nbsp; | &nbsp; |
|--------|--------|
| **Motivo da obsolescencia/eliminación** | Este parámetro utilizouse orixinalmente para permitir axustes cando se pechaba un período fiscal. Non obstante, xa non é necesario, porque a data contable da transacción pódese cambiar á primeira data do período aberto, se está configurada. Non se debe cambiar a data do proxecto, porque representa a data na que se produciu a transacción. |
| **Substituído por outra funcionalidade?** | No |
| **Áreas de produtos afectadas** | Aplicación |
| **Opción de despregamento** | Operacións do proxecto para escenarios de produción/stock |
| **Estado** | Obsoleto: ata o 1 de marzo de 2023, ocultaremos o parámetro e cambiaremos o comportamento do sistema para que nunca se cambie a data do proxecto nos axustes. |

### <a name="resource-request-workflow-in-project-operations-for-stockedproduction-based-scenarios"></a>Fluxo de traballo de solicitude de recursos en Project Operations para escenarios abastecidos/baseados na produción

| &nbsp; | &nbsp; |
|--------|--------|
| **Motivo da obsolescencia/eliminación** | Obsoleto debido ao baixo uso e ás limitacións do volume de transaccións. |
| **Substituído por outra funcionalidade?** | No |
| **Áreas de produtos afectadas** | Aplicación |
| **Opción de despregamento** | Operacións do proxecto para escenarios de produción/stock |
| **Estado** | Obsoleto: antes do 1 de marzo de 2023, desactivaremos a opción de solicitar recursos para o proxecto mediante o fluxo de traballo. |

### <a name="project-invoice-proposal-page-without-header-and-lines-views"></a>Páxina de proposta de factura do proxecto sen vistas de cabeceira e liñas

| &nbsp; | &nbsp; |
|--------|--------|
| **Motivo da obsolescencia/eliminación** | Obsoleto debido ás melloras na páxina que se introduciu xunto co **Use os formularios de proposta de factura do proxecto e diario de facturas coa vista Cabeceira e Liñas** tecla de función. |
| **Substituído por outra funcionalidade?** | Si |
| **Áreas de produtos afectadas** | Aplicación |
| **Opción de despregamento** | Operacións do proxecto para escenarios de produción/abastecemento; Operacións do proxecto para escenarios de recursos/non abastecidos |
| **Estado** | Obsoleto: antes do 1 de marzo de 2023, desactivaremos a páxina anterior (antigua) e activaremos o **Use os formularios de proposta de factura do proxecto e diario de facturas coa vista Cabeceira e Liñas** tecla de función por defecto. |

## <a name="features-removed-or-deprecated-in-the-project-operations-december-2021-release"></a>Funcións eliminadas ou obsoletas na versión de decembro de 2021 de Project Operations

### <a name="collaboration-workspaces"></a>Espazos de traballo de colaboración

[Crear ou vincular un espazo de traballo de colaboración (proxecto)](/dynamicsax-2012/appuser-itpro/create-or-link-to-a-collaboration-workspace-project)

| &nbsp; | &nbsp; |
|--------|--------|
| **Motivo da obsolescencia/eliminación** | Obsoleto debido ao pouco uso. Os clientes que usan Project Operations para escenarios de recursos/non abastecidos poden aproveitar [Colaboración con Grupos Office](../project-management/collaboration-groups.md). |
| **Substituído por outra funcionalidade?** | No |
| **Áreas de produtos afectadas** | Aplicación  |
| **Opción de despregamento** | Operacións do proxecto para escenarios de produción/stock |
| **Estado** | Obsoleto: para o 1 de decembro de 2022, pensamos deixar de admitir os espazos de traballo de colaboración. |
