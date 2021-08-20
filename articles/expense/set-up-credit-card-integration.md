---
title: Configurar a integración de tarxetas de crédito
description: Este tema explica como traballar con transaccións con tarxeta de crédito relacionadas cos gastos.
author: suvaidya
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 51c364dff41d856e493581e1b87fd29571f641c70e7233bdebb910efbc64b983
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996209"
---
# <a name="set-up-credit-card-integration"></a>Configurar a integración de tarxetas de crédito

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

As transaccións con tarxeta de crédito relacionadas cos gastos pódense configurar para que se importen automaticamente nunha programación periódica. Como alternativa, as transaccións pódense importar manualmente cando sexan necesarias. As transaccións con tarxeta de crédito impórtanse a través da entidade de datos de transaccións con tarxeta de crédito.

## <a name="import-credit-card-transactions"></a>Importar transaccións con tarxeta de crédito

Para importar transaccións con tarxeta de crédito, siga estes pasos:

1. Na páxina **Transaccións con tarxeta de crédito**, seleccione **Importar transaccións**. Se está a abrir a xestión de datos por primeira vez, o sistema debe actualizar a lista de entidades de datos antes de que poida continuar.
2. No campo **Nome**, introduza unha descrición única para o traballo de importación.
3. No campo **Formato de datos de orixe**, seleccione o formato do ficheiro que contén as transaccións con tarxeta de crédito para importar.
4. Seleccione **Cargar** e, a seguir, busque e seleccione o ficheiro para importar.
5. Despois de cargar o ficheiro, valide a asignación do ficheiro de transacción con tarxeta de crédito e as columnas da entidade de datos de transaccións con tarxeta de crédito seleccionando a ligazón **Ver mapa** no mosaico. Se hai erros de asignación ou se ten que cambiar a asignación, faga os cambios de asignación a partir de calquera separador de **Visualización de asignacións** ou o separador **Detalles de asignación**.
6. Para automatizar as transaccións con tarxeta de crédito, seleccione **Crear traballo de datos periódico**. A seguir, pode definir a periodicidade que define a frecuencia coa que se deben importar as transaccións con tarxeta de crédito. Ao concluír, seleccione **Aceptar**.
7. Para importar o ficheiro seleccionado agora, seleccione **Importar**.
8. Se se producen erros durante a importación, pode ver o rexistro de execución ou os datos intermedios para ver os erros que debe corrixir para garantir a importación.

> [!NOTE]
> Se precisa importar máis dun formato de ficheiro, debe crear traballos de importación separados para cada tipo de formato.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Atribuír de novo as transaccións con tarxeta de crédito para empregados cesados

Despois de concluír un rexistro de empregado, desactívase a conta de Active Directory Domain Services (AD DS) do empregado. Non obstante, pode haber transaccións con tarxeta de crédito activas que aínda se deben gastar e reembolsar. Na páxina **Transaccións con tarxeta de crédito**, pode atribuír de novo o empregado para calquera transacción con tarxeta de crédito na que o empregado asociado fose despedido.

Seleccione unha ou máis transaccións con tarxeta de crédito e logo seleccione **Reatribuír transaccións**. Despois pode seleccionar outro empregado ao que atribuír as transaccións con tarxeta de crédito. Despois de reatribuír as transaccións con tarxeta de crédito, pódense seleccionar para un informe de gastos e pagarse mediante o proceso habitual de reembolso do informe de gastos.

## <a name="delete-credit-card-transactions"></a>Eliminar transaccións con tarxeta de crédito 

Ás veces, despois de importar as transaccións con tarxeta de crédito, é posible que precise eliminar algunhas transaccións. Isto pode deberse a que as transaccións son duplicadas ou porque os datos poden non ser precisos. Os administradores poden usar a funcionalidade **"Eliminar transaccións con tarxeta de crédito"** para seleccionar e eliminar as transaccións con tarxeta de crédito que **non estean anexas** a un informe de gastos. 

1. Vaia a **Tarefas periódicas** > **Eliminar transaccións con tarxeta de crédito**.
2. Seleccione **Filtro** e proporcione información para identificar os rexistros a incluír.
3. Seleccione **Aceptar** para eliminar os rexistros. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
