---
title: Capturar un recibo usando OCR
description: Este artigo ofrece información sobre o proceso de recoñecemento óptico de caracteres (OCR) para recibos.
author: suvaidya
ms.date: 11/10/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: ee16a43fa544af793676072f304d732359d3d9ec
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917804"
---
# <a name="capture-a-receipt-using-ocr"></a>Capturar un recibo usando OCR

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

Para usar estas capacidades de gastos avanzadas, instale o complemento do servizo de xestión de gastos para Microsoft Dynamics 365 Finance e activa as funcións na túa instancia. Pode acceder ao complemento desde o seu proxecto en Microsoft Dynamics Lifecycle Services (LCS).

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

A dispoñibilidade desta función en diferentes rexións está listada na seguinte táboa. Se a túa rexión non é compatible actualmente, envía unha solicitude para priorizar a dispoñibilidade do servizo OCR na túa rexión. 

| Rexión | Compatible                         |
|--------|-----------------------------------|
| EUA    | Si                               |
| CAN    | Si                               |
| Reino Unido     | Si                               |
| AUS    | Si                               |
| UE     | Parcialmente. Só recibos en inglés. |
| Asia   | No                                |
| O Xapón  | No                                |
| África | No                                |

**Onde van os meus recibos?**

Finanzas contactará con Cognitive Services para extraer os datos do campo. Cognitive Services conservará unha copia do seu recibo ata 24 horas mentres se produce o procesamento. Unha vez finalizado o procesamento, Cognitive Services eliminará o recibo. Os recibos aínda se gardan en Finanzas.

Para obter máis información, consulte [Activar a comprensión de recibos coa nova capacidade de recoñecemento de formularios](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
