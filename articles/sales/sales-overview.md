---
title: Visión xeral do proceso de vendas
description: Este tema fornece información sobre os procesos básicos de vendas.
author: rumant
manager: Annbe
ms.date: 10/29/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8300887e7c5fbd78343d16d191775a67e43138e2
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277381"
---
# <a name="sales-process-overview"></a>Visión xeral do proceso de vendas

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Os procesos de vendas que se utilizan nunha organización baseada en proxectos difiren dos procesos de vendas que se utilizan nunha organización baseada en produtos. Isto prodúcese porque os ciclos de vendas das organizacións baseadas en proxectos son máis longos e requiren técnicas de estimación personalizadas para analizar e crear ofertas para cada operación. Dynamics 365 Project Operations usa algunhas das seguintes funcionalidades que se empregan nun proceso de vendas:

- Utilízase un rexistro de Cliente potencial para rastrexar o proceso de vendas.
- Os clientes potenciais cualificados rastréxanse como oportunidades.
- Pódese acceder a todos os artefactos relacionados para unha oportunidade. Estes artefactos inclúen equipo de vendas, partes interesadas, probabilidade, clasificación, fases de vendas e procesos empresariais.
- Créanse varias ofertas para unha oportunidade.
- Unha oferta recibe o estado **Pechada como gañada** para crear un pedido de vendas. En Project Operations, o pedido de vendas personalízase e chámase contrato de proxecto.

## <a name="estimate-a-sale"></a>Estimar unha venda
O valor dunha venda pódese estimar en función dos proxectos entregados anteriormente e da complexidade dos proxectos. Para proxectos que impliquen extensións de proxectos anteriores ou proxectos onde a experiencia do vendedor é alta e se empregan modelos de traballo coñecidos, pode empregar un proceso de estimación máis sinxelo. Os proxectos máis complexos adoitan ter un proceso de compra máis longo. Polo tanto, hai máis fases no proceso de estimación de vendas. Ao comezo do proceso, o equipo de vendas utiliza o aporte de xestores de contas e expertos na materia (SME) para crear unha estimación de alto nivel para cada compoñente distinto do traballo que se oferta. Estes compoñentes do traballo están representados por liñas de oferta. 

Pode crear unha estimación de alto nivel da oferta. Finalmente, esta estimación de alto nivel substituirase por unha estimación máis detallada baseada nun plan de proxecto que cree usando os modelos de proxecto normalizados. Estes modelos axúdanlle a crear un programa e a determinar os valores monetarios na oferta e os seus compoñentes (liñas de oferta). 

Pode crear varias ofertas para un proxecto e agrupalas baixo un único rexistro de oportunidade. Finalmente, unha das ofertas márcase **Pechado como gañada**, e créase un contrato de proxecto ou unha declaración de traballo (SOW). Un contrato de proxecto contén o valor contratado para cada compoñente (liña de contrato) que é aceptado polo cliente para a súa entrega. Normalmente créase unha SOW como documento de Microsoft Word. Todas as facturas que se envían ao cliente ao longo da entrega do proxecto fan referencia ao contrato do proxecto ou ña SOW.

Tamén pode crear ofertas alternativas baixo un rexistro de oportunidade ou configurar o sistema para que se cree un contrato de proxecto cando se gaña unha oferta. Neste caso, pode anexar un documento de Word que representa a SOW no rexistro do contrato do proxecto.

## <a name="configure-the-sales-process"></a>Configurar o proceso de vendas
Pode empregar fluxos do procesos de negocio para configurar o seu proceso de vendas. Estes fluxos proporcionan unha interface visual guiada para facer avanzar nas ofertas polas etapas do proceso de vendas.

Por exemplo, a súa empresa podería ter as seguintes seis fases no proceso de vendas:

1. Cualificar
2. Estimación
3. Revisión interna
4. Contrato
5. Entregar
6. Pechar
 
A súa organización podería usar entidades diferentes para representar a mesma operación a medida que evoluciona. Ao comezo do proceso de vendas, unha operación está representada pola entidade Oportunidade. A medida que pasa o tempo e aparecen máis detalles, pode usar estimacións de alto nivel para crear unha ou varias ofertas. Se unha destas ofertas é revisada por partes interesadas internas e de clientes, a entidade Oferta representa a operación. Despois de que o cliente acepte a oferta, un contrato de proxecto ou SOW representa a operación. Para apoiar este comportamento, as BPF estrutúranse de xeito que cada fase do proceso estea ligada a unha táboa de base de datos diferente.

A fase **Cualificar** do proceso de vendas pode estar apoiada por unha entidade Oportunidade. As fases **Estimación** e **Revisión interna** etapas poden estar apoiadas por unha entidade Oferta. As fases **Contrato**, **Entrega** e **Pechar** poden estar apoiadas por unha entidade Contrato de proxecto.

A medida que fai avanzar as operacións polas fases, solicitaráselle que cree o rexistro de entidade adecuado para axudar e guiar no proceso. As fases poden ser condicionais. Por exemplo, se precisa unha revisión interna dunha oferta só se a oferta usa unha lista de prezos personalizada, pode configurar esa condición na fase adecuada do proceso de negocio. A fase **Revisión interna** móstrase só para ofertas que usan unha lista de prezos personalizada. Para o resto de operacións e ofertas, a fase **Estimación** vai seguida pola fase **Contrato**.

> [!NOTE]
> Project Operations ten páxinas específicas para rexistros das entidades Oportunidade, Oferta, Pedido e Factura. Debe crear estes rexistros empregando as páxinas de información do proxecto para estas entidades. Se non o fai, non poderá abrir os rexistros desde a páxina **Información do proxecto**. Se quere abrir un rexistro desde a páxina **Información do proxecto**, ten que eliminar o rexistro e recrealo usando a páxina **Información do proxecto** onde a lóxica empresarial de cada un destes tipos de entidade garante que o campo **Tipo** do rexistro se defina correctamente e se inicien correctamente todos os conceptos obrigatorios.


## <a name="track-revisions-to-quotes-and-project-plans-in-the-sales-cycle"></a>Rastrexar as revisións de ofertas e plans de proxecto no ciclo de vendas
En Project Operations, non pode rastrexar as revisións feitas a unha oferta. No seu lugar, ten que marcar o a oferta existente **Pechada como perdida** para logo crear unha nova oferta. Pode copiar unha oferta ou clonar unha oferta baseada en proxecto.

## <a name="track-comments-and-approvals-of-quotes-and-project-contracts"></a>Rastrexar comentarios e aprobacións de ofertas e contratos de proxecto
Podes xestionar a revisión e aprobación de ofertas e contratos de proxecto empregando o taboleiro de información e as publicacións. A súa organización pode crear fluxos de traballo personalizados e complementos para atribuír, redirixir, escalar e xestionar as notificacións de revisión e a aprobación de elementos de traballo.


[!INCLUDE[footer-include](../includes/footer-banner.md)]