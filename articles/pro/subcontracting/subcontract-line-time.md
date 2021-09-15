---
title: Liñas de subcontrato para tempo
description: Este tema explica como rexistrar liñas de subcontrato para tempo e rexistrar a compra de tempo de fornecedores.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 10ebe0fcc86b4652ac01e28108361df1f768b61d
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323864"
---
# <a name="subcontract-lines-for-time"></a>Liñas de subcontrato para tempo

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

Un subcontrato en Dynamics 365 Project Operations pode ter unha liña de subcontrato para tempo. As liñas de subcontrato permiten ao xestor de proxectos mercar tempo de recursos do fornecedor para as tarefas do proxecto do persoal e os requisitos de recursos.

Para crear unha liña de subcontrato para tempo en Project Operations, complete os pasos seguintes.

1. No panel de navegación, seleccione **Subcontratos** e abra un subcontrato.
2. No separador **Liñas de subcontrato**, seleccione **Nova** para crear unha nova liña de subcontrato.
3. Na páxina **Creación rápida**, no campo **Clase de transacción**, seleccione **Tempo**.
4. Introduza a información do campo necesaria restante e, a seguir, seleccione **Gardar**.

  A seguinte táboa ofrece información sobre os campos na páxina de detalles **Liña de subcontrato** páxina e a páxina **Creación rápida**.

| **Campo** | **Descrición** |
| --- | --- |
| Nome | O nome da liña de subcontrato. |
| Descripción | Unha breve descrición dos servizos que se van comprar na liña de subcontrato. | 
| Tipo de liña | Este campo é un valor predefinido.  |
| Método de facturación | Seleccione o método de facturación. En función do método de facturación da liña de subcontrato de referencia, está dispoñible unha programación de facturas baseada en fitos para o método de facturación a prezo fixo. |
| Clase de transacción | Este campo é un valor predefinido que indica se se usa a liña de subcontrato para rexistrar unha compra de tempo de subcontratista. |
| Rol | O rol dos recursos de subcontrato cuxo tempo se está a mercar. A función atribuída aos recursos de subcontrato determina o custo da compra. |
| Inicio solicitado | A data na que se requiren os recursos do subcontratista para comezar a traballar. O inicio solicitado úsase para escoller unha lista de prezos do proxecto das listas de prezos do proxecto anexadas ao subcontrato. O custo do rol na liña de subcontrato é o predefinido desa lista de prezos. |
| Finalización solicitada | A data na que remata a atribución dos recursos do subcontratista. Esta data úsase para amosar advertencias cando un xestor de proxectos está sacando desta capacidade para os requisitos de recursos que se produzan despois desta data. |
| Cantidade solicitada | O número de horas do rol que se vai comprar ao fornecedor. Este valor úsase para amosar advertencias cando un xestor de proxectos está superando esta capacidade para os requisitos de recursos. |
| Grupo de unidades | Este valor de campo predefinido é o grupo de unidades de tempo e non se pode cambiar.  |
| Unidade | Este campo predefinido é a unidade base de horas do grupo de unidades de tempo. Pode cambiar este valor para mercar calquera unidade do grupo de unidades de tempo, como o día ou a semana. A combinación de rol e unidade úsase para calcular o prezo unitario para a liña de subcontrato. |
| Prezo por unidade | O valor do campo do prezo unitario é o predefinido a partir da combinación de rol e unidade da lista de prezos do proxecto que é aplicable para a data de inicio solicitada da liña de subcontrato. Cando a lista de prezos do proxecto aplicable ten o prezo configurado nunha unidade diferente á unidade da liña de subcontrato, o sistema utiliza a conversión unitaria para calcular o prezo por unidade. |
| Subtotal | Este é un campo de só lectura que se calcula automaticamente como **Cantidade x Prezo unitario** se se introducen tanto os valores de cantidade como os do prezo unitario. Se o campo cantidade, o prezo unitario ou ambos están baleiros, pode introducir un valor no campo. |
| Imposto de vendas |  Introduza o importe do imposto de vendas. |
| Cantidade total | Inclúese o importe total da liña de subcontrato despois de impostos. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
