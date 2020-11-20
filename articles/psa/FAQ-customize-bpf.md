---
title: Como podo personalizar o fluxo do proceso de negocio nas fases do proxecto?
description: Unha visión xeral de como personalizar o fluxo do proceso de negocio de Project Stages.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 10/11/2018
ms.topic: article
author: JohnPBurrows
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
ms.openlocfilehash: a999bbffff848db7a6349df380d9ed5e73c143ab
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4125035"
---
# <a name="how-do-i-customize-the-project-stages-business-process-flow"></a>Como podo personalizar o fluxo do proceso de negocio nas fases do proxecto?
[!INCLUDE[cc-applies-to-psa-app-2-4x-9-0-platform](../includes/cc-applies-to-psa-app-2-4x-9-0-platform.md)]
[!INCLUDE[cc-applies-to-psa-app-1x-8-2-platform](../includes/cc-applies-to-psa-app-1x-8-2-platform.md)]

Existe unha limitación coñecida en versións anteriores da aplicación Project Service que consiste en que os nomes das fases no fluxo do proceso de negocio de fases dos proxecto deben coincidir exactamente cos nomes en inglés previstos (**Quote**, **Plan**, **Close**). En caso contrario, a lóxica empresarial, que depende dos nomes de fase en inglés, non funciona conforme o esperado. Por eso non ve accións familiares como **Mudar proceso** ou **Editar proceso** dispoñibles no formulario do proxecto, e non se recomienda a personalización do fluxo do proceso de negocio. 

Esta limitación abordouse na versión 2.4.5.48 e posteriores. Este artigo suxire solucións para versións anteriores se ten que personalizar o fluxo do proceso de negocio para versións anteriores.  

## <a name="business-logic-requires-an-exact-match-with-english-stage-names"></a>A lóxica empresarial require unha coincidencia exacta cos nomes de fase en inglés.

O fluxo do proceso de negocio de fases dos proxecto inclúe unha lóxica empresarial que dirixe os comportamentos seguintes na aplicación:
- Cando o proxecto está asociada a unha oferta, o código define o fluxo do proceso de negocio á fase **Quote**.
- Cando o proxecto está asociada a un contrato, o código define o fluxo do proceso de negocio á fase **Plan**.
- Cando o fluxo do proceso de negocio avanza á fase **Close**, o rexistro de proxecto está desactivado. Cando o proxecto se desactiva, o formulario de proxecto e a estrutura de subdivisión do traballo (WBS) están definidas a só lectura, libéranse as reservas de recursos denominados e as listas de prezos asociadas desactívanse.

Esta lóxica empresarial depende dos nomes en inglés para as fases do proxecto. Este dependencia nos nomes de fase en inglés é o principal motivo polo que non se recomenda a personalización do fluxo do proceso de negocio nas fases do proxecto, e tamén pola que non ve accións de fluxo do proceso de negocio como **Cambiar proceso** ou **Editar proceso** na entidade do proxecto.

## <a name="what-happens-if-the-stage-names-dont-match-the-english-names"></a>Que ocorre se os nomes de fase non coinciden cos nomes en inglés?

Na versión da aplicación Project Service 1.x na plataforma 8.2, cando os nomes de fase do fluxo do proceso de negocio non coinciden cos nomes de fase en inglés exactamente, omítese a lóxica do negocio que define a fase correcta de ofertas ou contratos, ou que pecha o proxecto. Non se mostra ningunha mensaxe de erro. Por tanto parece que pode personalizar o fluxo do proceso de negocio das fases do proxecto. No entanto, non verá ningún dos procesos automáticos que funcionan con ofertas, contratos, e pechar proxecto.

Na versión da aplicación Project Service 2.4.4.30 ou anterior na plataforma 9.0, houbo un cambio arquitectónico considerable no fluxo do proceso de negocio que requeríu unha reescritura la lóxica empresarial do fluxo do proceso de negocio. Como resultado, se os nomes de fase de proceso non coinciden cos nomes en inglés previstos, recibirá unha mensaxe de erro. 

Por tanto, se desexa personalizar o fluxo do proceso de negocio de fases de proxecto para a entidade de proxecto, só pode engadir fases novas para o fluxo do proceso de negocio predefinido para a entidade de proxecto, mantendo as fases **Quote**, **Plan** e **Close** tal cual. Esta restrición garante que non reciba erros da lóxica empresarial que esperen os nomes de fase no fluxo do proceso de negocio en inglés.

Na versión 2.4.5.48 ou posteriores, a lóxica empresarial descrita neste artigo eliminouse do fluxo do proceso de negocio predefinido para o proxecto. Actualizar a esa versión ou posteriores permitiralle personalizar ou substituir o fluxo do proceso de negocio predefinido por un dos seus propios. 

## <a name="workarounds-for-earlier-versions"></a>Solucións para versións anteriores:

Se actualizar non é unha opción, pode personalizar o fluxo do proceso de negocio das fases do proxecto para a entidade de proxecto dunha das seguintes dúas maneiras:

1. Engada fases adicionais á configuración predefinida, e manteña os nomes de fase en inglés para **Quote**, **Plan** e **Close**.


![Captura de engadir fases á configuración predefinida](media/FAQ-Customize-BPF-1.png)
 
2. Cree o seu propio fluxo do proceso de negocio e convirtao en fluxo do proceso de negocio principal para a entidade de proxecto, que lle permite ter os nomes de fase que desexe. No entanto, se desexa utilizar as mesmas fases de proxecto estándar **Quote**, **Plan** e **Close**, ten que facer algunhas personalizacións alonxadas dos nomes de fase personalizados. A lóxica máis complexa está no proceso de peche do proxecto, que pode activar simplemente desactivando o rexistro de proxecto.

![Personalización de BPF](media/FAQ-Customize-BPF-2.png)

### <a name="additional-considerations-for-project-service-app-version-24430-or-earlier-on-platform-90"></a>Consideracións adicionais da versión da aplicación Project Service 2.4.4.30 ou anterior no plataforma 9.0

En Project Service 2.4.4.30 ou anterior na plataforma 9.0, cun fluxo do proceso de negocio personalizada, o campo **Nome da fase** na entidade do proxecto utilizado na gráfica **Proxecto por fase** e nas visualizacións de lista de proxecto non se actualiza porque está emparellado ao fluxo do proceso de negocio nas fases do proxecto. Para solucionar este problema, siga estes pasos:

- Engada un campo personalizado para capturar a fase de fluxo do proceso de negocio actual se actualiza cando o usuario avanza a través do fluxo do proceso de negocio personalizado.

- Modifique a gráfica **Proxecto por fase** para que funcione co seu campo personalizado en vez da configuración predefinida.

### <a name="steps-to-create-your-own-business-process-flow-for-the-project-entity"></a>Pasos para crear o seu propio fluxo do proceso de negocio para a entidade de proxecto

Para crear o seu propio fluxo do proceso de negocio para a entidade de proxecto, faga o seguinte:

1. Vaia a **Configuración** > **Centro de procesos**. Non copie o fluxo do proceso de negocio nas fases do proxecto, porque iso tamén copia a lóxica empresarial de Project Service.

  ![Crear proceso](media/FAQ-Customize-BPF-3.png)

2. Utilice o Deseñador de procesos para crear os nomes de fase que desexe. Se desexa a mesma funcionalidade que as fases predefinidas para **Quote**, **Plan** e **Close**, ten que creala baseándose nos seus nomes de fase do fluxo do proceso de negocio personalizado.

   ![Captura do Deseñador de procesos utilizado para personalizar BPF](media/FAQ-Customize-BPF-4.png) 

3. No Deseñador de procesos, prema **Ordenar fluxo do proceso** para que o fluxo do proceso de negocio personalizada sexa o principal para a entidade de proxecto movéndoo enriba do fluxo do proceso de negocio nas fases do proxecto á parte superior da lista.


   [Captura da utilización de Ordenar fluxo do proceso](media/FAQ-Customize-BPF-5-720.png)

### <a name="the-following-steps-apply-to-project-service-app-24430-or-earlier-on-the-90-platform"></a>Estes pasos aplícanse a aplicación Project Service 2.4.4.30 ou anterior na plataforma 9.0.

4. Engada un novo campo personalizado á entidade de proxecto para capturar fases personalizada no seu fluxo do proceso de negocio personalizado. Deberá engadir lóxica empresarial (complementos/fluxo de traballo) para actualizar este campo cando a fase do fluxo do proceso de negocio personalizado se actualice.

   ![Captura de personalizar entidades de proxecto](media/FAQ-Customize-BPF-6-720.png)

5. Modifique a gráfica **Proxecto por fase** para usar os seus novos campos personalizados para fases.

   ![Captura de utilizar a gráfica de Proxecto por fase](media/FAQ-Customize-BPF-7-720.png)

6. Modifique as visualizacións para que a entidade de proxecto inclúa o seu novo campo personalizado para fases.

   ![Captura de modificación de visualizacións na entidade de proxecto](media/FAQ-Customize-BPF-8-720.png)

