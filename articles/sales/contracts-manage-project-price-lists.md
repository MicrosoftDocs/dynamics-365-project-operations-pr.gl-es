---
title: Xestionar listas de prezos de proxecto nos contratos de proxecto
description: Este artigo ofrece información sobre a xestión de listas de prezos de proxecto en contratos de proxecto.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 23b9e6f9bc3e4bc3fb03de62064644dd58da34c7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926176"
---
# <a name="manage-project-price-lists-on-project-contracts"></a>Xestionar listas de prezos de proxecto nos contratos de proxecto

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Os contratos de proxecto en Dynamics 365 Project Operations están deseñados para admitir listas de prezos de venda efectivas en varias datas nun contrato. En Project Operations, hai unha nova entidade asociada chamada **Listas de prezos de proxecto**. Esta entidade ten unha relación de un a moitos cun contrato de proxecto.

As listas de prezos do proxecto úsanse para calcular as transaccións de tempo, material e gasto nun proxecto. Cando un contrato ten unha ou máis listas de prezos do proxecto, estas listas de prezos úsanse para fixar o prezo das estimacións de tempo, material e gasto, e os datos reais dos proxectos asociados ao contrato a través da liña de contrato.

Cando non haxa listas de prezos do proxecto nun contrato de proxecto, verá unha mensaxe de advertencia de que non hai listas de prezos do proxecto e as súas estimacións, traballo real do proxecto, material e gastos rexistrados non terán un prezo. Non haberá prezo para os valores de venda.

## <a name="associate-or-unassociate-a-project-price-list-on-a-project-contract"></a>Asociar ou desasociar unha lista de prezos de proxecto nun contrato de proxecto

### <a name="create-or-associate-a-specific-price-list-for-estimating-project-based-work-material-and-expenses"></a>Crear ou asociar unha lista de prezos específica para estimar o traballo, o material e os gastos baseados no proxecto

1. No contrato de proxecto, seleccione o separador **Listas de prezos de proxecto**.
2. Na subgrade, seleccione **+ Engadir nova lista de prezos de proxecto**.
3. Na barra de desprazamento de **Creación rápida**, seleccione unha lista de prezos. 

  A lista despregable mostra todas as listas de prezos que teñen o contexto establecido en **Vendas**, onde a moeda da lista de prezos coincide coa moeda do contrato.
  
4. Insira unha descrición para a asociación de lista de prezos de proxecto, seleccione **Gardar** e logo peche a barra de desprazamento de **Creación rápida**.

   Créase unha asociación de lista de prezos de proxecto.
   
5. Repita os pasos 1-4 para asociar máis dunha lista de prezos de proxecto ao contrato de proxecto. Cree varias listas de prezos de proxecto só se ten unha efectividade de datas diferente en cada unha das listas de prezos de proxecto asociado.

> [!NOTE]
> Project Operations non admite a superposición da efectividade das datas das listas de prezos de proxecto. Se hai varias listas de prezos de proxecto para unha transacción cunha data determinada, o prezo desa transacción por defecto será cero.

### <a name="remove-a-project-price-list-association"></a>Eliminar unha asociación de lista de prezos de proxecto

- Seleccione a lista de prezos de proxecto e logo seleccione **Eliminar lista de prezos de proxecto do contrato** na subgrade. 

  A lista de prezos elimínase das listas de prezos de proxecto no contrato. A propia lista de prezos non se eliminará. Só se eliminará a asociación ao contrato.

## <a name="set-up-automatic-defaulting-of-project-price-lists-on-a-contract"></a>Configurar por defecto automaticamente as listas de prezos de proxecto nun contrato

Pódese configurar unha lista de prezos do proxecto como lista de prezos por defecto do proxecto. Esta configuración garante que todos os contratos da súa organización sempre comecen cunha lista de prezos estándar do proxecto para ese período de prezos.

### <a name="set-up-the-organizational-default-for-project-price-lists"></a>Configurar o valor organizativo predefinido para as listas de prezos de proxecto

1. Vaia a **Configuración** > **Xeral** e logo seleccione **Parámetros**.
2. Na páxina de lista **Parámetros activos**, seleccione e prema dúas vece no rexistro para abrilo. Mentres preme dúas veces, asegúrese de non premer nun valor de campo que sexa hiperligazón. 
3. Na páxina **Parámetros activos**, seleccione o separador **Lista de prezos**. Unha subgrade mostra unha lista de listas de prezos predefinidas. Esta é unha lista de custos estándar e listas de prezos de venda. Ter unha lista de prezos de **Vendas** asociada aquí para cada moeda na que venda garante que a lista de prezos de venda é a predefinida en calquera contrato que cree para os clientes que realicen transaccións nesta moeda.

### <a name="set-up-a-customer-specific-project-price-list"></a>Configurar unha lista de prezos de proxecto específica do cliente

Tamén pode configurar listas de prezos de proxecto específicas para o cliente cando negocie un acordo mestre de prezos cos seus clientes.

1. Vaia a **Vendas** > **Clientes**.
2. Na lista de contas activas, seleccione o cliente para quen ten unha lista de prezos especial.
3. Seleccione o rexistro do cliente para abrilo e logo seleccione o separador **Listas de prezos de proxecto**. Unha subgrade mostra unha lista de listas de prezos de proxecto específicas para este cliente. 
4. Cree aquí unha nova asociación de lista de prezos para que a lista de prezos de proxecto sexa específica para este cliente.

## <a name="custom-pricing-on-a-project-contract"></a>Prezos personalizados nun contrato de proxecto

Despois de ter listas de prezos predefinidas organizativas e específicas para o cliente, os contratos de proxecto crearanse automaticamente con estas asociacións de listas de prezos de proxecto. Non obstante, as listas de prezos de proxecto nun contrato de proxecto sempre se copian coa data e o nome do contrato anexos a elas. Os xestores de contas e proxectos poden entón comezar a facer modificacións nos prezos destas copias. Estes prezos modificados só serán aplicables a este contrato de proxecto.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
