---
title: Copiar contratos de proxecto
description: Neste tema se proporciona información sobre a copia de contratos de proxecto en Project Operations.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6da8e3ba8e062f3e06dc7f440caebdd93e496c65
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076037"
---
# <a name="copying-project-contracts"></a>Copiar contratos de proxecto

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

Pode crear facilmente novos contratos de proxecto facendo copias dos contratos existentes de dous xeitos: 

  - Na páxina de lista **Contratos de proxecto** , seleccione un contrato de proxecto e, a seguir, seleccione **Copiar**.
  - Na páxina de detalles **Contrato de proxecto** , seleccione **Copiar**.

Abrirase unha páxina de diálogo onde pode seleccionar os parámetros do contrato copiado. Os seguintes campos están incluídos no diálogo. Dependendo dos valores que seleccione neste diálogo, o proceso de copia pode cambiar.

| **Campo** | **Relevancia, finalidade e orientación** | **Impacto descendente** |
| --- | --- | --- |
| Tema | Introduza o tema do contrato de destino. Cando se abra a páxina diálogo, o sistema configurará este campo co nome do contrato de orixe con **copia** anexa a el. | Non hai ningún impacto descendente para este campo. |
| Cliente | Referencia á empresa ou ao rexistro da conta do cliente. Cando se abra o diálogo, o sistema configurará este campo na conta do contrato de orixe. | Este campo é o cliente principal no contrato. |
| Unidade de contratación | A unidade de organización que se encarga da entrega dos proxectos asociados a esta oferta. Cando se abra a páxina de diálogo, o sistema configurarao na unidade de contratación do contrato de orixe. | A unidade de contratación é a división da empresa que executará os proxectos despois de pechar o acordo. Cada unidade de contratación ten unha moeda. Esta moeda úsase para informar dos custos estimados e reais incorridos durante o proxecto. |
| Moeda | A moeda na que se realizan as transaccións da oferta. Cando se abra a páxina de diálogo, o sistema configurará o campo na moeda do contrato de orixe. Non se pode modificar a moeda. Se é así, o campo **Copiar prezos** sempre está configurado en **Non** porque as listas de prezos do contrato de orixe xa non son relevantes. | A moeda úsase para predefinir listas de prezos, para elaborar estimacións financeiras no contrato e para facturar ao cliente cando se gaña o acordo. |
| Data de entrega solicitada | A data de entrega solicitada polo cliente. | Esta data úsase como data de finalización cando crea datas de facturación cunha frecuencia específica. |
| Copiar prezos | Indica se se deben copiar os prezos do contrato desde o contrato de orixe. | Se o campo está configurado en **Si** , as referencias da lista de prezos do proxecto e da lista de prezos do produto cópianse do contrato de orixe ao contrato de destino. Se se selecciona **Non** , as listas de prezos predefínense en función das últimas listas de prezos da conta ou dos parámetros do proxecto. |

Cando selecciona **Aceptar** na páxina de diálogo, o sistema crea unha copia do contrato en función dos parámetros seleccionados. Abrirase o novo contrato.

A seguinte información non se copia de **Contrato de orixe** a **Contrato de destino** :

  - Programacións de facturas
  - Clientes de contrato e liña de contrato
  - Referencia de proxecto nas liñas de contrato baseadas en proxecto
  - Información de orzamento de cliente

Debido a que esta información é moi específica para cada contrato, estes campos e rexistros non se copian. Cópianse as liñas de contrato para proxectos e produtos, as estimacións sobre os detalles da liña de contrato e os valores non superables a nivel de contrato. Os valores por defecto do prezo e do custo dependen da selección no campo **Copiar prezos** da páxina de diálogo **Copiar parámetros**.
