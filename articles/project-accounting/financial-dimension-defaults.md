---
title: Valores predefinidos das dimensións financeiras
description: Este tema ofrece información sobre como configurar valores predefinidos de dimensións financeiras.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 03b9a9028c1610b191db9c1bfb0163adc88bdf3e
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642361"
---
# <a name="financial-dimension-defaults"></a>Valores predefinidos das dimensións financeiras

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Operations usa o marco [Dimensións financeiras](https://docs.microsoft.com/dynamics365/finance/general-ledger/financial-dimensions) en Dynamics 365 Finance para proporcionar información adicional sobre as transaccións do libro maior e do libro auxiliar do proxecto.

As dimensións financeiras predefinidas pódense establecer nun cliente, fonte de financiamento do proxecto, fito, liña de contrato de proxecto ou proxecto.

## <a name="define-default-financial-dimensions-for-a-customer"></a>Definir dimensións financeiras por defecto para un cliente

Os valores predefinidos das dimensións do cliente especifícanse en Finance. Complete os seguintes pasos para establecer os valores predefinidos das dimensións.

1. Vaia a **Contas pendentes de cobro** > **Clientes** > **Todos os clientes**.
2. Na páxina **Clientes**, no separador **Dimensións financeiras**, defina os valores das dimensións financeiras para un cliente específico.

## <a name="define-default-financial-dimensions-for-project-contracts"></a>Definir dimensións financeiras por defecto para contratos de proxecto

Os contratos de proxecto créanse e mantéñense en Common Data Service (CDS). Os atributos de contabilidade para os contratos de proxecto configúranse no módulo **Xestión e contabilidade de proxectos** en Finance.

### <a name="set-financial-dimensions-for-a-project-funding-source"></a>Establecer dimensións financeiras para unha fonte de financiamento do proxecto

1. Vaia a **Xestión e contabilidade de proxectos** > **Proxectos** > **Contratos de proxecto**.
2. Seleccione o rexistro que desexa actualizar e no separador **Contrato de proxecto**, seleccione **Mostrar contabilidade predefinida**.
3. Expanda **Información relacionada** e seleccione o separador **Fontes de financiamento**.
4. Estableza os valores predefinidos das dimensións financeiras. Teña en conta que as dimensións financeiras predefínense na conta do cliente.

### <a name="set-financial-dimensions-for-a-project-contract-line"></a>Establecer dimensións financeiras para unha liña de contrato de proxecto

1. Vaia a **Xestión e contabilidade de proxectos** > **Proxectos** > **Contratos de proxecto**.
2. Seleccione o rexistro que desexa actualizar e no separador **Contrato de proxecto**, seleccione **Mostrar contabilidade predefinida**.
3. Expanda **Información relacionada** e seleccione o separador **Liñas de contrato**.
4. Estableza os valores predefinidos das dimensións financeiras. Os valores predefinidos das dimensións financeiras son aplicables e só se poden empregar con liñas de contrato de prezo fixo (fito).

Estes valores predefinidos úsanse en transaccións en conta de proxectos e liñas de facturación relacionadas.

## <a name="define-default-financial-dimensions-for-projects"></a>Definir dimensións financeiras por defecto para proxectos

Os proxectos créanse e mantéñense en (CDS). Os atributos de contabilidade para os proxectos configúranse no módulo **Xestión e contabilidade de proxectos** en Finance.

1. Vaia a **Xestión e contabilidade de proxectos** > **Proxectos** > **Todos os proxectos**.
2. Seleccione o rexistro que desexa actualizar e no separador **Proxecto**, seleccione **Mostrar contabilidade predefinida**.
3. Expanda **Información relacionada** e seleccione o separador **Configuración**.
4. Estableza os valores predefinidos das dimensións financeiras. Teña en conta que as dimensións financeiras predefínense na conta do cliente. Se o proxecto está asociado a unha liña de contrato con varios clientes de contrato de proxecto, o cliente principal úsase para as dimensións financeiras predefinidas.

As dimensións financeiras predefinidas do proxecto úsanse para establecer os valores predefinidos da liña de diario para transaccións de tempo, gastos e taxas no **Diario de Project Operations Integration** e nas liñas de factura de proxecto relacionadas.
