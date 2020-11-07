---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/invoke-azdatafactoryv2dataflowdebugsessioncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md
ms.openlocfilehash: 45419ede425b5d5ea3ba9fcbbbfb024fe8ba9358
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667040"
---
# <span data-ttu-id="56f86-101">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="56f86-101">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>

## <span data-ttu-id="56f86-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="56f86-102">SYNOPSIS</span></span>
<span data-ttu-id="56f86-103">Hibakeresési műveletek indítása az adatfolyam-hibakeresési munkamenetben.</span><span class="sxs-lookup"><span data-stu-id="56f86-103">Invoke debug action in data flow debug session.</span></span>

## <span data-ttu-id="56f86-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="56f86-104">SYNTAX</span></span>

### <span data-ttu-id="56f86-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="56f86-105">ByFactoryName (Default)</span></span>
```
Invoke-AzDataFactoryV2DataFlowDebugSessionCommand [-SessionId] <String> [-Command] <String>
 [-StreamName] <String> [[-RowLimits] <Int32>] [[-Expression] <String>]
 [[-Columns] <System.Collections.Generic.List`1[System.String]>] [-AsJob] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="56f86-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="56f86-106">ByFactoryObject</span></span>
```
Invoke-AzDataFactoryV2DataFlowDebugSessionCommand [-SessionId] <String> [-Command] <String>
 [-StreamName] <String> [[-RowLimits] <Int32>] [[-Expression] <String>]
 [[-Columns] <System.Collections.Generic.List`1[System.String]>] [-AsJob] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56f86-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="56f86-107">ByResourceId</span></span>
```
Invoke-AzDataFactoryV2DataFlowDebugSessionCommand [-SessionId] <String> [-Command] <String>
 [-StreamName] <String> [[-RowLimits] <Int32>] [[-Expression] <String>]
 [[-Columns] <System.Collections.Generic.List`1[System.String]>] [-AsJob] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56f86-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="56f86-108">DESCRIPTION</span></span>
<span data-ttu-id="56f86-109">Ez a parancs végrehajtja a hibakeresési munkamenetben az adatáramlás különböző adatfolyamait az előzetes verzió/statisztika előzetes verzió/kifejezés előzetes verziójában.</span><span class="sxs-lookup"><span data-stu-id="56f86-109">This command executes data preview/stats preview/expression preview for different stream of data flow in debug session.</span></span>
<span data-ttu-id="56f86-110">A PowerShell-parancsok az adatfolyam-hibakeresési munkafolyamatban a következőket tartalmazzák:</span><span class="sxs-lookup"><span data-stu-id="56f86-110">The PowerShell command sequence for data flow debug workflow should be:</span></span>
1. <span data-ttu-id="56f86-111">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="56f86-111">Start-AzDataFactoryV2DataFlowDebugSession</span></span>
1. <span data-ttu-id="56f86-112">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="56f86-112">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>
1. <span data-ttu-id="56f86-113">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (ismételje meg ezt a lépést a különböző parancsok/célok esetén, vagy ismételje meg az 2-3-es lépést a csomagfájl módosítása céljából)</span><span class="sxs-lookup"><span data-stu-id="56f86-113">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (repeat this step for different commands/targets, or repeat step 2-3 in order to change the package file)</span></span>
1. <span data-ttu-id="56f86-114">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="56f86-114">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="56f86-115">Példák</span><span class="sxs-lookup"><span data-stu-id="56f86-115">EXAMPLES</span></span>

### <span data-ttu-id="56f86-116">Példa 1</span><span class="sxs-lookup"><span data-stu-id="56f86-116">Example 1</span></span>
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

<span data-ttu-id="56f86-117">Ebben a példában a "fd76cd0d-8b37-4dc0-a370-3f9d43ac686d" Data Factory "WiKiADF" "az adatábrázoló" parancsa, majd a JSON-kimenet olvasható karakterláncba konvertálása</span><span class="sxs-lookup"><span data-stu-id="56f86-117">This example invokes data preview command for debug session "fd76cd0d-8b37-4dc0-a370-3f9d43ac686d" in data factory "WiKiADF" and then convert the JSON output into readable string.</span></span>

## <span data-ttu-id="56f86-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="56f86-118">PARAMETERS</span></span>

### <span data-ttu-id="56f86-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="56f86-119">-AsJob</span></span>
<span data-ttu-id="56f86-120">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="56f86-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="56f86-121">– Oszlopok</span><span class="sxs-lookup"><span data-stu-id="56f86-121">-Columns</span></span>
<span data-ttu-id="56f86-122">Az adatáramlási statisztika előnézetének oszlopok listája.</span><span class="sxs-lookup"><span data-stu-id="56f86-122">The columns list for data flow statistics preview.</span></span>

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

### <span data-ttu-id="56f86-123">-Command</span><span class="sxs-lookup"><span data-stu-id="56f86-123">-Command</span></span>
<span data-ttu-id="56f86-124">A Data flow debug parancs.</span><span class="sxs-lookup"><span data-stu-id="56f86-124">The data flow debug command.</span></span> <span data-ttu-id="56f86-125">Nem kötelező a executePreviewQuery, az executeStatisticsQuery és a executeExpressionQuery</span><span class="sxs-lookup"><span data-stu-id="56f86-125">Optionals are executePreviewQuery, executeStatisticsQuery and executeExpressionQuery</span></span>

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

### <span data-ttu-id="56f86-126">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="56f86-126">-DataFactory</span></span>
<span data-ttu-id="56f86-127">Az Data Factory objektum.</span><span class="sxs-lookup"><span data-stu-id="56f86-127">The data factory object.</span></span>

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

### <span data-ttu-id="56f86-128">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="56f86-128">-DataFactoryName</span></span>
<span data-ttu-id="56f86-129">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="56f86-129">The data factory name.</span></span>

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

### <span data-ttu-id="56f86-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56f86-130">-DefaultProfile</span></span>
<span data-ttu-id="56f86-131">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="56f86-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56f86-132">-Kifejezés</span><span class="sxs-lookup"><span data-stu-id="56f86-132">-Expression</span></span>
<span data-ttu-id="56f86-133">Az adatáramlási kifejezés előnézetének kifejezése.</span><span class="sxs-lookup"><span data-stu-id="56f86-133">The expression for data flow expression preview.</span></span>

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

### <span data-ttu-id="56f86-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56f86-134">-ResourceGroupName</span></span>
<span data-ttu-id="56f86-135">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="56f86-135">The resource group name.</span></span>

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

### <span data-ttu-id="56f86-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="56f86-136">-ResourceId</span></span>
<span data-ttu-id="56f86-137">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="56f86-137">The Azure resource ID.</span></span>

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

### <span data-ttu-id="56f86-138">-RowLimits</span><span class="sxs-lookup"><span data-stu-id="56f86-138">-RowLimits</span></span>
<span data-ttu-id="56f86-139">Az adatfolyam-adattovábbítás sorának korlátja.</span><span class="sxs-lookup"><span data-stu-id="56f86-139">The row limit for data flow data preview.</span></span>

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

### <span data-ttu-id="56f86-140">-Munkamenet</span><span class="sxs-lookup"><span data-stu-id="56f86-140">-SessionId</span></span>
<span data-ttu-id="56f86-141">Az adatfolyam-debug munkamenet azonosítója.</span><span class="sxs-lookup"><span data-stu-id="56f86-141">The data flow debug session ID.</span></span>

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

### <span data-ttu-id="56f86-142">-StreamName</span><span class="sxs-lookup"><span data-stu-id="56f86-142">-StreamName</span></span>
<span data-ttu-id="56f86-143">A hibakereséshez használt adatfolyam neve.</span><span class="sxs-lookup"><span data-stu-id="56f86-143">The stream name of data flow for debugging.</span></span>

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

### <span data-ttu-id="56f86-144">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="56f86-144">-Confirm</span></span>
<span data-ttu-id="56f86-145">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="56f86-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56f86-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56f86-146">-WhatIf</span></span>
<span data-ttu-id="56f86-147">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="56f86-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56f86-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="56f86-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56f86-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56f86-149">CommonParameters</span></span>
<span data-ttu-id="56f86-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="56f86-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56f86-151">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="56f86-151">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56f86-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="56f86-152">INPUTS</span></span>

### <span data-ttu-id="56f86-153">System. String</span><span class="sxs-lookup"><span data-stu-id="56f86-153">System.String</span></span>

### <span data-ttu-id="56f86-154">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="56f86-154">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="56f86-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="56f86-155">OUTPUTS</span></span>

### <span data-ttu-id="56f86-156">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionCommandResult</span><span class="sxs-lookup"><span data-stu-id="56f86-156">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionCommandResult</span></span>

## <span data-ttu-id="56f86-157">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="56f86-157">NOTES</span></span>
<span data-ttu-id="56f86-158">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, factoriesKeywords: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="56f86-158">Keywords: azure, azurerm, arm, resource, management, manager, data, factoriesKeywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="56f86-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="56f86-159">RELATED LINKS</span></span>

[<span data-ttu-id="56f86-160">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="56f86-160">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="56f86-161">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="56f86-161">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="56f86-162">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="56f86-162">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="56f86-163">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="56f86-163">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)
