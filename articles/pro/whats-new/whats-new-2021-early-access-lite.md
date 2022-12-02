---
title: Novidades do acceso anticipado da onda 2 de 2021 - Despregamento de Project Operations lite
description: Este artigo ofrece información sobre as funcionalidades dispoñibles na versión de acceso anticipado da onda 2 de 2021 do despregamento de Project Operations lite.
author: sigitac
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d245868c8bd9ff332707a81c074d6c7ae3649378
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924106"
---
# <a name="whats-new-2021-wave-2-early-access---project-operations-lite-deployment"></a>Novidades do acceso anticipado da onda 2 de 2021 - Despregamento de Project Operations lite

_Aplícase a: Despregamento de Lite - acordo para facturación proforma_

Este artigo aplícase aos seguintes compoñentes e versións de Dynamics 365 Project Operations:

  - Project Operations en ambiente de Dataverse versión 4.23.0.4

A versión só se aplica cando un ambiente o [se selecciona no acceso anticipado](/power-platform/admin/opt-in-early-access-updates#how-to-enable-early-access-updates).

## <a name="features-included-in-this-release"></a>Funcionalidades incluídas nesta versión

[Xestión de subcontratos](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview) - Esta funcionalidade proporciona unha mellor visibilidade e control sobre todos os aspectos do traballo nun proxecto. A versión preliminar da xestión de subcontratos inclúe as seguintes capacidades:

  - Un xestor do proxecto pode crear un subcontrato cun fornecedor. De xeito predefinido, as listas de prezos que se xuntan ao rexistro do fornecedor úsanse para o subcontrato. A conta do fornecedor ten un tipo de relación de **Fornecedor** ou **Provedor**.
  - Un xestor do proxecto pode detallar todas as compras como elementos de liña no subcontrato. As liñas de subcontrato poden ser por tempo, gastos ou produtos. A clase de transacción da liña de subcontrato determina para que serve a liña.
  - O xestor de contas do fornecedor e o xestor de proxectos poden repetir o subcontrato. Os prezos poden axustarse nas listas de prezos de compra que se xuntan ao subcontrato.
  - Durante o proceso, se a liña de subcontrato é para tempo, o xestor de contas do fornecedor pode asociar os contactos do fornecedor a cada liña de subcontrato. Esta asociación proporciona información ao xestor do proxecto que está a traballar no subcontrato. Cando un contacto de fornecedor está asociado a unha liña de subcontrato, o sistema crea automaticamente un recurso reservable a partir do contacto, se aínda non existe un recurso reservable.
  - O método de facturación en cada liña de subcontrato pode ser prezo fixo ou tempo e material. Para as liñas de subcontrato a prezo fixo, configúrase un programa de facturas baseado en fitos.
