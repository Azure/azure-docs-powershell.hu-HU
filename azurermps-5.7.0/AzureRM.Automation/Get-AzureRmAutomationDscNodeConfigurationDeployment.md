---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: d5732058c9bfe077a7241257b4b60865547787e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680825"
---
# <span data-ttu-id="042f6-101">Get-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="042f6-101">Get-AzureRmAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="042f6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="042f6-102">SYNOPSIS</span></span>
<span data-ttu-id="042f6-103">A DSC csomópontok konfigurációjának bevezetése az automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="042f6-103">Gets DSC Node configuration deployments in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="042f6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="042f6-104">SYNTAX</span></span>

### <span data-ttu-id="042f6-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="042f6-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscNodeConfigurationDeployment [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="042f6-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="042f6-106">ByJobId</span></span>
```
Get-AzureRmAutomationDscNodeConfigurationDeployment -JobId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="042f6-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="042f6-107">DESCRIPTION</span></span>
<span data-ttu-id="042f6-108">A **Get-AzureRmAutomationDscNodeConfigurationDeployment** parancsmag az Azure-alapú csomópont-konfiguráció (DSC) csomópont-konfigurációját telepíti az Azure automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="042f6-108">The **Get-AzureRmAutomationDscNodeConfigurationDeployment** cmdlet deployes an APS Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="042f6-109">Példák</span><span class="sxs-lookup"><span data-stu-id="042f6-109">EXAMPLES</span></span>

### <span data-ttu-id="042f6-110">Példa 1: csomópont-konfiguráció bevezetésének beszerzése</span><span class="sxs-lookup"><span data-stu-id="042f6-110">Example 1: Get a node configuration deployment</span></span>
```
PS C:\> $deployment = Get-AzureRmAutomationDscNodeConfigurationDeployment `
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

<span data-ttu-id="042f6-111">A fenti parancs az "Config01. Node1" nevű DSC csomópont-konfigurációt telepíti a csomópontok nevének adott kétdimenziós sorába.</span><span class="sxs-lookup"><span data-stu-id="042f6-111">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="042f6-112">A telepítés szakaszos módon történik.</span><span class="sxs-lookup"><span data-stu-id="042f6-112">The deployment happens in a staged manner.</span></span>

## <span data-ttu-id="042f6-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="042f6-113">PARAMETERS</span></span>

### <span data-ttu-id="042f6-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="042f6-114">-AutomationAccountName</span></span>
<span data-ttu-id="042f6-115">Annak az automatizálási fióknak a nevét adja meg, amely a parancsmag által lefordított DSC-konfigurációt tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="042f6-115">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="042f6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="042f6-116">-DefaultProfile</span></span>
<span data-ttu-id="042f6-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="042f6-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="042f6-118">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="042f6-118">-EndTime</span></span>
<span data-ttu-id="042f6-119">Befejezés időpontjának szűrője</span><span class="sxs-lookup"><span data-stu-id="042f6-119">End time filter.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ByAll
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="042f6-120">-JobId</span><span class="sxs-lookup"><span data-stu-id="042f6-120">-JobId</span></span>
<span data-ttu-id="042f6-121">A meglévő központi telepítés feladatának munkaazonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="042f6-121">Specifies the Job id of an existing deployment job.</span></span>

```yaml
Type: Guid
Parameter Sets: ByJobId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="042f6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="042f6-122">-ResourceGroupName</span></span>
<span data-ttu-id="042f6-123">Annak a csoportnak a nevét adja meg, amelyben a parancsmag egy konfigurációt összeállít.</span><span class="sxs-lookup"><span data-stu-id="042f6-123">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="042f6-124">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="042f6-124">-StartTime</span></span>
<span data-ttu-id="042f6-125">Kezdési idő szűrője</span><span class="sxs-lookup"><span data-stu-id="042f6-125">Start time filter.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ByAll
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="042f6-126">-Állapot</span><span class="sxs-lookup"><span data-stu-id="042f6-126">-Status</span></span>
<span data-ttu-id="042f6-127">A projekt szűrő állapota</span><span class="sxs-lookup"><span data-stu-id="042f6-127">Status of the Job filter.</span></span>

```yaml
Type: String
Parameter Sets: ByAll
Aliases: 
Accepted values: Completed, Failed, Queued, Starting, Resuming, Running, Stopped, Stopping, Suspended, Suspending, Activating

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="042f6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="042f6-128">CommonParameters</span></span>
<span data-ttu-id="042f6-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="042f6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="042f6-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="042f6-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="042f6-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="042f6-131">INPUTS</span></span>

### <span data-ttu-id="042f6-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="042f6-132">None</span></span>
<span data-ttu-id="042f6-133">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="042f6-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="042f6-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="042f6-134">OUTPUTS</span></span>

### <span data-ttu-id="042f6-135">Microsoft. Azure. Command. Automation. Model. NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="042f6-135">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="042f6-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="042f6-136">NOTES</span></span>

## <span data-ttu-id="042f6-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="042f6-137">RELATED LINKS</span></span>

[<span data-ttu-id="042f6-138">Start-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="042f6-138">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)

[<span data-ttu-id="042f6-139">Importálás – AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="042f6-139">Import-AzureRmAutomationDscNodeConfiguration</span></span>](./Import-AzureRmAutomationDscNodeConfiguration.md)

[<span data-ttu-id="042f6-140">Start-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="042f6-140">Start-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="042f6-141">Stop-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="042f6-141">Stop-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="042f6-142">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="042f6-142">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule.md)
