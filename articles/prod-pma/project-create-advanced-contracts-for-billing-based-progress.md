---
title: Crear contratos avanzados para a facturación baseada no progreso
description: Este tema explica como crear contratos de proxectos para que poida xerar facturas para os clientes, en función dunha porcentaxe do traballo rematado.
author: RadhikaRS
manager: AnnBe
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 1a83785a9db4dffc4585acf11ef971c08594f312
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076261"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a>Crear contratos avanzados para a facturación baseada no progreso
[!include [banner](../includes/banner.md)]

Este tema explica como crear contratos de proxectos para que poida crear facturas para os clientes, en función dunha porcentaxe do traballo rematado. Os importes da factura calcúlanse automaticamente para as categorías orzamentarias de traballo que configurou para un proxecto. O prazo de facturación establécese cando negocia o contrato do proxecto co cliente.

Utilice os procedementos deste tema para configurar un contrato, un proxecto asociado e as regras de facturación que calculan os importes da factura para as categorías de traballo orzamentarias que configurou para o proxecto.

Despois de crear o contrato e o proxecto, pode configurar os detalles do proxecto. Por exemplo, pode definir actividades e atribuír traballadores ao proxecto.

## <a name="example"></a>Exemplo

A súa organización é unha empresa de desenvolvemento de software. Acepta desenvolver un paquete de contabilidade da nóminas para un cliente por unha taxa total de 20 000 dólares estadounidenses (USD). A súa organización acepta facturar ao cliente a medida que completa porcentaxes específicas do proxecto. Vostede configura as seguintes categorías de proxectos para o traballo para que poida usalas no proceso de facturación:

- Consultoría
- Deseñar
- Instalación

Vostede tamén configura regras de facturación que calculan automaticamente os importes da factura para a porcentaxe de traballo do proxecto que se completa para cada categoría.

O xestor do orzamento crea un orzamento para as categorías do proxecto. A cantidade de traballo completado calcúlase automaticamente como unha porcentaxe do traballo real en comparación cos importes orzados.

## <a name="prerequisites"></a>Requisitos previos

Antes de crear un proxecto que use regras de facturación, debe configurar as secuencias numéricas para as regras de facturación e un diario de tarifas que se empregue para contabilizar as facturas de progreso.

1. Vaia a **Xestión e contabilidade de proxectos** \> **Configuración** \> **Parámetros de Xestión e contabilidade de proxectos**.
2. Na páxina **Parámetros de Xestión e contabilidade de proxectos**, no separador **Secuencias numéricas**, configure a secuencia numérica que desexa empregar cando se crean as regras de facturación.
3. Vaia a **Xestión e contabilidade de proxectos** \> **Diarios** \> **Tarifa**.
4. Na páxina **Diario de tarifas**, seleccione **Novo** e introduza o nome do diario.

## <a name="create-a-contract-for-progress-billings"></a>Crear un contrato para a facturación de progreso

Utilice este procedemento para crear un contrato de proxecto para un proxecto de prezo fixo. Vostede crea unha factura do proxecto cando o traballo rematado no proxecto alcanza unha porcentaxe especificada.

1. Vaia a **Xestión e contabilidade de proxectos** \> **Proxectos** \> **Contratos de proxecto**.
2. Na páxina **Contratos de proxecto**, seleccione **Novo**.
3. Na caixa de diálogo **Novo contrato de proxecto**, configure os seguintes campos:

    - **Nome**
    - **Tipo de financiamento**
    - **Fonte de financiamento**
    - **Moeda de vendas** - Por defecto, esta moeda úsase para as facturas dos clientes asociadas ao contrato do proxecto. Non obstante, pode cambiar a moeda de vendas nunha factura específica do cliente.

4. Seleccione **Aceptar**. A información copiase na cabeceira da páxina **Contratos de proxecto**.
5. Na páxina **Contratos de proxecto**, encha o resto da información requirida para o proxecto.

## <a name="create-a-project-for-progress-billings"></a>Crear un proxecto para a facturación de progreso

Siga estes pasos para crear un proxecto e calquera subproxecto asociado a un contrato de proxecto.

1. Vaia a **Xestión e contabilidade de proxectos** \> **Proxectos** \> **Todos os proxectos**.
2. Na páxina **Todos os proxectos**, seleccione **Novo**.
3. Na caixa de diálogo **Novo proxecto**, no campo **Tipo de proxecto**, seleccione **Tempo e material**.
4. Seleccionar un grupo de proxectos. Un grupo de proxectos define a información de contabilización dos proxectos asignados ao grupo.
5. Seleccione **Crear proxecto**.
6. Despois de crear o proxecto, configure a fase do proxecto en **En proceso**.

## <a name="create-a-budget-for-a-project"></a>Crear un orzamento para un proxecto

As categorías de orzamento utilízanse para calcular automaticamente os importes da factura para a porcentaxe de traballo que se completa para cada categoría. Siga estes pasos para crear categorías de orzamento para os custos estimados.

1. Vaia a **Xestión e contabilidade de proxectos** \> **Proxectos** \> **Todos os proxectos**.
2. Na páxina **Todos os proxectos**, seleccione e abra o proxecto que desexe.
3. Na páxina **Proxectos**, no Panel de acción, no separador **Plan**, no grupo **Orzamento**, seleccione **Orzamento do proxecto**.
4. Na páxina **Orzamento do proxecto**, introduza un custo estimado para cada categoría do proxecto.

## <a name="create-billing-rules-for-progress-billings"></a>Crear regras de facturación para a facturación de progreso

1. Vaia a **Xestión e contabilidade de proxectos** \> **Proxectos** \> **Contratos de proxecto**.
2. Na páxina de lista **Contratos de proxecto**, seleccione e abra un contrato de proxecto.
3. Na páxina do contrato do proxecto, no separador rápido **Regras de facturación**, seleccione **Engadir**.
4. Na páxina **Regra de facturación**, no campo **Tipo de liña**, seleccione **Progreso**.
5. No separador rápido **Detalles da liña de regra de facturación**, no campo **Valor do contrato**, introduza o valor total do contrato.
6. No campo **Categoría**, seleccione a categoría para contabilizar a transacción da tarifa.
7. No campo **Proxecto**, seleccione o proxecto que usa esta regra de facturación.
8. Opcional: Atribúa a regra de facturación a proxectos adicionais. No separador rápido **Proxecto**, na sección **Proxectos dispoñibles**, seleccione un proxecto e, a seguir, seleccione o botón de frecha dereita para engadir o proxecto á sección **Proxectos seleccionados**.
9. Opcional: Calcule a cantidade porcentual que o cliente retén dos pagamentos dunha factura. No separador rápido **Termos de retención do pagamento**, seleccione a fonte de financiamento e, a seguir, no campo **Porcentaxe de retención**, introduza a porcentaxe de retención.
10. Repita estes pasos para crear regras de facturación adicionais para o contrato do proxecto.
