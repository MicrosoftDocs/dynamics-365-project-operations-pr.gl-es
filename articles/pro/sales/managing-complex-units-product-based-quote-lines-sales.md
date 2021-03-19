---
title: Xestión de unidades complexas como por usuario, por mes para as liñas de oferta baseadas en produto - lite
description: Este tema ofrece información sobre a xestión de unidades complexas para liñas de oferta baseadas en produto.
author: rumant
manager: Annbe
ms.date: 10/06/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b4a075ae5a7329f241cc31afceab0e085c771f72
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272881"
---
# <a name="managing-complex-units-such-as-per-user-per-month-for-product-based-quote-lines---lite"></a><span data-ttu-id="abcd2-103">Xestión de unidades complexas como por usuario, por mes para as liñas de oferta baseadas en produto - lite</span><span class="sxs-lookup"><span data-stu-id="abcd2-103">Managing complex units such as per-user, per-month for product-based quote lines - lite</span></span>

<span data-ttu-id="abcd2-104">_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_</span><span class="sxs-lookup"><span data-stu-id="abcd2-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="abcd2-105">Dynamics 365 Project Operations usa factores de cantidade para apoiar a venda de produtos baseados en subscrición.</span><span class="sxs-lookup"><span data-stu-id="abcd2-105">Dynamics 365 Project Operations uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="abcd2-106">Para os produtos baseados en subscrición, a cantidade na liña de oferta ou contrato de proxecto exprésase como o número de meses de usuario.</span><span class="sxs-lookup"><span data-stu-id="abcd2-106">For subscription-based products, the quantity on the quote or project contract line is expressed as the number of user-months.</span></span>

<span data-ttu-id="abcd2-107">Normalmente, o prezo do software de subscrición almacénase no catálogo como o prezo por usuario ao mes.</span><span class="sxs-lookup"><span data-stu-id="abcd2-107">Usually, the price of subscription software is stored in the catalog as the price per user per month.</span></span> <span data-ttu-id="abcd2-108">Durante o proceso de vendas, o prezo na liña de oferta adoita ser o prezo por usuario, por mes que foi negociado e descontado polo axente de vendas de TI.</span><span class="sxs-lookup"><span data-stu-id="abcd2-108">During the sales process, the price on the quote line is usually the per-user, per-month price that was negotiated and discounted by the IT sales agent.</span></span> <span data-ttu-id="abcd2-109">Cada acordo ten un número diferente de usuarios e un número diferente de meses de subscrición.</span><span class="sxs-lookup"><span data-stu-id="abcd2-109">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="abcd2-110">A cantidade que se utiliza para calcular a liña de oferta é un produto do número de usuarios e do número de meses de subscrición.</span><span class="sxs-lookup"><span data-stu-id="abcd2-110">The quantity used to compute the quote line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="abcd2-111">Para apoiar este tipo de venda, Project Operations introduciu o concepto de factores de cantidade.</span><span class="sxs-lookup"><span data-stu-id="abcd2-111">To support this type of sale, Project Operations introduced the concept of quantity factors.</span></span> <span data-ttu-id="abcd2-112">Os factores de cantidade dependen dos atributos do produto en Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="abcd2-112">Quantity factors rely on the product attributes in Dynamics 365.</span></span> <span data-ttu-id="abcd2-113">Ao configurar propiedades específicas para un produto, Project Operations permítelle marcar un subconxunto ou todas as propiedades como factores de cantidade.</span><span class="sxs-lookup"><span data-stu-id="abcd2-113">When you configure specific properties for a product, Project Operations lets you flag a subset, or all of the properties, as quantity factors.</span></span>

<span data-ttu-id="abcd2-114">Project Operations valida que só as propiedades numéricas ou propiedades de produto que teñen un tipo de datos numéricos estean marcadas como factores de cantidade.</span><span class="sxs-lookup"><span data-stu-id="abcd2-114">Project Operations validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="abcd2-115">Cando engade un produto con factores de cantidade a unha liña de oferta, o campo **Cantidade** convértese en só de lectura.</span><span class="sxs-lookup"><span data-stu-id="abcd2-115">When you add a product with quantity factors to a quote line, the **Quantity** field becomes read-only.</span></span> <span data-ttu-id="abcd2-116">Despois de introducir valores para as propiedades do produto que son factores de cantidade, Project Operations calcula a cantidade da liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="abcd2-116">After you enter values for product properties that are quantity factors, Project Operations calculates the quantity of the quote line.</span></span>

<span data-ttu-id="abcd2-117">Por exemplo, Dynamics 365 Sales pode ter as seguintes propiedades:</span><span class="sxs-lookup"><span data-stu-id="abcd2-117">For example, Dynamics 365 Sales might have the following properties:</span></span>

- <span data-ttu-id="abcd2-118">**N.º de usuarios**: O número de usuarios</span><span class="sxs-lookup"><span data-stu-id="abcd2-118">**No of users**: The number of users</span></span>
- <span data-ttu-id="abcd2-119">**Nº de meses**: O número de meses de subscrición</span><span class="sxs-lookup"><span data-stu-id="abcd2-119">**No of Months**: The number of subscription months</span></span>
- <span data-ttu-id="abcd2-120">**SKU de produto**</span><span class="sxs-lookup"><span data-stu-id="abcd2-120">**Product SKU**</span></span>

<span data-ttu-id="abcd2-121">Pode marcar as propiedades **N.º de Usuarios** e **N.º de meses** como factores de cantidade editando as propiedades da liña de produtos.</span><span class="sxs-lookup"><span data-stu-id="abcd2-121">You can flag the **No of Users** and **No of Months** properties as quantity factors by editing the properties of the product line.</span></span>

<span data-ttu-id="abcd2-122">Para crear factores de cantidade a partir das propiedades do produto, siga estes pasos:</span><span class="sxs-lookup"><span data-stu-id="abcd2-122">To create Quantity factors from Product properties, follow these steps:</span></span>

1. <span data-ttu-id="abcd2-123">No panel de navegación esquerdo de Project Operations, vaia a **Vendas** > **Produtos**.</span><span class="sxs-lookup"><span data-stu-id="abcd2-123">On the Project Operations left navigation pane, go to **Sales** > **Products**.</span></span>
2. <span data-ttu-id="abcd2-124">Abra o produto para o que precisa configurar os factores de cantidade.</span><span class="sxs-lookup"><span data-stu-id="abcd2-124">Open the product for which you need to configure quantity factors.</span></span> <span data-ttu-id="abcd2-125">Asegúrese de que o produto xa ten propiedades configuradas.</span><span class="sxs-lookup"><span data-stu-id="abcd2-125">Make sure the product has properties already configured.</span></span>
3. <span data-ttu-id="abcd2-126">Na páxina **Información do proxecto** do produto, seleccione o separador **Factores de cantidade**.</span><span class="sxs-lookup"><span data-stu-id="abcd2-126">On the **Project Information** page for the Product, select the **Quantity Factors** tab.</span></span>
4. <span data-ttu-id="abcd2-127">Na subgrade, seleccione **+ Novo cálculo de campo**.</span><span class="sxs-lookup"><span data-stu-id="abcd2-127">In the subgrid, select **+ New field computation**.</span></span>
5. <span data-ttu-id="abcd2-128">Introduza o nome do factor de cantidade e seleccione o valor da propiedade que se asigna ao cálculo de campo.</span><span class="sxs-lookup"><span data-stu-id="abcd2-128">Enter the name of the Quantity factor and select the property value that maps to the field computation.</span></span>
6. <span data-ttu-id="abcd2-129">Garde e peche o formulario.</span><span class="sxs-lookup"><span data-stu-id="abcd2-129">Save and close the form.</span></span> <span data-ttu-id="abcd2-130">Repita estes pasos para todas as propiedades que se empregarán para calcular a cantidade da liña de oferta baseada en produto.</span><span class="sxs-lookup"><span data-stu-id="abcd2-130">Repeat these steps for all properties to use for computing the quantity for the product-based quote line.</span></span>

<span data-ttu-id="abcd2-131">Cando cree unha liña de oferta baseada en produto, bloquearase a cantidade da liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="abcd2-131">When you create a product-based quote line for a product, the quantity of the quote line will be locked.</span></span> <span data-ttu-id="abcd2-132">A cantidade calcularase como produto dos valores da propiedade que introduciu para esa liña de oferta.</span><span class="sxs-lookup"><span data-stu-id="abcd2-132">The quantity will be computed as a product of the property values that you input for that quote line.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]