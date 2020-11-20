---
title: Novidades ou cambios na versión 22 de actualización de Project Service Automation, V3
description: Este tema mostra as funcionalidades e correccións que están dispoñibles la versión 22 de actualización de Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 07/28/2020
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
ms.openlocfilehash: 456ed68bc1d74c2c8e5d2420a3f5d1fb8e0465d6
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126616"
---
# <a name="project-service-automation-update-release-22-v3"></a>Versión 22 de actualización de Project Service Automation, V3

Comprácenos anunciar a última actualización da aplicación Project Service Automation para Dynamics 365. Esta versión inclúe algunhas melloras importantes na calidade, rendemento e facilidade de uso. Esta versión é compatible con Dynamics 365 9.x. Para actualizar a esta versión, visite a paxina de solucións do Centro de administración para Dynamics 365 en liña para instalar a actualización. Para obter máis información, consulte [Instalar, actualizar ou eliminar unha solución preferida](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)

Este tema mostra as funcionalidades e correccións que son novas ou modificadas para Project Service Automation V3, versión 22 de actualización. Esta versión ten un número de compilación de V 3.10.33.48 e está xeralmente dispoñible a través dunha actualización automática en xuño de 2020.

## <a name="update-release-22"></a>Versión 22 de actualización

### <a name="bug-fixes"></a>Correccións de erros



**Tempo e gasto**

Resolvéronse os seguintes problemas:

- As **Entradas de tempo** non se engaden automaticamente na programación de entradas de tempo despois da importación.
- O selector de datas da grade **Entrada de tempo** non recoñece a configuración rexional dun usuario.

**Xestión de recursos**

Resolvéronse os seguintes problemas:

- No modo manual, os cambios nos contornos de **Atribución do recurso** non se recoñecen ao xerar **Requisitos do recurso**.
- **Solicitudes de recursos** non admite estados de solicitude personalizados.

**Xestión de proxectos**

Resolvéronse os seguintes problemas:

- Ao premer dúas veces en EstimateGridControl non se analizarán correctamente os números do formato holandés.
- As horas atribuídas non se actualizan correctamente cando as tarefas se cambian mediante o complemento de cliente de escritorio de Microsoft Project.
- As grades de rastrexo e estimacións de proxectos mostran un código de moeda de vendas incorrecto cando a moeda do contrato é diferente da moeda do cliente e a organización está configurada para mostrar códigos de moeda en lugar de símbolos de moeda.
- A data de finalización dun membro do equipo engadirá un día se o horario de traballo é de 24 horas ao día.
- Na programación do proxecto, ao engadir unha categoría de transacción a unha tarefa non se activa o aforro automático.
- Aparece o seguinte erro ao engadir un membro do equipo ao modelo do proxecto: "Non se poden asociar requisitos de recursos aos modelos de proxecto". 
- O script de regra de fita "msdyn.Approval.CanApproveOrReject" mostra un erro de tempo de espera.

**Sales**

Resolvéronse os seguintes problemas:

- A mensaxe de erro de validación non se mostra cando se selecciona unha Lista de prezos de custo na busca de Lista de prezos no formulario/entidade "Lista de prezos de proxecto de nova oferta".
- O peche do presuposto como gañado non navega ata o contrato creado se un BPF anexado á oferta está na fase final.
- A inversión de **Vendas sen facturar** está ligada ao custo orixinal cando se recupera unha entrada de tempo.
- Despois de seleccionar o botón **Confirmar**, o estado da factura non cambia a **Confirmada** a menos que se actualice a factura.
