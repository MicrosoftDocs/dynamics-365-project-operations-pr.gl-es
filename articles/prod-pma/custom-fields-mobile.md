---
title: Implementar campos personalizados para a aplicación móbil Microsoft Dynamics 365 Project Timesheet en iOS e Android
description: Este tema ofrece patróns comúns para usar extensións para implementar campos personalizados.
author: Yowelle
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 9f19a6d069c4f825be8515a6d26739c50d3b064698fc1872ede07a4e74ee4dcb
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7005749"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a>Implementar campos personalizados para a aplicación móbil Microsoft Dynamics 365 Project Timesheet en iOS e Android

[!include [banner](../includes/banner.md)]

Este tema ofrece patróns comúns para usar extensións para implementar campos personalizados. Trátanse os seguintes temas:

- Os distintos tipos de datos que admite o marco de campo personalizado
- Como amosar campos de só lectura ou editables nas entradas da folla de control horario e gardar os valores proporcionados polo usuario na base de datos
- Como amosar campos de só lectura na cabeceira da folla de control horario
- Como integrar outra lóxica empresarial personalizada para introducir valores predefinidos nos campos e facer validación adicional

## <a name="audience"></a>Audiencia

Este tema está destinado aos programadores que integran os seus campos personalizados na aplicación móbil Microsoft Dynamics 365 Project Timesheet dispoñible para Apple iOS e Google Android. A suposición é que os lectores están familiarizados co desenvolvemento de X++ e a funcionalidade da folla de control horario do proxecto.

## <a name="data-contract--tstimesheetcustomfield-x-class"></a>Contrato de datos - clase TSTimesheetCustomField X++

A clase **TSTimesheetCustomField** é a clase de contrato de datos X++ que representa información sobre un campo personalizado para a funcionalidade da folla de control horario. As listas dos obxectos de campo personalizados pásanse tanto ao contrato de datos TSTimesheetDetails como ao contrato de datos TSTimesheetEntry para amosar campos personalizados na aplicación móbil.

- **TSTimesheetDetails** - O contrato de cabeceira da folla de control horario.
- **TSTimesheetEntry** - O contrato de transacción de folla de control horario. Os grupos destes obxectos que teñen a mesma información do proxecto e o valor **timesheetLineRecId** constitúen unha liña.

### <a name="fieldbasetype-types"></a>fieldBaseType (Tipos)

A propiedade **FieldBaseType** no obxecto **TsTimesheetCustom** determina o tipo de campo que aparece na aplicación. Admítense os seguintes valores de **Tipos**.

| Valor de tipos | Tipo              | Notas |
|-------------|-------------------|-------|
| 0           | Cadea (e Enum) | O campo aparece como un campo de texto. |
| 1           | Integer           | O valor móstrase como un número sen cifras decimais. |
| 2           | Real              | O valor móstrase como un número que ten cifras decimais.<p>Para amosar o valor real como moeda na aplicación, use a propiedade **fieldExtenededType**. Pode usar a propiedade **numberOfDecimals** para establecer o número de decimais que se amosan.</p> |
| 3           | Data              | Os formatos de data están determinados pola configuración do usuario **Formato de datas, horas e números** que se especifica en **Idioma e preferencia de país/rexión** en **Opcións do usuario**. |
| 4           | Boolean           | |
| 15          | GUID              | |
| 16          | Int64             | |

- Se a propiedade **stringOptions** non se fornece no obxecto **TSTimesheetCustomField**, fornécese ao usuario un campo de texto libre.

    A propiedade **stringLength** pode usarse para establecer a lonxitude máxima da cadea que poden introducir os usuarios.

- Se a propiedade **stringOptions** se fornece no obxecto **TSTimesheetCustomField**, eses elementos da lista son os únicos valores que os usuarios poden seleccionar usando os botóns de opción.

    Neste caso, o campo de cadea pode actuar como un valor inicial para os fins da entrada do usuario. Para gardar o valor na base de datos como unha enumeración, asigne manualmente o valor da cadea ao valor enumerado antes de gardalo na base de datos empregando a cadea de comando (consulte a sección "Usar a cadea de comando na clase TSTimesheetEntryService para gardar unha entrada de folla de control horario da aplicación de novo na base de datos" máis adiante neste tema para ver un exemplo).

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a>fieldExtendedType (TSCustomFieldExtendedType)

Pode usar esta propiedade para formatear valores reais como a moeda. Este método só se aplica cando o valor **fieldBaseType** é **Real**.

- **TSCustomFieldExtendedType:None** – Non se aplica ningún formato.
- **TSCustomFieldExtendedType::Moeda** – Formatee o valor como moeda.

    Cando o formato de moeda está activo, o campo **stringValue** pode usarse despois do código de moeda que debería amosarse na aplicación. O valor é un valor de só lectura.

    O campo **realValue** contén a cantidade de diñeiro que se debe gardarse na base de datos.

### <a name="fieldsection-tscustomfieldsection"></a>fieldSection (TSCustomFieldSection)

Pode usar esta propiedade para especificar onde debería aparecer o campo personalizado na aplicación.

- **TSCustomFieldSection::Cabeceira** - O campo aparecerá na sección **Ver máis detalles** na aplicación. Estes campos son sempre de só lectura.
- **TSCustomFieldSection::Liña** - O campo aparecerá despois de todos os campos de liña listos para usar nas entradas da folla de control horario. Estes campos poden ser editables ou de só lectura.

### <a name="fieldname-fieldnameshort"></a>fieldName (FieldNameShort)

Esta propiedade identifica o campo cando os valores que proporciona a aplicación volven gardarse na base de datos.

### <a name="tablename-tablenameshort"></a>tableName (TableNameShort)

Esta propiedade identifica o campo cando os valores que proporciona a aplicación volven gardarse na base de datos.

### <a name="iseditable-noyes"></a>isEditable (NoYes)

Estableza esta propiedade en **Si** para especificar que os usuarios poden editar o campo da sección de entrada de folla de control horario. Estableza a propiedade en **Non** para que o campo sexa de só lectura.

### <a name="ismandatory-noyes"></a>isMandatory (NoYes)

Estableza esta propiedade en **Si** para especificar que o campo da sección de entrada de folla de control horario debe ser obrigatorio.

### <a name="label-str"></a>etiqueta (str)

Esta propiedade especifica a etiqueta que se mostra a continuación do campo na aplicación.

### <a name="stringoptions-list-of-strings"></a>stringOptions (Lista de cadeas)

Esta propiedade só se aplica cando **fieldBaseType** está establecido en **Cadea**. Se **stringOptions** está definido, os valores das cadeas dispoñibles para a selección mediante botóns de opción especifícanse nas cadeas da lista. Se non se proporcionan cadeas, permítese a entrada de texto libre no campo da cadea (consulte a sección "Usar a cadea de comando na clase TSTimesheetEntryService para gardar unha entrada de folla de control horario da aplicación de novo na base de datos" máis adiante neste tema para ver un exemplo) .

### <a name="stringlength-int"></a>stringLength (int)

Esta propiedade especifica a lonxitude máxima dun campo de cadea. Só se aplica cando **fieldBaseType** está establecido en **Cadea**.

### <a name="numberofdecimals-int"></a>numberOfDecimals (int)

Esta propiedade especifica o número de decimais que se amosan para un campo real. Só se aplica cando **fieldBaseType** está establecido en **Real**.

### <a name="ordersequence-int"></a>orderSequence (int)

Esta propiedade controla a orde na que se mostran os campos personalizados na aplicación cando se especifica máis dun campo personalizado. Os campos que teñen un número inferior móstranse primeiro.

### <a name="booleanvalue-boolean"></a>booleanValue (boolean)

Para campos do tipo **Booleano**, esta propiedade pasa o valor booleano do campo entre o servidor e a aplicación.

### <a name="guidvalue-guid"></a>guidValue (guid)

Para campos do tipo **GUID**, esta propiedade pasa o valor de identificador único global (GUID) do campo entre o servidor e a aplicación.

### <a name="int64value-int64"></a>int64Value (int64)

Para campos do tipo **Int64**, esta propiedade pasa o valor de int64 do campo entre o servidor e a aplicación.

### <a name="intvalue-int"></a>intValue (int)

Para campos do tipo **Int**, esta propiedade pasa o valor de int do campo entre o servidor e a aplicación.

### <a name="realvalue-real"></a>realValue (real)

Para campos do tipo **Real**, esta propiedade pasa o valor real do campo entre o servidor e a aplicación.

### <a name="stringvalue-str"></a>stringValue (str)

Para campos do tipo **Cadea**, esta propiedade pasa o valor de cadea do campo entre o servidor e a aplicación. Tamén se usa para campos do tipo **Real** que teñen o formato de moeda. Para eses campos, a propiedade úsase para pasar o código de moeda á aplicación.

### <a name="datevalue-date"></a>dateValue (data)

Para campos do tipo **Data**, esta propiedade pasa o valor de data do campo entre o servidor e a aplicación.

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a>Mostrar e gardar un campo personalizado na sección de entrada de folla de control horario

A continuación móstrase unha captura de pantalla da aplicación móbil da creación dunha entrada de folla de control horario. Mostra os campos listos para usar e un campo personalizado na sección "Entrada de tempo" chamado "Cadea de proba" cun valor enum de "Segunda opción" xa definido.

![Probar campo personalizado de cadea na aplicación.](media/timesheet-entry.jpg)



A continuación móstrase unha captura de pantalla da aplicación móbil do usuario que selecciona unha das opcións de enum dispoñibles para o campo personalizado "Cadea de proba".  As dúas opcións son "Primeira opción" e "Segunda opción" que se amosan como botóns de opción. A segunda opción está seleccionada actualmente.

![Botóns de opción para o campo personalizado da cadea de proba.](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a>Amplíe a táboa TSTimesheetLine para que teña un campo personalizado

En escenarios típicos, é probable que os datos dun campo personalizado na sección de entrada de folla de control horario se garden na táboa TSTimesheetLine. Non obstante, pódense usar outras táboas se os datos se poden recuperar segundo un rexistro de TSTimesheetTrans que se proporciona ou se non teñen un contexto de rexistro específico (por exemplo, se o campo está configurado como de só lectura nos parámetros do proxecto).

Teña en conta que os campos personalizados non teñen que ter ningún rexistro de base de datos de respaldo. Pódense xerar dinámicamente segundo a lóxica de X++. Este método pode ser útil en escenarios de só lectura (consulte a sección "Usar cadea de comando na clase TSTimesheetDetails, método buildCustomFieldListForHeader para encher os detalles da folla de control horario" para ver un exemplo de valores de campo personalizados xerados dinámicamente).

Debaixo móstrase unha captura de pantalla de Visual Studio da árbore de obxectos da aplicación. Mostra unha extensión da táboa TSTimesheetLine co campo TestLineString engadido como campo personalizado.

![Cadea de liña.](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a>Usar a cadea de comando no método buildCustomFieldList da clase TSTimesheetSettings para amosar un campo na sección de entrada de folla de control horario

Este código controla a configuración de visualización do campo na aplicación. Por exemplo, controla o tipo de campo, a etiqueta, se o campo é obrigatorio e en que sección aparece o campo.

O seguinte exemplo mostra un campo de cadea nas entradas de tempo. Este campo ten dúas opcións, **Primeira opción** e **Segunda opción**, que están dispoñibles a través dos botóns de opción. O campo da aplicación está asociado ao campo **TestLineString** que se engade á táboa TSTimesheetLine.

Teña en conta o uso do método **TSTimesheetCustomField::newFromMetatdata()** para simplificar a inicialización das propiedades do campo personalizado: **fieldBaseType**, **tableName**, **filedname**, **label**, **isEditable**, **isMandatory**, **stringLength** e **numberOfDecimals**. Tamén pode configurar estes parámetros manualmente, como prefira.

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a>Usar a cadea de comando no método buildCustomFieldListForEntry da clase TSTimesheetEntry para introducir valores nunha entrada de folla de control horario

O método **buildCustomFieldListForEntry** úsase para introducir valores nas liñas de folla de control horario gardadas na aplicación móbil. Toma un rexistro de TSTimesheetTrans como parámetro. Os campos dese rexistro pódense empregar para encher o valor do campo personalizado na aplicación.

```xpp
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a>Usar a cadea de comando na clase TSTimesheetEntryService para gardar unha entrada de folla control horario da aplicación de novo na base de datos

Para gardar un campo personalizado de novo na base de datos no uso normal, debe ampliar varios métodos:

- O método **timesheetLineNeedsUpdating** úsase para determinar se o usuario cambiou o rexistro de liña na aplicación e debe gardarse na base de datos. Se o rendemento non importa, este método pode simplificarse para que sempre sexa **true**.
- Os métodos **populateTimesheetLineFromEntryDuringCreate** e **populateTimesheetLineFromEntryDuringUpdate** pódense ampliar para que introduzan valores no rexistro da base de datos de TSTimesheetLine desde o contrato de datos de TSTimesheetEntry que se fornece. No exemplo seguinte, observe como a asignación entre o campo de base de datos e o campo de entrada faise manualmente a través do código de X++.
- O método **populateTimesheetWeekFromEntry** tamén se pode estender se o campo personalizado que está asignado ao obxecto de **TSTimesheetEntry** escribir de novo na táboa de base de datos TSTimesheetLineweek.

> [!NOTE]
> O seguinte exemplo garda o valor **firstOption** ou **secondOption** que o usuario selecciona na base de datos como un valor de cadea en bruto. Se o campo da base de datos é un campo do tipo **Enum**, eses valores pódense asignar manualmente a un valor enum e despois gardalos nun campo enum da táboa da base de datos.

```xpp
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a>Mostrar un campo personalizado na sección de cabeceira de folla de control horario

A continuación móstrase unha captura de pantalla da aplicación móbil dun usuario visualizando unha folla de control horario. Na esquina superior dereita seleccionouse o botón "Máis información" para amosar a opción "Ver máis detalles".  

![Comando de visualizar máis detalles.](media/show-more.png)

A continuación móstrase unha captura de pantalla da aplicación móbil que mostra a sección "Máis" dunha folla de control horario. Engadiuse un campo personalizado chamado "Taxa de utilización desta folla de control horario (campo personalizado computado)" á sección de cabeceira da folla de control horario. No campo personalizado establécese un valor de só lectura de "0,667".

![Sección Máis.](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a>Amplíe a táboa TSTimesheetTable para que teña un campo personalizado

En escenarios típicos, é probable que os datos dun campo personalizado na sección de cabeceira se tomen da táboa TSTimesheetHeader. Non obstante, pódense usar outras táboas se os datos se poden recuperar segundo un rexistro de TSTimesheetTable que se proporciona ou se non teñen un contexto de rexistro específico (por exemplo, se o campo está configurado como de só lectura nos parámetros do proxecto).

Teña en conta que os campos personalizados non teñen que ter ningún rexistro de base de datos de respaldo. Pódense xerar dinámicamente segundo a lóxica de X++. O exemplo que segue mostra este método.

Os campos da sección de cabeceira sempre son de só lectura na aplicación.

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a>Usar a cadea de comando no método buildCustomFieldList da clase TSTimesheetSettings para amosar un campo na sección de cabeceira

Este código controla a configuración de visualización do campo na aplicación. Por exemplo, controla o tipo de campo, a etiqueta, se o campo é obrigatorio e en que sección aparece o campo.

O seguinte exemplo mostra un valor calculado na sección de cabeceira da aplicación.

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a>Usar a cadea de comando no método buildCustomFieldListForHeader da clase TSTimesheetDetails para encher os detalles da folla de control horario

O método **buildCustomFieldListForHeader** úsase para encher os detalles da cabeceira da folla de control horario na aplicación móbil. Toma un rexistro de TSTimesheetTable como parámetro. Os campos dese rexistro pódense empregar para encher o valor do campo personalizado na aplicación. O seguinte exemplo non le ningún valor da base de datos. En vez diso, usa a lóxica de X++ para xerar un valor calculado que despois se mostra na aplicación.


```xpp
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a>Outras oportunidades de configurabilidade/extensibilidade

### <a name="adding-additional-validation-for-the-app"></a>Engadir validación adicional para a aplicación

A lóxica existente para a funcionalidade da folla de control horario a nivel de base de datos aínda funcionará como se esperaba. Para interromper a realización das operacións de gardar ou enviar e amosar unha mensaxe de erro específica, pode engadir **erro de lanzamento ("mensaxe ao usuario")** ao código mediante unha cadea de extensión de comando. Aquí ten tres exemplos de métodos extensibles útiles:

- Se **validateWrite** na táboa TSTimesheetLine mostra **false** durante unha operación de gardado para unha liña de folla de control horario, móstrase unha mensaxe de erro na aplicación móbil.
- Se **validateSubmit** na táboa TSTimesheetTable mostra **false** durante o envío da folla de control horario na aplicación, móstrase unha mensaxe de erro ao usuario.
- A lóxica que enche campos (por exemplo, **Propiedade de liña**) durante o método **inserir** na táboa TSTimesheetLine aínda se executará.

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a>Ocultar e marcar campos listos para usar como de só lectura mediante configuración

Desde os parámetros do proxecto, pode facer que os campos listos para usar sexan só de lectura ou estean ocultos na aplicación móbil. Estableza as opcións na sección **Follas de de control horario móbiles** no separador **Folla de control horario** da páxina **Parámetros de xestión de proxectos e contabilidad**.

![Parámetros do proxecto.](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a>Cambiar as actividades dispoñibles para a selección mediante extensións

As actividades dispoñibles para a selección dun proxecto énchense a través dos métodos **getActivitiesForProject()** e **getActivityQuery()** na clase **TsTimesheetProjectService**. Pode usar a cadea de mando para cambiar este comportamento para que coincida co seu escenario emprearial para as actividades dispoñibles para a selección dun proxecto específico.

### <a name="entering-a-default-project-category-on-timesheet-entries"></a>Introdución dunha categoría de proxecto predefinida nas entradas da folla de control horario

A entrada dunha categoría de proxecto predefinida nas entradas de folla de control horario prodúcese en tres niveis. Podes usar a cadea de mando para estender o comportamento en calquera ou en todos estes niveis para conseguir o comportamento desexado. Emprégase a seguinte xerarquía:

1. A aplicación tenta poñer a categoría predefinida do recurso do proxecto. Esta categoría predefinida establécese nos métodos **getCurrentUserResource** e **getDelegatedResourcesForCurrentUser** na clase **TSTimesheetSettingsService**.
2. Se a categoría predefinida non se proporciona no nivel de recursos do proxecto, a aplicación tenta tomala da actividade do proxecto. Esta categoría predefinida establécese no método **getActivitiesForProject** na clase **TSTimesheetProjectService**.
3. Se a categoría predefinida non se proporciona no nivel de actividade do proxecto, a categoría predefinida tómase dos parámetros do proxecto. Esta categoría predefinida establécese no método **getProjectDetailsbyRule** na clase **TSTimesheetProjectService**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]