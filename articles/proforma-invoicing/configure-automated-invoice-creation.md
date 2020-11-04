---
title: Configurar creación automática de facturas
description: Este tema ofrece información sobre como configurar o sistema para xerar facturas automaticamente.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4e7572f2bc6201960ac01ce521adf39ac2577dbe
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076025"
---
# <a name="configure-automatic-invoice-creation"></a>Configurar creación automática de facturas

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_


Complete os seguintes pasos para configurar unha factura automatizada executada en Dynamics 365 Project Operations.

1. Vaia a **Configuración** > **Traballos en lote**.
2. Cree un traballo en lotes noméelo **Crear facturas de Project Operations**. O nome do traballo por lotes debe incluír as palabras "crear facturas".
3. No campo **Tipo de traballo** , seleccione **Ningún**. Por defecto, as opcións **Frecuencia diaria** e **Está activo** están definidas en **Si**.
4. Seleccione **Executar fluxo de traballo**. Na caixa de diálogo **Buscar rexistro** , verá tres fluxos de traballo:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Seleccione **ProcessRunCaller** e, a seguir, seleccione **Engadir**.
6. Na caixa de diálogo seguinte, seleccione **Aceptar**. Un fluxo de traballo **Suspensión** vai seguido por fluxo de traballo **Proceso**.

  > [!NOTE]
  > Tamén pode seleccionar **ProcessRunner** no paso 5. Entón, cando seleccione **Aceptar** , o fluxo de traballo **Proceso** vai seguido por un fluxo de traballo **Suspensión**.

Os fluxos de traballo **ProcessRunCaller** e **ProcessRunner** crean facturas. **ProcessRunCaller** chama a **ProcessRunner**. **ProcessRunner** é o fluxo de traballo que realmente crea as facturas. Percorre todas as liñas de contrato nas que deben crearse as facturas e crea facturas para esas liñas. Para determinar as liñas de contrato para as que deben crearse as facturas, o traballo analiza as datas de execución de facturas para as liñas de contrato. Se as liñas de contrato que pertencen a un contrato teñen a mesma data de execución de facturas, as transaccións combínanse nunha factura que ten dúas liñas de factura. Se non hai transaccións para as que crear facturas, o traballo omite a creación de facturas.

Despois de que **ProcessRunner** remate a execución, chama a **ProcessRunCaller** , fornece a hora de finalización e péchase. A seguir, **ProcessRunCaller** inicia un temporizador que se executa durante 24 horas desde a hora de finalización especificada. Ao final do temporizador, **ProcessRunCaller** péchase.

O traballo de proceso por lotes para crear facturas é un traballo recorrente. Se este proceso de lotes se executa moitas veces, créanse varias instancias do traballo e causan erros. Polo tanto, debe iniciar o proceso por lotes unha soa vez e só debe reinicialo se deixa de executarse.

> [!NOTE]
> A facturación por lotes só se executa para as liñas de contrato do proxecto que están configuradas por programacións de facturas. Unha liña de contrato cun método de facturación de prezos fixos debe ter configurados os fitos. Unha liña de contrato de proxecto cun método de facturación de tempo e material necesitará unha programación de facturas baseado na data configurada. O mesmo se aplica a unha liña de contrato baseada nun proxecto.     
