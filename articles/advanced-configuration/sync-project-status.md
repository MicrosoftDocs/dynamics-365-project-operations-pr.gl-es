---
title: Sincronizar o estado do proxecto para evitar a entrada contra proxectos pechados
description: Este artigo explica como sincronizar o estado do proxecto para evitar a entrada de proxectos inactivos ou pechados.
author: ryansandnessMSFT
ms.date: 08/09/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ryansandnessMSFT
ms.openlocfilehash: 7a306da164235f36d9ed5e69196508dce6d257de
ms.sourcegitcommit: 6b6c2bfd04e3e613ed1f38355c7cd47c3a56748d
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/24/2022
ms.locfileid: "9348097"
---
# <a name="sync-project-status-to-prevent-entry-against-closed-projects"></a>Sincronizar o estado do proxecto para evitar a entrada contra proxectos pechados

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

## <a name="scenario"></a>Escenario

Contoso está en directo con Microsoft Dynamics 365 Project Operations para escenarios de recursos/non abastecidos. Como parte das actividades comerciais normais, os proxectos pódense completar ou suspender. Podes desactivar o proxecto para garantir que non se xeren gastos nin facturas.

## <a name="solution"></a>Solución

### <a name="prerequisites"></a>Requisitos previos

-   Microsoft Dynamics Debe instalarse 365 Finance 10.0.29 ou posterior.
-   Mapa de escritura dual 1.0.0.3 para Projects V2 (msdyn\_ proxectos) deben instalarse ou configurarse manualmente como se describe a continuación.

### <a name="create-an-updated-version-of-the-project-operations-integration-projects-v2-dual-write-map"></a>Crea unha versión actualizada do mapa de dobre escritura Projects V2 de integración de Project Operations

Para actualizar o mapa de dobre escritura de Project Operations Projects V2:

1. Vaia ao **Xestión de datos** espazo de traballo e seleccione **Escritura dual**.
2. Seleccione o **Escritura dual** tella.
3. Do T **Mapa de táboa** columna, localiza e selecciona **Proxecto V2 (msdyn\_ proxectos)** e, a continuación, seleccione Deter.
4. Seleccione o nome do mapa para abrir o mapa e, a continuación, seleccione **[Ningún]**.
5. No cadro de diálogo Seleccionar columna, seleccione **código de estado\[ Estado do proxecto\]** e, a continuación, seleccione Aceptar. Podes escribir **estado** no valor do filtro para restrinxir a lista.
6.  Seleccione **Engadir ou editar transformación** no **tipo de mapa** columna para editar a transformación.
7.  Desde **Tipo de transformación** seleccionar **ValueMap**.
8.  Seleccione **Mapeo de valor engadido**, e despois engade o seguinte **Chaves** e **Valores**:

   Tecla       | Valor 
   ----------|-------
   En proceso | 0     
   concluída | 1     

![Captura de pantalla que mostra a asignación de escritura dual](media/projectstage-dw-mapping.png)

9. Seleccione **Gardar**.
10. Dende a parte superior do **Escritura dual > Proxectos V2 (msdyn_projects)** páxina, seleccione **Gardar como**.
11. Desde **Engadir táboa** no **Editora** campo, seleccione **Editor predeterminado de CDS**.
12. Establece o **Versión** campo a 1.0.0.3.
13. Tipo a **Descrición** e, a continuación, seleccione **Gardar**.
14. Dende a parte superior do **Escritura dual > Proxectos V2 (msdyn_projects)** páxina, seleccione **Corre** para iniciar o mapa e, a continuación, sekect **Si** se se lle pide que confirme antes da execución. 

### <a name="close-a-newly-completed-project"></a>Pecha un proxecto recén rematado

Dynamics 365 Finance usa o **fase do proxecto** campo para diferenciar os proxectos **en proceso** ou **rematado**. **Rematou** os proxectos non poden incorrer en gastos nin facturar aos clientes.

1. Abre un proxecto para desactivalo.
2. Desde a cinta, selecciona **Desactivar**.

> [!NOTE]
> Podes desactivar ou pechar un proxecto xa que ambos se comportarán igual no contexto das finanzas.

3. En Finanzas, abra o **Lista de todos os proxectos** páxina.
4. Confirme que o proxecto desactivado non aparece na lista.
5. No **mostrar proxectos** filtro enriba da lista, cambie o valor de **Activo** a **Todos**.
6. Agora verás o proxecto desactivado.

Se tentas rexistrar o tempo ou os gastos para este proxecto en Finanzas, non deberías ver o proxecto para a selección. Se introduces manualmente o número do proxecto nun gasto, verás unha mensaxe como "A fase do proxecto rematada non permite gravar no proxecto". A facturación e outras funcións de facturación deberían estar desactivadas xa que se farán no contexto dun proxecto pechado.

