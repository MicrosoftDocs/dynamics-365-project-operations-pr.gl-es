---
title: Novidades ou cambios na versión 13 de actualización de Project Service Automation, V3
description: Este tema fornece información sobre as novidades e as modificacións na versión 13 de actualización de Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: bcb05b640966e760a7a74a306a3f0a39594baed8
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121621"
---
# <a name="project-service-automation-update-release-13-v3"></a><span data-ttu-id="3e4ec-103">Versión 13 de actualización de Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="3e4ec-103">Project Service Automation Update Release 13, V3</span></span>
<span data-ttu-id="3e4ec-104">Comprácenos anunciar a última actualización para a aplicación Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="3e4ec-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="3e4ec-105">Esta versión inclúe algunhas melloras importantes na calidade, rendemento e facilidade de uso.</span><span class="sxs-lookup"><span data-stu-id="3e4ec-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="3e4ec-106">Esta versión é compatible con Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="3e4ec-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="3e4ec-107">Para actualizar a esta versión, visite o Centro de administración para Dynamics 365 en liña e vaia á páxina de solucións para instalar a actualización.</span><span class="sxs-lookup"><span data-stu-id="3e4ec-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="3e4ec-108">Para obter máis información, consulte [Instalar, actualizar ou eliminar unha solución preferida](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)</span><span class="sxs-lookup"><span data-stu-id="3e4ec-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="3e4ec-109">Este tema mostra as funcionalidades e correccións que son novas ou modificadas para Project Service Automation V3, versión 13 de actualización.</span><span class="sxs-lookup"><span data-stu-id="3e4ec-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 13.</span></span> <span data-ttu-id="3e4ec-110">Esta versión ten un número de compilación de V3.10.3.18 e está dispoñible na seguinte programación:</span><span class="sxs-lookup"><span data-stu-id="3e4ec-110">This version has a build number of V3.10.3.18 and is available on the following schedule:</span></span>

- <span data-ttu-id="3e4ec-111">**Dispoñibilidade xeral (autoactualización):** Novembro de 2019</span><span class="sxs-lookup"><span data-stu-id="3e4ec-111">**General availability (self-update):** November 2019</span></span>
- <span data-ttu-id="3e4ec-112">**Autoactualización:** Decembro de 2019</span><span class="sxs-lookup"><span data-stu-id="3e4ec-112">**Auto-update:** December 2019</span></span>


## <a name="update-release-13"></a><span data-ttu-id="3e4ec-113">Versión 13 de actualización</span><span class="sxs-lookup"><span data-stu-id="3e4ec-113">Update Release 13</span></span> 

### <a name="bug-fixes"></a><span data-ttu-id="3e4ec-114">Correccións de erros</span><span class="sxs-lookup"><span data-stu-id="3e4ec-114">Bug fixes</span></span>

- <span data-ttu-id="3e4ec-115">Tempo e gasto</span><span class="sxs-lookup"><span data-stu-id="3e4ec-115">Time and Expense</span></span>

     - <span data-ttu-id="3e4ec-116">Corrixido: A funcionalidade de busca na páxina **Aprobación de gastos** non funciona cando se busca por finalidade do gasto.</span><span class="sxs-lookup"><span data-stu-id="3e4ec-116">Fixed: Search functionality on the **Expense approval** page does not work when searching by expense purpose.</span></span>

- <span data-ttu-id="3e4ec-117">Xestión de recursos</span><span class="sxs-lookup"><span data-stu-id="3e4ec-117">Resource Management</span></span>

     - <span data-ttu-id="3e4ec-118">Corrixido: Os números da conciliación actualizáronse para aliñarse á dereita.</span><span class="sxs-lookup"><span data-stu-id="3e4ec-118">Fixed: Numbers in the reconciliation have been updated to be right justified.</span></span>
     - <span data-ttu-id="3e4ec-119">Corrixido: Os recursos nomeados non se poden asignar a tarefas a través do separador **Programación**.</span><span class="sxs-lookup"><span data-stu-id="3e4ec-119">Fixed: Named Resources can't be assigned to tasks through the **Schedule** tab.</span></span>

- <span data-ttu-id="3e4ec-120">Xestión de proxectos</span><span class="sxs-lookup"><span data-stu-id="3e4ec-120">Project Management</span></span>

     - <span data-ttu-id="3e4ec-121">Corrixido: A excepción referencia nula ao atribuír o membro do equipo cando en **Tipo de transacción** falta información de configuración para **Unidade** e **Grupo predefinido**.</span><span class="sxs-lookup"><span data-stu-id="3e4ec-121">Fixed: Null reference exception when assigning team member when the **TransactionType** is missing setup information for **Unit** and **DefaultGroup**.</span></span>

- <span data-ttu-id="3e4ec-122">Sales</span><span class="sxs-lookup"><span data-stu-id="3e4ec-122">Sales</span></span>

     - <span data-ttu-id="3e4ec-123">Corrixido: Os rexistros de tipo de transacción duplicados mostran un erro ao crearse os rexistros de prezo de rol.</span><span class="sxs-lookup"><span data-stu-id="3e4ec-123">Fixed: Duplicate transaction type records return an error when role price records are created.</span></span>
     - <span data-ttu-id="3e4ec-124">Resolto: Os botóns adicionais para **Nova oportunidade**, **Oferta**, **Liña de pedido** e **Engadir produto** son visibles nos comandos de Oportunidades, Ofertas, Pedir produtos e a subgrade Liñas baseadas en proxectos.</span><span class="sxs-lookup"><span data-stu-id="3e4ec-124">Fixed: Extra buttons for **New Opportunity**, **Quote**, **Order Line**, and **Add Product** are visible in commands for Opportunities, Quotes, Order Products, and the project-based Lines subgrid.</span></span>


