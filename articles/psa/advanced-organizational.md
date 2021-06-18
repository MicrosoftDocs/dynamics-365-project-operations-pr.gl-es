---
title: Unidades organizativas
description: Este tema fornece información sobre as unidades organizativas en Dynamics 365 Project Service Automation.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/04/2019
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
ms.openlocfilehash: 3be18adfa1d346bdabae7e89375ca2c5a2dbda95
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009614"
---
# <a name="organizational-units"></a>Unidades organizativas 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation, unha unidade organizativa é un grupo ou división definido nunha empresa de servizos profesionais que emprega recursos facturables que teñen taxas de custo.

Para empresas de servizos profesionais que empreguen recursos técnicos en varias áreas de práctica ou liñas de negocio, o custo para cubrir un rol nunha área de práctica ou liña de negocio pode diferir do custo para cubrir un rol noutra área de práctica ou liña de negocio. O concepto de unidades organizativas axuda neste escenario ao proporcionar unha forma de agrupar un conxunto de roles facturables nunha división dunha empresa que ten unha estrutura de custos distinta para estes roles.

## <a name="key-attributes-and-associations-of-organizational-units"></a>Atributos e asociacións clave das unidades organizativas

En PSA, unha unidade organizativa ten unha moeda específica e listas de prezos de custo específicas.

A moeda dunha unidade organizativa é a moeda principal que se usa para rastrexar custos.

Pódense anexar unha ou varias listas de prezos de custo a cada unidade organizativa. PSA pon as seguintes limitacións nas listas de prezos que se poden anexar a unha unidade organizativa:

- As listas de prezos deben estar na moeda da unidade organizativa
- As listas de prezos deben ser de listas de prezos de custo

Ademais, hai un atributo para a unidade organizativa na entidade Recurso. Cada recurso pode atribuírse a unha unidade organizativa.

## <a name="roles-of-organizational-units"></a>Roles das unidades organizativas

A unidade organizativa desempeña dous roles en PSA:

- **Unidade contratante** - A unidade organizativa que representa ao grupo ou división da empresa que é o principal responsable de gañar a venda e xestionar a entrega de traballos e servizos ao cliente. A unidade contratante identifícase no campo **Unidade contratante** na sección de cabeceira das páxinas **Oportunidade**, **Oferta**, **Contrato do proxecto** e **Proxecto**.
- **Unidade de recursos** - A unidade organizativa á que pertence ou se atribúe un recurso. Esta unidade organizativa pode fornecer os seus recursos para algúns roles en declaracións de traballo (SOW) e proxectos que son propiedade da unidade contratante.

> ![Unidades contratantes e unidades de recursos](media/advanced-1.png)

## <a name="organizational-unit-faqs"></a>Preguntas frecuentes sobre as unidades organizativas

A continuación móstranse algunhas das preguntas máis frecuentes acerca das unidades organizativas:

### <a name="how-is-the-organizational-unit-entity-in-psa-related-to-the-organization-entity-that-already-exists-in-dynamics-365"></a>Como se relaciona a entidade Unidade organizativa en PSA coa entidade Organización que xa existe en Dynamics 365?

A entidade Organización en Microsoft Dynamics 365 representa o nome dunha instancia global de Dynamics 365. Este nome normalmente é o nome da empresa global.

A entidade Unidade Organizativa representa un grupo ou división na empresa global. Este grupo ou división ten un conxunto de roles e unha lista de prezos para eses roles, e eses roles e a lista de prezos difiren dos roles e da lista de prezos doutros grupos ou divisións da empresa.

Cando se instala PSA, créase unha unidade organizativa predeterminada baseada na organización. Todos os recursos existentes están asignados á unidade organizativa predefinida. No caso de que se importen novos usuarios ou recursos de Active Directory a Dynamics 365, o proceso de importación de usuarios atribúeos á unidade organizativa predefinida en PSA.
 
### <a name="how-does-the-organizational-unit-entity-differ-from-the-business-unit-entity"></a>En que se diferencia a entidade unidade organizativa da entidade unidade de negocio?

En Dynamics 365, a entidade Unidade de negocio é unha estrutura de seguridade. A asociación dun usuario a unha unidade empresarial determina as entidades e os rexistros de entidades aos que ten acceso o usuario. Tamén determina os permisos (Crear, Ler, Escribir, Eliminar, Anexar, Anexar a, Atribuír ou Compartir) que o usuario ten para eses rexistros de entidades.

A entidade Unidade organizativa representa un grupo ou división da empresa que ten taxas de custo distintas para os empregados que están atribuídos a ela. A asociación dun recurso a unha unidade organizativa determina o custo do recurso para un compromiso de proxecto.

Cando aplique Dynamics 365, optimice a autorización de seguridade para a xerarquía de unidades de negocio e a atribución de usuarios a unidades de negocio. Atribúa todos os usuarios que normalmente deben acceder ao mesmo conxunto de rexistros á mesma unidade de negocio. A unidade organizativa non ten efecto na autorización de seguridade ou o acceso.

#### <a name="example-of-organizational-units-and-business-units"></a>Exemplo de unidades organizativas e unidades de negocio

Contoso, Ltd. ten unha próspera práctica de tecnoloxía de Microsoft. Henrique e Lara son programadores de C\#, pero Lara está nos Estados Unidos, mentres que Henrique está na India. A maioría dos compromisos de proxectos requiren recursos de Contoso India e Contoso Estados Unidos, e Henrique e Lara requiren o mesmo nivel de acceso de seguridade aos proxectos nesta área de práctica. Non obstante, o custo dos programadores de Contoso India difire bastante do custo dos programadores de Contoso Estados Unidos.

Este é un xeito óptimo de deseñar para este escenario empregando Dynamics 365 e PSA.

1. Cree a práctica tecnolóxica de Microsoft como unidade empresarial e asocie a Henrique e Lara a ela. Deste xeito, pode axudar a garantir que os dous empregados teñan o mesmo nivel de acceso de seguridade para calquera proxecto nesa área de práctica. Ambos poderán comprobar o progreso e informar do tempo, gastos e actualizacións de tarefas. 
2. Cree dúas unidades organizativas para garantir que o custo do proxecto estea reflectido correctamente. 
3. Asocie a Lara con Contoso Estados Unidos e asocie a Henrique con Contoso India.
4. Atribúa listas de prezos de custo a ambas unidades organizativas. Deste xeito, pode axudar a garantir que os custos que se rexistran no proxecto para Henrique e Lara reflicten con precisión a diferenza de custos entre Contoso Estados Unidos e Contoso India.

### <a name="are-organizational-units-related-to-sales-territories-in-dynamics-365"></a>As unidades organizativas están relacionadas coas zonas de vendas en Dynamics 365?

Non hai ningunha asociación nin relación entre zonas de vendas e unidades organizativas. Unha zona de vendas é normalmente unha área xeográfica onde se producen as vendas. Pódese asociar unha lista de prezos de vendas con cada zona de vendas.

Unha unidade organizativa é un grupo ou división interna da empresa que rastrexa os custos dun conxunto de roles que vende a outras divisións ou a clientes externos.

#### <a name="example-of-organizational-units-and-sales-territories"></a>Exemplo de unidades organizativas e zonas de vendas

Contoso, Ltd. conta con dous centros de desenvolvemento: Contoso Estados Unidos e Contoso India. Os custos dos recursos difiren moito entre estes dous centros de desenvolvemento.

Contoso vende os seus servizos de TI en moitos mercados internacionais, como América Latina, América do Norte, Asia-Pacífico, Europa Occidental e Oriente Medio. As taxas de facturación para os mesmos roles de proxecto poden variar moito nestes mercados.

Contoso Estados Unidos e Contoso India deberían constituírse como unidades organizativas e cada unidade organizativa debería ter a súa propia lista de prezos. Asia-Pacífico, América Latina, América do Norte, Europa Occidental e Oriente Medio deberían establecerse como zonas de vendas e cada zona de vendas debería ter a súa propia lista de prezos de vendas.

### <a name="why-is-there-a-restriction-on-the-association-of-price-lists-with-organizational-units"></a>Por que existe unha restrición na asociación de listas de prezos a unidades organizativas? 

Os prezos das vendas adoitan ser exclusivos das zonas xeográficas ou mercados onde se venden servizos. As divisións internas dunha empresa non adoitan ter os seus propios prezos de vendas para o mesmo tipo de servizos. Non obstante, as divisións internas teñen un custo diferente dos produtos vendidos (COGS), dependendo das habilidades das persoas que empregan e das condicións laborais da rexión onde operan. Debido a que as unidades organizativas modélanse como divisións internas dunha empresa, só poden ter listas de prezos de custo.

### <a name="why-cant-we-associate-sales-price-lists-to-organizational-units"></a>Por que non podemos asociar listas de prezos de vendas a unidades organizativas?

En PSA, as listas de prezos de vendas poden asociarse a clientes e zonas de vendas. As entidades transaccionais como Oportunidade, Oferta, Contrato de Proxecto e Proxecto usan listas de prezos de vendas que se anexan á conta de cliente ou á zona de vendas para determinar os tipos de facturación e os ingresos potenciais do compromiso de proxecto.

As listas de prezos de custo están asociadas a unidades organizativas. As entidades transaccionais como Oportunidade, Oferta, Contrato de Proxecto e Proxecto usan listas de prezos que se anexan á unidade contratante para determinar os custos dun compromiso de proxecto.

### <a name="are-organizational-units-hierarchical-in-psa"></a>As unidades organizativas son xerárquicas en PSA?

Non. Na versión actual de PSA, as unidades organizativas non son xerárquicas. Isto significa que non pode:

- Configurar un padrón para predefinir os prezos de custo para toda a xerarquía. 
- Informar de ingresos ou custos agrupados en diferentes niveis da xerarquía da unidade organizativa.

### <a name="were-a-big-multinational-firm-with-a-complex-multilevel-hierarchy-of-cost-centers-divisions-and-billing-offices-how-can-we-make-the-best-use-of-the-organizational-unit-concept-in-this-version-of-the-project-service-app"></a>Somos unha gran empresa multinacional cunha xerarquía complexa e multinivel de centros de custos, divisións e oficinas de facturación. Como podemos aproveitar ao máximo o concepto de unidade organizativa nesta versión da aplicación Project Service?

Se ten unha xerarquía complexa de centros de custos, divisións, oficinas de facturación, etc., configure os nós folla desa xerarquía como unidades organizativas distintas.
O seguinte exemplo mostra unha xerarquía típica:

**ContosoIndia**

  - Práctica de SAP 

    - Consultores técnicos 
    - Consultores funcionais 
    
  - Práctica tecnolóxica de Microsoft 

    - Consultores técnicos
    - Consultores funcionais 
    
**Contoso Estados Unidos**

 - Práctica de SAP 

    - Consultores técnicos 
    - Consultores funcionais 
    
 - Práctica tecnolóxica de Microsoft 

    - Consultores técnicos 
    - Consultores funcionais 
 
Se a súa xerarquía é semellante, debe configurala como unha lista plana, como se mostra aquí:
- Contoso India - Práctica de SAP - Consultores técnicos 
- Contoso India - Práctica de SAP - Consultores funcionais       
- Contoso India - Práctica tecnolóxica de Microsoft - Consultores funcionais 
- Contoso India - Práctica tecnolóxica de Microsoft - Consultores funcionais 
- Contoso - Práctica de SAP - Consultores técnicos  
- Contoso Estados Unidos - Práctica de SAP - Consultores funcionais  
- Contoso Estados Unidos - Práctica tecnolóxica de Microsoft - Consultores técnicos 
- Contoso Estados Unidos - Práctica tecnolóxica de Microsoft - Consultores funcionais

### <a name="were-a-small-professional-services-company-that-operates-as-only-one-division-how-can-we-best-use-the-organizational-unit-concept-in-the-current-version-of-psa"></a>Somos unha pequena empresa de servizos profesionais que opera como unha única división. Como podemos empregar mellor o concepto de unidade organizativa na versión actual de PSA?

Se a súa empresa opera como unha unidade que ten unha lista de prezos de custo, non terá que configurar ningunha unidade organizativa. Durante a instalación de PSA, Dynamics 365 crea unha unidade organizativa predefinida que ten o mesmo nome que a organización. Por defecto, todos os usuarios están atribuídos á unidade organizativa predefinida. Sempre que o sistema esixe que se seleccione unha unidade organizativa, esta unidade organizativa selecciónase por defecto.

### <a name="when-a-project-is-created-from-a-quote-or-project-contract-line-the-default-contracting-unit-comes-from-the-quote-or-project-contract-if-a-project-is-created-before-sales-entities-such-as-quote-or-project-contract-what-is-the-default-contracting-unit"></a>Cando un proxecto se crea a partir dunha liña de oferta ou contrato do proxecto, a unidade contratante predeterminada procede da oferta ou do contrato de proxecto. Se un proxecto se crea antes que entidades de vendas como oferta ou contrato de proxecto, cal é a unidade contratante predefinida?

Cando un proxecto se crea por si só, a unidade contratante predefinida do proxecto baséase no usuario que o crea. Ese usuario tamén é o xestor de proxectos por defecto. Se o proxecto se asigna a unha entidade de vendas como oferta ou contrato de proxecto, a unidade contratante do proxecto baséase na entidade de vendas no seu lugar. Neste caso, as estimacións do proxecto poderían recalcularse porque se utiliza a lista de prezos de custo para calcular os cambios de estimación de custos se cambia a unidade contratante. A lista de prezos de vendas úsase para calcular as estimacións de vendas que se cambiarán de xeito que estean en sincronía coa lista de prezos do proxecto na oferta.

Os campos **Unidade contratante** e **Moeda** do proxecto están bloqueados para a súa edición, porque deben estar en sincronía cos valores da entidade de vendas (oferta ou contrato de proxecto) á que se asigna o proxecto.


[!INCLUDE[footer-include](../includes/footer-banner.md)]