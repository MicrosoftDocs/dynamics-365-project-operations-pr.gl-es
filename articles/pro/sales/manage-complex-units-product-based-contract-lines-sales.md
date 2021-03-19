---
title: Xestionar unidades complexas para liñas de contrato baseado en produto - lite
description: Este tema ofrece información sobre como apoiar a venda de produtos baseados en subscrición.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 029d2aa4fd20fc036a34ae6136fe12454f3b7703
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273331"
---
# <a name="manage-complex-units-for-product-based-contract-lines---lite"></a><span data-ttu-id="1d80a-103">Xestionar unidades complexas para liñas de contrato baseado en produto - lite</span><span class="sxs-lookup"><span data-stu-id="1d80a-103">Manage complex units for product-based contract lines - lite</span></span>

<span data-ttu-id="1d80a-104">_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="1d80a-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1d80a-105">Dynamics 365 Project Operations usa factores de cantidade para apoiar a venda de produtos baseados en subscrición.</span><span class="sxs-lookup"><span data-stu-id="1d80a-105">Dynamics 365 Project Operations uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="1d80a-106">Para os produtos baseados en subscrición, a cantidade na liña de contrato ou de contrato de proxecto exprésase como o número de meses de usuario.</span><span class="sxs-lookup"><span data-stu-id="1d80a-106">For subscription-based products, the quantity on the contract or project contract line is expressed as the number of user-months.</span></span>

<span data-ttu-id="1d80a-107">O prezo do software de subscrición almacénase no catálogo como o prezo por usuario ao mes.</span><span class="sxs-lookup"><span data-stu-id="1d80a-107">The price of subscription software is stored in the catalog as the price per-user, per-month.</span></span> <span data-ttu-id="1d80a-108">Durante o proceso de vendas, o prezo na liña de contrato adoita ser o prezo por usuario, por mes que foi negociado e descontado polo axente de vendas.</span><span class="sxs-lookup"><span data-stu-id="1d80a-108">During the sales process, the price on the contract line is usually the per-user, per-month price that was negotiated and discounted by the sales agent.</span></span> <span data-ttu-id="1d80a-109">Cada acordo ten un número diferente de usuarios e un número diferente de meses de subscrición.</span><span class="sxs-lookup"><span data-stu-id="1d80a-109">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="1d80a-110">A cantidade que se utiliza para calcular a cantidade da liña de contrato é un produto do número de usuarios e do número de meses de subscrición.</span><span class="sxs-lookup"><span data-stu-id="1d80a-110">The quantity used to calculate the amount of the contract line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="1d80a-111">Para apoiar este tipo de venda, Project Operations admite o concepto de *factores de cantidade*.</span><span class="sxs-lookup"><span data-stu-id="1d80a-111">To support this type of sale, Project Operations supports the concept of *quantity factors*.</span></span> <span data-ttu-id="1d80a-112">Os factores de cantidade dependen dos atributos do produto.</span><span class="sxs-lookup"><span data-stu-id="1d80a-112">Quantity factors rely on product attributes.</span></span> <span data-ttu-id="1d80a-113">Ao configurar propiedades específicas para un produto, pode marcar un subconxunto destas propiedades ou de todas as propiedades como factores de cantidade.</span><span class="sxs-lookup"><span data-stu-id="1d80a-113">When you configure specific properties for a product, you can flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="1d80a-114">Project Operations valida que só as propiedades numéricas ou propiedades de produto que teñen un tipo de datos numéricos estean marcadas como factores de cantidade.</span><span class="sxs-lookup"><span data-stu-id="1d80a-114">Project Operations validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="1d80a-115">Cando un produto con factores de cantidade configurados se engade a unha liña de contrato, o campo **Cantidade** convértese en só de lectura.</span><span class="sxs-lookup"><span data-stu-id="1d80a-115">When a product with configured quantity factors is added to a contract line, the **Quantity** field  becomes read-only.</span></span> <span data-ttu-id="1d80a-116">Despois de introducir valores para as propiedades do produto que son factores de cantidade, Project Operations calcula a cantidade da liña de contrato.</span><span class="sxs-lookup"><span data-stu-id="1d80a-116">After you enter values for product properties that are quantity factors, Project Operations calculates the quantity of the contract line.</span></span>

<span data-ttu-id="1d80a-117">Por exemplo, Dynamics 365 Sales pode ter as seguintes propiedades:</span><span class="sxs-lookup"><span data-stu-id="1d80a-117">For example, Dynamics 365 Sales might have the following properties:</span></span>

- <span data-ttu-id="1d80a-118">**N.º de usuarios**: O número de usuarios.</span><span class="sxs-lookup"><span data-stu-id="1d80a-118">**No of users**: The number of users.</span></span>
- <span data-ttu-id="1d80a-119">**Nº de meses**: O número de meses de subscrición.</span><span class="sxs-lookup"><span data-stu-id="1d80a-119">**No of Months**: The number of subscription months.</span></span>
- <span data-ttu-id="1d80a-120">**SKU do produto**: A unidade de mantemento de stock (SKU) do produto.</span><span class="sxs-lookup"><span data-stu-id="1d80a-120">**Product SKU**: The stock keeping unit (SKU) for the product.</span></span>

<span data-ttu-id="1d80a-121">As propiedades **N.º de Usuarios** e **N.º de meses** pódense marcar como factores de cantidade editando as propiedades da liña de produtos.</span><span class="sxs-lookup"><span data-stu-id="1d80a-121">The **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span>

<span data-ttu-id="1d80a-122">Para crear factores de cantidade a partir das propiedades do produto, complete os seguintes pasos.</span><span class="sxs-lookup"><span data-stu-id="1d80a-122">To create quantity factors from product properties, complete the following steps.</span></span>

1. <span data-ttu-id="1d80a-123">En **Project Operations**, seleccione **Produtos de vendas**.</span><span class="sxs-lookup"><span data-stu-id="1d80a-123">On the **Project Operations**, select **Sales-Products**.</span></span>
2. <span data-ttu-id="1d80a-124">Abra o produto para o que precisa configurar factores de cantidade.</span><span class="sxs-lookup"><span data-stu-id="1d80a-124">Open the product for which you need to set up quantity factors.</span></span> <span data-ttu-id="1d80a-125">Asegúrese de que o produto xa ten propiedades configuradas.</span><span class="sxs-lookup"><span data-stu-id="1d80a-125">Make sure that the product has properties already set up.</span></span>
3. <span data-ttu-id="1d80a-126">Na páxina **Información do proxecto**, seleccione o separador **Factores de cantidade**.</span><span class="sxs-lookup"><span data-stu-id="1d80a-126">On the **Project Information** page, select the **Quantity Factors** tab.</span></span>
4. <span data-ttu-id="1d80a-127">Na subgrade, seleccione **+ Novo cálculo de campo**.</span><span class="sxs-lookup"><span data-stu-id="1d80a-127">In the subgrid, select **+ New field computation**.</span></span>
5. <span data-ttu-id="1d80a-128">Introduza o nome do **Factor de cantidade** e seleccione o valor da propiedade que se asigna ao cálculo de campo.</span><span class="sxs-lookup"><span data-stu-id="1d80a-128">Enter the name of the **Quantity Factor** and select the property value that maps to the field computation.</span></span>
6. <span data-ttu-id="1d80a-129">Garde e peche o formulario.</span><span class="sxs-lookup"><span data-stu-id="1d80a-129">Save and close the form.</span></span>
7. <span data-ttu-id="1d80a-130">Repita os pasos 2-6 para todas as propiedades que xuntas constituirán a cantidade da liña de contrato baseado en produto.</span><span class="sxs-lookup"><span data-stu-id="1d80a-130">Repeat steps 2-6 for all the properties that together will make up the quantity for the product-based contract line.</span></span>

<span data-ttu-id="1d80a-131">Con factores de cantidade configurados, cando o usuario crea unha liña de contrato para este produto, a cantidade da liña de contrato está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="1d80a-131">With quantity factors set up, when the user creates a contract line for this product, the quantity of the contract line is locked.</span></span> <span data-ttu-id="1d80a-132">A cantidade calcúlase como produto dos valores da propiedade para esa liña de contrato.</span><span class="sxs-lookup"><span data-stu-id="1d80a-132">The quantity is then calculated as a product of the property values for that contract line.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]