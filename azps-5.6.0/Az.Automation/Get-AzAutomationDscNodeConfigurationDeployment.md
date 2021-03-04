---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: f5cbb59ffbd5b79087e9f338788dde9d1176f4d8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941290"
---
# <span data-ttu-id="d9f87-101">Get-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="d9f87-101">Get-AzAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="d9f87-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9f87-102">SYNOPSIS</span></span>
<span data-ttu-id="d9f87-103">DSC-csomópont-konfigurációs telepítéseket kap az automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="d9f87-103">Gets DSC Node configuration deployments in Automation.</span></span>

## <span data-ttu-id="d9f87-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d9f87-104">SYNTAX</span></span>

### <span data-ttu-id="d9f87-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d9f87-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNodeConfigurationDeployment [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9f87-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="d9f87-106">ByJobId</span></span>
```
Get-AzAutomationDscNodeConfigurationDeployment -JobId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9f87-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d9f87-107">DESCRIPTION</span></span>
<span data-ttu-id="d9f87-108">A **Get-AzAutomationDscNodeConfigurationDeployment parancsmag** egy APS–kívánt államkonfigurációt (DSC) telepít az Azure Automationben.</span><span class="sxs-lookup"><span data-stu-id="d9f87-108">The **Get-AzAutomationDscNodeConfigurationDeployment** cmdlet deploys an APS Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="d9f87-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d9f87-109">EXAMPLES</span></span>

### <span data-ttu-id="d9f87-110">1. példa: Csomópont-konfiguráció beállítása</span><span class="sxs-lookup"><span data-stu-id="d9f87-110">Example 1: Get a node configuration deployment</span></span>
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

<span data-ttu-id="d9f87-111">A fenti parancs a "Config01.Node1" nevű DSC-csomópont-konfigurációt telepíti a Csomópontnevek adott kétdimenziós tömbjéhez.</span><span class="sxs-lookup"><span data-stu-id="d9f87-111">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="d9f87-112">A telepítés szakaszos módon történik.</span><span class="sxs-lookup"><span data-stu-id="d9f87-112">The deployment happens in a staged manner.</span></span>

## <span data-ttu-id="d9f87-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d9f87-113">PARAMETERS</span></span>

### <span data-ttu-id="d9f87-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d9f87-114">-AutomationAccountName</span></span>
<span data-ttu-id="d9f87-115">Annak az automatizálási fióknak a nevét adja meg, amely a parancsmag által lefordított DSC-konfigurációt tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="d9f87-115">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="d9f87-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9f87-116">-DefaultProfile</span></span>
<span data-ttu-id="d9f87-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d9f87-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d9f87-118">-EndTime</span><span class="sxs-lookup"><span data-stu-id="d9f87-118">-EndTime</span></span>
<span data-ttu-id="d9f87-119">Záró időpont szűrője.</span><span class="sxs-lookup"><span data-stu-id="d9f87-119">End time filter.</span></span>

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

### <span data-ttu-id="d9f87-120">-JobId</span><span class="sxs-lookup"><span data-stu-id="d9f87-120">-JobId</span></span>
<span data-ttu-id="d9f87-121">Egy meglévő üzembe helyezési feladat feladatazonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d9f87-121">Specifies the Job id of an existing deployment job.</span></span>

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

### <span data-ttu-id="d9f87-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9f87-122">-ResourceGroupName</span></span>
<span data-ttu-id="d9f87-123">Annak az erőforráscsoportnak a nevét adja meg, amelyben ez a parancsmag konfigurációt fordít.</span><span class="sxs-lookup"><span data-stu-id="d9f87-123">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="d9f87-124">-StartTime</span><span class="sxs-lookup"><span data-stu-id="d9f87-124">-StartTime</span></span>
<span data-ttu-id="d9f87-125">Kezdési idő szűrője</span><span class="sxs-lookup"><span data-stu-id="d9f87-125">Start time filter.</span></span>

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

### <span data-ttu-id="d9f87-126">-Állapot</span><span class="sxs-lookup"><span data-stu-id="d9f87-126">-Status</span></span>
<span data-ttu-id="d9f87-127">A Feladat szűrő állapota.</span><span class="sxs-lookup"><span data-stu-id="d9f87-127">Status of the Job filter.</span></span>

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

### <span data-ttu-id="d9f87-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9f87-128">CommonParameters</span></span>
<span data-ttu-id="d9f87-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9f87-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9f87-130">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9f87-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9f87-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d9f87-131">INPUTS</span></span>

### <span data-ttu-id="d9f87-132">System.Guid</span><span class="sxs-lookup"><span data-stu-id="d9f87-132">System.Guid</span></span>

### <span data-ttu-id="d9f87-133">System.String</span><span class="sxs-lookup"><span data-stu-id="d9f87-133">System.String</span></span>

## <span data-ttu-id="d9f87-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d9f87-134">OUTPUTS</span></span>

### <span data-ttu-id="d9f87-135">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="d9f87-135">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="d9f87-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d9f87-136">NOTES</span></span>

## <span data-ttu-id="d9f87-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d9f87-137">RELATED LINKS</span></span>

[<span data-ttu-id="d9f87-138">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="d9f87-138">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="d9f87-139">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="d9f87-139">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="d9f87-140">Start-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="d9f87-140">Start-AzAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="d9f87-141">Stop-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="d9f87-141">Stop-AzAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="d9f87-142">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="d9f87-142">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md)
