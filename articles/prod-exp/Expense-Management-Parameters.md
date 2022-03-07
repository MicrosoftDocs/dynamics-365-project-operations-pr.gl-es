---
title: Parámetros de xestión de gastos
description: Os seguintes parámetros controlan o comportamento na xestión de gastos.
author: KimANelson
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 2ef48f844656ff5197ae1731fb3f9bdf91a1a906b16f35bb2124469743a9e954
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991349"
---
# <a name="expense-management-parameters"></a>Parámetros de xestión de gastos


Os parámetros controlan o comportamento xeral na xestión de gastos.

### <a name="general"></a>Xeral

| **Campo**                                                | **Descripción**                                                 |
|----------------------------------------------------------|---------------------------------------------------------------------|
| **Taxa estándar de quilometraxe**                             | Introduza a taxa de reembolso dos gastos de quilometraxe. A taxa multiplicarase pola quilometraxe introducida no gasto para calcular o importe que se reembolsa polo gasto de viaxe.                       |
|**Gastos persoais pagados por**                             | Seleccione quen é o responsable de pagar os importes das transaccións con tarxeta de crédito categorizadas como persoais.                                                                                                     |
|**Mostrar o informe de gastos completo en retorno**               | Seleccione esta opción para amosar todos os gastos dun informe de gastos cando se visualicen os detalles do documento orixinal para un vale específico que se xerou cando se contabilizou o informe de gastos.              |
|**A autorización previa da viaxe é obrigatoria**                 | Seleccione esta opción para requirir que se envíe e aprobe unha solicitude de viaxe antes de que un empregado poida presentar un informe de gastos.                                                                    |
|**Permitir a edición de distribucións antes da contabilización**            | Seleccione se se poden editar as distribucións dun informe de gastos antes de que se contabilice.                                                                                                                 |
|**Avaliar as políticas de xestión de gastos**                     | Seleccione cando se avalían os gastos para determinar se se incumpriu unha política de gastos. Os gastos pódense comprobar para detectar infraccións cando se introduce e garda a entrada de gastos ou cando se envía para a aprobación. As regras da política para os recibos que se requiren comprobaranse cando se garde a liña de gasto.                   |
|**Permitir liñas de gasto entre empresas**                         | Seleccione se se permite a entrada de gastos doutras entidades legais nun informe de gastos.                                                                                                          |
|**Permite editar a taxa de cambio dos gastos da tarxeta de crédito** | Seleccione esta opción para permitir ao usuario editar a taxa de cambio dos gastos de tarxeta de crédito importados.                                                                        |
|**Campos de xerarquía de varios niveis para amosar**                  | Seleccione os campos do responsable de aprobacións que se amosan cando o tipo de atribución de fluxo de traballo do informe de gastos estea configurado como xerarquía e a selección de xerarquía estea configurada para usar a xerarquía de aprobación de varios niveis de gastos. Cando se usa a xerarquía de aprobación de varios niveis para un fluxo de traballo, os campos seleccionados amosaranse e poderán editarse no informe de gastos. |
|**Introducir o número da tarxeta de crédito do empregado (actualización de xullo de 2017)**     | Seleccione se se pode introducir e gardar un número de 15 ou 16 caracteres no campo **ID da tarxeta** na páxina **Tarxetas de crédito** para un empregado.                                                                          |

### <a name="financial"></a>Actividades financeiras

| **Campo**                                                            | **Descrición**     |
|----------------------------------------------------------------------|------------------------------------|
|**Nome do diario de libro maior**                                         | Seleccione o nome do diario de libro maior no que se contabilizan os informes de gastos aprobados.            |
|**Permitir a recuperación de impostos dos gastos**                                  | Seleccione esta opción para permitir a recuperación do imposto de gastos para gastos que reúnan os requisitos. Esta opción non se pode activar se están activadas as regras do imposto sobre as vendas e o uso.      |
|**Contabilizar adiantos de efectivo de inmediato**                                     | Seleccione esta opción para contabilizar un adianto de efectivo aprobado cando remate o proceso de pagamento e transferencia. Se non se selecciona esta opción, o proceso de pagamento e transferencia xerará un diario xeral non contabilizado. |
|**Data contable correcta durante a contabilización**                             | Seleccione esta opción para actualizar a data contable cando se contabilizan os gastos, se o período actual está en espera ou pechado. A data contable establecerase no seguinte período aberto.   |
|**Permitir agrupar transaccións en función da conta compensada especificada no método de pago**      | Seleccione esta opción para resumir as transaccións de gastos dun informe de gastos, en función da conta compensada especificada no método de pagamento dos gastos.   
|**Imposto incluído**                                                   | Seleccione esta opción para incluír o imposto de vendas no importe do gasto por defecto.             |
|**Liberar gravames ao pechar as solicitudes de viaxe**            | Seleccione esta opción para liberar fondos gravados cando se peche unha solicitude de viaxe aprobada.                                                                                   |
|**Permitir que a solicitude de viaxe se envíe por exceso de orzamento para o rexistro de orzamento e o orzamento do proxecto** | Seleccione esta opción para permitir aos empregados enviar solicitudes de viaxe para a súa aprobación que superen o orzamento permitido establecido no rexistro de orzamento ou o orzamento permitido para un proxecto.            |
|**Permitir que o informe de gasto se envíe por exceso de orzamento para o rexistro de orzamento e o orzamento do proxecto**    | Seleccione esta opción para permitir aos empregados enviar informes de gastos para a súa aprobación que superen o orzamento permitido establecido no rexistro de orzamento ou o orzamento permitido para un proxecto.                |
|**Permitir a aprobación do informe de gasto por exceso de orzamento só para o rexistro de orzamento**                | Seleccione esta opción para permitir aos responsables de aprobacións aprobar informes de gastos que superen o orzamento permitido establecido no rexistro de orzamento.                                                                       |

### <a name="per-diem"></a>Dietas

| **Campo**                             | **Descripción**             |
|---------------------------------------|--------------------------------------------------------------------------------------|
|**Horas mínimas para dietas**           | Introduza o número mínimo de horas predeterminado que un empregado debe traballar nun día para poder optar a unha dieta por gastos de viaxe.  Este valor úsase só como valor predeterminado só para o campo Horas mínimas nos niveis de taxa de dieta.                                                                                      |
|**Porcentaxe de comida**                          | Introduza a porcentaxe predeterminada da dieta para as comidas que se usa nos primeiros e últimos días do gasto relacionado coa viaxe cando o campo **Calcular a redución de comidas por** está configurado en **Tipo de comida ao día** ou **Número de comidas ao día**. A xornada laboral do primeiro e último día pode ser máis curta que unha xornada laboral normal. Polo tanto, a cantidade da dieta nestes días pode diferir da cantidade estándar. Se a porcentaxe está establecida en 0, as deducións para o primeiro e último día serán de 0,00. |
|**Porcentaxe de hotel**                        | Introduza a porcentaxe predeterminada da dieta para hoteis que se usa nos primeiros e últimos días do gasto relacionado coa viaxe. A xornada laboral do primeiro e último día pode ser máis curta que unha xornada laboral normal. Polo tanto, a cantidade da dieta nestes días pode diferir da cantidade estándar. Se a porcentaxe está establecida en 0, as deducións para o primeiro e último día serán de 0,00.                                              |
|**Outra porcentaxe**                        | Introduza a porcentaxe predeterminada da dieta para gastos variados nos primeiros e últimos días do gasto relacionado coa viaxe. A xornada laboral do primeiro e último día pode ser máis curta que unha xornada laboral normal. Polo tanto, a cantidade da dieta nestes días pode diferir da cantidade estándar. Se a porcentaxe está establecida en 0, as deducións para o primeiro e último día serán de 0,00.                                                                                                     |
|**Redución da porcentaxe para almorzo** | Introduza a cantidade na que se reduce a dieta para o almorzo. Por exemplo, se un empregado recibe un almorzo de cortesía, é posible que queira reducir o importe da dieta nun 10 por cento.                               |
|**Redución da porcentaxe para a comida**    | Introduza a cantidade na que se reduce a dieta para a comida. Por exemplo, se un empregado recibe unha comida de cortesía, é posible que queira reducir o importe da dieta nun 15 por cento.                                       |
|**Redución da porcentaxe para a cea**   | Introduza a cantidade na que se reduce a dieta para a cea. Por exemplo, se un empregado recibe unha cea de cortesía, é posible que queira reducir o importe da dieta nun 25 por cento.                                     |
|**Calcular a redución da comida por**         | Seleccione como o sistema debe calcular a redución da comida por día seleccionando se a redución se basea no tipo de comida por viaxe ou por día ou se a redución se basea no número de comidas permitidas ao día.|
|**Redondeo da dieta**                  | Seleccione o tipo de redondeo que se usa para os gastos da dieta. Se selecciona o redondeo normal, calquera gasto de dieta que teña un importe de 0,50 redondearase ata 1,00 e calquera gasto diario que teña un importe inferior a 0,50 redondearase ata 0,00.                                                                                              |
|**Cálculo da dieta base en**         | Seleccione se unha cantidade da dieta se basea nun día natural ou nun período de 24 horas.       |

### <a name="fax-cover-pages"></a>Páxinas de portada de fax

| **Campo**                      | **Descripción**            |
|--------------------------------|-----------------------------------------------------------------------------|
| **Instrucións**                   | Introduza as instrucións que os empregados deben seguir cando crean unha portada para un fax que se usa para enviar recibos relacionados cun informe de gastos. Prema o botón **Traducións** para inserir texto específico do idioma que se mostrará, en función do idioma do usuario. |
|**ID de usuario (información de código de barras)** | Seleccione esta opción para almacenar o identificador único dun empregado no código de barras que se usa na portada do fax.                 |
|**Código de barras**                      | Seleccione o código de barras que se usa na portada do fax. Na xestión de gastos admítense os códigos de barras 39 e 128.               |

### <a name="anti-corruption"></a>Anticorrupción

|                 <strong>Campo</strong>                 |                                                                                                                                                                                            <strong>Descrición</strong>                                                                                                                                                                                             |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  <strong>Mostrar un certificado anticorrupción</strong>  | Seleccione esta opción para amosar o texto anticorrupción cando se crea un novo informe de gastos. Pódense habilitar categorías de gastos específicas que requirirán que se debe seleccionar no certificado anticorrupción no informe de gastos. Por exemplo, unha categoría de agasallo relacionada cun gasto oficial do goberno pode requirir que o empregado confirme que o gasto cumpre coa política da empresa relacionada cos funcionarios do goberno. |
| <strong>Mensaxe anticorrupción para o remitente</strong> |                                                                                             Introduza o texto que se lle mostrará ao empregado ao crear un novo informe de gastos. Prema o botón <strong>Traducións</strong> para inserir texto específico do idioma que se mostrará, en función do idioma do usuario.                                                                                             |
| <strong>Mensaxe anticorrupción para o responsable de aprobacións</strong>  |                                                                                             Introduza o texto que se lle mostrará ao responsable de aprobacións ao crear un novo informe de gastos. Prema o botón <strong>Traducións</strong> para inserir texto específico do idioma que se mostrará, en función do idioma do usuario.                                                                                             |



[!INCLUDE[footer-include](../includes/footer-banner.md)]