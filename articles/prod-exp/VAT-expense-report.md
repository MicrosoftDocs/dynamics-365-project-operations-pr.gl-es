---
title: Recuperación do IVE
description: Este tema explica como recuperar reembolsos das transaccións elixibles do imposto sobre o valor engadido (IVE).
author: saraschi2
ms.date: 02/26/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 76706fd8ced58063b05bc8ebe4b25c1dddbf0890e72e9c7194d17ff2937dc8ca
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986039"
---
# <a name="vat-recovery"></a>Recuperación do IVE 

Para recibir reembolsos por transaccións do imposto sobre o valor engadido (IVE) elixibles, unha empresa ou organización debe identificar, recoller, verificar e enviar información precisa. Este proceso inclúe varias tarefas e, dependendo do tamaño da súa empresa, pode incluír varios empregados ou funcións.

Para recuperar o IVE utilizando Xestión de gastos, deben cumprirse os seguintes requisitos previos:

- Débense crear códigos fiscais para os países/rexións que están asignados a categorías de gasto.
- Debe crearse un grupo fiscal de vendas para cada código fiscal.
- Debe crearse un código fiscal de vendas para cada grupo fiscal de vendas.

Unha vez cumpridos os requisitos previos, os empregados seguen estes pasos para solicitar o reembolso das transaccións do IVE.

1. Nun informe de gastos, introduza información fiscal sobre as transaccións con tarxeta de crédito para identificar os reembolsos do IVE elixibles.
2. Asegúrese de que toda a información fiscal estea completa e logo contabilice o informe de gastos.
3. Procese os gastos elixibles para a recuperación do IVE internacional.
4. Envíe os datos de recuperación do IVE a un fornecedor externo para presentar declaracións de recuperación internacionais.
5. Procese os gastos para a recuperación do IVE nacional.

As seguintes seccións fornecen exemplos que mostran como os empregados de Contoso completan cada paso.

## <a name="on-an-expense-report-enter-tax-information-about-credit-card-transactions-to-identify-eligible-vat-refunds"></a>Nun informe de gastos, introduza información fiscal sobre as transaccións con tarxeta de crédito para identificar os reembolsos do IVE elixibles

Nancy, unha representante de vendas de Contoso que reside nos Estados Unidos, regresou recentemente dunha viaxe de vendas ao Reino Unido. Durante a súa viaxe, realizou algúns gastos coa tarxeta de crédito persoal para as comidas. Nancy debe agora crear un informe de gastos para conciliar os seus gastos.

Cando Nancy introduce información no seu informe de gastos, selecciona **Reino Unido** no campo **País/rexión** da páxina **Editar informe de gastos**. A lista de grupos fiscais de vendas fíltrase de xeito que só amosa os grupos que se aplican ao Reino Unido. Nancy selecciona o grupo fiscal de vendas **Reino Unido 001** e despois selecciona o grupo fiscal de vendas específico **Comidas**. A seguir, engade unha nova transacción para o seu aloxamento. Debido a que só hai un grupo fiscal de vendas e un grupo fiscal de vendas específico para aloxamento no Reino Unido, esta información énchese automaticamente no informe de gastos de Nancy.

Segundo a política de Contoso, todos os gastos deben ter un recibo coincidente. Polo tanto, cando Nancy garda o seu informe de gastos, recibe unha mensaxe na que se indica que debe anexar un recibo de cada transacción que figura no seu informe de gastos. Nancy verifica que anexou unha imaxe dixital de cada recibo de transacción ao seu informe de gastos e despois envía o seu informe para a súa aprobación. Despois envía os recibos en papel ao equipo de procesamento de back-office. Este equipo enviará os datos de recuperación do IVE ao terceiro fornecedor que presente as declaracións internacionais de recuperación do IVE para Contoso.

## <a name="make-sure-that-all-tax-information-is-complete-and-then-post-the-expense-report"></a>Asegúrese de que toda a información fiscal estea completa e logo contabilice o informe de gastos

April, a coordinadora de contas pendentes de pago de Contoso, debe introducir calquera información fiscal que falte nun informe de gastos antes de que poida contabilizarse. Ela abre a páxina **Detalles do informe de gastos** e ve o informe de gastos aprobado de Nancy. April abre o informe de gastos para ver os detalles das transaccións. Ve que Nancy non ingresou un grupo fiscal de vendas específico dunha das transaccións. Debido a que non se proporciona esta información, April non pode contabilizar o informe de gastos. Por iso, April mira na páxina **Configuracións fiscais** en xestión de gastos e atopa o grupo fiscal de vendas específico adecuado para o país/rexión e o tipo de transacción. April xa pode contabilizar o informe de gastos no libro maior.

Cando April contabiliza o informe de gastos, créase un elemento de traballo con IVE recuperable. Este elemento de traballo atribúese a un membro do equipo de procesamento de back-office. April recibe unha mensaxe que confirma que a contabilización foi correcta. Esta mensaxe tamén recolle o número de transaccións con IVE identificadas para a súa recuperación.

## <a name="process-expenses-that-are-eligible-for-international-vat-recovery"></a>Procesar os gastos elixibles para a recuperación do IVE internacional

Arnie, membro do equipo de procesamento administrativo de Contoso é o responsable de confirmar que toda a información requirida para a recuperación do IVE está incluída nos informes de gastos. El abre a páxina **Recuperación de impostos de gastos** e selecciona o informe de gastos que presentou Nancy. Arnie verifica que se anexan todos os recibos requiridos e que se introduciron os códigos fiscais de vendas específicos correctos.

Cando Arnie recibe os recibos en papel de Nancy, verifica os recibos en papel contra os recibos dixitais e despois cambia o estado do informe de gastos a **Listo para a recuperación**.

## <a name="send-vat-recovery-data-to-the-third-party-vendor-to-file-international-recovery-returns"></a>Envíe os datos de recuperación do IVE a un fornecedor externo para presentar declaracións de recuperación internacionais

Cando Arnie estea listo para enviar os datos do informe de gastos ao fornecedor externo que presentará as declaracións de recuperación do IVE, abre a páxina **Recuperación de impostos de gastos**. Filtra a páxina de xeito que só amosa os informes de gastos marcados como **Listo para a recuperación**. Arnie selecciona entón **Ficheiro** &gt; **Exportar a Excel**. A información do IVE dos informes de gastos exportase a folla de cálculo de Microsoft Excel. Arnie envía esta folla de traballo ao fornecedor externo e inclúe unha mensaxe que indica que os recibos en papel foron enviados por mensaxería.

## <a name="process-expenses-for-domestic-vat-recovery"></a>Procesar os gastos para a recuperación do IVE nacional

Arnie debe verificar que as transaccións do informe de gastos son aptas para a recuperación do IVE e que os recibos dixitais están anexados aos informes. Para comezar a tramitar os gastos elixibles para a recuperación nacional, Arnie abre a páxina **Recuperación de impostos de gastos** e selecciona o informe de gastos que require a verificación. Verifica que os recibos están a nome da empresa en lugar do empregado. Para a recuperación do IVE, os recibos deben estar a nome da empresa. Arnie entón confirma que se aplicaron os códigos fiscais correctos do imposto sobre as vendas e do grupo.

Cando Arnie recibe os recibos en papel, cambia o estado do informe de gastos a **Listo para a recuperación**. Despois pode presentar a declaración ante a autoridade fiscal competente. Neste caso, a autoridade fiscal apropiada nos Estados Unidos é o Internal Revenue Service (IRS).


[!INCLUDE[footer-include](../includes/footer-banner.md)]