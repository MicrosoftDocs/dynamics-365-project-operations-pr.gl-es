---
title: Novidades ou cambios na versión 20 de actualización de Project Service Automation, V3
description: Este tema mostra as funcionalidades e correccións que están dispoñibles la versión 20 de actualización de Project Service Automation, V3
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
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
ms.openlocfilehash: ef24c20f3fa520b25a14773a15363a0f04f98d36
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126751"
---
# <a name="project-service-automation-update-release-20-v3"></a><span data-ttu-id="ef2e2-103">Versión 20 de actualización de Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="ef2e2-103">Project Service Automation Update Release 20, V3</span></span>

<span data-ttu-id="ef2e2-104">Comprácenos anunciar a última actualización da aplicación Project Service Automation para Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="ef2e2-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="ef2e2-105">Esta versión inclúe algunhas melloras importantes na calidade, rendemento e facilidade de uso.</span><span class="sxs-lookup"><span data-stu-id="ef2e2-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="ef2e2-106">Esta versión é compatible con Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="ef2e2-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="ef2e2-107">Para actualizar a esta versión, visite a paxina de solucións do Centro de administración para Dynamics 365 en liña para instalar a actualización.</span><span class="sxs-lookup"><span data-stu-id="ef2e2-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="ef2e2-108">Para obter máis información, consulte [Instalar, actualizar ou eliminar unha solución preferida](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)</span><span class="sxs-lookup"><span data-stu-id="ef2e2-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="ef2e2-109">Este tema mostra as funcionalidades e correccións que son novas ou modificadas para Project Service Automation V3, versión 20 de actualización.</span><span class="sxs-lookup"><span data-stu-id="ef2e2-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 20.</span></span> <span data-ttu-id="ef2e2-110">Esta versión ten un número de compilación de V 3.10.31.37 e está xeralmente dispoñible a través dunha actualización automática en xuño de 2020.</span><span class="sxs-lookup"><span data-stu-id="ef2e2-110">This version has a build number of V 3.10.31.37 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-20"></a><span data-ttu-id="ef2e2-111">Versión 20 de actualización</span><span class="sxs-lookup"><span data-stu-id="ef2e2-111">Update Release 20</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="ef2e2-112">Correccións de erros</span><span class="sxs-lookup"><span data-stu-id="ef2e2-112">Bug fixes</span></span>

<span data-ttu-id="ef2e2-113">**Xestión de proxectos**</span><span class="sxs-lookup"><span data-stu-id="ef2e2-113">**Project Management**</span></span>

<span data-ttu-id="ef2e2-114">Resolvéronse os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="ef2e2-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="ef2e2-115">A importación dos membros do equipo do proxecto cun método de atribución que require horas ten como resultado unha mensaxe de erro pouco clara cando as horas especificadas son cero.</span><span class="sxs-lookup"><span data-stu-id="ef2e2-115">Importing project team members with an allocation method that requires hours results in an unclear error message when the specified hours are zero.</span></span>
- <span data-ttu-id="ef2e2-116">Os usuarios reciben un erro incorrecto cando se introduciu o número máximo de caracteres no campo **Descrición** para unha tarefa de proxecto.</span><span class="sxs-lookup"><span data-stu-id="ef2e2-116">Users receive an incorrect error when the maximum number of characters have been entered into the **Description** field for a project task.</span></span>
- <span data-ttu-id="ef2e2-117">A páxina **Descarga de suplementos de Microsoft Dynamics 365 Project Service Automation** redireccionan á páxina de descargas en inglés cando a configuración do idioma do usuario é o xaponés.</span><span class="sxs-lookup"><span data-stu-id="ef2e2-117">The **Microsoft Dynamics 365 Project Service Automation add-in download** page redirects to the English download page when the user’s language settings are set to Japanese.</span></span>
- <span data-ttu-id="ef2e2-118">Cando se produce un erro no servidor, a etiqueta de sincronización no separador **Programar** do formulario **Proxectos** permanece ás veces.</span><span class="sxs-lookup"><span data-stu-id="ef2e2-118">When a server error occurs, the synchronization label on the **Schedule** tab of the **Projects** form sometimes remains.</span></span>
- <span data-ttu-id="ef2e2-119">As actualizacións de tarefas redundantes envíanse ao servidor cando se modifica unha tarefa.</span><span class="sxs-lookup"><span data-stu-id="ef2e2-119">Redundant task updates are being sent to the server when a task is modified.</span></span>

<span data-ttu-id="ef2e2-120">**Sales**</span><span class="sxs-lookup"><span data-stu-id="ef2e2-120">**Sales**</span></span>

<span data-ttu-id="ef2e2-121">Resolvéronse os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="ef2e2-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="ef2e2-122">No formulario **Contrato**, ao premer dúas veces **Crear factura** créanse dúas facturas para un único rexistro de datos reais.</span><span class="sxs-lookup"><span data-stu-id="ef2e2-122">On the **Contract** form, double-clicking **Create Invoice** creates two invoices for a single actuals record.</span></span>
- <span data-ttu-id="ef2e2-123">En Internet Explorer 11, os usuarios non poden crear entradas de gastos.</span><span class="sxs-lookup"><span data-stu-id="ef2e2-123">In Internet Explorer 11, users are unable to create expense entries.</span></span>
- <span data-ttu-id="ef2e2-124">A inversión do custo e a inversión dos datos reais de vendas non facturadas non están ligadas.</span><span class="sxs-lookup"><span data-stu-id="ef2e2-124">Reversal of Cost and reversal of Unbilled Sales Actuals are not linked.</span></span>
- <span data-ttu-id="ef2e2-125">O botón **Actualizar datos reais** no formulario **Proxecto** non actualiza **Horario real da tarefa**.</span><span class="sxs-lookup"><span data-stu-id="ef2e2-125">The **Refresh Actuals** button on the **Project** form does not refresh **Task Actual Hours**.</span></span>
- <span data-ttu-id="ef2e2-126">O suplemento **PreValidateProjectTeamMemberCreate** pode crear recursos xenéricos duplicados reservables cando o atributo **msdyn_isgenericresourceprojectscoped** está configurado en **Falso**.</span><span class="sxs-lookup"><span data-stu-id="ef2e2-126">The **PreValidateProjectTeamMemberCreate** plug-in can create duplicate generic bookable resources when the attribute **msdyn_isgenericresourceprojectscoped** is set to **False**.</span></span>
- <span data-ttu-id="ef2e2-127">**Calcular de novo** limpa os custos imputables dos detalles da liña de oferta baseada nos produtos e os detalles da liña de contrato.</span><span class="sxs-lookup"><span data-stu-id="ef2e2-127">**Recalculate** clears chargeable costs of product-based quote line details and contract line details.</span></span>
- <span data-ttu-id="ef2e2-128">En escenarios específicos, o suplemento **PostEstimateLineUpdate** mostra un erro de excepción de referencia nula.</span><span class="sxs-lookup"><span data-stu-id="ef2e2-128">In specific scenarios, the **PostEstimateLineUpdate** plug-in displays a null teference exception error.</span></span>
- <span data-ttu-id="ef2e2-129">A duración da fase de tempo na **Gráfica de análise da rendibilidade** non coincide coa duración dos custos no detalle da liña de oferta de prezo fixo da oferta.</span><span class="sxs-lookup"><span data-stu-id="ef2e2-129">Time phase duration on the **Profitability Analysis Chart** does not match duration of the costs in the fixed-price quote line detail of the quote.</span></span>
- <span data-ttu-id="ef2e2-130">Os valores de unidade e grupos de unidades non aparecen de forma predeterminada correctamente para as categorías de gasto nos formularios **Detalles da liña de contrato** e **Detalles da liña de oferta**.</span><span class="sxs-lookup"><span data-stu-id="ef2e2-130">Unit and unit group values do not default correctly for expense categories on the **Contract Line Details** and **Quote Line Details** forms.</span></span>
- <span data-ttu-id="ef2e2-131">As listas de **Prezo de custo da unidade organizativa** permiten solapamentos na data de validez.</span><span class="sxs-lookup"><span data-stu-id="ef2e2-131">**Org Unit Cost Price** lists permit overlaps in the date effectivity.</span></span>
- <span data-ttu-id="ef2e2-132">Os usuarios non teñen permiso para cambiar **OrgUnit** cando o tipo de pedido non está baseado en traballo, porque levará a un erro de excepción de referencia nula.</span><span class="sxs-lookup"><span data-stu-id="ef2e2-132">Users are not permitted to change the **OrgUnit** when the order type is not work-based because it will lead to a null reference exception error.</span></span>
- <span data-ttu-id="ef2e2-133">Ao intentar navegar desde o formulario **Detalles da liña de oferta**, ao volver ao separador **Oferta**, o formulario actualízase e mostra o separador **Resumo**.</span><span class="sxs-lookup"><span data-stu-id="ef2e2-133">When attempting to navigate from the **Quote Line Details** form, back to the **Quote** tab, the form refreshes and displays the **Summary** tab.</span></span>
