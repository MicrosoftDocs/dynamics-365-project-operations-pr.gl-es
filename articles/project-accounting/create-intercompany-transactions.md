---
title: Crear transaccións entre empresas
description: Este artigo ofrece información sobre como crear transaccións entre empresas.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: da6fd8e0e6bfe2e2543f5c4a453ed769e412f1e9
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919368"
---
# <a name="create-intercompany-transactions"></a>Crear transaccións entre empresas

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

As transaccións entre empresas son transaccións de tempo e gasto dun contrato de proxecto que pertencen a unha empresa ou unidade organizativa, mentres que os recursos do contrato de proxecto forman parte dunha empresa ou unidade organizativa diferente.

Cando se aproba unha transacción entre empresas, créanse as seguintes transaccións reais

| **Tipo de transacción** | **Lista de prezos aplicada** | **Moeda da transacción** |
| --- | --- | --- |
| Custo | Lista de prezos de custo da unidade de contratación | Moeda na liña de prezos |
| Vendas sen facturar. Estes créanse só para os datos reais asociados a unha liña de contrato co tipo de facturación, a hora e o material. | Lista de prezos de vendas do proxecto do contrato | Moeda do contrato |
| Custo da unidade de recursos | Lista de prezos de custo da unidade de recursos | Moeda na liña de prezos |
| Vendas da unidade entre organizacións | Lista de prezos de custo da unidade de contratación | Moeda na liña de prezos |

O custo, o custo unitario do recurso e os prezos e moeda das transaccións de venda de unidade entre organización están dirixidos pola **unidade organizativa**. É importante lembrar isto ao decidir como estruturar empresas e unidades organizativas na súa implementación.

Cando crea rexistros de oportunidade, oferta, contrato de proxecto e proxecto, o sistema verifica que a moeda da unidade contratante coincide coa moeda contable da empresa contratante. Cando non son a mesma, estes rexistros non se poden crear. A moeda da unidade organizativa defínese en Dynamics 365 Project Operations ao ir a **Dataverse** > **Configuración** > **Unidades organizativas**. A moeda contable dunha empresa defínese en Dynamics 365 Finance indo a **Contabilidade Xeral** > **Configuración do libro maior** > **Libro maior**. A moeda sincronízase co seu ambiente de Dataverse ambiente mediante o mapa de Escritura dobre de libro maior.

O sistema crea o custo da unidade de recursos e as vendas da unidade entre organizacións nas seguintes situacións:

  - Cando a unidade de recursos difire da unidade contratante
  - Cando a empresa de recursos difire da empresa contratante

Non obstante, só as transaccións que teñan unha empresa de recursos diferente da empresa contratante serán transferidas ao contorno Dynamics 365 Finance para a contabilidade adicional.

A contabilidade dos datos reais do proxecto rexístrase no diario de integración de Project Operations en Finance. O sistema crea as seguintes liñas de diario.

| **Tipo de transacción** | **Entidade legal** | **Crea unha transacción do proxecto na contabilización** | **Dimensións financeiras predefinidas de** | **Grupo de impostos sobre vendas de facturación predefinido e grupo de impostos sobre vendas individuais de facturación** |
| --- | --- | --- | --- | --- |
| Custo | Non se engade ao diario de integración | N\A | N\A | N\A |
| Vendas sen facturar | O diario de integración da entidade legal prestameira | Si | Project | **Grupo de impostos sobre vendas de facturación**: Baseado no **cliente do contrato** <br/> **Grupo de impostos sobre as vendas de facturación**: Da categoría de proxecto da entidade legal actual na liña de diario |
| Custo da unidade de recursos | Diario de integración da entidade legal prestamista | No | Cliente entre empresas | **Grupo de impostos sobre vendas de facturación**: Baseado no **cliente entre empresas** <br/> **Grupo de impostos sobre as vendas de facturación**: Da categoría de proxecto da entidade legal actual na liña de diario |
| Vendas entre organizacións | Diario de integración da entidade legal prestamista | No | Cliente entre empresas | **Grupo de impostos sobre vendas de facturación**: Baseado no **cliente entre empresas** <br/> **Grupo de impostos sobre as vendas de facturación**: Da categoría de proxecto da entidade legal actual na liña de diario |

### <a name="example-intercompany-transactions"></a>Exemplo: Transaccións entre empresas

Molly Clark, programadora empregada en GBPM, rexistra 10 horas de traballo contra un proxecto de USPM Adventure Works, aprobadas polo director do proxecto. O custo da programadora en GBPM é de 88 GBP por hora. GBPM facturará a USPM 120 USD por hora de programador. USPM facturará ao cliente Adventure Works 200 USD polo traballo realizado polo recurso de GBPM. Para obter máis información, consulte [Configurar facturación entre empresas](configure-intercompany-invoicing.md).

1. En Project Operations, vaia a **Recursos** e seleccione **Molly Clark** na lista. No separador **Programación**, no campo **Empresa**, seleccione **GBPM**.
2. Vaia a **Vendas** > **Clientes** e seleccione **Novo** para crear un novo rexistro de cliente para Adventure Works.
    1. Estableza a empresa en **USPM**.
    2. Estableza **Tipo de relación** en **Cliente**.
    3. Seleccione **Grupo de clientes 10 - Nacional**.
    4. Estableza a moeda en **USD**.
    5. Garde o rexistro.
3. Vaia a **Vendas** > **Contratos de proxecto** e cree un novo contrato de proxecto para Adventure Works.
    1. Estableza a empresa propietaria en **USPM** e a unidade contratante en **Contoso Robotics US**.
    2. Seleccione Adventure Works como cliente.
    3. Seleccione unha lista de prezos de produtos e garde o rexistro.
    4. No separador **Liñas de contrato**, cree unha nova liña de contrato. Estableza calquera nome e seleccione **Tempo e materiais** como método de facturación.
    5. Cree un novo proxecto e asócieo a esta liña de contrato.
4. Inicie sesión como o recurso, **Molly Clark**. Vaia a **Proxectos** > **Entradas de tempo** e cree unha entrada de tempo para o proxecto Adventure Works.
5. Inicie sesión como xestor de proxectos. Vaia a **Proxectos** > **Aprobacións** e aprobe a transacción de entrada de tempo rexistrada por Molly Clark.
6. Vaia ao proxecto Adventure Works e seleccione **Relacionado** > **Datos reais**. Créanse as seguintes transaccións de datos reais.

| **Tipo de transacción** | **Prezo** | **Moeda da transacción** | **Importe** |
| --- | --- | --- | --- |
| Custo | 120 | USD | 1200 |
| Vendas sen facturar | 200 | USD | 2000 |
| Custo da unidade de recursos | 88 | GBP | 880 |
| Vendas da unidade entre organizacións | 120 | USD | 1200 |

7. Inicie sesión como contable de USPM. Abra a instancia de Finance de Project Operations e seleccione a empresa **USPM**. 
8. Vaia a **Xestión e contabilidade de proxectos** > **Periódico** > **Project Operations on Customer Engagement** > **Importar desde transición** e seleccione executar o proceso periódico. Este proceso periódico encherá o diario de integración Project Operations.
9. Vaia a **Xestión e contabilidade de proxectos** > **Diarios** > **Diario de integración de Project Operations** e repase as liñas do diario. O sistema crea a seguinte liña de diario.

    | **Tipo de transacción** | **Prezo** | **Moeda da transacción** | **Importe** |
    | --- | --- | --- | --- |
    | Vendas sen facturar | 200 | USD | 2000 |

    Se o sistema está configurado para acumular ingresos por este proxecto, contabilízase o seguinte:

    - Débito: Proxecto - Valor de vendas de WIP 200 USD
    - Crédito: Proxecto - Ingresos acumulados 200 USD

    Esta venda sen facturar xa está lista para a facturación. A factura do cliente Adventure Works pode contabilizarse financeiramente cando sexa necesario.

10. Inicie sesión como contable de **GBPM**. Abra a instancia de Finance de Project Operations e abra a empresa **GBPM**. 
11. Vaia a **Xestión e contabilidade de proxectos** > **Periódico** > **Integración de Project Operations** > **Importar da táboa de transición** e execute o proceso periódico para encher o diario de integración de Project Operations.
12. Vaia a **Xestión e contabilidade de proxectos** > **Diarios** > **Diario de integración de Project Operations** e repase as liñas. O sistema crea as seguintes liñas.

    | **Tipo de transacción** | **Prezo** | **Moeda da transacción** | **Importe** |
    | --- | --- | --- | --- |
    | Custo da unidade de recursos | 88 | GBP | 880 |
    | Vendas da unidade entre organizacións | 120 | USD | 1200 |

    A contabilización destes rexistros orixina as seguintes transaccións de vales:

    - Débito: Custo do proxecto 88 GBP
    - Crédito: Asignación de nóminas 88 GBP

    Se o sistema está configurado para acumular ingresos entre empresas, contabilízase o seguinte:

    - Débito: Proxecto - Valor de vendas de WIP 120 USD
    - Crédito: Proxecto - Ingresos acumulados 120 USD

    O sistema xa está preparado para crear unha factura de cliente entre empresas.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
