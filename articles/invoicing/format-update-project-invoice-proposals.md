---
title: Xestionar propostas de facturas de proxecto
description: Este artigo ofrece detalles sobre o procesamento de facturas dirixidas ao cliente con Project Operations para escenarios baseados en recursos ou non almacenados.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: ef6003499f1372a51d7d1606db6f5bf9722a369d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927832"
---
# <a name="manage-project-invoice-proposals"></a>Xestionar propostas de facturas de proxecto

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

O seu departamento de facturación pode procesar as propostas de factura do proxecto cando se cumpran as dúas condicións seguintes:

  - O xestor de proxectos confirma a factura proforma en Microsoft Dataverse.
  - Todas as transaccións de vendas sen facturar de tempo e material incluídas na factura proforma contabilízanse mediante o diario de Dynamics 365 **Project Operations Integration**.

Use os seguintes pasos para completar unha proposta de factura de proxecto en Dynamics 365 Finance.

1. Revise a información de facturación por transaccións de tempo e material e publique o diario de **Project Operations Integration**.
2. Revise a información de facturación dos fitos de facturación a prezo fixo.
3. Revise e dea formato a unha proposta de factura de proxecto.
4. Publicar e imprimir facturas de proxecto.

## <a name="manage-billing-information-in-the-project-operations-integration-journal"></a>Xestionar información de facturación no diario de Project Operations Integration

Os datos reais do proxecto creados en Dataverse son revisados e publicados en Finance polo contable do proxecto. Para obter máis información sobre como traballar co diario de Integration, consulte [Disrio de Integration en Project Operations](../project-accounting/project-operations-integration-journal.md).

Os datos reais de custos e as vendas sen facturar engádense ao diario de Integration como liñas separadas:

  - O prezo de custo unitario e o importe do custo no dato real de custo establécense por defecto a partir do transacción de custo real do proxecto en Dataverse.
  - O prezo unitario de venda e o importe das vendas da transacción de vendas sen facturar establécense por defecto a partir da transacción de vendas sen facturar reais do proxecto en Dataverse.

### <a name="billing-sales-tax"></a>Imposto sobre as vendas de facturación

O cálculo do imposto sobre as vendas para a facturación está determinado pola combinación dos campos **Grupo de impostos sobre vendas de facturación** e **Grupo de impostos sobre vendas individuais de facturación** nun rexistro de vendas sen facturar na liña de diario de **Project Operations Integration**. O sistema predeterminará estes valores de campo en función da configuración do separador **Financials** na páxina **Parámetros de xestión e contabilidade de proxectos**.

- **Método do grupo de impostos sobre as vendas** determina a lóxica predefinida do grupo de impostos sobre as vendas:
  
  - **Proxecto**: Sempre predefinirá o grupo de impostos sobre as vendas de facturación a partir do proxecto. Pode revisar ou cambiar o grupo de impostos sobre as vendas por defecto nun proxecto seleccionando **Mostrar contabilidade predefinida** na páxina **Todos os proxectos**.
  - **Contrato de proxecto**: Sempre predefinirá o grupo de impostos sobre as vendas de facturación de facturación a partir do contrato do proxecto. Pode revisar ou cambiar o grupo de impostos sobre as vendas por defecto nun contrato de proxecto seleccionando **Mostrar contabilidade predefinida** na páxina **Contratos de proxecto**.
  - **Cliente**: Sempre predefinirá o grupo de impostos sobre as vendas de facturación a partir do cliente.
  - **Buscar**: Buscará en todas as entidades anteriores e seleccionará o primeiro valor dispoñible. A busca comeza coa entidade **Proxecto**, logo a entidade **Contrato do proxecto** e, finalmente, a entidade **Cliente**.

- **Método do grupo de impostos sobre as vendas individuais** determina a lóxica predefinida do grupo de impostos sobre as vendas individuais:
  
  - Para os tipos de transacción de tempo, gasto e tarifa, o grupo de impostos sobre as vendas individuais de facturación sempre se predefinirá a partir da entidade **Categoría do proxecto**.
  - Para os tipos de transaccións materiais, o grupo de impostos sobre as vendas individuais de facturación baséase na configuración do **Método do grupo do imposto sobre as vendas individuais** en **Parámetros de xestión de proxectos e contabilidade**. O número de artigo predefine o grupo de impostos sobre as vendas individuais a partir da entidade **Produto lanzado**. A categoría predefine o grupo de impostos sobre as vendas individuais a partir da entidade **Categoría de proxecto**.

### <a name="financial-dimensions"></a>Dimensións financeiras

As dimensións financeiras dos rexistros de vendas sen facturar no diario de **Project Operations Integration** predefínense a partir da entidade **Proxecto**. As dimensións financeiras pódense revisar e axustar seleccionando **Distribuír importes**. Se precisa cambiar as dimensións financeiras do rexistro de vendas sen facturar despois de publicar o diario de Integration pero antes de confirmar a factura proforma, vaia a **Todos os proxectos** > **Xestionar** > **Transaccións publicadas**, seleccione a transacción e, a seguir, seleccione **Procesar** > **Axustar contabilidade**.

### <a name="exchange-rates"></a>Taxas de cambio

A divisa das transaccións sen facturar en Dataverse úsase como moeda das transaccións en Finance e convértese en divisa de contabilidade da empresa empregando as taxas de cambio definidas en Finance.


## <a name="manage-the-financial-attributes-of-billing-milestones"></a>Xestionar os atributos financeiros dos fitos de facturación 

As liñas de contrato do proxecto que utilizan o método de facturación a prezo fixo factúranse a través dos [Fitos de prezo fixo](../sales/invoice-schedules-contract-line.md#create-a-fixed-price-invoice-schedule-for-a-contract-line). O contable do proxecto pode revisar os fitos da facturación en Finance indo a **Xestión e contabilidade de proxectos** > **Todos os proxectos** > **Xestionar** > **Transaccións a conta**.

### <a name="billing-sales-tax"></a>Imposto sobre as vendas de facturación

Os valores do **Grupo do imposto sobre as vendas** e o **Grupo do imposto sobre as vendas individuais** predefínense a partir da configuración cando se crea un novo fito de facturación en Dataverse. O sistema predefine os valores destes campos en función da configuración do separador **Financial** na páxina **Parámetros de xestión de proxectos e contabilidade**.

- **Método do grupo de impostos sobre as vendas** determina a lóxica para predefinir do **Grupo do imposto sobre as vendas de facturación**:

    - **Proxecto** sempre predefinirá o grupo de impostos sobre as vendas a partir do proxecto. Pode revisar ou cambiar o grupo de impostos sobre as vendas por defecto nun proxecto seleccionando **Mostrar contabilidade predefinida** na páxina **Todos os proxectos**.
    - **Contrato de proxecto** sempre predefinirá o grupo de impostos sobre as vendas de facturación a partir do contrato do proxecto. Pode revisar ou cambiar o grupo de impostos sobre as vendas por defecto nun contrato de proxecto seleccionando **Mostrar contabilidade predefinida** na páxina **Contratos de proxecto**.
    - **Cliente** sempre predefinirá o grupo de impostos sobre as vendas de facturación a partir do cliente.
    - **Buscar** buscará en todas as entidades desta lista e seleccionará o primeiro valor dispoñible. A busca comeza coa entidade **Proxecto**, logo a entidade **Contrato do proxecto** e despois a entidade **Cliente**.

- **Grupo de impostos sobre as vendas do elemento fito de prezo fixo** úsase como valor predefinido no campo **Grupo de impostos sobre as vendas de elementos** para o fito de facturación. O contable pode revisar e modificar este valor na páxina **Transaccións a conta**. O sistema utiliza o valor da transacción a conta ao crear unha liña de proposta de factura do proxecto.
 

### <a name="financial-dimensions"></a>Dimensións financeiras

As dimensións financeiras predefinidas para o fito de facturación a prezo fixo establécense nas liñas de contrato do proxecto. Vaia a **Contratos de proxecto** > **Mostrar contabilidade predefinida** e no separador **Liñas de contrato**, seleccione **liña de contrato de prezo**, logo configure os valores das dimensións financeiras que desexe usar como predefinidas.

O contable do proxecto pode editar a información sobre o imposto sobre as vendas e as dimensións financeiras dos fitos da factura ata que se cree a proposta de factura do proxecto.


## <a name="create-project-invoice-proposals"></a>Crear propostas de facturas de proxecto

As propostas de facturas do proxecto pódense revisar no módulo **Xestión e contabilidade de proxectos** indo a **Facturas do proxecto** > **Propostas de factura do proxecto**.

A cabeceira da proposta de factura do proxecto créase en Finance cando se confirma a factura proforma en Dataverse. Para facilitar a conciliación, o sistema establece o número de proposta de factura do proxecto en Finance no mesmo número que o ID da factura proforma en Dataverse. Debido a que as facturas proforma non se confirman necesariamente na mesma orde na que se crearon, a secuencia de números da proposta de factura do proxecto en Finance debe permitir cambios a números máis baixos e máis altos. Configure secuencias numéricas cos seguintes pasos:

1. En Finance, vaia a **Administración da organización** > **Secuencias numéricas** > **Secuencias numéricas**.
2. No filtro **Área**, seleccione **Proxectos**.
3. No filtro **Referencia**, seleccione **Proposta de factura**.
4. Use o campo **Empresa** campo para filtrar cada entidade legal coa integración de Project Operations Dataverse activada.
5. Abra **Detalles da secuencia numérica** e no separador **Xeral** estableza:

    - **Permitir cambios de usuario: A un número inferior** = **Si**
    - **Permitir cambios de usuario: A un número superior** = **Si**

O sistema engade as liñas de proposta de factura do proxecto mediante o proceso periódico **Importar da táboa de transición** (**Xestión de proxectos e contabilidade** > **Periódico** > **Integración de Project Operations** > **Importar da táboa de transición**). Este proceso pode executarse manualmente ou mediante unha programación periódica. O sistema non engadirá liñas ao documento de proposta de factura ata que todas as liñas estean listas para ser facturadas. As transaccións de tempo e material están listas para facturarse só cando se contabilizan mediante o diario de **Project Operations Integration**.

## <a name="format-and-print-invoice-proposals"></a>Dar formato e imprimir as propostas de factura

O contable do proxecto pode personalizar a impresión da factura do proxecto empregando a páxina **Dar formato a proposta de factura** e as capacidades de xestión impresión.

### <a name="format-invoice-proposals"></a>Dar formato ás propostas de factura

A páxina **Dar formato ás propostas de factura** permite que as transaccións de agrupación personalizadas se mostren na factura do proxecto do cliente.

1. Na páxina **Proposta de factura do proxecto**, seleccione **Imprimir** > **Dar formato á proposta de factura**.
2. Seleccione **Nova** para crear unha nova agrupación para a impresión da factura do proxecto.
3. No campo **Detalle/Resumo**, seleccione opcións para esta agrupación:

    - Seleccione **Detalle** para imprimir os detalles da transacción da factura do cliente.
    - Seleccione **Resumo** para imprimir o resumo da transacción da factura do cliente.

> [!NOTE]
> A selección no campo **Detalle/Resumo** na páxina **Ar formato a proposta de factura** anula a opción seleccionada no campo **Formato de factura** na páxina **Propostas de factura** para imprimir unha factura detallada ou unha factura resumida.

- Seleccione as liñas de transacción para incluír nesta sección no separador **Transaccións dispoñibles** e seleccione **Incluír transaccións** para movelas ao separador **Transaccións seleccionadas**.
- Seleccione **Mover cara arriba** e **Mover cara abaixo** para cambiar a orde das seccións.
- Seleccione **Previsualización de impresión** para previsualizar a factura con formato.

### <a name="print-management"></a>Xestión de impresión

A xestión de impresión utiliza diferentes ficheiros de informe para imprimir, especificar destinos e personalizar o texto do pé de páxina para a factura. A xestión da impresión pódese configurar a nivel de módulo, pero estas opcións pódense anular para un cliente, contrato ou proposta de factura específicos. Para acceder a esta función na páxina **Proposta de factura do proxecto**, seleccione **Imprimir** > **Xestión da impresión**.

A configuración de xestión de impresión móstrase como unha vista de árbore, onde cada nivel de nó mostra os documentos dispoñibles para axustalos. Pode atribuír impresións personalizadas a nivel de módulo, cliente, contrato ou documento de proposta de factura. Para modificar a impresión do documento orixinal, expanda o nó desexado e seleccione **Elemento orixinal**. No campo **Formato do informe**, seleccione o formato do informe que se usará para imprimir. Pode usar formatos de informe personalizados usando [Marco de xestión de documentos empresariais](/dynamics365/fin-ops-core/dev-itpro/analytics/er-business-document-management).

## <a name="post-invoice-proposals"></a>Publicar as propostas de factura

Despois de revisar e editar a factura e cando as liñas de proposta de factura son satisfactorias, comprobe os totais da factura e o imposto sobre as vendas. No grupo **Detalles**, seleccione **Totais** e logo seleccione **Publicar** para publicar a factura.

Para ver a factura antes de publicar, borre a caixa de verificación **Publicación**. **Pro forma** imprimirase na factura para indicar que é un exemplo de factura. Para imprimir a factura, seleccione a caixa de verificación **Imprimir factura**.

Ademais da páxina **Proposta de factura**, as propostas de factura tamén se poden publicar executando a tarefa periódica **Publicar propostas de factura**. Para atopar esta tarefa, vaia a **Xestión e contabilidade de proxectos** > **Periódico** > **Facturas do proxecto** > **Publicar propostas de factura**.

Esta páxina mostra todas as propostas de factura que están listas para publicar. Pode programar a publicación de propostas de factura seleccionando **Lote**. Configure o **Parámetro de procesamento por lotes** a **Si** e configure a repetición do procesamento por lotes seleccionando **Periodicidade**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
