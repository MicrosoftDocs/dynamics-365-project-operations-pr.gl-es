---
title: Novidades ou cambios na versión 21 de actualización de Project Service Automation, V3
description: Este tema mostra as funcionalidades e correccións que están dispoñibles la versión 21 de actualización de Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 799be481c365e82e8ffb59ba242e30378644008b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126706"
---
# <a name="project-service-automation-update-release-21-v3"></a><span data-ttu-id="84601-103">Versión 21 de actualización de Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="84601-103">Project Service Automation Update Release 21, V3</span></span>

<span data-ttu-id="84601-104">Comprácenos anunciar a última actualización da aplicación Project Service Automation para Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="84601-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="84601-105">Esta versión inclúe algunhas melloras importantes na calidade, rendemento e facilidade de uso.</span><span class="sxs-lookup"><span data-stu-id="84601-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="84601-106">Esta versión é compatible con Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="84601-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="84601-107">Para actualizar a esta versión, visite a paxina de solucións do Centro de administración para Dynamics 365 en liña para instalar a actualización.</span><span class="sxs-lookup"><span data-stu-id="84601-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="84601-108">Para obter máis información, consulte [Instalar, actualizar ou eliminar unha solución preferida](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)</span><span class="sxs-lookup"><span data-stu-id="84601-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="84601-109">Este tema mostra as funcionalidades e correccións que son novas ou modificadas para Project Service Automation V3, versión 21 de actualización.</span><span class="sxs-lookup"><span data-stu-id="84601-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 21.</span></span> <span data-ttu-id="84601-110">Esta versión ten un número de compilación de V 3.10.32.50 e está xeralmente dispoñible a través dunha actualización automática en xuño de 2020.</span><span class="sxs-lookup"><span data-stu-id="84601-110">This version has a build number of V 3.10.32.50 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-21"></a><span data-ttu-id="84601-111">Versión 21 de actualización</span><span class="sxs-lookup"><span data-stu-id="84601-111">Update Release 21</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="84601-112">Correccións de erros</span><span class="sxs-lookup"><span data-stu-id="84601-112">Bug fixes</span></span>

<span data-ttu-id="84601-113">**Tempo e gasto**</span><span class="sxs-lookup"><span data-stu-id="84601-113">**Time and Expense**</span></span>

<span data-ttu-id="84601-114">Resolvéronse os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="84601-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="84601-115">Cando se aloxa o **Control de grade de entradas de tempo** en paneis, a grade non usa todo o ancho do contedor da grade do panel.</span><span class="sxs-lookup"><span data-stu-id="84601-115">When hosting the **Time Entry Grid Control** in Dashboards, the grid does not utilize the full width of the dashboard grid container.</span></span>
- <span data-ttu-id="84601-116">Para zonas horarias específicas, o control da grade **Entrada de tempo** non mostra rexistros.</span><span class="sxs-lookup"><span data-stu-id="84601-116">For specific time zones, the **Time Entry** grid control does not display records.</span></span>
- <span data-ttu-id="84601-117">As entradas de tempo posteriores ás 21:00 aparecen no día incorrecto.</span><span class="sxs-lookup"><span data-stu-id="84601-117">Time entries that are after 9:00 PM appear on the wrong day.</span></span>
- <span data-ttu-id="84601-118">Os usuarios non poden enviar gastos se a categoría de gastos, **Recibo de gasto requirido** non ten ningún valor.</span><span class="sxs-lookup"><span data-stu-id="84601-118">Users are unable to submit expenses if the expense category, **Expense receipt required** has no value.</span></span>

<span data-ttu-id="84601-119">**Xestión de recursos**</span><span class="sxs-lookup"><span data-stu-id="84601-119">**Resource Management**</span></span>

<span data-ttu-id="84601-120">Resolvéronse os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="84601-120">The following issues have been fixed:</span></span>

- <span data-ttu-id="84601-121">As reservas inactivas móstranse na vista **Conciliación**.</span><span class="sxs-lookup"><span data-stu-id="84601-121">Inactive bookings are displayed in the **Reconciliation** view.</span></span>
- <span data-ttu-id="84601-122">Faltou a validación do cumprimento xenérico do recurso para garantir que existe un estado de reserva válida.</span><span class="sxs-lookup"><span data-stu-id="84601-122">Generic resource fulfillment was missing validation to ensure that a valid booking status exists.</span></span>

<span data-ttu-id="84601-123">**Xestión de proxectos**</span><span class="sxs-lookup"><span data-stu-id="84601-123">**Project Management**</span></span>

<span data-ttu-id="84601-124">Resolvéronse os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="84601-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="84601-125">As grades do formulario **Proxecto** (**Atribución do recurso**, **Tarefa**, vista **Conciliación**, **Estimacións de gastos**) poden editarse aínda que o proxecto non estea activo.</span><span class="sxs-lookup"><span data-stu-id="84601-125">The **Project** form grids (**Resource Assignment**, **Task**, **Reconciliation** view, **Expense Estimates**) remain editable even when a project is not active.</span></span>
- <span data-ttu-id="84601-126">Non se poden combinar clientes duplicados con clientes que están vinculados a contratos de proxecto confirmados.</span><span class="sxs-lookup"><span data-stu-id="84601-126">Duplicate customers can't be merged with customers that are linked to confirmed project contracts.</span></span>
- <span data-ttu-id="84601-127">Cando se engade un recurso que non ten un calendario válido, o sistema non devolve unha mensaxe de erro fácil de entender.</span><span class="sxs-lookup"><span data-stu-id="84601-127">When a resource who does not have a valid calendar is added, the system does not return a user friendly-error message.</span></span>
- <span data-ttu-id="84601-128">O botón **Engadir tarefa** da grade de tarefas está activado cando o proxecto está ligado ao **complemento Microsoft Project**.</span><span class="sxs-lookup"><span data-stu-id="84601-128">The **Add Task** button on the task grid is enabled when the project is linked to **Microsoft Project add-in**.</span></span>
- <span data-ttu-id="84601-129">O esforzo crece de xeito incontrolado cando se asigna unha tarefa cunha categoría a un recurso cun rol para o que hai definido un prezo de custo.</span><span class="sxs-lookup"><span data-stu-id="84601-129">Effort grows uncontrollably when a task with a category is assigned to a resource with a role for which there is a cost price defined.</span></span>

<span data-ttu-id="84601-130">**Sales**</span><span class="sxs-lookup"><span data-stu-id="84601-130">**Sales**</span></span>

<span data-ttu-id="84601-131">Fixéronse as seguintes melloras:</span><span class="sxs-lookup"><span data-stu-id="84601-131">The following enhancements have been made:</span></span>

- <span data-ttu-id="84601-132">**Frecuencia da factura** e **Inicio de facturación** movéronse ao separador **Programación de factura**.</span><span class="sxs-lookup"><span data-stu-id="84601-132">**Invoice Frequency** and **Billing Start** have been moved to the **Invoice Schedule** tab.</span></span>

<span data-ttu-id="84601-133">Resolvéronse os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="84601-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="84601-134">**Prezo de venda total** é cero (0) para **Categoría** aínda que **Rol** ten un prezo de venda total que non é cero.</span><span class="sxs-lookup"><span data-stu-id="84601-134">**Total Sales Price** is zero (0) for **Category** even though **Role** has a total sales price that is not zero.</span></span>
- <span data-ttu-id="84601-135">Os clientes non poden cambiar o valor do campo **Estado da factura** a **Listo para facturarse** cando outro proceso personalizado está a actualizar un campo adicional.</span><span class="sxs-lookup"><span data-stu-id="84601-135">Customers can't change the value of the **Invoice Status** field to **Ready for invoicing** when another customized process is updating an additional field.</span></span>
- <span data-ttu-id="84601-136">O botón **Actualizar liñas de factura** pode crear varias liñas duplicadas se se selecciona repetidamente.</span><span class="sxs-lookup"><span data-stu-id="84601-136">The **Refresh Invoice Lines** button can create multiple duplicated lines if it is repeatedly selected.</span></span>
- <span data-ttu-id="84601-137">O botón **Actualizar prezos** o botón non funciona na subgrade **Prezos de rol** do formulario de **Visualización rápida**.</span><span class="sxs-lookup"><span data-stu-id="84601-137">The **Update Prices** button doesn't work on the **Role Prices** subgrid in the **Quick View** form.</span></span>
- <span data-ttu-id="84601-138">A lóxica de **Resolución da lista de prezos de venda** trata inadecuadamente os fusos horarios, o que produce unha selección incorrecta das listas de prezos.</span><span class="sxs-lookup"><span data-stu-id="84601-138">The **Sales Price List Resolution** logic improperly handles time zones, resulting in the incorrect selection of price lists.</span></span>
- <span data-ttu-id="84601-139">O **Custo real total** dun proxecto pódese desactivar por unha cantidade fraccionada despois de aprobar unha entrada de tempo única.</span><span class="sxs-lookup"><span data-stu-id="84601-139">A project’s **Total Actual Cost** can be off by a fractional amount after a single time entry is approved.</span></span>
- <span data-ttu-id="84601-140">A lóxica de **Resolución de prezos** non fornece unha mensaxe de erro fácil de entender se **Prezo de rol recuperado** non ten valores nos campos **"Unidade Primaria"** e **"Prezo na unidade primaria"**.</span><span class="sxs-lookup"><span data-stu-id="84601-140">The **Price Resolution** logic does not provide a user-friendly error message if **Retrieved RolePrice** doesn't have values in **'Primary Unit'** and **'Price In Primary Unit'** fields.</span></span>
