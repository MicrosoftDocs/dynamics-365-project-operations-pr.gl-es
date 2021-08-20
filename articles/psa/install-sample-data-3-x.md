---
title: Instalación dos datos de exemplo
description: Este tema ofrece información sobre a instalación de datos de exemplo en Project Service Automation.
ms.custom: dyn365-projectservice
ms.date: 11/08/2018
ms.reviewer: kfend
ms.suite: ''
applies_to: Dynamics 365 Project Service Automation
author: ruhercul
ms.author: ruhercul
search.audienceType: IT Pro, Developer
search.app: ''
ms.openlocfilehash: 01e2f1f6b29e040d5c72af402031e13a867736405c4ee161e49b74a30e4b506e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6985544"
---
# <a name="sample-data-installation-for-the-project-service-application"></a>Instalación de datos de exemplo para a aplicación Project Service

[!include [banner](../includes/psa-now-project-operations.md)]

Para axudarlle a crear os seus propios ambientes de demostración, Microsoft ofrece os paquetes descargables de datos de exemplo que mostran as capacidades das súas aplicacións. Hai dous tipos de paquetes de datos de exemplo:
- datos de referencia/configuración
- datos de demostración (datos de referencia/configuración e transaccionais, como os pedidos de traballo e os proxectos)

Os paquetes de datos de **referencia** de exemplo se poden descargar en tres paquetes diferentes, polo que pode instalar datos só para Project Service ou só para Field Service ou ben pode instalar datos de exemplo para ambas aplicacións ao mesmo tempo.

Os paquetes de datos de configuración/referencia de exemplo son:

- [**V902PSMasterData** - Só Project Service versión 3.x](https://go.microsoft.com/fwlink/?linkid=2026540&clcid=0x409)

- [**V902FSMasterData** - Só Field Service versión 8.x](https://go.microsoft.com/fwlink/?linkid=2026536&clcid=0x409)

- [**V902FPSMasterData** - Field Service 8.x e Project Service 3.x](https://go.microsoft.com/fwlink/?linkid=2026041&clcid=0x409)

O paquete de datos de **demostración** máis recente é:

 - [**FPSDemoData** - Field Service 8.x e Project Service 3.x](https://aka.ms/fpsdemodatapackage)

   As instrucións de instalación difiren lixeiramente nos usuarios para crear e configurar unha sección pero o resto é o mesmo que na [**publicación de blog**](https://aka.ms/fpsdemodatablog) previa. Este paquete incorpora un conxunto reducido de datos de demostración e tarda aproximadamente 3 horas en instalarse.

Os paquetes de datos de exemplo só están dispoñibles en inglés.

> [!IMPORTANT]
> **Non hai forma de desinstalar os datos de exemplo.** Só debe instalar estes paquetes en sistemas de demostración, avaliación, formación ou probas. Teña en conta tamén que non se admite instalar un paquete individual e, a seguir, instalar outro paquete individual. (É dicir, non pode instalar **FSMasterData** seguido de **PSMasterData**, ou viceversa). Se ve que necesita datos de exemplo para ambas aplicacións en calquera momento no futuro, debe instalar o paquete **v902FPSMasterData**.

Ao instalar calquera dos paquetes de datos de exemplo, o proceso de instalación realiza as seguintes accións:

- Crea ou define parámetros predefinidos para usar Project Service, Field Service, ou ambas aplicacións (se corresponde).

- Importa datos de exemplo para as aplicacións, como recursos reservables, os roles específicos da aplicación, vendas e listas de prezos de custo, unidades organizativas, rexistros de proceso de ventas e outras entidades para mostrar as capacidades clave.  

Co paquete de **datos de demostración**, vostede obtén os datos anteriores e datos transaccionais adicionais como pedidos de traballo e proxectos.

Quere saber que capacidades pode demostrar cos datos de exemplo? Consulte o a situación ficticia de Fabrikam Robotics en [Notas técnicas](#technical-notes).

Se ten preguntas sobre a instalación destes paquetes de datos de exemplo, [envíenos un correo electrónico a fpsdemodata@microsoft.com](mailto:fpsdemodata@microsoft.com).

## <a name="requirements"></a>Requisitos

O protocolo de instalación asume o seguinte sobre a súa instancia de destino (organización):

- O idioma base é o inglés e a moeda base o dólar estadounidense (USD, $).

- A organización aínda non ten datos de Project Service ou Field Service, ou só ten datos predefinidos básicos que veñen con calquera nova organización

- A versión correcta da aplicación empresarial xa está instalada:
       
    - **Para FPSDemoData ou v902FPSMasterData:** A organización ten Field Service versión 8.x e Project Service versión 3.x instaladas.

    - **Para v902PSMasterData:** A organización ten Project Service versión 3.x instalada.

    - **Para v902FSMasterData:** A organización ten Field Service versión 8.x instalada.

> [!NOTE]
> Se necesita instalar os datos de exemplo sobre un ambiente de proba ou demostración de Project Service ou Field Service existente que xa ten datos (non recomendado), deberá suspender os controis previos de seguranza realizados polo instalador. Para obter máis información, consulte as notas técnicas a continuación.

## <a name="prepare-for-installation"></a>Preparar para a instalación

Debe executar o instalador nun equipo cunha versión de Windows recente (Windows 10 preferiblemente).

Debe planificar que o equipo siga conectado a unha rede, e que a instalación se execute nun máximo de **1 hora** para **datos de configuración/referencia**. (Normalmente a instalación tarda aproximadamente 30 minutos para **FPSMasterData**, que inclúe datos de exemplo para ambas as aplicacións.) Para **FPSDemoData**, a instalación tardará aproximadamente **3 horas**.

O equipo debe ter a función de protector de pantalla desactivada. Do contrario, as credenciais de sesión para a instalación se poden perder cando se active o protector de pantalla (a menos que manteña a sesión activa todo o tempo).

> [!div class="mx-imgBorder"]
> ![Captura de pantalla da configuración do protector de pantalla, co protector de pantalla desactivado.](media/sample-data-1.png)

## <a name="download-and-unpack"></a>Descargar e desempaquetar

O instalador dos datos de exemplo de Project Service e Field Service distribúese como executable autoextraíble. Os nomes de ficheiro poden variar segundo o paquete de datos de exemplo, pero polo demais os pasos son os mesmos para o paquete que instale.

Despois de descargar un paquete, execute o ficheiro .exe e, a seguir, acepte as condicións para desempaquetar o ficheiro zip comprimido. Entón deberá extraer o contido dese ficheiro nun cartafol no equipo.

En función do sistema operativo e da configuración de seguranza, é posible que deba realizar os seguintes pasos despois de desempaquetar o ficheiro zip:

1. Busque e prema co botón secundario no ficheiro **FPSDemoData.dll** no cartafol **v902FPSMasterData** / **PackageDeployer_FPSDemoData**.

2. Escolla **Desbloquear**.

3. Seleccione **Aplicar**.

4. Seleccione **Aceptar**.


## <a name="create-or-configure-users"></a>Creación ou configuración de usuarios

O paquete **FPSDemoData** require seis usuarios mentres que o paquete **FPSMasterData** require un usuario. Consulte o correcto para o seu paquete de datos de exemplo.

## <a name="create-or-configure-users---setupreference-data-packages"></a>Crear ou configurar usuarios - paquetes de datos de configuración/referencia

O paquete **FPSMasterData** está deseñado para a instalación cun usuario chamado Spencer Low coa configuración descrita aquí. Para instalar o paquete correctamente, debe crear (ou cambiar temporalmente) usuarios no seu ambiente para que coincidan coa configuración entrante de datos de exemplo.

Para crear ou configurar usuarios, vaia a **Configuración** > **Seguranza** > **Usuarios** e faga o seguinte:

1. Estableza UserFullname=”Spencer Low” co nome de usuario “spencerl” (**minúsculas**) nos roles de Administrador de proxecto e Director de prácticas.

2. Seleccione o usuario **Spencer Low** e despois seleccione **Administrar roles**. Busque e seleccione o rol **Administrador do sistema** e, a seguir, seleccione **Aceptar** para conceder dereitos completos de administración a Spencer Low. Este paso é necesario para garantir que os rexistros de exemplo se crean coa propiedade do usuario correcto e por tanto encher as vistas correctamente.

3. Desde o paquete descargado, necesita actualizar un ficheiro de asignación de datos con enderezos de correo electrónico do contexto do usuario predefinido. Para facelo, abra **PkgFolder** e, a seguir, busque y abra o ficheiro **ImportUserMapFile.xml** en Caderno de notas (ou Visual Studio ou outro editor de XML). Estableza o campo **DefaultUserToMapTo=** no enderezo de correo electrónico do usuario Spencer Low.

4. Se non está a usar Spencer Low co nome de usuario **spencerl**, necesita actualizar un ficheiro adicional. Abra o ficheiro **DemoDataPreImportConfig.xml** e, a seguir, busque a etiqueta **userstocreateandconfigure**. Actualice a etiqueta **\<login\>** co nome de usuario do seu usuario Spencer Low. Para obter máis información, consulte as [Notas técnicas](#technical-notes).

## <a name="create-or-configure-users---demo-data-package"></a>Crear ou configurar usuarios - paquete de datos de demostración

O paquete de datos de demostración require seis usuarios. Para que o paquete se instale correctamente, faga o seguinte:

 1. Cree ou cambie o nome temporalmente a usuarios existentes para que coincidan coa configuración de datos de exemplo entrantes indo a **Configuración** > **Seguranza** > **Usuarios**.
 
    Estes roles só son necesarios para demostracións baseadas en persoas.  
    - Nome completo de usuario = "David So" como Técnico de Field Service   
    - Nome completo de usuario = "Jamie Reding" como Despachador de Customer Service e Field Service   
    - Nome completo de usuario = "Molly Clark" como Xestor de Contas   
    - Nome completo de usuario = "Spencer Low" Xestor de prácticas e proxectos  
    - Nome completo de usuario = "Veronica Quek" como Membro de equipo   
    - Nome completo de usuario = "William Contoso"
  
2. Por motivos de importación de datos de demostración, atribuía aos seis usuarios anteriores o rol de Administrador para que os rexistros de exemplo se iporten correctamente. 

3. Abra **PkgFolder** e, a seguir, localice e abra **ImportUserMapFile.xml**. Actualice os campos **Novo=** aos enderezos de correo electrónico dos Usuarios correspondentes no seu sistema.

   > [!div class="mx-imgBorder"]
   > ![Captura de pantalla de UserMapFile.](media/sample-data-7.png)

4. O usuario con nome completo "Spencer Low" ten un ID de usuario diferente de **"spencerl"**, polo que ten que actualizar un ficheiro adicional. Abra **DemoDataPreImportConfig.xml** e busque a etiqueta **userstocreateandconfigure**. Actualice a etiqueta **\<login\>** con loginId (distingue maiúsculas e minúsculas). 

5. O primeiro calendario do usuario (na etiqueta **userstocreateandconfigure**) utilízase para encher as horas de traballo para todos os recursos reservables ao importar os datos de demostración. Navegue a **Configuración** > **Seguranza** > **Usuarios**, busque o usuario "Spencer Low" e abra a opción "Horas Laborables". Edite as horas laborables existentes seleccionando a opción **Toda a programación periódica semanal de principio a fin**. Asegúrese de que as **Horas laborables están definidas como 8 AM - 5 PM (9 horas), de luns a venres, e co fuso horario en hora do Pacífico (Estados Unidos e Canadá)**. Isto é necesario para garantir que o panel Proxecto e Programación se mostran como está previsto.

**Recomendación:** Considere crear unha copia de seguranza da súa organización agora, en acaso de que necesite volver ao punto de partida se algo sae mal durante a instalación dos datos de exemplo. Para obter máis información, vexa [Copia de seguranza e restauración de instancias](/dynamics365/customer-engagement/admin/backup-restore-instances).

## <a name="run-the-package-deployer"></a>Executar o Package Deployer

1. Atope e execute **PackageDeployer.exe** no cartafol **v902FPSMasterData** OU **PackageDeployer_FPSDemoData**.

2. Acepte os termos e condicións.

3. Na seguinte ventá:

   a. Seleccione o tipo de despregamento **Office 365**.

   b. Utilice o usuario e o contrasinal do usuario administrador do sistema configurados en “Crear ou configurar usuarios” (”Spencer Low” con nome de usuario “spencerl”).

   c. Asegúrese de que **Mostrar a lista de organizacións dispoñibles** estea seleccionado.

      > [!div class="mx-imgBorder"]
      > ![Captura de pantalla da ventá de Package Deployer con “Mostrar a lista de organizacións dispoñibles” seleccionado](media/sample-data-2.png)

4. Seleccione a organización onde desexa instalar os datos de exemplo.

5. Seleccione **Seguinte** ata que vexa o diálogo **Configurar datos de demostración**.

   > [!div class="mx-imgBorder"]
   > ![Captura de pantalla da ventá de estado do instalador dos datos de demostración.](media/sample-data-3.png)

6. Antes de continuar, teña en conta que instalar datos de exemplo pode tardar ata unha hora (normalmente ~10 minutos). Deberá asegurarse de que o equipo permanece acendido e conectado a unha rede durante todo o proceso de instalación, e que a sesión permanece activa.   

7. Cando estea listo, prema **Seguinte** para iniciar o proceso de instalación de datos de exemplo. Despois de cargar os datos de exemplo, prema **Finalizar**.

## <a name="verify-the-sample-data-installation"></a>Comprobe a instalación dos datos de exemplo

Para unha comprobación de estado, comprobe que aparecen o número de rexistros e os tipos de entidades incluídas no escenario ficticio Fabrikam Robotics correctamente.

Unha vez que os datos de exemplo se carguen completamente, inicie sesión como o usuario Spencer Low e confirme o seguinte:

- Se a aplicación Project Service está instalada, vaia a **Project Service** > **Configuración** > **Listas de prezos**. Confirme que existen taxas de facturación e taxas de custo coa divisa adecuada para cada país ou rexión no conxunto de datos.

- Se a aplicación Project Service está instalada, vaia a **Universal Resource Scheduling** > **Configuración** > **Unidades organizativas**. Confirme que unha lista de prezos de custo coa divisa adecuada se asociou a cada unidade organizativa (excluíndo entradas de cidade). Se falta algunha, busque e asocie a lista de prezos de custo correcta.

- Se a aplicación Field Service está instalada, vaia a **Project Service** > **Configuración** > **Listas de prezos**. Confirme que existen taxas de facturación e taxas de custo. Vaia a **Field Service** > **Configuración** > **Listas de prezos** e comprobe que existen taxas de facturación e taxas de custos, coa divisa adecuada para cada país ou rexión no conxunto de datos.

  > [!div class="mx-imgBorder"]
  > ![Captura de pantalla de listas de prezos activas.](media/sample-data-4.png)

  > [!div class="mx-imgBorder"]
  > ![Captura de pantalla de unidades organizativas activas.](media/sample-data-5.png)

## <a name="technical-notes"></a>Notas técnicas

Consulte a continuación para obter máis detalles técnicos sobre a instalación destes datos.

### <a name="installing-sample-data-on-top-of-existing-data-not-recommended"></a>Instalación de datos de exemplo sobre datos existentes (non recomendado)

Se necesita instalar datos de exemplo sobre un ambiente de proba ou demostración de Field Service ou Project Service existente que xa ten datos, deberá suspender os controis previos de seguranza realizados polo instalador.

Para facelo, vaia ao cartafol **PkgFolder** para buscar e abrir o ficheiro **DemoDataPreImportConfig.xml** con Caderno de notas (ou outro editor de XML).

Busque o valor seguinte e, a seguir, cambie o valor de true a false:

```alias
<TerminateOnPreCheckFailure>true</TerminateOnPreCheckFailure>
```

Este cambio fai que o instalador omita algunhas comprobacións de seguranza importantes, entre elas:

- Confirmar que non hai más que un rexistro activo de **Unidade organizativa** e, a seguir, cambiar o seu nome a **Fabrikam US**.

- Confirmar que non hai más que un rexistro activo de **Modelo de traballo**.

- Confirmar que non hai más que un rexistro activo de **Parámetro de proxecto** e, a seguir, cambiar o nome desa entidade a **Parámetros**.

### <a name="configuration-components"></a>Compoñentes de configuración

Hai varios outros compoñentes de configuración neste ficheiro de configuración previo á importación. Para usuarios técnicos, algúns destes inclúen:

- **\<RequiredSolutions\>** especifica as instalacións da solución requiridas previamente e os seus números de versión.

- **\<InstallSampleData\>** controla se os datos de exemplo estándar para as aplicacións se instalan.

    - false - omite a instalación destes datos integrados (que son extraíbles)

    - true - instala os datos integrados simultaneamente á instalación dos datos de exemplo de FS e PSA

- **\<PreImportDataCollection\>** especifica as asignacións de datos de ficheiro plano e os rexistros asociados que se importarán antes da instalación dos datos de exemplo principais.

- **\<EntitiesToEnableScheduling\>** especifica que entidades deben estar activadas para a reserva en Microsoft Dynamics Scheduling (tamén denominado Universal Resource Scheduling).

- **\<UsersToCreateAndConfigure\>** especifica os recursos reservables que se crearán (se aínda non existen) antes de que se execute a importación de datos de exemplo. Teña en conta que os recursos reservables dos datos de exemplo do sistema de orixe coinciden cos rexistros de recursos reservables do sistema de destino en FullName e inicio de sesión de cada recurso. Por tanto, NON é posible cambiar os nomes deste ficheiro de preconfiguración a menos que primeiro importe os datos de exemplo nun sistema de destino utilizando estes nomes, logo cambie o nome dos recursos reservables ao nome que desexe xunto cos rexistros de usuarios habilitados e, a seguir, exporte os datos de novo para importalos no sistema de destino final (actualizando as entradas antigas e novas de **ImportUserMapFile.xml** en consecuencia).

- **\<PluginsToDisable\>** especifica complementos de elemento de liña moi discretos que é necesario desactivar durante a importación de datos de exemplo e volver a activar posteriormente.

### <a name="fabrikam-robotics-fictitious-scenario"></a>Escenario ficticio Fabrikam Robotics

Os paquetes de datos de referencia de Field Service e Project Service instalan a **Solución de datos Fabrikam Manufacturing Master Data (v3.0.0.0)**, xunto con aproximadamente 4000 rexistros e aproximadamente 40 entidades distintas. Los paquetes separados de datos de exemplo para Field Service ou Project Service conteñen un subconxunto dos datos de exemplo **v902FPSMasterData** desa aplicación. O paquete de **Datos de demostración** instala a **solución Fabrikam Manufacturing Demo Data (v3.0.0.7)** con aproximadamente 22 000 rexistros de 148 entidades.

A empresa ficticia Fabrikam Robotics é fabricante de robots de liña de montaxe de dispositivos electrónicos e é coñecida pola calidade dos seus produtos, a innovación e a sólida atención ao cliente, incluídos servizos de planificación de instalación, implementación e mantemento continuo. Fabrikam ten a súa sede en Estados Unidos (Fabrikam Estados Unidos) e ten operacións de servizo baseadas en proxectos en Francia, India, Reino Unido e Suíza.

As operacións de servizo de campo céntranse en Estados Unidos, sobre todo na área do gran Seattle. La empresa céntrase en sacar proveito da conectividade de Internet das Cousas (IoT) para supervisar o rendemento dos activos do cliente e para ofrecer servizos proactivos nas instalacións.

A continuación ofrécese un resumo de alto nivel dos datos de exemplo:

- Elementos de datos de exemplo comúns (incluídos para ambas aplicacións)

    - 1 usuario

    - 71 contas

    - 137 contactos

    - Diferentes tipos e categorías de transaccións

    - 50 produtos con 1 lista de prezos de produtos

    - 14 listas de prezos/custos

    - 31 características (cualificacións de recursos) en 2 modelos de clasificación con 3 niveis (valores de clasificación)

- Project Service

    - 8 unidades organizativas

    - 6 niveis de uso específicos do rol

    - Más de 2800 especificacións de prezos de rol

- Field Service

    - 4 zonas de vendas

    - 5 tipos de orde de traballo

    - 22 activos de cliente

    - 9 tipos de incidentes cun intervalo de características de recurso asociadas (9), servizos (13) e tarefas de servizo (13)
   
O paquete de **Datos de demostración** instala aproximadamente 179 pedidos de traballo, 12 proxectos e datos transaccionais asociados. 

### <a name="change-the-work-hours-for-sample-resources"></a>Cambiar as horas laborables para recursos de exemplo

Por defecto, todos os recursos reservables teñen un calendario de 24 horas laborables.

Se necesita cambiar as horas laborables dos recursos reservables de exemplo, vaia a **Universal Resource Scheduling** > **Programación** > **Recursos**.

Seleccione un usuario (por exemplo, Spencer Low) e cambie as horas laborables de Spencer polas horas que desexe aplicar a varios usuarios. Vaia a **Universal Resource Scheduling** > **Configuración** > **Modelos de horas laborables** e edite o rexistro **Modelo de traballo predeterminado**. No campo **Recurso de modelo**, seleccione un usuario coas horas laborables que desexe aplicar a outros recursos. Vaia a **Universal Resource Scheduling** > **Programación** > **Recursos** > **Recursos reservables activos**. Seleccione os recursos que desexe cambiar e, a seguir, seleccione **Establecer calendario**. Na lista despregable **Modelo de traballo** , seleccione o modelo **Hora laborable predefinida** ou outro modelo co recurso de modelo correcto. Cando vaia ao panel de programación, verá que os recursos agora teñen horas laborables actualizadas.

> [!div class="mx-imgBorder"]
> ![Captura de pantalla de recursos reservables activos.](media/sample-data-6.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]