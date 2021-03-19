---
title: Implementar campos personalizados para a aplicación móbil Microsoft Dynamics 365 Project Timesheet en iOS e Android
description: Este tema ofrece patróns comúns para usar extensións para implementar campos personalizados.
author: Yowelle
manager: AnnBe
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 5dae571fce746b49281587f5349774a7f2c4111b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: gl-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270991"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a><span data-ttu-id="a4ba9-103">Implementar campos personalizados para a aplicación móbil Microsoft Dynamics 365 Project Timesheet en iOS e Android</span><span class="sxs-lookup"><span data-stu-id="a4ba9-103">Implement custom fields for the Microsoft Dynamics 365 Project Timesheet mobile app on iOS and Android</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a4ba9-104">Este tema ofrece patróns comúns para usar extensións para implementar campos personalizados.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-104">This topic provides common patterns for using extensions to implement custom fields.</span></span> <span data-ttu-id="a4ba9-105">Trátanse os seguintes temas:</span><span class="sxs-lookup"><span data-stu-id="a4ba9-105">The following topics are covered:</span></span>

- <span data-ttu-id="a4ba9-106">Os distintos tipos de datos que admite o marco de campo personalizado</span><span class="sxs-lookup"><span data-stu-id="a4ba9-106">The various data types that the custom field framework supports</span></span>
- <span data-ttu-id="a4ba9-107">Como amosar campos de só lectura ou editables nas entradas da folla de control horario e gardar os valores proporcionados polo usuario na base de datos</span><span class="sxs-lookup"><span data-stu-id="a4ba9-107">How to show read-only or editable fields on timesheet entries, and save user-provided values back to the database</span></span>
- <span data-ttu-id="a4ba9-108">Como amosar campos de só lectura na cabeceira da folla de control horario</span><span class="sxs-lookup"><span data-stu-id="a4ba9-108">How to show read-only fields on the timesheet header</span></span>
- <span data-ttu-id="a4ba9-109">Como integrar outra lóxica empresarial personalizada para introducir valores predefinidos nos campos e facer validación adicional</span><span class="sxs-lookup"><span data-stu-id="a4ba9-109">How to integrate other custom business logic to enter default values in fields and do additional validation</span></span>

## <a name="audience"></a><span data-ttu-id="a4ba9-110">Audiencia</span><span class="sxs-lookup"><span data-stu-id="a4ba9-110">Audience</span></span>

<span data-ttu-id="a4ba9-111">Este tema está destinado aos programadores que integran os seus campos personalizados na aplicación móbil Microsoft Dynamics 365 Project Timesheet dispoñible para Apple iOS e Google Android.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-111">This topic is intended for developers who are integrating their custom fields into the Microsoft Dynamics 365 Project Timesheet mobile application that is available for Apple iOS and Google Android.</span></span> <span data-ttu-id="a4ba9-112">A suposición é que os lectores están familiarizados co desenvolvemento de X++ e a funcionalidade da folla de control horario do proxecto.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-112">The assumption is that readers are familiar with X++ development and project timesheet functionality.</span></span>

## <a name="data-contract--tstimesheetcustomfield-x-class"></a><span data-ttu-id="a4ba9-113">Contrato de datos - clase TSTimesheetCustomField X++</span><span class="sxs-lookup"><span data-stu-id="a4ba9-113">Data contract – TSTimesheetCustomField X++ class</span></span>

<span data-ttu-id="a4ba9-114">A clase **TSTimesheetCustomField** é a clase de contrato de datos X++ que representa información sobre un campo personalizado para a funcionalidade da folla de control horario.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-114">The **TSTimesheetCustomField** class is the X++ data contract class that represents information about a custom field for timesheet functionality.</span></span> <span data-ttu-id="a4ba9-115">As listas dos obxectos de campo personalizados pásanse tanto ao contrato de datos TSTimesheetDetails como ao contrato de datos TSTimesheetEntry para amosar campos personalizados na aplicación móbil.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-115">Lists of the custom field objects are passed on both the TSTimesheetDetails data contract and the TSTimesheetEntry data contract to show custom fields in the mobile app.</span></span>

- <span data-ttu-id="a4ba9-116">**TSTimesheetDetails** - O contrato de cabeceira da folla de control horario.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-116">**TSTimesheetDetails** - The timesheet header contract.</span></span>
- <span data-ttu-id="a4ba9-117">**TSTimesheetEntry** - O contrato de transacción de folla de control horario.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-117">**TSTimesheetEntry** - The timesheet transaction contract.</span></span> <span data-ttu-id="a4ba9-118">Os grupos destes obxectos que teñen a mesma información do proxecto e o valor **timesheetLineRecId** constitúen unha liña.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-118">Groups of these objects that have the same project information and **timesheetLineRecId** value constitute a line.</span></span>

### <a name="fieldbasetype-types"></a><span data-ttu-id="a4ba9-119">fieldBaseType (Tipos)</span><span class="sxs-lookup"><span data-stu-id="a4ba9-119">fieldBaseType (Types)</span></span>

<span data-ttu-id="a4ba9-120">A propiedade **FieldBaseType** no obxecto **TsTimesheetCustom** determina o tipo de campo que aparece na aplicación.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-120">The **FieldBaseType** property on the **TsTimesheetCustom** object determines the type of the field that appears in the app.</span></span> <span data-ttu-id="a4ba9-121">Admítense os seguintes valores de **Tipos**.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-121">The following **Types** values that are supported.</span></span>

| <span data-ttu-id="a4ba9-122">Valor de tipos</span><span class="sxs-lookup"><span data-stu-id="a4ba9-122">Types value</span></span> | <span data-ttu-id="a4ba9-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="a4ba9-123">Type</span></span>              | <span data-ttu-id="a4ba9-124">Notas</span><span class="sxs-lookup"><span data-stu-id="a4ba9-124">Notes</span></span> |
|-------------|-------------------|-------|
| <span data-ttu-id="a4ba9-125">0</span><span class="sxs-lookup"><span data-stu-id="a4ba9-125">0</span></span>           | <span data-ttu-id="a4ba9-126">Cadea (e Enum)</span><span class="sxs-lookup"><span data-stu-id="a4ba9-126">String (and Enum)</span></span> | <span data-ttu-id="a4ba9-127">O campo aparece como un campo de texto.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-127">The field appears as a text field.</span></span> |
| <span data-ttu-id="a4ba9-128">1</span><span class="sxs-lookup"><span data-stu-id="a4ba9-128">1</span></span>           | <span data-ttu-id="a4ba9-129">Integer</span><span class="sxs-lookup"><span data-stu-id="a4ba9-129">Integer</span></span>           | <span data-ttu-id="a4ba9-130">O valor móstrase como un número sen cifras decimais.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-130">The value is shown as a number without decimal places.</span></span> |
| <span data-ttu-id="a4ba9-131">2</span><span class="sxs-lookup"><span data-stu-id="a4ba9-131">2</span></span>           | <span data-ttu-id="a4ba9-132">Real</span><span class="sxs-lookup"><span data-stu-id="a4ba9-132">Real</span></span>              | <span data-ttu-id="a4ba9-133">O valor móstrase como un número que ten cifras decimais.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-133">The value is shown as a number that has decimal places.</span></span><p><span data-ttu-id="a4ba9-134">Para amosar o valor real como moeda na aplicación, use a propiedade **fieldExtenededType**.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-134">To show the real value as a currency in the app, use the **fieldExtenededType** property.</span></span> <span data-ttu-id="a4ba9-135">Pode usar a propiedade **numberOfDecimals** para establecer o número de decimais que se amosan.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-135">You can use the **numberOfDecimals** property to set the number of decimal places that are shown.</span></span></p> |
| <span data-ttu-id="a4ba9-136">3</span><span class="sxs-lookup"><span data-stu-id="a4ba9-136">3</span></span>           | <span data-ttu-id="a4ba9-137">Data</span><span class="sxs-lookup"><span data-stu-id="a4ba9-137">Date</span></span>              | <span data-ttu-id="a4ba9-138">Os formatos de data están determinados pola configuración do usuario **Formato de datas, horas e números** que se especifica en **Idioma e preferencia de país/rexión** en **Opcións do usuario**.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-138">Date formats are determined by the user's **Date, times, and number format** setting that is specified under **Language and country/region preference** in **User options**.</span></span> |
| <span data-ttu-id="a4ba9-139">4</span><span class="sxs-lookup"><span data-stu-id="a4ba9-139">4</span></span>           | <span data-ttu-id="a4ba9-140">Boolean</span><span class="sxs-lookup"><span data-stu-id="a4ba9-140">Boolean</span></span>           | |
| <span data-ttu-id="a4ba9-141">15</span><span class="sxs-lookup"><span data-stu-id="a4ba9-141">15</span></span>          | <span data-ttu-id="a4ba9-142">GUID</span><span class="sxs-lookup"><span data-stu-id="a4ba9-142">GUID</span></span>              | |
| <span data-ttu-id="a4ba9-143">16</span><span class="sxs-lookup"><span data-stu-id="a4ba9-143">16</span></span>          | <span data-ttu-id="a4ba9-144">Int64</span><span class="sxs-lookup"><span data-stu-id="a4ba9-144">Int64</span></span>             | |

- <span data-ttu-id="a4ba9-145">Se a propiedade **stringOptions** non se fornece no obxecto **TSTimesheetCustomField**, fornécese ao usuario un campo de texto libre.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-145">If the **stringOptions** property isn't provided on the **TSTimesheetCustomField** object, a free-text field is provided to the user.</span></span>

    <span data-ttu-id="a4ba9-146">A propiedade **stringLength** pode usarse para establecer a lonxitude máxima da cadea que poden introducir os usuarios.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-146">The **stringLength** property can be used to set the maximum string length that users can enter.</span></span>

- <span data-ttu-id="a4ba9-147">Se a propiedade **stringOptions** se fornece no obxecto **TSTimesheetCustomField**, eses elementos da lista son os únicos valores que os usuarios poden seleccionar usando os botóns de opción.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-147">If the **stringOptions** property is provided on the **TSTimesheetCustomField** object, those list elements are the only values that users can select by using option buttons (radio buttons).</span></span>

    <span data-ttu-id="a4ba9-148">Neste caso, o campo de cadea pode actuar como un valor inicial para os fins da entrada do usuario.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-148">In this case, the string field can act as an enum value for the purpose of user entry.</span></span> <span data-ttu-id="a4ba9-149">Para gardar o valor na base de datos como unha enumeración, asigne manualmente o valor da cadea ao valor enumerado antes de gardalo na base de datos empregando a cadea de comando (consulte a sección "Usar a cadea de comando na clase TSTimesheetEntryService para gardar unha entrada de folla de control horario da aplicación de novo na base de datos" máis adiante neste tema para ver un exemplo).</span><span class="sxs-lookup"><span data-stu-id="a4ba9-149">To save the value to the database as an enum, manually map the string value back to the enum value before you save to the database by using chain of command (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a><span data-ttu-id="a4ba9-150">fieldExtendedType (TSCustomFieldExtendedType)</span><span class="sxs-lookup"><span data-stu-id="a4ba9-150">fieldExtendedType (TSCustomFieldExtendedType)</span></span>

<span data-ttu-id="a4ba9-151">Pode usar esta propiedade para formatear valores reais como a moeda.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-151">You can use this property to format real values as currency.</span></span> <span data-ttu-id="a4ba9-152">Este método só se aplica cando o valor **fieldBaseType** é **Real**.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-152">This approach is applicable only when the **fieldBaseType** value is **Real**.</span></span>

- <span data-ttu-id="a4ba9-153">**TSCustomFieldExtendedType:None** – Non se aplica ningún formato.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-153">**TSCustomFieldExtendedType:None** – No formatting is applied.</span></span>
- <span data-ttu-id="a4ba9-154">**TSCustomFieldExtendedType::Moeda** – Formatee o valor como moeda.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-154">**TSCustomFieldExtendedType::Currency** – Format the value as currency.</span></span>

    <span data-ttu-id="a4ba9-155">Cando o formato de moeda está activo, o campo **stringValue** pode usarse despois do código de moeda que debería amosarse na aplicación.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-155">When currency formatting is active, the **stringValue** field can be used pass the currency code that should be shown in the app.</span></span> <span data-ttu-id="a4ba9-156">O valor é un valor de só lectura.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-156">The value is a read-only value.</span></span>

    <span data-ttu-id="a4ba9-157">O campo **realValue** contén a cantidade de diñeiro que se debe gardarse na base de datos.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-157">The **realValue** field contains the money amount that should be saved to the database.</span></span>

### <a name="fieldsection-tscustomfieldsection"></a><span data-ttu-id="a4ba9-158">fieldSection (TSCustomFieldSection)</span><span class="sxs-lookup"><span data-stu-id="a4ba9-158">fieldSection (TSCustomFieldSection)</span></span>

<span data-ttu-id="a4ba9-159">Pode usar esta propiedade para especificar onde debería aparecer o campo personalizado na aplicación.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-159">You can use this property specify where the custom field should appear in the app.</span></span>

- <span data-ttu-id="a4ba9-160">**TSCustomFieldSection::Cabeceira** - O campo aparecerá na sección **Ver máis detalles** na aplicación.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-160">**TSCustomFieldSection::Header** – The field will appear in the **View more details** section in the app.</span></span> <span data-ttu-id="a4ba9-161">Estes campos son sempre de só lectura.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-161">These fields are always read-only.</span></span>
- <span data-ttu-id="a4ba9-162">**TSCustomFieldSection::Liña** - O campo aparecerá despois de todos os campos de liña listos para usar nas entradas da folla de control horario.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-162">**TSCustomFieldSection::Line** – The field will appear after all the out-of-box line fields on timesheet entries.</span></span> <span data-ttu-id="a4ba9-163">Estes campos poden ser editables ou de só lectura.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-163">These fields can be either editable or read-only.</span></span>

### <a name="fieldname-fieldnameshort"></a><span data-ttu-id="a4ba9-164">fieldName (FieldNameShort)</span><span class="sxs-lookup"><span data-stu-id="a4ba9-164">fieldName (FieldNameShort)</span></span>

<span data-ttu-id="a4ba9-165">Esta propiedade identifica o campo cando os valores que proporciona a aplicación volven gardarse na base de datos.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-165">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="tablename-tablenameshort"></a><span data-ttu-id="a4ba9-166">tableName (TableNameShort)</span><span class="sxs-lookup"><span data-stu-id="a4ba9-166">tableName (TableNameShort)</span></span>

<span data-ttu-id="a4ba9-167">Esta propiedade identifica o campo cando os valores que proporciona a aplicación volven gardarse na base de datos.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-167">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="iseditable-noyes"></a><span data-ttu-id="a4ba9-168">isEditable (NoYes)</span><span class="sxs-lookup"><span data-stu-id="a4ba9-168">isEditable (NoYes)</span></span>

<span data-ttu-id="a4ba9-169">Estableza esta propiedade en **Si** para especificar que os usuarios poden editar o campo da sección de entrada de folla de control horario.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-169">Set this property to **Yes** to specify that the field in the timesheet entry section should be editable by users.</span></span> <span data-ttu-id="a4ba9-170">Estableza a propiedade en **Non** para que o campo sexa de só lectura.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-170">Set the property to **No** to make the field read-only.</span></span>

### <a name="ismandatory-noyes"></a><span data-ttu-id="a4ba9-171">isMandatory (NoYes)</span><span class="sxs-lookup"><span data-stu-id="a4ba9-171">isMandatory (NoYes)</span></span>

<span data-ttu-id="a4ba9-172">Estableza esta propiedade en **Si** para especificar que o campo da sección de entrada de folla de control horario debe ser obrigatorio.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-172">Set this property to **Yes** to specify that the field in the timesheet entry section should be mandatory.</span></span>

### <a name="label-str"></a><span data-ttu-id="a4ba9-173">etiqueta (str)</span><span class="sxs-lookup"><span data-stu-id="a4ba9-173">label (str)</span></span>

<span data-ttu-id="a4ba9-174">Esta propiedade especifica a etiqueta que se mostra a continuación do campo na aplicación.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-174">This property specifies the label that is shown next the field in the app.</span></span>

### <a name="stringoptions-list-of-strings"></a><span data-ttu-id="a4ba9-175">stringOptions (Lista de cadeas)</span><span class="sxs-lookup"><span data-stu-id="a4ba9-175">stringOptions (List of Strings)</span></span>

<span data-ttu-id="a4ba9-176">Esta propiedade só se aplica cando **fieldBaseType** está establecido en **Cadea**.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-176">This property is applicable only when **fieldBaseType** is set to **String**.</span></span> <span data-ttu-id="a4ba9-177">Se **stringOptions** está definido, os valores das cadeas dispoñibles para a selección mediante botóns de opción especifícanse nas cadeas da lista.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-177">If **stringOptions** is set, the string values that are available for selection via option buttons (radio buttons) are specified by the strings in the list.</span></span> <span data-ttu-id="a4ba9-178">Se non se proporcionan cadeas, permítese a entrada de texto libre no campo da cadea (consulte a sección "Usar a cadea de comando na clase TSTimesheetEntryService para gardar unha entrada de folla de control horario da aplicación de novo na base de datos" máis adiante neste tema para ver un exemplo) .</span><span class="sxs-lookup"><span data-stu-id="a4ba9-178">If no strings are provided, free-text entry in the string field is allowed (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="stringlength-int"></a><span data-ttu-id="a4ba9-179">stringLength (int)</span><span class="sxs-lookup"><span data-stu-id="a4ba9-179">stringLength (int)</span></span>

<span data-ttu-id="a4ba9-180">Esta propiedade especifica a lonxitude máxima dun campo de cadea.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-180">This property specifies the maximum length for a string field.</span></span> <span data-ttu-id="a4ba9-181">Só se aplica cando **fieldBaseType** está establecido en **Cadea**.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-181">It's applicable only when **fieldBaseType** is set to **String**.</span></span>

### <a name="numberofdecimals-int"></a><span data-ttu-id="a4ba9-182">numberOfDecimals (int)</span><span class="sxs-lookup"><span data-stu-id="a4ba9-182">numberOfDecimals (int)</span></span>

<span data-ttu-id="a4ba9-183">Esta propiedade especifica o número de decimais que se amosan para un campo real.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-183">This property specifies the number of decimal places that are shown for a real field.</span></span> <span data-ttu-id="a4ba9-184">Só se aplica cando **fieldBaseType** está establecido en **Real**.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-184">It's applicable only when **fieldBaseType** is set to **Real**.</span></span>

### <a name="ordersequence-int"></a><span data-ttu-id="a4ba9-185">orderSequence (int)</span><span class="sxs-lookup"><span data-stu-id="a4ba9-185">orderSequence (int)</span></span>

<span data-ttu-id="a4ba9-186">Esta propiedade controla a orde na que se mostran os campos personalizados na aplicación cando se especifica máis dun campo personalizado.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-186">This property controls the order in which the custom fields are shown in the app when more than one custom field is specified.</span></span> <span data-ttu-id="a4ba9-187">Os campos que teñen un número inferior móstranse primeiro.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-187">Fields that have lower numbers are shown first.</span></span>

### <a name="booleanvalue-boolean"></a><span data-ttu-id="a4ba9-188">booleanValue (boolean)</span><span class="sxs-lookup"><span data-stu-id="a4ba9-188">booleanValue (boolean)</span></span>

<span data-ttu-id="a4ba9-189">Para campos do tipo **Booleano**, esta propiedade pasa o valor booleano do campo entre o servidor e a aplicación.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-189">For fields of the **Boolean** type, this property passes the Boolean value of the field between the server and the app.</span></span>

### <a name="guidvalue-guid"></a><span data-ttu-id="a4ba9-190">guidValue (guid)</span><span class="sxs-lookup"><span data-stu-id="a4ba9-190">guidValue (guid)</span></span>

<span data-ttu-id="a4ba9-191">Para campos do tipo **GUID**, esta propiedade pasa o valor de identificador único global (GUID) do campo entre o servidor e a aplicación.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-191">For fields of the **GUID** type, this property passes the globally unique identifier (GUID) value of the field between the server and the app.</span></span>

### <a name="int64value-int64"></a><span data-ttu-id="a4ba9-192">int64Value (int64)</span><span class="sxs-lookup"><span data-stu-id="a4ba9-192">int64Value (int64)</span></span>

<span data-ttu-id="a4ba9-193">Para campos do tipo **Int64**, esta propiedade pasa o valor de int64 do campo entre o servidor e a aplicación.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-193">For fields of the **Int64** type, this property passes the int64 value of the field between the server and the app.</span></span>

### <a name="intvalue-int"></a><span data-ttu-id="a4ba9-194">intValue (int)</span><span class="sxs-lookup"><span data-stu-id="a4ba9-194">intValue (int)</span></span>

<span data-ttu-id="a4ba9-195">Para campos do tipo **Int**, esta propiedade pasa o valor de int do campo entre o servidor e a aplicación.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-195">For fields of the **Int** type, this property passes the int value of the field between the server and the app.</span></span>

### <a name="realvalue-real"></a><span data-ttu-id="a4ba9-196">realValue (real)</span><span class="sxs-lookup"><span data-stu-id="a4ba9-196">realValue (real)</span></span>

<span data-ttu-id="a4ba9-197">Para campos do tipo **Real**, esta propiedade pasa o valor real do campo entre o servidor e a aplicación.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-197">For fields of the **Real** type, this property passes the real value of the field between the server and the app .</span></span>

### <a name="stringvalue-str"></a><span data-ttu-id="a4ba9-198">stringValue (str)</span><span class="sxs-lookup"><span data-stu-id="a4ba9-198">stringValue (str)</span></span>

<span data-ttu-id="a4ba9-199">Para campos do tipo **Cadea**, esta propiedade pasa o valor de cadea do campo entre o servidor e a aplicación.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-199">For fields of the **String** type, this property passes the string value of the field between the server and the app.</span></span> <span data-ttu-id="a4ba9-200">Tamén se usa para campos do tipo **Real** que teñen o formato de moeda.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-200">It's also used for fields of the **Real** type that are formatted as currency.</span></span> <span data-ttu-id="a4ba9-201">Para eses campos, a propiedade úsase para pasar o código de moeda á aplicación.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-201">For those fields, the property is used to pass the currency code to the app.</span></span>

### <a name="datevalue-date"></a><span data-ttu-id="a4ba9-202">dateValue (data)</span><span class="sxs-lookup"><span data-stu-id="a4ba9-202">dateValue (date)</span></span>

<span data-ttu-id="a4ba9-203">Para campos do tipo **Data**, esta propiedade pasa o valor de data do campo entre o servidor e a aplicación.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-203">For fields of the **Date** type, this property passes the date value of the field between the server and the app.</span></span>

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a><span data-ttu-id="a4ba9-204">Mostrar e gardar un campo personalizado na sección de entrada de folla de control horario</span><span class="sxs-lookup"><span data-stu-id="a4ba9-204">Show and save a custom field in the timesheet entry section</span></span>

<span data-ttu-id="a4ba9-205">A continuación móstrase unha captura de pantalla da aplicación móbil da creación dunha entrada de folla de control horario.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-205">Below is a screenshot from the mobile app of a timesheet entry creation.</span></span> <span data-ttu-id="a4ba9-206">Mostra os campos listos para usar e un campo personalizado na sección "Entrada de tempo" chamado "Cadea de proba" cun valor enum de "Segunda opción" xa definido.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-206">It shows the out-of-box fields and a custom field in the "Time entry" section called "Test string" with an enum value of "Second option" already set.</span></span>

![Probar campo personalizado de cadea na aplicación](media/timesheet-entry.jpg)



<span data-ttu-id="a4ba9-208">A continuación móstrase unha captura de pantalla da aplicación móbil do usuario que selecciona unha das opcións de enum dispoñibles para o campo personalizado "Cadea de proba".</span><span class="sxs-lookup"><span data-stu-id="a4ba9-208">Below is a screenshot from the mobile app of the user selecting one of the enum options available for the "Test string" custom field.</span></span>  <span data-ttu-id="a4ba9-209">As dúas opcións son "Primeira opción" e "Segunda opción" que se amosan como botóns de opción.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-209">The two options are "First option" and "Second option" shown as radio buttons.</span></span> <span data-ttu-id="a4ba9-210">A segunda opción está seleccionada actualmente.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-210">The second option is currently selected.</span></span>

![Botóns de opción para o campo personalizado da cadea de proba](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="a4ba9-212">Amplíe a táboa TSTimesheetLine para que teña un campo personalizado</span><span class="sxs-lookup"><span data-stu-id="a4ba9-212">Extend the TSTimesheetLine table so that it has a custom field</span></span>

<span data-ttu-id="a4ba9-213">En escenarios típicos, é probable que os datos dun campo personalizado na sección de entrada de folla de control horario se garden na táboa TSTimesheetLine.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-213">In typical scenarios, it's likely that the data for a custom field in the timesheet entry section will be saved to the TSTimesheetLine table.</span></span> <span data-ttu-id="a4ba9-214">Non obstante, pódense usar outras táboas se os datos se poden recuperar segundo un rexistro de TSTimesheetTrans que se proporciona ou se non teñen un contexto de rexistro específico (por exemplo, se o campo está configurado como de só lectura nos parámetros do proxecto).</span><span class="sxs-lookup"><span data-stu-id="a4ba9-214">However, other tables can be used if the data can be retrieved based on a TSTimesheetTrans record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="a4ba9-215">Teña en conta que os campos personalizados non teñen que ter ningún rexistro de base de datos de respaldo.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-215">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="a4ba9-216">Pódense xerar dinámicamente segundo a lóxica de X++.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-216">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="a4ba9-217">Este método pode ser útil en escenarios de só lectura (consulte a sección "Usar cadea de comando na clase TSTimesheetDetails, método buildCustomFieldListForHeader para encher os detalles da folla de control horario" para ver un exemplo de valores de campo personalizados xerados dinámicamente).</span><span class="sxs-lookup"><span data-stu-id="a4ba9-217">This approach can be useful in read-only scenarios (see the “Use chain of command on the TSTimesheetDetails class, buildCustomFieldListForHeader method to fill in timesheet details” section for an example of dynamically generated custom field values.)</span></span>

<span data-ttu-id="a4ba9-218">Debaixo móstrase unha captura de pantalla de Visual Studio da árbore de obxectos da aplicación.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-218">Below is a screenshot from Visual Studio of the Application Object Tree.</span></span> <span data-ttu-id="a4ba9-219">Mostra unha extensión da táboa TSTimesheetLine co campo TestLineString engadido como campo personalizado.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-219">It shows an extension of the TSTimesheetLine table with the TestLineString field added as a custom field.</span></span>

![Cadea de liña](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a><span data-ttu-id="a4ba9-221">Usar a cadea de comando no método buildCustomFieldList da clase TSTimesheetSettings para amosar un campo na sección de entrada de folla de control horario</span><span class="sxs-lookup"><span data-stu-id="a4ba9-221">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the timesheet entry section</span></span>

<span data-ttu-id="a4ba9-222">Este código controla a configuración de visualización do campo na aplicación.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-222">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="a4ba9-223">Por exemplo, controla o tipo de campo, a etiqueta, se o campo é obrigatorio e en que sección aparece o campo.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-223">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="a4ba9-224">O seguinte exemplo mostra un campo de cadea nas entradas de tempo.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-224">The following example shows a string field on time entries.</span></span> <span data-ttu-id="a4ba9-225">Este campo ten dúas opcións, **Primeira opción** e **Segunda opción**, que están dispoñibles a través dos botóns de opción.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-225">This field has two options, **First option** and **Second option**, that are available via option buttons (radio buttons).</span></span> <span data-ttu-id="a4ba9-226">O campo da aplicación está asociado ao campo **TestLineString** que se engade á táboa TSTimesheetLine.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-226">The field in the app is associated with the **TestLineString** field that is added to the TSTimesheetLine table.</span></span>

<span data-ttu-id="a4ba9-227">Teña en conta o uso do método **TSTimesheetCustomField::newFromMetatdata()** para simplificar a inicialización das propiedades do campo personalizado: **fieldBaseType**, **tableName**, **filedname**, **label**, **isEditable**, **isMandatory**, **stringLength** e **numberOfDecimals**.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-227">Note the use of the **TSTimesheetCustomField::newFromMetatdata()** method to simplify the initialization of the custom field properties: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength**, and **numberOfDecimals**.</span></span> <span data-ttu-id="a4ba9-228">Tamén pode configurar estes parámetros manualmente, como prefira.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-228">You can also set these parameters manually, as you prefer.</span></span>

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

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a><span data-ttu-id="a4ba9-229">Usar a cadea de comando no método buildCustomFieldListForEntry da clase TSTimesheetEntry para introducir valores nunha entrada de folla de control horario</span><span class="sxs-lookup"><span data-stu-id="a4ba9-229">Use chain of command on the buildCustomFieldListForEntry method of the TSTimesheetEntry class to enter values in a timesheet entry</span></span>

<span data-ttu-id="a4ba9-230">O método **buildCustomFieldListForEntry** úsase para introducir valores nas liñas de folla de control horario gardadas na aplicación móbil.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-230">The **buildCustomFieldListForEntry** method is used to enter values on the saved timesheet lines in the mobile app.</span></span> <span data-ttu-id="a4ba9-231">Toma un rexistro de TSTimesheetTrans como parámetro.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-231">It takes a TSTimesheetTrans record as a parameter.</span></span> <span data-ttu-id="a4ba9-232">Os campos dese rexistro pódense empregar para encher o valor do campo personalizado na aplicación.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-232">Fields from that record can be used to fill in the custom field value in the app.</span></span>

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

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a><span data-ttu-id="a4ba9-233">Usar a cadea de comando na clase TSTimesheetEntryService para gardar unha entrada de folla control horario da aplicación de novo na base de datos</span><span class="sxs-lookup"><span data-stu-id="a4ba9-233">Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database</span></span>

<span data-ttu-id="a4ba9-234">Para gardar un campo personalizado de novo na base de datos no uso normal, debe ampliar varios métodos:</span><span class="sxs-lookup"><span data-stu-id="a4ba9-234">To save a custom field back to the database in typical usage, you must extend multiple methods:</span></span>

- <span data-ttu-id="a4ba9-235">O método **timesheetLineNeedsUpdating** úsase para determinar se o usuario cambiou o rexistro de liña na aplicación e debe gardarse na base de datos.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-235">The **timesheetLineNeedsUpdating** method is used to determine whether the line record has been changed by the user in the app and must be saved to the database.</span></span> <span data-ttu-id="a4ba9-236">Se o rendemento non importa, este método pode simplificarse para que sempre sexa **true**.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-236">If performance isn't a concern, this method can be simplified so that it always returns **true**.</span></span>
- <span data-ttu-id="a4ba9-237">Os métodos **populateTimesheetLineFromEntryDuringCreate** e **populateTimesheetLineFromEntryDuringUpdate** pódense ampliar para que introduzan valores no rexistro da base de datos de TSTimesheetLine desde o contrato de datos de TSTimesheetEntry que se fornece.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-237">The **populateTimesheetLineFromEntryDuringCreate** and **populateTimesheetLineFromEntryDuringUpdate** methods can be extended so that they enter values in the TSTimesheetLine database record from the TSTimesheetEntry data contract record that is provided.</span></span> <span data-ttu-id="a4ba9-238">No exemplo seguinte, observe como a asignación entre o campo de base de datos e o campo de entrada faise manualmente a través do código de X++.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-238">In the example that follows, notice how the mapping between the database field and the entry field is manually done via X++ code.</span></span>
- <span data-ttu-id="a4ba9-239">O método **populateTimesheetWeekFromEntry** tamén se pode estender se o campo personalizado que está asignado ao obxecto de **TSTimesheetEntry** escribir de novo na táboa de base de datos TSTimesheetLineweek.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-239">The **populateTimesheetWeekFromEntry** method can also be extended if the custom field that is mapped to the **TSTimesheetEntry** object must write back to the TSTimesheetLineweek database table.</span></span>

> [!NOTE]
> <span data-ttu-id="a4ba9-240">O seguinte exemplo garda o valor **firstOption** ou **secondOption** que o usuario selecciona na base de datos como un valor de cadea en bruto.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-240">The following example saves the **firstOption** or **secondOption** value that the user selects to the database as a raw string value.</span></span> <span data-ttu-id="a4ba9-241">Se o campo da base de datos é un campo do tipo **Enum**, eses valores pódense asignar manualmente a un valor enum e despois gardalos nun campo enum da táboa da base de datos.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-241">If the database field is a field of the **Enum** type, those values can be manually mapped to an enum value and then saved to an enum field on the database table.</span></span>

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

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a><span data-ttu-id="a4ba9-242">Mostrar un campo personalizado na sección de cabeceira de folla de control horario</span><span class="sxs-lookup"><span data-stu-id="a4ba9-242">Show a custom field in the timesheet header section</span></span>

<span data-ttu-id="a4ba9-243">A continuación móstrase unha captura de pantalla da aplicación móbil dun usuario visualizando unha folla de control horario.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-243">Below is a screenshot from the mobile app of a user viewing a timesheet.</span></span> <span data-ttu-id="a4ba9-244">Na esquina superior dereita seleccionouse o botón "Máis información" para amosar a opción "Ver máis detalles".</span><span class="sxs-lookup"><span data-stu-id="a4ba9-244">The "More information" button has been selected in the upper-right corner to show the "View more details" option.</span></span>  

![Comando de visualizar máis detalles](media/show-more.png)

<span data-ttu-id="a4ba9-246">A continuación móstrase unha captura de pantalla da aplicación móbil que mostra a sección "Máis" dunha folla de control horario.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-246">Below is a screenshot from the mobile app showing the “More” section of a timesheet.</span></span> <span data-ttu-id="a4ba9-247">Engadiuse un campo personalizado chamado "Taxa de utilización desta folla de control horario (campo personalizado computado)" á sección de cabeceira da folla de control horario.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-247">A custom field called “Utilization rate of this timesheet (computed custom field)” has been added to the timesheet header section.</span></span> <span data-ttu-id="a4ba9-248">No campo personalizado establécese un valor de só lectura de "0,667".</span><span class="sxs-lookup"><span data-stu-id="a4ba9-248">A read-only value of "0.667" is set on the custom field.</span></span>

![Sección Máis](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="a4ba9-250">Amplíe a táboa TSTimesheetTable para que teña un campo personalizado</span><span class="sxs-lookup"><span data-stu-id="a4ba9-250">Extend the TSTimesheetTable table so that it has a custom field</span></span>

<span data-ttu-id="a4ba9-251">En escenarios típicos, é probable que os datos dun campo personalizado na sección de cabeceira se tomen da táboa TSTimesheetHeader.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-251">In typical scenarios, it's likely that the data for a custom field in the header section will be pulled from the TSTimesheetHeader table.</span></span> <span data-ttu-id="a4ba9-252">Non obstante, pódense usar outras táboas se os datos se poden recuperar segundo un rexistro de TSTimesheetTable que se proporciona ou se non teñen un contexto de rexistro específico (por exemplo, se o campo está configurado como de só lectura nos parámetros do proxecto).</span><span class="sxs-lookup"><span data-stu-id="a4ba9-252">However, other tables can be used if the data can be retrieved based on a TSTimesheetTable record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="a4ba9-253">Teña en conta que os campos personalizados non teñen que ter ningún rexistro de base de datos de respaldo.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-253">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="a4ba9-254">Pódense xerar dinámicamente segundo a lóxica de X++.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-254">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="a4ba9-255">O exemplo que segue mostra este método.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-255">The example that follows shows this approach.</span></span>

<span data-ttu-id="a4ba9-256">Os campos da sección de cabeceira sempre son de só lectura na aplicación.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-256">Fields in the header section are always read-only in the app.</span></span>

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a><span data-ttu-id="a4ba9-257">Usar a cadea de comando no método buildCustomFieldList da clase TSTimesheetSettings para amosar un campo na sección de cabeceira</span><span class="sxs-lookup"><span data-stu-id="a4ba9-257">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the header section</span></span>

<span data-ttu-id="a4ba9-258">Este código controla a configuración de visualización do campo na aplicación.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-258">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="a4ba9-259">Por exemplo, controla o tipo de campo, a etiqueta, se o campo é obrigatorio e en que sección aparece o campo.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-259">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="a4ba9-260">O seguinte exemplo mostra un valor calculado na sección de cabeceira da aplicación.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-260">The following example shows a computed value in the header section in the app.</span></span>

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

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a><span data-ttu-id="a4ba9-261">Usar a cadea de comando no método buildCustomFieldListForHeader da clase TSTimesheetDetails para encher os detalles da folla de control horario</span><span class="sxs-lookup"><span data-stu-id="a4ba9-261">Use chain of command on the buildCustomFieldListForHeader method of the TSTimesheetDetails class to fill in timesheet details</span></span>

<span data-ttu-id="a4ba9-262">O método **buildCustomFieldListForHeader** úsase para encher os detalles da cabeceira da folla de control horario na aplicación móbil.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-262">The **buildCustomFieldListForHeader** method is used to fill in the timesheet header details in the mobile app.</span></span> <span data-ttu-id="a4ba9-263">Toma un rexistro de TSTimesheetTable como parámetro.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-263">It takes a TSTimesheetTable record as a parameter.</span></span> <span data-ttu-id="a4ba9-264">Os campos dese rexistro pódense empregar para encher o valor do campo personalizado na aplicación.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-264">Fields from that record can be used to fill in the custom field value in the app.</span></span> <span data-ttu-id="a4ba9-265">O seguinte exemplo non le ningún valor da base de datos.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-265">The following example doesn't read any values from the database.</span></span> <span data-ttu-id="a4ba9-266">En vez diso, usa a lóxica de X++ para xerar un valor calculado que despois se mostra na aplicación.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-266">Instead, it uses X++ logic to generate a computed value that is then shown in the app.</span></span>


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

## <a name="other-configurabilityextensibility-opportunities"></a><span data-ttu-id="a4ba9-267">Outras oportunidades de configurabilidade/extensibilidade</span><span class="sxs-lookup"><span data-stu-id="a4ba9-267">Other configurability/extensibility opportunities</span></span>

### <a name="adding-additional-validation-for-the-app"></a><span data-ttu-id="a4ba9-268">Engadir validación adicional para a aplicación</span><span class="sxs-lookup"><span data-stu-id="a4ba9-268">Adding additional validation for the app</span></span>

<span data-ttu-id="a4ba9-269">A lóxica existente para a funcionalidade da folla de control horario a nivel de base de datos aínda funcionará como se esperaba.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-269">Existing logic for timesheet functionality at the database level will still work as expected.</span></span> <span data-ttu-id="a4ba9-270">Para interromper a realización das operacións de gardar ou enviar e amosar unha mensaxe de erro específica, pode engadir **erro de lanzamento ("mensaxe ao usuario")** ao código mediante unha cadea de extensión de comando.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-270">To interrupt the completion of save or submit operations and show a specific error message, you can add **throw error("message to user")** to the code via a chain of command extension.</span></span> <span data-ttu-id="a4ba9-271">Aquí ten tres exemplos de métodos extensibles útiles:</span><span class="sxs-lookup"><span data-stu-id="a4ba9-271">Here are three examples of useful extensible methods:</span></span>

- <span data-ttu-id="a4ba9-272">Se **validateWrite** na táboa TSTimesheetLine mostra **false** durante unha operación de gardado para unha liña de folla de control horario, móstrase unha mensaxe de erro na aplicación móbil.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-272">If **validateWrite** on the TSTimesheetLine table returns **false** during a save operation for a timesheet line, an error message is shown in the mobile app.</span></span>
- <span data-ttu-id="a4ba9-273">Se **validateSubmit** na táboa TSTimesheetTable mostra **false** durante o envío da folla de control horario na aplicación, móstrase unha mensaxe de erro ao usuario.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-273">If **validateSubmit** on the TSTimesheetTable table returns **false** during timesheet submission in the app, an error message is shown to the user.</span></span>
- <span data-ttu-id="a4ba9-274">A lóxica que enche campos (por exemplo, **Propiedade de liña**) durante o método **inserir** na táboa TSTimesheetLine aínda se executará.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-274">Logic that fills in fields (for example, **Line Property**) during the **insert** method on the TSTimesheetLine table will still run.</span></span>

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a><span data-ttu-id="a4ba9-275">Ocultar e marcar campos listos para usar como de só lectura mediante configuración</span><span class="sxs-lookup"><span data-stu-id="a4ba9-275">Hiding and marking out-of-box fields as read-only via configuration</span></span>

<span data-ttu-id="a4ba9-276">Desde os parámetros do proxecto, pode facer que os campos listos para usar sexan só de lectura ou estean ocultos na aplicación móbil.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-276">From the project parameters, you can make out-of-box fields read-only or hidden in the mobile app.</span></span> <span data-ttu-id="a4ba9-277">Estableza as opcións na sección **Follas de de control horario móbiles** no separador **Folla de control horario** da páxina **Parámetros de xestión de proxectos e contabilidad**.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-277">Set the options in the **Mobile timesheets** section on the **Timesheet** tab of the **Project management and accounting parameters** page.</span></span>

![Parámetros do proxecto](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a><span data-ttu-id="a4ba9-279">Cambiar as actividades dispoñibles para a selección mediante extensións</span><span class="sxs-lookup"><span data-stu-id="a4ba9-279">Changing the activities that are available for selection via extensions</span></span>

<span data-ttu-id="a4ba9-280">As actividades dispoñibles para a selección dun proxecto énchense a través dos métodos **getActivitiesForProject()** e **getActivityQuery()** na clase **TsTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-280">The activities that are available for selection for a project are filled in via the **getActivitiesForProject()** and **getActivityQuery()** methods in the **TsTimesheetProjectService** class.</span></span> <span data-ttu-id="a4ba9-281">Pode usar a cadea de mando para cambiar este comportamento para que coincida co seu escenario emprearial para as actividades dispoñibles para a selección dun proxecto específico.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-281">You can use chain of command to change this behavior to match your business scenario for the activities that are available for selection for a specific project.</span></span>

### <a name="entering-a-default-project-category-on-timesheet-entries"></a><span data-ttu-id="a4ba9-282">Introdución dunha categoría de proxecto predefinida nas entradas da folla de control horario</span><span class="sxs-lookup"><span data-stu-id="a4ba9-282">Entering a default project category on timesheet entries</span></span>

<span data-ttu-id="a4ba9-283">A entrada dunha categoría de proxecto predefinida nas entradas de folla de control horario prodúcese en tres niveis.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-283">Entry of a default project category on timesheet entries occurs at three levels.</span></span> <span data-ttu-id="a4ba9-284">Podes usar a cadea de mando para estender o comportamento en calquera ou en todos estes niveis para conseguir o comportamento desexado.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-284">You can use chain of command to extend the behavior at any or all of these levels to achieve the desired behavior.</span></span> <span data-ttu-id="a4ba9-285">Emprégase a seguinte xerarquía:</span><span class="sxs-lookup"><span data-stu-id="a4ba9-285">The following hierarchy is used:</span></span>

1. <span data-ttu-id="a4ba9-286">A aplicación tenta poñer a categoría predefinida do recurso do proxecto.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-286">The app tries to put the default category from the project resource.</span></span> <span data-ttu-id="a4ba9-287">Esta categoría predefinida establécese nos métodos **getCurrentUserResource** e **getDelegatedResourcesForCurrentUser** na clase **TSTimesheetSettingsService**.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-287">This default category is set in the **getCurrentUserResource** and **getDelegatedResourcesForCurrentUser** methods in the **TSTimesheetSettingsService** class.</span></span>
2. <span data-ttu-id="a4ba9-288">Se a categoría predefinida non se proporciona no nivel de recursos do proxecto, a aplicación tenta tomala da actividade do proxecto.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-288">If the default category isn't provided at the project resource level, the app tries to pull it from the project activity.</span></span> <span data-ttu-id="a4ba9-289">Esta categoría predefinida establécese no método **getActivitiesForProject** na clase **TSTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-289">This default category is set in the **getActivitiesForProject** method in the **TSTimesheetProjectService** class.</span></span>
3. <span data-ttu-id="a4ba9-290">Se a categoría predefinida non se proporciona no nivel de actividade do proxecto, a categoría predefinida tómase dos parámetros do proxecto.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-290">If the default category isn't provided at the project activity level, the default category it taken from the project parameters.</span></span> <span data-ttu-id="a4ba9-291">Esta categoría predefinida establécese no método **getProjectDetailsbyRule** na clase **TSTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-291">This default category is set in the **getProjectDetailsbyRule** method in the **TSTimesheetProjectService** class.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]