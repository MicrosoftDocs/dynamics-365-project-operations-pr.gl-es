---
title: Recuperación do IVE na xestión de gastos
description: Este tema explica como recibir reembolsos das transaccións elixibles do imposto sobre o valor engadido (IVE).
author: suvaidya
ms.date: 10/10/2020
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 64e9f4091fdf40cc702e83a165fe0a5be5043359348210bbe4afcd8a18055133
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6999359"
---
# <a name="vat-recovery-in-expense-management"></a>Recuperación do IVE na xestión de gastos

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Para recibir reembolsos por transaccións do imposto sobre o valor engadido (IVE) elixibles, unha empresa ou organización debe identificar, recoller, verificar e enviar información precisa. Este proceso inclúe varias tarefas e, dependendo do tamaño da súa empresa, pode incluír varios empregados ou funcións.

Para recuperar o IVE no módulo **Xestión de gastos**, deben cumprirse os seguintes requisitos previos:

- Débense crear códigos fiscais para os países/rexións que están asignados a categorías de gasto.
- Debe crearse un grupo fiscal de vendas para cada código fiscal.
- Debe crearse un código fiscal de vendas para cada grupo fiscal de vendas.

Unha vez cumpridos os requisitos previos, débense completar os seguintes pasos para solicitar o reembolso das transaccións do IVE.

1. Nun informe de gastos, introduza información fiscal sobre as transaccións con tarxeta de crédito para identificar os reembolsos do IVE elixibles.
2. Verifique que toda a información fiscal estea completa e logo contabilice o informe de gastos.
3. Procese os gastos elixibles para a recuperación do IVE internacional.
4. Envíe os datos de recuperación do IVE a un fornecedor externo para presentar declaracións de recuperación internacionais.
5. Procese os gastos para a recuperación do IVE nacional.

As seguintes seccións fornecen exemplos que mostran como os empregados de Contoso completan cada paso.

## <a name="enter-tax-information-about-credit-card-transactions-to-identify-eligible-vat-refunds"></a>Introduza información fiscal sobre as transaccións con tarxeta de crédito para identificar os reembolsos do IVE elixibles.

Nancy, unha representante de vendas de Contoso que reside nos Estados Unidos, regresou recentemente dunha viaxe de vendas ao Reino Unido. Durante a viaxe, Nancy realizou algúns gastos coa tarxeta de crédito persoal para as comidas. Nancy debe agora crear un informe de gastos para conciliar os gastos.

Cando Nancy introduce información no informe de gastos, selecciona **Reino Unido** no campo **País/rexión** da páxina **Editar informe de gastos**. A lista de grupos fiscais de vendas fíltrase de xeito que só amosa os grupos que se aplican ao Reino Unido. Nancy selecciona o grupo fiscal de vendas **Reino Unido 001** e despois selecciona o grupo fiscal de vendas específico **Comidas**. A seguir, Nancy engade unha nova transacción para aloxamento. Debido a que só hai un grupo fiscal de vendas e un grupo fiscal de vendas específico para aloxamento no Reino Unido, esta información énchese automaticamente no informe de gastos de Nancy.

Segundo a política de Contoso, todos os gastos deben ter un recibo coincidente. Polo tanto, cando Nancy garda o informe de gastos, recibe unha mensaxe na que se indica que debe anexar un recibo de cada transacción que figura no seu informe de gastos. Nancy verifica que anexou unha imaxe dixital de cada recibo de transacción ao seu informe de gastos e despois envía o seu informe para a súa aprobación. Despois envía os recibos en papel ao equipo de procesamento de back-office. Este equipo enviará os datos de recuperación do IVE ao terceiro fornecedor que presente as declaracións internacionais de recuperación do IVE para Contoso.

## <a name="verify-tax-information-and-post-an-expense-report"></a>Verificar a información fiscal e contabilizar un informe de gastos

Antes de que April, a coordinadora de contas pendentes de pago de Contoso, poida contabilizar un informe de gastos, debe introducir calquera información fiscal que falte nel. Ela abre a páxina **Detalles do informe de gastos** e ve o informe de gastos aprobado de Nancy. April abre o informe de gastos para ver os detalles das transaccións. Ve que Nancy non ingresou un grupo fiscal de vendas específico dunha das transaccións. Debido a que non se proporciona esta información, April non pode contabilizar o informe de gastos. Por iso, mira na páxina **Configuracións fiscais** en xestión de gastos e atopa o grupo fiscal de vendas específico adecuado para o país/rexión e o tipo de transacción. April xa pode contabilizar o informe de gastos no libro maior.

Cando April contabiliza o informe de gastos, créase un elemento de traballo con IVE recuperable. Este elemento de traballo atribúese a un membro do equipo de procesamento de back-office. April recibe unha mensaxe que confirma que a contabilización foi correcta. Esta mensaxe tamén recolle o número de transaccións con IVE identificadas para a súa recuperación.

## <a name="process-expenses-that-are-eligible-for-international-vat-recovery"></a>Procesar os gastos elixibles para a recuperación do IVE internacional

Arnie, membro do equipo de procesamento administrativo de Contoso é o responsable de verificar que toda a información requirida para a recuperación do IVE está incluída nos informes de gastos. El abre a páxina **Recuperación de impostos de gastos** e selecciona o informe de gastos que presentou Nancy. Arnie verifica entón que se anexan todos os recibos requiridos e que se introduciron os códigos fiscais de vendas específicos correctos.

Cando Arnie recibe os recibos en papel de Nancy, compróbaos contra os recibos dixitais e despois cambia o estado do informe de gastos a **Listo para a recuperación**.

## <a name="send-vat-recovery-data-to-the-third-party-vendor"></a>Enviar datos de recuperación do IVE ao fornecedor externo

Cando Arnie estea listo para enviar os datos do informe de gastos ao fornecedor externo que presentará as declaracións de recuperación do IVE, abre a páxina **Recuperación de impostos de gastos**. Filtra a páxina de xeito que só amosa os informes de gastos marcados como **Listo para a recuperación**. Arnie selecciona entón **Ficheiro** &gt; **Exportar a Excel**. A información do IVE dos informes de gastos exportase a folla de cálculo de Microsoft Excel. Arnie envía esta folla de traballo ao fornecedor externo e inclúe unha mensaxe que indica que os recibos en papel foron enviados por mensaxería.

## <a name="process-expenses-for-domestic-vat-recovery"></a>Procesar os gastos para a recuperación do IVE nacional

Arnie debe verificar que as transaccións do informe de gastos son aptas para a recuperación do IVE e que os recibos dixitais están anexados aos informes. Para comezar a tramitar os gastos elixibles para a recuperación nacional, Arnie abre a páxina **Recuperación de impostos de gastos** e selecciona o informe de gastos que require a verificación. Verifica que os recibos están a nome da empresa en lugar do empregado. (Para a recuperación de IVE, os recibos debe estar a nome da empresa). Arnie verifica entón que se anexan todos os recibos requiridos e que se introduciron os códigos fiscais de vendas específicos correctos.

Cando Arnie recibe os recibos en papel, cambia o estado do informe de gastos a **Listo para a recuperación**. Despois pode presentar a declaración ante a autoridade fiscal competente. Neste caso, a autoridade fiscal apropiada nos Estados Unidos é o Internal Revenue Service (IRS).


[!INCLUDE[footer-include](../includes/footer-banner.md)]