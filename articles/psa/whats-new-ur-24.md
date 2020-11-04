---
title: Novidades ou cambios na versión 24 de actualización de Project Service Automation, V3
description: Este tema mostra as funcionalidades e correccións que están dispoñibles la versión 24 de actualización de Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 10/02/2020
ms.topic: article
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 6c8348e65307f63a251f97bf1ea17578e7026da8
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076084"
---
# <a name="project-service-automation-update-release-24-v3"></a>Versión 24 de actualización de Project Service Automation, V3

Comprácenos anunciar a última actualización da aplicación Project Service Automation para Dynamics 365. Esta versión inclúe algunhas melloras importantes na calidade, rendemento e facilidade de uso. Esta versión é compatible con Dynamics 365 9.x. Para actualizar a esta versión, visite a paxina de solucións do Centro de administración para Dynamics 365 en liña para instalar a actualización. Para obter máis información, consulte [Instalar, actualizar ou eliminar unha solución preferida](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)

Este tema mostra as funcionalidades e correccións que son novas ou modificadas para Project Service Automation V3, versión 24 de actualización. Esta versión ten un número de compilación de V 3.10.42.43 e está dispoñible xeralmente a través dunha autoactualización desde outubro de 2020.

## <a name="update-release-24"></a>Versión 24 de actualización

### <a name="bug-fixes"></a>Correccións de erros

**Sales**

Resolvéronse os seguintes problemas:

- Problema ao configurar a lista de prezos predefinida dos produtos.
- O rendemento de gañar oferta é lento debido á copia da lista de prezos integrada e os rexistros de prezos de rol.
- **Contrato de proxecto/Plataforma común de vendas** > **Elemento da liña de produtos/Cantidade da liña de pedido** redondéase automaticamente ao numero enteiro máis próximo.
- Eleve os privilexios do sistema ao ler listas de prezos.
- Copie os campos de enderezo do cliente **address1_freighttermscode** e **address1_shippingmethodcode** en Oferta/Pedido. 


**Tempo e gasto**

Resolvéronse os seguintes problemas:

- A **Grade de entrada de tempo** non admite o comportamento de tempo **Só data**.
- **Entrada de tempo** non se actualiza automaticamente. É necesaria unha actualización manual.
- Non se poden importar as entradas de tempo dunha atribución cando hai unha pausa (0 horas) nas atribucións dun recurso.
- Cando cree unha entrada de tempo, configure o inicio igual que **data_msdyn**.
- Volva activar a edición en masa para a entrada de tempo.

**Xestión de recursos**

Resolvéronse os seguintes problemas:

- Tratar de actualizar o estado dunha reserva de entre días sen un requisito activará unha excepción de referencia nula.
- Erro ao cargar a **Vista de reconciliación**.


**Xestión de proxectos**

Resolvéronse os seguintes problemas:

- No **Programa do proxecto** , ao cambiar de **Manual** a **Automático** , gardar automaticamente non se está completando.
- Os custos de gastos non deben calcularse para a variación na **Grade de rastrexo de proxecto**.
- Comportamento incoherente das columnas **Etiqueta de estimacións** durante a carga fronte ao cambio do tipo **Fase de tempo**.
- É posible que o custo real dun proxecto non reflicta os totais de **Datos reais**.
- **Data de finalización estimada** no separador **Resumo** non coincide co **Programa WBS**.
- **Actualizar as horas reais** ao cancelar sangría non funciona correctamente.
- Un xestor de proxectos fóra da **BU** raíz non pode crear un proxecto.
- Os cambios na tarefa ou na categoría en **Estimacións de gastos** non persisten.
- **Copia do contrato** copia os programas de facturación e o estado de execución.
- O botón **Actualizar datos reais** calcula incorrectamente as tarefas de resumo.
- Suplemento de Microsoft Project: Corrixe un erro de referencia nula se algún membro do equipo ten unha unidade de recursos baleira.
