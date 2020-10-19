---
title: Visión xeral dos gastos
description: Este tema ofrece información sobre a funcionalidade de gasto en Project Operations.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 6da831fef5dba060b8019d7689645405c7ebdbed
ms.sourcegitcommit: 0874b3d89e1dc0e65a51cedb82bf8f80831ca0bb
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/06/2020
ms.locfileid: "3967364"
---
# <a name="expense-home-page"></a><span data-ttu-id="7f08a-103">Páxina de inicio de gastos</span><span class="sxs-lookup"><span data-stu-id="7f08a-103">Expense home page</span></span>

<span data-ttu-id="7f08a-104">_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="7f08a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="7f08a-105">Dynamics 365 Project Operations admite a capacidade de procesar gastos.</span><span class="sxs-lookup"><span data-stu-id="7f08a-105">Dynamics 365 Project Operations supports the ability to process expenses.</span></span> <span data-ttu-id="7f08a-106">O procesamento de gastos prodúcese con ou sen proxectos mediante un fluxo de traballo personalizable de políticas, categorías de transaccións e aprobacións.</span><span class="sxs-lookup"><span data-stu-id="7f08a-106">Expense processing occurs with or without projects by using a customizable workflow of policies, transaction categories, and approvals.</span></span>

<span data-ttu-id="7f08a-107">En Project Operations, hai dous modelos de despregamento compatibles con gasto:</span><span class="sxs-lookup"><span data-stu-id="7f08a-107">In Project Operations, there are two supported deployment models for Expense:</span></span> 

- <span data-ttu-id="7f08a-108">**Completo**: Está dispoñible o despregamento completo para **Project Operations para situacións baseadas en recursos/sen fornecemento** ou **Project Operations para situacións baseadas en pedidos de produción**.</span><span class="sxs-lookup"><span data-stu-id="7f08a-108">**Full**: Full deployment is available for **Project Operations for resource/non-stocked based scenarios** or **Project Operations for production order based scenarios**.</span></span>
- <span data-ttu-id="7f08a-109">**Básico**: O despregamento básico está dispoñible para **Project Operations para situacións baseadas en recursos/sen fornecemento** e **Despregamento Lite: acordo para a facturación proforma**.</span><span class="sxs-lookup"><span data-stu-id="7f08a-109">**Basic**: Basic deployment is available for **Project Operations for resource/non-stocked based scenarios** and **Lite deployment – deal to proforma invoicing**.</span></span>

## <a name="full"></a><span data-ttu-id="7f08a-110">Completo</span><span class="sxs-lookup"><span data-stu-id="7f08a-110">Full</span></span> 
<span data-ttu-id="7f08a-111">O despregamento de gastos completos proporciona unha aplicación completa das políticas que inclúe a posibilidade de crear políticas, como:</span><span class="sxs-lookup"><span data-stu-id="7f08a-111">Full Expense deployment provides a complete policy enforcement which includes the ability to create policies, such as:</span></span>

  - <span data-ttu-id="7f08a-112">Límites de categorías de gasto</span><span class="sxs-lookup"><span data-stu-id="7f08a-112">Expense category limits</span></span>
  - <span data-ttu-id="7f08a-113">Viaxe</span><span class="sxs-lookup"><span data-stu-id="7f08a-113">Travel</span></span>
  - <span data-ttu-id="7f08a-114">Dietas</span><span class="sxs-lookup"><span data-stu-id="7f08a-114">Per diem</span></span>
  - <span data-ttu-id="7f08a-115">Importacións de tarxeta de crédito</span><span class="sxs-lookup"><span data-stu-id="7f08a-115">Credit card imports</span></span>
  - <span data-ttu-id="7f08a-116">Recoñecemento óptico de caracteres de recibos</span><span class="sxs-lookup"><span data-stu-id="7f08a-116">Receipt optical character recognition</span></span>

## <a name="basic"></a><span data-ttu-id="7f08a-117">Básico</span><span class="sxs-lookup"><span data-stu-id="7f08a-117">Basic</span></span> 
<span data-ttu-id="7f08a-118">O escenario de despregamento de gastos básicos só permite rexistrar os gastos básicos nun proxecto.</span><span class="sxs-lookup"><span data-stu-id="7f08a-118">Basic Expense deployment scenario only allows you to record basic expenses against a project.</span></span> 

<span data-ttu-id="7f08a-119">Para obter máis información, consulte [Entrada de gasto (lite)](basic-expense.md).</span><span class="sxs-lookup"><span data-stu-id="7f08a-119">For more information, see [Expense entry (lite)](basic-expense.md)</span></span>

## <a name="determine-your-expense-deployment"></a><span data-ttu-id="7f08a-120">Determinar o seu despregamento de gasto</span><span class="sxs-lookup"><span data-stu-id="7f08a-120">Determine your Expense deployment</span></span>
<span data-ttu-id="7f08a-121">Para determinar se está a executar o despregamento de xestión de gastos básicos, verifique que o enderezo URL remate con **. crm.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="7f08a-121">To determine if you're running the Basic Expense management deployment, verify that the address URL ends with **.crm.dynamics.com**.</span></span> 
