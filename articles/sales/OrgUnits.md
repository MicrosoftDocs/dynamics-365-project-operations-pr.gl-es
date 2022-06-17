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

En Microsoft Dynamics 365 Project Operations, un *unidade organizativa* é un grupo ou división distinto nunha empresa de servizos profesionais que emprega recursos facturables que teñen taxas de custo.

Para as empresas de servizos profesionais que empregan recursos técnicos en diferentes áreas de práctica ou liñas de negocio, o custo para cubrir unha función pode variar, dependendo da área de práctica ou da liña de negocio onde se cubra a función. Neste escenario, o concepto de unidades organizativas axuda proporcionando unha forma de agrupar un conxunto de roles facturables nunha división dunha empresa que ten unha estrutura de custos distinta para eses roles.

## <a name="the-concept-of-organizational-units-in-project-operations"></a>O concepto de unidades organizativas nas Operacións do Proxecto

Nas operacións do proxecto, unha unidade organizativa ten unha moeda específica e listas de prezos de custo específicas.

A moeda dunha unidade organizativa é a moeda principal que se usa para rastrexar custos.

Pódense anexar unha ou varias listas de prezos de custo a cada unidade organizativa. Project Operations pon as seguintes limitacións nas listas de prezos que se poden anexar a unha unidade organizativa:

- As listas de prezos deben estar na moeda da unidade organizativa.
- As listas de prezos deben ser listas de prezos de custo.

Ademais, a entidade Recurso inclúe un atributo para a unidade organizativa. Cada recurso pode atribuírse a unha unidade organizativa.

### <a name="roles-of-organizational-units"></a>Roles das unidades organizativas

A unidade organizativa desempeña dúas funcións nas operacións do proxecto:

- **Unidade contratante** - A unidade organizativa que representa ao grupo ou división da empresa que é o principal responsable de gañar a venda e xestionar a entrega de traballos e servizos ao cliente. A unidade contratante identifícase no campo **Unidade contratante** na sección de cabeceira das páxinas **Oportunidade**, **Oferta**, **Contrato do proxecto** e **Proxecto**.
- **Unidade de recursos** - A unidade organizativa á que pertence ou se atribúe un recurso. Esta unidade organizativa pode fornecer os seus recursos para algúns roles en declaracións de traballo (SOW) e proxectos que son propiedade da unidade contratante.

![Unidades contratantes e unidades de recursos.](media/OrgUnits.png)

### <a name="organizational-unit-faq"></a>Preguntas frecuentes sobre unidade organizativa

A continuación móstranse algunhas das preguntas máis frecuentes acerca das unidades organizativas:

#### <a name="how-is-the-organizational-unit-entity-in-project-operations-related-to-the-organization-entity-that-already-exists-in-dynamics-365"></a>Como se relaciona a entidade da Unidade organizativa en Project Operations coa entidade Organización que xa existe en Dynamics 365?

A entidade Organización en Dynamics 365 representa o nome dunha instancia global de Dynamics 365. Este nome normalmente é o nome da empresa global.

A entidade Unidade Organizativa representa un grupo ou división na empresa global. Este grupo ou división ten un conxunto de roles e unha lista de prezos para eses roles, e eses roles e a lista de prezos difiren dos roles e da lista de prezos doutros grupos ou divisións da empresa.

Cando se instala Project Operations, créase unha unidade organizativa predeterminada en función da organización. Todos os recursos existentes están asignados á unidade organizativa predefinida. Se se importan novos usuarios ou recursos de Active Directory en Dynamics 365, o proceso de importación de usuarios asígnaos á unidade organizativa predeterminada en Project Operations.

#### <a name="how-does-the-organizational-unit-entity-differ-from-the-business-unit-entity"></a>En que se diferencia a entidade da Unidade Organizativa da entidade da Unidade de Negocio?

En Dynamics 365, a entidade Unidade de negocio é unha estrutura de seguridade. A asociación dun usuario a unha unidade empresarial determina as entidades e os rexistros de entidades aos que ten acceso o usuario. Tamén determina os permisos (Crear, Ler, Escribir, Eliminar, Anexar, Anexar a, Atribuír ou Compartir) que o usuario ten para eses rexistros de entidades.

A entidade Unidade organizativa representa un grupo ou división da empresa que ten taxas de custo distintas para os empregados que están atribuídos a ela. A asociación dun recurso a unha unidade organizativa determina o custo do recurso para un compromiso de proxecto.

Cando aplique Dynamics 365, optimice a autorización de seguridade para a xerarquía de unidades de negocio e a atribución de usuarios a unidades de negocio. Atribúa todos os usuarios que normalmente deben acceder ao mesmo conxunto de rexistros á mesma unidade de negocio. A unidade organizativa non ten efecto na autorización de seguridade ou o acceso.

**Exemplo que mostra unha diferenza potencial no modelado de unidades organizativas e unidades de negocio**

Contoso, Ltd. ten unha próspera práctica de tecnoloxía de Microsoft. Henrique e Lara son programadores de C\#, pero Lara está nos Estados Unidos, mentres que Henrique está na India. A maioría dos compromisos do proxecto requiren recursos tanto de Contoso India como de Contoso EU, e Prakash e Tricia requiren o mesmo nivel de acceso de seguridade aos proxectos desta área de práctica. Non obstante, o custo dos programadores de Contoso India difire bastante do custo dos programadores de Contoso EUA.

Aquí tes unha forma óptima de deseñar para este escenario usando Dynamics 365 e Project Operations.

1. Cree a práctica tecnolóxica de Microsoft como unidade empresarial e asocie a Henrique e Lara a ela. Deste xeito, axudas a garantir que ambos os empregados teñan o mesmo nivel de acceso de seguridade a calquera proxecto nesa área de práctica. Ambos poderán comprobar o progreso e informar o tempo, os gastos, o uso de material e as actualizacións de tarefas.
2. Crea dúas unidades organizativas para garantir que o custo do proxecto se reflicta correctamente.
3. Asocia a Tricia con Contoso EU e Prakash con Contoso India.
4. Atribúa listas de prezos de custo a ambas unidades organizativas. Deste xeito, axudas a garantir que os custos que se rexistran no proxecto de Prakash e Tricia reflictan con precisión a diferenza de custos entre Contoso EU e Contoso India.

#### <a name="are-organizational-units-related-to-sales-territories-in-dynamics-365"></a>As unidades organizativas están relacionadas coas zonas de vendas en Dynamics 365?

Non hai ningunha asociación nin relación entre zonas de vendas e unidades organizativas. Unha zona de vendas é normalmente unha área xeográfica onde se producen as vendas. Pódese asociar unha lista de prezos de vendas con cada zona de vendas.

Unha unidade organizativa é un grupo ou división interna da empresa que rastrexa os custos dun conxunto de roles que vende a outras divisións ou a clientes externos.

**Exemplo que mostra unha diferenza potencial no modelado de unidades organizativas e territorios de vendas**

Contoso, Ltd. conta con dous centros de desenvolvemento: Contoso EUA e Contoso India. O custo dos recursos varía moito entre estes dous centros de desenvolvemento. Contoso vende os seus servizos de tecnoloxía da información (TI) en moitos mercados internacionais, como América Latina, América do Norte, Asia-Pacífico, Europa Occidental e Oriente Medio. As taxas de facturación para os mesmos roles de proxecto poden variar moito nestes mercados. Contoso EUA e Contoso India deberían constituírse como unidades organizativas e cada unidade organizativa debería ter a súa propia lista de prezos. Asia-Pacífico, América Latina, América do Norte, Europa Occidental e Oriente Medio deberían establecerse como zonas de vendas e cada zona de vendas debería ter a súa propia lista de prezos de vendas.

#### <a name="why-is-there-a-restriction-on-the-association-of-price-lists-with-organizational-units"></a>Por que existe unha restrición na asociación de listas de prezos a unidades organizativas?

Os prezos das vendas adoitan ser exclusivos das zonas xeográficas ou mercados onde se venden servizos. As divisións internas dunha empresa non adoitan ter os seus propios prezos de vendas para o mesmo tipo de servizos. Non obstante, as divisións internas teñen un custo diferente dos produtos vendidos (COGS), dependendo das habilidades das persoas que empregan e das condicións laborais da rexión onde operan. Debido a que as unidades organizativas modélanse como divisións internas dunha empresa, só poden ter listas de prezos de custo.

#### <a name="why-cant-we-associate-sales-price-lists-with-organizational-units"></a>Por que non podemos asociar as listas de prezos de venda con unidades organizativas?

En Project Operations, as listas de prezos de venda pódense asociar con clientes e territorios de vendas. As entidades transaccionais como Oportunidade, Presuposto, Contrato de Proxecto e Proxecto usan listas de prezos de venda anexas á conta do cliente ou ao territorio de vendas para determinar as taxas de facturación e os ingresos potenciais para o compromiso do proxecto.

As listas de prezos de custo están asociadas a unidades organizativas. As entidades transaccionais como Oportunidade, Presuposto, Contrato de Proxecto e Proxecto utilizan as listas de prezos de custo que se anexan á unidade de contratación para determinar os custos dun compromiso do proxecto.

#### <a name="are-organizational-units-hierarchical-in-project-operations"></a>As unidades organizativas son xerárquicas nas Operacións do Proxecto?

Non. Na versión actual de Project Operations, as unidades organizativas non son xerarquizadas. Polo tanto, non pode realizar as seguintes tarefas:

- Configure un patrón para introducir prezos de custo predeterminados que atravese unha xerarquía.
- Informe de ingresos ou custos que se acumulan en diferentes niveis da xerarquía da unidade organizativa.

#### <a name="were-a-big-multinational-firm-that-has-a-complex-multilevel-hierarchy-of-cost-centers-divisions-and-billing-offices-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>Somos unha gran empresa multinacional que ten unha xerarquía complexa e multinivel de centros de custos, divisións e oficinas de facturación. Como podemos utilizar mellor o concepto de unidades organizativas na versión actual de Project Operations?

Cando teña unha xerarquía complexa de centros de custo, divisións, oficinas de facturación, etc., configure os nodos follas desa xerarquía como unidades organizativas distintas.

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

Se a túa xerarquía se asemella a este exemplo, debes configurala como unha lista plana, como se mostra aquí:

- Contoso India - Práctica de SAP - Consultores técnicos
- Contoso India - Práctica de SAP - Consultores funcionais
- Contoso India - Práctica tecnolóxica de Microsoft - Consultores funcionais
- Contoso India - Práctica tecnolóxica de Microsoft - Consultores funcionais
- Contoso EUA - Práctica de SAP - Consultores técnicos
- Contoso EUA - Práctica de SAP - Consultores funcionais
- Contoso EUA - Práctica tecnolóxica de Microsoft - Consultores técnicos
- Contoso EUA - Práctica tecnolóxica de Microsoft - Consultores funcionais

#### <a name="were-a-small-professional-services-company-that-operates-as-only-one-division-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>Somos unha pequena empresa de servizos profesionais que opera como unha única división. Como podemos utilizar mellor o concepto de unidades organizativas na versión actual de Project Operations?

Se a súa empresa opera como unha unidade que ten unha lista de prezos de custo, non terá que configurar ningunha unidade organizativa. A instalación de Project Operations crea unha unidade organizativa predeterminada que ten o mesmo nome que a organización. Por defecto, todos os usuarios están atribuídos á unidade organizativa predefinida. Sempre que o sistema esixe que se seleccione unha unidade organizativa, esta unidade organizativa selecciónase por defecto.

#### <a name="when-a-project-is-created-from-a-quote-or-project-contract-line-the-default-contracting-unit-comes-from-the-quote-or-project-contract-what-is-the-default-contracting-unit-if-a-project-is-created-before-sales-entities-such-as-quote-or-project-contract"></a>Cando un proxecto se crea a partir dunha liña de oferta ou contrato do proxecto, a unidade contratante predeterminada procede da oferta ou do contrato de proxecto. Cal é a unidade de contratación predeterminada se se crea un proxecto antes de entidades de venda como Presuposto ou Contrato de Proxecto?

Cando un proxecto se crea por si só, a unidade contratante predefinida do proxecto baséase no usuario que o crea. Ese usuario tamén é o xestor de proxectos por defecto. Se o proxecto está asignado a unha entidade de vendas, como unha cotización ou un contrato de proxecto, a unidade de contratación do proxecto baséase no seu lugar na entidade de vendas. Neste caso, as estimacións do proxecto poderían recalcularse porque se utiliza a lista de prezos de custo para calcular os cambios de estimación de custos se cambia a unidade contratante. A lista de prezos de venda úsase para calcular as estimacións de vendas que se modificarán para que estean sincronizadas coa lista de prezos do proxecto da cotización.

O **Unidade de Contratación** e **Moeda** os campos do proxecto están bloqueados para a súa edición, porque deben estar sincronizados cos valores da entidade de vendas (cotización ou contrato do proxecto) á que está asignado o proxecto.

## <a name="create-and-maintain-organizational-units-in-project-operations"></a>Crear e manter unidades organizativas en Operacións do Proxecto

Para crear unha unidade organizativa en Project Operations, siga estes pasos.

1. Ir a **Configuración \> Unidades organizativas**.
2. Seleccione **Nova**.
3. No **Xeral** zona, na **Nome** campo, introduza un nome para a unidade organizativa. A continuación, configure os outros campos segundo sexa necesario.
4. Seleccione **Gardar** para crear o rexistro para que poida continuar editándoo.
5. Baixo **Listas de prezos de custo**, seleccione o signo máis (**+**) para engadir unha lista de prezos. Só podes engadir listas de prezos que teñan o **Custo** contexto aquí.
6. No **Nome** campo, seleccione o **Busca** botón e seleccione unha lista de prezos que quere poñer a disposición da unidade organizativa. Continúa engadindo listas de prezos segundo sexa necesario.
7. Cando remates de engadir as listas de prezos, selecciona **Gardar** na esquina inferior dereita da páxina.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
