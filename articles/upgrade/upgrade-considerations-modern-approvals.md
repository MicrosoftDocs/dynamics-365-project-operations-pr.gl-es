---
title: Consideracións de actualización para as aprobacións modernas
description: O tema trata os puntos que os administradores deben ter en conta cando activan a funcionalidade de Aprobacións modernas.
author: stsporen
ms.date: 01/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: a3757f057a801318feccde9be3e49c7b40fa8fcb
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578384"
---
# <a name="upgrade-considerations-for-modern-approvals"></a>Consideracións de actualización para as aprobacións modernas 

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Como parte da versión Wave 1 de abril de 2022, a funcionalidade de aprobacións modernas activarase de forma predeterminada. Esta funcionalidade mellora a fiabilidade da lóxica de aprobación e garante que pode determinar o motivo se a lóxica de aprobación falla.

Como parte deste cambio, actualízanse os cambios de estado para as aprobacións de proxectos. O estado agora vai directamente desde **Enviado** a **Aprobado**. **Pendente** xa non é un estado para as aprobacións. Para determinar se está pendente de aprobación, verifique que a aprobación forma parte dun conxunto de aprobación e revise o estado do conxunto de aprobación adxunto.

## <a name="before-you-upgrade"></a>Antes de actualizar

Antes de actualizar a Modern Approvals, asegúrate de que non tes ningunha aprobación pendente. Modern Approvals non usa o **Pendente** estado. Polo tanto, todas as aprobacións que aínda estean marcadas como **Pendente** despois da actualización non se procesará.

## <a name="after-you-upgrade"></a>Despois de actualizar

Despois de actualizar a Modern Approvals, un administrador debe validar que se habilitou o fluxo na nube que procesa as aprobacións.

1. Iniciar sesión en [flow.microsoft.com](https://flow.microsoft.com)
2. Na parte superior dereita da páxina, cambia o teu ambiente ao ambiente que actualizaches.
3. Seleccione **Solucións** para enumerar as solucións que están instaladas no entorno.
4. Na lista de solucións, seleccione **Operacións do proxecto** ou **Servizo de Proxectos**.
5. Cambia o filtro de **Todos** a **Fluxos de nubes**.
6. Verifique que o **Servizo de proxectos: programa de xeito recorrente conxuntos de aprobación de proxectos** opción está definida en **Activado**. Se non o é, seleccione o fluxo e, a continuación, seleccione **Acende**.
7. Verifique que o procesamento se está a producir cada cinco minutos revisando o **Traballos do sistema** lista na **Configuración** área.

## <a name="short-term-rollback"></a>Reversión a curto prazo

Se non podes aceptar os cambios ou se atopas un problema grave con esta función, podes volver temporalmente ao fluxo de aprobación orixinal realizando os seguintes pasos:
1. Inicia sesión no teu entorno e verifica que non hai aprobacións pendentes.
2. Ir a **Configuración** > **Parámetros do proxecto**.
3. Seleccione **Control de funcións** e despois seleccione **Aprobacións modernas** para desactivar a función.

## <a name="removing-the-feature-flag"></a>Eliminando a bandeira de funcións

Na actualización Wave 2 de outubro de 2022, eliminarase a posibilidade de desactivar esta función.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
