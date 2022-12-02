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

Contoso publicouse con Microsoft Dynamics 365 Project Operations para escenarios de recursos/sen fornecemento. Como parte das actividades comerciais normais, os proxectos pódense completar ou suspender. Podes desactivar o proxecto para garantir que non se xeren gastos nin facturas.

## <a name="solution"></a>Solución

### <a name="prerequisites"></a>Requisitos previos

-   Microsoft Dynamics 365 Finance 10.0.29 ou posterior debe estar instalado.
-   Mapa de escrita dual 1.0.0.3 para Projects V2 (msdyn\_projects) deben instalarse ou configurarse manualmente como se describe a continuación.

### <a name="create-an-updated-version-of-the-project-operations-integration-projects-v2-dual-write-map"></a>Crear unha versión actualizada do mapa de escrita dual de Projects V2 de integración de Project Operations

Para actualizar o mapa de escrita dual de Projects V2 de Project Operations:

1. Vaia á área de traballo **Xestión de datos** e seleccione **Escrita dual**.
2. Seleccione o mosaico **Escrita dual**.
3. do columna **Mapa de táboa**, localice e seleccione **Project V2 (msdyn\_projects)** e, a seguir, seleccione Deter.
4. Seleccione o nome do mapa para abrir o mapa e, a seguir, seleccione **[Ningún]**.
5. Na caixa de diálogo Seleccionar columna, seleccione **código de estado \[Estado do proxecto\]** e, a seguir, seleccione Aceptar. Pode escribir **estado** no valor do filtro para restrinxir a lista.
6.  Seleccione **Engadir ou editar transformación** na columna **tipo de mapa** para editar a transformación.
7.  Desde **Tipo de transformación** seleccione **ValueMap**.
8.  Seleccione **Engador asignación de valores**, e despois engada as seguintes **Claves** e **Valores**:

   Tecla       | Valor 
   ----------|-------
   InProcess | 0     
   concluída | 1     

![Captura de pantalla que mostra a asignación de escrita dual](media/projectstage-dw-mapping.png)

9. Seleccione **Gardar**.
10. Desde a parte superior da páxina **Escrita dual > Projects V2 (msdyn_projects)**, seleccione **Gardar como**.
11. Desde **Engadir táboa** no campo **Editor**, seleccione **Editor predeterminado de CDS**.
12. Establece o campo **Versión** en 1.0.0.3.
13. Escriba unha **Descrición** e, a seguir, seleccione **Gardar**.
14. Dende a parte superior da páxina **Escrita dual > Projects V2 (msdyn_projects)**, seleccione **Executar** para iniciar o mapa e, a continuación, seleccione **Si** se se lle pide que confirme antes da execución. 

### <a name="close-a-newly-completed-project"></a>Pechar un proxecto rematado recentemente

Dynamics 365 Finance usa o campo **fase do proxecto** campo para diferenciar os proxectos **en proceso** ou **rematados**. Os proxectos **Rematados** non poden incorrer en gastos nin facturar aos clientes.

1. Abra un proxecto para desactivalo.
2. Desde a fita, seleccione **Desactivar**.

> [!NOTE]
> Pode desactivar ou pechar un proxecto xa que ambos se comportarán igual no contexto de Finance.

3. En Finance, abra a páxina **Lista de todos os proxectos**.
4. Confirme que o proxecto desactivado non aparece na lista.
5. No filtro **mostrar proxectos** enriba da lista, cambie o valor de **Activo** a **Todos**.
6. Agora verá o proxecto desactivado.

Se tenta rexistrar o tempo ou os gastos para este proxecto en Finance, non deberías ver o proxecto para a selección. Se introduce manualmente o número do proxecto nun gasto, verás unha mensaxe como "A fase do proxecto rematada non permite gravar no proxecto". A facturación e outras funcións de facturación deberían estar desactivadas xa que se farán no contexto dun proxecto pechado.

