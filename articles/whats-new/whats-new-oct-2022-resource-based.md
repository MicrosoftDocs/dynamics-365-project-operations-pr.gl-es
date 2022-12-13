---
title: Novidades de outubro de 2022 - Project Operations para situacións baseadas en recursos/sen fornecemento
description: Este artigo ofrece información sobre as actualizacións de calidade dispoñibles na versión de outubro de 2022 de Microsoft Dynamics 365 Project Operations para escenarios baseados en recursos ou non almacenados.
author: ramagadu
ms.date: 11/17/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 392a12d6954c2390e5bad8e8e36cf58b7a1d0749
ms.sourcegitcommit: 1f162707ac342343fb5390fb9ae335e4cea4f3f2
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806730"
---
# <a name="whats-new-october-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades de outubro de 2022 - Project Operations para situacións baseadas en recursos/sen fornecemento

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Este artigo aplícase aos seguintes compoñentes e versións de Microsoft Dynamics 365 Project Operations:

- Project Operations nun ambiente de Dataverse versión 4.57.0.176
- Xestión e contabilidade de proxectos nun ambiente de aplicacións de Dynamics 365 Finance versión 10.0.30

## <a name="features-included-in-this-release"></a>Funcionalidades incluídas nesta versión

| Área de funcionalidades | Nome da funcionalidade | Máis información |
| --- | --- | --- |
| Planificación e rastrexo de proxectos | **Programación externa de operacións do proxecto**<br>O modo de programación externa permite aos clientes crear, actualizar e eliminar de forma nativa entidades relacionadas coas estruturas de descomposición do traballo (WBS) mediante as API nativas Dataverse , sen os límites actuais que aplica Project for the Web. . | [Programación externa](/dynamics365/project-operations/project-management/external-scheduling) |
| Despregamento e configuración | <p>**Permitir aos clientes escoller o tipo de implantación**<br>As actualizacións dirixidas ao produto (PDU) de Project Operations utilízanse para instalar automaticamente a solución de escritura dual de Project Operations cando se instalan solucións de orquestración e núcleo de escritura dual no ambiente.</p><p>Esta función introduce un novo parámetro **Comportamento de actualización da solución** nos parámetros do proxecto. Cando este parámetro se define en **Só Lite**, os PUD xa non instalarán automaticamente a solución de escritura dual de Project Operations, aínda que no contorno se instalen solucións de orquestración e núcleo de escritura dual. . Este comportamento beneficiará aos clientes que planean utilizar solucións de escritura dual para integrar pedidos de venda en aplicacións de finanzas e operacións, pero que queiran usar Project Operations nun modo Lite (é dicir, sen integración nas aplicacións de finanzas e operacións).</p> | |
| Facturación e prezos | <p>**Conversión de moeda para transaccións de venda sen facturar de gastos en contornos integrados**<br>Para os clientes que usan Project Operations integradas con aplicacións de finanzas e operacións (é dicir, no tipo de implantación de recursos/non abastecidos), os tipos de cambio adoitan dominarse nas aplicacións de finanzas e operacións. However, if an expense category should be priced by using the "at cost" or "markup over cost" price calculation method when the customer is billed, the exchange rate that's used to calculate sales amount uses the exchange rates in Dataverse, not the exchange rates from finance and operations apps.</p><p>Esta función introduce un novo parámetro **Comportamento de conversión de moeda** nos parámetros do proxecto. Cando este parámetro se define como **Ampliado con reserva**, os importes das vendas non facturadas nas transaccións de gastos calcúlanse utilizando os tipos de cambio das aplicacións de finanzas e operacións.</p> | |

## <a name="project-operations-dual-write-maps-updates"></a>Actualizacións de mapas de escrita dual en Project Operations

Non hai actualizacións para mapas de escrita dual de Project Operations nesta versión. Para obter unha lista actual e versións dos mapas de escrita dual de Project Operations, consulte [Versións de mapa de escrita dual de Project Operations](../environment/resource-dual-write-maps.md).

Execute sempre a última versión do mapa no seu ambiente e active todos os mapas de táboa relacionados mentres actualiza a súa solución de Project Operations Dataverse e a versión da solución de Finance. É posible que algunhas funcionalidades e capacidades non funcionen correctamente se a última versión do mapa non está activada. Pode ver a versión activa do mapa na columna **Versión** columna na páxina **Escrita dual**. Para activar unha nova versión do mapa, seleccione **Versións do mapa de táboa**, seleccione a versión máis recente e logo garde a versión seleccionada. Se personalizou un mapa de táboa listo para usar, aplique de novo os cambios. Para obter máis información, consulte [Xestión do ciclo de vida da aplicación](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se ten algún problema cando inicie o mapa, siga as instrucións da sección [Problema de falta de columnas da táboa nos mapas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) da guía de resolución de problemas de escrita dual.

## <a name="quality-updates"></a>Actualizacións de calidade

### <a name="project-operations-on-dataverse"></a>Project Operations en Dataverse

| Área de funcionalidades | Número de referencia | Actualización de calidade |
| --- | --- | --- |
| Facturación e prezos | 2316317 | O sistema permite crear facturas que non teñan transaccións cobrables. |
| Facturación e prezos | 2737300 | Valida a dispoñibilidade do campo **Cliente** antes de acceder ao formulario. |
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
| Planificación e rastrexo de proxectos | 2957840 | Non se poden gardar tarefas e non se poden engadir columnas á páxina **Tarefas** en Operacións integradas do proxecto. |
| Xestión de recursos | 2751560 | Unidades organizativas preferidas inconsistentes no requisito de recursos. |
| Subcontratación | 2853245 | A coincidencia dos reais da liña de factura do provedor non actualiza o estado de verificación se unha liña de contrato xa está ligada á liña de factura do provedor. |
| Subcontratación | 2907231 | A fase de proceso das facturas de provedores non pode avanzar. |
| Tempo e gasto | 2867363 | Os rexistros non caen da vista Ausencias/Vacacións para aprobación cando están en cola para a súa aprobación. |
| Tempo e gasto | 2894405 | TESA: o directorio POC non utilizado está causando problemas de cumprimento. |

### <a name="project-management-and-accounting-in-finance"></a>Xestión e contabilidade de proxectos en Finance

Para obter información sobre as correccións incluídas nesta actualización, inicie sesión en Microsoft Dynamics Lifecycle Services (LCS) e vexa o [artigo de KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468).
