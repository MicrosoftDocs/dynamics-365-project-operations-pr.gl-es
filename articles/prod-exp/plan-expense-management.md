---
title: Configurar a xestión de gastos
description: Este artigo describe as consideracións e as decisións que debes tomar durante o proceso de planificación antes de configurar a xestión de gastos Microsoft Dynamics 365 Finanzas.
author: KimANelson
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d919a26000b127dd6fb2fd8a49d79e3087f1c403
ms.sourcegitcommit: 7e419a5f73f80fa887084e3b212c90586fc397dd
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/05/2022
ms.locfileid: "8710110"
---
# <a name="configure-expense-management"></a>Configurar a xestión de gastos

Este tema describe as consideracións e as decisións que debe tomar durante o proceso de planificación antes de configurar a xestión de gastos. Na xestión de gastos, pode almacenar información sobre métodos de pago, solicitudes de viaxes, informes de gastos, políticas, etc.

Debido a que moitas das decisións que toma cando planifica a súa configuración para a xestión de gastos baséanse na xerarquía e na estrutura financeira da súa organización, debe consultar os documentos de planificación desas áreas.

## <a name="intercompany-expenses"></a>Gastos entre empresas

Cando activa os gastos entre empresas, permite que as entidades legais e os empregados incorran en gastos por conta doutra entidade legal e cobren o pagamento da entidade legal de emprego dentro da súa organización. Por exemplo, un empregado da entidade legal A completa un proxecto para a entidade legal B e o proxecto supón gastos relacionados con viaxes. Se se activan os gastos entre empresas, o empregado pode presentar un informe de gastos que contabilizará o gasto na entidade legal B e os gastos deberán ser pagados pola entidade legal A. Se a súa organización non ten varias entidades legais, non o fará. Non ten que activar os gastos entre empresas.

**Decisión:** Quere activar os gastos entre empresas?

## <a name="financial-management"></a>Xestión financeira

A xestión dos gastos está moi integrada coa xestión financeira da súa organización. Moita da súa configuración para a xestión de gastos basearase nas decisións que tomou sobre as finanzas da súa organización. As seguintes seccións describen as distintas áreas que requiren planificación e decisións, en función das decisións financeiras da súa organización e das orientacións do seu equipo directivo.

### <a name="per-diems"></a>Dietas

Debe definir as dietas dos empregados que proporciona a súa organización. Debido a que os dietas adoitan empregarse para cubrir gastos como comidas, aloxamento e outros gastos incidentais, pode crear regras para as dietas que ofrece a súa organización. As taxas das dietas poden basearse na época do ano, na localización da viaxe ou en ambas. Cando define unha regra de dietas, pode especificar que se reterá unha porcentaxe da taxa de dietas se un traballador recibe comidas ou servizos de cortesía. Tamén pode definir os niveis de dietas para establecer un número mínimo e máximo de horas que a taxa de dietas se poden aplicar ás viaxes dun traballador.

**Decisións:**

- Regras de dietas predefinidas para os primeiros e últimos días:

    - Cal é o número mínimo de horas que pode solicitar un empregado por día e aínda así recibir unha dieta?
    - Redúcese a cantidade que se ofrece para as comidas do primeiro día e do último día? Se hai unha redución, cal é a porcentaxe da redución?
    - Redúcese a cantidade que se ofrece para o hotel do primeiro día e do último día? Se hai unha redución, cal é a porcentaxe da redución?
    - Redúcese a cantidade que se ofrece para outros gastos no que se incorre o primeiro día e do último día? Se hai unha redución, cal é a porcentaxe da redución?

- Regras de dietas predefinidas:

    - Hai unha redución porcentual do subsidio de dietas para cada comida se, por exemplo, a comida é gratuíta? Se hai unha redución, cal é a porcentaxe da redución por cada comida?
    - Calcúlase a redución das comidas por día, por viaxe ou polo número de comidas ao día?
    - Deberían redondearse as cantidades de dieta de xeito regular ou redondealas?
    - Calcúlanse as dietas nun período de 24 horas ou nun día natural?

- Regras de dietas baseadas na localización:

    - As taxas de dietas varían segundo a localización? Que localizacións se inclúen?
    - Se as taxas de dietas varían segundo a localización, para cada localización, que cantidade porcentual se proporciona para os seguintes tipos de gastos:

        - Comidas
        - Hotel
        - Outros gastos

### <a name="expense-management-journals-and-accounts"></a>Diarios e contas de xestión de gastos

A xestión de gastos require que utilice varios diarios e contas. Debe decidir, por exemplo, se a mesma conta se usa para adiantos de efectivo e disputas de tarxetas de crédito.

**Decisións:**

- En que diario de libro maior se contabilizan os informes de gastos aprobados?
- Que conta se usa para adiantos de efectivo?
- Os adiantos efectivo deberían contabilizarse inmediatamente?

### <a name="payment-methods"></a>Métodos de pagamento

Cando permite aos empregados incorrer en gastos en nome da súa empresa, debe definir os métodos de pagamento que os empregados teñen permiso para usar. Por exemplo, pode permitir que os empregados utilicen efectivo ou unha tarxeta de crédito corporativa. Tamén pode permitir que os empregados utilicen tarxetas de crédito persoais e logo reembolsarlles aos empregados. Debe tomar as seguintes decisións para cada método de pagamento que permita.

**Decisións:**

- Que métodos de pagamento están permitidos?
- Quen é o responsable dos gastos do método de pagamento?
- Hai algún tipo de conta compensada? Se hai un tipo de conta compensada, cal é?
- Se hai un tipo de conta compensada, cal é a conta?
- Se o método de pagamento é unha tarxeta de crédito, debería empregarse só coas transaccións importadas?

### <a name="expense-categories-and-shared-categories"></a>Categorías de gasto e categorías compartidas

Cando os empregados crean un informe de gastos, cada gasto que rexistran debe asociarse a unha categoría de gastos. As categorías de gastos derivan de categorías compartidas que se poden compartir entre as entidades legais da súa organización. Estas categorías tamén se poden compartirse na xestión e contabilidade de proxectos, dependendo da forma na que se defina a súa organización. En función da definición da súa organización e das orientacións do equipo de implementación, debe determinar se as categorías que se usan na xestión de gastos só se usarán na xestión de gastos ou se deben compartise entre a xestión e contabilidade de proxectos e a xestión de gastos. Teña en conta que estas categorías pódense compartir entre Proxecto e Gasto ou Proxecto e Produción, pero non entre Gasto e Produción. Debe tomar as seguintes decisións para cada categoría de gastos.

**Decisións:**

- Que é a categoría de gasto? Entre os exemplos inclúense as categorías de voos, hotel ou quilometraxe.
- A categoría de gasto tamén se pode usar na xestión e contabilidade de proxectos?
- Que é o tipo de gasto?
- Cal é o método de pagamento predefinido para a categoría de gasto?
- Hai que detallar os gastos da categoría de gasto?
- Cal é a principal conta predefinida para a categoría de gasto?
- Cal é o grupo predeterminado do imposto sobre as vendas para a categoría de gasto?
- Permítense métodos adicionais de pagamento para a categoría de gasto? Se se permiten métodos adicionais de pagamento, cales son?
- Hai subcategorías nesta categoría de gasto? Se hai subcategorías, tamén debe tomar as seguintes decisións:

    - Está excluída algunha das subcategorías da recuperación de impostos?
    - Cal é o grupo do imposto sobre as vendas das subcategorías?

Se a categoría de gasto tamén se usa na xestión e contabilidade de proxectos, responda ás preguntas restantes. Se non, vaia á seguinte sección.

- Que contas de custos se utilizarán para os seguintes gastos?

    - Custo
    - Asignación de nóminas
    - WIP-valor de custo
    - Elemento de custo
    - WIP-elemento de valor de custo
    - Perda acumulada
    - WIP-perda acumulada

- Que contas de ingresos se utilizarán para o seguinte?

    - Ingresos facturados
    - Ingresos acumulados-valor de vendas
    - WIP-valor de vendas
    - Ingresos acumulados-produción
    - WIP-produción
    - Ingresos acumulados-beneficio
    - WIP-beneficio
    - Ingresos acumulados-subscrición
    - WIP-subscrición

### <a name="taxes"></a>Impostos

Para os impostos relacionados cos gastos, debe determinar o que está incluído ou activado nos informes de gastos.

**Decisións:**

- O imposto sobre as vendas está incluído nos importes dos gastos?
- Debería activarse a recuperación de impostos sobre os gastos?

    > [!NOTE]
    > Cando planificaba o libro maior, se decidiu aplicar o imposto sobre as vendas dos Estados Unidos e usar as regras fiscais, non pode activar a recuperación de impostos sobre os gastos. (Para aplicar as regras de impostos sobre vendas dos Estados Unidos e usar as regras fiscais, configure a opción **Aplicar regras de impostos sobre as vendas** en **Si**.)

## <a name="policies"></a>Políticas

Ao crear políticas de informes de gastos, pode axudar á súa organización a aforrar tempo e diñeiro cando os empregados incorran en gastos no seu nome. As políticas axudan a garantir que os empregados permanecen dentro do orzamento, proporcionan toda a información requirida e gastan cartos só cando o necesiten. Debe tomar as seguintes decisións para cada política de informe de gastos e cada política de aprobación de informe de gastos que cree.

**Decisións:**

- Cal é o nome da política?
- Para que serve a política de gastos?
- Se anteriormente decidiu activar os gastos entre empresas, a que empresas da súa organización se aplicará esta política?
- Cando entra en vigor a política?
- Cando caduca a política?
- Cal é a regra da política?
- Cal é o resultado da regra da política?


[!INCLUDE[footer-include](../includes/footer-banner.md)]