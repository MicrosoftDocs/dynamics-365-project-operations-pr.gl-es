---
title: Axustes do proxecto
description: Este artigo ofrece información sobre os axustes do proxecto.
author: ryansandness
ms.date: 11/09/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: 52a262adce2bb624bc088e50858e25824f845e5c
ms.sourcegitcommit: bb03ac64e01112c93bb24035a51653a0a88cd5fc
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 11/18/2022
ms.locfileid: "9788364"
---
# <a name="project-adjustments"></a>Axustes do proxecto

_**Aplícase a:** Project Operations para situacións baseadas en produción/con fornecemento_

## <a name="adjustments-overview"></a>Visión xeral dos axustes

Podes configurar Microsoft Dynamics 365 Project Operations para que os usuarios poidan facer cambios nas transaccións publicadas. Pode axustar as transaccións do proxecto individualmente ou seleccionar varias transaccións á vez nunha lista de todas as transaccións do proxecto. Os axustes do proxecto utilízanse, por exemplo, para actualizar masivamente o estado facturable, recalcular o custo despois dun cambio de configuración ou actualizar as fontes de financiamento.

Os usuarios poden acceder á funcionalidade de axuste do proxecto de varias maneiras:

- Ao usar a páxina **Axustar transaccións** á que se pode acceder desde **Xestión de proxectos e contabilidade** \> **Configuración**.
- Usando o botón **Axuste** da páxina **Transaccións publicadas do proxecto** á que se pode acceder desde **Xestión de proxectos e contabilidade** \> **Transaccións**.
- Usando o botón **Axuste** da páxina **Transaccións publicadas do proxecto** no contexto dun proxecto. Pódese acceder a esta páxina desde **Xestión de proxectos e contabilidade** \> **Todos os proxectos**.

To allow for adjustments you must enable one or more transaction statuses from **Project Management and accounting** \> **Project Management and accounting paramaters** on the **General** tab under the section **Allow adjustment of transaction status**. Exemplos de estados de transacción inclúen transaccións publicadas, transaccións facturadas ou transaccións eliminadas. Calquera estado de transacción que estea configurado como **Non**  terá transaccións nese estado que non aparecerán no proceso de axuste como seleccionables para o axuste.

Actualmente está dispoñible unha opción de configuración que se chama **Crear sempre transacción de axuste**  en Xestión de proxectos e parámetros de contabilidade. Podes desactivar esta opción para actualizar a transacción orixinal en lugar de crear novas transaccións durante o axuste nun subconxunto de escenarios. Anunciouse que este parámetro quedará obsoleto o 1 de marzo de 2023. Despois do 1 de marzo de 2023, o sistema sempre se comportará coma se a opción estivese habilitada.

## <a name="adjustments-process-flow"></a>Fluxo do proceso de axustes

Os seguintes pasos mostran o fluxo típico para procesar axustes.

1. Abre a páxina **Axustes do proxecto** .
2. Seleccione **Seleccione** para buscar transaccións que cumpran os criterios de axuste previstos.
3. Na lista de transaccións, seleccione todas as transaccións ou un subconxunto das transaccións para o axuste.
4. Seleccione **Axustar** e modifique os atributos da liña. Alternativamente, se os valores se especificaron manualmente durante a entrada da transacción, pode seleccionar introducir os valores predeterminados do sistema.
5. Devólvese a lista de transaccións e aparece unha marca de verificación na columna **Axuste pendente** para indicar onde se realizaron os cambios. Calquera axuste que teña cambios pendentes móstrase na metade inferior da páxina. Alí, pode facer cambios detallados adicionais máis aló do que se mostraba na páxina anterior.
6. Seleccione **Publicar** para publicar as transaccións de axuste.

Dependendo da configuración, adoitan crearse novas transaccións para o axuste.

- O campo **Estado da factura** da transacción orixinal está definido como **Axustado**.
- Créase unha transacción de reversión para revertir a transacción orixinal e o campo **Estado** defínese como **Axustado**.
- Créase unha nova transacción que ten os cambios que se fixeron durante o proceso de axuste.

### <a name="selecting-multiple-posted-project-transactions-at-a-time-for-adjustments-and-credit-notes"></a>Seleccionando varias transaccións de proxecto publicadas á vez para axustes e notas de crédito

Unha nova función que se introduciu na versión 10.0.30 permite seleccionar varias transaccións para axustar á vez desde a páxina **Transaccións publicadas do proxecto** .

Antes de poder usar esta función, debe estar activada no seu sistema. Os administradores poden usar o espazo de traballo **Xestión de funcións** para comprobar o estado da función e activala se é necesario. No espazo de traballo **Xestión de funcións**, busque e seleccione **Transaccións de proxecto publicadas de selección múltiple para axustes e notas de crédito**, e, a continuación, seleccione **Activar agora**.

Esta función activa as seguintes funcións clave:

- Pódese acceder desde a páxina de transacción publicada nun proxecto mediante o botón **Axuste** existente.
- Permite un control de selección de varias filas na páxina **Transaccións publicadas do proxecto** . Pode aplicar filtros á páxina da lista e seleccionar os seus rexistros antes de comezar os axustes.
- Desactiva o botón **Axuste** se non se pode axustar ningunha transacción ou se selecciona unha combinación de notas de crédito e diarios xuntos en lugar de individualmente.
- Debido á adición do control de selección de varias filas, a ligazón **Custo comprometido** da cinta xa non está desactivada se se seleccionan varias filas.
- Engade a seguinte mensaxe de aviso: "Seleccionou máis de (número seleccionado) rexistros para axustar. Proseguir con esta acción pode levar algún tempo. Estás seguro de que queres continuar con esta acción?"

Esta función tamén elimina o paso 2 do fluxo do proceso que se describiu anteriormente neste artigo. Polo tanto, todas as transaccións que se seleccionaron antes de abrir a páxina **Axustar transaccións**  incluiranse na lista de transaccións para o axuste. Non tes que utilizar o botón **Seleccionar** para buscalos.

> [!NOTE] 
> Aínda que esta función estea desactivada, aínda pode seleccionar varios rexistros para axustar. Non obstante, só un rexistro  *permanecerá seleccionado* e a caixa de diálogo **Seleccionar transaccións** aparecerá inmediatamente despois de seleccionar axustes abertos.

## <a name="adjustment-transaction-statuses-that-can-be-enabled-or-disabled-for-adjustments"></a>Os estados das transaccións de axuste que se poden activar ou desactivar para realizar axustes

Os seguintes estados pódense activar ou desactivar na pestana **Xeral** da páxina **Parámetros de contabilidade e xestión de proxectos** :

- Publicado
- Proposta de factura
- Facturado
- Estimado
- Eliminado
- Saldo inicial (hora)

## <a name="adjustment-parameters"></a>Parámetros de axuste

Estes parámetros están listados na páxina **Parámetros de contabilidade e xestión de proxectos** na pestana **Xerais** na **O axuste** agrupará e modificará o comportamento de como se procesan os axustes. 

| Nome do parámetro | Descripción |
|----------------|-------------
| Cree sempre transacción de axuste | Se este parámetro está activado, o proceso de axuste sempre creará unha nova transacción de reversión e unha nova transacción axustada cando haxa un impacto financeiro ou de informes. Se o parámetro está desactivado, o proceso de axuste actualizará a transacción orixinal en lugar de crear unha reversión e unha nova transacción para un escenario como unha actualización do texto da transacción. |
| Campo de actualización automática | Se este parámetro está habilitado, o sistema volverá calcular o prezo de custo e o prezo de venda. |
| Usa a data de axuste como novo proxecto | Este parámetro úsase para mover transaccións a un futuro período fiscal antes de que o sistema admitise esta función. Non recomendamos que o utilices, porque cambia a data comercial da transacción e quedará obsoleto nunha versión futura. |
| Permitir actividades pechadas | Normalmente, non se poden crear transaccións para actividades pechadas. Se este parámetro está activado, ese comportamento anularase. Polo tanto, pódense crear axustes para actividades pechadas. |
