---
title: Novidades ou cambios na versión 3.x onda 1 2020 de Project Service Automation
description: Este tema fornece información sobre as novidades e as modificacións na versión 3 onda 1 2020 de Project Service Automation.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/15/2020
ms.topic: article
author: stsporen
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 2308f83e09c25059b6a36599b04b5b00f66c704f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126481"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a><span data-ttu-id="477ef-103">Novidades ou cambios na versión 3 onda 1 2020 de Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="477ef-103">What's new or changed in Project Service Automation version 3 wave 1 2020</span></span>
<span data-ttu-id="477ef-104">O tema resalta as principais consideracións da actualización ao pasar á última versión de Project Service Automation (PSA) versión 3.x onda 1 2020.</span><span class="sxs-lookup"><span data-stu-id="477ef-104">The topic highlights key upgrade considerations when moving to the latest release of Project Service Automation (PSA) version 3.x wave 1 2020.</span></span>

## <a name="time-entry"></a><span data-ttu-id="477ef-105">Entrada de tempo</span><span class="sxs-lookup"><span data-stu-id="477ef-105">Time entry</span></span>
<span data-ttu-id="477ef-106">A experiencia de entrada de tempo ampliouse para ofrecer capacidades para ampliar a entrada de tempo a máis escenarios de clientes.</span><span class="sxs-lookup"><span data-stu-id="477ef-106">The time entry experience has been extended to deliver capabilities for extending time entry into more customer scenarios.</span></span> <span data-ttu-id="477ef-107">Isto inclúe a capacidade de engadir tipos de entrada, que agora favorecen un comportamento específico baseado no nome do esquema de campo **Configuración de entrada de hora**, amosado como **Orixe de tempo**.</span><span class="sxs-lookup"><span data-stu-id="477ef-107">This includes the capability to add entry types, which now drive specific behavior based on the field schema name **Time Entry Settings**, displayed as **Time Source**.</span></span> <span data-ttu-id="477ef-108">Engadiuse unha nova solución, chamada Time, Expense, Statusing, and Approvals (TESA) para permitir esta funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="477ef-108">A new solution, called Time, Expense, Statusing, and Approvals (TESA) has been added to support this functionality.</span></span>

### <a name="upgrade-consideration"></a><span data-ttu-id="477ef-109">Consideración sobre a actualización</span><span class="sxs-lookup"><span data-stu-id="477ef-109">Upgrade consideration</span></span>
<span data-ttu-id="477ef-110">Para apoiar esta funcionalidade, os roles dentro de PSA actualizáronse para incluír novos privilexios.</span><span class="sxs-lookup"><span data-stu-id="477ef-110">To support this functionality, the roles within PSA have been updated to include new privileges.</span></span> <span data-ttu-id="477ef-111">Estes privilexios conceden acceso de lectura á nova entidade, **Configuración de entrada de hora**.</span><span class="sxs-lookup"><span data-stu-id="477ef-111">These privileges grant read access to the new entity, **Time Entry Settings**.</span></span>

<span data-ttu-id="477ef-112">Os usuarios que requiran a capacidade de rexistro de tempo deben recibir o rol de usuario **Usuario de entrada de tempo** ademais dos roles existentes.</span><span class="sxs-lookup"><span data-stu-id="477ef-112">Users who require the ability to log time should be granted the user role **Time Entry User** in addition to existing roles.</span></span> <span data-ttu-id="477ef-113">Este papel inclúe a nova funcionalidade e garante que a entrada de tempo seguirá funcionando.</span><span class="sxs-lookup"><span data-stu-id="477ef-113">This role includes the new functionality and ensures that time entry will continue to work.</span></span>

<span data-ttu-id="477ef-114">Ademais, se ten módulos de aplicación personalizados que inclúan todos os formularios para a entidade de entrada de tempo, deberá eliminar o **Formulario de creación rápida da entradas de tempo de TESA** desde o módulo.</span><span class="sxs-lookup"><span data-stu-id="477ef-114">Additionally, if you have any custom app modules that include all forms for the time entry entity, you will be required to remove the **TESA time Entry Quick Create Form** from the module.</span></span>

### <a name="currently-extended-time-entry-changes"></a><span data-ttu-id="477ef-115">Cambios de entrada de tempo ampliado actualmente</span><span class="sxs-lookup"><span data-stu-id="477ef-115">Currently extended time entry changes</span></span>
<span data-ttu-id="477ef-116">Para minimizar o impacto para os usuarios actuais de entrada de tempo, este cambio de rol é o único requisito básico necesario para continuar utilizando a entrada de tempo.</span><span class="sxs-lookup"><span data-stu-id="477ef-116">To minimize the impact to current users of time entry, this role change is the only core requirement necessary to continue utilizing time entry.</span></span> <span data-ttu-id="477ef-117">Se creou vistas personalizadas ou experiencias de entrada de tempo independentes, ten que configurar os campos de **Configuración de entrada de tempo** co valor de PSA correcto.</span><span class="sxs-lookup"><span data-stu-id="477ef-117">If you have created custom views or separate time entry experiences, you must set the **Time Entry Setting** fields to the correct PSA value.</span></span>
