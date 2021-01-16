---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 91FFBEE9-A488-49ED-8C6C-2DE891CE0749
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountSchema.md
ms.openlocfilehash: 8887cdf7da3b69d826bedd4f6de97a8cf39d4a6e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98353801"
---
# <span data-ttu-id="859d8-101">New-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="859d8-101">New-AzIntegrationAccountSchema</span></span>

## <span data-ttu-id="859d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="859d8-102">SYNOPSIS</span></span>
<span data-ttu-id="859d8-103">Létrehoz egy integrációs fióksémát.</span><span class="sxs-lookup"><span data-stu-id="859d8-103">Creates an integration account schema.</span></span>

## <span data-ttu-id="859d8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="859d8-104">SYNTAX</span></span>

```
New-AzIntegrationAccountSchema -ResourceGroupName <String> -Name <String> -SchemaName <String>
 [-SchemaFilePath <String>] [-SchemaDefinition <String>] [-SchemaType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="859d8-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="859d8-105">DESCRIPTION</span></span>
<span data-ttu-id="859d8-106">A **New-AzIntegrationAccountSchema** parancsmag létrehoz egy integrációs fióksémát.</span><span class="sxs-lookup"><span data-stu-id="859d8-106">The **New-AzIntegrationAccountSchema** cmdlet creates an integration account schema.</span></span>
<span data-ttu-id="859d8-107">Ez a parancsmag egy objektumot ad vissza, amely az integrációs fióksémát képviseli.</span><span class="sxs-lookup"><span data-stu-id="859d8-107">This cmdlet returns an object that represents the integration account schema.</span></span>
<span data-ttu-id="859d8-108">Adja meg az integrációs fiók nevét, az erőforráscsoport nevét, a séma nevét és a sémadefiníciót.</span><span class="sxs-lookup"><span data-stu-id="859d8-108">Specify the integration account name, resource group name, schema name, and schema definition.</span></span>
<span data-ttu-id="859d8-109">A parancssorban megadott paraméterfájlértékek elsőbbséget élveznek a sablon paraméterobjektumában megadott paraméterértékekkel.</span><span class="sxs-lookup"><span data-stu-id="859d8-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="859d8-110">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="859d8-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="859d8-111">Ha dinamikus paramétert használ, írja be a parancsba.</span><span class="sxs-lookup"><span data-stu-id="859d8-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="859d8-112">A dinamikus paraméterek nevének felfedezéséhez írjon be egy kötőjelet (-) a parancsmag neve után, majd a Tab billentyű többszöri lenyomása után lépkedhet a rendelkezésre álló paraméterek között.</span><span class="sxs-lookup"><span data-stu-id="859d8-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="859d8-113">Ha kihagy egy kötelező sablonparamétert, a parancsmag rákérdez az értékre.</span><span class="sxs-lookup"><span data-stu-id="859d8-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="859d8-114">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="859d8-114">EXAMPLES</span></span>

### <span data-ttu-id="859d8-115">1. példa: Az integrációs fiókséma létrehozása</span><span class="sxs-lookup"><span data-stu-id="859d8-115">Example 1: Create the integration account schema</span></span>
```
PS C:\>New-AzIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema1" -SchemaFilePath "c:\temp\schema1"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/schemas/IntegrationAccountSchema1
Name        : IntegrationAccountSchema1
Type        : Microsoft.Logic/integrationAccounts/schemas
CreatedTime : 3/26/2016 7:21:10 PM
ChangedTime : 3/26/2016 7:21:10 PM
SchemaType  : Xml
ContentLink : https://<baseurl>/integrationaccounts68a13b6b49f14995ba7c5f3aedcbd7ad/3839E_XML_INTEGRATIONACCOUNTSCHEMA2-5A6650B914454A2CAB16
              B4A8D3F9840D?sv=2014-02-14&sr=b&sig=<value>
ContentSize : 7901
```

<span data-ttu-id="859d8-116">Ez a parancs létrehozza az IntegrationAccountSchema1 nevű integrációs fióksémát a megadott erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="859d8-116">This command creates the integration account schema named IntegrationAccountSchema1 in the specified resource group.</span></span>

## <span data-ttu-id="859d8-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="859d8-117">PARAMETERS</span></span>

### <span data-ttu-id="859d8-118">-ContentType</span><span class="sxs-lookup"><span data-stu-id="859d8-118">-ContentType</span></span>
<span data-ttu-id="859d8-119">Az integrációs fióksémának megfelelő tartalomtípust ad meg.</span><span class="sxs-lookup"><span data-stu-id="859d8-119">Specifies a content type for the integration account schema.</span></span>
<span data-ttu-id="859d8-120">Ez a parancsmag megfeleltetési tartalomtípusként támogatja az alkalmazás/xml formátumot.</span><span class="sxs-lookup"><span data-stu-id="859d8-120">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="859d8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="859d8-121">-DefaultProfile</span></span>
<span data-ttu-id="859d8-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="859d8-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="859d8-123">-Metadata</span><span class="sxs-lookup"><span data-stu-id="859d8-123">-Metadata</span></span>
<span data-ttu-id="859d8-124">A séma metaadat-objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="859d8-124">Specifies a metadata object for the schema.</span></span>

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

### <span data-ttu-id="859d8-125">-Name</span><span class="sxs-lookup"><span data-stu-id="859d8-125">-Name</span></span>
<span data-ttu-id="859d8-126">Egy integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="859d8-126">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="859d8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="859d8-127">-ResourceGroupName</span></span>
<span data-ttu-id="859d8-128">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="859d8-128">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="859d8-129">-SchemaDefinition</span><span class="sxs-lookup"><span data-stu-id="859d8-129">-SchemaDefinition</span></span>
<span data-ttu-id="859d8-130">Egy definícióobjektumot ad meg az integrációs fióksémához.</span><span class="sxs-lookup"><span data-stu-id="859d8-130">Specifies a definition object for integration account schema.</span></span>
<span data-ttu-id="859d8-131">Adja meg ezt a paramétert vagy *a SchemaFilePath paramétert.*</span><span class="sxs-lookup"><span data-stu-id="859d8-131">Specify either this parameter or the *SchemaFilePath* parameter.</span></span>

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

### <span data-ttu-id="859d8-132">-SchemaFilePath</span><span class="sxs-lookup"><span data-stu-id="859d8-132">-SchemaFilePath</span></span>
<span data-ttu-id="859d8-133">Az integrációs fiókséma definíciójának fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="859d8-133">Specifies the file path of a definition for the integration account schema.</span></span>
<span data-ttu-id="859d8-134">Adja meg ezt a paramétert vagy *a SchemaDefinition paramétert.*</span><span class="sxs-lookup"><span data-stu-id="859d8-134">Specify either this parameter or the *SchemaDefinition* parameter.</span></span>

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

### <span data-ttu-id="859d8-135">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="859d8-135">-SchemaName</span></span>
<span data-ttu-id="859d8-136">Megadja az integrációs fióksémának a nevét.</span><span class="sxs-lookup"><span data-stu-id="859d8-136">Specifies a name for the integration account schema.</span></span>

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

### <span data-ttu-id="859d8-137">-SchemaType</span><span class="sxs-lookup"><span data-stu-id="859d8-137">-SchemaType</span></span>
<span data-ttu-id="859d8-138">Az integrációs fiókséma típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="859d8-138">Specifies the type for the integration account schema.</span></span>
<span data-ttu-id="859d8-139">Ez a paraméter típusként támogatja az Xml formátumot.</span><span class="sxs-lookup"><span data-stu-id="859d8-139">This parameter supports Xml as the type.</span></span>

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

### <span data-ttu-id="859d8-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="859d8-140">-Confirm</span></span>
<span data-ttu-id="859d8-141">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="859d8-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="859d8-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="859d8-142">-WhatIf</span></span>
<span data-ttu-id="859d8-143">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="859d8-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="859d8-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="859d8-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="859d8-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="859d8-145">CommonParameters</span></span>
<span data-ttu-id="859d8-146">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="859d8-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="859d8-147">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="859d8-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="859d8-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="859d8-148">INPUTS</span></span>

### <span data-ttu-id="859d8-149">System.String</span><span class="sxs-lookup"><span data-stu-id="859d8-149">System.String</span></span>

## <span data-ttu-id="859d8-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="859d8-150">OUTPUTS</span></span>

### <span data-ttu-id="859d8-151">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="859d8-151">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span></span>

## <span data-ttu-id="859d8-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="859d8-152">NOTES</span></span>

## <span data-ttu-id="859d8-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="859d8-153">RELATED LINKS</span></span>

[<span data-ttu-id="859d8-154">Get-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="859d8-154">Get-AzIntegrationAccountSchema</span></span>](./Get-AzIntegrationAccountSchema.md)

[<span data-ttu-id="859d8-155">Remove-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="859d8-155">Remove-AzIntegrationAccountSchema</span></span>](./Remove-AzIntegrationAccountSchema.md)

[<span data-ttu-id="859d8-156">Set-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="859d8-156">Set-AzIntegrationAccountSchema</span></span>](./Set-AzIntegrationAccountSchema.md)


