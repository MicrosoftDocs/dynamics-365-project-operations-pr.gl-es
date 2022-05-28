---
title: Procesamento de recibos de gastos
description: Este tema ofrece información sobre o procesamento de recoñecemento óptico de caracteres (OCR) para recibos. Esta función está deseñada para mellorar a experiencia do usuario cando se crean informes de gastos Microsoft Dynamics 365 Finanzas.
author: stsporen
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 067432106742447d2b8fa215ec05bf05f4b41e70
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 05/04/2022
ms.locfileid: "8684318"
---
# <a name="expense-receipt-processing"></a>Procesamento de recibos de gastos

A entrada de gastos mellorouse mediante a introdución do procesamento de recoñecemento óptico de caracteres (OCR) para recibos. Esta funcionalidade está deseñada para mellorar a experiencia do usuario ao crear informes de gastos.

## <a name="key-features"></a>Funcionalidades clave

- O nome do comerciante, a data e o importe total extráense dos recibos.
- A funcionalidade tenta emparellar os recibos non anexados coas transaccións de gastos non anexadas.
- Os usuarios poden crear transaccións de gastos introducidas manualmente a partir de recibos.

## <a name="usage-examples"></a>Exemplos de uso

Para anexar automaticamente recibos que inclúan transaccións con tarxeta de crédito cando se crea un informe de gastos, faga o seguinte:

  1. Abra a área de traballo **Xestión de gastos**.
  2. No separador **Recibos**, comprobe que existen recibos non anexados. Tamén pode cargar recibos no separador **Recibos**.
  3. No separador **Gastos**, comprobe que existen gastos non anexados. Normalmente, o administrador de gastos importa estes gastos do provedor da tarxeta de crédito.
  4. Seleccione **Novo informe de gastos**. Teña en conta que agora tamén pode incluír gastos e recibos tamén cando crea un informe de gastos. Se engade tanto gastos como recibos, activarase a correspondencia automática dos recibos cos gastos.

Para crear un gasto ou emparellar un gasto desde un recibo, faga o seguinte:

  1. Nun informe de gastos, no separador **Recibos**, anexe un recibo seleccionando **Engadir recibos**.
  2. Debaixo da imaxe cargada do recibo, observe as opcións **Crear** e **Emparellar**.

      - Seleccione **Crear** para crear unha transacción de gastos introducida manualmente e encher os valores que se extraen do recibo.
      - Se selecciona **Emparellar**, o sistema tenta emparellar un gasto existente co recibo.

## <a name="installation"></a>Instalación

Esta funcionalidade funciona en combinación coa funcionalidade **Reinvención dos informes de gastos** para axudar a simplificar a experiencia dos gastos. Esta función só está dispoñible para ambientes de nivel 2+, que son Illamento de procesos e Produción.

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

Para obter máis información sobre a funcionalidade de reinvención dos informes de gastos, consulte [Reinvención dos informes de gastos](ExpenseWorkspaceNew.md).

## <a name="frequently-asked-questions"></a>Preguntas máis frecuentes

**Usa Microsoft os meus datos para os seus modelos?**

Non, Microsoft creou un modelo xeral de aprendizaxe automático para o seu servizo de procesamento de recibos. Este modelo non está baseado nos recibos que vostede cargue.

**Onde está dispoñible e se procesa esta funcionalidade?**

Actualmente, está dispoñible nos Estados Unidos.

**Onde van os meus recibos?**

Finanzas contactará con Cognitive Services para extraer os datos do campo. Cognitive Services conservará unha copia do seu recibo ata 24 horas mentres se produce o procesamento. Unha vez finalizado o procesamento, Cognitive Services eliminará o recibo. Os recibos aínda se gardan en Finanzas.

Para obter máis información, consulte [Activar a comprensión de recibos coa nova capacidade de recoñecemento de formularios](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).


[!INCLUDE[footer-include](../includes/footer-banner.md)]