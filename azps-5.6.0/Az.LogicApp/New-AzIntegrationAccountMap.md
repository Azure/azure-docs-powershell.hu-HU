---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: DF71430C-F33F-409B-A550-CC7285252E91
online version: https://docs.microsoft.com/powershell/module/az.logicapp/new-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountMap.md
ms.openlocfilehash: 7ce86f893cbead5b2c5ac7a57af44eeb7f92f9ae
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921961"
---
# <span data-ttu-id="64041-101">New-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="64041-101">New-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="64041-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64041-102">SYNOPSIS</span></span>
<span data-ttu-id="64041-103">Létrehoz egy integrációs fióktérképet.</span><span class="sxs-lookup"><span data-stu-id="64041-103">Creates an integration account map.</span></span>

## <span data-ttu-id="64041-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="64041-104">SYNTAX</span></span>

```
New-AzIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String>
 [-MapFilePath <String>] [-MapDefinition <String>] [-MapType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64041-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="64041-105">DESCRIPTION</span></span>
<span data-ttu-id="64041-106">A **New-AzIntegrationAccountMap** parancsmag létrehoz egy integrációs fióktérképet.</span><span class="sxs-lookup"><span data-stu-id="64041-106">The **New-AzIntegrationAccountMap** cmdlet creates an integration account map.</span></span>
<span data-ttu-id="64041-107">Ez a parancsmag egy objektumot ad vissza, amely az integrációs fiók térképét képviseli.</span><span class="sxs-lookup"><span data-stu-id="64041-107">This cmdlet returns an object that represents the integration account map.</span></span>
<span data-ttu-id="64041-108">Megadhatja az integrációs fiók nevét, az erőforráscsoport nevét, a leképezés nevét és a leképezés definícióját.</span><span class="sxs-lookup"><span data-stu-id="64041-108">Specifying the integration account name, resource group name, map name, and map definition.</span></span>
<span data-ttu-id="64041-109">A parancssorban megadott paraméterfájlértékek elsőbbséget élveznek a sablon paraméterértékeivel a sablon paraméterobjektumában.</span><span class="sxs-lookup"><span data-stu-id="64041-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="64041-110">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="64041-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="64041-111">Ha dinamikus paramétert használ, írja be a parancsba.</span><span class="sxs-lookup"><span data-stu-id="64041-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="64041-112">A dinamikus paraméterek nevének felfedezéséhez írjon be egy kötőjelet (-) a parancsmag neve után, majd a Tab billentyű többszöri lenyomása után lépkedhet a rendelkezésre álló paraméterek között.</span><span class="sxs-lookup"><span data-stu-id="64041-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="64041-113">Ha kihagy egy kötelező sablonparamétert, a parancsmag rákérdez az értékre.</span><span class="sxs-lookup"><span data-stu-id="64041-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="64041-114">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="64041-114">EXAMPLES</span></span>

### <span data-ttu-id="64041-115">1. példa: Integrációs fióktérkép létrehozása</span><span class="sxs-lookup"><span data-stu-id="64041-115">Example 1: Create an integration account map</span></span>
```powershell
PS C:\>New-AzIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47" -MapDefinition $MapContent
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/maps/IntegrationAccountMap47
Name        : IntegrationAccountMap47
Type        : Microsoft.Logic/integrationAccounts/maps
CreatedTime : 3/26/2016 7:12:22 PM
ChangedTime : 3/26/2016 7:12:22 PM
MapType     : Xslt
ContentLink : https://<baseurl>/integrationaccounts68a13b6b49f14995ba7c5f3aedcbd7ad/99D1E_XSLT_INTEGRATIONACCOUNTMAP47-9C97D973088B4256A1893B
              BCB1F85246?sv=2014-02-14&sr=b&sig=<value>
ContentSize : 3056
Metadata    :
```

<span data-ttu-id="64041-116">Ez a parancs létrehozza az integrációs fiók leképezését a megadott erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="64041-116">This command creates the integration account map in the specified resource group.</span></span>
<span data-ttu-id="64041-117">A parancs egy korábbi parancs által a $MapContent egy leképezésdefiníciót ad meg.</span><span class="sxs-lookup"><span data-stu-id="64041-117">The command specifies a map definition stored in the $MapContent variable by a previous command.</span></span>

### <span data-ttu-id="64041-118">2. példa</span><span class="sxs-lookup"><span data-stu-id="64041-118">Example 2</span></span>

<span data-ttu-id="64041-119">Létrehoz egy integrációs fióktérképet.</span><span class="sxs-lookup"><span data-stu-id="64041-119">Creates an integration account map.</span></span> <span data-ttu-id="64041-120">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="64041-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzIntegrationAccountMap -MapFilePath <String> -MapName 'IntegrationAccountMap47' -MapType Xslt -Name 'IntegrationAccount31' -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="64041-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="64041-121">PARAMETERS</span></span>

### <span data-ttu-id="64041-122">-ContentType</span><span class="sxs-lookup"><span data-stu-id="64041-122">-ContentType</span></span>
<span data-ttu-id="64041-123">Megadja az integrációs fiók térképének tartalomtípusát.</span><span class="sxs-lookup"><span data-stu-id="64041-123">Specifies a content type for the integration account map.</span></span>
<span data-ttu-id="64041-124">Ez a parancsmag megfeleltetési tartalomtípusként támogatja az alkalmazás/xml formátumot.</span><span class="sxs-lookup"><span data-stu-id="64041-124">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="64041-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64041-125">-DefaultProfile</span></span>
<span data-ttu-id="64041-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="64041-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="64041-127">-MapDefinition</span><span class="sxs-lookup"><span data-stu-id="64041-127">-MapDefinition</span></span>
<span data-ttu-id="64041-128">Egy definícióobjektumot ad meg az integrációs fiók leképezésében.</span><span class="sxs-lookup"><span data-stu-id="64041-128">Specifies a definition object for integration account map.</span></span>
<span data-ttu-id="64041-129">Adja meg ezt a paramétert vagy *a MapFilePath paramétert.*</span><span class="sxs-lookup"><span data-stu-id="64041-129">Specify either this parameter or the *MapFilePath* parameter.</span></span>

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

### <span data-ttu-id="64041-130">-MapFilePath</span><span class="sxs-lookup"><span data-stu-id="64041-130">-MapFilePath</span></span>
<span data-ttu-id="64041-131">Az integrációs fiók leképezés definíciójának fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="64041-131">Specifies the file path of a definition for the integration account map.</span></span> <span data-ttu-id="64041-132">Adja meg ezt a paramétert vagy *a MapDefinition paramétert.*</span><span class="sxs-lookup"><span data-stu-id="64041-132">Specify either this parameter or the *MapDefinition* parameter.</span></span>

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

### <span data-ttu-id="64041-133">-MapName</span><span class="sxs-lookup"><span data-stu-id="64041-133">-MapName</span></span>
<span data-ttu-id="64041-134">Megadja az integrációs fiók térképének nevét.</span><span class="sxs-lookup"><span data-stu-id="64041-134">Specifies a name for the integration account map.</span></span>

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

### <span data-ttu-id="64041-135">-MapType</span><span class="sxs-lookup"><span data-stu-id="64041-135">-MapType</span></span>
<span data-ttu-id="64041-136">Az integrációs fiók térképének típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="64041-136">Specifies the type for the integration account map.</span></span>
<span data-ttu-id="64041-137">Ez a parancsmag térképtípusként támogatja az Xslt-et.</span><span class="sxs-lookup"><span data-stu-id="64041-137">This cmdlet supports Xslt as a map type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Xslt, Xslt20, Xslt30, Liquid

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64041-138">-Metadata</span><span class="sxs-lookup"><span data-stu-id="64041-138">-Metadata</span></span>
<span data-ttu-id="64041-139">A leképezés metaadat-objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="64041-139">Specifies a metadata object for the map.</span></span>

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

### <span data-ttu-id="64041-140">-Name</span><span class="sxs-lookup"><span data-stu-id="64041-140">-Name</span></span>
<span data-ttu-id="64041-141">Megadja az integrációs fiók nevét.</span><span class="sxs-lookup"><span data-stu-id="64041-141">Specifies a name for the integration account.</span></span>

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

### <span data-ttu-id="64041-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64041-142">-ResourceGroupName</span></span>
<span data-ttu-id="64041-143">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="64041-143">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="64041-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="64041-144">-Confirm</span></span>
<span data-ttu-id="64041-145">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="64041-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64041-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64041-146">-WhatIf</span></span>
<span data-ttu-id="64041-147">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="64041-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64041-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="64041-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64041-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64041-149">CommonParameters</span></span>
<span data-ttu-id="64041-150">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64041-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64041-151">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64041-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64041-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="64041-152">INPUTS</span></span>

### <span data-ttu-id="64041-153">System.String</span><span class="sxs-lookup"><span data-stu-id="64041-153">System.String</span></span>

## <span data-ttu-id="64041-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="64041-154">OUTPUTS</span></span>

### <span data-ttu-id="64041-155">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="64041-155">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="64041-156">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="64041-156">NOTES</span></span>

## <span data-ttu-id="64041-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="64041-157">RELATED LINKS</span></span>

[<span data-ttu-id="64041-158">Get-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="64041-158">Get-AzIntegrationAccountMap</span></span>](./Get-AzIntegrationAccountMap.md)

[<span data-ttu-id="64041-159">Remove-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="64041-159">Remove-AzIntegrationAccountMap</span></span>](./Remove-AzIntegrationAccountMap.md)

[<span data-ttu-id="64041-160">Set-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="64041-160">Set-AzIntegrationAccountMap</span></span>](./Set-AzIntegrationAccountMap.md)


