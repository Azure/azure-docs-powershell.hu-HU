---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/start-azdatafactoryv2dataflowdebugsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2DataFlowDebugSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2DataFlowDebugSession.md
ms.openlocfilehash: 27a7f0ee401f044cc693cecf103f2bed1e8ce946
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480381"
---
# <span data-ttu-id="f8236-101">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="f8236-101">Start-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="f8236-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8236-102">SYNOPSIS</span></span>
<span data-ttu-id="f8236-103">Adatfolyam-hibakeresési munkamenet indítása az Azure Data Factoryban</span><span class="sxs-lookup"><span data-stu-id="f8236-103">Starts a data flow debug session in Azure Data Factory</span></span>

## <span data-ttu-id="f8236-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f8236-104">SYNTAX</span></span>

### <span data-ttu-id="f8236-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f8236-105">ByFactoryName (Default)</span></span>
```
Start-AzDataFactoryV2DataFlowDebugSession [[-IntegrationRuntimeFile] <String>] [-AsJob]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8236-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="f8236-106">ByFactoryObject</span></span>
```
Start-AzDataFactoryV2DataFlowDebugSession [[-IntegrationRuntimeFile] <String>] [-AsJob]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f8236-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f8236-107">ByResourceId</span></span>
```
Start-AzDataFactoryV2DataFlowDebugSession [[-IntegrationRuntimeFile] <String>] [-AsJob] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8236-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f8236-108">DESCRIPTION</span></span>
<span data-ttu-id="f8236-109">Ez a hosszú ideig futó parancs adatfolyam-hibakeresési munkamenetet kezd a közelgő hibakeresési parancsokhoz.</span><span class="sxs-lookup"><span data-stu-id="f8236-109">This long running command starts a data flow debug session for the upcoming debug commands.</span></span> <span data-ttu-id="f8236-110">Ez a parancs egy integrációs futásidejű definícióval csatolható a hibakeresési munkamenetcsoport méretének/típusának beállításához.</span><span class="sxs-lookup"><span data-stu-id="f8236-110">This command can attach with an integration runtime definition to configure the size/type of debug session cluster.</span></span>
<span data-ttu-id="f8236-111">Az adatfolyam-hibakeresési munkafolyamat PowerShell-parancssorának a következőnek kell lennie:</span><span class="sxs-lookup"><span data-stu-id="f8236-111">The PowerShell command sequence for data flow debug workflow should be:</span></span>
1. <span data-ttu-id="f8236-112">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="f8236-112">Start-AzDataFactoryV2DataFlowDebugSession</span></span>
1. <span data-ttu-id="f8236-113">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="f8236-113">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>
1. <span data-ttu-id="f8236-114">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (ismételje meg ezt a lépést a különböző parancsok/célok esetén, vagy ismételje meg a 2–3. lépést a csomagfájl módosítása érdekében)</span><span class="sxs-lookup"><span data-stu-id="f8236-114">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (repeat this step for different commands/targets, or repeat step 2-3 in order to change the package file)</span></span>
1. <span data-ttu-id="f8236-115">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="f8236-115">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="f8236-116">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f8236-116">EXAMPLES</span></span>

### <span data-ttu-id="f8236-117">1. példa</span><span class="sxs-lookup"><span data-stu-id="f8236-117">Example 1</span></span>
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

<span data-ttu-id="f8236-118">Hibakeresési munkamenetet kezd AsBug jelzővel.</span><span class="sxs-lookup"><span data-stu-id="f8236-118">Starts a debug session with AsJob flag.</span></span>

## <span data-ttu-id="f8236-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f8236-119">PARAMETERS</span></span>

### <span data-ttu-id="f8236-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f8236-120">-AsJob</span></span>
<span data-ttu-id="f8236-121">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="f8236-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f8236-122">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="f8236-122">-DataFactory</span></span>
<span data-ttu-id="f8236-123">A data factory objektum.</span><span class="sxs-lookup"><span data-stu-id="f8236-123">The data factory object.</span></span>

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

### <span data-ttu-id="f8236-124">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f8236-124">-DataFactoryName</span></span>
<span data-ttu-id="f8236-125">Az adatüzem neve.</span><span class="sxs-lookup"><span data-stu-id="f8236-125">The data factory name.</span></span>

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

### <span data-ttu-id="f8236-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8236-126">-DefaultProfile</span></span>
<span data-ttu-id="f8236-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f8236-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8236-128">-IntegrationRuntimeFile</span><span class="sxs-lookup"><span data-stu-id="f8236-128">-IntegrationRuntimeFile</span></span>
<span data-ttu-id="f8236-129">A JSON fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="f8236-129">The JSON file path.</span></span>

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

### <span data-ttu-id="f8236-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8236-130">-ResourceGroupName</span></span>
<span data-ttu-id="f8236-131">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f8236-131">The resource group name.</span></span>

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

### <span data-ttu-id="f8236-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f8236-132">-ResourceId</span></span>
<span data-ttu-id="f8236-133">Az Azure-erőforrásazonosító.</span><span class="sxs-lookup"><span data-stu-id="f8236-133">The Azure resource ID.</span></span>

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

### <span data-ttu-id="f8236-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f8236-134">-Confirm</span></span>
<span data-ttu-id="f8236-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f8236-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8236-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8236-136">-WhatIf</span></span>
<span data-ttu-id="f8236-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f8236-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8236-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f8236-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8236-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8236-139">CommonParameters</span></span>
<span data-ttu-id="f8236-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8236-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8236-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f8236-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8236-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f8236-142">INPUTS</span></span>

### <span data-ttu-id="f8236-143">System.String</span><span class="sxs-lookup"><span data-stu-id="f8236-143">System.String</span></span>

### <span data-ttu-id="f8236-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="f8236-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="f8236-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f8236-145">OUTPUTS</span></span>

### <span data-ttu-id="f8236-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="f8236-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSession</span></span>

## <span data-ttu-id="f8236-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f8236-147">NOTES</span></span>
<span data-ttu-id="f8236-148">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, adatok, faktorok</span><span class="sxs-lookup"><span data-stu-id="f8236-148">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="f8236-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f8236-149">RELATED LINKS</span></span>

[<span data-ttu-id="f8236-150">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="f8236-150">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="f8236-151">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="f8236-151">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="f8236-152">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="f8236-152">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)

[<span data-ttu-id="f8236-153">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="f8236-153">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)