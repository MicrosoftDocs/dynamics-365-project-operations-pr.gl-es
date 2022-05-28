---
title: Erro de incompatibilidade de moeda
description: Este tema ofrece información de solución de problemas sobre un erro de desajuste de moeda que se produce cando garda tipos de rexistro específicos.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5bb54a121f0dc22f1c0ea88ada9c922c1d4c6544
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589746"
---
# <a name="currency-mismatch-error"></a>Erro de incompatibilidade de moeda 

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Cando garda un proxecto, contrato, presuposto ou recurso reservable, é posible que reciba o erro: **A moeda da empresa propietaria non coincide coa moeda da unidade contratante. Escolla unha empresa ou unidade contratante diferente para continuar**. Isto débese a que hai un desaxuste de moeda entre a moeda da unidade contratante para o rexistro e a moeda da empresa propietaria.


## <a name="resolution"></a>Resolución

Para solucionar este problema, faga o seguinte:
- Verifique a moeda da unidade de contratación para este rexistro. Podes ver a moeda abrindo o rexistro da unidade organizativa e verificando o valor no **Xeral** ficha na **Moeda** campo.
- Verifica a moeda da empresa propietaria. Podes ver a moeda indo a **Relacionado** > **Libros contables** no rexistro da empresa. Fai dobre clic no rexistro do libro maior que está asociado á empresa e verifique o valor no **Xeral** ficha na **Moeda contable** campo.

Se a moeda definida na unidade de contratación e o rexistro do libro maior non coinciden, axuste a configuración ou seleccione diferentes valores cando garde o rexistro. O sistema require que estes rexistros coincidan para garantir os fluxos correctos de facturación entre empresas. Para obter máis información sobre as configuracións entre empresas, consulte [Crea transaccións entre empresas](../../project-accounting/create-intercompany-transactions.md).

Se o rexistro da empresa non ten ningún rexistro asociado, isto indica que falta unha configuración ao configurar o ambiente. A configuración debe ser corrixida polo administrador do sistema. O administrador do sistema debe ir a **Configuracións de dobre escritura** e parar e reiniciar **Mapa de escritura dual Ledgers** coa sincronización inicial deste mapa e os seus requisitos previos. Para obter máis información, consulte [Versións de mapa de escrita dual de Project Operations](../../environment/resource-dual-write-maps.md).
