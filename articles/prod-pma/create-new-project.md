---
title: Crear un novo proxecto
description: Este tema fornece información sobre como crear un novo proxecto.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5aa5e00252697f91a585eaaa83a0c8a39b315cc1b25fcbf6343fdf2ce31a824e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6985949"
---
# <a name="create-a-new-project"></a>Crear un novo proxecto

[!include [banner](../includes/banner.md)]

Complete os seguintes pasos para crear un novo proxecto.

1. Na páxina **Xestión de proxectos**, seleccione **Novo proxecto** e introduza os seguintes valores:

    - **Tipo de proxecto:** Tempo e material
    - **Nome do proxecto:** Fase 2 de actualización de XYZ
    - **Grupo de proxectos:** TM\_WIP
    - **ID do contrato do proxecto:** 00000002

2. Seleccione **Crear proxecto**.

## <a name="assign-a-resource-to-a-project"></a>Atribuír un recurso a un proxecto

1. Na páxina **Traballadores**, na lista **Traballadores**, seleccione o rexistro do traballador para o que configurou competencias previamente e abra o rexistro de traballador.
2. No panel Acción, no separador **Proxecto**, no grupo **Configurar**, seleccione **Atribuír proxectos**.
3. Na páxina **Atribucións de proxectos de validación de recursos**, no separador **Proxectos**, no campo **Engadir o proxecto aos proxectos seleccionados**, filtre no proxecto **Fase 2 de actualización de XYZ**.
4. No panel **Proxectos restantes**, seleccione un proxecto e seleccione o botón de frecha para engadilo ao panel **Proxectos seleccionados**.

Tamén pode atribuír categorías a un recurso segundo o precise. O tipo de categoría é **Custo** ou **Ingresos**. O tipo de categoría está determinado pola súa organización. Se non se atribúen categorías a un recurso, Finanzas busca a categoría predefinida en prezos de hora para custo e ingresos.

## <a name="set-up-project-resource-and-role-characteristics"></a>Configurar as características do recurso e do rol do proxecto

Un xestor de proxectos pode usar a funcionalidade de dotación de recursos para crear os roles necesarios para o proxecto. Pódense usar roles se aínda se descoñecen os recursos confirmados cando se reservan os recursos. Os roles pódense reservar temporalmente como recursos planificados, para que poida continuar as fases de planificación do proxecto.

[![Exemplo de rol.](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Escenario:** Contratouse a Contoso para completar un proxecto de tempo e material que ten unha carta de proxecto aprobada. O xestor de proxectos subalterno aínda está completando o alcance do proxecto. O xestor de recursos está a identificar actualmente recursos específicos que se reservarán para traballar no novo proxecto. Debido á natureza crítica do proxecto, o patrocinador do proxecto solicitou ao xestor de proxectos principal como un dos roles. O xestor de recursos debe adquirir o novo recurso e definir o rol no sistema no caso de que o xestor de proxectos subalterno precise a información do recurso durante a planificación do proxecto.

Os seguintes pasos mostran como o xestor de recursos pode configurar a función de xestor de proxectos principal e asociar as características dos recursos a el. Máis tarde, o rol pódese empregar para buscar recursos dispoñibles que coincidan coas competencias requiridas.

1. Na páxina **Configurar roles**, seleccione **Novo** e introduza os seguintes valores:

    - **ID de rol:** Xestor de proxectos principal
    - **Descrición:** Xestor de proxectos principal

2. Seleccione **Crear**.
3. Seleccione o rol **Xestor de proxectos principal** e seleccione **Configurar características**.
4. No campo **Tipo de características**, seleccione **Habilidade**.
5. No campo **Características dispoñibles**, introduza a habilidade para buscar.
6. No campo **Tipo de característica**, seleccione **Certificado**.
7. No campo **Características dispoñibles**, introduza o tipo de certificado para buscar.

## <a name="assign-a-project-resource-to-a-project"></a>Atribuír un recurso de proxecto a un proxecto

1. Na páxina **Todos os proxectos**, seleccione o proxecto **Fase 2 de actualización de XYZ**.
2. No separador **Equipo do proxecto e programación**, seleccione **Engadir**.
3. No campo **Rol**, seleccione **Membro do equipo**.
4. Seleccione **Reservar desde calendario**.
5. Na páxina **Dispoñibilidade de recursos**, seleccione **Ver configuración**.
6. Na páxina **Axustar configuración de visualización**, introduza os seguintes valores:

    - **Formato para a visualización do intervalo de datas:** Día
    - **Mostrar descricións de dispoñibilidade:** Si
    - **Mostrar capacidade restante:** Si

7. Na lista de recursos, seleccione un recurso.
8. Seleccione **Reserva dura** e **Capacidade total**.

## <a name="assign-a-resource-to-a-default-role"></a>Atribuír un recurso a un rol predefinido

Para axudar aos xestores de proxectos ou recursos, pode profundizar nos recursos que se poden reservar para un proxecto. Pode asociar un rol predefinido a un recurso existente ou a un recurso adquirido recentemente. Por exemplo, cando se contratou a Daniel, tiña a experiencia e as habilidades para ocupar o rol de analista empresarial. O xestor de recursos asignou este rol como o rol predefinido de Daniel. Polo tanto, o xestor de recursos engadiu a Daniel a un grupo de analistas empresariais dispoñibles para traballar en proxectos.

Durante a reserva de recursos, os xestores de proxectos poden filtrar os recursos de rol dispoñibles para traballar en proxectos. Poden utilizar esta información como un criterio cando realizan análises de decisións con múltiples criterios durante o cumprimento dos recursos. Tamén poden engadir outras características de recurso ao filtro para buscar recursos que teñan habilidades, educación e experiencia específicas para un determinado proxecto.

**Escenario:** Comezou un proxecto aprobado e reservouse a función de xestor de proxectos principal como recurso planificado durante a fase de planificación do proxecto. O xestor de recursos agora adquiriu un recurso para cubrir o rol de xestor de proxectos principal.

1. Na páxina **Lista de recursos**, seleccione **Daniel Goldschmidt**.
2. Na páxina **Rol de recurso**, seleccione **Novo** e introduza os seguintes valores:

    - **Efectivo:** Introduza a data actual.
    - **Caducidade:** Introduce **Nunca**.
    - **Rol:** Introduza **Xestor de proxectos principal**.

3. Seleccione **Gardar** e logo peche a páxina.
4. No separador **Competencias**, engada a habilidade **ProjectMgmt** e o certificado **PMP**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]