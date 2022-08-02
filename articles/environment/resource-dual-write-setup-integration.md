---
title: Integración de datos de instalación e configuración de Project Operations
description: Este artigo ofrece información sobre a configuración e configuración de mapas de dobre escritura de Project Operations.
author: sigitac
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d03393de893c39ceb53c06a3031395f765a26f55
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029150"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Integración de datos de instalación e configuración de Project Operations

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Este artigo ofrece información sobre a integración de dobre escritura de Project Operations para as entidades de configuración e instalación.

## <a name="project-contracts-contract-lines-and-projects"></a>Contratos do proxecto, liñas de contrato e proxectos

Os contratos de proxectos, liñas de contratos e proxectos créanse en Dataverse e sincronizado con aplicacións de finanzas e operacións para contabilidade adicional. Os rexistros nestas entidades só se poden crear e eliminar en Dataverse. Non obstante, a estes rexistros pódense engadir atributos contables como os valores predeterminados do grupo de impostos sobre vendas e as dimensións financeiras nas aplicacións de finanzas e operacións.

  ![Conceptos de integración de contrato de proxecto.](./media/1ProjectContract.jpg)

Realízanse un seguimento das oportunidades, oportunidades e presupostos da actividade de vendas Dataverse e non sincronices coas aplicacións de finanzas e operacións porque non hai ningunha contabilidade posterior asociada a esta actividade.

A funcionalidade do contrato do proxecto en Dataverse crea un rexistro de contrato de proxecto en aplicacións de finanzas e operacións usando o **Cabeceiras do contrato do proxecto (pedidos de venda)** mapa de mesa. Ao gardar un contrato de proxecto en Dataverse tamén comeza a creación dun rexistro da entidade cliente de contrato de proxecto. Este rexistro está sincronizado coas aplicacións de finanzas e operacións que utilizan o **Fonte de financiamento do proxecto (msdyn\_ regras de facturación dividida de contratos de proxectos)** mapa de mesa. Este mapa tamén sincroniza as adicións, actualizacións e eliminacións de clientes do contrato do proxecto. As porcentaxes de facturación divididas entre os clientes do contrato do proxecto só se dominan en Dataverse e non sincronizado coas aplicacións de finanzas e operacións.

Despois de crear un contrato de proxecto en Dataverse, o contador do proxecto pode actualizar os atributos contables deste contrato de proxecto nas aplicacións de finanzas e operacións.**Xestión de proxectos e contabilidade** > **Contratos de proxectos** > **Montar** > **Mostrar a contabilidade predeterminada**. O contable pode revisar os atributos do contrato do proxecto operativo, como a data de entrega solicitada e o importe do contrato, seleccionando o ID do contrato do proxecto nas aplicacións de finanzas e operacións que abre o rexistro do contrato do proxecto relacionado en Dataverse.

A entidade do proxecto está sincronizada coas aplicacións de financiamento e operacións mediante o **Proxectos V2 (msdyn\_ proxectos)** mapa de mesa. O contable do proxecto pode:

  - Revisa proxectos en aplicacións de finanzas e operacións accedendo a **Xestión de proxectos e contabilidade** > **Todos os proxectos**. 
  - Actualice os atributos de contabilidade para o proxecto nas aplicacións de finanzas e operacións accedendo a **Xestión de proxectos e contabilidade** > **Todos os proxectos** > **Montar** > **Mostrar a contabilidade predeterminada**.  
  - Revisa os atributos operativos do proxecto, como as datas estimadas de inicio e finalización, seleccionando o ID do proxecto nas aplicacións de finanzas e operacións que abre o rexistro do proxecto relacionado en Dataverse.

Un proxecto asóciase a un contrato de proxecto a través da entidade **Liña de contrato de proxecto**.

Liñas de contrato do proxecto en Dataverse crea unha regra de facturación do contrato do proxecto en aplicacións de finanzas e operacións usando o **Liñas de contrato do proxecto (detalles da orde de venda)** mapa de mesa. O método de facturación define o tipo de regra de facturación do contrato do proxecto nas aplicacións de finanzas e operacións:

  - As liñas de contrato do proxecto cun método de facturación de tempo e material crean unha regra de facturación de tempo e tipo de material.
  - As liñas de contrato do método de facturación de prezo fixo crean unha regra de facturación de fitos.

O contador do proxecto pode revisar as liñas de contrato do proxecto nas aplicacións de finanzas e operacións **Xestión de proxectos e contabilidade** > **Contratos de proxectos** > **Montar** > **Mostrar a contabilidade predeterminada**, e revisando os detalles sobre o **Liñas de contrato** ficha. O contable tamén pode establecer dimensións financeiras predeterminadas para as liñas de contrato do método de facturación de prezo fixo nesta pestana.

## <a name="billing-milestones"></a>Fitos de facturación

As liñas de contrato do proxecto que utilizan o método de facturación de prezo fixo factúranse mediante fitos de facturación. Os fitos de facturación sincronízanse para proxectar transaccións na conta nas aplicacións de finanzas e operacións mediante o **Fitos da liña de contrato de integración de operacións do proxecto (msdyn\_ Planificación de valores de liñas de contrato)** mapa de mesa.

  ![Integración de fitos de facturación.](./media/2Milestones.jpg)

O contable pode revisar as transaccións a conta e axustar os atributos contables desas transaccións dirixíndose a **Xestión e contabilidade de proxectos** > **Contratos de proxecto** > **Manter** > **Transaccións a conta** ou **Xestión de proxectos e contabilidade** > **Todos os proxectos** > **Manter** > **Transaccións a conta**.

Cando crea por primeira vez un fito de facturación para unha liña de contrato de proxecto determinada, o sistema crea automaticamente un proxecto de estimación de ingresos de prezo fixo para o proxecto asociado a esta liña de contrato. Os proxectos de estimación de ingresos a prezo fixo pódense revisar indo a **Xestión e contabilidade de proxectos** > **Proxectos de estimación de ingresos a prezo fixo**.

### <a name="project-tasks"></a>Tarefas do proxecto

As tarefas do proxecto sincronízanse coas aplicacións de financiamento e operacións a través de **Tarefas do proxecto (msdyn\_ tarefas do proxecto)** mapa de táboa só con fins de referencia. A creación, actualización e eliminación de operacións non son compatibles coas aplicacións financeiras e de operacións.

  ![Integración de tarefas de proxecto.](./media/3Tasks.jpg)

## <a name="project-resources"></a>Recursos de proxecto

O **Roles dos recursos do proxecto** a entidade está sincronizada coas aplicacións de financiamento e operacións mediante o **Roles de recursos do proxecto para todas as empresas (categorías de recursos reservables)** mapa de táboa só con fins de referencia. Porque os roles de recursos en Dataverse non son específicos da empresa, o sistema crea automaticamente os respectivos rexistros de roles de recursos específicos da empresa en aplicacións de finanzas e operacións automaticamente para todas as entidades xurídicas incluídas no ámbito de integración de dobre escritura.

![Integración de roles de recursos.](./media/5Resources.jpg)

Os recursos do proxecto en Operacións do proxecto mantéñense en Dataverse e non están sincronizados coas aplicacións financeiras e de operacións.

### <a name="transaction-categories"></a>Categorías de transaccións

As categorías de transaccións mantéñense en Dataverse e sincronizado coas aplicacións de finanzas e operacións mediante o **Categorías de transacción do proxecto (msdyn\_ categorías de transacción)** mapa de mesa. Despois de sincronizar o rexistro de categorías de transacción, o sistema crea automaticamente catro rexistros de categorías compartidas. Cada rexistro corresponde a un tipo de transacción nas aplicacións de finanzas e operacións e enlázaos co rexistro da categoría de transacción.

![integración de categorías de transacción.](./media/4TransactionCategories.jpg)

O uso de categorías de transaccións para estimacións e datos reais require que o contable do proxecto ou o administrador do sistema creen categorías de proxectos correspondentes en todas as entidades legais. Para obter máis información, consulte [Configurar categorías de proxecto](../project-accounting/configure-project-categories.md).
