---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 3D4E44E3-0B55-4699-944F-412EE80CEEEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountSchema.md
ms.openlocfilehash: c43bfb5fd43df92d6b8d1674b4a856829b3258d8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100154787"
---
# <span data-ttu-id="90c14-101">Set-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="90c14-101">Set-AzIntegrationAccountSchema</span></span>

## <span data-ttu-id="90c14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90c14-102">SYNOPSIS</span></span>
<span data-ttu-id="90c14-103">Módosít egy integrációs fióksémát.</span><span class="sxs-lookup"><span data-stu-id="90c14-103">Modifies an integration account schema.</span></span>

## <span data-ttu-id="90c14-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="90c14-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountSchema -ResourceGroupName <String> -Name <String> -SchemaName <String>
 [-SchemaFilePath <String>] [-SchemaDefinition <String>] [-SchemaType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="90c14-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="90c14-105">DESCRIPTION</span></span>
<span data-ttu-id="90c14-106">A **Set-AzIntegrationAccountSchema** parancsmag módosítja az integrációs fióksémát.</span><span class="sxs-lookup"><span data-stu-id="90c14-106">The **Set-AzIntegrationAccountSchema** cmdlet modifies an integration account schema.</span></span>
<span data-ttu-id="90c14-107">Ez a parancsmag egy objektumot ad vissza, amely az integrációs fióksémát képviseli.</span><span class="sxs-lookup"><span data-stu-id="90c14-107">This cmdlet returns an object that represents the integration account schema.</span></span>
<span data-ttu-id="90c14-108">Adja meg az integrációs fiók nevét, az erőforráscsoport nevét és a séma nevét.</span><span class="sxs-lookup"><span data-stu-id="90c14-108">Specify the integration account name, resource group name, and schema name.</span></span>
<span data-ttu-id="90c14-109">A parancssorban megadott paraméterfájlértékek elsőbbséget élveznek a sablon paraméterértékeivel a sablon paraméterobjektumában.</span><span class="sxs-lookup"><span data-stu-id="90c14-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="90c14-110">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="90c14-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="90c14-111">Ha dinamikus paramétert használ, írja be a parancsba.</span><span class="sxs-lookup"><span data-stu-id="90c14-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="90c14-112">A dinamikus paraméterek nevének felfedezéséhez írjon be egy kötőjelet (-) a parancsmag neve után, majd a Tab billentyű többszöri lenyomása után lépkedhet a rendelkezésre álló paraméterek között.</span><span class="sxs-lookup"><span data-stu-id="90c14-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="90c14-113">Ha kihagy egy kötelező sablonparamétert, a parancsmag rákérdez az értékre.</span><span class="sxs-lookup"><span data-stu-id="90c14-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="90c14-114">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="90c14-114">EXAMPLES</span></span>

### <span data-ttu-id="90c14-115">1. példa: Integrációs fióksémának módosítása</span><span class="sxs-lookup"><span data-stu-id="90c14-115">Example 1: Modify an integration account schema</span></span>
```
PS C:\>Set-AzIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema43" -SchemaFilePath "c:\temp\schema1"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/schemas/IntegrationAccountSchema43
Name        : IntegrationAccountSchema43
Type        : Microsoft.Logic/integrationAccounts/schemas
CreatedTime : 3/26/2016 7:21:10 PM
ChangedTime : 3/26/2016 7:21:10 PM
SchemaType  : Xml
ContentLink : https://<baseurl>/integrationaccounts68a13b6b49f14995ba7c5f3aedcbd7ad/3839E_XML_INTEGRATIONACCOUNTSCHEMA2-5A6650B914454A2CAB16
              B4A8D3F9840D?sv=2014-02-14&sr=b&sig=<value>
ContentSize : 7901
```

<span data-ttu-id="90c14-116">Ez a parancs módosítja az IntegrationAccountSchema43 nevű integrációs fióksémát.</span><span class="sxs-lookup"><span data-stu-id="90c14-116">This command modifies the integration account schema named IntegrationAccountSchema43.</span></span>

## <span data-ttu-id="90c14-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="90c14-117">PARAMETERS</span></span>

### <span data-ttu-id="90c14-118">-ContentType</span><span class="sxs-lookup"><span data-stu-id="90c14-118">-ContentType</span></span>
<span data-ttu-id="90c14-119">Az integrációs fióksémának megfelelő tartalomtípust ad meg.</span><span class="sxs-lookup"><span data-stu-id="90c14-119">Specifies a content type for the integration account schema.</span></span>
<span data-ttu-id="90c14-120">Ez a parancsmag megfeleltetési tartalomtípusként támogatja az alkalmazás/xml formátumot.</span><span class="sxs-lookup"><span data-stu-id="90c14-120">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="90c14-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90c14-121">-DefaultProfile</span></span>
<span data-ttu-id="90c14-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="90c14-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="90c14-123">-Force</span><span class="sxs-lookup"><span data-stu-id="90c14-123">-Force</span></span>
<span data-ttu-id="90c14-124">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="90c14-124">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90c14-125">-Metadata</span><span class="sxs-lookup"><span data-stu-id="90c14-125">-Metadata</span></span>
<span data-ttu-id="90c14-126">A séma metaadat-objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="90c14-126">Specifies a metadata object for the schema.</span></span>

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

### <span data-ttu-id="90c14-127">-Name</span><span class="sxs-lookup"><span data-stu-id="90c14-127">-Name</span></span>
<span data-ttu-id="90c14-128">Az integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="90c14-128">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="90c14-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90c14-129">-ResourceGroupName</span></span>
<span data-ttu-id="90c14-130">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="90c14-130">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="90c14-131">-SchemaDefinition</span><span class="sxs-lookup"><span data-stu-id="90c14-131">-SchemaDefinition</span></span>
<span data-ttu-id="90c14-132">Egy definícióobjektumot ad meg az integrációs fióksémához.</span><span class="sxs-lookup"><span data-stu-id="90c14-132">Specifies a definition object for integration account schema.</span></span>

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

### <span data-ttu-id="90c14-133">-SchemaFilePath</span><span class="sxs-lookup"><span data-stu-id="90c14-133">-SchemaFilePath</span></span>
<span data-ttu-id="90c14-134">Az integrációs fiókséma definíciójának fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="90c14-134">Specifies the file path of a definition for the integration account schema.</span></span>

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

### <span data-ttu-id="90c14-135">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="90c14-135">-SchemaName</span></span>
<span data-ttu-id="90c14-136">Az integrációs fiókséma nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="90c14-136">Specifies the name of the integration account schema.</span></span>

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

### <span data-ttu-id="90c14-137">-SchemaType</span><span class="sxs-lookup"><span data-stu-id="90c14-137">-SchemaType</span></span>
<span data-ttu-id="90c14-138">Az integrációs fiókséma típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="90c14-138">Specifies the type for the integration account schema.</span></span>
<span data-ttu-id="90c14-139">Ez a paraméter típusként támogatja az Xml formátumot.</span><span class="sxs-lookup"><span data-stu-id="90c14-139">This parameter supports Xml as the type.</span></span>

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

### <span data-ttu-id="90c14-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="90c14-140">-Confirm</span></span>
<span data-ttu-id="90c14-141">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="90c14-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90c14-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90c14-142">-WhatIf</span></span>
<span data-ttu-id="90c14-143">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="90c14-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90c14-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="90c14-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90c14-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90c14-145">CommonParameters</span></span>
<span data-ttu-id="90c14-146">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90c14-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90c14-147">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90c14-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90c14-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="90c14-148">INPUTS</span></span>

### <span data-ttu-id="90c14-149">System.String</span><span class="sxs-lookup"><span data-stu-id="90c14-149">System.String</span></span>

## <span data-ttu-id="90c14-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="90c14-150">OUTPUTS</span></span>

### <span data-ttu-id="90c14-151">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="90c14-151">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span></span>

## <span data-ttu-id="90c14-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="90c14-152">NOTES</span></span>

## <span data-ttu-id="90c14-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="90c14-153">RELATED LINKS</span></span>

[<span data-ttu-id="90c14-154">Get-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="90c14-154">Get-AzIntegrationAccountSchema</span></span>](./Get-AzIntegrationAccountSchema.md)

[<span data-ttu-id="90c14-155">New-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="90c14-155">New-AzIntegrationAccountSchema</span></span>](./New-AzIntegrationAccountSchema.md)

[<span data-ttu-id="90c14-156">Remove-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="90c14-156">Remove-AzIntegrationAccountSchema</span></span>](./Remove-AzIntegrationAccountSchema.md)


