---
title: Emparellar un recibo cun gasto mediante OCR
description: Este tema ofrece información sobre o procesamento de recoñecemento óptico de caracteres (OCR) para recibos.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 02c1bafbe907a657689b610ae792f88085320903
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896999"
---
# <a name="match-a-receipt-to-an-expense-using-ocr"></a>Emparellar un recibo cun gasto mediante OCR

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

A entrada de gastos mellorouse mediante a introdución do procesamento de recoñecemento óptico de caracteres (OCR) para recibos. Esta funcionalidade está deseñada para mellorar a experiencia do usuario ao crear informes de gastos.

## <a name="key-features"></a>Funcionalidades clave

- O sistema extrae o nome do comerciante, a data e o importe total dos recibos.
- O sistema tentará emparellar os recibos non anexados coas transaccións de gastos non anexadas.
- Pode crear transaccións de gastos introducidas manualmente a partir de recibos.

## <a name="attach-receipts-to-an-expense-report"></a>Anexar recibos a un informe de gastos

Para anexar automaticamente recibos que inclúan transaccións con tarxeta de crédito cando se crea un informe de gastos, complete os seguintes pasos.

  1. Abra a área de traballo **Xestión de gastos**.
  2. No separador **Recibos**, comprobe que existen recibos non anexados. Tamén pode cargar recibos no separador **Recibos**.
  3. No separador **Gastos**, comprobe que existen gastos non anexados. Normalmente, o administrador de gastos importa estes gastos do provedor da tarxeta de crédito.
  4. Seleccione **Novo informe de gastos**. Teña en conta que agora tamén pode incluír gastos e recibos tamén cando crea un informe de gastos. Se engade tanto gastos como recibos, activarase a correspondencia automática dos recibos cos gastos.

## <a name="create-or-match-receipts-to-an-expense-report"></a>Crear ou emparellar recibos cun informe de gastos
Para crear un gasto ou emparellar un gasto desde un recibo, complete os seguintes pasos.

  1. Nun informe de gastos, no separador **Recibos**, anexe un recibo seleccionando **Engadir recibos**.
  2. Debaixo da imaxe cargada do recibo, observe as opcións **Crear** e **Emparellar**.

      - Seleccione **Crear** para crear unha transacción de gastos introducida manualmente e encher os valores que se extraen do recibo.
      - Se selecciona **Emparellar**, o sistema tenta emparellar un gasto existente co recibo.

## <a name="installation"></a>Instalación

Para utilizar estas capacidades avanzadas de gastos, instale o complemento Servizo de xestión de gastos para Microsoft Dynamics 365 Finance e active as funcionalidades na súa instancia. Pode acceder ao complemento desde o seu proxecto en Microsoft Dynamics Lifecycle Services (LCS).

1. Inicie sesión en LCS e abra o ambiente desexado.
2. Vaia a **Detalles completos**.
3. Seleccione **Manter** ou desprácese ata o separador rápido **Complementos de ambiente**.
4. Seleccione **Instala un novo complemento**.
5. Seleccione **Servizo de xestión de gastos**.
6. Siga a guía de instalación e acepte os termos e condicións.
7. Seleccionar **Instalar**.

Na área de traballo **Xestión de funcionalidades**, active as seguintes funcionalidades:

- Os informes de gastos reinventáronse
- Emparellar automaticamente e crear gastos a partir do recibo

Ao activar estas funcionalidades, prodúcense as seguintes accións:

- A área de traballo **Xestión de gastos** existente substitúese pola nova área de traballo.
- Engádese un novo elemento de menú para a visibilidade do campo de gastos.
- Aínda pode abrir a páxina **Informes de gastos** anterior indo a **Xestión de gastos > Os meus gastos > Informes de gastos**.
- Os fluxos de traballo e as aprobacións aínda o levarán á páxina de informes de gastos existente.
- Os recibos procesaranse mediante Microsoft Azure Cognitive Services e os metadatos extraeranse e engadiranse.
- Engádese unha opción que lle permite crear un informe de gastos que inclúe recibos non anexados emparellados.
- Unha opción que se engade aos informes de gastos permítelle crear unha liña de gasto a partir dun recibo ou tentar emparellar un recibo existente cunha liña de gasto existente.

## <a name="frequently-asked-questions"></a>Preguntas máis frecuentes

**Usa Microsoft os meus datos para os seus modelos?**

Non, Microsoft creou un modelo xeral de aprendizaxe automático para o seu servizo de procesamento de recibos. Este modelo non está baseado nos recibos que vostede cargue.

**Onde está dispoñible e se procesa esta funcionalidade?**

Actualmente, está dispoñible nos Estados Unidos.

**Onde van os meus recibos?**

Finanzas contactará con Cognitive Services para extraer os datos do campo. Cognitive Services conservará unha copia do seu recibo ata 24 horas mentres se produce o procesamento. Unha vez finalizado o procesamento, Cognitive Services eliminará o recibo. Os recibos aínda se gardan en Finanzas.

Para obter máis información, consulte [Activar a comprensión de recibos coa nova capacidade de recoñecemento de formularios](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).
