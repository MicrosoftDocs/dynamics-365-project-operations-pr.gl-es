---
title: Copiar contratos baseados en proxecto
description: Este artigo fornece información sobre a copia de contratos de proxecto en Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 21994ef6d8f6e6cdf321599d107cc80368c96ecc
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410364"
---
# <a name="copy-project-based-contracts"></a>Copiar contratos baseados en proxecto

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Pode crear facilmente novos contratos de proxecto copiando contratos existentes de dous xeitos:

- Na páxina de lista **Contratos de proxecto**, seleccione un contrato de proxecto e, a seguir, seleccione **Copiar**.
- Na páxina de detalles **Contrato de proxecto**, seleccione **Copiar**.

En ambos casos, aparece unha caixa de diálogo, onde pode establecer os parámetros do contrato copiado. A caixa de diálogo inclúe os campos seguintes. Dependendo dos valores que seleccione, o proceso de copia podería cambiar.

| Campo | Descripción | Impacto descendente |
| --- | --- | --- |
| Tema | Introduza o tema do contrato de destino. Cando se abra a caixa de diálogo, o sistema establece o campo co nome do contrato de orixe, pero a palabra "copia" está anexa a el. | Non hai ningún impacto descendente para este campo. |
| cliente/a | A referencia á empresa ou ao rexistro da conta do cliente. Cando se abra a caixa de diálogo, o sistema establece o campo na conta do contrato de orixe. | Este campo é o cliente principal no contrato. |
| Empresa propietaria | A empresa que se encarga da entrega dos proxectos que están asociados a esta oferta. Cando se abra a caixa de diálogo, o sistema establece o campo na conta do contrato de orixe. | A empresa propietaria é a entidade legal que executará o proxecto despois de pechar o acordo. A moeda da empresa propietaria debe coincidir coa moeda da unidade contratante do proxecto. |
| Unidade de contratación | A unidade de organización que se encarga da entrega dos proxectos que están asociados a esta oferta. Cando se abra a caixa de diálogo, o sistema establece o campo na unidade de contratación do contrato de orixe. | A unidade de contratación é a división da empresa que executará os proxectos despois de pechar o acordo. Cada unidade de contratación ten unha moeda. Esta moeda úsase para informar dos custos estimados e reais que se incorren durante o proxecto. |
| Moeda | A moeda na que se realizan as transaccións da oferta. Cando se abra a caixa de diálogo, o sistema establece o campo na moeda do contrato de orixe. Non se pode modificar a moeda. Se é así, o campo **Copiar prezos** sempre está configurado en **Non**, porque as listas de prezos do contrato de orixe xa non son relevantes. | Esta moeda úsase para predefinir listas de prezos, para xerar estimacións financeiras no contrato e para facturar ao cliente cando se gaña o acordo. |
| Data de entrega solicitada | A data de entrega que solicita o cliente. | Esta data úsase como data de finalización cando crea datas de facturación cunha frecuencia específica. |
| Copiar prezos | Un valor que indica se se deben copiar os prezos do contrato desde o contrato de orixe. | Se o campo está configurado en **Si**, as referencias da lista de prezos do proxecto e da lista de prezos do produto cópianse do contrato de orixe ao contrato de destino. Se está establecido en **Non**, utilízanse as listas de prezos predefinidas, en función das últimas listas de prezos da conta ou dos parámetros do proxecto. |

Cando selecciona **Aceptar** na caixa de diálogo, o sistema crea unha copia do contrato, en función dos valores dos parámetros que estableceu. A seguir ábrese o novo contrato.

A seguinte información **non** se copia do contrato de orixe ao contrato de destino, porque é específico para cada contrato:

- Programacións de facturas
- Clientes de contrato e liña de contrato
- Referencia de proxecto nas liñas de contrato baseadas en proxecto
- Información de orzamento de cliente

Cópianse as liñas de contrato para proxectos e produtos, as estimacións nos detalles da liña de contrato e os valores non superables a nivel de contrato. A entrada de prezos e taxas de custo predefinidos depende da selección no campo **Copiar prezos** da páxina de diálogo **Copiar parámetros**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
