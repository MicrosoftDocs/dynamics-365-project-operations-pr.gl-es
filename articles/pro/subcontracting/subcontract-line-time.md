---
title: Liñas de subcontrato para tempo
description: Este artigo explica como rexistrar liñas de subcontratación para o tempo e rexistrar a compra de tempo dos provedores.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3ba013dd7ad023acc4f0cf077099c8c2c8d5bcd8
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522230"
---
# <a name="subcontract-lines-for-time"></a>Liñas de subcontrato para tempo

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Un subcontrato en Dynamics 365 Project Operations pode ter unha liña de subcontrato para tempo. As liñas de subcontrato permiten ao xestor de proxectos mercar tempo de recursos do fornecedor para as tarefas do proxecto do persoal e os requisitos de recursos.

Para crear unha liña de subcontrato para tempo en Project Operations, complete os pasos seguintes.

1. No panel de navegación, seleccione **Subcontratos** e abra un subcontrato.
2. No separador **Liñas de subcontrato**, seleccione **Nova** para crear unha nova liña de subcontrato.
3. Na páxina **Creación rápida**, no campo **Clase de transacción**, seleccione **Tempo**.
4. Introduza a información do campo necesaria restante e, a seguir, seleccione **Gardar**.

  A seguinte táboa ofrece información sobre os campos na páxina de detalles **Liña de subcontrato** páxina e a páxina **Creación rápida**.

| **Campo** | **Descrición** | **Impacto funcional** |
| --- | --- | --- |
| Nome | Nome da liña de subcontrato para axudar na identificación. | Esta amosarase como a primeira columna en todas as buscas baseadas en liñas de subcontrato. |
| Descripción | Unha breve descrición dos servizos que se van comprar na liña de subcontrato. |Nada |
| Tipo de liña |   Este campo ten un valor predefinido de **Baseado na cantidade**.| Nada |
| Método de facturación | Este é un conxunto de opcións que representa os dous principais modelos de contratación admitidos por Project Operations: **Prezo fixo** e **Tempo e Material**. | Segundo o método de facturación seleccionado, unha programación de facturas baseada en fitos está dispoñible para as liñas de subcontrato co método de facturación de prezo fixo. |
| Clase de transacción | O valor predefinido é **Tempo**. | Isto indica que a liña de subcontrato estase a empregar para rexistrar unha compra de tempo de subcontratista. |
| Rol | Seleccione o rol dos recursos de subcontrato cuxo tempo se está a mercar. | O rol desempeñado polos recursos de subcontrato determina o custo da compra. |
| Inicio solicitado | Introduza a data na que se requiren os recursos do subcontratista para comezar a traballar. | Isto úsase para escoller unha lista de prezos do proxecto das listas de prezos do proxecto anexas ao subcontrato. O custo do rol na liña de subcontrato procede desa lista de prezos. |
| Finalización solicitada | Introduza a data na que finaliza a atribución do recurso de subcontratista. | Isto empregarase para amosar avisos cando un xestor de proxectos estea aproveitando a capacidade para os requisitos de recursos que se producen despois desta data. |
| Cantidade solicitada | Introduza o número de horas de compra do rol ao fornecedor. | Isto empregarase para amosar avisos cando un xestor de proxectos estea aproveitando a capacidade para os requisitos de recursos. |
| Grupo de unidades | O valor predefinido é **Grupo de unidades de tempo**, que non se pode cambiar. | Nada|
| Unidade | O valor predefinido para este campo é a unidade base de horas do **Grupo de unidades de tempo**. Pode cambiar este valor para mercar calquera unidade do **grupo de unidades de tempo**, como o día ou a semana. | A combinación de **Rol** e **Unidade** usarase como predefinida ou computada para o prezo unitario da liña de subcontrato. |
| Prezo por unidade | O prezo unitario predefinido usa a combinación de **Rol** e **Unidade** da lista de prezos do proxecto aplicable para a data de **inicio solicitado** da liña de subcontrato. | Cando a lista de prezos do proxecto aplicable ten o prezo configurado nunha unidade diferente á unidade da liña de subcontrato, o sistema utiliza a conversión unitaria para calcular o prezo por unidade. |
| Subtotal |    Este é un campo de só lectura que se calcula como Cantidade x Prezo unitario, se se introducen tanto a cantidade como os valores do prezo unitario. Se o campo cantidade, o prezo unitario ou ambos están baleiros, pode introducir un valor no campo. | Nada|
| Imposto de vendas |   Introduza o importe do imposto de vendas. |Nada |
| Cantidade total | O importe total da liña de subcontrato, incluídos os impostos. Este campo calcúlase como Subtotal + Imposto sobre as vendas.|Nada |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
