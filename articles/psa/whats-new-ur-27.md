---
title: Novidades ou cambios na versión 27 de actualización de Project Service Automation, V3
description: Este artigo enumera as funcións e correccións dispoñibles na actualización de Project Service Automation, versión 27, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 6c8f4f736f0659f9b6db25f4685ef1278c45d034
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912928"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-27-v3"></a>Novidades ou cambios na versión 27 de actualización de Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Comprácenos anunciar a última actualización da aplicación Project Service Automation para Dynamics 365. Esta versión inclúe algunhas melloras importantes na calidade, rendemento e facilidade de uso. Esta versión é compatible con Dynamics 365 9.x. Para actualizar a esta versión, visite a paxina de solucións do Centro de administración para Dynamics 365 en liña para instalar a actualización. Para obter máis información, consulte [Instalar, actualizar ou eliminar unha solución preferida](/power-platform/admin/install-remove-preferred-solution)

Este artigo enumera as funcións e correccións que son novas ou modificadas para Project Service Automation V3, actualización 27. Esta versión ten un número de compilación de V3.10.45.98 e está dispoñible xeralmente a través dunha autoactualización desde xaneiro de 2021.

## <a name="update-release-27"></a>Versión 27 de actualización

### <a name="bug-fixes"></a>Correccións de erros

**Xeral**

Resolvéronse os seguintes problemas:

- Os rexistros xerados polos complementos en Project Service Automation non se configuraron para eliminarse automaticamente.
- A actualización automática falla porque a solución Project Service Automation contén un elemento de título e NavBarArea nulos herdados.

**Tempo e gasto**

Resolvéronse os seguintes problemas:

- A grade **Entrada de tempo** mostra datos incorrectos para o comportamento da data de **Zona horaria independente**.
- A grade **Entrada de tempo** crea un tempo incorrecto para o comportamento da data de **Zona horaria independente**.
- A busca de tarefas non se limita ao proxecto seleccionado na páxina **Editar entrada de tempo**.
- A aprobación do tempo para as entradas de tempo que non sexan do proxecto bloquéase porque o sistema está a buscar un responsable de aprobación de proxecto.
- As entradas correctas en Datos reais amosan unha mensaxe de erro incorrecta.
- Cando unha tarefa contén un valor nulo para o custo real e os totais do proxecto actualízanse, prodúcese o seguinte erro: "A clave indicada non está presente no dicionario".
- En casos específicos, os filtros **Agrupar por** no separador **Estimación do proxecto** non mostra as estimacións de gastos.
- O intervalo **Horario de verán** non é correcto para as entradas de tempo.

**Xestión de proxectos**

Resolvéronse os seguintes problemas:

- Melloras na caché, que mellora o rendemento relacionado coa carga da páxina **Proxecto**.
- Regra de negocio obsoleta que impide completar as tarefas do proxecto.
- Os contornos do complemento de Microsoft Project non respectan o calendario do complemento, o que resulta en requisitos de recursos incorrectos.
- A creación de proxectos a partir de modelos establece incorrectamente as datas de atribución e impide a capacidade de xerar requisitos de recursos.
- O usuario non pode acceder ás opcións **Categoría**, **Descrición**, **Estado** usando o teclado.
- Os valores de vendas reais do proxecto non inclúen os valores de vendas de tarifa e materiais.
- A agregación das vendas reais e do custo real ocorre incorrectamente con diferentes taxas de cambio.
- A descrición no **Modelo de hora de traballo predefinido** é enganoso.
- A baixada de nivel dunha tarefa non elimina a **Categoría** na interface de usuario ata que se actualice.
- Non está permitido omitir a validación para garantir o traslado un proxecto máis alá da súa data de finalización.

**Sales**

Resolvéronse os seguintes problemas:

- Xérase unha excepción de referencia nula nunha liña de oferta do proxecto porque **Importar desde a estimación do proxecto** é visible cando non se seleccionou un proxecto.
- O seguinte erro, "A referencia de obxecto non definida como unha instancia dun obxecto", prodúcese ao pechar unha oferta como **Gañada**.
- O estado do axuste non se establece durante unha reversión real mentres se desvincula un proxecto dunha liña de contrato.
- Cando Dynamics 365 Field Service e Project Service Automation están instalados, as opcións **Bloquear prezos** e **Usar os prezos actual** non se amosan ao mesmo tempo na páxina **Factura**.
- Para o idioma xaponés, hai tradución incoherente con outras páxinas baseadas en calendario.
- **Activar** e **Desactivar** elimináronse das entidades **Asociación e lista de prezos** en Project Service Automation.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
