---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/start-azdatafactoryv2dataflowdebugsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2DataFlowDebugSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2DataFlowDebugSession.md
ms.openlocfilehash: 27a7f0ee401f044cc693cecf103f2bed1e8ce946
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847110"
---
# <span data-ttu-id="47fd8-101">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="47fd8-101">Start-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="47fd8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="47fd8-102">SYNOPSIS</span></span>
<span data-ttu-id="47fd8-103">Adatfolyam-debug munkamenet indítása az Azure Data Factory-ban</span><span class="sxs-lookup"><span data-stu-id="47fd8-103">Starts a data flow debug session in Azure Data Factory</span></span>

## <span data-ttu-id="47fd8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="47fd8-104">SYNTAX</span></span>

### <span data-ttu-id="47fd8-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="47fd8-105">ByFactoryName (Default)</span></span>
```
Start-AzDataFactoryV2DataFlowDebugSession [[-IntegrationRuntimeFile] <String>] [-AsJob]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47fd8-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="47fd8-106">ByFactoryObject</span></span>
```
Start-AzDataFactoryV2DataFlowDebugSession [[-IntegrationRuntimeFile] <String>] [-AsJob]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="47fd8-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="47fd8-107">ByResourceId</span></span>
```
Start-AzDataFactoryV2DataFlowDebugSession [[-IntegrationRuntimeFile] <String>] [-AsJob] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47fd8-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="47fd8-108">DESCRIPTION</span></span>
<span data-ttu-id="47fd8-109">Ez a hosszú futó parancs a közelgő debug parancsok adatfolyam-hibakeresési munkamenetét indítja el.</span><span class="sxs-lookup"><span data-stu-id="47fd8-109">This long running command starts a data flow debug session for the upcoming debug commands.</span></span> <span data-ttu-id="47fd8-110">Ez a parancs egy integrációs futtatókörnyezet-definícióval tud csatlakozni a Debug-munkamenetek fürtjének méretének és típusának beállításához.</span><span class="sxs-lookup"><span data-stu-id="47fd8-110">This command can attach with an integration runtime definition to configure the size/type of debug session cluster.</span></span>
<span data-ttu-id="47fd8-111">A PowerShell-parancsok az adatfolyam-hibakeresési munkafolyamatban a következőket tartalmazzák:</span><span class="sxs-lookup"><span data-stu-id="47fd8-111">The PowerShell command sequence for data flow debug workflow should be:</span></span>
1. <span data-ttu-id="47fd8-112">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="47fd8-112">Start-AzDataFactoryV2DataFlowDebugSession</span></span>
1. <span data-ttu-id="47fd8-113">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="47fd8-113">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>
1. <span data-ttu-id="47fd8-114">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (ismételje meg ezt a lépést a különböző parancsok/célok esetén, vagy ismételje meg az 2-3-es lépést a csomagfájl módosítása céljából)</span><span class="sxs-lookup"><span data-stu-id="47fd8-114">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (repeat this step for different commands/targets, or repeat step 2-3 in order to change the package file)</span></span>
1. <span data-ttu-id="47fd8-115">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="47fd8-115">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="47fd8-116">Példák</span><span class="sxs-lookup"><span data-stu-id="47fd8-116">EXAMPLES</span></span>

### <span data-ttu-id="47fd8-117">Példa 1</span><span class="sxs-lookup"><span data-stu-id="47fd8-117">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> $job = Start-AzDataFactoryV2DataFlowDebugSession -ResourceGroupName adf -DataFactoryName jikma0601sea -AsJob
PS C:\WINDOWS\system32> $job 

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
1      Long Running... AzureLongRun... Running       True            localhost            Start-AzDataFactoryV2D...

(After 5 minutes)

PS C:\WINDOWS\system32> $job

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
1      Long Running... AzureLongRun... Completed     True            localhost            Start-AzDataFactoryV2D...


PS C:\WINDOWS\system32> $job.Output

SessionId                            Status
---------                            ------
550effe4-93a3-485c-8525-eaf25259efbd Succeeded

```

<span data-ttu-id="47fd8-118">Elindítja a Debug-munkamenetet a AsJob-jelölővel.</span><span class="sxs-lookup"><span data-stu-id="47fd8-118">Starts a debug session with AsJob flag.</span></span>

## <span data-ttu-id="47fd8-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="47fd8-119">PARAMETERS</span></span>

### <span data-ttu-id="47fd8-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="47fd8-120">-AsJob</span></span>
<span data-ttu-id="47fd8-121">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="47fd8-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="47fd8-122">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="47fd8-122">-DataFactory</span></span>
<span data-ttu-id="47fd8-123">Az Data Factory objektum.</span><span class="sxs-lookup"><span data-stu-id="47fd8-123">The data factory object.</span></span>

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

### <span data-ttu-id="47fd8-124">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="47fd8-124">-DataFactoryName</span></span>
<span data-ttu-id="47fd8-125">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="47fd8-125">The data factory name.</span></span>

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

### <span data-ttu-id="47fd8-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47fd8-126">-DefaultProfile</span></span>
<span data-ttu-id="47fd8-127">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="47fd8-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47fd8-128">-IntegrationRuntimeFile</span><span class="sxs-lookup"><span data-stu-id="47fd8-128">-IntegrationRuntimeFile</span></span>
<span data-ttu-id="47fd8-129">A JSON-fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="47fd8-129">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47fd8-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47fd8-130">-ResourceGroupName</span></span>
<span data-ttu-id="47fd8-131">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="47fd8-131">The resource group name.</span></span>

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

### <span data-ttu-id="47fd8-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="47fd8-132">-ResourceId</span></span>
<span data-ttu-id="47fd8-133">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="47fd8-133">The Azure resource ID.</span></span>

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

### <span data-ttu-id="47fd8-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="47fd8-134">-Confirm</span></span>
<span data-ttu-id="47fd8-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="47fd8-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47fd8-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47fd8-136">-WhatIf</span></span>
<span data-ttu-id="47fd8-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="47fd8-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47fd8-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="47fd8-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47fd8-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47fd8-139">CommonParameters</span></span>
<span data-ttu-id="47fd8-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="47fd8-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47fd8-141">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="47fd8-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47fd8-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="47fd8-142">INPUTS</span></span>

### <span data-ttu-id="47fd8-143">System. String</span><span class="sxs-lookup"><span data-stu-id="47fd8-143">System.String</span></span>

### <span data-ttu-id="47fd8-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="47fd8-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="47fd8-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="47fd8-145">OUTPUTS</span></span>

### <span data-ttu-id="47fd8-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="47fd8-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSession</span></span>

## <span data-ttu-id="47fd8-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="47fd8-147">NOTES</span></span>
<span data-ttu-id="47fd8-148">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="47fd8-148">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="47fd8-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="47fd8-149">RELATED LINKS</span></span>

[<span data-ttu-id="47fd8-150">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="47fd8-150">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="47fd8-151">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="47fd8-151">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="47fd8-152">Meghívó-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="47fd8-152">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)

[<span data-ttu-id="47fd8-153">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="47fd8-153">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)