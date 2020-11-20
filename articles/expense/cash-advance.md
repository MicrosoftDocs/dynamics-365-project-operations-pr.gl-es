---
title: Adianto en efectivo
description: Este tema fornece información sobre adiantos de efectivo.
author: suvaidya
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: c5839fbdab58903555936324139b76f4c94b6c35
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122747"
---
# <a name="cash-advance"></a>Adianto en efectivo

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Un adianto de efectivo permite aos empregados pedir diñeiro prestado á súa empresa antes de incorrer en gastos. Cando se aproba e paga un adianto de efectivo solicitado, o empregado pode usar o diñeiro para os gastos empresariais nos que estea a piques de incorrer. 

## <a name="create-and-submit-a-cash-advance-request"></a>Crear e enviar unha solicitude de adianto de efectivo

1. En **Os meus gastos**, seleccione **Adiantos de efectivo** > **Novo** para crear un novo adianto de efectivo. 
2. Na páxina **Nova solicitude de adianto de efectivo**, introduza a finalidade do gasto e seleccione o lugar onde se incorrerá no gasto.
3. Introduza o importe solicitado e a moeda e seleccione **Gardar**. 
4. Cando estea listo para enviar a solicitude de adianto de efectivo, na páxina **Solicitude de adianto de efectivo**, seleccione **Fluxo de traballo** > **Enviar**.

## <a name="modify-a-cash-advance-request"></a>Modificar unha solicitude de adianto de efectivo

Pode modificar unha solicitude de adianto de efectivo se non se enviou para a súa aprobación.

1. En **Os meus gastos: adiantos de efectivo** localice e seleccione o adianto de efectivo que queira editar.
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

Cando cree e envíe un informe de gastos para o adianto de efectivo que xa recibiu, os gastos axustaranse automaticamente con respecto a ese adianto. Se o seu adianto de efectivo é superior ao importe gastado, deberá devolver o saldo á empresa mediante a categoría de gasto **Devolución de efectivo**. Se o adianto de efectivo pagado pola empresa é inferior ao importe que gastou, a empresa deberá reembolsarlle o saldo. 

### <a name="example"></a>Exemplo
Ten pensado viaxar a unha conferencia desde Seattle ata Nova York. Crea unha solicitude de adianto de efectivo para 3000,00 USD, xa que estimou que o custo do billete de conferencia, voos, hotel, comidas e taxis será de aproximadamente esta cantidade. Non se lle pagará a menos que o seu xestor aprobase esta solicitude. Despois de que o xestor o aprobe, o adianto de efectivo solicitado págase como 3000,00 USD na súa conta bancaria. Despois asistirá á conferencia. Ao finalizar a viaxe, atopa que o gasto total foi de só 2790.00 USD. Seleccione **Efectivo** no campo **Modo de pagamento** e envíe o seu gasto por 2790,00 USD. O importe do gasto enviado axústase automaticamente co adianto de efectivo de 3000,00 USD que lle foi prestado. Agora debe un saldo de 210,00 USD (3000,00-2790,00) á empresa, que pode devolver á empresa usando a categoría de gasto **Devolución de efectivo**. 
