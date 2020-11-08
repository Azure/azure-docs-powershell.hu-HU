---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/start-azautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 41605bbdd37ae29f420581f9ad916a1cc87150be
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017912"
---
# <span data-ttu-id="abeb6-101">Start-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="abeb6-101">Start-AzAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="abeb6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="abeb6-102">SYNOPSIS</span></span>
<span data-ttu-id="abeb6-103">A DSC csomópontok konfigurációját telepíti automatizálással.</span><span class="sxs-lookup"><span data-stu-id="abeb6-103">Deploys a DSC Node configuration in Automation.</span></span>

## <span data-ttu-id="abeb6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="abeb6-104">SYNTAX</span></span>

### <span data-ttu-id="abeb6-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="abeb6-105">ByAll (Default)</span></span>
```
Start-AzAutomationDscNodeConfigurationDeployment [-NodeConfigurationName] <String> [-NodeName] <String[][]>
 [-Schedule <Schedule>] [-Force] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abeb6-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="abeb6-106">ByInputObject</span></span>
```
Start-AzAutomationDscNodeConfigurationDeployment [-NodeConfigurationName] <String> [-NodeName] <String[][]>
 -InputObject <NodeConfigurationDeployment> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abeb6-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="abeb6-107">DESCRIPTION</span></span>
<span data-ttu-id="abeb6-108">A **Start-AzAutomationDscNodeConfigurationDeployment** parancsmag a kívánt állapot-konfigurációs (DSC) csomópont-konfigurációt telepíti az Azure automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="abeb6-108">The **Start-AzAutomationDscNodeConfigurationDeployment** cmdlet deploys a Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="abeb6-109">Példák</span><span class="sxs-lookup"><span data-stu-id="abeb6-109">EXAMPLES</span></span>

### <span data-ttu-id="abeb6-110">1. példa: Azure DSC csomópont-konfiguráció telepítése automatizálással</span><span class="sxs-lookup"><span data-stu-id="abeb6-110">Example 1: Deploy an Azure DSC node configuration in Automation</span></span>
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

<span data-ttu-id="abeb6-111">A fenti parancs az "Config01. Node1" nevű DSC csomópont-konfigurációt telepíti a csomópontok nevének adott kétdimenziós sorába.</span><span class="sxs-lookup"><span data-stu-id="abeb6-111">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="abeb6-112">A telepítés szakaszos módon történik.</span><span class="sxs-lookup"><span data-stu-id="abeb6-112">The deployment happens in a staged manner.</span></span>

### <span data-ttu-id="abeb6-113">2. példa: az Azure DSC csomópont-konfiguráció bevezetésének ütemezése automatizálással</span><span class="sxs-lookup"><span data-stu-id="abeb6-113">Example 2: Schedule an Azure DSC node configuration deployment in Automation</span></span>
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

<span data-ttu-id="abeb6-114">A fenti parancs az "Config01. Node1" nevű DSC-csomópont konfigurációját ütemezi a csomópontok adott kétdimenziós sorába.</span><span class="sxs-lookup"><span data-stu-id="abeb6-114">The above command schedules a deployment of a DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="abeb6-115">A telepítés szakaszos módon történik, és a program az ütemterv alapján hajtja végre.</span><span class="sxs-lookup"><span data-stu-id="abeb6-115">The deployment happens in a staged manner and will be executed based on the schedule.</span></span>

## <span data-ttu-id="abeb6-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="abeb6-116">PARAMETERS</span></span>

### <span data-ttu-id="abeb6-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="abeb6-117">-AutomationAccountName</span></span>
<span data-ttu-id="abeb6-118">Annak az automatizálási fióknak a nevét adja meg, amely a parancsmag által lefordított DSC-konfigurációt tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="abeb6-118">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="abeb6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abeb6-119">-DefaultProfile</span></span>
<span data-ttu-id="abeb6-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="abeb6-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="abeb6-121">-Force</span><span class="sxs-lookup"><span data-stu-id="abeb6-121">-Force</span></span>
<span data-ttu-id="abeb6-122">ps_force</span><span class="sxs-lookup"><span data-stu-id="abeb6-122">ps_force</span></span>

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

### <span data-ttu-id="abeb6-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="abeb6-123">-InputObject</span></span>
<span data-ttu-id="abeb6-124">A csővezeték beviteli objektuma</span><span class="sxs-lookup"><span data-stu-id="abeb6-124">Input object for Piping</span></span>

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

### <span data-ttu-id="abeb6-125">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="abeb6-125">-NodeConfigurationName</span></span>
<span data-ttu-id="abeb6-126">Annak a DSC csomópont-konfigurációnak a nevét adja meg, amelyet a parancsmag telepített.</span><span class="sxs-lookup"><span data-stu-id="abeb6-126">Specifies the name of the DSC node configuration that this cmdlet deploys.</span></span>

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

### <span data-ttu-id="abeb6-127">-Csomópontnév</span><span class="sxs-lookup"><span data-stu-id="abeb6-127">-NodeName</span></span>
<span data-ttu-id="abeb6-128">Annak a csomópontnak a nevét adja meg, amelyre a csomópont-konfigurációt telepíteni kell.</span><span class="sxs-lookup"><span data-stu-id="abeb6-128">Specifies the names of the nodes to which the Node Configuration would be deployed to.</span></span>

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

### <span data-ttu-id="abeb6-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abeb6-129">-ResourceGroupName</span></span>
<span data-ttu-id="abeb6-130">Annak a csoportnak a nevét adja meg, amelyben a parancsmag egy konfigurációt összeállít.</span><span class="sxs-lookup"><span data-stu-id="abeb6-130">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="abeb6-131">– Ütemezés</span><span class="sxs-lookup"><span data-stu-id="abeb6-131">-Schedule</span></span>
<span data-ttu-id="abeb6-132">Automatizálási ütemezés objektum a központi telepítés ütemezéséhez.</span><span class="sxs-lookup"><span data-stu-id="abeb6-132">Automation Schedule object to schedule the deployment job.</span></span>

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

### <span data-ttu-id="abeb6-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="abeb6-133">-Confirm</span></span>
<span data-ttu-id="abeb6-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="abeb6-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abeb6-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abeb6-135">-WhatIf</span></span>
<span data-ttu-id="abeb6-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="abeb6-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abeb6-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="abeb6-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abeb6-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abeb6-138">CommonParameters</span></span>
<span data-ttu-id="abeb6-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="abeb6-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abeb6-140">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abeb6-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abeb6-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="abeb6-141">INPUTS</span></span>

### <span data-ttu-id="abeb6-142">System. String</span><span class="sxs-lookup"><span data-stu-id="abeb6-142">System.String</span></span>

### <span data-ttu-id="abeb6-143">Microsoft. Azure. Command. Automation. Model. NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="abeb6-143">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="abeb6-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="abeb6-144">OUTPUTS</span></span>

### <span data-ttu-id="abeb6-145">Microsoft. Azure. Command. Automation. Model. NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="abeb6-145">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="abeb6-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="abeb6-146">NOTES</span></span>

## <span data-ttu-id="abeb6-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="abeb6-147">RELATED LINKS</span></span>

[<span data-ttu-id="abeb6-148">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="abeb6-148">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="abeb6-149">Importálás – AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="abeb6-149">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="abeb6-150">Stop-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="abeb6-150">Stop-AzAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="abeb6-151">Get-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="abeb6-151">Get-AzAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="abeb6-152">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="abeb6-152">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md)

[<span data-ttu-id="abeb6-153">Új – AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="abeb6-153">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)
