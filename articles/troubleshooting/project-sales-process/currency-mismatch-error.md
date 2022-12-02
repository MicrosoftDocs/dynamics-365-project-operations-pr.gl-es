---
title: Erro de moeda que non coincide
description: Este artigo ofrece información de solución de problemas sobre un erro de moeda que non coincide que se produce cando garda tipos de rexistro específicos.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5b0973a340dec8e68f326803d75bea9803e19791
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914722"
---
# <a name="currency-mismatch-error"></a>Erro de moeda que non coincide 

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Ao gardar un proxecto, un contrato, unha oferta ou un recurso reservable, pode aparecer o erro **A moeda da empresa propietaria do contrato non coincide coa moeda da unidade de contratación. Escolla outra empresa propietaria ou outra unidade de contratación para o contrato para continuar**. Isto débese a que hai un desaxuste de moeda entre a moeda da unidade contratante para o rexistro e a moeda da empresa propietaria.


## <a name="resolution"></a>Resolución

Para solucionar este problema, faga o seguinte:
- Verifique a moeda da unidade de contratación para este rexistro. Pode ver a moeda abrindo o rexistro da unidade organizativa e verificando o valor do separador **Xeral** no campo **Moeda**.
- Verifique a moeda da empresa propietaria. Pode ver a moeda indo a **Relacionado** > **Libros de contabilidade** no rexistro da empresa. Faga dobre clic no rexistro do libro maior que está asociado á empresa e verifique o valor no separador **Xeral** no campo **Moeda de contabilidade**.

Se a moeda definida na unidade de contratación e o rexistro do libro maior non coinciden, axuste a configuración ou seleccione diferentes valores cando garde o rexistro. O sistema require que estes rexistros coincidan para garantir os fluxos correctos de facturación entre empresas. Para obter máis información sobre as configuracións entre empresas, consulte [Crear transaccións entre empresas](../../project-accounting/create-intercompany-transactions.md).

Se o rexistro da empresa non ten ningún rexistro asociado, isto indica que falta unha configuración ao configurar o ambiente. A configuración debe ser corrixida polo administrador do sistema. O administrador do sistema debe ir a **Configuracións de escrita dual** e parar e reiniciar **Mapa de escrita dual de libros maiores** coa sincronización inicial deste mapa e os seus requisitos previos. Para obter máis información, consulte [Versións de mapa de escrita dual de Project Operations](../../environment/resource-dual-write-maps.md).
