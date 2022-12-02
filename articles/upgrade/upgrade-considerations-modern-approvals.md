---
title: Consideracións de actualización para aprobacións modernas
description: O artigo recolle os puntos que os administradores deben considerar cando activan a funcionalidade de Aprobacións modernas.
author: stsporen
ms.date: 01/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 44a933c92d4ef8dff40f20200d74c4bbdf8caa76
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931742"
---
# <a name="upgrade-considerations-for-modern-approvals"></a>Consideracións de actualización para aprobacións modernas 

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Como parte da versión da onda 1 de abril de 2022, a funcionalidade de aprobacións modernas activarase de forma predeterminada. Esta funcionalidade mellora a fiabilidade da lóxica de aprobación e garante que pode determinar o motivo se a lóxica de aprobación falla.

Como parte deste cambio, actualízanse os cambios de estado para as aprobacións de proxectos. O estado agora vai directamente desde **Enviado** a **Aprobado**. **Pendente** xa non é un estado para as aprobacións. Para determinar se hai unha aprobación pendente, verifique que a aprobación forma parte dun conxunto de aprobacións e revise o estado do conxunto de aprobacións anexo.

## <a name="before-you-upgrade"></a>Antes de actualizar

Antes de actualizar a aprobacións modernas, asegúrese de que non ten ningunha aprobación pendente. As aprobacións modernas non usan o estado **Pendente**. Polo tanto, todas as aprobacións que aínda estean marcadas como **Pendente** despois da actualización non se procesarán.

## <a name="after-you-upgrade"></a>Despois da actualización

Despois de actualizar ás aprobacións modernas, un administrador debe validar que o fluxo de nube que procesa as aprobacións está activado.

1. Inicie sesión en [flow.microsoft.com](https://flow.microsoft.com)
2. Na parte superior dereita da páxina, cambie o seu ambiente ao ambiente que actualizou.
3. Seleccione **Solucións** para enumerar as solucións que están instaladas no ambiente.
4. Na lista de solucións, seleccione **Project Operations** ou **Project Service**.
5. Cambie o filtro de **Todos** a **Fluxos de nube**.
6. Verifique que a opción **Project Service: programar de forma recorrente os conxuntos de aprobacións do proxecto** está configurada en **Activado**. Se non está, seleccione o fluxo e logo seleccione **Activar**.
7. Verifique que o procesamento se está a producir cada cinco minutos revisando a lista **Traballos do sistema** na área **Configuración**.

## <a name="short-term-rollback"></a>Reversión a curto prazo

Se non pode aceptar os cambios ou se atopa un problema grave con esta funcionalidade, pode volver temporalmente ao fluxo de aprobación orixinal realizando os seguintes pasos:
1. Inicie sesión no seu ambiente e verifique que non hai aprobacións pendentes.
2. Vaia a **Configuración** > **Parámetros do proxecto**
3. Seleccione **Control de funcionalidades** e despois seleccione **Aprobacións modernas** para desactivar a funcionalidade.

## <a name="removing-the-feature-flag"></a>Eliminación de marca de funcionalidade

Na actualización da onda 2 de outubro de 2022, eliminarase a posibilidade de desactivar esta funcionalidade.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
