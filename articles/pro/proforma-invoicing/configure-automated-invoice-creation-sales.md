---
title: Configurar creación automática de facturas - lite
description: Este tema ofrece información sobre a configuración da creación automática de facturas proforma.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0ce9cb9090c44762f370bf8d574d179077b6a821
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176564"
---
# <a name="configure-automatic-invoice-creation---lite"></a>Configurar creación automática de facturas - lite
 
_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

Pode configurar a creación automática de facturas en Dynamics 365 Project Operations. O sistema crea un borrador de factura proforma baseado na programación de facturas de cada contrato de proxecto e liña de contrato. As programacións de facturas configúranse a nivel de liña de contrato. Cada liña dun contrato pode ter unha programación de facturas distinta ou pode incluírse a mesma programación de facturas en cada liña do contrato.

Cando crea unha factura, o sistema sempre crea polo menos unha factura por contrato de proxecto. Nalgúns casos, pode haber varias facturas creadas.

Por exemplo, se o contrato ten varios clientes, crearase o mesmo número de facturas que o número de clientes que teñen que facturar transaccións facturables nese contrato do proxecto.

## <a name="understand-how-transactions-are-included-on-an-invoice"></a>Comprender como se inclúen as transaccións nunha factura 

Ás veces, cada liña de contrato baseada en proxectos especifica unha programación de facturas independente. Por exemplo, os servizos de implementación do contrato de Adatum teñen as seguintes liñas de contrato:

- Traballo de prototipo que é un prezo fixo con dous fitos creados manualmente.
- Traballo de implementación que inclúe o tempo e que se facturará cada dous semanas os luns.
- Gastos incorridos que deben ser facturados mensualmente o primeiro luns de cada mes.

As programacións de facturas definidas en cada unha destas dúas partidas parécense á seguinte táboa:

| Liña de contrato | Data de execución da factura | Data límite da transacción | Data do fito | Cantidade do fito |
| --- | --- | --- | --- | --- |
| Traballo de prototipo | Luns 5 de outubro | - | Luns 5 de outubro | 5000 USD |
| - | Martes 3 de decembro | - | Martes 3 de decembro | 12,000 USD |
| Traballo de implementación | Luns 5 de outubro | Domingo 4 de outubro | - | - |
| - | Luns 19 de outubro | Domingo 18 de outubro | - | - |
| - | Luns 2 de novembro | Domingo 1 de novembro | - | - |
| - | Luns 16 de novembro | Domingo 15 de novembro | - | - |
| Gastos incorridos | Luns 5 de outubro | Domingo 4 de outubro | - | - |
| - | Luns 2 de novembro | Domingo 1 de novembro | - | - |

Neste exemplo cando se executa a facturación automática:

- **4 de outubro ou calquera data anterior**: Non se xera ningunha factura por este contrato porque a táboa **Programación de facturas** para cada unha destas liñas de contrato non indica o domingo 4 de outubro como data de execución da factura.
- **Luns 5 de outubro**: Xérase unha factura por:

    - Traballo de prototipo que inclúe o fito, se está marcado como **Listo para facturar**.
    - Traballo de implementación que inclúe todas as transaccións de tempo creadas antes da data de corte da transacción de domingo 4 de outubro, que está marcada como **Lista para facturar**.
    - Gasto incorrido que inclúe todas as transaccións de gasto creadas antes da data de corte da transacción de domingo 4 de outubro, que está marcada como **Lista para facturar**.
  
- **O 6 de outubro ou calquera data anterior ao 19 de outubro**: Non se xera ningunha factura por este contrato porque a táboa **Programación de facturas** para cada unha destas liñas de contrato non indica o 6 de outubro ou calquera data anterior ao 19 de outubro como data de execución da factura.
- **Domingo 19 de outubro**: Xérase unha factira por traballo de implementación que inclúe todas as transaccións de tempo creadas antes da data de corte da transacción de domingo 1 de outubro, que está marcada como **Lista para facturar**.
- **Luns 2 de novembro**: Xérase unha factura por:

    - Traballo de implementación que inclúe todas as transaccións de tempo creadas antes da data de corte da transacción de domingo 1 de novembro, que está marcada como **Lista para facturar**.
    - Gasto incorrido que inclúe todas as transaccións de gasto creadas antes da data de corte da transacción de domingo 1 de novembro, que está marcada como **Lista para facturar**.

- **Martes 3 de novembro**: Xérase unha factura para o traballo de prototipo xerado que inclúe o fito para 12000 USD, se está marcado como **Listo para facturar**.

## <a name="configure-automatic-invoicing"></a>Configurar facturación automática

Complete os pasos seguintes para configurar unha factura automatizada executada.

1. En **Project Operations**, vaia a **Configuración** > **Configuración de facturas periódicas**.
2. Cree un traballo en lote e noméelo **Crear facturas de Project Operations**. O nome do traballo en lote debe incluír as palabras "crear facturas".
3. No campo **Tipo de traballo**, seleccione **Ningún**. Por defecto, os campos **Frecuencia diaria** e **Está activo** están definidas en **Si**.
4. Seleccione **Executar fluxo de traballo**. Na caixa de diálogo **Buscar rexistro**, verá tres fluxos de traballo:

- ProcessRunCaller
- ProcessRunner
- UpdateRoleUtilization

5. Seleccione **ProcessRunCaller** e, a seguir, seleccione **Engadir**.
6. Na caixa de diálogo seguinte, seleccione **Aceptar**. Un fluxo de traballo **Suspensión** vai seguido por fluxo de traballo **Proceso**. 

> [!NOTE]
> Tamén pode seleccionar **ProcessRunner** no paso 5. Entón, cando seleccione **Aceptar**, o fluxo de traballo **Proceso** vai seguido por un fluxo de traballo **Suspensión**.

Os fluxos de traballo **ProcessRunCaller** e **ProcessRunner** crean facturas. **ProcessRunCaller** chama a **ProcessRunner**. **ProcessRunner** é o fluxo de traballo que realmente crea as facturas. O fluxo de traballo percorre todas as liñas de contrato nas que deben crearse as facturas e crea facturas para esas liñas. Para determinar as liñas de contrato para as que deben crearse as facturas, o traballo analiza as datas de execución de facturas para as liñas de contrato. Se as liñas de contrato que pertencen a un contrato teñen a mesma data de execución de facturas, as transaccións combínanse nunha factura que ten dúas liñas de factura. Se non hai transaccións para as que crear facturas, o traballo omite a creación dunha factura.

Despois de que **ProcessRunner** remate a execución, chama a **ProcessRunCaller**, fornece a hora de finalización e péchase. A seguir, **ProcessRunCaller** inicia un temporizador que se executa durante 24 horas desde a hora de finalización especificada. Ao final do temporizador, **ProcessRunCaller** péchase.

O traballo de proceso por lotes para crear facturas é un traballo recorrente. Se este proceso de lotes se executa moitas veces, créanse varias instancias do traballo e causa erros. Polo tanto, debe iniciar o proceso por lotes unha soa vez e logo reinícieo só se deixa de executarse.

> [!NOTE]
> A facturación por lotes en Project Operations só se executa para as liñas de contrato do proxecto que están configuradas por programacións de facturas. Unha liña de contrato cun método de facturación de prezos fixos debe ter configurados os fitos. Unha liña de contrato de proxecto cun método de facturación de tempo e material necesitará unha programación de facturas baseado na data configurada.
