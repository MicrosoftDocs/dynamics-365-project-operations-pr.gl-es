---
title: Configurar a integración de tarxetas de crédito
description: Neste tema explícase como importar e manter transaccións con tarxeta de crédito relacionadas cos gastos.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
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
ms.openlocfilehash: e0004f9096ea8a03745dbfce35fe0d32d3d707f6
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120856"
---
# <a name="set-up-credit-card-integration"></a><span data-ttu-id="a92f5-103">Configurar a integración de tarxetas de crédito</span><span class="sxs-lookup"><span data-stu-id="a92f5-103">Set up credit card integration</span></span>

<span data-ttu-id="a92f5-104">_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="a92f5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a92f5-105">As transaccións con tarxeta de crédito relacionadas cos gastos pódense configurar para que se importen automaticamente nunha programación periódica.</span><span class="sxs-lookup"><span data-stu-id="a92f5-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="a92f5-106">Como alternativa, as transaccións pódense importar manualmente cando sexan necesarias.</span><span class="sxs-lookup"><span data-stu-id="a92f5-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="a92f5-107">As transaccións con tarxeta de crédito importanse a través da entidade de datos de transaccións con tarxeta de crédito.</span><span class="sxs-lookup"><span data-stu-id="a92f5-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="a92f5-108">Importar transaccións con tarxeta de crédito</span><span class="sxs-lookup"><span data-stu-id="a92f5-108">Import credit card transactions</span></span>

1. <span data-ttu-id="a92f5-109">Na páxina **Transaccións con tarxeta de crédito**, seleccione **Importar transaccións**.</span><span class="sxs-lookup"><span data-stu-id="a92f5-109">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="a92f5-110">Se está a abrir a xestión de datos por primeira vez, o sistema debe actualizar a lista de entidades de datos antes de que poida continuar.</span><span class="sxs-lookup"><span data-stu-id="a92f5-110">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="a92f5-111">No campo **Nome**, introduza unha descrición única do traballo de importación.</span><span class="sxs-lookup"><span data-stu-id="a92f5-111">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="a92f5-112">No campo **Formato de datos de orixe**, seleccione o formato do ficheiro que contén as transaccións con tarxeta de crédito para importar.</span><span class="sxs-lookup"><span data-stu-id="a92f5-112">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="a92f5-113">Seleccione **Cargar** e, a seguir, busque e seleccione o ficheiro para importar.</span><span class="sxs-lookup"><span data-stu-id="a92f5-113">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="a92f5-114">Despois de cargar o ficheiro, valide a asignación do ficheiro de transacción con tarxeta de crédito e as columnas da entidade de datos de transaccións con tarxeta de crédito seleccionando a ligazón **Ver mapa** no mosaico.</span><span class="sxs-lookup"><span data-stu-id="a92f5-114">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="a92f5-115">Se hai erros de asignación ou se ten que cambiar a asignación, faga os cambios de asignación a partir de calquera separador de **Visualización de asignacións** ou o separador **Detalles de asignación**.</span><span class="sxs-lookup"><span data-stu-id="a92f5-115">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="a92f5-116">Para automatizar as transaccións con tarxeta de crédito, seleccione **Crear traballo de datos periódico**.</span><span class="sxs-lookup"><span data-stu-id="a92f5-116">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="a92f5-117">A seguir, pode definir a periodicidade que define a frecuencia coa que se deben importar as transaccións con tarxeta de crédito.</span><span class="sxs-lookup"><span data-stu-id="a92f5-117">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="a92f5-118">Ao concluír, seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="a92f5-118">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="a92f5-119">Para importar o ficheiro seleccionado agora, seleccione **Importar**.</span><span class="sxs-lookup"><span data-stu-id="a92f5-119">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="a92f5-120">Se se producen erros durante a importación, pode ver o rexistro de execución ou os datos intermedios para ver os erros que debe corrixir para axudar a garantir a importación.</span><span class="sxs-lookup"><span data-stu-id="a92f5-120">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="a92f5-121">Se debe importar máis dun formato de ficheiro, debe crear traballos de importación separados para cada tipo de formato.</span><span class="sxs-lookup"><span data-stu-id="a92f5-121">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="a92f5-122">Atribuír de novo as transaccións con tarxeta de crédito para empregados cesados</span><span class="sxs-lookup"><span data-stu-id="a92f5-122">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="a92f5-123">Despois de concluír un rexistro de empregado, desactívase a conta de Active Directory Domain Services (AD DS) do empregado.</span><span class="sxs-lookup"><span data-stu-id="a92f5-123">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="a92f5-124">Non obstante, pode haber transaccións con tarxeta de crédito activas que aínda se deben gastar e reembolsar.</span><span class="sxs-lookup"><span data-stu-id="a92f5-124">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="a92f5-125">Desde a páxina **Transaccións con tarxeta de crédito**, pode reatribuír ao empregado para calquera transacción con tarxeta de crédito na que o empregado asociado fose cesado.</span><span class="sxs-lookup"><span data-stu-id="a92f5-125">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="a92f5-126">Seleccione unha ou máis transaccións con tarxeta de crédito e logo seleccione **Reatribuír transaccións**.</span><span class="sxs-lookup"><span data-stu-id="a92f5-126">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="a92f5-127">Despois pode seleccionar outro empregado ao que atribuír as transaccións con tarxeta de crédito.</span><span class="sxs-lookup"><span data-stu-id="a92f5-127">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="a92f5-128">Despois de reatribuír as transaccións con tarxeta de crédito, pódense seleccionar para un informe de gastos e pagarse mediante o proceso habitual de reembolso do informe de gastos.</span><span class="sxs-lookup"><span data-stu-id="a92f5-128">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>
