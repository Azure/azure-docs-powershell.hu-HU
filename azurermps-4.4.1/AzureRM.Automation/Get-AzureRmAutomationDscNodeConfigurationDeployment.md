---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 889318c911ae6f34b3655583ea2e9693da3bf80f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498012"
---
# <span data-ttu-id="41b53-101">Get-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="41b53-101">Get-AzureRmAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="41b53-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="41b53-102">SYNOPSIS</span></span>
<span data-ttu-id="41b53-103">A DSC csomópontok konfigurációjának bevezetése az automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="41b53-103">Gets DSC Node configuration deployments in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41b53-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="41b53-104">SYNTAX</span></span>

### <span data-ttu-id="41b53-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="41b53-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscNodeConfigurationDeployment [[-Status] <String>] [[-StartTime] <DateTimeOffset>]
 [[-EndTime] <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="41b53-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="41b53-106">ByJobId</span></span>
```
Get-AzureRmAutomationDscNodeConfigurationDeployment -JobId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41b53-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="41b53-107">DESCRIPTION</span></span>
<span data-ttu-id="41b53-108">A **Get-AzureRmAutomationDscNodeConfigurationDeployment** parancsmag az Azure-alapú csomópont-konfiguráció (DSC) csomópont-konfigurációját telepíti az Azure automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="41b53-108">The **Get-AzureRmAutomationDscNodeConfigurationDeployment** cmdlet deployes an APS Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="41b53-109">Példák</span><span class="sxs-lookup"><span data-stu-id="41b53-109">EXAMPLES</span></span>

### <span data-ttu-id="41b53-110">Példa 1: csomópont-konfiguráció bevezetésének beszerzése</span><span class="sxs-lookup"><span data-stu-id="41b53-110">Example 1: Get a node configuration deployment</span></span>
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

<span data-ttu-id="41b53-111">A fenti parancs az "Config01. Node1" nevű DSC csomópont-konfigurációt telepíti a csomópontok nevének adott kétdimenziós sorába.</span><span class="sxs-lookup"><span data-stu-id="41b53-111">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="41b53-112">A telepítés szakaszos módon történik.</span><span class="sxs-lookup"><span data-stu-id="41b53-112">The deployment happens in a staged manner.</span></span>

## <span data-ttu-id="41b53-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="41b53-113">PARAMETERS</span></span>

### <span data-ttu-id="41b53-114">-JobId</span><span class="sxs-lookup"><span data-stu-id="41b53-114">-JobId</span></span>
<span data-ttu-id="41b53-115">A meglévő központi telepítés feladatának munkaazonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="41b53-115">Specifies the Job id of an existing deployment job.</span></span>

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

### <span data-ttu-id="41b53-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41b53-116">-ResourceGroupName</span></span>
<span data-ttu-id="41b53-117">Annak a csoportnak a nevét adja meg, amelyben a parancsmag egy konfigurációt összeállít.</span><span class="sxs-lookup"><span data-stu-id="41b53-117">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="41b53-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="41b53-118">-AutomationAccountName</span></span>
<span data-ttu-id="41b53-119">Annak az automatizálási fióknak a nevét adja meg, amely a parancsmag által lefordított DSC-konfigurációt tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="41b53-119">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="41b53-120">-Állapot</span><span class="sxs-lookup"><span data-stu-id="41b53-120">-Status</span></span>
<span data-ttu-id="41b53-121">A projekt szűrő állapota</span><span class="sxs-lookup"><span data-stu-id="41b53-121">Status of the Job filter.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41b53-122">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="41b53-122">-StartTime</span></span>
<span data-ttu-id="41b53-123">Kezdési idő szűrője</span><span class="sxs-lookup"><span data-stu-id="41b53-123">Start time filter.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41b53-124">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="41b53-124">-EndTime</span></span>
<span data-ttu-id="41b53-125">Befejezés időpontjának szűrője</span><span class="sxs-lookup"><span data-stu-id="41b53-125">End time filter.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41b53-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41b53-126">-DefaultProfile</span></span>
<span data-ttu-id="41b53-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="41b53-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41b53-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41b53-128">CommonParameters</span></span>
<span data-ttu-id="41b53-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="41b53-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41b53-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41b53-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41b53-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="41b53-131">INPUTS</span></span>

## <span data-ttu-id="41b53-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="41b53-132">OUTPUTS</span></span>

### <span data-ttu-id="41b53-133">Microsoft. Azure. Command. Automation. Model. NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="41b53-133">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="41b53-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="41b53-134">NOTES</span></span>

## <span data-ttu-id="41b53-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="41b53-135">RELATED LINKS</span></span>

[<span data-ttu-id="41b53-136">Start-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="41b53-136">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)

[<span data-ttu-id="41b53-137">Importálás – AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="41b53-137">Import-AzureRmAutomationDscNodeConfiguration</span></span>](./Import-AzureRmAutomationDscNodeConfiguration.md)

[<span data-ttu-id="41b53-138">Start-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="41b53-138">Start-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="41b53-139">Stop-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="41b53-139">Stop-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="41b53-140">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="41b53-140">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule.md)
