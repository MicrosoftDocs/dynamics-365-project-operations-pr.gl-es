---
title: Unidades organizativas
description: Este artigo describe o concepto de unidades organizativas e explica como crear e manter unidades organizativas en Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 1/31/2022
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
ms.reviewer: johnmichalak
ms.openlocfilehash: a20a37b61db68d70869a11e10bef5d30c422b1eb
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921622"
---
# <a name="organizational-units-overview"></a>Visión xeral das unidades organizativas

En Microsoft Dynamics 365 Project Operations, unha *unidade organizativa* é un grupo ou división definido nunha empresa de servizos profesionais que emprega recursos facturables que teñen taxas de custo.

Para empresas de servizos profesionais que empreguen recursos técnicos en diferentes áreas de práctica ou liñas de negocio, o custo para cubrir un rol podería variar, dependendo da área de práctica ou liña de negocio onde de cubre o rol. Neste escenario, o concepto de unidades organizativas axuda ao proporcionar unha forma de agrupar un conxunto de roles facturables nunha división dunha empresa que ten unha estrutura de custos distinta para eses roles.

## <a name="the-concept-of-organizational-units-in-project-operations"></a>O concepto de unidades organizativas en Project Operations

En Project Operations, unha unidade organizativa ten unha moeda específica e listas de prezos de custo específicas.

A moeda dunha unidade organizativa é a moeda principal que se usa para rastrexar custos.

Pódense anexar unha ou varias listas de prezos de custo a cada unidade organizativa. Project Operations pon as seguintes limitacións nas listas de prezos que se poden anexar a unha unidade organizativa:

- As listas de prezos deben estar na moeda da unidade organizativa.
- As listas de prezos deben ser de listas de prezos de custo.

Ademais, a entidade Recurso inclúe un atributo para a unidade organizativa. Cada recurso pode atribuírse a unha unidade organizativa.

### <a name="roles-of-organizational-units"></a>Roles das unidades organizativas

A unidade organizativa desempeña dous roles en Project Operations:

- **Unidade contratante** - A unidade organizativa que representa ao grupo ou división da empresa que é o principal responsable de gañar a venda e xestionar a entrega de traballos e servizos ao cliente. A unidade contratante identifícase no campo **Unidade contratante** na sección de cabeceira das páxinas **Oportunidade**, **Oferta**, **Contrato do proxecto** e **Proxecto**.
- **Unidade de recursos** - A unidade organizativa á que pertence ou se atribúe un recurso. Esta unidade organizativa pode fornecer os seus recursos para algúns roles en declaracións de traballo (SOW) e proxectos que son propiedade da unidade contratante.

![Unidades contratantes e unidades de recursos.](media/OrgUnits.png)

### <a name="organizational-unit-faq"></a>Preguntas frecuentes sobre a unidade organizativa

A continuación móstranse algunhas das preguntas máis frecuentes acerca das unidades organizativas:

#### <a name="how-is-the-organizational-unit-entity-in-project-operations-related-to-the-organization-entity-that-already-exists-in-dynamics-365"></a>Como se relaciona a entidade Unidade organizativa en Project Operations coa entidade Organización que xa existe en Dynamics 365?

A entidade Organización en Dynamics 365 representa o nome dunha instancia global de Dynamics 365. Este nome normalmente é o nome da empresa global.

A entidade Unidade Organizativa representa un grupo ou división na empresa global. Este grupo ou división ten un conxunto de roles e unha lista de prezos para eses roles, e eses roles e a lista de prezos difiren dos roles e da lista de prezos doutros grupos ou divisións da empresa.

Cando se instala Project Operations, créase unha unidade organizativa predeterminada baseada na organización. Todos os recursos existentes están asignados á unidade organizativa predefinida. No caso de que se importen novos usuarios ou recursos de Active Directory a Dynamics 365, o proceso de importación de usuarios atribúeos á unidade organizativa predefinida en Project Operations.

#### <a name="how-does-the-organizational-unit-entity-differ-from-the-business-unit-entity"></a>En que se diferencia a entidade unidade organizativa da entidade unidade de negocio?

En Dynamics 365, a entidade Unidade de negocio é unha estrutura de seguridade. A asociación dun usuario a unha unidade empresarial determina as entidades e os rexistros de entidades aos que ten acceso o usuario. Tamén determina os permisos (Crear, Ler, Escribir, Eliminar, Anexar, Anexar a, Atribuír ou Compartir) que o usuario ten para eses rexistros de entidades.

A entidade Unidade organizativa representa un grupo ou división da empresa que ten taxas de custo distintas para os empregados que están atribuídos a ela. A asociación dun recurso a unha unidade organizativa determina o custo do recurso para un compromiso de proxecto.

Cando aplique Dynamics 365, optimice a autorización de seguridade para a xerarquía de unidades de negocio e a atribución de usuarios a unidades de negocio. Atribúa todos os usuarios que normalmente deben acceder ao mesmo conxunto de rexistros á mesma unidade de negocio. A unidade organizativa non ten efecto na autorización de seguridade ou o acceso.

**Exemplo que mostra unha diferenza potencial no modelado de unidades organizativas e unidades de negocio**

Contoso, Ltd. ten unha próspera práctica de tecnoloxía de Microsoft. Henrique e Lara son programadores de C\#, pero Lara está nos Estados Unidos, mentres que Henrique está na India. A maioría dos compromisos de proxectos requiren recursos de Contoso India e Contoso EUA, e Henrique e Lara requiren o mesmo nivel de acceso de seguridade aos proxectos nesta área de práctica. Non obstante, o custo dos programadores de Contoso India difire bastante do custo dos programadores de Contoso EUA.

Este é un xeito óptimo de deseñar para este escenario empregando Dynamics 365 e Project Operations.

1. Cree a práctica tecnolóxica de Microsoft como unidade empresarial e asocie a Henrique e Lara a ela. Deste xeito, pode axudar a garantir que os dous empregados teñan o mesmo nivel de acceso de seguridade para calquera proxecto nesa área de práctica. Ambos poderán comprobar o progreso e informar do tempo, gastos, uso de material e actualizacións de tarefas.
2. Cree dúas unidades organizativas para axudar a garantir que o custo do proxecto estea reflectido correctamente.
3. Asocie a Tricia con Contoso EUA e a Prakash con Contoso India.
4. Atribúa listas de prezos de custo a ambas unidades organizativas. Deste xeito, pode axudar a garantir que os custos que se rexistran no proxecto para Henrique e Lara reflicten con precisión a diferenza de custos entre Contoso EUA e Contoso India.

#### <a name="are-organizational-units-related-to-sales-territories-in-dynamics-365"></a>As unidades organizativas están relacionadas coas zonas de vendas en Dynamics 365?

Non hai ningunha asociación nin relación entre zonas de vendas e unidades organizativas. Unha zona de vendas é normalmente unha área xeográfica onde se producen as vendas. Pódese asociar unha lista de prezos de vendas con cada zona de vendas.

Unha unidade organizativa é un grupo ou división interna da empresa que rastrexa os custos dun conxunto de roles que vende a outras divisións ou a clientes externos.

**Exemplo que mostra unha diferenza potencial no modelado de unidades organizativas e territorios de vendas**

Contoso, Ltd. conta con dous centros de desenvolvemento: Contoso EUA e Contoso India. O custo dos recursos difire moito entre estes dous centros de desenvolvemento. Contoso vende os seus servizos de tecnoloxía de información (TI) en moitos mercados internacionais, como América Latina, América do Norte, Asia-Pacífico, Europa Occidental e Oriente Medio. As taxas de facturación para os mesmos roles de proxecto poden variar moito nestes mercados. Contoso EUA e Contoso India deberían constituírse como unidades organizativas e cada unidade organizativa debería ter a súa propia lista de prezos. Asia-Pacífico, América Latina, América do Norte, Europa Occidental e Oriente Medio deberían establecerse como zonas de vendas e cada zona de vendas debería ter a súa propia lista de prezos de vendas.

#### <a name="why-is-there-a-restriction-on-the-association-of-price-lists-with-organizational-units"></a>Por que existe unha restrición na asociación de listas de prezos a unidades organizativas?

Os prezos das vendas adoitan ser exclusivos das zonas xeográficas ou mercados onde se venden servizos. As divisións internas dunha empresa non adoitan ter os seus propios prezos de vendas para o mesmo tipo de servizos. Non obstante, as divisións internas teñen un custo diferente dos produtos vendidos (COGS), dependendo das habilidades das persoas que empregan e das condicións laborais da rexión onde operan. Debido a que as unidades organizativas modélanse como divisións internas dunha empresa, só poden ter listas de prezos de custo.

#### <a name="why-cant-we-associate-sales-price-lists-with-organizational-units"></a>Por que non podemos asociar listas de prezos de vendas a unidades organizativas?

En Project Operations, as listas de prezos de vendas poden asociarse a clientes e zonas de vendas. As entidades transaccionais como Oportunidade, Oferta, Contrato de Proxecto e Proxecto usan listas de prezos de vendas que se anexan á conta de cliente ou á zona de vendas para determinar os tipos de facturación e os ingresos potenciais para o compromiso de proxecto.

As listas de prezos de custo están asociadas a unidades organizativas. As entidades transaccionais como Oportunidade, Oferta, Contrato de Proxecto e Proxecto usan listas de prezos que se anexan á unidade contratante para determinar os custos dun compromiso de proxecto.

#### <a name="are-organizational-units-hierarchical-in-project-operations"></a>As unidades organizativas son xerárquicas en Project Operations?

Non. Na versión actual de Project Operations, as unidades organizativas non son xerárquicas. Polo tanto, non pode realizar as seguintes tarefas:

- Configurar un padrón para introducir os prezos de custo predefinidos para toda a xerarquía.
- Informar de ingresos ou custos que se agrupan en diferentes niveis da xerarquía da unidade organizativa.

#### <a name="were-a-big-multinational-firm-that-has-a-complex-multilevel-hierarchy-of-cost-centers-divisions-and-billing-offices-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>Somos unha gran empresa multinacional que ten unha xerarquía complexa e multinivel de centros de custos, divisións e oficinas de facturación. Como podemos empregar mellor o concepto de unidades organizativas na versión actual de Project Operations?

Se ten unha xerarquía complexa de centros de custos, divisións, oficinas de facturación, etc., configure os nós folla desa xerarquía como unidades organizativas distintas.

O seguinte exemplo mostra unha xerarquía típica.

**Contoso India**

- Práctica de SAP

    - Consultores técnicos
    - Consultores funcionais

- Práctica tecnolóxica de Microsoft

    - Consultores técnicos
    - Consultores funcionais

**Contoso EUA**

- Práctica de SAP

    - Consultores técnicos
    - Consultores funcionais

- Práctica tecnolóxica de Microsoft

    - Consultores técnicos
    - Consultores funcionais

Se a súa xerarquía é semellante a este exemplo, debe configurala como unha lista plana, como se mostra aquí:

- Contoso India - Práctica de SAP - Consultores técnicos
- Contoso India - Práctica de SAP - Consultores funcionais
- Contoso India - Práctica tecnolóxica de Microsoft - Consultores funcionais
- Contoso India - Práctica tecnolóxica de Microsoft - Consultores funcionais
- Contoso EUA - Práctica de SAP - Consultores técnicos
- Contoso EUA - Práctica de SAP - Consultores funcionais
- Contoso EUA - Práctica tecnolóxica de Microsoft - Consultores técnicos
- Contoso EUA - Práctica tecnolóxica de Microsoft - Consultores funcionais

#### <a name="were-a-small-professional-services-company-that-operates-as-only-one-division-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>Somos unha pequena empresa de servizos profesionais que opera como unha única división. Como podemos empregar mellor o concepto de unidades organizativas na versión actual de Project Operations?

Se a súa empresa opera como unha unidade que ten unha lista de prezos de custo, non terá que configurar ningunha unidade organizativa. A instalación de Project Operations crea unha unidade organizativa predefinida que ten o mesmo nome que a organización. Por defecto, todos os usuarios están atribuídos á unidade organizativa predefinida. Sempre que o sistema esixe que se seleccione unha unidade organizativa, esta unidade organizativa selecciónase por defecto.

#### <a name="when-a-project-is-created-from-a-quote-or-project-contract-line-the-default-contracting-unit-comes-from-the-quote-or-project-contract-what-is-the-default-contracting-unit-if-a-project-is-created-before-sales-entities-such-as-quote-or-project-contract"></a>Cando un proxecto se crea a partir dunha liña de oferta ou contrato do proxecto, a unidade contratante predeterminada procede da oferta ou do contrato de proxecto. Cal é a unidade contratante predefinida se un proxecto se crea antes que entidades de vendas como Oferta ou Contrato de proxecto?

Cando un proxecto se crea por si só, a unidade contratante predefinida do proxecto baséase no usuario que o crea. Ese usuario tamén é o xestor de proxectos por defecto. Se o proxecto se asigna a unha entidade de vendas como oferta ou contrato de proxecto, a unidade contratante do proxecto baséase na entidade de vendas no seu lugar. Neste caso, as estimacións do proxecto poderían recalcularse porque se utiliza a lista de prezos de custo para calcular os cambios de estimación de custos se cambia a unidade contratante. A lista de prezos de vendas úsase para calcular as estimacións de vendas que se cambiarán de xeito que estean en sincronía coa lista de prezos do proxecto da oferta.

Os campos **Unidade contratante** e **Moeda** do proxecto están bloqueados para a súa edición, porque deben estar en sincronía cos valores da entidade de vendas (oferta ou contrato de proxecto) á que se asigna o proxecto.

## <a name="create-and-maintain-organizational-units-in-project-operations"></a>Crear e manter unidades organizativas en Project Operations

Para crear unha unidade organizativa en Project Operations, siga estes pasos.

1. Vaia a **Configuración \> Unidades organizativas**.
2. Seleccione **Nova**.
3. Na área **Xeral**, no campo **Nome**, introduza un nome para a unidade organizativa. A continuación, configure os outros campos segundo sexa necesario.
4. Seleccione **Gardar** para crear o rexistro para poder editalo.
5. En **Listas de prezos de custo**, seleccione o signo máis (**+**) para engadir unha lista de prezos. Só pode engadir listas de prezos que teñan o contexto de **Custo** aquí.
6. No campo **Nome**, seleccione o botón **Buscar** e seleccione a lista de prezos que desexa que estea dispoñible para a unidade organizativa. Continúe para engadir listas de prezos segundo sexa necesario.
7. Cando termine de engadir listas de prezos, seleccione a icona **Gardar** na esquina inferior dereita da páxina.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
