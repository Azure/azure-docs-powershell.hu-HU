---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/powershell/module/az.automation/start-azautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 477b8f5853d9a5dbe3dd030e7419316825088807
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921473"
---
# <span data-ttu-id="497ad-101">Start-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="497ad-101">Start-AzAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="497ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="497ad-102">SYNOPSIS</span></span>
<span data-ttu-id="497ad-103">DSC-csomópont-konfigurációt telepít az automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="497ad-103">Deploys a DSC Node configuration in Automation.</span></span>

## <span data-ttu-id="497ad-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="497ad-104">SYNTAX</span></span>

### <span data-ttu-id="497ad-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="497ad-105">ByAll (Default)</span></span>
```
Start-AzAutomationDscNodeConfigurationDeployment [-NodeConfigurationName] <String> [-NodeName] <String[][]>
 [-Schedule <Schedule>] [-Force] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="497ad-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="497ad-106">ByInputObject</span></span>
```
Start-AzAutomationDscNodeConfigurationDeployment [-NodeConfigurationName] <String> [-NodeName] <String[][]>
 -InputObject <NodeConfigurationDeployment> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="497ad-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="497ad-107">DESCRIPTION</span></span>
<span data-ttu-id="497ad-108">A **Start-AzAutomationDscNodeConfigurationDeployment** parancsmag egy DSC-csomópont-konfigurációt telepít az Azure Automationben.</span><span class="sxs-lookup"><span data-stu-id="497ad-108">The **Start-AzAutomationDscNodeConfigurationDeployment** cmdlet deploys a Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="497ad-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="497ad-109">EXAMPLES</span></span>

### <span data-ttu-id="497ad-110">1. példa: Azure DSC-csomópont konfigurációjának üzembe helyezése az Automatizálásban</span><span class="sxs-lookup"><span data-stu-id="497ad-110">Example 1: Deploy an Azure DSC node configuration in Automation</span></span>
```
PS C:\> $pilot = @("WebServerPilot1", "WebServerPilot2")
PS C:\> $prod = @("WebServerProd1", "WebServerProd2")
PS C:\> $nodes = @($pilot, $prod)
PS C:\> Start-AzAutomationDscNodeConfigurationDeployment `
            -NodeConfigurationName "Config01.Node1" `
            -AutomationAccountName "Contoso01"  `
            -ResourceGroupName "ResourceGroup01" `
            -NodeName $nodes `

Starting a node configuration deployment.
Starting a node configuration deployment. It will override any existing node configurations assigned to the node.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Yes

ResourceGroupName     : ResourceGroup01
AutomationAccountName : Contoso01
JobId                 : 35b14eb4-52b7-4a1d-ad62-8e9f84adc657
Job                   : Microsoft.Azure.Commands.Automation.Model.Job
JobStatus             : New
NodeStatus            :
NodeConfigurationName : Config01.Node1
JobSchedule           :
JobScheduleId         : 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="497ad-111">A fenti parancs a "Config01.Node1" nevű DSC-csomópont-konfigurációt telepíti a Csomópontnevek adott kétdimenziós tömbjéhez.</span><span class="sxs-lookup"><span data-stu-id="497ad-111">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="497ad-112">A telepítés szakaszos módon történik.</span><span class="sxs-lookup"><span data-stu-id="497ad-112">The deployment happens in a staged manner.</span></span>

### <span data-ttu-id="497ad-113">2. példa: Azure DSC-csomópont konfigurációjának ütemezése az Automatizálásban</span><span class="sxs-lookup"><span data-stu-id="497ad-113">Example 2: Schedule an Azure DSC node configuration deployment in Automation</span></span>
```
PS C:\> $sched = New-AzAutomationSchedule -AutomationAccountName "Contoso01" `
            -ResourceGroupName "ResourceGroup01" `
            -Name "TestSchedule" `
            -StartTime "23:00" `
            -OneTime
PS C:\> $pilot = @("WebServerPilot1", "WebServerPilot2")
PS C:\> $prod = @("WebServerProd1", "WebServerProd2")
PS C:\> $nodes = @($pilot, $prod)
PS C:\> Start-AzAutomationDscNodeConfigurationDeployment `
            -NodeConfigurationName "Config01.Node1" `
            -AutomationAccountName "Contoso01"  `
            -ResourceGroupName "ResourceGroup01" `
            -NodeName $nodes `
            -Schedule $sched

Starting a node configuration deployment.
Starting a node configuration deployment. It will override any existing node configurations assigned to the node.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

ResourceGroupName     : ResourceGroup01
AutomationAccountName : Contoso01
JobId                 : 00000000-0000-0000-0000-000000000000
Job                   :
JobStatus             :
NodeStatus            :
NodeConfigurationName : Config01.Node1
JobSchedule           : Microsoft.Azure.Commands.Automation.Model.JobSchedule
JobScheduleId         : 2b1d7738-093d-4ff7-b87b-e4b2321319e5
```

<span data-ttu-id="497ad-114">A fenti parancs a "Config01.Node1" nevű DSC-csomópont-konfigurációt a csomópontnevek adott kétdimenziós tömbjére ütemezi.</span><span class="sxs-lookup"><span data-stu-id="497ad-114">The above command schedules a deployment of a DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="497ad-115">A telepítés szakaszos módon történik, és az ütemezés alapján hajtódik végre.</span><span class="sxs-lookup"><span data-stu-id="497ad-115">The deployment happens in a staged manner and will be executed based on the schedule.</span></span>

## <span data-ttu-id="497ad-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="497ad-116">PARAMETERS</span></span>

### <span data-ttu-id="497ad-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="497ad-117">-AutomationAccountName</span></span>
<span data-ttu-id="497ad-118">Annak az automatizálási fióknak a nevét adja meg, amely a parancsmag által lefordított DSC-konfigurációt tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="497ad-118">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="497ad-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="497ad-119">-DefaultProfile</span></span>
<span data-ttu-id="497ad-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="497ad-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="497ad-121">-Force</span><span class="sxs-lookup"><span data-stu-id="497ad-121">-Force</span></span>
<span data-ttu-id="497ad-122">ps_force</span><span class="sxs-lookup"><span data-stu-id="497ad-122">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="497ad-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="497ad-123">-InputObject</span></span>
<span data-ttu-id="497ad-124">Input object for Piping</span><span class="sxs-lookup"><span data-stu-id="497ad-124">Input object for Piping</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="497ad-125">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="497ad-125">-NodeConfigurationName</span></span>
<span data-ttu-id="497ad-126">A parancsmag által üzembe helyezett DSC-csomópont-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="497ad-126">Specifies the name of the DSC node configuration that this cmdlet deploys.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObject
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="497ad-127">-NodeName</span><span class="sxs-lookup"><span data-stu-id="497ad-127">-NodeName</span></span>
<span data-ttu-id="497ad-128">Megadja azoknak a csomópontoknak a nevét, amelyekre a csomópont-konfigurációt telepíteni szeretné.</span><span class="sxs-lookup"><span data-stu-id="497ad-128">Specifies the names of the nodes to which the Node Configuration would be deployed to.</span></span>

```yaml
Type: System.String[][]
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="497ad-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="497ad-129">-ResourceGroupName</span></span>
<span data-ttu-id="497ad-130">Annak az erőforráscsoportnak a nevét adja meg, amelyben ez a parancsmag konfigurációt fordít.</span><span class="sxs-lookup"><span data-stu-id="497ad-130">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="497ad-131">-Schedule</span><span class="sxs-lookup"><span data-stu-id="497ad-131">-Schedule</span></span>
<span data-ttu-id="497ad-132">Automatizálási ütemezési objektum a telepítési feladat ütemezéséhez.</span><span class="sxs-lookup"><span data-stu-id="497ad-132">Automation Schedule object to schedule the deployment job.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.Schedule
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="497ad-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="497ad-133">-Confirm</span></span>
<span data-ttu-id="497ad-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="497ad-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="497ad-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="497ad-135">-WhatIf</span></span>
<span data-ttu-id="497ad-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="497ad-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="497ad-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="497ad-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="497ad-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="497ad-138">CommonParameters</span></span>
<span data-ttu-id="497ad-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="497ad-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="497ad-140">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="497ad-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="497ad-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="497ad-141">INPUTS</span></span>

### <span data-ttu-id="497ad-142">System.String</span><span class="sxs-lookup"><span data-stu-id="497ad-142">System.String</span></span>

### <span data-ttu-id="497ad-143">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="497ad-143">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="497ad-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="497ad-144">OUTPUTS</span></span>

### <span data-ttu-id="497ad-145">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="497ad-145">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="497ad-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="497ad-146">NOTES</span></span>

## <span data-ttu-id="497ad-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="497ad-147">RELATED LINKS</span></span>

[<span data-ttu-id="497ad-148">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="497ad-148">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="497ad-149">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="497ad-149">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="497ad-150">Stop-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="497ad-150">Stop-AzAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="497ad-151">Get-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="497ad-151">Get-AzAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="497ad-152">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="497ad-152">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md)

[<span data-ttu-id="497ad-153">New-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="497ad-153">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)
