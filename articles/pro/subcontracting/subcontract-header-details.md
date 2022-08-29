---
title: Detalles da cabeceira para subcontratos
description: Este artigo explica a funcionalidade proporcionada na cabeceira do subcontrato en Operacións do proxecto.
author: rumant
ms.date: 09/14/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: ce16b7a968bc7e6904411ae9e021a5ca1839d02e
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261415"
---
# <a name="header-details-for-subcontracts"></a>Detalles da cabeceira para subcontratos

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

Este artigo explica a funcionalidade proporcionada na cabeceira do subcontrato en Dynamics 365 Project Operations.

Como un xestor de proxectos planifica e executa proxectos, pode empregar subcontratistas e mercar produtos e servizos a fornecedores. Cando un xestor de proxectos precisa mercar produtos ou servizos, pode crear un subcontrato en Project Operations.

Para crear un subcontrato, complete os seguintes pasos.

1. No panel de navegación, seleccione **Subcontratos**, e na páxina **Subcontrato**, seleccione **Novo**.
2. Introduza a información necesaria e, a seguir, seleccione **Gardar**.

    A seguinte táboa ofrece información sobre os campos da páxina de **cabeceira de subcontrato**.

    | Campo | Descripción |Impacto funcional |
    |---|------|---| 
    | Nome | O nome do subcontrato. | En todas as listas despregables de subcontratos, o nome do subcontrato aparece na primeira columna para axudarlle a identificar o subcontrato. | 
    | Descripción | Unha breve descrición dos servizos e produtos que se van mercar no subcontrato. | Nada |
    | Fornecedor | O nome da empresa á que se van mercar os produtos e servizos. Este rexistro de conta ten un tipo de relación de **Fornecedor** ou **Provedor**. | En función do fornecedor seleccionado, os valores predefinidos introdúcense automaticamente para os seguintes campos:<br/> **• Moeda** </br> **• Listas de prezos** </br> **• Termos de pagamento**</br> **• Enderezo de pagamento**</br> **• Enderezo de facturación**</br> **• Nome de facturación** </br>**• Xestor de contas do fornecedor**|
    | Data do subcontrato | A data na que se crea o subcontrato. | A data de subcontratación úsase para seleccionar a lista de prezos de compra correcta entre as listas de prezos que se xuntan ao fornecedor relacionado ou entre os parámetros do proxecto. |
    | Motivo para o estado | O estado do subcontrato. | O estado determina onde se atopa o subcontrato no proceso comercial e se se pode editar. <br/>Os valores inclúen:<br>• **Borrador**: Pódese editar o subcontrato. Só pode editar subcontratos cun estado de **Borrador**.<br/>• **Confirmado**: A negociación co vendedor está completa e o subcontrato está aprobado para a súa entrega. <br/>• **Pechado**: A entrega do subcontrato está completa.<br/>• **Cancelado**: O subcontrato foi cancelado e non está prevista a entrega.  | 
    | Moeda | A moeda na que se mercan produtos e servizos. O valor predefinido introdúcese automaticamente desde a conta do fornecedor, pero pódese cambiar. | A moeda do subcontrato úsase para seleccionar a lista de prezos de compra entre as listas de prezos que se xuntan ao fornecedor relacionado ou entre os parámetros do proxecto. As listas de prezos noutra moeda non se poden asociar ao subcontrato. O custo de tempo, gastos e materiais que os recursos do vendedor entregan deste subcontrato rexístranse nesta moeda no proxecto. Despois de gardar o rexistro do subcontrato, a moeda do subcontrato non se pode cambiar.|
    | Unidade de contratación | A división da empresa que vai celebrar un contrato de compra ou un subcontrato co fornecedor. | Nada |
    | Condicións de pagamento | As condicións de pagamento das facturas do fornecedor que se emiten neste subcontrato. O valor predefinido introdúcese automaticamente desde o rexistro conta do fornecedor. | As condicións de pagamento do subcontrato copianse en todas as facturas do fornecedor relacionadas con este subcontrato. As condicións de pagamento pódense actualizar se o subcontrato ten un estado de **Borrador**. | 
    | Enderezo de pagamento | O enderezo do fornecedor ao que se deben enviar os pagamentos. O valor predefinido introdúcese automaticamente desde o rexistro conta do fornecedor. | O enderezo de pagamento do subcontrato copiase como o enderezo de pagamento a todas as facturas do fornecedor que se crean para este subcontrato. O enderezo de pagamento pódese actualizar se o subcontrato ten un estado de **Borrador**.|
    | Nome de facturación | O nome da persoa ou división da empresa do fornecedor que enviará a factura. O valor predefinido introdúcese automaticamente desde o rexistro conta do fornecedor. | O valor de **Nome de facturación** do subcontrato copiase en todas as facturas do fornecedor relacionadas con este subcontrato. Este campo pódese actualizar se o subcontrato ten un estado de **Borrador**.|
    | Enderezo de facturación | O enderezo que se usa nas facturas do fornecedor. O valor predefinido introdúcese automaticamente desde o rexistro conta do fornecedor. | Este enderezo é o enderezo de orixe das facturas do provedor que se crean para este subcontrato. |
    | Subtotal | Se un subcontrato non ten liñas, introduza o subtotal do pedido antes de impostos. Se o subcontrato ten liñas, este campo só será de lectura. A cantidade que se mostra é a cantidade subtotal de todas as liñas do subcontrato. | Nada |
    | Imposto total | Se un subcontrato non ten liñas, introduza os impostos totais deste subcontrato. Se o subcontrato ten liñas, este campo só será de lectura. A cantidade que se mostra é a suma do importe dos impostos de todas as liñas do subcontrato. | Nada |
    | Cantidade total | Este campo calculado mostra o importe total do subcontrato despois de incluír os impostos. | Nada |
    | Data confirmada | A data na que se confirmou o subcontrato. | Nada |
    | Solicitado por | Por defecto, este campo establécese no nome do usuario que crea o subcontrato. Non obstante, o creador do subcontrato pode cambiar o valor para indicar á persoa no nome da cal está a crear o subcontrato. | Nada |
    | Xestor de contas do fornecedor | O nome do contacto principal da conta do fornecedor. O valor predefinido introdúcese automaticamente desde o rexistro conta do fornecedor. Pode seleccionar un contacto diferente como xestor de contas do fornecedor do subcontrato. | Pode configurar alertas por correo electrónico para notificar ao contacto cando se realicen cambios no subcontrato como resultado das negociacións de prezos. |
