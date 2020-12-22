---
title: Modelo de seguranza
description: Este tema fornece información sobre o modelo de seguridade en Dynamics 365 Project Operations.
author: stsporen
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: b01f3d88dd021895933bc863b762f019ae50eed6
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642901"
---
# <a name="security-model"></a>Modelo de seguranza

_**Aplícase a:** Project Operations para escenarios baseados en recursos/sen fornecemento, despregamento de Lite: xestionar a facturación proforma_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Microsoft Dynamics 365 Project Operations contén un modelo de seguridade exclusivo que permite un modelo de seguridade empresarial baseado en roles que colabora con Grupos de Microsoft Office. 


## <a name="security-roles"></a>Roles de seguranza
As capacidades front-end de Project Operations inclúen os seguintes roles:

| Rol                          | Descripción                                                                                                                                                                 | Scope |
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------|
| Xestor de prácticas              | Admite informes entre proxectos.                                                                                                            | Unidade empresarial              |
| Responsable da aprobación do proxecto              | Aproba tempo e gastos dun proxecto.                                                                                                                              | Unidade empresarial |
| Administrador de facturación de proxecto | Crea a proposta de factura.                                                                                                                                                 | Unidade empresarial |
| Xestor de proxectos               | Crea o plan do proxecto e solicita recursos.                                                                                                                              | Unidade empresarial |
| Recursos de proxecto              | Membros do equipo que se poden reservar e informar do tempo.                                                                                                          | Unidade empresarial|
| Xestor de recursos              | Todas as funcións de xestión de recursos, como cumprir as solicitudes e reservas de recursos, separáronse para admitir unha configuración híbrida de Xestor de proxectos + Xestor de recursos e un rol de xestor de recursos único e centralizado. | Unidade empresarial |


Microsoft Project para a web inclúe os seguintes roles:

| Rol           | Descripción                                                                                                        | Scope  |
|----------------|--------------------------------------------------------------------------------------------------------------------|--------|
| Usuario do proxecto   | Usuario cooperativo de Project que pode crear os seus propios proxectos e ver os proxectos compartidos con eles. | Usuario   |
| Sistema do proxecto | Rol empregado para o contexto da aplicación. Os clientes non deben usar este rol do sistema.                                    | Global |

## <a name="security-enforcement"></a>Aplicación da seguranza
As accións que se realizan a nivel de proxecto realízanse no contexto do usuario que iniciou sesión. Isto significa que para crear, abrir ou eliminar un proxecto, o usuario debe ter acceso dispoñible en CDS. O acceso a CDS pode concederse a través de calquera dos posibles mecanismos incluídos na plataforma. Por exemplo, un usuario cun alcance maior pode acceder ao proxecto ou se se realizou unha acción explícita para compartir o proxecto que concede acceso ao usuario.

É importante telo en conta ao crear proxectos en Project Operations.

## <a name="modern-group-collaboration-with-project-operations"></a>Colaboración moderna de grupo con Project Operations
Project para a web e Project Operations apoian a colaboración de grupos modernos. Os usuarios engadidos ao proxecto a través dun grupo poden editar o plan do proxecto.

Project para a web engade usuarios ao grupo automaticamente despois da atribución.

Os grupos permiten que traballar nos permisos do proxecto e os artefactos de colaboración complementarios de xeito cooperativo. O seguinte diagrama mostra os eventos e os cambios de estado que ocorren durante o proceso de atribución de grupos.

Project Operations non crea un grupo a través da acción implícita e só o fai a través da acción explícita de grupos de presión.

A busca de membros do grupo no diálogo **Xestión de grupo** está limitada a aqueles que se configuran como parte do grupo de seguranza do ambiente. Para obter máis información, vexa [Controlar o acceso de usuario a ambientes: grupos de seguranza e licenzas](https://docs.microsoft.com/power-platform/admin/control-user-access).

![Modo de grupo](./media/groupsmode.png)

1. O proxecto é creado e pertence ao usuario creador.
2. O propietario do proxecto actualízase co equipo.
3. O equipo do propietario está asignado ao grupo de Office especificado ou creado.
4. O propietario orixinal do proxecto engádese ao grupo de Office.

## <a name="deployment-recommendation"></a>Recomendacións de despregamento
A medida que evoluciona o modelo de colaboración dos grupos de Office, engadirase funcionalidade para proporcionar un control máis detallado ao longo do tempo. Anímase aos clientes que despregan Project Operations actualmente a centrarse nun modelo de seguranza tradicional de Microsoft Dynamics 365.

Para obter máis información, consulte [Seguranza en Common Data Service](https://docs.microsoft.com/power-platform/admin/wp-security).

## <a name="project-operations-and-microsoft-dynamics-365-finance-security"></a>Seguranza de Project Operations e Microsoft Dynamics 365 Finance
Project Operations inclúe os seguintes roles:

- Xestor de proxectos
- Contable do proxecto

Para obter máis información sobre seguranza en Finance, consulte [Seguranza baseada en roles](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/role-based-security).


