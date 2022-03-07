---
title: Procesos de vendas
description: Este tema fornece información sobre os procesos básicos de vendas.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 58d5aa68dd5af7fc2b39caac429948e55bbc94c39dfb7fc9ae15a37cc3c92ce6
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7000529"
---
# <a name="sales-processes"></a>Procesos de vendas

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Os procesos de vendas que se utilizan nunha organización baseada en proxectos difiren dos procesos de vendas que se utilizan nunha organización baseada en produtos. Esta diferenza prodúcese porque os ciclos de vendas das organizacións baseadas en proxectos son máis longos e requiren técnicas de estimación personalizadas para analizar e crear ofertas para cada operación. Dynamics 365 Project Service Automation utiliza unha parte da mesma funcionalidade que se emprega no proceso de vendas para Dynamics 365 Sales. Aquí van algúns exemplos:

- Utilízase unha entidade Cliente potencial para rastrexar o proceso de vendas.
- Os clientes potenciais cualificados rastréxanse como oportunidades. O proceso de vendas tamén pode comezar coa oportunidade.
- Accédese a todos os artefactos relacionados para unha oportunidade. Estes artefactos inclúen equipo de vendas, partes interesadas, probabilidade, clasificación, fases de vendas e procesos empresariais.
- Créanse varias ofertas para unha oportunidade.
- Unha oferta márcase **Pechada como gañada** para crear un pedido de vendas. En PSA, o pedido de vendas personalízase e chámase contrato de proxecto.

A seguinte ilustración mostra un proceso de vendas típico nunha organización baseada en proxectos.

> ![Proceso de vendas nunha organización baseada en proxectos.](media/basic-guide-1.png)

## <a name="estimating-a-sale"></a>Estimación dunha venda
O valor dunha venda pódese estimar en función dos proxectos entregados anteriormente e da complexidade dos proxectos. Para proxectos que impliquen extensións de proxectos anteriores ou proxectos onde a experiencia do vendedor é alta e se empregan modelos de traballo coñecidos, pode empregar un proceso de estimación máis sinxelo. Os proxectos máis complexos adoitan ter un proceso de compra máis longo. Polo tanto, hai máis fases no proceso de estimación de vendas. Ao comezo do proceso, o equipo de vendas utiliza o aporte de xestores de contas e expertos na materia (SME) para comezar a crear unha estimación de alto nivel para cada compoñente distinto do traballo que se oferta. Estes compoñentes do traballo están representados por liñas de oferta. 

Pode crear unha estimación de alto nivel da oferta. Finalmente, esta estimación de alto nivel substituirase por unha estimación máis detallada baseada nun plan de proxecto que cree usando os modelos de proxecto normalizados. Estes modelos axúdanlle a crear un programa e a determinar os valores monetarios na oferta e os seus compoñentes (liñas de oferta). 

Pode crear varias ofertas para un proxecto e agrupalas baixo un tipo de entidade de oportunidade única. Finalmente, unha desas ofertas márcase **Pechado como gañada**, e créase un contrato de proxecto ou unha declaración de traballo (SOW). Un contrato de proxecto contén o valor contratado para cada compoñente (liña de contrato) que é aceptado polo cliente para a súa entrega. Normalmente créase unha SOW como documento de Microsoft Word. Todas as facturas que se envían ao cliente ao longo da entrega do proxecto fan referencia ao contrato do proxecto ou ña SOW.

Tamén pode crear ofertas alternativas baixo un tipo de entidade de oportunidade ou configurar o sistema para que se cree un contrato de proxecto cando se gaña unha oferta. Neste caso, pode anexar un documento de Word que representa a SOW no rexistro do contrato do proxecto.

![Peche de unha oferta para crear un contrato de proxecto.](media/basic-guide-2.png)

## <a name="configuring-the-sales-process"></a>Configuración do proceso de vendas
Pode empregar fluxos de procesos empresariais (BPF) en Microsoft Dynamics 365 para configurar o seu proceso de vendas. Os BPF proporcionan ao seu persoal de vendas unha interface visual guiada que poden usar para facer avanzar as operacións a través das fases típicas da súa empresa.

Por exemplo, a súa empresa podería ter as seguintes seis fases no proceso de vendas:

1. Cualificar
2. Estimación
3. Revisión interna
4. Contrato
5. Entregar
6. Pechar

Estas seis fases están representadas por comiñas angulares (\>) que selecciona para expandir en cada tipo de entidade de oportunidade que cree.

![Configuración do proceso de negocio en Dynamics 365.](media/basic-guide-3.png)
 
A súa organización podería usar entidades diferentes para representar a mesma operación a medida que evoluciona. Ao comezo do proceso de vendas, unha operación está representada pola entidade Oportunidade. A medida que pasa o tempo e aparecen máis detalles, pode usar estimacións de alto nivel para crear unha ou varias ofertas. Se unha destas ofertas é revisada por partes interesadas internas e de clientes, a entidade Oferta representa a operación. Despois de que o cliente acepte a oferta, un contrato de proxecto ou SOW representa a operación. Para apoiar este comportamento, as BPF estrutúranse de xeito que cada fase do proceso estea ligada a unha táboa de base de datos diferente.

A fase **Cualificar** do proceso de vendas pode estar apoiada por unha entidade Oportunidade. As fases **Estimación** e **Revisión interna** etapas poden estar apoiadas por unha entidade Oferta. As fases **Contrato**, **Entrega** e **Pechar** poden estar apoiadas por unha entidade Contrato de proxecto.

A medida que fai avanzar as operacións polas fases, solicitaráselle que cree o rexistro de entidade adecuado para axudar e guiar no proceso. As fases poden ser condicionais. Por exemplo, se precisa unha revisión interna dunha oferta só se a oferta usa unha lista de prezos personalizada, pode configurar esa condición na fase adecuada do proceso de negocio. A fase **Revisión interna** móstrase só para ofertas que usan unha lista de prezos personalizada. Para o resto de operacións e ofertas, a fase **Estimación** vai seguida pola fase **Contrato**.

> [!NOTE]
> PSA ten páxinas específicas para as entidades Oportunidade, Oferta, Pedido e Factura. Debe crear oportunidades de servizo de proxecto, ofertas, pedidos e facturas usando as páxinas de información do proxecto para estas entidades. Se usa outra páxina para crear un rexistro, non poderá abrir o rexistro desde a páxina **Información do proxecto**. Se desexa abrir un rexistro desde a páxina **Información do proxecto**, ten que eliminar o rexistro e recrealo usando a páxina **Información do proxecto**. Na páxina **Información do proxecto**, a lóxica de negocio para cada un destes tipos de entidades asegura que o campo **Tipo** campo do rexistro está configurado correctamente e todos os conceptos obrigatorios están iniciados adecuadamente.

> ![Información do proxecto para un novo pedido.](media/basic-guide-4.png)
 
## <a name="differences-between-project-service-automation-and-sales"></a>Diferenzas entre Project Service Automation e Sales
Aínda que o proceso de vendas en PSA usa as capacidades básicas do proceso de vendas en Sales, ten algunhas diferenzas importantes debido ás variacións nas prácticas de negocio das organizacións baseadas en proxectos. Aquí van algúns exemplos:

- **Ofertas do proxecto** - En Project Service Automation, unha oferta péchase despois de crear un contrato de proxecto a partir dunha oferta. En Sales, pode manter unha oferta aberta despois de gañala. O motivo desta diferenza é que un emparellamento entre un presuposto e un contrato de proxecto é mellor para as organizacións baseadas en proxectos. 
- **Activación e revisións** - En PSA, a activación e as revisións non son compatibles coas ofertas do proxecto. En Sales, pódese bloquear unha oferta para evitar edicións adicionais.
- **Peche dunha oferta como perdida ou gañada** - En PSA, cando unha oferta de proxecto se pecha como gañada ou perdida, a oportunidade permanece aberta. As outras ofertas da oportunidade pecharanse como perdidas. En Sales, cando se pecha unha oferta como gañada ou perdida, solicítase ao usuario que realice unha acción sobre a oportunidade. Dependendo do aporte do usuario, a oportunidade subxacente pode pecharse ou deixarse aberta.

## <a name="tracking-revisions-to-quotes-and-project-plans-in-the-sales-cycle"></a>Rastrexo das revisións de ofertas e plans de proxecto no ciclo de vendas
En PSA, non pode rastrexar as revisións feitas a unha oferta. No seu lugar, ten que marcar o a oferta existente **Pechada como perdida** para logo crear unha nova oferta. Pode copiar unha oferta ou clonar unha oferta baseada en proxecto empregando PSA.

## <a name="tracking-comments-and-approvals-of-quotes-and-project-contracts"></a>Rastrexo de comentarios e aprobacións de ofertas e contratos de proxecto
Podes xestionar a revisión e aprobación de ofertas e contratos de proxecto empregando o taboleiro de información e as publicacións. A súa organización pode crear fluxos de traballo personalizados e complementos para atribuír, redirixir, escalar e xestionar as notificacións de elementos de traballo de revisión e aprobación.


[!INCLUDE[footer-include](../includes/footer-banner.md)]