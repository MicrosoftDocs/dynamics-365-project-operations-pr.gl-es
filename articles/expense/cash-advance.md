---
title: Adianto en efectivo
description: Este artigo fornece información sobre adiantos de efectivo.
author: suvaidya
ms.date: 03/25/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: bc270944faa7c16d2e97a988495a2a16380ba879
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931512"
---
# <a name="cash-advance"></a>Adianto en efectivo

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Un adianto de efectivo permite aos empregados pedir diñeiro prestado á súa empresa antes de incorrer en gastos. Cando se aproba e paga un adianto de efectivo solicitado, o empregado pode usar o diñeiro para os gastos empresariais nos que estea a piques de incorrer. 

## <a name="create-and-submit-a-cash-advance-request"></a>Crear e enviar unha solicitude de adianto de efectivo
Para crear un novo adianto en efectivo e enviar unha solicitude de adianto en efectivo, faga o seguinte: 

1. En **Os meus gastos**, seleccione **Adiantos en efectivo** > **Novo**. 
2. Na páxina **Nova solicitude de adianto de efectivo**, introduza a finalidade do gasto e seleccione o lugar onde se incorrerá no gasto.
3. Introduza o importe solicitado e a moeda e seleccione **Gardar**. 
4. Cando estea listo para enviar a solicitude de adianto de efectivo, na páxina **Solicitude de adianto de efectivo**, seleccione **Fluxo de traballo** > **Enviar**.

## <a name="modify-a-cash-advance-request"></a>Modificar unha solicitude de adianto de efectivo

Pode modificar unha solicitude de adianto de efectivo se non se enviou para a súa aprobación.

1. En **Os meus gastos: adiantos en efectivo** localice e seleccione o adianto en efectivo que quere editar.
2. Seleccione **Editar** e faga os cambios necesarios na solicitude de adianto de efectivo. 
3. Seleccione **Gardar e pechar**.


## <a name="view-cash-advance-requests"></a>Ver solicitudes de adianto de efectivo
Pode revisar a lista de todos os adiantos de efectivo que están en borrador, enviados, en revisión ou pagados en **Os meus gastos: adiantos de efectivo**. 

## <a name="approve-cash-advance-requests"></a>Aprobar solicitudes de adianto de efectivo

Os xestores ou usuarios configurados como responsables de aprobacións no fluxo de traballo poderán aprobar os adiantos de efectivo que se lles envíen para a súa revisión. 

1. Para aprobar un adianto de efectivo, en **Procesar adiantos de efectivo**, seleccione **Adiantos de efectivo para a miña revisión**.
2. Seleccione o adianto de efectivo que precisa revisar e seleccione **Aprobar**.  

## <a name="pay-cash-advances"></a>Pagar adianto de efectivo 
O seguinte procedemento normalmente complétano un contable ou un usuario con permisos de contabilidade.

1. Para publicar os adiantos de efectivo aprobados, seleccione **Adiantos de efectivo aprobados** e, a seguir, seleccione **Pagar e transferir**.  
2. Proporcione os detalles do diario para os adiantos de efectivo e logo seleccione **Aceptar**. 

## <a name="submit-an-expense-report-against-a-paid-cash-advance"></a>Enviar un informe de gastos cun adianto de efectivo pagado 

Cando cree e envíe un informe de gastos para o adianto en efectivo que xa recibiu, os gastos axustaranse automaticamente con ese adianto. Se o seu adianto de efectivo é superior ao importe gastado, deberá devolver o saldo á empresa mediante a categoría de gasto **Devolución de efectivo**. Se o adianto en efectivo pagado pola empresa é inferior ao importe que gastou, a empresa deberá reembolsarlle o saldo. 

### <a name="select-cash-advances-that-apply-to-your-expenses"></a>Seleccionar adiantos de efectivo que se aplican aos seus gastos
Antes de enviar un informe de gastos, pode seleccionar o adianto de efectivo que se axuste ás transaccións de gastos do informe. Para usar esta funcionalidade, as seguintes dúas funcións deben activarse desde a área de traballo **Xestión de funcionalidades**:

  - Os informes de gastos reinventáronse
  - Capacidade para asignar os adiantos de efectivo ás liñas de gasto
 
 Cando estas funcionalidades están activadas:
 
  - Pode engadir un ou máis adiantos de efectivo por cada liña de gasto.
  - O saldo dispoñible dun adianto de efectivo é visible en tempo real cando se garda un informe de gasto. Isto permítelle procesar transaccións de gasto e devolver transaccións en efectivo ao mesmo tempo.
  - Pode seleccionar varios adiantos de efectivo para unha transacción de gasto.
  - Os datos de conciliación de adiantos de efectivo están dispoñibles mediante unha consulta. 
 
Se non usa estas funcións, a funcionalidade seguirá sendo a mesma, reducíndose automaticamente os adiantos de efectivo existentes despois de enviar un gasto.

### <a name="example"></a>Exemplo 
Vostede ten previsto viaxar de Seattle a Nova York para unha conferencia. Crea unha solicitude de adianto en efectivo para 3000,00 USD en función do custo estimado da entrada da conferencia, voos, hotel, comidas e taxi. Non se lle pagará a menos que o seu xestor aprobe esta solicitude. Despois de que o xestor o aprobe, o adianto de efectivo solicitado págase como 3000,00 USD na súa conta bancaria. Despois asistirá á conferencia. Ao finalizar a viaxe, atopa que o gasto total foi de só 2790.00 USD. Seleccione **Efectivo** no campo **Método de pagamento** e envíe o seu gasto por 2790,00 USD. O importe do gasto enviado axústase automaticamente co adianto de efectivo de 3000,00 USD que lle foi prestado. Agora debe un saldo de 210,00 USD (3000,00 - 2790,00), que pode devolver á empresa mediante a categoría de gasto **Devolución de efectivo**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
