---
title: Configurar a integración de tarxetas de crédito
description: Este tema explica como traballar con transaccións con tarxeta de crédito relacionadas cos gastos.
author: suvaidya
manager: AnnBe
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 72ff98f5985af4362cde3c9914e0d20247f1f09a
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866681"
---
# <a name="set-up-credit-card-integration"></a><span data-ttu-id="df9fb-103">Configurar a integración de tarxetas de crédito</span><span class="sxs-lookup"><span data-stu-id="df9fb-103">Set up credit card integration</span></span>

<span data-ttu-id="df9fb-104">_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="df9fb-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="df9fb-105">As transaccións con tarxeta de crédito relacionadas cos gastos pódense configurar para que se importen automaticamente nunha programación periódica.</span><span class="sxs-lookup"><span data-stu-id="df9fb-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="df9fb-106">Como alternativa, as transaccións pódense importar manualmente cando sexan necesarias.</span><span class="sxs-lookup"><span data-stu-id="df9fb-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="df9fb-107">As transaccións con tarxeta de crédito impórtanse a través da entidade de datos de transaccións con tarxeta de crédito.</span><span class="sxs-lookup"><span data-stu-id="df9fb-107">The credit card transactions are imported through the credit card transactions data entity.</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="df9fb-108">Importar transaccións con tarxeta de crédito</span><span class="sxs-lookup"><span data-stu-id="df9fb-108">Import credit card transactions</span></span>

<span data-ttu-id="df9fb-109">Para importar transaccións con tarxeta de crédito, siga estes pasos:</span><span class="sxs-lookup"><span data-stu-id="df9fb-109">To import credit card transactions, follow these steps:</span></span>

1. <span data-ttu-id="df9fb-110">Na páxina **Transaccións con tarxeta de crédito**, seleccione **Importar transaccións**.</span><span class="sxs-lookup"><span data-stu-id="df9fb-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="df9fb-111">Se está a abrir a xestión de datos por primeira vez, o sistema debe actualizar a lista de entidades de datos antes de que poida continuar.</span><span class="sxs-lookup"><span data-stu-id="df9fb-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="df9fb-112">No campo **Nome**, introduza unha descrición única para o traballo de importación.</span><span class="sxs-lookup"><span data-stu-id="df9fb-112">In the **Name** field, enter a unique description for the import job.</span></span>
3. <span data-ttu-id="df9fb-113">No campo **Formato de datos de orixe**, seleccione o formato do ficheiro que contén as transaccións con tarxeta de crédito para importar.</span><span class="sxs-lookup"><span data-stu-id="df9fb-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="df9fb-114">Seleccione **Cargar** e, a seguir, busque e seleccione o ficheiro para importar.</span><span class="sxs-lookup"><span data-stu-id="df9fb-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="df9fb-115">Despois de cargar o ficheiro, valide a asignación do ficheiro de transacción con tarxeta de crédito e as columnas da entidade de datos de transaccións con tarxeta de crédito seleccionando a ligazón **Ver mapa** no mosaico.</span><span class="sxs-lookup"><span data-stu-id="df9fb-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="df9fb-116">Se hai erros de asignación ou se ten que cambiar a asignación, faga os cambios de asignación a partir de calquera separador de **Visualización de asignacións** ou o separador **Detalles de asignación**.</span><span class="sxs-lookup"><span data-stu-id="df9fb-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="df9fb-117">Para automatizar as transaccións con tarxeta de crédito, seleccione **Crear traballo de datos periódico**.</span><span class="sxs-lookup"><span data-stu-id="df9fb-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="df9fb-118">A seguir, pode definir a periodicidade que define a frecuencia coa que se deben importar as transaccións con tarxeta de crédito.</span><span class="sxs-lookup"><span data-stu-id="df9fb-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="df9fb-119">Ao concluír, seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="df9fb-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="df9fb-120">Para importar o ficheiro seleccionado agora, seleccione **Importar**.</span><span class="sxs-lookup"><span data-stu-id="df9fb-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="df9fb-121">Se se producen erros durante a importación, pode ver o rexistro de execución ou os datos intermedios para ver os erros que debe corrixir para garantir a importación.</span><span class="sxs-lookup"><span data-stu-id="df9fb-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help ensure a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="df9fb-122">Se precisa importar máis dun formato de ficheiro, debe crear traballos de importación separados para cada tipo de formato.</span><span class="sxs-lookup"><span data-stu-id="df9fb-122">If you need to import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="df9fb-123">Atribuír de novo as transaccións con tarxeta de crédito para empregados cesados</span><span class="sxs-lookup"><span data-stu-id="df9fb-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="df9fb-124">Despois de concluír un rexistro de empregado, desactívase a conta de Active Directory Domain Services (AD DS) do empregado.</span><span class="sxs-lookup"><span data-stu-id="df9fb-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="df9fb-125">Non obstante, pode haber transaccións con tarxeta de crédito activas que aínda se deben gastar e reembolsar.</span><span class="sxs-lookup"><span data-stu-id="df9fb-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="df9fb-126">Na páxina **Transaccións con tarxeta de crédito**, pode atribuír de novo o empregado para calquera transacción con tarxeta de crédito na que o empregado asociado fose despedido.</span><span class="sxs-lookup"><span data-stu-id="df9fb-126">On the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="df9fb-127">Seleccione unha ou máis transaccións con tarxeta de crédito e logo seleccione **Reatribuír transaccións**.</span><span class="sxs-lookup"><span data-stu-id="df9fb-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="df9fb-128">Despois pode seleccionar outro empregado ao que atribuír as transaccións con tarxeta de crédito.</span><span class="sxs-lookup"><span data-stu-id="df9fb-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="df9fb-129">Despois de reatribuír as transaccións con tarxeta de crédito, pódense seleccionar para un informe de gastos e pagarse mediante o proceso habitual de reembolso do informe de gastos.</span><span class="sxs-lookup"><span data-stu-id="df9fb-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>

## <a name="delete-credit-card-transactions"></a><span data-ttu-id="df9fb-130">Eliminar transaccións con tarxeta de crédito</span><span class="sxs-lookup"><span data-stu-id="df9fb-130">Delete credit card transactions</span></span> 

<span data-ttu-id="df9fb-131">Ás veces, despois de importar as transaccións con tarxeta de crédito, é posible que precise eliminar algunhas transaccións.</span><span class="sxs-lookup"><span data-stu-id="df9fb-131">Sometimes, after credit card transactions are imported, certain transactions may need to be deleted.</span></span> <span data-ttu-id="df9fb-132">Isto pode deberse a que as transaccións son duplicadas ou porque os datos poden non ser precisos.</span><span class="sxs-lookup"><span data-stu-id="df9fb-132">This could be because the transactions are duplicates or because the data might isn't accurate.</span></span> <span data-ttu-id="df9fb-133">Os administradores poden usar a funcionalidade **"Eliminar transaccións con tarxeta de crédito"** para seleccionar e eliminar as transaccións con tarxeta de crédito que **non estean anexas** a un informe de gastos.</span><span class="sxs-lookup"><span data-stu-id="df9fb-133">Admins can use the **"Delete credit card transactions"** feature to select and delete credit card transactions that are **not attached** to an expense report.</span></span> 

1. <span data-ttu-id="df9fb-134">Vaia a **Tarefas periódicas** > **Eliminar transaccións con tarxeta de crédito**.</span><span class="sxs-lookup"><span data-stu-id="df9fb-134">Go to **Periodic tasks** > **Delete credit card transactions**.</span></span>
2. <span data-ttu-id="df9fb-135">Seleccione **Filtro** e proporcione información para identificar os rexistros a incluír.</span><span class="sxs-lookup"><span data-stu-id="df9fb-135">Select **Filter** and provide information to identify the records to include.</span></span>
3. <span data-ttu-id="df9fb-136">Seleccione **Aceptar** para eliminar os rexistros.</span><span class="sxs-lookup"><span data-stu-id="df9fb-136">Select **OK** to delete the records.</span></span> 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
