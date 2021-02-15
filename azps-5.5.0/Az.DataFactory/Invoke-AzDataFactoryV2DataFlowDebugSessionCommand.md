---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/invoke-azdatafactoryv2dataflowdebugsessioncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md
ms.openlocfilehash: 4009835b2efe8346ff873bde59870954c73ab5d7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165410"
---
# <span data-ttu-id="59c2b-101">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="59c2b-101">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>

## <span data-ttu-id="59c2b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59c2b-102">SYNOPSIS</span></span>
<span data-ttu-id="59c2b-103">Hibakeresési művelet meghívása adatfolyam-hibakeresési munkamenetben.</span><span class="sxs-lookup"><span data-stu-id="59c2b-103">Invoke debug action in data flow debug session.</span></span>

## <span data-ttu-id="59c2b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="59c2b-104">SYNTAX</span></span>

### <span data-ttu-id="59c2b-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="59c2b-105">ByFactoryName (Default)</span></span>
```
Invoke-AzDataFactoryV2DataFlowDebugSessionCommand [-SessionId] <String> [-Command] <String>
 [-StreamName] <String> [[-RowLimits] <Int32>] [[-Expression] <String>]
 [[-Columns] <System.Collections.Generic.List`1[System.String]>] [-AsJob] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="59c2b-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="59c2b-106">ByFactoryObject</span></span>
```
Invoke-AzDataFactoryV2DataFlowDebugSessionCommand [-SessionId] <String> [-Command] <String>
 [-StreamName] <String> [[-RowLimits] <Int32>] [[-Expression] <String>]
 [[-Columns] <System.Collections.Generic.List`1[System.String]>] [-AsJob] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59c2b-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="59c2b-107">ByResourceId</span></span>
```
Invoke-AzDataFactoryV2DataFlowDebugSessionCommand [-SessionId] <String> [-Command] <String>
 [-StreamName] <String> [[-RowLimits] <Int32>] [[-Expression] <String>]
 [[-Columns] <System.Collections.Generic.List`1[System.String]>] [-AsJob] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59c2b-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="59c2b-108">DESCRIPTION</span></span>
<span data-ttu-id="59c2b-109">Ez a parancs végrehajtja az adat előnézetét/stats előnézetét/kifejezés előnézetét a különböző adatfolyamok hibakeresési munkamenetben való végrehajtásához.</span><span class="sxs-lookup"><span data-stu-id="59c2b-109">This command executes data preview/stats preview/expression preview for different stream of data flow in debug session.</span></span>
<span data-ttu-id="59c2b-110">Az adatfolyam-hibakeresési munkafolyamat PowerShell-parancssorának a következőnek kell lennie:</span><span class="sxs-lookup"><span data-stu-id="59c2b-110">The PowerShell command sequence for data flow debug workflow should be:</span></span>
1. <span data-ttu-id="59c2b-111">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="59c2b-111">Start-AzDataFactoryV2DataFlowDebugSession</span></span>
1. <span data-ttu-id="59c2b-112">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="59c2b-112">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>
1. <span data-ttu-id="59c2b-113">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (ismételje meg ezt a lépést a különböző parancsok/célok esetén, vagy ismételje meg a 2–3. lépést a csomagfájl módosítása érdekében)</span><span class="sxs-lookup"><span data-stu-id="59c2b-113">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (repeat this step for different commands/targets, or repeat step 2-3 in order to change the package file)</span></span>
1. <span data-ttu-id="59c2b-114">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="59c2b-114">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="59c2b-115">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="59c2b-115">EXAMPLES</span></span>

### <span data-ttu-id="59c2b-116">1. példa</span><span class="sxs-lookup"><span data-stu-id="59c2b-116">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> $result = Invoke-AzDataFactoryV2DataFlowDebugSessionCommand -ResourceGroupName adf -DataFactoryName WiKiADF -Command executePreviewQuery -SessionId fd76cd0d-8b37-4dc0-a370-3f9d43ac686d -StreamName source1 -RowLimits 100 -AsJob
PS C:\WINDOWS\system32> $result

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
3      Long Running... AzureLongRun... Running       True            localhost            Invoke-AzDataFactoryV2...


(After 2 minutes)

PS C:\WINDOWS\system32> $result

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
3      Long Running... AzureLongRun... Completed     True            localhost            Invoke-AzDataFactoryV2...

PS C:\WINDOWS\system32> $output = ConvertFrom-Json($result.Output.Data)
PS C:\WINDOWS\system32> $output.output

    {
      "schema": "output(ResourceAgencyNum as string, PublicName as string)" ,
      "data": [["4445679354", "Syrian Refugee Information", 1], ["44456793", "Syrian Refugee Information", 1]]
    }


```

<span data-ttu-id="59c2b-117">Ez a példa meghívja az "fd76cd0d-8b37-4dc0-a370-3f9d43ac686d" hibakeresési munkamenet adatbetekintő parancsát a "WiKiADF" adatüzemben, majd olvasható karakterláncba konvertálja a JSON kimenetet.</span><span class="sxs-lookup"><span data-stu-id="59c2b-117">This example invokes data preview command for debug session "fd76cd0d-8b37-4dc0-a370-3f9d43ac686d" in data factory "WiKiADF" and then convert the JSON output into readable string.</span></span>

## <span data-ttu-id="59c2b-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="59c2b-118">PARAMETERS</span></span>

### <span data-ttu-id="59c2b-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="59c2b-119">-AsJob</span></span>
<span data-ttu-id="59c2b-120">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="59c2b-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="59c2b-121">-Columns</span><span class="sxs-lookup"><span data-stu-id="59c2b-121">-Columns</span></span>
<span data-ttu-id="59c2b-122">The columns list for data flow statistics preview.</span><span class="sxs-lookup"><span data-stu-id="59c2b-122">The columns list for data flow statistics preview.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59c2b-123">-Command</span><span class="sxs-lookup"><span data-stu-id="59c2b-123">-Command</span></span>
<span data-ttu-id="59c2b-124">Az adatfolyam hibakeresési parancsa.</span><span class="sxs-lookup"><span data-stu-id="59c2b-124">The data flow debug command.</span></span> <span data-ttu-id="59c2b-125">Optionals are executePreviewQuery, executeStatisticsQuery and executeExpressionQuery</span><span class="sxs-lookup"><span data-stu-id="59c2b-125">Optionals are executePreviewQuery, executeStatisticsQuery and executeExpressionQuery</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59c2b-126">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="59c2b-126">-DataFactory</span></span>
<span data-ttu-id="59c2b-127">A data factory objektum.</span><span class="sxs-lookup"><span data-stu-id="59c2b-127">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59c2b-128">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="59c2b-128">-DataFactoryName</span></span>
<span data-ttu-id="59c2b-129">Az adatüzem neve.</span><span class="sxs-lookup"><span data-stu-id="59c2b-129">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59c2b-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59c2b-130">-DefaultProfile</span></span>
<span data-ttu-id="59c2b-131">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="59c2b-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59c2b-132">-Expression</span><span class="sxs-lookup"><span data-stu-id="59c2b-132">-Expression</span></span>
<span data-ttu-id="59c2b-133">Az adatfolyam-kifejezés előnézetének kifejezése.</span><span class="sxs-lookup"><span data-stu-id="59c2b-133">The expression for data flow expression preview.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59c2b-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59c2b-134">-ResourceGroupName</span></span>
<span data-ttu-id="59c2b-135">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="59c2b-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59c2b-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="59c2b-136">-ResourceId</span></span>
<span data-ttu-id="59c2b-137">Az Azure-erőforrásazonosító.</span><span class="sxs-lookup"><span data-stu-id="59c2b-137">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59c2b-138">-RowLimits</span><span class="sxs-lookup"><span data-stu-id="59c2b-138">-RowLimits</span></span>
<span data-ttu-id="59c2b-139">Az adatfolyamok előnézeti sorkorlátja.</span><span class="sxs-lookup"><span data-stu-id="59c2b-139">The row limit for data flow data preview.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59c2b-140">-SessionId</span><span class="sxs-lookup"><span data-stu-id="59c2b-140">-SessionId</span></span>
<span data-ttu-id="59c2b-141">Az adatfolyam hibakeresési munkamenet azonosítója.</span><span class="sxs-lookup"><span data-stu-id="59c2b-141">The data flow debug session ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59c2b-142">-StreamName</span><span class="sxs-lookup"><span data-stu-id="59c2b-142">-StreamName</span></span>
<span data-ttu-id="59c2b-143">A hibakeresés adatfolyamának neve.</span><span class="sxs-lookup"><span data-stu-id="59c2b-143">The stream name of data flow for debugging.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59c2b-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="59c2b-144">-Confirm</span></span>
<span data-ttu-id="59c2b-145">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="59c2b-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59c2b-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59c2b-146">-WhatIf</span></span>
<span data-ttu-id="59c2b-147">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="59c2b-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59c2b-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="59c2b-148">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59c2b-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59c2b-149">CommonParameters</span></span>
<span data-ttu-id="59c2b-150">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59c2b-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59c2b-151">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="59c2b-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59c2b-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="59c2b-152">INPUTS</span></span>

### <span data-ttu-id="59c2b-153">System.String</span><span class="sxs-lookup"><span data-stu-id="59c2b-153">System.String</span></span>

### <span data-ttu-id="59c2b-154">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="59c2b-154">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="59c2b-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="59c2b-155">OUTPUTS</span></span>

### <span data-ttu-id="59c2b-156">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionCommandResult</span><span class="sxs-lookup"><span data-stu-id="59c2b-156">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionCommandResult</span></span>

## <span data-ttu-id="59c2b-157">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="59c2b-157">NOTES</span></span>
<span data-ttu-id="59c2b-158">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, kezelő, adatok, faktorokKeywords: azure, azurerm, arm, erőforrás, kezelés, vezető, adatok, faktorok</span><span class="sxs-lookup"><span data-stu-id="59c2b-158">Keywords: azure, azurerm, arm, resource, management, manager, data, factoriesKeywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="59c2b-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="59c2b-159">RELATED LINKS</span></span>

[<span data-ttu-id="59c2b-160">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="59c2b-160">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="59c2b-161">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="59c2b-161">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="59c2b-162">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="59c2b-162">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="59c2b-163">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="59c2b-163">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)
