---
title: Programación externa
description: Este artigo fornece información sobre a programación externa.
author: ruhercul
ms.date: 10/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 746fb3a7c812b2b387ec707e58796d02d2473847
ms.sourcegitcommit: b1a5b9bb8b826678fc52f1d5a3d199a71caccb0a
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 11/03/2022
ms.locfileid: "9736984"
---
# <a name="external-scheduling"></a>Programación externa

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

O modo de programación externa permítelle crear, actualizar e eliminar de forma nativa entidades relacionadas coas estruturas de subdivisión do traballo (WBS), pero sen os límites actuais que aplica Microsoft Project for the Web. Tamén ofrece validación limitada. Este modo só debe ser usado polos seguintes clientes:

- Clientes que dispoñen das ferramentas necesarias para definir unha WBS fóra da lóxica de programación que proporciona Project Operations
- Clientes que teñen que xestionar a xerarquía da programación, as dependencias ou a duración da tarefa

> [!IMPORTANT]
> É posible que os datos que non se introduzan correctamente nas entidades relacionadas coa WBS non se mostren na grade de conciliación de recursos, na grade de estimacións, na grade de seguimento ou na grade de atribución de recursos.

## <a name="configuration"></a>Configuración

Esta función está activada por defecto. Non obstante, na páxina principal lista para usar para proxectos, o campo relacionado non está visible por defecto. Para habilitar o campo, no Maker Portal, abra a páxina principal da entidade do proxecto, seleccione o campo **Motor de programación** e, a seguir, cambie o campo a **Visible por defecto**. Se non utiliza a páxina principal do proxecto lista para usar, edite a túa páxina existente e engádalle o campo **Motor de programación**.

## <a name="settings"></a>Configuracións

Para usar o modo de programación externa, primeiro debe crear un novo proxecto e seleccionar o motor de programación **Programado externamente** na lista despregable da páxina principal do proxecto. Despois de configurar este modo para un proxecto, non se pode cambiar.

## <a name="viewing-the-wbs"></a>Visualización da WBS

Se un proxecto está programado externamente, o acceso a Project for the Web está restrinxido para ese proxecto. Para ver a WBS, debe ir á grade de seguimento, onde se mostra a WBS completa.

## <a name="creating-and-editing-the-wbs"></a>Creación e edición de WBS

Se a programación externa está habilitada para un proxecto, debe definir os datos de todas as entidades relacionadas coa WBS, incluíndo tarefas, membros do equipo, atribucións de recursos e dependencias.

A seguinte ilustración mostra o modelo de datos para a planificación do proxecto.

![Modelo de datos de planificación do proxecto.](media/projectplanningdatamodel.png)

## <a name="functional-limitations"></a>Limitacións funcionais

As seguintes operacións non están permitidas en proxectos programados externamente.

### <a name="project-planning"></a>Planificación de proxectos

- **Copiar proxecto** - Esta operación non é compatible cos proxectos programados externamente.
- **Mover proxecto** – Os cambios na data de inicio dun proxecto non moverán o inicio das tarefas nin as atribucións de recursos na WBS.
- **Actualización do xestor do proxecto** – Os cambios no xestor do proxecto na páxina principal do proxecto non crearán automaticamente un novo membro do equipo do proxecto ata que o proxecto sexa convertido.
- **Actualización do modelo de horas de traballo do proxecto** – Os cambios no modelo de horas de traballo do proxecto non volverán calcular a programación do proxecto.
- **Contornos de atribución de recursos** – A creación de atribucións de recursos non actualizará automaticamente o campo **mdyn\_PlannedWork**. Este campo úsase para almacenar contornos para o esforzo de atribución de recursos. Se mostra o esforzo por fases de tempo na grade de atribución de recursos ou na grade de conciliación de recursos, debe definir contornos de atribución de recursos válidos. Estes contornos deben ter un formato correcto para que desencadeen o cálculo tanto dos contornos de custo como dos prezos de venda. Recomendamos que cree un proxecto de proba programado por Project for the Web e, a seguir, revise os datos asociados para confirmar os requisitos e o formato.

### <a name="resource-management"></a>Xestión de recursos

- **Cumprimento de recursos xenéricos** – O cumprimento de recursos xenéricos non é compatible con proxectos programados externamente. Os intentos de cumprir os requisitos abertos activos crearán novos membros do equipo do proxecto, pero non eliminará o membro xenérico do equipo nin substituirá o membro xenérico do equipo nas atribucións de recursos existentes.
- **Eliminar membro do equipo** – A eliminación dun membro do equipo non eliminará automaticamente as atribucións de recursos.

### <a name="quoting-and-contracting"></a>Ofertas e contratación

- **Importación de detalles da liña de oferta e da liña de contrato** – Cando se importan detalles da liña de oferta ou contrato dun proxecto, a aplicación probouse para admitir un máximo de só 500 tarefas na WBA, baseándose nun límite de 20 atribucións por tarefa.

### <a name="actuals-and-invoicing"></a>Datos reais e facturación

- Aínda que non hai cambios nas validacións existentes entre a WBS e as transaccións financeiras, é importante que se axuste ao modelo de datos listo para usar para garantir que todas as transaccións posteriores se executen como se espera.
