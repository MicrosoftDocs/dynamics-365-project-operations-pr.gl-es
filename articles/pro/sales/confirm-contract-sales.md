---
title: Confirmar un contrato de proxecto
description: Este artigo ofrece información sobre como confirmar un contrato en Project Operations.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0e92dc42c4ff6bdc40c479511c80d3e500df781a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929994"
---
# <a name="confirm-a-project-contract"></a>Confirmar un contrato de proxecto

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Un contrato de proxecto en Dynamics 365 Project Operations pode estar activo cun motivo de **Confirmado** ou pechado cun motivo de **Perdido**. Cando confirme un contrato de proxecto, o estado actualízase de **Borrador** a **Activo** e o motivo para o estado é **Confirmado**. Non se pode editar nin reabrir un contrato activo ou pechado. 

### <a name="financial-impact-of-confirming-a-project-contract"></a>Impacto financeiro da confirmación dun contrato de proxecto

Despois de confirmar un contrato de proxecto, a aplicación calculará de novo os custos revertendo os datos reais de custos máis antigos e creando novos datos reais de custos. Despois os novos datos reais de custos se procesan en función do método de facturación da liña de contrato do proxecto asociado. Se os datos reais de custos fan referencia a unha liña de contrato de tempo e material, a aplicación recrea automaticamente os datos reais de vendas non facturados correspondentes. Se os datos reais de custos fan referencia a unha liña de contrato de prezo fixo, a aplicación deixa de reprocesar os datos reais de custos.

Os límites non superables, a configuración de imputabilidade e os prezos e custos dos datos reais avalíanse e actualízanse como parte do proceso de confirmación.

## <a name="close-a-project-contract-as-lost"></a>Pechar un contrato de proxecto como perdido

Cando pecha un contrato de proxecto como perdido, o estado do contrato actualízase a **Pechado** e o motivo para o estado é **Perdido**. O contrato de proxecto pasa a ser de só lectura. Ofrécese un diálogo de confirmación antes de completar os cambios porque non pode volver abrir un contrato de proxecto pechado.

Se o contrato de proxecto pechado como perdido fai referencia a un proxecto nas súas liñas, ese proxecto tamén se marcará como pechado. Cancélanse as reservas de recursos a partir dese día. Os datos reais de vendas non facturadas do contrato de proxecto que aínda non figuren nunha factura reverteranse.

> [!NOTE]
> En Dynamics 365 Project Operations, pechar un contrato de proxecto como perdido non repercutirá nese estado da oportunidade asociada. A oportunidade permanecerá aberta e debe pecharse manualmente.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]