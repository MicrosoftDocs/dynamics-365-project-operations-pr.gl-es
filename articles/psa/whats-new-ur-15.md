---
title: Novidades ou cambios na versión 15 de actualización de Project Service Automation, V3
description: Este tema fornece información sobre as novidades e as modificacións na versión 15 de actualización de Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
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
ms.openlocfilehash: 2112e70d7359e7f30725ef3069a18570da651c06
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119911"
---
# <a name="project-service-automation-update-release-15-v3"></a>Versión 15 de actualización de Project Service Automation, V3

Comprácenos anunciar a última actualización para a aplicación Dynamics 365 Project Service Automation (PSA). Esta versión inclúe algunhas melloras importantes na calidade, rendemento e facilidade de uso. Esta versión é compatible con Dynamics 365 9.x. Para actualizar a esta versión, visite o Centro de administración para Dynamics 365 en liña e vaia á páxina de solucións para instalar a actualización. Para obter máis información, consulte [Instalar, actualizar ou eliminar unha solución preferida](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)

Este tema mostra as funcionalidades e correccións que son novas ou modificadas para PSA V3, versión 15 de actualización. Esta versión ten un número de compilación de V3.10.5.28 e está dispoñible xeralmente a través dunha autoactualización desde xaneiro de 2020.

## <a name="update-release-15"></a>Versión 15 de actualización 

### <a name="enhancements"></a>Melloras

- Xestión de proxectos

### <a name="bug-fixes"></a>Correccións de erros

- Tempo e gasto

  - Corrixido: Engadiuse o tratamento de erros de carga na vista de conciliación.
  - Corrixido: Plataforma común de recursos do proxecto: Cambiouse o nome **Cantidade** para reducir a ambigüidade.
  - Corrixido: Axustouse a vista **Copiar columnas de entrada de tempo** para incluír o tipo.
  - Corrixido: A edición da duración de entrada de tempo na vista de grade usando números decimais produce un erro descoñecido para algúns números.

- Xestión de proxectos

  - Corrixido: O menú despregable para **Usar en vista de rastrexo** agora expándese en función do ancho das opcións.
  - Corrixido: Ao xestionar proxectos no fuso horario +13, os cálculos de tarefas poden mostrar resultados incorrectos.
  - Corrixido: **Hora de finalización do membro do equipo** corrixiuse cando se usa un calendario de 24 horas.
  - Corrixido: Reactivouse o **BPF** no formulario principal **msdyn_project**.
  - Corrixido: O cálculo de atribucións xa non ignora un día.
  - Corrixido: Engadiuse unha nova faixa de notificación ao formulario do proxecto cando o fuso horario difire entre usuario e proxecto.

- Sales

  - Corrixido: A busca de categoría de estimación de gasto pódese usar para filtrar duplicados.
  - Corrixido: O código **PluginDomain.ExecuteInTryCatchBlock(..)** xa non oculta a orixe da excepción.
  - Corrixido: Xa non se recibe unha mensaxe de erro en **Busca de proxectos** no formulario **Liña de oferta** cando hai máis de 1000 proxectos.
  - Corrixido: A grade **Estimacións** para estimacións laborais e estimacións de gastos agora mostra o símbolo monetario correcto.
  - Corrixido: Despois de que unha organización actualice PSA desde a versión 14 de actualización á versión 15 de actualización, o separador **Programación** xa non aparece en branco no formulario **Proxecto**.
