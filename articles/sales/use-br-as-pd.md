---
title: Usar un recurso reservable como dimensión de prezos
description: Este tema fornece información sobre como usar recurso reservable como dimensión de prezos.
author: Rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: dcd01d80236f0218bc6fa3a1fe1389f8314f3c9b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598625"
---
# <a name="use-a-bookable-resource-as-a-pricing-dimension"></a>Usar un recurso reservable como dimensión de prezos

 _**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_ 

Este tema fornece información sobre como usar recurso reservable como dimensión de prezos. Se a súa estratexia de prezos está configurada de xeito que cada recurso reservable debe ter un prezo ou unha taxa de custo específicos, use un recurso reservable como dimensión de prezos.

## <a name="prerequisites"></a>Requisitos previos
Antes de completar os procedementos deste tema, debe ter unha nova solución de dimensión de prezos para a súa organización. Se aínda non o creou, consulte [Crear campos e entidades personalizados](../pricing-costing/create-custom-fields-entities-pricing-dimensions.md).

## <a name="add-the-bookable-resource-field-to-forms-and-views"></a>Engadir un campo de recurso reservable a formularios e vistas
Para facer o campo **Recurso reservable** visible na solución de dimensión de prezos, cómpre engadir o campo a todos os formularios e vistas como unha entidade.

A seguinte táboa indica todos os formularios e vistas listos para usar, por entidade. Tamén necesitará engadir o novo campo a calquera formulario ou vista adicional nas súas entidades personalizadas.

|   Entity        | Formularios   |Visualizacións        |
| ------------------------------|---------------------------------|----------------------------------|
|  Prezo do rol| Información | - Prezos de categorías de recursos activos<br> - Visualización asociada do prezo da categoría de recursos |
|  Sobreprezo do prezo da función| Información| - Sobreprezo do prezo do rol activo<br>- Sobreprezo do prezo do rol asociado |
|  Detalle da liña da oferta| - Información do proxecto<br>- Creación rápida do proxecto| - Detalles da liña de oferta activos<br>- Detalles da liña de oferta combinados<br>- Detalles da liña de oferta asociada |
|  Detalle da liña de contrato do proxecto| - Información do proxecto<br>- Creación rápida do proxecto| - Detalles da liña de contrato combinados<br>- Detalles activos da liña de contrato<br>- Detalles da liña de contrato asociada |
|  Tarefa do proxecto| - Información<br>- Novo formulario| &nbsp; |
|  Membro do equipo do proxecto| - Información<br>- Novo formulario| - Membros do equipo de proxecto activos<br>- Membros do equipo do proxecto<br>- Membros do equipo de proxecto asociados |
|  Entrada de tempo| - Información<br>- Crear entrada de tempo| - As miñas entradas de tempo por data<br>- As miñas entradas de tempo desta semana<br>- Entradas de tempo para aprobar|
|  Liña de diario| - Información<br>- Creación rápida| - Liñas de diario activas<br>- Liña de diario asociada |
|  Detalle da liña da factura| - Información<br>- Creación rápida| - Detalles da liña de factura activa<br>- Transaccións de facturas imputables<br>- Transaccións de facturas complementarias<br>- Detalles da liña de factura asociada <br>- Transaccións de facturas non imputables|
|  Dato real| - Información<br>- Datos reais activos| Datos reais asociados |

## <a name="set-up-a-bookable-resource-as-a-pricing-dimension"></a>Configurar un recurso reservable como dimensión de prezos
Para configurar un recurso reservable como dimensión de prezos, siga estes pasos:

1. Vaia a **Configuración** > **Parámetros**. 
2. Na páxina **Parámetro**, no separador **Dimensións de prezos baseados na cantidade**, verifique que a grade do separador mostra os rexistros da entidade **Dimensións de prezos**. 
2. Engada **Recurso reservable** a esta lista de dimensións de prezos como **msdyn_bookableresource**. 
3. En **Aplicable ao custo** e **Aplicable ás vendas**, seleccione un valor.
4. En **Tipo de dimensión**, seleccione **Baseado na cantidade**. 
5. Seleccione a prioridade de custo e vendas para o recurso reservable. Normalmente, un recurso reservable ten a máxima prioridade cando se inclúe como dimensión de prezo. Estableza a prioridade en **1** (ou **0** dependendo de como se conte a prioridade) para garantir este comportamento.

## <a name="set-up-pricing-dimension-field-names"></a>Configurar nomes de campo de dimensións de prezos

Cando o nome de campo dunha dimensión de prezos na táboa **Prezo de rol** é diferente do seu nome de campo en calquera das outras entidades onde se utiliza o prezo predefinido, o rexistro de dimensión de prezos debe recibir unha notificación dos diferentes nomes.  

Para un recurso reservable, a entidade **Membros do equipo** do proxecto ten un nome de campo lixeiramente diferente do da entidade **Prezo de rol**. 

 - Entidade **Membros do equipo do proxecto** =**msdyn_bookableresourceid**
 - Entidade **Prezo do rol** =**msdyn_bookableresource**

O rexistro da dimensión de prezos para **msydn_bookableresource** debe recibir notificación desta diferencia.

1. Prema dúas veces na fila na grade **Dimensións dos prezos** para abrir a páxina de dimensións de **msdyn_bookableresource**.
2. Na páxina de dimensión, no separador **Relacionado**, seleccione **Nomes de campo da dimensión de prezos**.

  ![Separador de nomes de campo de dimensión de prezos.](media/PD-fieldname.png)

3. Na vista asociada que se abre, seleccione **Engadir novo nome de campo da dimensión de prezos**.

  ![Engadir novos nomes de campo de dimensión de prezos.](media/Add-NewPD-fieldname.png)

  Isto abre a páxina **Novo nome de campo da dimensión de prezos** para **msdyn_bookableresource**. 

4. Na páxina **Nome do campo de nova dimensión de prezos**, engada **msdyn_projectteam** a **Nome lóxico da entidade**.
5. Engada **msdyn_bookableresourceid** a **Nome do campo**.

 ![Novo formulario de nome de campo de dimensión de prezos.](media/PD-fieldname-Added.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]