---
title: Despregar manualmente a aplicación Project Operations Dataverse con soporte de escrita dual
description: Este tema explica como despregar manualmente a aplicación Project Operations Dataverse para que admita a escrita dual.
author: stsporen
ms.date: 06/18/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 06325a9a9f9084d1f506f2493c32565fe7b7c52ae6fe22c81339b9c1d632e688
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986444"
---
# <a name="manually-deploy-the-project-operations-dataverse-app-with-dual-write-support"></a>Despregar manualmente a aplicación Project Operations Dataverse con soporte de escrita dual

_**Aplícase a:** Project Operations para situacións baseadas en recursos/sen fornecemento_

Este tema explica como despregar manualmente Microsoft Dynamics 365 Project Operations en Microsoft Dataverse para que admita a escrita dual. Project Operations detecta a configuración do ambiente e engade soporte adicional para a escritura dual se se cumpren os requisitos previos.

Durante o despregamento a través de Microsoft Dynamics Lifecycle Services (LCS), se seguiu as instrucións deste tema, podes omitir o despregamento da integración de Microsoft Power Platform (anteriormente coñecida como o ambiente de Common Data Service).

O proceso de despregamento de Project Operations en Dataverse para que admita a escrita dual ten catro pasos principais:

1. [Cree un novo ambiente en Dataverse que admita a escrita dual](#create).
2. [Engada requisitos previos de escrita dual ao ambiente](#prerequisites).
3. [Engada a aplicación Project Operations Dataverse](#dataverse).
4. [Ligue os seus ambientes](#link).

## <a name="create-a-new-environment-in-dataverse-that-supports-dual-write"></a><a name="create"></a>Crear un novo ambiente en Dataverse que admita a escrita dual

Para completar este procedemento, debe iniciar sesión como administrador.

1. Abra o [centro de administración de Power Platform](https://admin.powerplatform.com) e inicie sesión como administrador.
2. Cree un novo ambiente e noméeo.
3. Seleccione o tipo de ambiente. Se se rexistrou para a oferta de proba, seleccione **Proba (baseada en subscrición)**.
4. Confirme a rexión de despregamento.
5. Active a opción **Crear unha base de datos para este ambiente**. 
6. Confirme o idioma e, a seguir, confirme que a moeda coincide coa moeda para as súas aplicacións de Finance and Operations.
7. Active a opción **Aplicacións de Dynamics 365** e confirme que o campo **Despregar automaticamente estas aplicacións** está definido como **Ningunha**.
8. Engada un grupo de seguranza, se é necesario un grupo de seguranza.
9. Seleccione **Gardar** para crear o ambiente.
10. Agarde a que se complete o despregamento e o ambiente chegue ao estado **Listo**.

## <a name="add-dual-write-prerequisites-to-the-environment"></a><a name="prerequisites"></a>Engadir requisitos previos de escrita dual ao ambiente

A compatibilidade coa escrita dual inclúe campos adicionais que se engaden a entidades clave, como a entidade **Empresa**. Se está engadindo compatibilidade con escrita dual a un ambiente existente, pode que teña que actualizar os datos para activar a compatibilidade. Para obter información sobre como facer o bootstrap dos datos, consulte [Facer bootstrap dos datos da empresa](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data). Para obter máis información sobre a escrita dual, consulte [Requisitos do sistema de escrita dual](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req).

Complete este procedemento para engadir os requisitos previos de escrita dual ao seu ambiente.

1. Abra o ambiente que acaba de crear e logo vaia a **Recurso** \> **Aplicacións de Dynamics 365**.
2. Seleccione **Solución principal de escrita dual** na lista de aplicacións e instálea.
3. Agarde ata que finalice a instalación. Logo seleccione **Solución de orquestración de escrita dual** na lista de aplicacións e instálea.

## <a name="add-the-project-operations-dataverse-app"></a><a name="dataverse"></a>Engadir a aplicación Project Operations Dataverse

Só pode completar este procedemento se completou os procedementos anteriores antes de instalar Project Operations. Durante a instalación, o sistema analiza a configuración do ambiente e engade compatibilidade con escrita dual se é necesario.

1. Abra o ambiente que creou antes e logo vaia a **Recurso** \> **Aplicacións de Dynamics 365**.
2. Seleccione **Microsoft Dynamics 365 Project Operations** na lista de aplicacións e instálea.

## <a name="link-your-environments"></a><a name="link"></a>Ligar os seus ambientes

Despois do despregamento de Dataverse, pode configurar a ligazón nas súas aplicacións de Finance and Operations. Siga os pasos indicados en [Usar asistente de escrita dual para ligar os seus ambientes](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment).
