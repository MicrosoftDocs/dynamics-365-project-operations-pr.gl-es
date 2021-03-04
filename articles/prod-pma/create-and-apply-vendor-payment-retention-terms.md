---
title: Crear e aplicar os termos de retención do pagamento do fornecedor
description: Este tema ofrece información sobre como configurar e manter os termos de retención para os pagamentos do fornecedor.
author: Yowelle
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 1970a24a5073de6af43db1f1c068332c9ba9c8fe
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076269"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a>Crear e aplicar os termos de retención do pagamento do fornecedor

[!include [banner](../includes/banner.md)] 

Configurar as condicións de retención de pagamentos do fornecedor para un proxecto é útil cando a súa organización quere reter parte dos pagamentos realizados a un fornecedor. Por exemplo, cando quere reter o pagamento a un fornecedor ata que os produtos entregados cumpran as súas expectativas. Pódense especificar as condicións de retención do pagamento do fornecedor cando negocie un contrato de fornecedor.

## <a name="create-vendor-payment-retention-terms"></a>Crear os termos de retención do pagamento do fornecedor

Pode introducir a porcentaxe de pagamento do fornecedor para a retención e a porcentaxe das cantidades retidas anteriormente que se liberarán. As cantidades retéñense automaticamente nas facturas do fornecedor ata que o contrato alcanza o estado especificado de finalización. Despois de configurar os termos de retención, pode aplicalos a calquera proxecto dese fornecedor.

Utilice os seguintes pasos para configurar e manter os termos de retención dos pagamentos do fornecedor. 

1. Vaia a **Xestión e contabilidade de proxectos** > **Retención** > **Condicións de retención do pagamento do fornecedor**.
2. Seleccione **Novo** para engadir un novo termo de retención do fornecedor. O valor de **ID da regra** introdúcese automaticamente para o novo termo. 
3. Introduza unha breve descrición no campo **Descrición** e no separador rápido **Termos** , seleccione **Engadir liña** para introducir valores de termo para o seguinte:

   - **Porcentaxe de unidades entregadas** : Introduza unha porcentaxe de finalización para o termo. As cantidades retéñense automaticamente nas facturas do fornecedor ata que a fase de finalización do proxecto sexa igual á porcentaxe especificada. Por exemplo, se introduce 50,00, as cantidades retéñense ata que o proxecto se complete nun 50 por cento.
   - **Porcentaxe para reter** : Insira unha porcentaxe do importe da factura do fornecedor que se reterá. Por exemplo, se introduce 10,00, reterase o 10 por cento do importe da factura dun fornecedor ata que o proxecto alcance a porcentaxe de finalización establecida no campo **Porcentaxe de unidades entregadas**.
   - **Porcentaxe para liberar** : Seleccione **Engadir liña** para introducir unha porcentaxe de cantidades retidas anteriormente que se liberarán para o nivel seleccionado de finalización do proxecto.

> [!NOTE]
> Se ten máis dun fito para os diferentes niveis de finalización do proxecto, escriba unha liña de termo de retención do fornecedor separada para cada regra de retención. Cada liña pode especificar unha porcentaxe de retención diferente e unha porcentaxe de liberación diferente para cada nivel designado de finalización do proxecto.

Despois de crear os termos de retención para un fornecedor, pode aplicar os termos a un proxecto.

## <a name="apply-vendor-retention-terms-to-a-project"></a>Aplicar os termos de retención do fornecedor a un proxecto

1. Vaia a **Xestión e contabilidade de proxectos** > **Proxectos** > **Todos os proxectos** e abra un proxecto desde a páxina da lista de proxectos.
2. No separador rápido **Acordos de fornecedores** , seleccione **Engadir liña**.
3. No campo **Código de conta** , seleccione unha das seguintes opcións: 

   - **Táboa** : Os termos de retención do fornecedor aplícanse a un único fornecedor.
   - **Grupo** : Os termos de retención do fornecedor aplícanse a todos os fornecedores dun grupo de fornecedores.
   - **Todos** : Os termos de retención do fornecedor aplícanse a todos os fornecedores.

4. No campo **Fornecedor/grupo de fornecedores** , seleccione o fornecedor ou grupo de fornecedores ao que se aplican os termos de retención do fornecedor. Se seleccionou **Todos** no paso anterior, este campo non está dispoñible.
5. No campo **Termos de retención do fornecedor** , seleccione os termos de retención que creou no procedemento anterior.
6. Se o proxecto tamén ten configurados os termos de pagar ao recibir o pagamento (PWP) para o fornecedor, escriba a porcentaxe limiar para o proxecto no campo **Porcentaxe de limiar de PWP**.

Os termos de retención do fornecedor tamén se mostran nos pedidos de compra que cree para o fornecedor.


[!INCLUDE[footer-include](../includes/footer-banner.md)]