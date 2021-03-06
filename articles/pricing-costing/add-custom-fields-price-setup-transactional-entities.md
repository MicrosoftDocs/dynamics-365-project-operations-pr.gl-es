---
title: Engadir campos personalizados requiridos á configuración de prezos e ás entidades transaccionais
description: Este tema ofrece información sobre como engadir as referencias de campo personalizadas requiridas a entidades e a formularios e vistas.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: a27bfe881fdb6431941fa860d279e3e7b526f623
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898304"
---
# <a name="add-required-custom-fields-to-price-setup-and-transactional-entities"></a>Engadir campos personalizados requiridos á configuración de prezos e ás entidades transaccionais

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Este tema supón que completou os procedementos do tema, [Crear campos e entidades para usar como entidades de prezos](create-custom-fields-entities-pricing-dimensions.md). Se non completou eses procedementos, volva e compléteos e despois volva a este tema. 

Neste tema, os procedementos amosaranlle como engadir as referencias de campo personalizadas necesarias ás entidades e aos elementos de interface de usuario (IU) como formularios e vistas.

## <a name="add-custom-pricing-dimension-fields"></a>Engadir campos de dimensión de prezos personalizados 
Despois de que se crearon campos e entidades personalizadas, o seguinte paso é facer que a configuración de prezos e as entidades transaccionais coñezan as entidades personalizadas ou conxuntos de opcións creando campos de referencia. Dependendo de se a lista de dimensións de prezos inclúe dimensións de conxunto de opcións ou dimensións de entidade ou ambas, siga só os pasos de **Dimensións de prezos personalizados baseadas en conxunto de opcións** ou **Dimensións dos prezos personalizados baseadas na entidade**, ou ambos, respectivamente.

### <a name="option-set-based-custom-pricing-dimensions"></a>Dimensións de prezos personalizadas baseadas en conxunto de opcións
Cando unha dimensión de prezos personalizada estea baseada en conxuntos de opcións, engádaa como campo ás entidades clave. No seguinte procedemento, **Localización do traballo de recurso** e **Horas de traballo de recurso** úsanse como dimensións de prezos baseadas en conxunto de opcións. Estas deben engadirse primeiro como campos ás entidades de prezos, **Prezo de rol** e **Sobreprezo de rol**.

1. En Project Operations, seleccione **Configuración** > **Solucións** e prema dúas veces **\<your organization name> dimensións de prezos**. 
2. No explorador de solucións, no panel de navegación da esquerda, seleccione **Entidades > Prezo de rol**.
3. Expanda a entidade **Prezo de rol** e seleccione **Campos**.
4. Seleccione **Novo** para crear un novo campo chamado **Localización de traballo de recurso** e seleccione **Conxunto de opcións** como tipo de campo. 
5. Seleccione **Usar un conxunto de opcións existente**, seleccione o conxunto de opcións **Localización do traballo de recurso** e, a seguir, seleccione **Gardar**.
6. Repita os pasos 1 - 5 para engadir este campo á entidade **Sobreprezo de rol**. 
7. Repita os pasos 1-5 para o conxunto de opcións **Horas de traballo de recurso**.

> [!IMPORTANT]
> Cando engada un campo a máis dunha entidade, use o mesmo nome de campo en todas as entidades. 

Nas fases de vendas e estimación dun proxecto, as estimacións do esforzo laboral que se precisa para completar o traballo **Local** e **No sitio**, en **Horario normal** e **Horas extraordinarias** úsanse para estimar o valor da oferta/proxecto. Os campos **Localización de traballo de recurso** e **Horas de traballo de recurso** engadiranse ás entidades de estimación, **Detalle da liña de oferta**, **Detalle da liña de contrato**, **Membro do equipo de proxecto** e **Liña de estimación**.

1. En Project Operations, seleccione **Configuración** > **Solucións** e logo prema dúas veces **\<your organization name> dimensións de prezos**. 
2. No explorador de solucións, no panel de navegación da esquerda, seleccione **Entidades > Detalle de liña de oferta**.
3. Expanda a entidade **Detalle de liña de oferta** e seleccione **Campos**.
4. Seleccione **Novo** para crear un novo campo chamado **Localización de traballo de recurso** e seleccione o tipo de campo **Conxunto de opcións**. 
5. Seleccione **Usar un conxunto de opcións existente** e **Localización do traballo de recurso** e, a seguir, seleccione **Gardar**.
6. Repita os pasos 1 - 5 para engadir este campo ás entidades **Detalle de liña de contrato de proxecto**, **Membro do equipo de proxecto** e **Liña de estimación**.
7. Repita os pasos 1-6 para o conxunto de opcións **Horas de traballo de recurso**. 

Para a entrega e facturación, o traballo finalizado debe ter un prezo preciso para seleccionar se se realizou **Local** ou **No sitio** e se se completou durante o **Horario normal** ou en **Horas extra** nos datos reais do proxecto. Os campos **Localización de traballo de recurso** e **Horas de traballo de recurso** deben engadirse ás entidades **Entrada de tempo**, **Dato real**, **Detalle de liña de factura**, e **Liña de diario**.

1. Seleccione **Configuración** > **Solucións** e logo prema dúas veces **\<your organization name> dimensións de prezos**.
2. No explorador de solucións, no panel de navegación da esquerda, seleccione **Entidades > Entrada de tempo**.
3. Expanda a entidade **Detalle de liña de oferta** e, a seguir, seleccione **Campos**.
4. Seleccione **Novo** para crear un novo campo chamado **Localización de traballo de recurso** e seleccione **Conxunto de opcións** como tipo de campo. 
5. Seleccione **Usar un conxunto de opcións existente**, seleccione o conxunto de opcións **Localización do traballo de recurso** e, a seguir, seleccione **Gardar**.
6. Repita os pasos 1 - 5 para engadir este campo ás entidades **Dato real**, **Detalle de liña de factura**, e **Liña de diario**.
7. Repita os pasos 1-6 para o conxunto de opcións **Horas de traballo de recurso**. 

Isto completa os cambios de esquema necesarios para as dimensións personalizadas baseadas en conxunto de opcións.

## <a name="entity-based-custom-pricing-dimensions"></a>Dimensións de prezos personalizadas baseadas en entidades

Cando a dimensión de prezos personalizada é unha entidade, engadirá relacións 1: N entre a entidade de dimensión e as entidades clave. Usando o exemplo de título estándar de arriba, é razoable esperar que cada empregado teña asignado un título estándar. Como resultado, necesitará unha relación 1: N desde o título estándar ata o recurso reservable ou unha relación N:1 se se crease desde o recurso reservable ata o título estándar.

1. En Project Operations, seleccione **Configuración** > **Solucións** e logo prema dúas veces **\<your organization name> dimensións de prezos**. 
2. No explorador de solucións, no panel de navegación da esquerda, seleccione **Entidades > Título estándar**.
3. Expanda a entidade **Título estándar** e seleccione **Relacións 1:N**.
4. Seleccione **Nova** para crear unha nova relación 1:N chamada **Título estándar para recurso reservable**. Introduza a información necesaria e, a seguir, seleccione **Gardar**.

Tamén debe engadirse o título estándar ás entidades de prezos, **Prezo de rol** e **Sobreprezo de rol**. Tamén se completa usando relacións 1:N entre as entidades **Título estándar** e **Prezo de rol** e as entidades **Título estándar** e **Sobreprezo de rol**.

1. No explorador de solucións, no panel de navegación da esquerda, seleccione **Entidades > Título estándar**.
2. Expanda a entidade **Título estándar** e seleccione **Relacións 1:N**.
3. Seleccione **Nova** para crear unha nova relación 1:N chamada **Título estándar para prezo de rol**. Introduza a información necesaria e, a seguir, seleccione **Gardar**.
4. Repita os pasos 1 - 4 para crear relacións 1: N entre as entidades **Título estándar** e **Sobreprezo de rol**.

Nas fases de vendas e estimación do proxecto, para o prezo da oferta/proxecto, necesítanse estimacións do esforzo de traballo para cada título estándar. Isto significa que son necesarias relacións 1: N desde o título estándar a cada unha destas entidades de estimación: 

- **Detalle de liña de oferta**
- **Detalle da liña de contrato do proxecto**
- **Membro do equipo do proxecto**
- **Liña de estimación**

5. Repita os pasos 1-5 para crear relacións 1:N desde **Título estándar** ata **Detalle de liña de oferta**, **Detalle da liña de contrato de proxecto**, **Membro do equipo de proxecto** e **Liña de estimación**.

  Nas fases de Entrega e Facturación, o traballo completado por cada título estándar deberá ter un prezo exacto nos datos reais do proxecto. Isto significa que ten que haber relacións 1:N desde **Título estándar** ata **Entrada de tempo**, **Dato real**, **Detalle de liña de factura** e **Entidades de liña de diario**.

6. Repita os pasos 1 - 6 para crear relacións 1:N desde **Título estándar** ata **Entrada de tempo**, **Dato real**, **Detalle de liña de factura** e **Entidades de liña de diario**.

### <a name="set-up-dimension-value-defaulting-using-the-mappings-features-of-the-platform"></a>Configurar o valor de dimensión predefinido utilizando as funcionalidades de asignacións da plataforma
Para a entrada de tempo, sería útil facer o sistema utilizase o título estándar por defecto na entrada de tempo do recurso reservable que está a rexistrar a entrada de tempo. Siga os seguintes pasos para engadir asignacións de campo na relación 1:N desde **Recurso reservable** ata **Entrada de tempo**.

1. No explorador de solucións, no panel de navegación da esquerda, seleccione **Entidades > Título estándar**.
2. Expanda a entidade **Título estándar** e seleccione **Relacións 1:N**.
3. Prema dás veces en **Recurso reservable a entrada de tempo**. Na páxina **Relación**, seleccione **Usar asignacións de campo**. 
4. Seleccione **Novo** para crear unha nova asignación de campo entre o campo **Título estándar** na entidade **Recurso reservable** ao campo de referencia **Título estándar** na entidade **Entrada de tempo**. 

Isto completa os cambios de esquema necesarios para as dimensións personalizadas baseadas en entidades.

##  <a name="add-custom-fields-to-forms-views-and-business-rules"></a>Engadir campos personalizados a formularios, visualizacións e regras de negocio

Despois de facer todos os cambios de esquema necesarios, o seguinte paso é facer visibles os campos na IU engadindo os campos aos formularios e ás visualizacións.

1. Abra o formulario ou a visualización. No panel de navegación dereito, seleccione o campo e arrástreo ao lenzo do formulario. 
2. Se está editando unha visualización, use o panel de navegación dereito, seleccione **Engadir campos** e, na caixa de diálogo **Listado de campos**, seleccione os campos que necesite e seleccione **Aceptar**.

A seguinte táboa fornece unha lista completa de formularios listos para usar, listados por entidade, que terán que ser actualizados cos novos campos. Se ten vistas ou formularios adicionais nas súas personalizacións nestas entidades, engada os novos campos a eles tamén.

| Entity        | Formularios que precisan o novo campo   |Visualizacións que precisan o novo campo      |
| ------------------------------|---------------------------------|----------------------------------|
|  Prezo do rol|• Información |• Prezos de categorías de recursos activos<br> • Visualización asociada do prezo da categoría de recursos|
|  Sobreprezo de rol|• Información|• Sobreprezo de rol activo<br>• Vista asociada a sobreprezo de rol|
|  Detalle da liña da oferta|• Información do proxecto<br>• Creación rápida do proxecto|• Detalles da liña de oferta activos<br>• Detalles da liña de oferta combinados<br>• Visualización asociada de detalles da liña de oferta|
|  Detalle da liña de contrato do proxecto|• Información do proxecto<br>• Creación rápida do proxecto|• Detalles de liña de contrato combinados<br>• Detalles activos da liña de contrato<br>• Visualización asociada aos detalles de liña de contrato|
|  Membro do equipo do proxecto|• Información<br>• Novo formulario|• Membros do equipo de proxecto activos<br>• Membros do equipo do proxecto<br>• Visualización asociada de membros do equipo de proxecto|
|  Entrada de tempo|• Información<br>• Crear entrada de tempo|• As miñas entradas de tempo por data<br>• As miñas entradas de tempo desta semana<br>• Entradas de tempo para aprobar|
|  Liña de diario|• Información<br>• Creación rápida|• Liñas de diario activas<br>• Visualización asociada da liña de diario|
|  Detalle da liña da factura|• Información<br>• Creación rápida|• Detalles da liña de factura activos<br>• Transaccións de facturas imputables<br>• Transaccións de facturas complementarias<br>• Visualización asociada de detalles da liña de factura<br>• Transacción de facturas non imputables|
|  Real|• Información<br>• Datos reais activos|• Visualización asociada dos datos reais|

Os campos personalizados tamén poden ter que engadirse nas regras de negocio segundo o que definira. Un exemplo listo para usar é a regra do negocio **Editabilidade de entrada de tempo en función do estado**. Esta regra define os campos que deben ser bloqueados cando a entrada de tempo está nun estado non editable como **Aprobado**. Engada campos a esta regra de negocio para que os campos estean bloqueados para a súa edición cando a entrada de tempo está nun estado distinto de **Borrador** ou **Devolto**.
