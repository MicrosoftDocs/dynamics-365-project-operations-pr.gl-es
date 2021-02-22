---
title: Configurar a facturación entre empresas
description: Este tema ofrece información e exemplos sobre como configurar a facturación entre empresas para proxectos.
author: sigitac
manager: tfehr
ms.date: 11/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: bdb6122d8aba84d2b449f9f17a4093388b585614
ms.sourcegitcommit: addbe0647619413e85e7cde80f6a21db95ab623e
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 11/20/2020
ms.locfileid: "4595470"
---
# <a name="configure-intercompany-invoicing"></a>Configurar a facturación entre empresas

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Complete os seguintes pasos para configurar a facturación entre empresas para proxectos en Dynamics 365 Project Operations. As transaccións entre empresas son transaccións de tempo e gasto dun contrato de proxecto que pertencen a unha empresa ou unidade organizativa, mentres que os recursos do contrato de proxecto forman parte dunha empresa ou unidade organizativa diferente.

## <a name="example-configure-intercompany-invoicing"></a>Exemplo: Configurar facturación entre empresas

No seguinte exemplo, Contoso Robotics USA (USPM) é a entidade legal prestameira e Contoso Robotics UK (GBPM) é a entidade legal prestamista. 

1. **Configure a contabilidade entre empresas entre entidades legais**. Cada par de entidades legais prestameira e prestamista debe estar configurado na páxina [Contabilidade entre empresas](https://docs.microsoft.com/dynamics365/finance/general-ledger/intercompany-accounting-setup) do libro maior.
    
    1. En Dynamics 365 Finance, vaia a **Libro maior** > **Configuración da contabilización** > **Contabilidade entre empresas**. Cree un rexistro coa seguinte información:

        - **Empresa de orixe** = **GBPM**
        - **Empresa de destino** = **USPM**

2. **Configure a relación comercial entre as entidades legais**. O rexistro de cliente que representa á entidade legal prestameira debe crearse na entidade legal prestamista. O rexistro de fornecedor que representa á entidade legal prestamista debe crearse na entidade legal prestameira.

     1. En Finance, seleccione a entidade legal **GBPM**.
     2. Vaia a **Contas pendentes de cobro** > **Cliente** > **Todos os clientes**. Cree un novo rexistro para a entidade legal **USPM**.
     3. Expanda **Nome**, filtre os rexistros por **Tipo** e seleccione **Entidades legais**. 
     4. Busque e seleccione o rexistro do cliente para **Contoso Robotics USA (USPM)**.
     5. Seleccione **Usar coincidencia**. 
     6. Seleccione o grupo de clientes e logo garde o rexistro.
     7. Seleccione a entidade legal **USPM**.
     8. Vaia a **Contas pendentes de pago** > **Fornecedores** > **Todos os fornecedores**. Cree un novo rexistro para a entidade legal **GBPM**.
     9. Expanda **Nome**, filtre os rexistros por **Tipo** e seleccione **Entidades legais**. 
     10. Busque e seleccione o rexistro do cliente para **Contoso Robotics UK (GBPM)**.
     11. Seleccione **Usar coincidencia**, seleccione o grupo de fornecedores e logo garde o rexistro.
     12. No rexistro do fornecedor, seleccione **Xeral** > **Configurar** > **Entre empresas**.
     13. No separador **Relación comercial**, estableza **Activa** en **Si**.
     14. Seleccione a empresa do fornecedor **GBPM** e en **Rexistro da miña conta**, seleccione o rexistro de cliente que creou anteriormente no procedemento.

3. **Configure os axustes entre empresas nos parámetros de xestión de proxectos e contabilidade**. 

    1. Seleccione a entidade legal **USPM** e vaia a **Xestión e contabilidade de proxectos** > **Configuración** > **Parámetros de xestión de proxectos e contabilidade**.
    2. No separador **Entre empresas**, seleccione a categoría de adquisición para que coincida coas facturas do fornecedor que se xeran automaticamente.
    3. En **Categoría predefinida**, seleccione **Recursos entre empresas**.
    4. Seleccione a entidade legal **GBPM** e vaia a **Xestión e contabilidade de proxectos** > **Configuración** > **Parámetros de xestión de proxectos e contabilidade**.
    5. No separador **Entre empresas**, seleccione unha categoría de proxecto predefinida para cada tipo de transacción. As categorías de proxectos úsanse para a configuración de impostos cando a categoría facturada en transaccións entre empresas só existe na persoa xurídica prestameira. Pode optar por acumular ingresos por transaccións entre empresas. A acumulación ocorre cando as transaccións se contabilizan a través do diario de integración de Project Operations na entidade legal prestamista. O diario invértese cando se contabiliza a factura entre empresas.
    6. No grupo **Cando se prestan recursos**, seleccione **...** > **Novo**. 
    7. Na grade seleccione a seguinte información:

          - **Entidade legal prestameira** = **GBPM**
          - **Acumular ingresos** = **Si**
          - **Categoría de folla de control horario predefinida** = **Predefinida - Hora**
          - **Categoría de gasto predefinida** = **Predefinida - gasto**

4. **Estableza contas de custos e ingresos entre empresas na configuración de contabilización do libro maior**. A conta de ingresos entre empresas cobra cando a factura de cliente entre empresas se contabiliza na entidade legal prestamista. A conta de custos entre empresas cárgase cando a factura do fornecedor pendente coincidente se contabiliza na entidade legal prestameira. Estas contas configúranse nas entidades legais correspondentes. 
      
     1. En Finance, seleccione a entidade legal prestameira **USPM**. 
     2. Vaia a **Xestión e contabilidade de proxectos** > **Configurar** > **Contabilización** > **Configuración de contabilización de libro maior**. 
     3. No separador **Contas de custos**, en **Tipo de conta de libro maior**, seleccione **Custo entre empresas**. Cree un novo rexistro coa seguinte información:
      
        - **Entidade legal prestamista** = **GBPM**
        - **Conta principal** = Seleccione a conta principal para o custo entre empresas
        
     4. Seleccione a entidade legal prestamista, **GBPM**. 
     5. Vaia a **Xestión e contabilidade de proxectos** > **Configurar** > **Contabilización** > **Configuración de contabilización de libro maior**. 
     6. No separador **Contas de ingresos**, en **Tipo de conta de libro maior**, seleccione **Ingresos entre empresas**. Cree un novo rexistro coa seguinte información:

        - **Entidade legal prestameira** = **USPM**
        - **Conta principal** = Seleccione a conta principal para os ingresos entre empresas 

5. **Configure os prezos de transferencia da man de obra**. O prezo de transferencia entre empresas configúrase en Project Operations en Dataverse. Configure [taxas de custo laboral](../pricing-costing/set-up-labor-cost-rate.md#transfer-pricing-and-costs-for-resources-outside-of-your-division-or-legal-entity) e [taxas de factura laboral](../pricing-costing/set-up-labor-bill-rate.md#transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions) para a facturación entre empresas. Non se admiten prezos de transferencia para transaccións de gastos entre empresas. O prezo de venda unitario entre organizacións establecerase sempre no mesmo valor que o prezo de custo unitario do recurso.

      O custo do recurso para programadores en Contoso Robotics UK é de 88 GBP por hora. Contoso Robotics UK facturará a Contoso Robotics USA 120 USD por cada hora que este recurso traballou en proxectos estadounidenses. Contoso Robotics USA facturará ao cliente Adventure Works 200 USD polo traballo realizado polo recurso de programador de Contoso Robotics UK.

      1. En Project Operations en Dataverse, vaia a **Venda** > **Listas de prezos**. Cree unha nova lista de prezos de custo chamada **Taxas de custo de Contoso Robotics UK.** 
      2. Na lista de prezos de custo, cree un rexistro coa seguinte información:
         - **Rol** = **Programador**
         - **Custo** = **88 GBP**
      3. Vaia a **Configuración** > **Unidades organizativas** e achegue esta lista de prezos de custo á unidade organizativa **Contoso Robotics UK**.
      4. Vaia a **Vendas** > **Listas de prezos**. Cree unha lista de prezos de custo chamada **Taxas de custo de Contoso Robotics USA**. 
      5. Na lista de prezos de custo, cree un rexistro coa seguinte información:
          - **Rol** = **Programador**
          - **Empresa de recursos** = **Contoso Robotics UK**
          - **Custo** = **120 USD**
      6. Vaia a **Configuración** > **Unidades organizativas** e achegue a lista de prezos de custo **taxas de custo de Contoso Robotics USA** á unidade organizativa **Contoso Robotics USA**.
      7. Vaia a **Vendas** > **Listas de prezos**. Cree unha lista de prezos de venda chamada **Taxas de factura de Adventure Works**. 
      8. Na lista de prezos de vendas, cree un rexistro coa seguinte información:
          - **Rol** = **Programador**
          - **Empresa de recursos** = **Contoso Robotics UK**
          - **Taxa de facturación** = **200 USD**
      9. Vaia a **Vendas** > **Contratos de proxecto** e achega a lista de prezos **Taxas de factura de Adventure Works** á lista de prezos do proxecto Adventure Works do contrato do proxecto.