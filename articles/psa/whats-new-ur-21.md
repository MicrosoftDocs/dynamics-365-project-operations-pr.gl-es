---
title: Novidades ou cambios na versión 21 de actualización de Project Service Automation, V3
description: Este tema mostra as funcionalidades e correccións que están dispoñibles la versión 21 de actualización de Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: e8a15d5f723da528640c62c1892bac0d801c2bee
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076083"
---
# <a name="project-service-automation-update-release-21-v3"></a>Versión 21 de actualización de Project Service Automation, V3

Comprácenos anunciar a última actualización da aplicación Project Service Automation para Dynamics 365. Esta versión inclúe algunhas melloras importantes na calidade, rendemento e facilidade de uso. Esta versión é compatible con Dynamics 365 9.x. Para actualizar a esta versión, visite a paxina de solucións do Centro de administración para Dynamics 365 en liña para instalar a actualización. Para obter máis información, consulte [Instalar, actualizar ou eliminar unha solución preferida](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)

Este tema mostra as funcionalidades e correccións que son novas ou modificadas para Project Service Automation V3, versión 21 de actualización. Esta versión ten un número de compilación de V 3.10.32.50 e está xeralmente dispoñible a través dunha actualización automática en xuño de 2020.

## <a name="update-release-21"></a>Versión 21 de actualización

### <a name="bug-fixes"></a>Correccións de erros

**Tempo e gasto**

Resolvéronse os seguintes problemas:

- Cando se aloxa o **Control de grade de entradas de tempo** en paneis, a grade non usa todo o ancho do contedor da grade do panel.
- Para zonas horarias específicas, o control da grade **Entrada de tempo** non mostra rexistros.
- As entradas de tempo posteriores ás 21:00 aparecen no día incorrecto.
- Os usuarios non poden enviar gastos se a categoría de gastos, **Recibo de gasto requirido** non ten ningún valor.

**Xestión de recursos**

Resolvéronse os seguintes problemas:

- As reservas inactivas móstranse na vista **Conciliación**.
- Faltou a validación do cumprimento xenérico do recurso para garantir que existe un estado de reserva válida.

**Xestión de proxectos**

Resolvéronse os seguintes problemas:

- As grades do formulario **Proxecto** ( **Atribución do recurso** , **Tarefa** , vista **Conciliación** , **Estimacións de gastos** ) poden editarse aínda que o proxecto non estea activo.
- Non se poden combinar clientes duplicados con clientes que están vinculados a contratos de proxecto confirmados.
- Cando se engade un recurso que non ten un calendario válido, o sistema non devolve unha mensaxe de erro fácil de entender.
- O botón **Engadir tarefa** da grade de tarefas está activado cando o proxecto está ligado ao **complemento Microsoft Project**.
- O esforzo crece de xeito incontrolado cando se asigna unha tarefa cunha categoría a un recurso cun rol para o que hai definido un prezo de custo.

**Sales**

Fixéronse as seguintes melloras:

- **Frecuencia da factura** e **Inicio de facturación** movéronse ao separador **Programación de factura**.

Resolvéronse os seguintes problemas:

- **Prezo de venda total** é cero (0) para **Categoría** aínda que **Rol** ten un prezo de venda total que non é cero.
- Os clientes non poden cambiar o valor do campo **Estado da factura** a **Listo para facturarse** cando outro proceso personalizado está a actualizar un campo adicional.
- O botón **Actualizar liñas de factura** pode crear varias liñas duplicadas se se selecciona repetidamente.
- O botón **Actualizar prezos** non funciona na subgrade **Prezos de rol** no formulario **Visualización rápida**.
- A lóxica de **Resolución da lista de prezos de venda** trata inadecuadamente os fusos horarios, o que produce unha selección incorrecta das listas de prezos.
- O **Custo real total** dun proxecto pódese desactivar por unha cantidade fraccionada despois de aprobar unha entrada de tempo única.
- A lóxica de **Resolución de prezos** non fornece unha mensaxe de erro fácil de entender se **Prezo de rol recuperado** non ten valores nos campos **"Unidade Primaria"** e **"Prezo na unidade primaria"**.