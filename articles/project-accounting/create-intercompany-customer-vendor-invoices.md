---
title: Crear facturas entre empresas de clientes e fornecedores
description: Este tema ofrece información sobre como crear facturas de clientes e fornecedores entre empresas.
author: sigitac
manager: tfehr
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: f1560469d2bdbb8e81dc26c16b272c44446ab20a
ms.sourcegitcommit: addbe0647619413e85e7cde80f6a21db95ab623e
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 11/20/2020
ms.locfileid: "4595468"
---
# <a name="create-intercompany-customer-and-vendor-invoices"></a>Crear facturas entre empresas de clientes e fornecedores

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Un contable do proxecto nunha entidade legal prestamista crea unha factura de cliente entre empresas polos custos do proxecto que se están a transferir á entidade prestameira. Despois de que se aproba e contabiliza a factura de cliente entre empresas, a entidade legal prestamista envía a factura entre empresas á entidade legal prestameira.

O contable do proxecto da entidade legal prestamista pode configurar un proceso por lotes para xerar facturas entre empresas de forma recorrente. O contable do proxecto especifica os criterios, como proxectos específicos, para crear facturas entre empresas nun lote.

## <a name="manually-create-an-intercompany-customer-invoice-for-project-transactions"></a>Crear manualmente unha factura de cliente entre empresas para as transaccións do proxecto 

Utilice este procedemento para crear manualmente unha factura de cliente entre empresas para as transaccións do proxecto. Busque as horas contabilizadas polos traballadores en proxectos das entidades legais prestameiras e polos gastos nos que a súa entidade legal incorreu en nome das persoas legais prestameiras. Pode buscar por nome da entidade legal, número do contrato do proxecto, número do proxecto, intervalo de datas ou calquera combinación destas opcións. Nos resultados da busca, seleccione as transaccións que desexe engadir a unha factura entre empresas.

1. En Dynamics 365 Finance, vaia a **Xestión e contabilidade de proxectos** > **Facturas do proxecto** > **Facturas de clientes entre empresas**. Na páxina de lista **Facturas de clientes entre empresas**, no Panel de acción, seleccione **Novo.**
2. Na páxina **Crear factura entre empresas**, no campo **Entidade legal**, seleccione unha entidade legal prestameira.
3. Opcional: Introduza un contrato de proxecto e un número de proxecto específicos.
4. Limite a busca seleccionando un intervalo de datas. Insira datas específicas nos campos **Data de inicio** e **Data de finalización**. Nos resultados da busca só se amosan as transaccións entre empresas que se contabilicen dentro deste intervalo de datas.
5. Estableza **Parámetro de liña de diario avanzada do proxecto** en **Si** e seleccione **Buscar**.
6. Nos resultados da busca, seleccione as transaccións que desexa incluír na proposta de factura entre empresas e, a continuación, seleccione **Aceptar**.
7. Na páxina **Factura de cliente entre empresas**, móstranse as transaccións do proxecto entre empresas que seleccionou entre os resultados da busca. Para modificar as transaccións antes de enviar a factura á entidade prestameira, faga o seguinte:
  
    1. Abra a páxina **Crear proposta de factura**. Seleccione as transaccións entre empresas adicionais para a factura actual e logo seleccione **Engadir liña**.
    2. Para eliminar unha liña, selecciónea e logo seleccione **Eliminar**.
    3. Vexa comentarios, motivos, dimensións financeiras e outra información sobre unha liña seleccionada no separador rápido **Liñas de factura**.
    
8. Para contabilizar a factura de cliente entre empresas, no Panel de acción seleccione **Contabilizar**.

> [!NOTE]
> Se a súa organización require que se revisen as facturas entre empresas antes de que se contabilicen, un administrador do sistema podería configurar un fluxo de traballo para as facturas entre empresas. Se non se configura un fluxo de traballo para as facturas entre empresas, pode contabilizar a factura entre empresas.

## <a name="create-a-batch-job-for-intercompany-invoices"></a>Crear un traballo por lotes para as facturas entre empresas

Pode crear varias facturas entre empresas ao mesmo tempo para todas as entidades legais prestameiras. Usando a funcionalidade de busca, pode buscar, por exemplo, todas as transaccións contabilizadas por traballadores en préstamo e relacionadas con proxectos xestionados por outras entidades legais. Despois, para cada entidade legal prestameira, pode crear unha factura entre empresas para as transaccións proporcionadas nos resultados da busca.

1. Vaia a **Xestión e contabilidade de proxectos** > **Periódico** > **Facturas de proxecto** > **Crear facturas de clientes entre empresas**.
2. Na páxina **Crear facturas de clientes entre empresas**, no campo **Empresa**, seleccione unha entidade legal para facturar. Se non selecciona unha empresa, mostraranse todas as transaccións que cumpran os criterios de busca para todas as entidades legais prestameiras.
3. En **Crear unha factura por**, seleccione se desexa crear unha factura para transaccións entre empresas baseada nun proxecto ou baseada nunha entidade legal prestameira.
4. Opcional: Para seleccionar un proxecto específico e un contrato de proxecto para crear facturas entre empresas, prema **Seleccionar**. Na páxina **Consulta**, no campo **Criterios**, seleccione o contrato do proxecto, o número do proxecto ou ambos e logo seleccione **Aceptar**.
5. No separador **Lote**, configure un proceso por lotes para crear facturas entre empresas de forma recorrente. Para obter máis información, consulte [Enviar un traballo de procesamento por lotes desde un formulario](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/submit-a-batch-processing-job-from-a-form).
6. Para contabilizar facturas entre empresas, no Panel de acción seleccione **Contabilizar**.

> [!NOTE]
> Se a súa organización require que se revisen as facturas entre empresas antes de que se contabilicen, un administrador do sistema podería configurar un fluxo de traballo para as facturas entre empresas. Se non se configura un fluxo de traballo para as facturas entre empresas, pode contabilizar facturas entre empresas.

## <a name="post-the-intercompany-vendor-invoice"></a>Contabilizar factura de fornecedor entre empresas

Un contable do proxecto da entidade legal prestameira pode revisar as facturas de fornecedor pendentes entre empresas cando se contabilice a correspondente factura de cliente entre empresas. En Finance, na entidade legal prestameira, vaia a **Contas pendentes de pago** > **Facturas** > **Factura de fornecedor pendente**. O número de factura pendente coincidirá co número de factura de cliente entre empresas. Comprobe que a factura é correcta e logo contabilícea. A contabilización da factura de fornecedor entre empresas crea un subprograma de proxecto e unha transacción de libro maior que reflicte os custos de transacción na entidade legal prestameira.


[!INCLUDE[footer-include](../includes/footer-banner.md)]