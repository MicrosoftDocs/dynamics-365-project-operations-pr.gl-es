---
title: Conceptos clave na subcontratación
description: Este tema explica algúns conceptos clave que se aplican á subcontratación en Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 08/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 159eeca3aa9ed0c490be5ce3a8f46c7d7206aebe
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578109"
---
# <a name="key-concepts-in-subcontracting"></a>Conceptos clave na subcontratación

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

O tema explica algúns conceptos clave que debe ter en conta antes de comezar a empregar a funcionalidade de subcontratación en Microsoft Dynamics 365 Project Operations.

## <a name="contracting-unit-on-the-subcontract"></a>Unidade de contratación do subcontrato

A unidade de contratación representa a división ou práctica responsable da entrega do proxecto final. A unidade de contratación é tamén a división que establece a relación contractual co fornecedor.

## <a name="purchase-currency"></a>Moeda de compra

En Project Operations, a moeda de compra é a moeda na que se crea o subcontrato. Tamén é a moeda na que se rexistran os custos dun subcontratista nun proxecto. A moeda de compra pode diferir da moeda do proxecto e, á súa vez, pode diferir da moeda de vendas.

## <a name="billing-methods-on-subcontract-lines"></a>Métodos de facturación en liñas de subcontratación

Para os proxectos, normalmente hai modelos de contratación de tarifa fixa e baseados no consumo. Project Operations admite estes métodos de facturación nos contextos de compra e venda. Para unha compra, os métodos de facturación funcionan do seguinte xeito:

- **Tempo e Material** - Cando unha liña de subcontratación usa o método de facturación **Tempo e Material**, o custo do tempo rexístrase no proxecto cando os subcontratistas traballan nese proxecto e rexistran o tempo. Estas transaccións de custos de subcontratistas combínanse coas partidas da factura do provedor. Neste modelo, os xestores de proxectos que usan Project Operations poden coincidir e verificar as liñas de factura do provedor co tempo do subcontratista que se rexistra e aproba. Despois de completar a verificación, os custos previos que se rexistraron despois da aprobación revértense e os novos custos baseados na factura do provedor créanse no proxecto.
- **Prezo fixo** - Neste modelo de contratación de tarifa fixa, as facturas do fornecedor baséanse en fitos fixos. Non obstante, os recursos dos subcontratistas tamén poden informar do tempo. A hora é entón revisada e aprobada polo xestor do proxecto. Cando se aproba, as Project Operations crean datos reais de custos temporais no proxecto. Despois de que o fornecedor envíe unha factura por un fito, o xestor do proxecto pode comparar os datos de custo rexistrados anteriormente co fito. Cando se completa a verificación, os custos reais revértense e rexístrase o custo baseado no fito.

## <a name="project-price-lists-on-subcontracts"></a>Listas de prezos de proxecto en subcontratistas

As listas de prezos do proxecto son listas de prezos que se usan para establecer prezos de compra de tempo, gasto e outros compoñentes relacionados co proxecto. Pode haber varias listas de prezos, cada unha das cales pode ter o seu propio subcontrato con data efectiva en Project Operations. Project Operations non admite a superposición de datas efectivas nas listas de prezos do proxecto para un subcontrato.

## <a name="transaction-classes-on-subcontracts"></a>Clases de transaccións en subcontratos

Project Operations admite catro tipos de clases de transacción:

- Tempo
- Gasto
- Material
- Cota

Os custos de compra pódense estimar e incorrer só nas clases de transaccións **Tempo**, **Gasto** e **Material**. **Tarifa** é unha clase de transaccións só con ingresos e non está dispoñible no contido da compra.

## <a name="purchase-pricing-dimensions"></a>Dimensións de prezos de compra

As dimensións de prezos permítenlle decidir que atributos se usan para a configuración do prezo de compra e as transaccións por defecto. En relación coa compra, Project Operations só admite conxuntos de dimensións fixas para a configuración do prezo de compra e por defecto. Para a configuración do prezo de compra e por defecto de liñas de subcontratación e transaccións de tempo de subcontratación, os atributos son **Rol** e **Recurso reservable**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
