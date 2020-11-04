---
title: Configurar recursos de proxectos
description: Este tema fornece información sobre a configuración ou solicitude de recursos de proxecto.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7eec8ad5d78019219b2e04ca75eeaa5a3c8a748f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076304"
---
# <a name="set-up-project-resources"></a>Configurar recursos de proxectos

[!include [banner](../includes/banner.md)]

Debe configurar un calendario e asocialo a un empregado ou a un traballador. O calendario úsase para programar o proxecto e o tempo de traballo dos recursos reservados para o proxecto. Durante a configuración do calendario, os xestores de proxectos poden realizar a nivelación de recursos como parte da optimización de recursos. En función do programa do calendario, pódense aplicar restricións aos recursos. Pode configurar un calendario na páxina **Calendarios**.

Cando configura un traballador como recurso do proxecto, pode seleccionar entre os traballadores que traballan na empresa para a que configura recursos. Como alternativa, pode seleccionar traballadores doutras empresas da súa organización. Estes traballadores son coñecidos como recursos entre empresas.

Os seguintes procedementos explican como configurar un traballador como recurso de proxecto na súa empresa e como configurar un recurso de proxecto entre empresas.

## <a name="set-up-a-worker-as-a-project-resource"></a>Configurar un traballador como recurso do proxecto

1. Na páxina **Traballadores** , na lista **Traballadores** , seleccione o traballador que está a engadir como recurso do proxecto e abra o rexistro de traballador.
2. No panel de acción, seleccione **Proxecto** &gt; **Configurar** &gt; **Configuración do proxecto**.
3. Seleccione un calendario e logo peche a páxina.

Tamén pode especificar proxectos predefinidos para un recurso como un tipo de atribución previa. As atribucións previas pódense empregar cando o xestor de recursos ou o xestor de proxectos saiban en que proxectos traballará o recurso con antelación. As asignacións previas tamén poden basearse na solicitude dun patrocinador ou cliente do proxecto. Para atribuír previamente un proxecto, na páxina **Atribuír proxectos** , no separador **Proxectos** , na lista **Proxectos restantes** , seleccione o proxecto axeitado.

## <a name="set-up-an-intercompany-resource"></a>Configurar un recurso entre empresas

Cando configura un traballador como recurso entre empresas, debe completar a configuración tanto na empresa prestamista como na empresa prestameira.

### <a name="in-the-lending-company"></a>Na empresa prestamista

1. En Finanzas, verifique que a empresa prestamista está seleccionada e logo complete o procedemento da sección anterior, "Configurar un traballador como recurso do proxecto".
2. Na páxina **Contabilidade entre empresas** , seleccione **Nova**.
3. No campo **ID da persoa xurídica** , seleccione a empresa prestamista. Encha os campos como corresponda e, a seguir, seleccione **Gardar**.
4. Na páxina **Prezo de transferencia** , seleccione **Novo**.
5. No campo **Persoa xurídica prestameira** , seleccione a empresa apropiada.
6. Para prestar á empresa prestameira só o recurso que creou ao comezo desta sección, no campo **Recurso** , seleccione o nome do recurso que creou. Para poñer todos os recursos da empresa prestamista a disposición da empresa prestameira, deixe o campo **Recurso** en branco.
7. Na páxina **Parámetros de xestión de proxectos e contabilidade** , no separador **Entre empresas** , configure a opción **Activar a programación de recursos e follas de control horario entre empresas** en **Si**.

### <a name="in-the-borrowing-company"></a>Na empresa prestameira

- Na páxina **Lista de recursos** , no filtro de busca, introduza o nome do recurso que creou para a empresa prestamista, para comprobar que o nome está incluído na lista de recursos para a empresa prestameira.

## <a name="request-project-resources"></a>Solicitar recursos de proxecto
A funcionalidade para a programación de recursos do proxecto só permite aos xestores de recursos distribuír recursos con persoal en compromisos ou proxectos. Para activar esta funcionalidade, complete as seguintes tarefas ou verifique que se completaron:

- Configurar as secuencias numéricas.
- Configurar fluxos de traballo de xestión de proxectos e contabilidade.
- Activar fluxos de traballo de solicitude de recursos.

Despois de completar as tarefas anteriores, pode completar as seguintes tarefas se o precisa:

- Crear unha solicitude de recurso a partir dun recurso con persoal con reserva branda.
- Supervisar solicitudes de recursos.
- Cumprir de solicitudes de recursos.
- Solicitar un recurso con persoal dunha WBS.
- Reservar recursos para un proxecto sen ter unha solicitude dun recurso con persoal.
