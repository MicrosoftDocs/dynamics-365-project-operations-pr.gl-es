---
title: Configurar a contabilidade para proxectos facturables
description: Este artigo ofrece información sobre as opcións de contabilidade para proxectos facturables.
author: sigitac
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5020c978f0667543aed2b373d262dcda9688b02c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916424"
---
# <a name="configure-accounting-for-billable-projects"></a>Configurar a contabilidade para proxectos facturables

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

Dynamics 365 Project Operations admite varias opcións de contabilidade para proxectos facturables que inclúen transaccións de tempo e material e prezo fixo.

- **Transaccións de tempo e material**: Estas transaccións factúranse a medida que avanza o traballo en función do consumo de horas, gastos, elementos ou taxas do proxecto. Estes custos de transacción poden combinarse cos ingresos de cada transacción e o proxecto factúrase a medida que avanza o traballo. Os ingresos do proxecto tamén se poden acumular no momento en que se produce a transacción. Durante a facturación, recoñécense os ingresos e, se é o caso, revértense os ingresos acumulados.
- **Transaccións de prezo fixo**: Estas transaccións factúranse segundo un programa de facturación baseado nun contrato de proxecto.. Os ingresos por transaccións a prezo fixo pódense recoñecer na facturación ou calcularse e contabilizarse periodicamente, segundo os métodos de **Contrato completado** ou **Porcentaxe completada**.

Un proxecto considérase facturable cando está asociado a unha ou máis liñas de contrato. Unha liña de contrato de proxecto define por si mesma que método de facturación e tipos de transaccións están permitidos.

Por exemplo, Fabrikam Robotics gañou un contrato de proxecto coa corporación Adatum para a optimización de equipos. Adatum pagará unha cantidade fixa de 10 000 USD para cubrir os gastos incorridos do proxecto. Este é un método de facturación de prezo fixo O tempo e as taxas do proxecto facturaranse por uso. Este é un método de facturación de tempo e material. Todo o traballo rastrexarase nun único proxecto chamado optimización de equipos de Adatum.

Un membro do equipo do proxecto envía oito horas de traballo no proxecto de optimización de equipos de Adatum. Cando o xestor do proxecto aproba este tempo, o sistema usa o método de facturación de tempo e material para crear transaccións reais, unha factura e unha conta. Esta transacción non se incluirá no cálculo da estimación dos ingresos de prezo fixo.

Outro membro do equipo do proxecto envía un gasto de viaxe por 2000,00 USD contra o proxecto de optimización de equipos de Adatum. Cando o xestor do proxecto aproba este envío, o sistema usa o método de facturación de prezo fixo para crear transaccións reais e unha conta para este gasto do proxecto. Non se facturará ao cliente en función desta transacción. Pola contra, facturaranse mediante fitos de facturación configurados por separado. Esta transacción de gasto, xunto coas estimacións de gastos, incluirase no cálculo da estimación dos ingresos de prezo fixo.

Os principios contables para as transaccións do proxecto defínense nos perfís de custos e ingresos do proxecto. Para cada transacción do proxecto, o sistema determina o perfil de custo e ingresos do proxecto empregando as regras do perfil de custo e ingresos do proxecto configuradas.

## <a name="define-project-cost-and-revenue-profiles"></a>Definir os perfís de custo e ingresos do proxecto 

Os perfís de custos e ingresos do proxecto determinan as regras de contabilidade para as transaccións do proxecto. Estes perfís configúranse na xestión e a contabilidade do proxecto. 

Complete os seguintes pasos para crear un novo perfil de custo e ingresos do proxecto. 

1. Vaia a **Xestión e contabilidade do proxecto** > **Configuración** > **Publicación** > **Perfís de custo e ingresos do proxecto**. 
2. Seleccione **Novo** para crear un novo perfil de custo e ingresos do proxecto.
3. No campo **Nome**, introduza o nome e unha breve descrición do perfil.
4. No campo **Método de facturación**, seleccione **Tempo e material** ou **Prezo fixo**.
5. Expanda o separador rápido **Libro maior**. Os campos deste separador definen os principios de contabilidade que se utilizan cando as transaccións do proxecto se rexistran mediante o diario de integración de Project Operations e logo se facturan a través da proposta de factura do proxecto.
6. Seleccione a información adecuada nos campos seguintes no separador rápido **Libro maior**:

    - **Contabilizar custos - hora**:

       - *Sen libro maior*: O custo das transaccións por tempo non se contabilizará no libro maior cando se contabilice o diario de integración de Project Operations. Non obstante, o contable pode contabilizar custos utilizando a función Contabilizar custos máis tarde.
       - **Saldo**: O custo das transaccións de tempo cargarase no tipo de conta de libro maior, *WIP - Valor de custo* e na *Conta de asignación de nóminas* na configuración de contabilización do libro maior. O contable utilizará a función de contabilizar custos para mover periodicamente este custo dunha conta de saldo a unha conta de resultados.
       - **Resultados**: Ao publicar o diario de integración de Project Operations, o custo da transacción de tempo cargarase no tipo de conta de libro maior *Custo* e na *Conta de asignación de nóminas* definida no separador **Custo** na páxina **Configuración contabilización de libro maior** (**Xestión e contabilidade de proxectos** \> **Configuración** \> **Contabilización** \> **Configuración de contabilización de libro maior**). Esta é a configuración máis frecuente para transaccións de tempo e material.
        - *Nunca libro maior*: O custo das transaccións de tempo nunca se contabilizará no libro maior.

    - **Contabilizar custos – gasto**:

         - **Saldo**: Ao publicar o diario de integración de Project Operations, o custo da transacción do gasto cargarase no tipo de conta de libro maior *WIP - Valor de custo* como se define no separador **Custo** na páxina **Configuración de contabilización de libro maior** e na acreditada na conta de compensación na liña de diario. As contas compensadas predefinidas para gastos defínense en **Xestión e contabilidade de proxectos** > **Configuración** \> **Contabilización** \> **Conta compensada por defecto para gastos**. O contable utilizará a función de **Contabilizar custos** para mover periodicamente este custo dunha conta de saldo a unha conta de resultados.
        - **Resultados**: Ao publicar o diario de integración de Project Operations, o custo da transacción do gasto cargarase no tipo de conta de libro maior *Custo* como se define no separador **Custo** na páxina **Configuración de contabilización de libro maior** e na acreditada na conta de compensación na liña de diario. As contas compensadas predefinidas para gastos defínense en **Xestión e contabilidade de proxectos** \> **Configuración** \> **Contabilización** \> **Conta compensada por defecto para gastos**.
      
    - **Contabilizar custos - elemento**:

         - **Saldo**: Ao contabilizar o diario de integración de Project Operations, o custo da transacción do elemento cargarase no tipo de conta Libro maior *WIP - Valor de custo - elemento* como se define no separador **Custo** na páxina **Configuración de contabilización de libro maior** e pagarase da seguinte maneira:
    
              - Para o documento de tipo uso: Conta **Custo - elemento** na **Configuración de contabilización de libro maior**.  
              - Para o documento de tipo compra: **Conta de integración de adquisicións** nos **Parámetros de xestión e contabilidade de proxectos**.
           O contable utilizará a función de **Contabilizar custos** para mover periodicamente este custo dunha conta de saldo a unha conta de resultados.
        - **Ganancias e perdas**: Ao contabilizar o diario de integración de Project Operations, o custo da transacción do elemento cargarase no tipo de conta Libro maior *WIP - Valor de custo - elemento* como se define no separador **Custo** na páxina **Configuración de contabilización de libro maior** e pagarase da seguinte maneira:
         
             - Para o documento de tipo uso: Conta **Custo - elemento** na **Configuración de contabilización de libro maior**.  
             - Para o documento de tipo compra: **Conta de integración de adquisicións** nos **Parámetros de xestión e contabilidade de proxectos**.
       
    - **Facturación en conta**:

        - **Saldo**: Ao contabilizar a proposta de factura do proxecto, pagarase unha transacción na conta (fito de facturación) no tipo de conta de libro maior *WIP facturado - en conta* como se define no separador **Ingresos** na páxina **Configuración de contabilización de libro maior** e cargarase na conta de saldo do cliente.
         - **Resultados**: Ao contabilizar a proposta de factura do proxecto, pagarase unha transacción na conta (fito de facturación) no tipo de conta de libro maior *Ingresos facturados - en conta* como se define no separador **Ingresos** na páxina **Configuración de contabilización de libro maior** e cargarase na conta de saldo do cliente. As contas de saldo de clientes defínense en **Contas pendentes de cobro** \> **Configuración** \> **Perfís de contabilización de clientes**.

   Cando defina os perfís de contabilización dos métodos de facturación de tempo e material, ten a opción de acumular ingresos por tipo de transacción (hora, gasto, elemento e taxa). Se a opción **Acumular ingresos** a opción está definida como **Si**, as transaccións de vendas sen facturar no diario de integración de Project Operations rexistraranse no libro maior. O valor de vendas cárgase en **WIP - conta de valor de vendas** e págase na conta **Ingresos acumulados - valor de vendas** que se configurou na páxina **Configuración de contabilización de libro maior**, no separador **Ingresos**. 
  
  > [!NOTE]
  > A opción **Acumular ingresos** está dispoñible só cando o tipo de transacción respectivo **Custo** contabilízase na conta de resultados.
    
7. Expanda o separador rápido **Estimaciónr**. Os campos deste separador definen a configuración de cálculo para estimacións de ingresos de prezo fixo. Os campos deste separador só se aplican aos perfís de custos e ingresos do proxecto cun método de facturación de **Prezo fixo**.
8. Seleccione a información adecuada nos campos seguintes no separador rápido **Estimación**:

    - **Principio empregado para os cálculos de finalización do proxecto**:

        - **Contrato finalizado**: A correspondencia de custos e o recoñecemento de ingresos non se producen ata o final do proxecto. Os custos reflíctense como WIP no saldo ata que o proxecto estea completo.
        - **Porcentaxe finalizada**: Os ingresos acumulados calcúlanse e contabilízanse no libro maior cada período en función da porcentaxe de finalización do proxecto. Hai varios métodos dispoñibles para calcular a porcentaxe de finalización. Estes métodos poden ser automáticos en función da configuración ou manuais.
        - **Sen WIP**: Esta configuración úsase para proxectos de prezo fixo cun período de tempo curto e onde a factura e os custos se producen no mesmo período. Neste caso, o valor do campo **Facturación en conta** no separador rápido **Libro maior** configúrase automaticamente en **Resultados** para garantir que os ingresos se recoñecen na facturación. O proceso de estimación de ingresos non se utilizará para este perfil de custos e ingresos do proxecto.

    - **Principio de correspondencia**: Este campo determina como se contabilizará no libro maior o valor de vendas calculado (ingresos acumulados).

        - Usando o principio de **Valor das vendas**, o sistema calculará o valor das vendas facendo coincidir os custos e os ingresos e logo contabilizándoo como un importe único.
        - Usando o principio de **Produción e beneficio**, o sistema dividirá o valor das vendas en custos realizados e beneficio calculado. Estes contabilízanse por separado.

    - **Modelos de custos**: Permitir agrupar as transaccións do proxecto en función do tipo de transacción e a categoría do proxecto e definir as regras de cálculo de finalización porcentual para estes grupos.
    - **Códigos de período**: Definir a frecuencia coa que se calculan as estimacións de ingresos para un determinado perfil de custos e ingresos de proxecto.
    - **Categorías para estimación**: Úsase para contabilizar o valor das vendas (ingresos acumulados) nas transaccións do proxecto. Primeiro, configure a categoría de proxecto dedicado para un tipo de transacción **Taxa** e logo configure o indicador **Estimación** para esta categoría de proxecto. A seguir, dependendo do principio de coincidencia seleccionado, escolla esta categoría de proxecto no valor **Vendas** ou o campo **Beneficio** no perfil de custos e ingresos do proxecto.

### <a name="sample-configurations-for-project-cost-and-revenue-profiles"></a>Exemplos de configuracións para perfís de custos e ingresos do proxecto

Tempo e materiais - sen WIP

![Perfil de custos e ingresos: tempo e materiais - sen WIP.](media/time-material-no-wip.png)

Tempo e materiais – WIP (ingresos)

![Perfil de custos e ingresos: tempo e materiais - WIP.](media/time-material-with-wip.png)

Prezo fixo - Sen WIP

![Perfil de custos e ingresos: prezo fixo - sen WIP.](media/fixed-price-no-wip.png)

Prezo fixo - contrato finalizado

![Perfil de custos e ingresos: prezo fixo - contrato finalizado.](media/fixed-price-completed-contract.png)

Prezo fixo - porcentaxe de finalización

![Perfil de custos e ingresos: prezo fixo - porcentaxe de finalización.](media/fixed-price-completed-percentage.png)


## <a name="accounting-event-examples-for-sample-project-cost-and-revenue-profiles"></a>Exemplos de eventos de contabilidade para perfís de custos e ingresos do proxecto.

| Evento de contabilidade                  | Tempo e material - Sen WIP                       | Tempo e material - WIP                                                                                           | Prezo fixo - sen WIP                                            | Prezo fixo - Contrato finalizado                                                                            | Prezo fixo - Porcentaxe de finalización                             |
|-----------------------------------|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| Diarización de transaccións de tempo    | Débito - Custo <br>Crédito –Asignación de nóminas          | Débito - Custo <br>Crédito –Asignación de nóminas <br>Débito – Valor de vendas WIP <br>Crédito - Valor de vendas de ingresos acumulados                | Débito - Custo <br>Crédito –Asignación de nóminas                         | Débito - Custo <br>Crédito – Asignación de nóminas                                                                    | Débito - Custo <br>Crédito – Asignación de nóminas                       |
| Diarización de transaccións de gasto | Débito - Custo <br>Crédito - Conta compensada para gastos | Débito - Custo <br>Crédito - Conta compensada para gastos <br>Débito – Valor de vendas WIP <br>Crédito - Valor de vendas de ingresos acumulados      | Débito - Custo <br>Crédito - Conta compensada para gastos                 | Débito - Custo<br> Crédito - Conta compensada para gastos                                                            | Débito - Custo <br>Crédito - Conta compensada para gastos               |
| Facturación ao cliente                | Débito – Saldo de cliente <br>Crédito - ingresos facturados | Débito – Saldo de cliente <br>Crédito - Ingresos facturados <br>Crédito - Valor de vendas WIP Débito - Valor de vendas de ingresos acumulados | Débito – Saldo de cliente <br>Crédito - Ingresos facturados - en conta | Débito – Saldo de cliente <br>Crédito - WIP - Facturado en conta                                                  | Débito – Saldo de cliente <br>Crédito - WIP - Facturado en conta    |
| Contabilizar estimación de ingresos             | Non aplicable                                   | Non aplicable                                                                                                    | Non aplicable                                                  | Débito - Valor de custo WIP <br>Crédito – Custo                                                                         | Débito – WIP - Valor de vendas <br>Crédito - Valor de vendas de ingresos acumulados |
| Eliminar                         | Non aplicable                                   | Non aplicable                                                                                                    | Non aplicable                                                  | Crédito - Valor de custo WIP <br>Débito - Custo <br>Crédito - Ingresos acumulados - Valor de vendas <br>Débito - WIP - Facturado en conta | Débito - WIP - Facturado en conta <br>Débito – WIP Valor de vendas     |

## <a name="configure-project-cost-and-revenue-profile-rules"></a>Configurar as regras do perfil de custos e ingresos do proxecto

As regras do perfil de custos e ingresos do proxecto determinan o perfil de custos e ingresos do proxecto que se deben empregar ao procesar calquera transacción facturable do proxecto. Defina as regras indo a **Xestión e contabilidade de proxectos** \> **Configuración** \> **Contabilización** \> **Regras do perfil de custos e ingresos do proxecto**.

As regras poden definirse por contrato de proxecto, grupo de proxectos ou por un proxecto específico. O sistema sempre escollerá a regra de granularidade máis alta primeiro.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
