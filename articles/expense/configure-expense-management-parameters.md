---
title: Configurar os parámetros de xestión de gastos
description: Este tema describe os parámetros que controlan o comportamento xeral na xestión de gastos.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 8ecbd0abc16d0a29eea47d6bd1653a204a83de4c
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076014"
---
# <a name="configure-expense-management-parameters"></a>Configurar os parámetros de xestión de gastos

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Este tema describe os parámetros que controlan o comportamento xeral na xestión de gastos.

## <a name="general"></a>Xeral

| Campo                                                    | Descripción |
|----------------------------------------------------------|-------------|
| Taxa estándar de quilometraxe                                 | Introduza a taxa de reembolso dos gastos de quilometraxe. Esta taxa multiplícase pola quilometraxe que se introduce para o gasto para calcular o importe que se reembolsa polo gasto de viaxe. |
| Validar motivo do gasto                                 | Active esta opción para limitar os usuarios a un conxunto de valores existente configurado no campo **Informe de motivo do gasto** cando crean informes de gastos. |
| Gastos persoais pagados por                                | Seleccione quen é o responsable de pagar os importes das transaccións con tarxeta de crédito que se categorizan como persoais. |
| Mostrar o informe de gastos completo en retorno               | Seleccione esta opción para amosar todos os gastos dun informe de gastos cando se visualicen os detalles do documento orixinal para un vale específico que se xerou cando se contabilizou o informe de gastos. |
| A autorización previa da viaxe é obrigatoria                 | Seleccione esta opción para requirir que se envíe e aprobe unha solicitude de viaxe antes de que un empregado poida presentar un informe de gastos. |
| Permitir a edición de distribucións antes da contabilización            | Seleccione se se poden editar as distribucións dun informe de gastos antes de que se contabilice. |
| Avaliar as políticas de xestión de gastos                     | Seleccione cando se avalían os gastos para determinar se se incumpriu unha política de gastos. Os gastos pódense avaliar por infraccións cando se introduce e garda a entrada de gastos ou cando se envía para a aprobación. As regras da política para os recibos que se requiren avaliaranse cando se garde a liña de gasto. |
| Permitir liñas de gasto entre empresas                         | Seleccione se os gastos doutras entidades legais poden introducirse nun informe de gastos. |
| Permite editar a taxa de cambio dos gastos da tarxeta de crédito | Seleccione esta opción para permitir ao usuario editar a taxa de cambio dos gastos de tarxeta de crédito importados. |
| Campos de xerarquía de varios niveis para amosar                  | Seleccione os campos do responsable de aprobacións que se amosan cando o tipo de atribución de fluxo de traballo estea configurado como xerarquía e a selección **Xerarquía** estea configurada para usar a xerarquía de aprobación, aprobación de varios niveis de gastos. Cando se usa a xerarquía de aprobación de varios niveis para un fluxo de traballo, os campos seleccionados amosaranse no informe de gastos e poden editarse. |
| Introducir o número da tarxeta de crédito do empregado                        | Seleccione se se pode introducir e gardar un número de 15 ou 16 caracteres no campo **ID da tarxeta** da páxina **Tarxetas de crédito** para un empregado. |
| Validar o motivo da solicitude de viaxe                      | Active esta opción para limitar os usuarios a un conxunto de valores existente configurado no campo **Informe de motivo do gasto** cando crean solicitudes de viaxe. |

## <a name="financial"></a>Actividades financeiras

| Campo                                                                                    | Descripción |
|------------------------------------------------------------------------------------------|-------------|
| Nome do diario de libro maior                                                                | Seleccione o nome do diario de libro maior no que se contabilizan os informes de gastos aprobados. |
| Permitir a recuperación de impostos dos gastos                                                        | Seleccione esta opción para permitir a recuperación do imposto de gastos para gastos que reúnan os requisitos. Esta opción non se pode seleccionar se están activadas as regras do imposto sobre as vendas e o uso. |
| Contabilizar adiantos de efectivo de inmediato                                                           | Seleccione esta opción para contabilizar un adianto de efectivo aprobado cando remate o proceso de pagamento e transferencia. Se non se selecciona esta opción, o proceso de pagamento e transferencia xera un diario xeral non contabilizado. |
| Data contable correcta durante a contabilización                                                   | Seleccione esta opción para actualizar a data contable cando se contabilizan os gastos, se o período actual está en espera ou pechado. A data contable establecerase no seguinte período aberto. |
| Permitir agrupar transaccións en función da conta compensada especificada no método de pago       | Seleccione esta opción para resumir as transaccións de gastos dun informe de gastos, en función da conta compensada especificada no método de pagamento dos gastos. |
| Imposto incluído                                                                             | Seleccione esta opción para incluír o imposto de vendas no importe do gasto por defecto. |
| Liberar gravames ao pechar as solicitudes de viaxe                                      | Seleccione esta opción para liberar fondos gravados cando se peche unha solicitude de viaxe aprobada. |
| Permitir que a solicitude de viaxe se envíe por exceso de orzamento para o rexistro de orzamento e o orzamento do proxecto | Seleccione esta opción para permitir aos empregados enviar solicitudes de viaxe para a súa aprobación, aínda que superen o orzamento permitido establecido no rexistro de orzamento ou o orzamento permitido para un proxecto. |
| Permitir que o informe de gasto se envíe por exceso de orzamento para o rexistro de orzamento e o orzamento do proxecto     | Seleccione esta opción para permitir aos empregados enviar informes de gastos para a súa aprobación, aínda que superen o orzamento permitido establecido no rexistro de orzamento ou o orzamento permitido para un proxecto. |
| Permitir a aprobación do informe de gasto por exceso de orzamento só para o rexistro de orzamento                 | Seleccione esta opción para permitir aos responsables de aprobacións aprobar informes de gastos que superen o orzamento permitido establecido no rexistro de orzamento. |

## <a name="per-diem"></a>Dietas

| Campo                                 | Descripción |
|---------------------------------------|-------------|
| Horas mínimas para dietas            | Introduza o número mínimo de horas predeterminado que un empregado debe traballar nun día para poder optar a unha dieta por gastos de viaxe. Este valor úsase como valor predeterminado só para o campo **Horas mínimas** para os niveis de taxa de dieta. |
| Porcentaxe de comida                          | Introduza a porcentaxe predeterminada da dieta para as comidas que se usa nos primeiros e últimos días do gasto relacionado coa viaxe cando o campo **Calcular a redución de comidas por** está configurado en **Tipo de comida ao día** ou **Número de comidas ao día**. A xornada laboral do primeiro e último día pode ser máis curta que unha xornada normal. Polo tanto, a cantidade da dieta neses días pode diferir da cantidade estándar. Se a porcentaxe está establecida en **0** (cero), as deducións para o primeiro e último día serán de 0,00. |
| Porcentaxe de hotel                         | Introduza a porcentaxe predeterminada da dieta para hoteis que se usa nos primeiros e últimos días do gasto relacionado coa viaxe. A xornada laboral do primeiro e último día pode ser máis curta que unha xornada normal. Polo tanto, a cantidade da dieta neses días pode diferir da cantidade estándar. Se a porcentaxe está establecida en **0** (cero), as deducións para o primeiro e último día serán de 0,00. |
| Outra porcentaxe                         | Introduza a porcentaxe predeterminada da dieta para gastos variados nos primeiros e últimos días do gasto relacionado coa viaxe. A xornada laboral do primeiro e último día pode ser máis curta que unha xornada normal. Polo tanto, a cantidade da dieta neses días pode diferir da cantidade estándar. Se a porcentaxe está establecida en **0** (cero), as deducións para o primeiro e último día serán de 0,00. |
| Redución da porcentaxe para almorzo | Introduza a cantidade na que se reduce a dieta para o almorzo. Por exemplo, se un empregado recibe un almorzo de cortesía, é posible que queira reducir o importe da dieta nun 10 por cento. |
| Redución da porcentaxe para a comida     | Introduza a cantidade na que se reduce a dieta para a comida. Por exemplo, se un empregado recibe unha comida de cortesía, é posible que queira reducir o importe da dieta nun 15 por cento. |
| Redución da porcentaxe para a cea    | Introduza a cantidade na que se reduce a dieta para a cea. Por exemplo, se un empregado recibe unha cea de cortesía, é posible que queira reducir o importe da dieta nun 25 por cento. |
| Calcular a redución da comida por           | Especifique como o sistema debe calcular a redución da comida por día seleccionando se a redución se basea no tipo de comida por viaxe ou por día ou se se basea no número de comidas permitidas ao día. |
| Redondeo da dieta                     | Seleccione o tipo de redondeo que se usa para os gastos da dieta. Se selecciona o redondeo normal, calquera gasto de dieta que teña un importe de 0,50 redondearase ata 1,00 e calquera gasto diario que teña un importe inferior a 0,50 redondearase ata 0,00. |
| Cálculo da dieta base en          | Seleccione se unha cantidade da dieta se basea nun día natural ou nun período de 24 horas. |

## <a name="fax-cover-pages"></a>Páxinas de portada de fax

| Campo                          | Descripción |
|--------------------------------|-------------|
| Instrucións                   | Introduza as instrucións que os empregados deben seguir cando crean unha portada para un fax que se usa para enviar recibos relacionados cun informe de gastos. Para inserir texto específico do idioma que se mostrará, en función do idioma do usuario, seleccione **Traducións**. |
| ID de usuario (información de código de barras) | Seleccione esta opción para almacenar o identificador único dun empregado no código de barras que se usa na portada do fax. |
| Código de barras                       | Seleccione o código de barras que se usa na portada do fax. Na xestión de gastos admítense os códigos de barras 39 e 128. |

## <a name="anti-corruption"></a>Anticorrupción

| Campo                                 | Descripción |
|---------------------------------------|-------------|
| Mostrar un certificado anticorrupción   | Seleccione esta opción para amosar o texto anticorrupción cando se crea un informe de gastos. Pódense habilitar categorías de gastos específicas que requirirán que se seleccione o certificado anticorrupción no informe de gastos. Por exemplo, unha categoría de agasallo relacionada cun gasto oficial do goberno pode requirir que o empregado confirme que o gasto cumpre coa política da empresa relacionada cos funcionarios do goberno. |
| Mensaxe anticorrupción para o remitente | Introduza o texto que se debe mostrar a un empregado que está a crear un informe de gastos. Para inserir texto específico do idioma que se mostrará, en función do idioma do usuario, seleccione **Traducións**. |
| Mensaxe anticorrupción para o responsable de aprobacións  | Introduza o texto que se debe mostrar ao responsable de aprobacións cando se crea un informe de gastos. Para inserir texto específico do idioma que se mostrará, en función do idioma do usuario, seleccione **Traducións**. |
