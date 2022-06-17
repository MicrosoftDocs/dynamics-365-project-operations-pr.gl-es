---
title: Modos de programación
description: Este artigo ofrece información sobre os modos de programación.
author: ruhercul
ms.date: 05/28/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 3cbe14f8d458c5d9631e0595912afa8cbb87b9de
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923646"
---
# <a name="scheduling-modes"></a>Modos de programación

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_


Dynamics 365 Project Operations proporciona ás organizacións a capacidade de definir como xestionan os cambios das variables clave nas tarefas dentro da estrutura de subdivisión do traballo. En función das necesidades específicas da organización, os xestores de proxectos poden facer cambios no modo de programación cando se crea un proxecto.

Hai tres modos de programación dispoñibles en Project Operations:

  - Duración fixa (este é o modo predefinido)
  - Esforzo fixo (*Traballo*)
  - Unidades fixas

Os valores afectados pola definición dun modo de programación específico determínanse coa seguinte fórmula:

  Esforzo = Duración x Unidades

Cando define o modo de programación dun proxecto, está configurando un destes valores, que logo non se pode cambiar. Manter este valor como unha constante dá prioridade a ese valor, que notifica ao sistema que non o cambie cando cambien os outros dous valores. A seguinte táboa ofrece información sobre os efectos de seleccionar un modo específico.

| **Nesta tarefa**             | **Se revisa unidades**   | **Se revisa duración** | **Se revisa esforzo**  |
|----------------------|---------------------------|----------------------------|---------------------------|
| Tarefa de unidades fixas     | A duración calcúlase de novo. | O esforzo calcúlase de novo.    | A duración calcúlase de novo. |
| Tarefa de esforzo fixo    | A duración calcúlase de novo. | As unidades calcúlanse de novo.    | A duración calcúlase de novo. |
| Tarefa de duración fixa  | O esforzo calcúlase de novo.   | O esforzo calcúlase de novo.    | As unidades calcúlanse de novo.   |

Para obter máis información sobre as implicacións dun modo determinado, consulte [Cambiar o tipo de tarefa para unha programación máis precisa](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72). No artigo, o termo **Traballo** úsase en lugar de **Esforzo**.

## <a name="change-the-organizations-scheduling-mode"></a>Cambiar o modo de programación da organización

Complete os seguintes pasos para definir o modo de programación dunha organización.

1. Vaia a **Configuración** \> **Xeral** \> **Parámetros** e, a seguir, seleccione o parámetro do proxecto. 
2. Na páxina **Parámetros do proxecto**, seleccione o modo de programación predefinido para a organización e, a seguir, defina a capacidade do xestor de proxectos para anular a configuración ao crear un novo proxecto.

## <a name="change-the-scheduling-mode-setting-on-a-project"></a>Cambiar a configuración do modo de programación nun proxecto

Se unha organización permite ao xestor de proxectos substituír o modo de programación predefinido, o xestor de proxectos pode facer ese cambio cando crea un novo proxecto. Non obstante, despois de gardar o proxecto, o modo de programación non se pode cambiar.

## <a name="copied-projects"></a>Proxectos copiados

Debido a que se crea un proxecto cando se realiza a acción de copiar proxecto, o xestor de proxectos non pode establecer o modo de programación. O proxecto de destino sempre estará de xeito predefinido no modo definido a nivel organizativo.

## <a name="copied-tasks"></a>Tarefas copiadas

Cando se copia unha tarefa dun proxecto a outro, a tarefa herda o modo de programación do proxecto de destino.
