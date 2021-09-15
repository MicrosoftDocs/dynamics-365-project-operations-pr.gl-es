---
title: Detalles da cabeceira para subcontratos
description: Este tema explica a funcionalidade proporcionada na cabeceira de subcontrato en Project Operations.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 49158af1a430033db3a5db57a840512c45bc17e2
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323639"
---
# <a name="header-details-for-subcontracts"></a>Detalles da cabeceira para subcontratos

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

Este tema explica a funcionalidade proporcionada na cabeceira de subcontrato en Dynamics 365 Project Operations.

Como un xestor de proxectos planifica e executa proxectos, pode empregar subcontratistas e mercar produtos e servizos a fornecedores. Cando un xestor de proxectos precisa mercar produtos ou servizos, pode crear un subcontrato en Project Operations.

Para crear un subcontrato, complete os seguintes pasos.

1. No panel de navegación, seleccione **Subcontratos**, e na páxina **Subcontrato**, seleccione **Novo**.
2. Introduza a información necesaria e, a seguir, seleccione **Gardar**.

    A seguinte táboa ofrece información sobre os campos da páxina de cabeceira de subcontrato.

    | **Campo** | **Descrición** |
    | --- | --- | 
    | Nome | O nome do subcontrato. |
    | Descripción | Unha breve descrición dos servizos e produtos que se van mercar no subcontrato. |
    | Fornecedor | O nome da empresa á que se van mercar os produtos e servizos. Este rexistro de conta ten un tipo de relación de **Fornecedor** ou **Provedor**. |
    | Data do subcontrato | A data na que se crea o subcontrato. |
    | Motivo para o estado | O estado do subcontrato. |
    | Moeda | A moeda na que se mercan produtos e servizos. O valor neste campo é o predefinido na conta do provedor, pero se pode cambiar. As listas de prezos do proxecto que se usan para fixar o prezo dos produtos e servizos do subcontrato deberían estar nesta moeda. As listas de prezos en calquera outra moeda non se poden asociar ao subcontrato. O custo dos produtos e servizos incorrido neste subcontrato rexistrarase no proxecto nesta moeda. |
    | Unidade de contratación | A división da empresa que vai celebrar un contrato de compra ou un subcontrato co fornecedor. |
    | Condicións de pagamento | As condicións de pagamento das facturas do fornecedor que se emiten neste subcontrato. O valor neste campo é o predefinido no rexistro da conta do fornecedor. |
    | Enderezo de pagamento | O enderezo onde se envía o pagamento das facturas do fornecedor. O valor neste campo é o predefinido no rexistro da conta do fornecedor. |
    | Nome de facturación | O nome da persoa ou división da empresa do fornecedor que enviará a factura. O valor neste campo é o predefinido no rexistro da conta do fornecedor e usarase como nome do contacto principal nas facturas do fornecedor creadas para este subcontrato. |
    | Enderezo de facturación | O enderezo usado nas facturas deste fornecedor. O valor neste campo é o predefinido no rexistro da conta do fornecedor. Este enderezo tamén se usa como factura do enderezo nas facturas do provedor creadas para este subcontrato. |
    | Subtotal | Se un subcontrato non ten liñas, introduza neste campo un valor que denote o subtotal do pedido antes de impostos. Se o subcontrato ten liñas, este campo só será de lectura. A cantidade mostrada é a cantidade subtotal de todas as liñas do subcontrato. |
    | Imposto total | Se un subcontrato non ten liñas, introduza neste campo un valor que denote os impostos deste subcontrato. Se o subcontrato ten liñas, este campo só será de lectura. A cantidade mostrada é a suma da cantidade de impostos de todas as liñas do subcontrato. |
    | Cantidade total |  Este campo calculado mostra o importe total do subcontrato despois de incluír os impostos.  |
    | Data confirmada | A data na que se confirmou o subcontrato.  |
    | Solicitado por | O valor predefinido deste campo é o nome do usuario que crea o subcontrato. Este valor pode ser modificado polo creador do subcontrato para indicar á persoa en nome da que está a crear o subcontrato.  |
    | Xestor de contas do fornecedor | O nome do contacto principal da conta do fornecedor. O valor neste campo é o predefinido no rexistro da conta do fornecedor. O usuario pode cambiar este valor de campo para seleccionar un contacto diferente como xestor de contas do fornecedor do subcontrato. Este contacto pode configurar e enviar alertas por correo electrónico e negociacións de prezos. |


