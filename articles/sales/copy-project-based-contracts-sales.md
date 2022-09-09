---
title: Copiar contratos baseados en proxectos
description: Este artigo ofrece información sobre como copiar contratos de proxecto en Microsoft Dynamics 365 Project Operations.
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
# <a name="copy-project-based-contracts"></a>Copiar contratos baseados en proxectos

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Podes crear novos contratos de proxectos facilmente copiando os contratos existentes de dúas formas:

- No **Contratos de Proxecto** páxina de lista, seleccione un contrato de proxecto e, a continuación, seleccione **Copiar**.
- Na páxina de detalles **Contrato de proxecto**, seleccione **Copiar**.

En ambos os casos, aparece un cadro de diálogo onde se poden configurar os parámetros do contrato copiado. O cadro de diálogo inclúe os seguintes campos. Dependendo dos valores que seleccione, o proceso de copia pode cambiar.

| Campo | Descripción | Impacto descendente |
| --- | --- | --- |
| Tema | Introduza o tema do contrato de destino. Cando se abre a caixa de diálogo, o sistema configura o campo co nome do contrato de orixe, pero a palabra "copiar" engádese a el. | Non hai ningún impacto descendente para este campo. |
| cliente/a | A referencia á empresa ou ao rexistro da conta do cliente. Cando se abre a caixa de diálogo, o sistema configura o campo na conta do contrato de orixe. | Este campo é o cliente principal no contrato. |
| Empresa propietaria | A empresa responsable da entrega dos proxectos asociados a este acordo. Cando se abre a caixa de diálogo, o sistema configura o campo para a empresa propietaria do contrato de orixe. | A empresa propietaria é a persoa xurídica que executará o proxecto despois de pechar o acordo. A moeda da empresa propietaria debe coincidir coa moeda da unidade contratante. |
| Unidade de contratación | A unidade organizativa responsable da entrega dos proxectos asociados a este acordo. Cando se abre a caixa de diálogo, o sistema configura o campo na unidade de contratación do contrato orixe. | A unidade de contratación é a división da empresa que executará os proxectos despois de pechar o acordo. Cada unidade de contratación ten unha moeda. Esta moeda úsase para informar dos custos estimados e reais que se incorren durante o proxecto. |
| Moeda | A moeda na que se realizan as transaccións da oferta. Cando se abre a caixa de diálogo, o sistema configura o campo na moeda do contrato de orixe. Non se pode modificar a moeda. Se o é, o **Copiar prezos** campo sempre está configurado como **Non**, porque as listas de prezos do contrato de orixe xa non son relevantes. | Esta moeda úsase para as listas de prezos predeterminadas, para xerar estimacións financeiras sobre o contrato e para facturar ao cliente cando se gaña o acordo. |
| Data de entrega solicitada | A data de entrega que solicita o cliente. | Esta data úsase como data de finalización cando crea datas de facturación cunha frecuencia específica. |
| Copiar prezos | Un valor que indica se o prezo do contrato debe copiarse do contrato de orixe. | Se o campo está definido como **Si**, as referencias á lista de prezos do proxecto e do produto cópianse do contrato de orixe ao contrato de destino. Se está configurado para **Non**, utilízanse listas de prezos predeterminadas en función das listas de prezos máis recentes dos parámetros da conta ou do proxecto. |

Cando selecciones **Ok** no cadro de diálogo, o sistema crea unha copia do contrato, en función dos valores dos parámetros que estableceu. Despois ábrese o novo contrato.

A seguinte información é **non** copiado do contrato de orixe ao contrato de destino, porque é específico para cada contrato:

- Programacións de facturas
- Clientes de contrato e liña de contrato
- Referencia de proxecto nas liñas de contrato baseadas en proxecto
- Información de orzamento de cliente

Copíanse as liñas de contrato para proxectos e produtos, as estimacións nos detalles das liñas de contrato e os valores que non deben exceder a nivel de contrato. A entrada dos prezos predeterminados e das taxas de custo depende da selección no **Copiar prezos** campo no **Copiar parámetros** caixa de diálogo.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
