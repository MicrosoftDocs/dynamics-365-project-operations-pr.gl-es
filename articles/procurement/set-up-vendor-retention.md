---
title: Configurar a retención de fornecedores
description: Este tema explica como configurar a retención de fornecedores.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: e0cd7669c7d6b916261e2c85cce0f24ff241a075
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583702"
---
# <a name="set-up-vendor-retention"></a>Configurar a retención de fornecedores

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Este tema ofrece información sobre como configurar a retención de fornecedores.

## <a name="set-up-a-vendor-retention-account-in-general-ledger"></a>Configurar unha conta de retención de fornecedores no libro maior xeral

1. En Dynamics 365 Finance, vai a **Contabilidade Xeral** > **Configuración da publicación** > **Contas para transaccións automáticas**.
2. Engada unha liña nova.
3. No campo **Tipo de contabilización**, seleccione **Retención de fornecedores**.
4. Seleccione a conta principal para a contabilización de retención de fornecedores.

## <a name="create-vendor-retention-terms"></a>Crea condicións de retención de fornecedores

Use a páxina **Condicións de retención de fornecedores** para configurar e manter as condicións de retención para os pagos do fornecedor. Introduza a porcentaxe do pago do fornecedor a reter e a porcentaxe dos importes retidos anteriormente para liberar. As cantidades retéñense automaticamente nas facturas do fornecedor ata que o contrato alcanza o estado especificado de finalización. Despois de configurar as condicións de retención para un fornecedor, pode aplicalos a calquera proxecto no que traballe o fornecedor.

1. En Finance, vaia a **Xestión e contabilidade de proxectos** > **Configuración** > **Retención** > **Condicións de retención do pagamento de fornecedores**.
2. Seleccione **Novo** para engadir un novo termo de retención do fornecedor. O valor do campo **ID da regra** para a nova condición introdúcese automaticamente. 
3. No campo **Descrición**, introduce un nome descritivo para a nova condición.
4. No separador **Condicións**, seleccione **Engadir liña** para introducir unha condición de retención do fornecedor.
5. No campo **Porcentaxe de unidades entregadas**, introduza unha porcentaxe de finalización para a regra. As cantidades retéñense automaticamente nas facturas do fornecedor ata que a fase de finalización do proxecto sexa igual á porcentaxe que introduza. Por exemplo, se introduce 50,00, as cantidades retéñense ata que o proxecto se complete nun 50 por cento.
6. No campo **Porcentaxe a reter**, introduza a porcentaxe do importe da factura do fornecedor a reter. Por exemplo, se introduce 10,00 neste campo, o 10 por cento do importe das facturas do fornecedor retense ata que o proxecto alcance a porcentaxe de finalización que seleccione no campo **Porcentaxe de unidades entregadas**.
7. No campo **Porcentaxe a liberar**, introduza a porcentaxe de cantidades retidas anteriormente para liberar no nivel seleccionado de finalización do proxecto.

> [!NOTE]
> Se ten máis dun fito para os diferentes niveis de finalización do proxecto, introduza unha liña de condición de retención do fornecedor separada para cada regra de retención. Cada liña pode especificar unha porcentaxe diferente a reter e unha porcentaxe diferente a liberar para cada nivel designado de finalización do proxecto.

## <a name="set-up-a-vendor-agreement-for-the-project"></a>Configurar un acordo de fornecedor para o proxecto

Configure as condicións de retención do fornecedor que se aplican ao proxecto. Os termos de retención do fornecedor tamén se mostran nos pedidos de compra que cree para o fornecedor.

1. En Finance, vaia a **Xestión e contabilidade de proxectos** > **Proxectos** > **Todos os proxectos**. 
2. Seleccione un proxecto e, no panel de acción, seleccione **Grupo do proxectos** > **Acordos de fornecedores**.
3. Na páxina **Acordos de fornecedores**, engada unha nova liña.
4. No campo **Código de conta**, seleccione unha das seguintes opcións:
   - **Táboa**: Os termos de retención do fornecedor aplícanse a un único fornecedor.
   - **Grupo**: Os termos de retención do fornecedor aplícanse a todos os fornecedores dun grupo de fornecedores.
   - **Todos**: Os termos de retención do fornecedor aplícanse a todos os fornecedores.
5. No campo **Fornecedor/grupo de fornecedores**, seleccione o fornecedor ou grupo de fornecedores ao que se aplican os termos de retención do fornecedor. Se seleccionou **Todos** no paso anterior, este campo non está dispoñible.
6. No campo **Condicións de retención do fornecedor**, seleccione o ID da regra para as condicións de retención que se aplicarán a este fornecedor.

