---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 91FFBEE9-A488-49ED-8C6C-2DE891CE0749
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/new-azurermintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountSchema.md
ms.openlocfilehash: 19f6884e9359612eab1d22018a7ebc1295f81210
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504392"
---
# <span data-ttu-id="273e4-101">New-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="273e4-101">New-AzureRmIntegrationAccountSchema</span></span>

## <span data-ttu-id="273e4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="273e4-102">SYNOPSIS</span></span>
<span data-ttu-id="273e4-103">Integrációs fiók sémáját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="273e4-103">Creates an integration account schema.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="273e4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="273e4-104">SYNTAX</span></span>

```
New-AzureRmIntegrationAccountSchema -ResourceGroupName <String> -Name <String> -SchemaName <String>
 [-SchemaFilePath <String>] [-SchemaDefinition <String>] [-SchemaType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="273e4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="273e4-105">DESCRIPTION</span></span>
<span data-ttu-id="273e4-106">A **New-AzureRmIntegrationAccountSchema** parancsmag létrehoz egy integrációs fiók sémát.</span><span class="sxs-lookup"><span data-stu-id="273e4-106">The **New-AzureRmIntegrationAccountSchema** cmdlet creates an integration account schema.</span></span>
<span data-ttu-id="273e4-107">Ez a parancsmag egy olyan objektumot ad eredményül, amely az integrációs fiók sémáját jelképezi.</span><span class="sxs-lookup"><span data-stu-id="273e4-107">This cmdlet returns an object that represents the integration account schema.</span></span>
<span data-ttu-id="273e4-108">Adja meg az integrációs fiók nevét, az erőforrás csoport nevét, a séma nevét és a séma definícióját.</span><span class="sxs-lookup"><span data-stu-id="273e4-108">Specify the integration account name, resource group name, schema name, and schema definition.</span></span>
<span data-ttu-id="273e4-109">A parancssorban megadott sablon paraméterben megadott értékek elsőbbséget élveznek a Template paraméteres objektumban lévő sablon paraméter értékeivel.</span><span class="sxs-lookup"><span data-stu-id="273e4-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="273e4-110">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="273e4-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="273e4-111">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="273e4-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="273e4-112">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="273e4-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="273e4-113">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="273e4-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="273e4-114">Példák</span><span class="sxs-lookup"><span data-stu-id="273e4-114">EXAMPLES</span></span>

### <span data-ttu-id="273e4-115">Példa 1: az integrációs fiók sémájának létrehozása</span><span class="sxs-lookup"><span data-stu-id="273e4-115">Example 1: Create the integration account schema</span></span>
```
PS C:\>New-AzureRmIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema1" -SchemaFilePath "c:\temp\schema1"
Id          : /subscriptions/<SusbcriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/schemas/IntegrationAccountSchema1
Name        : IntegrationAccountSchema1
Type        : Microsoft.Logic/integrationAccounts/schemas
CreatedTime : 3/26/2016 7:21:10 PM
ChangedTime : 3/26/2016 7:21:10 PM
SchemaType  : Xml
ContentLink : https://<baseurl>/integrationaccounts68a13b6b49f14995ba7c5f3aedcbd7ad/3839E_XML_INTEGRATIONACCOUNTSCHEMA2-5A6650B914454A2CAB16
              B4A8D3F9840D?sv=2014-02-14&sr=b&sig=<value>
ContentSize : 7901
```

<span data-ttu-id="273e4-116">A parancs létrehozza a IntegrationAccountSchema1 nevű integrációs fiók sémáját a megadott erőforráscsoport számára.</span><span class="sxs-lookup"><span data-stu-id="273e4-116">This command creates the integration account schema named IntegrationAccountSchema1 in the specified resource group.</span></span>

## <span data-ttu-id="273e4-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="273e4-117">PARAMETERS</span></span>

### <span data-ttu-id="273e4-118">-ContentType</span><span class="sxs-lookup"><span data-stu-id="273e4-118">-ContentType</span></span>
<span data-ttu-id="273e4-119">Az integrációs fiók sémájának tartalomtípusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="273e4-119">Specifies a content type for the integration account schema.</span></span>
<span data-ttu-id="273e4-120">Ez a parancsmag a térképes tartalomtípusként támogatja az Application/XML-t.</span><span class="sxs-lookup"><span data-stu-id="273e4-120">This cmdlet supports application/xml as a map content type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="273e4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="273e4-121">-DefaultProfile</span></span>
<span data-ttu-id="273e4-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="273e4-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="273e4-123">-Metadata</span><span class="sxs-lookup"><span data-stu-id="273e4-123">-Metadata</span></span>
<span data-ttu-id="273e4-124">A séma metaadat-objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="273e4-124">Specifies a metadata object for the schema.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="273e4-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="273e4-125">-Name</span></span>
<span data-ttu-id="273e4-126">Az integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="273e4-126">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="273e4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="273e4-127">-ResourceGroupName</span></span>
<span data-ttu-id="273e4-128">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="273e4-128">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="273e4-129">-SchemaDefinition</span><span class="sxs-lookup"><span data-stu-id="273e4-129">-SchemaDefinition</span></span>
<span data-ttu-id="273e4-130">Az integrációs fiók sémájának meghatározási objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="273e4-130">Specifies a definition object for integration account schema.</span></span>
<span data-ttu-id="273e4-131">Adja meg ezt a paramétert vagy a *SchemaFilePath* paramétert.</span><span class="sxs-lookup"><span data-stu-id="273e4-131">Specify either this parameter or the *SchemaFilePath* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="273e4-132">-SchemaFilePath</span><span class="sxs-lookup"><span data-stu-id="273e4-132">-SchemaFilePath</span></span>
<span data-ttu-id="273e4-133">Az integrációs fiók sémájának definíciójának elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="273e4-133">Specifies the file path of a definition for the integration account schema.</span></span>
<span data-ttu-id="273e4-134">Adja meg ezt a paramétert vagy a *SchemaDefinition* paramétert.</span><span class="sxs-lookup"><span data-stu-id="273e4-134">Specify either this parameter or the *SchemaDefinition* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="273e4-135">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="273e4-135">-SchemaName</span></span>
<span data-ttu-id="273e4-136">Az integrációs fiók sémájának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="273e4-136">Specifies a name for the integration account schema.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="273e4-137">-SchemaType</span><span class="sxs-lookup"><span data-stu-id="273e4-137">-SchemaType</span></span>
<span data-ttu-id="273e4-138">Az integrációs fiók sémájának típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="273e4-138">Specifies the type for the integration account schema.</span></span>
<span data-ttu-id="273e4-139">Ez a paraméter az XML típust támogatja.</span><span class="sxs-lookup"><span data-stu-id="273e4-139">This parameter supports Xml as the type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Xml

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="273e4-140">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="273e4-140">-Confirm</span></span>
<span data-ttu-id="273e4-141">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="273e4-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="273e4-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="273e4-142">-WhatIf</span></span>
<span data-ttu-id="273e4-143">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="273e4-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="273e4-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="273e4-144">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="273e4-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="273e4-145">CommonParameters</span></span>
<span data-ttu-id="273e4-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="273e4-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="273e4-147">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="273e4-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="273e4-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="273e4-148">INPUTS</span></span>

### <span data-ttu-id="273e4-149">System. String</span><span class="sxs-lookup"><span data-stu-id="273e4-149">System.String</span></span>

## <span data-ttu-id="273e4-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="273e4-150">OUTPUTS</span></span>

### <span data-ttu-id="273e4-151">Microsoft. Azure. Management. Logic. models. IntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="273e4-151">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span></span>

## <span data-ttu-id="273e4-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="273e4-152">NOTES</span></span>

## <span data-ttu-id="273e4-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="273e4-153">RELATED LINKS</span></span>

[<span data-ttu-id="273e4-154">Get-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="273e4-154">Get-AzureRmIntegrationAccountSchema</span></span>](./Get-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="273e4-155">Remove-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="273e4-155">Remove-AzureRmIntegrationAccountSchema</span></span>](./Remove-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="273e4-156">Set-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="273e4-156">Set-AzureRmIntegrationAccountSchema</span></span>](./Set-AzureRmIntegrationAccountSchema.md)

