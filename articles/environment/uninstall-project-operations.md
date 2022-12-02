---
title: Desinstalar Dynamics 365 Project Operations
description: Este artigo fornece información sobre como desinstalar Dynamics 365 Project Operations.
author: stsporen
ms.date: 11/09/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 33a505594d6db47b4f8a0c8a630a0836f424e7d5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911962"
---
# <a name="uninstall-dynamics-365-project-operations"></a>Desinstalar Dynamics 365 Project Operations 

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Para desinstalar Dynamics 365 Project Operations, debe ter atribuído o rol de Administrador.

1. Vaia a **Configuración** > **Solucións**.

    ![Páxina de configuración.](./media/uninstall-proj-ops-solutions.png)
  
2. Elimine as solucións na orde exacta en que se indican na seguinte táboa. 

    | Paso | Nome da solución                                    | Nota                                                                                         |
    |------|----------------------------------------------------|----------------------------------------------------------------------------------------------|
    | 1 | msdyn_ProjectServiceUpgrade_managed.cab            | Se non se atopa, omita esta solución.                                                            |
    | 2 | ProjectOperations_Anchor                           | Se non se atopa, omita esta solución.                                                            |
    | 3 | Dynamics365ProjectOperationsDualWriteEntityMaps    | Se non se atopa, omita esta solución.                                                            |
    | 4 | Dynamics365ProjectOperationsDualWrite              | Se non se atopa, omita esta solución.                                                            |
    | 5 | ProjectService                                     | Non hai notas adicionais.                                                                         |
    | 6 | ProjectServiceCore_Patch                           | Non hai notas adicionais.                                                                         |
    | 7 | ProjectServiceCore                                 | Non hai notas adicionais.                                                                         |
    | 8 | ProjectServiceDeprecatedComponents                 | Se non se atopa, omita esta solución.                                                            |
    | 9 | FieldServiceCommon                                 | Necesario para a escrita dual con Dynamics 365 Finance ou Dynamics 365 Supply Chain Management.   |
    | 1,0 | msdyn_AssetCommon                                  | Necesario para a escrita dual con Dynamics 365 Finance ou Dynamics 365 Supply Chain Management.   |
    | 11 | msdyn_TESA_Anchor                                  | Necesario para Dynamics 365 Field Service.                                                     |
    | 12 | msdyn_TESA_Patch                                   | Necesario para Dynamics 365 Field Service.                                                     |
    | 13 | msdyn_TESA                                         | Necesario para Dynamics 365 Field Service.                                                     |
    | 14 | ResourceSchedulingControls                         | Necesario para Dynamics 365 Field Service.                                                     |
    | 15 | MicrosoftDynamicsScheduling3_CumulativePatch       | Necesario para Dynamics 365 Field Service.                                                     |
    | 16 | MicrosoftDynamicsScheduling_Patch_xx               | Necesario para Dynamics 365 Field Service.                                                     |
    | 17 | MicrosoftDynamicsScheduling                        | Necesario para Dynamics 365 Field Service.                                                     |
    | 18 | Dynamics365FinanceAndOperationsAnchor              | Se non se atopa, omita esta solución.                                                            |
    | 19 | Dynamics365Notas                                   | Se non se atopa, omita esta solución.                                                            |
    | 20 | Dynamics365FinanceAndOperationsDualWriteEntityMaps | Se non se atopa, omita esta solución.                                                            |
    | 21 | DualWriteCore                                      | Se non se atopa, omita esta solución.                                                            |
    | 22 | Dynamics365AssetManagementApp                      | Se non se atopa, omita esta solución.                                                            |
    | 23 | Dynamics365AssetManagement                         | Se non se atopa, omita esta solución.                                                            |
    | 24 | Dynamics365SupplyChainExtended                     | Se non se atopa, omita esta solución.                                                            |
    | 25 | Dynamics365FinanceExtended                         | Se non se atopa, omita esta solución.                                                            |
    | 26 | HCMCommon                                          | Se non se atopa, omita esta solución.                                                            |
    | 27 | Dynamics365FinanceAndOperationsCommon              | Se non se atopa, omita esta solución.                                                            |
    | 28 | Participante                                              | Se non se atopa, omita esta solución.                                                            |
    | 29 | Dynamics365Company                                 | Se non se atopa, omita esta solución.                                                            |
    | 30 | CurrencyExchangeRates                              | Se non se atopa, omita esta solución.                                                            |
    | 31 | AssetCommon                                        | Se non se atopa, omita esta solución.                                                            |
