---
title: Novidades de novembro de 2020 - Project Operations para situacións baseadas en recursos/sen fornecemento
description: Este tema ofrece información sobre as actualizacións de calidade dispoñibles na versión de novembro de 2020 de Project Operations para situacións baseadas en recursos/sen fornecemento.
author: sigitac
ms.date: 10/30/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9eda9d75f5a4d71e6e4b8bd22dce973270639db3f927ac6a76be5b3c4303fc31
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007954"
---
# <a name="whats-new-november-2020---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades de novembro de 2020 - Project Operations para situacións baseadas en recursos/sen fornecemento

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Este tema aplícase aos seguintes compoñentes e versións de Dynamics 365 Project Operations:

- Project Operations en ambiente de CDS versión 4.4.0.70
- Xestión e contabilidade de proxectos en ambiente de Dynamics 365 Finance versión 10.0.14

## <a name="updates-to-project-operations-for-resource-non-stocked-based-scenarios"></a>Actualizacións de Project Operations para situacións baseadas en recursos/sen fornecemento

### <a name="project-operations-on-cds"></a>Project Operations en CDS

| Área de funcionalidades                 | Número de referencia | Actualización de calidade                                                                                                                                                                    |
|------------------------------|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   Xestión de oportunidades       | 2036993          | A liña de estimación e as liñas de contrato de atribución de recursos actualízanse nas ofertas gañadoras cando o tipo de liña de oferta é **Todas as tarefas**.                                                 |
| Facturación e prezos          | 2070392          | As liñas de contrato do proxecto na factura aumentan cada vez que se selecciona **Actualizar transaccións de facturas**.                                                                         |
| Planificación de proxectos             | 2043336          | Non se puido eliminar un rexistro de membro do equipo do proxecto.                                                                                                                                  |
| Planificación de proxectos             | 2046013          | Comportamento incoherente para as columnas de etiquetas de estimacións durante a carga fronte ao cambio de tipo de fase de tempo.                                                                                   |
| Planificación de proxectos             | 2046647          | As horas de inicio e finalización están desactivadas nunha hora cando os membros do equipo do proxecto xeran requisitos de recursos.                                                                      |
| Planificación de proxectos             | 2053879          | (Segundo o próximo lanzamento de CDS) PublishUnassignedAssignments rompe un intento de gardar unha tarefa cando o erro "O valor que se pasou para ConditionOperator.In está baleiro."                       |
| Planificación de proxectos             | 2055501          | Deixar a **Data de inicio do proxecto** baleira provoca un fallo na programación.                                                                                                      |
| Planificación de proxectos             | 2066817          | Non se pode crear un recurso xenérico usando o selector de persoas do separador **Tarefas**.                                                                                                   |
| Planificación de proxectos             | 2067034          | O botón **Ver detalles** non está dispoñible na páxina **Detalles da tarefa**.                                                                                                       |
| Xestión de recursos          | 2046667          | Os membros xenéricos do equipo non se eliminan aínda que se cumpran todos os recursos.                                                                                                    |
| Entrada rápida de tempo e gasto | 2047499          | O botón **Novo** da páxina de entrada de tempo abre a páxina **Nova sinatura de correo electrónico**.                                                                                               |
| Entrada rápida de tempo e gasto | 2059859          | Ábrese unha ventá emerxente inesperada ao crear unha entrada de gasto.                                                                                                                         |
| Outras                        | 2044181          | (Desinstalación do pedido de compra)   Cando se intentan desinstalar as solucións básicas msdyn_ProjectServiceCore_Patch e msdyn Project   service, prodúcese o erro "O rexistro non está dispoñible".  |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Xestión e contabilidade de proxectos en Dynamics 365 Finance

| Área de funcionalidades        | Número de referencia | Actualización de calidade                                                                                                                                                            |
|---------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Recoñecemento de ingresos | [451662](https://fix.lcs.dynamics.com/Issue/Details/?bugId=451662)           | A porcentaxe de estimación do proxecto finalizado é incorrecta cando o contrato usa unha moeda estranxeira e a porcentaxe de progreso do traballo para o método de finalización.                     |
| Recoñecemento de ingresos | [469894](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469894)           | Non se poden contabilizar estimacións co método de finalización de **Custo real**.                                                                                                    |
| Recoñecemento de ingresos | [485439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485439)           | A eliminación falla debido a un erro de desequilibrio do vale cando a moeda da empresa e a moeda da transacción son diferentes.                                              |
| Xestión de gastos  | [456882](https://fix.lcs.dynamics.com/Issue/Details/?bugId=456822)           | Para usuarios que non sexan administradores, os valores de busca para columnas de liña de gasto como **ID do proxecto** e **Categoría de gasto** non se amosan correctamente no marco do conector de datos. |
| Xestión de gastos  | [469300](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469300)           | O valor predefinido de propiedade da liña non se mostra para as categorías de gasto.                                                                                                         |
| Xestión de gastos  | [469302](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469302)           | A integración de gasto debe incluír a propiedade de liña do informe de gastos.                                                                                             |
| Facturación           | [462499](https://fix.lcs.dynamics.com/Issue/Details/?bugId=462499)           | Non se poden contabilizar propostas de factura do proxecto debido a unha mensaxe de erro que di que a combinación de FD non foi validada.                                                    |
| Facturación           | [470614](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470614)           | Non se poden ver as transaccións desde a páxina de detalles da **factura**.                                                                                                              |
| Facturación           | [480070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480070)           | Pódense eliminar as liñas da proposta de factura.                                                                                                                                  |
| Contabilidade de proxectos  | [470293](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470293)           | Os elementos do menú **Previsión** non son visibles na páxina de lista **Proxectos**.                                                                                                   |
| Contabilidade de proxectos  | [475873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475873)           | Non se pode abrir **Declaración do proxecto**   > **Transaccións e previsión**.                                                                                                       |
| Contabilidade de proxectos  | [475879](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475879)           | **Axustar contabilidade** non está activado para transaccións de proxectos facturados.                                                                                                  |
| Contabilidade de proxectos  | [480962](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480962)           | Os datos de contabilidade non están incluídos na táboa **ProjCDSActualsImport** cando o diario de **Integration** se contabiliza.                                                  |
| Contabilidade de proxectos  | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558)           | A entrada de previsión do proxecto duplícase cando se elimina e despois se le unha atribución de recursos.                                                                            |
| Contabilidade de proxectos  | [502019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=502019)           | Ao seleccionar unha ligazón de ID de proxecto non se abre o URL da ligazón profunda do CDS.                                                                                                         |
| Contabilidade de proxectos  | [505458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505458)           | Non se pode actualizar a data de inicio dunha tarefa en CDS.                                                                                                                           |
| Contabilidade de proxectos  | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041)           | Activando a funcionalidade, non son posibles varias liñas de contrato sen a integración de CDS.                                                                                   |

### <a name="regulatory-updates"></a>Actualizacións normativas
Para obter información sobre actualizacións normativas para aplicacións de Finance and Operations, vexa [Actualizacións normativas](/dynamics365/finance/localizations/regulatory-updates). Tamén pode iniciar sesión en LCS e ver as actualizacións normativas previstas usando a ferramenta de busca de problemas. A busca de problemas permítelle buscar por país, tipo de funcionalidade e lanzamento.


[!INCLUDE[footer-include](../includes/footer-banner.md)]