---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 4810fe549f0edd109d83391e3df56916ec48b8ec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667858"
---
# <span data-ttu-id="a0a2d-101">Get-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="a0a2d-101">Get-AzAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="a0a2d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a0a2d-102">SYNOPSIS</span></span>
<span data-ttu-id="a0a2d-103">A DSC csomópontok konfigurációjának bevezetése az automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="a0a2d-103">Gets DSC Node configuration deployments in Automation.</span></span>

## <span data-ttu-id="a0a2d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a0a2d-104">SYNTAX</span></span>

### <span data-ttu-id="a0a2d-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a0a2d-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNodeConfigurationDeployment [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a0a2d-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="a0a2d-106">ByJobId</span></span>
```
Get-AzAutomationDscNodeConfigurationDeployment -JobId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0a2d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a0a2d-107">DESCRIPTION</span></span>
<span data-ttu-id="a0a2d-108">A **Get-AzAutomationDscNodeConfigurationDeployment** parancsmag az Azure-alapú csomópont-konfiguráció (DSC) csomópont-konfigurációját telepíti az Azure automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="a0a2d-108">The **Get-AzAutomationDscNodeConfigurationDeployment** cmdlet deploys an APS Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="a0a2d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a0a2d-109">EXAMPLES</span></span>

### <span data-ttu-id="a0a2d-110">Példa 1: csomópont-konfiguráció bevezetésének beszerzése</span><span class="sxs-lookup"><span data-stu-id="a0a2d-110">Example 1: Get a node configuration deployment</span></span>
```
PS C:\> $deployment = Get-AzAutomationDscNodeConfigurationDeployment `
                         -JobId 35b14eb4-52b7-4a1d-ad62-8e9f84adc657 `
                         -AutomationAccountName "Contoso01"  `
                         -ResourceGroupName "ResourceGroup01" `
            
ResourceGroupName     : ResourceGroup01
AutomationAccountName : Contoso01
JobId                 : 35b14eb4-52b7-4a1d-ad62-8e9f84adc657
Job                   : Microsoft.Azure.Commands.Automation.Model.Job
JobStatus             : Running
NodeStatus            : {System.Collections.Generic.Dictionary`2[System.String,System.String], System.Collections.Generic.Dictionary`2[System.String,System.String]}
NodeConfigurationName : Config01.Node1
JobSchedule           :
JobScheduleId         : 00000000-0000-0000-0000-000000000000

PS C:\> $deployment | Select -expand nodeStatus

Key        Value
---        -----
WebServer  Pending
WebServer2 Pending
WebServer3 Compliant
```

<span data-ttu-id="a0a2d-111">A fenti parancs az "Config01. Node1" nevű DSC csomópont-konfigurációt telepíti a csomópontok nevének adott kétdimenziós sorába.</span><span class="sxs-lookup"><span data-stu-id="a0a2d-111">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="a0a2d-112">A telepítés szakaszos módon történik.</span><span class="sxs-lookup"><span data-stu-id="a0a2d-112">The deployment happens in a staged manner.</span></span>

## <span data-ttu-id="a0a2d-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a0a2d-113">PARAMETERS</span></span>

### <span data-ttu-id="a0a2d-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a0a2d-114">-AutomationAccountName</span></span>
<span data-ttu-id="a0a2d-115">Annak az automatizálási fióknak a nevét adja meg, amely a parancsmag által lefordított DSC-konfigurációt tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="a0a2d-115">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="a0a2d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0a2d-116">-DefaultProfile</span></span>
<span data-ttu-id="a0a2d-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a0a2d-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a0a2d-118">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="a0a2d-118">-EndTime</span></span>
<span data-ttu-id="a0a2d-119">Befejezés időpontjának szűrője</span><span class="sxs-lookup"><span data-stu-id="a0a2d-119">End time filter.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0a2d-120">-JobId</span><span class="sxs-lookup"><span data-stu-id="a0a2d-120">-JobId</span></span>
<span data-ttu-id="a0a2d-121">A meglévő központi telepítés feladatának munkaazonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a0a2d-121">Specifies the Job id of an existing deployment job.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ByJobId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0a2d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0a2d-122">-ResourceGroupName</span></span>
<span data-ttu-id="a0a2d-123">Annak a csoportnak a nevét adja meg, amelyben a parancsmag egy konfigurációt összeállít.</span><span class="sxs-lookup"><span data-stu-id="a0a2d-123">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="a0a2d-124">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="a0a2d-124">-StartTime</span></span>
<span data-ttu-id="a0a2d-125">Kezdési idő szűrője</span><span class="sxs-lookup"><span data-stu-id="a0a2d-125">Start time filter.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0a2d-126">-Állapot</span><span class="sxs-lookup"><span data-stu-id="a0a2d-126">-Status</span></span>
<span data-ttu-id="a0a2d-127">A projekt szűrő állapota</span><span class="sxs-lookup"><span data-stu-id="a0a2d-127">Status of the Job filter.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll
Aliases:
Accepted values: Completed, Failed, Queued, Starting, Resuming, Running, Stopped, Stopping, Suspended, Suspending, Activating

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0a2d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0a2d-128">CommonParameters</span></span>
<span data-ttu-id="a0a2d-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a0a2d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0a2d-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0a2d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0a2d-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0a2d-131">INPUTS</span></span>

### <span data-ttu-id="a0a2d-132">System. GUID</span><span class="sxs-lookup"><span data-stu-id="a0a2d-132">System.Guid</span></span>

### <span data-ttu-id="a0a2d-133">System. String</span><span class="sxs-lookup"><span data-stu-id="a0a2d-133">System.String</span></span>

## <span data-ttu-id="a0a2d-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0a2d-134">OUTPUTS</span></span>

### <span data-ttu-id="a0a2d-135">Microsoft. Azure. Command. Automation. Model. NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="a0a2d-135">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="a0a2d-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a0a2d-136">NOTES</span></span>

## <span data-ttu-id="a0a2d-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a0a2d-137">RELATED LINKS</span></span>

[<span data-ttu-id="a0a2d-138">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="a0a2d-138">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="a0a2d-139">Importálás – AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="a0a2d-139">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="a0a2d-140">Start-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="a0a2d-140">Start-AzAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="a0a2d-141">Stop-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="a0a2d-141">Stop-AzAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="a0a2d-142">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="a0a2d-142">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md)
