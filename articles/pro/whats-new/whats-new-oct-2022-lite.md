---
title: Novidades de outubro de 2022 - Despregamento de Project Operations lite
description: Este artigo ofrece información sobre as actualizacións de calidade dispoñibles na versión de outubro de 2022 da implantación de Microsoft Dynamics 365 Project Operations lite.
author: ramagadu
ms.date: 11/17/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: b6975e1f8645721fc03239b355b117eb664785f0
ms.sourcegitcommit: 1f162707ac342343fb5390fb9ae335e4cea4f3f2
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806733"
---
# <a name="whats-new-october-2022---project-operations-lite-deployment"></a>Novidades de outubro de 2022 - Despregamento de Project Operations lite

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

Este artigo aplícase aos seguintes compoñentes e versións de Microsoft Dynamics 365 Project Operations:

- Project Operations nun ambiente de Dataverse versión 4.57.0.176

## <a name="features-included-in-this-release"></a>Funcionalidades incluídas nesta versión

| Área de funcionalidades | Nome da funcionalidade | Máis información |
| --- | --- | --- |
| Planificación e rastrexo de proxectos | **Programación externa de operacións do proxecto**<br>O modo de programación externa permite aos clientes crear, actualizar e eliminar de forma nativa entidades relacionadas coas estruturas de descomposición do traballo (WBS) mediante as API nativas Dataverse , sen os límites actuais que aplica Project for the Web. . | [Programación externa](/dynamics365/project-operations/project-management/external-scheduling) |
| Despregamento e configuración | <p>**Permitir aos clientes escoller o tipo de implantación**<br>As actualizacións dirixidas ao produto (PDU) de Project Operations utilízanse para instalar automaticamente a solución de escritura dual de Project Operations cando se instalan solucións de orquestración e núcleo de escritura dual no ambiente.</p><p>Esta función introduce un novo parámetro **Comportamento de actualización da solución** nos parámetros do proxecto. Cando este parámetro se define en **Só Lite**, os PUD xa non instalarán automaticamente a solución de escritura dual de Project Operations, aínda que no contorno se instalen solucións de orquestración e núcleo de escritura dual. . Este comportamento beneficiará aos clientes que planean utilizar solucións de escritura dual para integrar pedidos de venda en aplicacións de finanzas e operacións, pero que queiran usar Project Operations nun modo Lite (é dicir, sen integración nas aplicacións de finanzas e operacións).</p> | |

## <a name="quality-updates"></a>Actualizacións de calidade

| Área de funcionalidades | Número de referencia | Actualización de calidade |
| --- | --- | --- |
| Facturación e prezos | 2316317 | O sistema permite crear facturas que non teñan transaccións cobrables. |
| Facturación e prezos | 2737300 | Valide a dispoñibilidade do campo do cliente antes de acceder ao formulario. |
| Facturación e prezos | 2744948 | Engade unha comprobación nula para o método de facturación. |
| Facturación e prezos | 2763515 | Controlador de erro de referencia nulo cando falta o contrato de venda da factura. |
| Facturación e prezos | 2844301 | Produciuse un erro na creación de facturas por lotes debido a un erro. |
| Facturación e prezos | 2845869 | Almacenamento incorrecto do Servizo de Organización. |
| Facturación e prezos | 2853729 | Os detalles do papel e do prezo actualízanse cando se modifica o tipo de facturación. |
| Facturación e prezos | 2940350 | Cando se fixen prezos reais, só se deben introducir automaticamente as listas de prezos activas. |
| Despregamento e configuración | 3001206 | A entidade msdyn\_ replaylogheader impide as actualizacións das organizacións de clientes. |
| Xestión de oportunidades | 2755582 | Control de excepcións de referencia nula no Asistente de regras de facturación dividida. |
| Xestión de oportunidades | 2761477 | Cando se utiliza a facturación dividida, a eliminación dun marco (encabezado) deixa os marcos orfos. |
| Xestión de oportunidades | 2767595 | Cando se abre un rexistro de uso de material no formulario principal, o recurso reservable para o rexistro cámbiase polo usuario que iniciou sesión actualmente. |
| Planificación e rastrexo de proxectos | 2790384 | O tempo de espera Pending OperationSet é demasiado curto. |
| Xestión de recursos | 2751560 | Unidades organizativas preferidas inconsistentes no requisito de recursos. |
| Subcontratación | 2907231 | A fase de proceso das facturas de provedores non pode avanzar. |
| Tempo e gasto | 2867363 | Os rexistros non caen da vista Ausencias/Vacacións para aprobación cando están en cola para a súa aprobación. |
| Tempo e gasto | 2894405 | TESA: o directorio POC non utilizado está causando problemas de cumprimento. |
