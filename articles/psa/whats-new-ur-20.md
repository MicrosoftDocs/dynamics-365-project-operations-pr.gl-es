---
title: Novidades ou cambios na versión 20 de actualización de Project Service Automation, V3
description: Este tema mostra as funcionalidades e correccións que están dispoñibles la versión 20 de actualización de Project Service Automation, V3
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 124dad5438f9489d1ddbc952cecaee977b6b7f01
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949092"
---
# <a name="project-service-automation-update-release-20-v3"></a>Versión 20 de actualización de Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Comprácenos anunciar a última actualización da aplicación Project Service Automation para Dynamics 365. Esta versión inclúe algunhas melloras importantes na calidade, rendemento e facilidade de uso. Esta versión é compatible con Dynamics 365 9.x. Para actualizar a esta versión, visite a paxina de solucións do Centro de administración para Dynamics 365 en liña para instalar a actualización. Para obter máis información, consulte [Instalar, actualizar ou eliminar unha solución preferida](/power-platform/admin/install-remove-preferred-solution)

Este tema mostra as funcionalidades e correccións que son novas ou modificadas para Project Service Automation V3, versión 20 de actualización. Esta versión ten un número de compilación de V 3.10.31.37 e está xeralmente dispoñible a través dunha actualización automática en xuño de 2020.

## <a name="update-release-20"></a>Versión 20 de actualización

### <a name="bug-fixes"></a>Correccións de erros

**Xestión de proxectos**

Resolvéronse os seguintes problemas:

- A importación dos membros do equipo do proxecto cun método de atribución que require horas ten como resultado unha mensaxe de erro pouco clara cando as horas especificadas son cero.
- Os usuarios reciben un erro incorrecto cando se introduciu o número máximo de caracteres no campo **Descrición** para unha tarefa de proxecto.
- A páxina **Descarga de complementos de Microsoft Dynamics 365 Project Service Automation** redirixe á páxina de descarga en inglés cando a configuración de idioma do usuario está definida en xaponés.
- Cando se produce un erro no servidor, a etiqueta de sincronización no separador **Programar** do formulario **Proxectos** permanece ás veces.
- As actualizacións de tarefas redundantes envíanse ao servidor cando se modifica unha tarefa.

**Sales**

Resolvéronse os seguintes problemas:

- No formulario **Contrato**, ao premer dúas veces **Crear factura** créanse dúas facturas para un único rexistro de datos reais.
- En Internet Explorer 11, os usuarios non poden crear entradas de gastos.
- A inversión do custo e a inversión dos datos reais de vendas non facturadas non están ligadas.
- O botón **Actualizar datos reais** no formulario **Proxecto** non actualiza **Horario real da tarefa**.
- O suplemento **PreValidateProjectTeamMemberCreate** pode crear recursos xenéricos duplicados reservables cando o atributo **msdyn_isgenericresourceprojectscoped** está configurado en **Falso**.
- **Calcular de novo** limpa os custos imputables dos detalles da liña de oferta baseada nos produtos e os detalles da liña de contrato.
- En escenarios específicos, o suplemento **PostEstimateLineUpdate** mostra un erro de excepción de referencia nula.
- A duración da fase de tempo na **Gráfica de análise da rendibilidade** non coincide coa duración dos custos no detalle da liña de oferta de prezo fixo da oferta.
- Os valores de unidade e grupos de unidades non aparecen de forma predeterminada correctamente para as categorías de gasto nos formularios **Detalles da liña de contrato** e **Detalles da liña de oferta**.
- As listas de **Prezo de custo da unidade organizativa** permiten solapamentos na data de validez.
- Os usuarios non teñen permiso para cambiar **OrgUnit** cando o tipo de pedido non está baseado en traballo, porque levará a un erro de excepción de referencia nula.
- Ao intentar navegar desde o formulario **Detalles da liña de oferta**, ao volver ao separador **Oferta**, o formulario actualízase e mostra o separador **Resumo**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]