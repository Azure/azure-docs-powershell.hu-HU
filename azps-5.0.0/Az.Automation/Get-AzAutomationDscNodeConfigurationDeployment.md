---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 449d539b767883bb075bcf333695b3285e047a9c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186123"
---
# <span data-ttu-id="5993f-101">Get-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="5993f-101">Get-AzAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="5993f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5993f-102">SYNOPSIS</span></span>
<span data-ttu-id="5993f-103">A DSC csomópontok konfigurációjának bevezetése az automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="5993f-103">Gets DSC Node configuration deployments in Automation.</span></span>

## <span data-ttu-id="5993f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5993f-104">SYNTAX</span></span>

### <span data-ttu-id="5993f-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5993f-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNodeConfigurationDeployment [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5993f-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="5993f-106">ByJobId</span></span>
```
Get-AzAutomationDscNodeConfigurationDeployment -JobId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5993f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="5993f-107">DESCRIPTION</span></span>
<span data-ttu-id="5993f-108">A **Get-AzAutomationDscNodeConfigurationDeployment** parancsmag az Azure-alapú csomópont-konfiguráció (DSC) csomópont-konfigurációját telepíti az Azure automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="5993f-108">The **Get-AzAutomationDscNodeConfigurationDeployment** cmdlet deploys an APS Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="5993f-109">Példák</span><span class="sxs-lookup"><span data-stu-id="5993f-109">EXAMPLES</span></span>

### <span data-ttu-id="5993f-110">Példa 1: csomópont-konfiguráció bevezetésének beszerzése</span><span class="sxs-lookup"><span data-stu-id="5993f-110">Example 1: Get a node configuration deployment</span></span>
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

<span data-ttu-id="5993f-111">A fenti parancs az "Config01. Node1" nevű DSC csomópont-konfigurációt telepíti a csomópontok nevének adott kétdimenziós sorába.</span><span class="sxs-lookup"><span data-stu-id="5993f-111">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="5993f-112">A telepítés szakaszos módon történik.</span><span class="sxs-lookup"><span data-stu-id="5993f-112">The deployment happens in a staged manner.</span></span>

## <span data-ttu-id="5993f-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5993f-113">PARAMETERS</span></span>

### <span data-ttu-id="5993f-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5993f-114">-AutomationAccountName</span></span>
<span data-ttu-id="5993f-115">Annak az automatizálási fióknak a nevét adja meg, amely a parancsmag által lefordított DSC-konfigurációt tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="5993f-115">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="5993f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5993f-116">-DefaultProfile</span></span>
<span data-ttu-id="5993f-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5993f-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5993f-118">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="5993f-118">-EndTime</span></span>
<span data-ttu-id="5993f-119">Befejezés időpontjának szűrője</span><span class="sxs-lookup"><span data-stu-id="5993f-119">End time filter.</span></span>

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

### <span data-ttu-id="5993f-120">-JobId</span><span class="sxs-lookup"><span data-stu-id="5993f-120">-JobId</span></span>
<span data-ttu-id="5993f-121">A meglévő központi telepítés feladatának munkaazonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5993f-121">Specifies the Job id of an existing deployment job.</span></span>

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

### <span data-ttu-id="5993f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5993f-122">-ResourceGroupName</span></span>
<span data-ttu-id="5993f-123">Annak a csoportnak a nevét adja meg, amelyben a parancsmag egy konfigurációt összeállít.</span><span class="sxs-lookup"><span data-stu-id="5993f-123">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="5993f-124">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="5993f-124">-StartTime</span></span>
<span data-ttu-id="5993f-125">Kezdési idő szűrője</span><span class="sxs-lookup"><span data-stu-id="5993f-125">Start time filter.</span></span>

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

### <span data-ttu-id="5993f-126">-Állapot</span><span class="sxs-lookup"><span data-stu-id="5993f-126">-Status</span></span>
<span data-ttu-id="5993f-127">A projekt szűrő állapota</span><span class="sxs-lookup"><span data-stu-id="5993f-127">Status of the Job filter.</span></span>

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

### <span data-ttu-id="5993f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5993f-128">CommonParameters</span></span>
<span data-ttu-id="5993f-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5993f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5993f-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5993f-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5993f-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5993f-131">INPUTS</span></span>

### <span data-ttu-id="5993f-132">System. GUID</span><span class="sxs-lookup"><span data-stu-id="5993f-132">System.Guid</span></span>

### <span data-ttu-id="5993f-133">System. String</span><span class="sxs-lookup"><span data-stu-id="5993f-133">System.String</span></span>

## <span data-ttu-id="5993f-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5993f-134">OUTPUTS</span></span>

### <span data-ttu-id="5993f-135">Microsoft. Azure. Command. Automation. Model. NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="5993f-135">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="5993f-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5993f-136">NOTES</span></span>

## <span data-ttu-id="5993f-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5993f-137">RELATED LINKS</span></span>

[<span data-ttu-id="5993f-138">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="5993f-138">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="5993f-139">Importálás – AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="5993f-139">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="5993f-140">Start-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="5993f-140">Start-AzAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="5993f-141">Stop-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="5993f-141">Stop-AzAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="5993f-142">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="5993f-142">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md)
