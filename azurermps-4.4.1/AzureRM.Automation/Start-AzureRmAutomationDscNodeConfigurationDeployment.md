---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRmAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRmAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: f822f6060827718945f12f998662caeee3b349eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500951"
---
# <span data-ttu-id="24a6a-101">Start-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="24a6a-101">Start-AzureRmAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="24a6a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="24a6a-102">SYNOPSIS</span></span>
<span data-ttu-id="24a6a-103">A DSC csomópontok konfigurációját telepíti automatizálással.</span><span class="sxs-lookup"><span data-stu-id="24a6a-103">Deploys a DSC Node configuration in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24a6a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="24a6a-104">SYNTAX</span></span>

### <span data-ttu-id="24a6a-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="24a6a-105">ByAll (Default)</span></span>
```
Start-AzureRmAutomationDscNodeConfigurationDeployment [-NodeConfigurationName] <String>
 [-NodeName] <String[][]> [-Schedule <Schedule>] [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="24a6a-106">ByByInputObject</span><span class="sxs-lookup"><span data-stu-id="24a6a-106">ByByInputObject</span></span>
```
Start-AzureRmAutomationDscNodeConfigurationDeployment [-NodeConfigurationName] <String>
 [-NodeName] <String[][]> -InputObject <NodeConfigurationDeployment> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="24a6a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="24a6a-107">DESCRIPTION</span></span>
<span data-ttu-id="24a6a-108">A **Start-AzureRmAutomationDscNodeConfigurationDeployment** parancsmag a kívánt állapot-konfiguráció (DSC) csomópont-konfigurációt telepíti az Azure automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="24a6a-108">The **Start-AzureRmAutomationDscNodeConfigurationDeployment** cmdlet deployes a Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="24a6a-109">Példák</span><span class="sxs-lookup"><span data-stu-id="24a6a-109">EXAMPLES</span></span>

### <span data-ttu-id="24a6a-110">1. példa: Azure DSC csomópont-konfiguráció telepítése automatizálással</span><span class="sxs-lookup"><span data-stu-id="24a6a-110">Example 1: Deploy an Azure DSC node configuration in Automation</span></span>
```
PS C:\> $pilot = @("WebServerPilot1", "WebServerPilot2")
PS C:\> $prod = @("WebServerProd1", "WebServerProd2")
PS C:\> $nodes = @($pilot, $prod)
PS C:\> Start-AzureRmAutomationDscNodeConfigurationDeployment `
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

<span data-ttu-id="24a6a-111">A fenti parancs az "Config01. Node1" nevű DSC csomópont-konfigurációt telepíti a csomópontok nevének adott kétdimenziós sorába.</span><span class="sxs-lookup"><span data-stu-id="24a6a-111">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="24a6a-112">A telepítés szakaszos módon történik.</span><span class="sxs-lookup"><span data-stu-id="24a6a-112">The deployment happens in a staged manner.</span></span>

### <span data-ttu-id="24a6a-113">2. példa: az Azure DSC csomópont-konfiguráció bevezetésének ütemezése automatizálással</span><span class="sxs-lookup"><span data-stu-id="24a6a-113">Example 2: Schedule an Azure DSC node configuration deployment in Automation</span></span>
```
PS C:\> $sched = New-AzureRmAutomationSchedule -AutomationAccountName "Contoso01" `
            -ResourceGroupName "ResourceGroup01" `
            -Name "TestSchedule" `
            -StartTime "23:00" `
            -OneTime
PS C:\> $pilot = @("WebServerPilot1", "WebServerPilot2")
PS C:\> $prod = @("WebServerProd1", "WebServerProd2")
PS C:\> $nodes = @($pilot, $prod)
PS C:\> Start-AzureRmAutomationDscNodeConfigurationDeployment `
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

<span data-ttu-id="24a6a-114">A fenti parancs az "Config01. Node1" nevű DSC-csomópont konfigurációját ütemezi a csomópontok adott kétdimenziós sorába.</span><span class="sxs-lookup"><span data-stu-id="24a6a-114">The above command schedules a deployment of a DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="24a6a-115">A telepítés szakaszos módon történik, és a program az ütemterv alapján hajtja végre.</span><span class="sxs-lookup"><span data-stu-id="24a6a-115">The deployment happens in a staged manner and will be executed based on the schedule.</span></span>

## <span data-ttu-id="24a6a-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="24a6a-116">PARAMETERS</span></span>

### <span data-ttu-id="24a6a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24a6a-117">-ResourceGroupName</span></span>
<span data-ttu-id="24a6a-118">Annak a csoportnak a nevét adja meg, amelyben a parancsmag egy konfigurációt összeállít.</span><span class="sxs-lookup"><span data-stu-id="24a6a-118">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="24a6a-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="24a6a-119">-AutomationAccountName</span></span>
<span data-ttu-id="24a6a-120">Annak az automatizálási fióknak a nevét adja meg, amely a parancsmag által lefordított DSC-konfigurációt tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="24a6a-120">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="24a6a-121">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="24a6a-121">-NodeConfigurationName</span></span>
<span data-ttu-id="24a6a-122">Annak a DSC csomópont-konfigurációnak a nevét adja meg, amelyet a parancsmag telepített.</span><span class="sxs-lookup"><span data-stu-id="24a6a-122">Specifies the name of the DSC node configuration that this cmdlet deploys.</span></span>

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
Parameter Sets: ByByInputObject
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24a6a-123">-Csomópontnév</span><span class="sxs-lookup"><span data-stu-id="24a6a-123">-NodeName</span></span>
<span data-ttu-id="24a6a-124">Annak a csomópontnak a nevét adja meg, amelyre a csomópont-konfigurációt telepíteni kell.</span><span class="sxs-lookup"><span data-stu-id="24a6a-124">Specifies the names of the nodes to which the Node Configuration would be deployed to.</span></span>

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

### <span data-ttu-id="24a6a-125">– Ütemezés</span><span class="sxs-lookup"><span data-stu-id="24a6a-125">-Schedule</span></span>
<span data-ttu-id="24a6a-126">Automatizálási ütemezés objektum a központi telepítés ütemezéséhez.</span><span class="sxs-lookup"><span data-stu-id="24a6a-126">Automation Schedule object to schedule the deployment job.</span></span>

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

### <span data-ttu-id="24a6a-127">-Force</span><span class="sxs-lookup"><span data-stu-id="24a6a-127">-Force</span></span>
<span data-ttu-id="24a6a-128">ps_force</span><span class="sxs-lookup"><span data-stu-id="24a6a-128">ps_force</span></span>

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

### <span data-ttu-id="24a6a-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="24a6a-129">-Confirm</span></span>
<span data-ttu-id="24a6a-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="24a6a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24a6a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24a6a-131">-WhatIf</span></span>
<span data-ttu-id="24a6a-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="24a6a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24a6a-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="24a6a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24a6a-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24a6a-134">-DefaultProfile</span></span>
<span data-ttu-id="24a6a-135">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="24a6a-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24a6a-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="24a6a-136">-InputObject</span></span>
<span data-ttu-id="24a6a-137">A csővezeték beviteli objektuma.</span><span class="sxs-lookup"><span data-stu-id="24a6a-137">Input object for Piping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment
Parameter Sets: ByByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="24a6a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24a6a-138">CommonParameters</span></span>
<span data-ttu-id="24a6a-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="24a6a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24a6a-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24a6a-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24a6a-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="24a6a-141">INPUTS</span></span>

## <span data-ttu-id="24a6a-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="24a6a-142">OUTPUTS</span></span>

### <span data-ttu-id="24a6a-143">Microsoft. Azure. Command. Automation. Model. NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="24a6a-143">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="24a6a-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="24a6a-144">NOTES</span></span>

## <span data-ttu-id="24a6a-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="24a6a-145">RELATED LINKS</span></span>

[<span data-ttu-id="24a6a-146">Start-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="24a6a-146">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)

[<span data-ttu-id="24a6a-147">Importálás – AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="24a6a-147">Import-AzureRmAutomationDscNodeConfiguration</span></span>](./Import-AzureRmAutomationDscNodeConfiguration.md)

[<span data-ttu-id="24a6a-148">Stop-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="24a6a-148">Stop-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="24a6a-149">Get-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="24a6a-149">Get-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="24a6a-150">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="24a6a-150">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule.md)

[<span data-ttu-id="24a6a-151">Új – AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="24a6a-151">New-AzureRmAutomationSchedule</span></span>](./New-AzureRmAutomationSchedule.md)
