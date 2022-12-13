---
title: Novidades de novembro de 2022 - Project Operations para situacións baseadas en recursos/sen fornecemento
description: Este artigo ofrece información sobre as actualizacións de calidade que están dispoñibles na versión de novembro de 2022 de Microsoft Dynamics 365 Project Operations para escenarios baseados en recursos ou non almacenados.
author: ryansandness
ms.date: 12/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: 509e303aeb0567627590fd89c6888b59a414c6f1
ms.sourcegitcommit: 952fcefe33de192ad48f4108c3adbe658fd7b94f
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831126"
---
# <a name="whats-new-november-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades de novembro de 2022 - Project Operations para situacións baseadas en recursos/sen fornecemento

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Este artigo aplícase aos seguintes compoñentes e versións de Microsoft Dynamics 365 Project Operations:

- Project Operations nun ambiente de Dataverse versión 4.58.0.119
- Xestión e contabilidade de proxectos nun ambiente de aplicacións de Dynamics 365 Finance versión 10.0.30

## <a name="project-operations-dual-write-maps-updates"></a>Actualizacións de mapas de escrita dual en Project Operations

Non hai actualizacións para mapas de escrita dual de Project Operations nesta versión. Para obter unha lista actual e versións dos mapas de escrita dual de Project Operations, consulte [Versións de mapa de escrita dual de Project Operations](../environment/resource-dual-write-maps.md).

Execute sempre a última versión do mapa no seu ambiente e active todos os mapas de táboa relacionados mentres actualiza a súa solución de Project Operations Dataverse solución e a versión da solución de Finance. É posible que algunhas funcionalidades e capacidades non funcionen correctamente se a última versión do mapa non está activada. Pode ver a versión activa do mapa na columna **Versión** columna na páxina **Escrita dual**. Para activar unha nova versión do mapa, seleccione **Versións do mapa de táboa**, seleccione a versión máis recente e logo garde a versión seleccionada. Se personalizou un mapa de táboa listo para usar, aplique de novo os cambios. Para obter máis información, consulte [Xestión do ciclo de vida da aplicación](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se ten algún problema cando inicie o mapa, siga as instrucións da sección [Problema de falta de columnas da táboa nos mapas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) da guía de resolución de problemas de escrita dual.

## <a name="quality-updates"></a>Actualizacións de calidade

### <a name="project-operations-on-dataverse"></a>Project Operations en Dataverse

| Área de funcionalidades | Número de referencia | Actualización de calidade |
| --- | --- | --- |
| Facturación e prezos | 2781818 | Erro de clave non atopada ao establecer o prezo predeterminado para o rexistro de uso do material. |
| Facturación e prezos | 2922373 | Non se pode ligar a liña de cotización ao proxecto que se pechou como cotización perdida. |
| Facturación e prezos | 2943206 | **O campo Liña de contrato**  da Entidade do proxecto debería ser opcional. |
| Facturación e prezos | 2953182 | Mellora a mensaxe de erro para as facturas de corrección.|
| Facturación e prezos | 2959500 | Non se pode ligar a liña de cotización a unha tarefa do proxecto que xa está asociada cunha cotización perdida.|
| Facturación e prezos | 2959560 | Recibiuse a mensaxe "Este cliente xa está no contrato do proxecto" ao pechar a cotización como gañada en determinadas localidades. |
| Facturación e prezos | 3031727 | As asignacións de recursos fallan e falta o campo obrigatorio 'msdyn_Company'. |
| Facturación e prezos | 3036905 | A empresa propietaria nunca se inicializa no ProjectTeamMember. |
| Xestión de oportunidades | 2763519 | Erro de referencia nula en EnsureProjectContractAllowsUpdates. |
| Xestión de oportunidades | 2783798 | Ao importar estimacións do proxecto na liña de cotización, faltan as descricións das tarefas para as estimacións de gastos e materiais.|
| Xestión de oportunidades | 2988635 | Mellora a descrición do mensaxe de erro ao eliminar o cliente na cotización. |
| Xestión de oportunidades | 3001191 | Non se puido crear unha cotización de Opportunity onde o método de facturación se especifica como nulo. |
| Actualizar | 3012324 | Produciuse un erro na conversión do proxecto nun proxecto con caracteres de control como Tab no seu nome. || Planificación e rastrexo de proxectos | 2790384 | O tempo de espera Pending OperationSet é demasiado curto. |
| Planificación e rastrexo de proxectos | 3044275 | Falta a localización para: missingProjectSchedulerErrorMessage. |
| Planificación e rastrexo de proxectos | 3044277 | A grella Project Recon non se carga cando o planificador non está configurado.|
| Xestión de recursos | 2943153 | Actualiza a pestana Seguimento para mostrar dúas cifras decimais para a duración.|
| Subcontratación | 2932774 | Liña de factura do provedor de só lectura erro ao lanzar incorrectamente. |
| Subcontratación | 2939556 | O estado da cabeceira da factura do provedor non debe establecerse como Borrador de eliminación en liña se non está activo. |
| Tempo e gasto | 2939998 | Adopta a nova versión de TESA en ProjOps. |


### <a name="project-management-and-accounting-in-finance"></a>Xestión e contabilidade de proxectos en Finance

Para obter información sobre as correccións incluídas nesta actualización, inicie sesión en Microsoft Dynamics Lifecycle Services (LCS) e vexa o [artigo de KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468).
