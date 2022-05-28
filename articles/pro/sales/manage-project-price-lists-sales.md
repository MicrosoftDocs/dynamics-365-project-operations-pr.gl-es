---
title: Xestionar listas de prezos de proxecto nas ofertas de proxecto
description: Este tema ofrece información sobre como traballar con listas de prezos de proxecto nas ofertas.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3d9c13568921540f4cc2e1e5e58d01803631a339
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598256"
---
# <a name="manage-project-price-lists-on-project-quotes"></a>Xestionar listas de prezos de proxecto nas ofertas de proxecto 

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

As ofertas de proxecto están deseñadas para admitir listas de prezos de vendas vixentes en varias datas. Con Dynamics 365 Project Operations, engádese unha nova entidade asociada chamada **Listas de prezos do proxecto**. Esta entidade ten unha relación de un a moitos cunha oferta de proxecto.

As listas de prezos do proxecto úsanse para calcular as transaccións de tempo, material e gasto nun proxecto. Cando unha oferta ten unha ou máis listas de prezos do proxecto, estas listas de prezos úsanse para fixar o prezo das estimacións de tempo, material e gasto, e os datos reais dos proxectos asociados ao oferta a través da liña de oferta.

Cando non haxa listas de prezos do proxecto nunha oferta de proxecto, recibirá unha mensaxe de advertencia. A mensaxe indica que, debido a que non hai listas de prezos do proxecto, o traballo e os gastos do proxecto estimados e reais non terán un prezo. Pola contra, terán un prezo cero (0) para os valores de venda.

## <a name="associate-or-disassociate-a-project-price-list-on-a-project-quote"></a>Asociar ou desvincular unha lista de prezos de proxecto nunha oferta de proxecto

Para crear ou seleccionar unha lista de prezos específica para estimar o traballo e os gastos baseados en proxectos, complete os seguintes pasos.

1. Na oferta, seleccione o separador **Prezo do proxecto** e na subgrade seleccione **+ Engadir nova lista de prezos de proxecto**.
2. Na páxina de creación rápida, seleccione unha lista de prezos. A lista despregable mostra todas as listas de prezos que teñen o contexto establecido en **Vendas** e a moeda coincide coa moeda da oferta.
4. Insira unha descrición para a asociación de lista de prezos do proxecto e seleccione **Gardar e pechar**.

Créase unha asociación de lista de prezos de proxecto.

Pode repetir este proceso se precisa asociar máis dunha lista de prezos de proxecto á oferta de proxecto. Cree varias listas de prezos de proxecto só se ten datas efectivas diferentes en cada unha das listas de prezos de proxecto asociadas.

> [!NOTE]
> Project Operations non admite a superposición das datas de vixencia das listas de prezos de proxecto. Se hai varias listas de prezos de proxecto para unha transacción con data determinada, o prezo desa transacción por defecto será cero (0).
Para eliminar unha asociación de lista de prezos de proxecto, seleccione a lista de prezos de proxecto e logo seleccione **Eliminar lista de prezos de proxecto**. A lista de prezos elimínase das listas de prezos de proxecto da oferta, pero a propia lista de prezos non se elimina. Só se elimina a asociación á oferta.

## <a name="set-up-default-project-price-lists-on-a-quote"></a>Configurar as listas de prezos de proxecto por defecto nunha oferta

As listas de prezos de proxecto pódense configurar por defecto nunha oferta de proxecto. Esta configuración garante que todas as ofertas da súa organización comecen sempre cunha lista de prezos estándar para ese período de prezo.

### <a name="set-up-organizational-default-for-project-price-lists"></a>Configurar os valores organizativos por defecto para listas de prezos de proxecto

1. Vaia a **Configuración** > **Xeral** > **Parámetros**.
2. Na páxina de lista **Parámetros activos**, localice o rexistro e prema dúas veces para abrilo. 
3. Na páxina **Parámetros**, seleccione o separador **Lista de prezos**. Pode ver que se mostra a lista de listas de prezos por defecto. Esta é unha lista de listas de prezos estándar de custo e vendas. Se ten asociada aquí unha lista de prezos de venda para cada moeda na que vende, asegurarase de que esta lista de prezos de venda está por defecto en calquera oferta que cree para os clientes que fagan transaccións nesta moeda.

### <a name="set-up-customer-specific-project-price-lists"></a>Configurar listas de prezos de proxecto específicas do cliente

Tamén se poden configurar listas de prezos de proxecto específicas para o cliente cando negociou un acordo mestre de prezos cos seus clientes.

Para configurar unha lista de prezos de proxecto específica do cliente, complete os seguintes pasos.

1. Na área **Vendas**, seleccione **Clientes**.
2. Na lista das súas contas activas, seleccione e abra o rexistro do cliente para o que ten unha lista de prezos especial.
3. No separador **Listas de prezos de proxecto**, pode crear unha nova asociación de lista de prezos para ter a lista de prezos de proxecto específica para este cliente.

## <a name="create-custom-pricing-on-a-project-quote"></a>Crear prezos personalizados nunha oferta de proxecto

Despois de ter listas de prezos de proxecto por defecto organizativas e específicas do cliente, as súas ofertas de proxecto crearanse automaticamente con estas asociacións de listas de prezos de proxecto. Non obstante, en certos casos, pode que teña que crear prezos personalizados para unha oferta de proxecto específica. 

1. En **Oferta de proxecto**, no separador **Lista de prezos de proxecto**, verifique na subgrade que non hai ningún rexistro de lista de prezos específica seleccionada.
2. Seleccione **Crear prezos personalizados**. Isto fará copias de todas as listas de prezos estándar asociadas actualmente á oferta e asociará estas copias á oferta. Eliminaranse as asociacións existentes ás listas de prezos estándar. O comercial pode entón comezar a facer modificacións nos prezos destas copias. Estes prezos modificados só serán aplicables a esta oferta de proxecto.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
