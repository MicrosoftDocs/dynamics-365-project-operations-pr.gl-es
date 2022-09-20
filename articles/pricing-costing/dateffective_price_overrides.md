---
title: Anulacións de prezos en vigor na data
description: Este artigo explica como configurar as substitucións de prezos para prezos específicos na lista de prezos.
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
# <a name="date-effective-price-overrides"></a>Anulacións de prezos en vigor na data 

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

*Anulacións de prezos en vigor na data* proporcionar unha forma de anular ou cambiar prezos específicos na lista de prezos. Por exemplo, tes unha lista de prezos estándar que está en vigor desde o 1 de xaneiro de 2022 ata o 31 de decembro de 2022. Esta lista de prezos ten prezos para moitos papeis. O prezo que se establece para o **Técnico de redes** rol é de 100 dólares estadounidenses (USD) por hora. Cando un técnico de rede rexistra o tempo entre o 1 de xaneiro de 2022 e o 31 de decembro de 2022, a hora ten un prezo de 100 USD. O 1 de outubro de 2022, debes axustar o prezo *só* para o **Técnico de redes** rol, desde 100 USD por hora ata 110 USD por hora. O **Data de anulación do prezo efectivo** A función permítelle configurar este cambio como unha substitución da fila para ese prezo específico de función. Polo tanto, non tes que copiar toda a lista de prezos e cambiar o prezo só desa fila.

## <a name="date-effective-price-overrides-for-labor-pricing"></a>Anulacións de prezos efectivos na data para os prezos da man de obra

O proceso de configuración de substitucións de prezos efectivos na data para o tempo de traballo nun proxecto consta de dous pasos básicos.

1. Activar **Data de anulación do prezo efectivo** característica.
1. Configura un cambio de prezo efectivo na data.

### <a name="enable-the-date-effective-price-overrides-feature"></a>Activa a función de anulacións de prezos en vigor da data

> [!NOTE]
> Tras o **Data de anulación do prezo efectivo** a función está activada, non se pode desactivar.

Para habilitar o **Anulacións de prezos en vigor na data** función, siga estes pasos.

1. Ir a **Configuración** \> **Parámetros**.
1. Abre o **Parámetros** rexistro.
1. No panel de accións, no **Control de funcións** ficha, seleccione **Activar as anulacións de prezos efectivos da data**.
1. Na caixa de diálogo de confirmación, seleccione **Aceptar**.
1. Despois duns momentos, actualice o navegador. Agora deberían estar dispoñibles as capacidades de anulación de prezos efectivas na data. Saberá que estas capacidades foron habilitadas se **Activar as anulacións de prezos efectivos da data** xa non aparece no Panel de accións.

### <a name="set-up-a-date-effective-price-override"></a>Configura un cambio de prezo efectivo na data

Pódense configurar as anulacións de prezos en vigor na data **Custo**, **·**, ou **Compra** listas de prezos.

> [!NOTE]
>O comportamento do **Data de anulación do prezo efectivo** actualmente ten as seguintes limitacións:
>
> - Só os prezos de funcións e as marcas de prezos de función admiten **Data de anulación do prezo efectivo** función en Operacións do proxecto.
> - Cando copias unha lista de prezos usando o **Copiar** acción sobre o **Detalles da lista de prezos** e cando crea unha lista de prezos dun proxecto a partir dunha lista de prezos estándar ou personalizada durante a creación do contrato, as anulacións de prezos en vigor na data.**non** copiado da lista de prezos de orixe.

Para configurar unha substitución de prezos en vigor na data para un prezo de función ou unha marca de prezo de función, siga estes pasos.

1. Abre a páxina da lista de prezos para a que queres configurar a substitución de prezos en vigor na data.
1. Seleccione o **Prezos dos roles** ficha. Esta pestana lista todos os **Prezo do papel** rexistros na lista de prezos.
1. Seleccione o **Prezo do papel** rexistra o que queres configurar un novo prezo de anulación efectivo para a data e, a continuación, toca dúas veces (ou fai dobre clic) **Prezo do papel** para abrir o **Detalles do prezo do rol** páxina.
1. Seleccione o **Anulacións efectivas da data** ficha. A grade desta pestana enumera todas as anulacións de prezos en vigor na data para o seleccionado **Prezo do papel** rexistro.
1. Na barra de ferramentas situada enriba da grade, seleccione **Nova substitución do prezo do rol**. O **Nova substitución do prezo do rol** ábrese o control deslizante.
1. Especifique a data de entrada en vigor, a unidade e o novo prezo para a substitución do prezo. A continuación, seleccione **Gardar**, e pecha o formulario.

> [!NOTE]
> - Unha substitución de prezos en vigor na data para un prezo de función ou unha marca de prezo de función aplícase á mesma combinación de valores de dimensión de prezos que existe no pai.**Prezo do papel** ou **Marxe de prezo de función** fila.
> - A data seleccionada no **Efectivo desde** campo debe estar dentro das datas de vixencia da lista de prezos dos pais. A anulación do prezo terá efecto na data seleccionada no **Efectivo desde** campo e aplicarase ata o final da data de finalización da lista de prezos. Se configuras outra anulación de prezos en vigor na data para o mesmo prezo de función, a primeira anulación de prezos terá efecto na data seleccionada no **Efectivo dende** campo e aplicarase ata o inicio da segunda anulación.

## <a name="examples"></a>Exemplos

### <a name="example-1-determining-date-effectivity-for-a-role-price-that-has-role-price-overrides"></a>Exemplo 1: determinación da data de vixencia para un prezo de función que teña substitucións de prezo de función

O seguinte exemplo mostra como se determina a efectividade da data para un prezo de función específico para o que se configuran as substitucións de prezos de función.

**Lista de prezos A: do 1 de xaneiro ao 30 de xuño**

*Prezo do papel*

| Prezo do papel | Unidade | Prezo | Efecto sobre o prezo das transaccións entrantes |
|---|---|---|---|
| Técnico de redes | Hora | 100 | Este prezo utilizarase en todas as transaccións nas que a data da transacción sexa entre o 1 de xaneiro e o 14 de marzo. |

*Anulación do prezo do rol*

| Efectivo dende | Unidade | Prezo | Efecto sobre o prezo das transaccións entrantes |
|---|---|---|---|
| Marzo 15 | Hora | 110 | Este prezo utilizarase en todas as transaccións nas que a data da transacción estea entre o 15 e o 30 de marzo. |
| Abril de 1 | Hora | 120 | Este prezo utilizarase en todas as transaccións nas que a data da transacción sexa entre o 1 de abril e o 30 de xuño. |

### <a name="example-2-determining-date-effectivity-for-a-role-price-markup-that-has-role-price-markup-overrides"></a>Exemplo 2: determinación da data de efectividade para unha marca de prezos de función que teña anulacións de marca de prezos de función

O seguinte exemplo mostra como se determina a efectividade da data para unha marca de prezo de función específica para a que se configuran as substitucións de marca de prezo de función.

**Lista de prezos A: do 1 de xaneiro ao 30 de xuño**

*Prezo do papel*

| Prezo do papel | Horas laborables | Unidade | Prezo | Efecto sobre o prezo das transaccións entrantes |
|---|---|---|---|---|
| Técnico de redes | Regular | Hora | 100 | Este prezo utilizarase en todas as transaccións nas que a data da transacción sexa entre o 1 de xaneiro e o 14 de marzo. |

*Marxe de prezo de función*

| Unidade organizativa | Horas laborables | Marcar % |
|---|---|---|
| Contoso EUA | Horas extra | 10 % |

*Anulación da marca de prezos de función*

| Efectivo desde | Prezo | Efecto sobre o prezo das transaccións entrantes |
|---|---|---|
| Marzo 15 | 20 % | Este porcentaxe de recargo utilizarase en todas as transaccións nas que a data da transacción estea entre o 15 e o 30 de marzo. |
| Abril de 1 | 25 % | Este marcado utilizarase en todas as transaccións nas que a data da transacción estea entre o 1 de abril e o 30 de xuño. |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
