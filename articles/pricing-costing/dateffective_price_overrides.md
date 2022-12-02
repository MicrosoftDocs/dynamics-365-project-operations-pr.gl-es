---
title: Anulacións de prezos con datas efectivas
description: Este artigo explica como configurar as anulacións de prezos para prezos específicos na lista de prezos.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 41af5176c0809c9621fc0fa946a04492da7d152b
ms.sourcegitcommit: 37293b0b28f072deafc00112ddbbea91c48a7802
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 09/08/2022
ms.locfileid: "9446000"
---
# <a name="date-effective-price-overrides"></a>Anulacións de prezos con datas efectivas 

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

*Anulacións de prezos con datas efectivas* proporciona unha forma de anular ou cambiar prezos específicos na lista de prezos. Por exemplo, vostede ten unha lista de prezos estándar que está en vigor desde o 1 de xaneiro de 2022 ata o 31 de decembro de 2022. Esta lista de prezos ten prezos para moitos roles. O prezo que se establece para o rol **Técnico de redes** é de 100 dólares estadounidenses (USD) por hora. Cando un técnico de redes rexistra o tempo entre o 1 de xaneiro de 2022 e o 31 de decembro de 2022, a hora ten un prezo de 100 USD. O 1 de outubro de 2022, debe axustar o prezo *só* para o rol **Técnico de redes**, desde 100 USD por hora ata 110 USD por hora. A funcionalidade **Anulacións de prezos con data efectiva** permítelle configurar este cambio como unha anulación da fila para ese prezo específico de rol. Polo tanto, non ten que copiar toda a lista de prezos e cambiar o prezo só desa fila.

## <a name="date-effective-price-overrides-for-labor-pricing"></a>Anulacións de prezos con data efectiva para fixar os prezos da man de obra

O proceso de configuración de anulacións de prezos con data efectiva para o tempo de traballo nun proxecto consta de dous pasos básicos.

1. Active a funcionalidade **Anulacións de prezos con datas efectivas**.
1. Configure unha anulación de prezos con datas efectivas.

### <a name="enable-the-date-effective-price-overrides-feature"></a>Activar a funcionalidade Anulacións de prezos con datas efectivas

> [!NOTE]
> Despois de activar a funcionalidade **Anulacións de prezos con datas efectivas**, non se pode desactivar.

Para activar a funcionalidade **Anulacións de prezos con datas efectivas**, siga estes pasos.

1. Vaia a **Configuración** \> **Parámetros**.
1. Abra o rexistro **Parámetros**.
1. No panel Acción, no separador **Control de funcións**, seleccione **Activar as anulacións de prezos con datas efectivas**.
1. Na caixa de diálogo de confirmación, seleccione **Aceptar**.
1. Despois duns momentos, actualice o navegador. Agora deberían estar dispoñibles as capacidades de anulación de prezos con datas efectivas. Saberá que estas capacidades foron habilitadas se o botón **Activar anulacións de prezos con datas efectivas** xa non aparece no panel Acción.

### <a name="set-up-a-date-effective-price-override"></a>Configurar unha anulación de prezos con datas efectivas

As anulacións de prezos con datas efectivas pódense configurar nas listas de prezos **Custo**, **Vendas** ou **Compra**.

> [!NOTE]
>O comportamento das **Anulacións de prezos con datas efectivas** actualmente ten as seguintes limitacións:
>
> - Só os prezos de rol e os sobreprezos de rol admiten a funcionalidade **Anulacións de prezos con datas efectivas** en Project Operations.
> - Cando copia unha lista de prezos usando a acción **Copiar** na páxina **Detalles da lista de prezos** e cando crea unha lista de prezos de proxecto a partir dunha lista de prezos estándar ou personalizada durante a creación do contrato, as anulacións de prezos con datas efectivas **non** se copian da lista de prezos de orixe.

Para configurar unha substitución de prezos con datas efectivas para un prezo de rol ou un sobreprezo de rol, siga estes pasos.

1. Abra a páxina da lista de prezos para a que quere configurar a anulación de prezos con datas efectivas.
1. Seleccione o separador **Prezos de rol**. Este separador lista todos os rexistros de **Prezo de rol** na lista de prezos.
1. Seleccione o rexistro de **Prezo de rol** para o que quere configurar una nova anulación de prezos con datas efectivas, e logo toque dúas veces (ou prema dúas veces) **Prezo de rol** para abrir a páxina **Detalles de prezo de rol**.
1. Seleccione o separador **Anulacións con datas efectivas**. A grade deste separador enumera todas as anulacións de prezos con datas efectivas para o rexistro de **Prezo de rol** seleccionado.
1. Na barra de ferramentas situada enriba da grade, seleccione **Nova anulación de prezo de rol**. Ábrese a barra de desprazamento **Nova anulación de prezo de rol**.
1. Especifique a data de entrada en vigor, a unidade e o novo prezo para a anulación do prezo. Logo seleccione **Gardar** e peche o formulario.

> [!NOTE]
> - Unha anulación de prezos con datas efectivas para un prezo de rol ou un sobreprezo de rol aplícase á mesma combinación de valores de dimensión de prezos que existe na fila **Prezo de rol** ou **Sobreprezo de rol** principal.
> - A data seleccionada no campo **Efectivo desde** debe estar dentro das datas efectivas da lista de prezos principal. A anulación de prezos terá efecto na data seleccionada no campo **Efectivo desde** e aplicarase ata o final da data de finalización da lista de prezos principal. Se configura outra anulación de prezos con datas efectivas para o mesmo prezo de rol, a primeira anulación de prezos terá efecto na data seleccionada no campo **Efectivo desde** e aplicarase ata o inicio da segunda anulación.

## <a name="examples"></a>Exemplos

### <a name="example-1-determining-date-effectivity-for-a-role-price-that-has-role-price-overrides"></a>Exemplo 1: Determinación da data efectiva para un prezo de rol que teña anulacións de prezo de rol

O seguinte exemplo mostra como se determinan as datas efectivas para un prezo de rol específico para o que se configuran as anulacións de prezos de rol.

**Lista de prezos A: do 1 de xaneiro ao 30 de xuño**

*Prezo de rol*

| Prezo de rol | Unidade | Prezo | Efecto sobre a fixación de prezos das transaccións entrantes |
|---|---|---|---|
| Técnico de redes | Hora | 100 | Este prezo utilizarase en todas as transaccións nas que a data da transacción sexa entre o 1 de xaneiro e o 14 de marzo. |

*Anulación de prezo de rol*

| Efectivo desde | Unidade | Prezo | Efecto sobre a fixación de prezos das transaccións entrantes |
|---|---|---|---|
| Marzo 15 | Hora | 110 | Este prezo utilizarase en todas as transaccións nas que a data da transacción sexa entre o 15 de marzo e o 30 de marzo. |
| Abril de 1 | Hora | 120 | Este prezo utilizarase en todas as transaccións nas que a data da transacción sexa entre o 1 de abril e o 30 de xuño. |

### <a name="example-2-determining-date-effectivity-for-a-role-price-markup-that-has-role-price-markup-overrides"></a>Exemplo 2: Determinación da data efectiva para un sobreprezo de rol que teña anulacións de sobreprezo de rol

O seguinte exemplo mostra como se determinan as datas efectivas para un sobreprezo de rol específico para o que se configuran as anulacións de sobreprezos de rol.

**Lista de prezos A: do 1 de xaneiro ao 30 de xuño**

*Prezo de rol*

| Prezo de rol | Horas laborables | Unidade | Prezo | Efecto sobre a fixación de prezos das transaccións entrantes |
|---|---|---|---|---|
| Técnico de redes | Habituais | Hora | 100 | Este prezo utilizarase en todas as transaccións nas que a data da transacción sexa entre o 1 de xaneiro e o 14 de marzo. |

*Sobreprezo de rol*

| Unidade organizativa | Horas laborables | % de sobreprezo |
|---|---|---|
| Contoso EUA | Horas extra | 10 % |

*Anulación de sobreprezo de rol*

| Efectivo desde | Prezo | Efecto sobre a fixación de prezos das transaccións entrantes |
|---|---|---|
| Marzo 15 | 20 % | Esta porcentaxe de sobreprezo utilizarase en todas as transaccións nas que a data da transacción sexa entre o 15 de marzo e o 30 de marzo. |
| Abril de 1 | 25 % | Este sobreprezo utilizarase en todas as transaccións nas que a data da transacción sexa entre o 1 de abril e o 30 de xuño. |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
