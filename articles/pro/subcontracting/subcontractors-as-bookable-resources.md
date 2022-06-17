---
title: Configurar subcontratistas como recursos reservables
description: Este artigo explica como configurar e manter os recursos de subcontratistas que se crean a partir de usuarios e contactos do sistema, para que poidan asociarse a subcontratos en Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 07/28/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f005a05fb874f9e32a0041db5fc8fa1228fc91f1
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927512"
---
# <a name="set-up-subcontractors-as-bookable-resources"></a>Configurar subcontratistas como recursos reservables

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplícase a:** Despregamento de Lite - de acordo a facturación proforma_

Siga estes pasos para configurar os subcontratistas como recursos reservables en Microsoft Dynamics 365 Project Operations.

1. Vaia a **Proxecto** \> **Recursos** e seleccione **Novo**.
2. Na páxina **Novo recurso reservable**, na campo **Tipo de recurso**, seleccione unha das seguintes opcións:

    - **Usuario** - Seleccione este tipo de recurso se o subcontratista debe acceder a Project Operations para introducir tempo ou gastos. Se selecciona **Usuario**, o subcontratista require unha licenza válida para acceder ao sistema.
    - **Contacto** ou **Conta** - Seleccione un destes tipos de recursos se o subcontratista non precisa acceso a Project Operations, pero debe estar dispoñible para tarefas ou reservas de proxectos. Ningún destes tipos de recursos proporciona acceso ao sistema. Seleccione **Conta** para representar á empresa do vendedor como un recurso reservable. Seleccione **Contacto** para representar aos empregados individuais do fornecedor.

3. Dependendo do tipo de recurso que seleccionou, solicitaráselle que seleccione o usuario, a conta ou o rexistro de contacto correspondentes.
4. No campo **Tipo de traballador**, seleccione o "Traballador contratado" para configurar o subcontratista como recurso reservable.

    > [!NOTE]
    > Se deixa o campo **Tipo de traballador** en branco, o recurso reservable considerarase como un empregado.

5. Se seleccionou **Traballador contratado** como tipo de traballador, seleccione o fornecedor para o que traballa o recurso.
6. Seleccione a zona horaria do recurso e logo seleccione **Gardar**. Para atribuír un modelo de hora de traballo ao recurso reservable, pode seleccionar **Establecer calendario** na páxina de lista **Recurso reservable**.

Para estar asociado a unha liña de subcontrato, un recurso reservable debe cumprir estas condicións.

- O recurso reservable debe ser un traballador contratado.
- Un recurso reservable do tipo de recurso **Contacto** debe estar asociado á conta do fornecedor como contacto. Un recurso reservable do tipo de recurso **Usuario** non ten que estar asociado á conta do fornecedor como contacto.
- O valor do campo **Fornecedor** do recurso reservable debe coincidir co valor do campo **Fornecedor** do subcontrato.

## <a name="update-the-type-of-worker-and-vendor-mapping-for-bookable-resources"></a>Actualice o tipo de asignación de traballadores e fornecedores para recursos reservables

O campo **Tipo de traballador** para un recurso reservable determina se o recurso reservable é un traballador contratado ou un empregado. O campo **Fornecedor** define a conta do fornecedor á que está asociado o recurso reservable. Asociar un recurso reservable a un fornecedor como contacto indica que o contacto é un empregado da empresa do fornecedor.

Se os campos **Tipo de traballador** e **Fornecedor** para un recurso reservable cambian, os cambios afectan a todas as validacións futuras nos novos rexistros que crea o recurso reservable, como as entradas de tempo. Non obstante, os cambios non invalidan os rexistros existentes.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
