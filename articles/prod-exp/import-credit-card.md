---
title: Importar e manter transaccións con tarxeta de crédito
description: Neste tema explícase como importar e manter transaccións con tarxeta de crédito relacionadas cos gastos. Estas transaccións pódense configurar para que se importen automaticamente nunha programación recorrente ou se poidan importar manualmente segundo sexan necesarias.
author: KimANelson
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: bd7ca997e18bf3c11fa188b603c899cc470df035
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/04/2022
ms.locfileid: "8683766"
---
# <a name="import-and-maintain-credit-card-transactions"></a>Importar e manter transaccións con tarxeta de crédito

As transaccións con tarxeta de crédito relacionadas cos gastos pódense configurar para que se importen automaticamente nunha programación periódica. Como alternativa, as transaccións pódense importar manualmente cando sexan necesarias. As transaccións con tarxeta de crédito importanse a través da entidade de datos de transaccións con tarxeta de crédito.

Para obter máis información sobre entidades de datos, consulte [Entidades de datos](/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).

## <a name="import-credit-card-transactions"></a>Importar transaccións con tarxeta de crédito

1. Na páxina **Transaccións con tarxeta de crédito**, seleccione **Importar transaccións**. Se está a abrir a xestión de datos por primeira vez, o sistema debe actualizar a lista de entidades de datos antes de que poida continuar.
2. No campo **Nome**, introduza unha descrición única do traballo de importación.
3. No campo **Formato de datos de orixe**, seleccione o formato do ficheiro que contén as transaccións con tarxeta de crédito para importar.
4. Seleccione **Cargar** e, a seguir, busque e seleccione o ficheiro para importar.
5. Despois de cargar o ficheiro, valide a asignación do ficheiro de transacción con tarxeta de crédito e as columnas da entidade de datos de transaccións con tarxeta de crédito seleccionando a ligazón **Ver mapa** no mosaico. Se hai erros de asignación ou se ten que cambiar a asignación, faga os cambios de asignación a partir de calquera separador de **Visualización de asignacións** ou o separador **Detalles de asignación**.
6. Para automatizar as transaccións con tarxeta de crédito, seleccione **Crear traballo de datos periódico**. A seguir, pode definir a periodicidade que define a frecuencia coa que se deben importar as transaccións con tarxeta de crédito. Ao concluír, seleccione **Aceptar**.
7. Para importar o ficheiro seleccionado agora, seleccione **Importar**.
8. Se se producen erros durante a importación, pode ver o rexistro de execución ou os datos intermedios para ver os erros que debe corrixir para axudar a garantir a importación.

> [!NOTE]
> Se debe importar máis dun formato de ficheiro, debe crear traballos de importación separados para cada tipo de formato.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Atribuír de novo as transaccións con tarxeta de crédito para empregados cesados

Despois de concluír un rexistro de empregado, desactívase a conta de Active Directory Domain Services (AD DS) do empregado. Non obstante, pode haber transaccións con tarxeta de crédito activas que aínda se deben gastar e reembolsar. Desde a páxina **Transaccións con tarxeta de crédito**, pode reatribuír ao empregado para calquera transacción con tarxeta de crédito na que o empregado asociado fose cesado.

Seleccione unha ou máis transaccións con tarxeta de crédito e logo seleccione **Reatribuír transaccións**. Despois pode seleccionar outro empregado ao que atribuír as transaccións con tarxeta de crédito. Despois de reatribuír as transaccións con tarxeta de crédito, pódense seleccionar para un informe de gastos e pagarse mediante o proceso habitual de reembolso do informe de gastos.


[!INCLUDE[footer-include](../includes/footer-banner.md)]