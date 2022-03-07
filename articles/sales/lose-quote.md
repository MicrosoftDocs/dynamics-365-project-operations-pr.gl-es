---
title: Copiar ofertas baseadas en proxecto
description: Este tema ofrece información sobre como copiar ofertas baseadas en proxecto en Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 247f9d33bc2e7b0bcbeae8114bb436ed237efce660d0840e58d536d2a290639e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6992159"
---
# <a name="copy-project-based-quotes"></a>Copiar ofertas baseadas en proxecto

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Pode crear facilmente unha nova oferta de proxecto copiando unha xa existente. 

- Para copiar unha oferta de proxecto, na páxina de lista **Ofertas de proxecto** ou na páxina de detalles **Oferta de proxecto**, seleccione a oferta de proxecto que desexa copiar e logo seleccione **Copiar**.

Abrirase unha páxina de diálogo onde pode introducir os parámetros da copia. A seguinte táboa indica os campos incluídos na páxina de diálogo. Dependendo dos valores que seleccione, o proceso de copia pode cambiar.

| **Campo** | **Descrición** | **Impacto descendente** |
| --- | --- | --- |
| Tema | Introduza o tema ou nome relevante da oferta de destino. Cando se abra o diálogo, o sistema configurarao co tema da oferta de destino con **-copia** anexa a el. | |
| Cliente | Referencia á empresa ou ao rexistro da conta do cliente. Cando se abra o diálogo, o sistema configurarao na conta da oferta de orixe. | Este campo é o cliente principal na oferta. |
| Unidade de contratación | A unidade organizativa que se encarga da entrega dos proxectos asociados a esta oferta.
Cando se abra o diálogo, o sistema configurarao na unidade de contratación da oferta de orixe. | A unidade de contratación é a división da empresa que executará os proxectos despois de pechar a oferta. Cada unidade de contratación ten unha moeda. A moeda úsase para informar dos custos estimados e reais incorridos durante a execución do proxecto. |
| Moeda | Esta é a moeda na que se realizan as transaccións da oferta. Cando se abra o diálogo, o sistema configurarao na moeda da oferta de orixe. Isto pódese modificar e se hai un cambio, o campo **Copiar prezos** sempre se establece en **Non**. Isto débese a que as listas de prezos da oferta de orixe de orixe xa non son relevantes. | A moeda úsase para predefinir unha lista de prezos, para elaborar unha estimación financeira na oferta e, finalmente, para facturar ao cliente cando se gaña a oferta. |
| Data de entrega solicitada | Esta é a data de entrega solicitada polo cliente. | Esta data úsase como data de finalización cando se crean datas de facturación cunha frecuencia específica. |
| Copiar prezos | Un valor Si/Non indica se se debe copiar na oferta o prezo da oferta de orixe. | Se se selecciona **Si**, as referencias da lista de prezos do proxecto e da lista de prezos do produto cópianse da oferta de orixe á oferta de destino. Se se selecciona **Non**, as listas de prezos restablécense por defecto en función das últimas listas de prezos que se configuraron nos parámetros da conta ou do proxecto. |

Cando selecciona **Aceptar** na páxina de diálogo, o sistema crea unha copia da oferta do proxecto en función dos parámetros seleccionados no diálogo. Ábrese a nova oferta de proxecto. 

> [!NOTE]
> A seguinte información non se copia da oferta de orixe á de destino:
>
> - Programacións de facturas
> - Clientes da oferta e da liña de oferta
> - Referencia do proxecto nas liñas de oferta baseada en proxecto -Información sobre o orzamento do cliente
>
>Debido a que esta información é moi específica para cada oferta, estes campos e rexistros non se copian. Cópianse as liñas de oferta para proxectos e produtos, as estimacións sobre os detalles da liña de oferta e os valores que no deben superar o nivel da oferta. Os valores por defecto do prezo e do custo dependen da opción de **Copiar prezos** seleccionada na páxina de diálogo **Copiar parámetros**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]