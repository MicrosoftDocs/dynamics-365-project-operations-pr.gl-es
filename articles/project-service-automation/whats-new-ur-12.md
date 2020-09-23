---
title: Novidades na versión 12 de actualización de Project Service Automation, V3
description: Este tema fornece información sobre as novidades e as modificacións na versión 12 de actualización de Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: af8dbfe3-7ce9-4374-9c03-17b2e1d6ac32
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 758717562c12a72848f1a874fa8b1171139ebb0c
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751386"
---
# <a name="project-service-automation-v3-update-release-12"></a>Project Service Automation V3, versión 12 de actualización
Comprácenos anunciar a última actualización para a aplicación Dynamics 365 Project Service Automation (PSA). Esta versión inclúe algunhas melloras importantes na calidade, rendemento e facilidade de uso. Esta versión é compatible con Dynamics 365 9.x. Para actualizar a esta versión, visite o Centro de administración para Dynamics 365 en liña e vaia á páxina de solucións para instalar a actualización. Para obter máis información, consulte [Instalar, actualizar ou eliminar unha solución preferida](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)

Este tema mostra as funcionalidades e correccións que son novas ou modificadas para Project Service Automation V3, versión 12 de actualización. Esta versión ten un número de compilación de V3.10.2.34 e está dispoñible xeralmente a través dunha autoactualización desde outubro de 2019.

## <a name="update-release-12"></a>Versión 12 de actualización

### <a name="bug-fixes"></a>Correccións de erros

- Tempo e gasto

    - Corrixido: As mensaxes de erro de entrada de tempo actualizáronse cun contexto máis relevante.
    - Corrixido: A grade de entrada de tempo e a programación mostran correctamente a barra de desprazamento vertical cando é necesario.
    - Corrixido: As entradas de gasto e tempo enviadas poden aprobarse.
    - Corrixido: Corrixiuse a mensaxe de diálogo de Cancelar confirmación de aprobación para reflectir o estado da aprobación cando se cambia de **Aprobado** a **Enviado**.
    - Corrixido: Os campos **Prezo**, **Unidade** e **Cantidade** campos agora están bloqueados no rexistro Gasto despois de que se aprobaron.

- Xestión de proxectos

    - Fixado: A acción **Novo** no formulario principal de **Membro do equipo** eliminouse.
    - Corrixido: As atribucións de recursos actualizáronse para dar conta de erros de redondeo inexacto, que provocan un cambio na data de finalización dunha tarefa.
    - Corrixido: Na grade de tarefas, mostraranse ao usuario os erros relevantes do servidor.
    - Corrixido: O nome do membro do equipo móstrase agora no selector de tarefas en vez do nome do posto.

- Xestión de recursos

    - Corrixido: Os detalles do requisito do recurso para os proxectos creados a partir dun modelo agora usan o calendario do proxecto.
    - Corrixido: As habilidades e as competencias agora se definen segundo os datos mestres do rol no requisito de recurso creado para ese rol.

- Sales

    - Corrixido: Os ID de obxecto duplicados atopados no formulario **Principal do contrato**.
    - Corrixido: A lóxica actualizouse para facer que o separador **Análise de ofertas** sexa visible e mostre a configuración de metadatos do separador.
    - Corrixido: A data de contabilidade do rexistro real agora procede da data da entrada de tempo/gasto e non da data de aprobación.
