---
title: Contratos do proxecto
description: Este tema ofrece exemplos dos contratos de proxecto que pode crear para varios tipos de proxectos e fontes de financiamento e de como pode xestionar os contratos e facturar aos clientes do proxecto.
author: KimANelson
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 854ddfe6db93b7e93a4ee640268a9c8f254f24e7
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751416"
---
# <a name="project-contracts"></a>Contratos do proxecto

[!include [banner](../includes/banner.md)]

Este artigo ofrece exemplos dos contratos de proxecto que pode crear para varios tipos de proxectos e fontes de financiamento e de como pode xestionar os contratos e facturar aos clientes do proxecto.

O tipo de proxecto que cree para un contrato de proxecto determina o método que se usa para facturar aos clientes do proxecto. Pode cambiar un contrato de proxecto e o proxecto relacionado, pero non pode cambiar o tipo de proxecto. 

Ao usar un contrato de proxecto, pode facturar un ou máis proxectos ao mesmo tempo. O contrato do proxecto tamén axuda a garantir un procedemento de facturación uniforme para cada subproxecto dunha estrutura de proxecto. 

Todo proxecto que se facturará debe estar asociado a un contrato de proxecto. A configuración dun contrato de proxecto aplícase a todos os proxectos e subproxectos asociados a ese contrato de proxecto. 

Un contrato de proxecto pode especificar unha ou máis fontes de financiamento. Polo tanto, pode dividir a facturación entre varios patrocinadores, establecer límites de financiamento para que non se facture ás fontes de financiamento máis dun importe especificado e configurar regras de financiamento para cobrar gastos.

## <a name="funding-for-project-contracts"></a>Financiamento para contratos de proxectos
Algúns contratos de proxecto especifican que varias partes comparten a responsabilidade de financiar os custos do proxecto. Aquí van algúns exemplos:

-   Un gran cliente que ten varias divisións solicita que o financiamento dun proxecto se divida por división.
-   A súa empresa comparte os custos dun gran proxecto cunha organización externa.
-   Un proxecto de carreteira está cofinanciado por dous concellos.
-   Un proxecto de ponte está financiado por unha subvención do goberno e unha corporación privada.

En Dynamics 365 Finance, pode dividir a facturación dunha única transacción ou un proxecto completo entre varios clientes, subvencións ou organizacións. 

Nos proxectos que teñen varios patrocinadores, todas as partes que contribúen ao financiamento dun proxecto de financiamento avanzado chámanse fontes de financiamento. Despois de que un cliente, organización ou subvención se defina como unha fonte de financiamento, pódese asignar a unha ou máis regras de financiamento. As regras de financiamento conteñen os criterios que determinan como se asignan os cargos ás distintas fontes de financiamento dun proxecto. 

Debido a que os artigos almacenados, como os que aparecen nas solicitudes de compra e nos pedidos de compra, non se poden dividir, o importe do custo non se pode dividir entre varias fontes de financiamento no momento da distribución. Polo tanto, o valor da fonte de financiamento segue sendo 0 (cero) ata que se contabilice a emisión do inventario. Cando se contabiliza a emisión do inventario, o importe do custo distribúese segundo as regras de distribución da conta para o proxecto.

Aquí ten algúns pasos que pode seguir para facer máis doado dividir a facturación entre varias fontes de financiamento:

-   Especifique que todas as transaccións que se introducen nun proxecto utilizan a mesma moeda de vendas que o contrato do proxecto.
-   Configure límites de financiamento para que non se facture a unha fonte de financiamento máis dun importe especificado para un proxecto.
-   Configure as regras de financiamento e os límites de financiamento para cada traballador, artigo, categoría, grupo de categorías e tipo de transacción (ou para todos os tipos de transacción).
-   Seleccione as datas opcionais de inicio e fin para definir o período en que cada regra de financiamento é válida.
-   Especifique a porcentaxe da que é responsable cada fonte de financiamento.
-   Especifique que fonte de financiamento é responsable de redondear as diferenzas causadas polos cálculos de asignación de financiamento.
-   Configure regras que determinen como se facturan os custos do proxecto a clientes externos e se cargan ás organizacións internas.
-   Rexistre as transaccións nunha conta de financiamento en espera ata que se poida obter financiamento adicional ou ata que decida asumir os custos internamente.

Para determinar que grupo fiscal se asocia a unha transacción, búscase no proxecto unha atribución de grupo fiscal. Se non se realizou ningunha atribución de grupo fiscal ao nivel do proxecto, búscase no contrato do proxecto.

### <a name="example-multiple-funding-sources-simple"></a>Exemplo: Varias fontes de financiamento (simple)

A seguinte táboa ofrece escenarios para xestionar a asignación de financiamento entre varias fontes de financiamento. Estes escenarios baséanse nos seguintes supostos:

-   A configuración de prioridades inclúese na asignación de fondos antes de que se apliquen outros criterios de regras de financiamento.
-   Non se especificou un intervalo de datas para definir o período cando a regra de financiamento é válida.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Escenario</strong></td>
<td><strong>Fonte de financiamento</strong></td>
<td><strong>Porcentaxe de asignación</strong></td>
<td><strong>Prioridade de asignación</strong></td>
</tr>
<tr class="even">
<td>Vostede quere asignar custos a unha fonte de financiamento ata esgotar os seus fondos, asignar custos a unha segunda fonte de financiamento ata esgotar os seus fondos e, finalmente, asignar os custos restantes a unha terceira fonte de financiamento.</td>
<td><ul>
<li>Fonte de financiamento 1</li>
<li>Fonte de financiamento 2</li>
<li>Fonte de financiamento 3</li>
</ul></td>
<td><ul>
<li>100 %</li>
<li>100 %</li>
<li>100 %</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
<li>3</li>
</ul></td>
</tr>
<tr class="odd">
<td>Vostede quere destinar o 75 por cento dos custos a unha fonte de financiamento e o 25 por cento a unha segunda fonte de financiamento. Cando se esgota calquera desas fontes de financiamento, quere pagar os custos restantes dunha terceira fonte de financiamento.</td>
<td><ul>
<li>Fonte de financiamento 1</li>
<li>Fonte de financiamento 2</li>
<li>Fonte de financiamento 3</li>
</ul></td>
<td><ul>
<li>75 %</li>
<li>25 %</li>
<li>100 %</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
<tr class="even">
<td>Vostede quere destinar o 75 por cento dos custos a unha fonte de financiamento e o 25 por cento a unha segunda fonte de financiamento. Cando se esgota calquera desas fontes de financiamento, quere dividir os custos restantes entre unha terceira fonte de financiamento e unha cuarta fonte de financiamento.</td>
<td><ul>
<li>Fonte de financiamento 1</li>
<li>Fonte de financiamento 2</li>
<li>Fonte de financiamento 3</li>
<li>Fonte de financiamento 4</li>
</ul></td>
<td><ul>
<li>75 %</li>
<li>25 %</li>
<li>50 %</li>
<li>50 %</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
<li>2</li>
</ul></td>
</tr>
<tr class="odd">
<td>Vostede quere destinar o primeiro 25 por cento dos custos a unha fonte de financiamento e o resto a unha segunda fonte de financiamento.</td>
<td><ul>
<li>Fonte de financiamento 1</li>
<li>Fonte de financiamento 2</li>
</ul></td>
<td><ul>
<li>25 %</li>
<li>100 %</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a>Exemplo: Varias fontes de financiamento (complexo)

Vostede ten tres fontes de financiamento que desexa empregar na seguinte orde:

1.  Usar a fonte de financiamento 2 e a fonte de financiamento 3 por igual ata esgotar a fonte de financiamento 2.
2.  Continuar usando a fonte de financiamento 3 ata esgotala.
3.  Usar a fonte de financiamento 1 despois de esgotar a fonte de financiamento 3.

Para lograr este obxectivo, debe facer o seguinte:

-   Configurar límites de financiamento para a fonte de financiamento 2 e a fonte de financiamento 3, polas súas respectivas cantidades.
-   Crear as seguintes regras de financiamento:
    -   Regra 1 (Prioridade 1): Asignar o 50 por cento das transaccións á fonte de financiamento 2 e o 50 por cento á fonte de financiamento 3.
    -   Regra 2 (Prioridade 2): Asignar o 100 por cento das transaccións á fonte de financiamento 3.
    -   Regra 3 (Prioridade 3): Asignar o 100 por cento das transaccións á fonte de financiamento 1.

Esta configuración funciona porque as transaccións se contrastan con regras e límites para determinar se algunha delas se aplica á transacción. Se non se aplican regras nin límites específicos á transacción, aplícase a regra Todas as transaccións. A regra Todas as transaccións coincide con todas as transaccións. 

Se se atopa unha regra que coincide cunha transacción, a porcentaxe que se asignou nesa regra aplicase primeiro, pero só despois de que as coincidencias se contrasten con calquera límite establecido. Se se cumpriu un límite e se esgotan os fondos dunha fonte de financiamento, non se terá en conta a regra de financiamento asociada ao límite de financiamento e o programa comproba a seguinte regra que se aplica. 

Nalgúns casos, só unha parte dunha transacción pode asignarse baixo unha regra. Isto podería ocorrer porque se alcanza un límite cando se asigna a transacción. Neste caso, só se asigna unha determinada cantidade segundo esa regra, por exemplo, o 50 por cento a cada fonte de financiamento. É o caso da regra 1, que se describe anteriormente nesta sección. O resto asígnase segundo a seguinte regra da secuencia. 

A seguinte táboa examina este escenario con máis detalle.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Foco</strong></td>
<td><strong>Detalles</strong></td>
</tr>
<tr class="even">
<td>Regras de financiamento</td>
<td><ul>
<li>Regra 1 (Prioridade 1): Todas as transaccións. Asigne á fonte de financiamento 2 o 50 % e á fonte de financiamento 3 o 50 %.</li>
<li>Regra 2 (Prioridade 2): Todas as transaccións. Asigne á fonte de financiamento 3 o 100 %.</li>
<li>Regra 3 (Prioridade 2): Todas as transaccións. Asigne á fonte de financiamento 1 o 100 %.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Límites de financiamento</td>
<td><ul>
<li>Límite da fonte de financiamento 1 = 10 000,00</li>
<li>Límite da fonte de financiamento 2 = 500,00</li>
<li>Límite da fonte de financiamento 3 = 750,00</li>
</ul></td>
</tr>
<tr class="even">
<td>Transacción 1</td>
<td><strong>Importe da transacción:</strong> 100,00<strong>Financiamento:</strong> A transacción só se paga segundo a regra 1, porque a transacción se paga totalmente despois de aplicarse a regra 1. A transacción finánciase equitativamente entre a fonte de financiamento 2 e a fonte de financiamento 3.
<ul>
<li>Fonte de financiamento 2: 50,00</li>
<li>Fonte de financiamento 3: 50,00</li>
</ul></td>
</tr>
<tr class="odd">
<td>Transacción 2</td>
<td><strong>Importe da transacción:</strong> 5000,00<strong>Financiamento:</strong> A transacción págase segundo as tres regras. <strong>Regra 1</strong>
<ul>
<li>Fonte de financiamento 2: 450,00</li>
<li>Fonte de financiamento 3: 450,00</li>
</ul>
<strong>Regra 2</strong>
<ul>
<li>Fonte de financiamento 3: 250,00 (= 750,00 – 50,00 – 450,00)</li>
</ul>
<strong>Regra 3</strong>
<ul>
<li>Fonte de financiamento 1: 3850,00 (= 5000,00 – 450,00 – 450,00 – 250,00)</li>
</ul></td>
</tr>
<tr class="even">
<td>Total de fondos que se distribúen para cada fonte de financiamento</td>
<td><ul>
<li>Fonte de financiamento 1: 3850,00</li>
<li>Fonte de financiamento 2: 500,00</li>
<li>Fonte de financiamento 3: 750,00</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a>Regras de facturación
Cando negocia un contrato de proxecto cun cliente, vostede define como e cando pode facturar ao cliente o traballo nun proxecto. Despois de configurar o contrato do proxecto e o proxecto, pode configurar as regras de facturación do proxecto. As regras de facturación baséanse nos termos do proxecto que se especifican no contrato do proxecto. As regras de facturación que pode crear dependen das condicións do contrato do proxecto e do tipo de proxecto, como Tempo e material ou Prezo fixo, que vostede asocia á regra de facturación. Pode crear máis dunha regra de facturación para un contrato de proxecto. Tamén pode asignar unha regra de facturación a varios proxectos asociados ao mesmo contrato de proxecto e con condicións de facturación similares. 

Pode configurar os seguintes tipos de regras de facturación:

-   **Unidade de entrega** - Facture a un cliente cando complete unha unidade de entrega. Vostede define as unidades de entrega no contrato.
-   **Progreso** - Facture a un cliente cando complete unha porcentaxe especificada do proxecto. Pode configurar unha regra de facturación para calcular automaticamente a porcentaxe de traballo realizado ou pode calcular manualmente a porcentaxe de traballo rematado e o importe para facturar ao cliente.
-   **Fito** - Facture a un cliente o importe total dun fito do proxecto cando se alcance o fito.
-   **Tarifa** - Facture a un cliente os seus servizos máis unha comisión de xestión, que normalmente é unha porcentaxe do custo dos servizos.
-   **Tempo e material** - Facture a un cliente polo valor do tempo e os materiais que se utilizan nun proxecto.

Para todo tipo de regras de facturación, pode especificar unha porcentaxe de retención que se deduce das facturas dos clientes ata que un proxecto alcanza a fase acordada. A porcentaxe de retención do pagamento especifícase no contrato do proxecto. O importe calcúlase en función do valor total das liñas nunha factura do cliente e réstase del. 

Para as regras de facturación **Tempo e material** e **Progreso**, pode atribuír categorías imputables. As categorías imputables indican as transaccións que deben incluírse nas facturas dos clientes. 

Cando estea listo para facturar ao cliente, o importe a facturar polo proxecto calcúlase en función das regras de facturación e xérase unha proposta de factura do proxecto. 

As seguintes seccións ofrecen exemplos que mostran como configurar e xestionar as regras de facturación dun proxecto.

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a>Exemplo: Crear unha regra de facturación baseada no número de unidades entregadas

A súa organización asina un contrato para proporcionar un total de cinco sesións de formación aos empregados dun cliente cun custo de 10 000 por sesión de formación. Vostede factura ao cliente despois de cada sesión de formación. 

Cando configura as regras de facturación do contrato, usa os seguintes valores:

-   A unidade de entrega é unha sesión de formación.
-   O prezo unitario é de 10 000 por sesión de formación.
-   O número total de unidades é de cinco sesións de formación.

Cando remate unha sesión de formación, pode crear unha factura por 10 000 para a primeira unidade que se entregou e enviar a factura ao cliente.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a>Exemplo: Crear unha regra de facturación baseada nunha porcentaxe especificada de finalización do proxecto (cálculo manual)

A súa organización, unha empresa de consultoría de software, asina un contrato cun cliente para desenvolver parte dun produto que o cliente está a desenvolver. A súa organización acepta entregar o código do software nun período de seis meses. O cliente comprométese a pagar á súa organización un total de 100 000 polo traballo. Vostede crea unha regra de facturación para facturar ao cliente en función da porcentaxe de traballo finalizado no proxecto, segundo se especifica no contrato.

-   Ao final do primeiro mes, reúnese co cliente para determinar a porcentaxe de traballo realizado. Despois de que vostede e o cliente revisen o proxecto, decide que o proxecto está completado nun 15 por cento.
-   Vostede crea unha factura por 15 000 (15 por cento de 100 000) e envíaa ao cliente.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a>Exemplo: Crear unha regra de facturación baseada nunha porcentaxe especificada de finalización do proxecto (cálculo automático)

A súa organización, unha empresa de desenvolvemento de software, acepta desenvolver un paquete de contabilidade de nóminas para un cliente por 30 000. O cliente comprométese a pagar á súa organización segundo a porcentaxe do traballo finalizada. Vostede calcula que os custos do proxecto son 20 000. O contrato do proxecto especifica as categorías de traballo que vostede usa no proceso de facturación. Vostede configura regras de facturación que calculan automaticamente os importes da factura para a porcentaxe de traballo que se completa para cada categoría. Vostede configura un orzamento para cada categoría:

-   **Desenvolvemento** - Custo de 15 000 e ingresos de 20 000
-   **Instalación** - Custo de 5000 e ingresos de 10 000

Cando crea unha factura de cliente por primeira vez, o importe da factura calcúlase automaticamente en función da seguinte información:

-   Despois dun mes, o traballador do proxecto envía unha folla de control horario para o proxecto. O custo das horas do traballador é de 5000 para o desenvolvemento e 1000 para a instalación. Os traballos de desenvolvemento remataron nun 33 por cento (5000 de custo real/15 000 de custo orzamentario) e os traballos de instalación remataron nun 20 por cento (1000 de custo real/5000 de custo orzamentario).
-   O importe da factura de 8667 calcúlase automaticamente (33 por cento de 20 000 + 20 por cento de 10 000).
-   Vostede crea unha factura por 8667 e envíaa ao cliente.

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a>Exemplo: Crear unha regra de facturación baseada en fitos acordados

A súa organización, unha empresa de consultoría de xestión, acepta realizar investigacións de mercado para un produto de consumo que o cliente ten previsto vender. O cliente comprométese a utilizar os seus servizos durante un período de tres meses, a partir de marzo, e comprométese a pagarlle á organización 50 000. O proxecto ten tres fitos:

-   Fito 1: Recompilar datos de consumidores - 31 de marzo
-   Fito 2: Analizar os datos dos consumidores - 30 de abril
-   Fito 3: Presentar unha proposta de viabilidade do produto - 31 de maio

O cliente acepta pagarlle á súa organización 10 000 polo primeiro fito, 20 000 polo segundo e 20 000 polo terceiro. 

Cando configura o contrato do proxecto, acepta facturar ao cliente en función do fito completado. A configuración da regra de facturación inclúe os seguintes pasos:

-   Definir os fitos do proxecto.
-   Definir o importe que debe facturar ao cliente cando se complete cada fito.

Cando se completa o primeiro fito o 31 de marzo, vostede marca o fito como rematado e, a seguir, crea unha factura por 10 000 e envíaa ao cliente. Non pode crear unha factura para un fito ata que o marque como finalizado.

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a>Exemplo: Crear unha regra de facturación baseada en servizos máis unha tarifa de xestión

A súa organización, unha empresa de consultoría de xestión, acepta realizar investigacións de mercado para avaliar a viabilidade dun produto que o cliente, unha empresa de venda polo miúdo, está a desenvolver. Os termos do acordo especifican que proporcionará os servizos dos seus tres principais consultores de xestión, que realizarán a investigación en función do tempo e dos materiais. O cliente comprométese a pagar 100 por hora, máis unha tarifa de xestión do 10 por cento polas horas de consulta que se cargan ao proxecto. 

Cando configure o contrato do proxecto, cree unha regra de facturación para engadir unha tarifa de xestión do 10 por cento ás horas de consulta que se carguen ao proxecto. 

Cando crea unha factura para o cliente, factúrase ao cliente unha tarifa de xestión do 10 por cento máis o custo das horas de consultoría. Por exemplo, se os tres consultores traballaron un total de 200 horas no proxecto, créase unha factura por 22 000 baseada no seguinte cálculo:

-   200 horas a 100 por hora = 20 000
-   10 por cento de tarifa de xestión = 2 000
-   Importe total da factura = 22 000

Se as tarifas son tributables para un cliente e vostede selecciona un grupo de impostos sobre as vendas no contrato do proxecto, o grupo de impostos sobre as vendas introdúcese automaticamente nunha regra de facturación para as tarifas.

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a>Exemplo: Crear unha regra de facturación polo valor do tempo e dos materiais

A súa organización, unha empresa de consultoría de software, acepta proporcionar cinco consultores técnicos para traballar nun proxecto de desenvolvemento de software para un cliente durante os próximos seis meses. O cliente comprométese a pagar 150 por cada hora de consultoría, máis o custo do material de oficina. A súa organización envía unha factura ao cliente ao final de cada mes. 

Cando configura o contrato do proxecto, acepta facturar ao cliente cada mes o tempo e os materiais do proxecto. Crea unha regra de facturación que inclúe a seguinte información:

-   O período do contrato é de seis meses.
-   O tempo de consultoría calcúlase a un prezo de 150 por hora.
-   O material de oficina factúrase ao custo e o custo total do proxecto non debe superar os 10 000.
-   Vostede crea unha factura de cliente ao final de cada mes natural durante o proxecto.

Durante o primeiro mes, os consultores do proxecto rexistran un total de 800 horas. O custo do material de oficina que se carga ao proxecto é de 2.000. Polo tanto, a finais de mes crea unha factura por 122 000, que se calcula como 800 horas a 150 por hora, máis 2000 para material de oficina.



