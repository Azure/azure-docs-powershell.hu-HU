---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 449d539b767883bb075bcf333695b3285e047a9c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98342714"
---
# <span data-ttu-id="c8eaa-101">Get-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="c8eaa-101">Get-AzAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="c8eaa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8eaa-102">SYNOPSIS</span></span>
<span data-ttu-id="c8eaa-103">DSC-csomópont-konfigurációs telepítéseket kap az automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="c8eaa-103">Gets DSC Node configuration deployments in Automation.</span></span>

## <span data-ttu-id="c8eaa-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c8eaa-104">SYNTAX</span></span>

### <span data-ttu-id="c8eaa-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c8eaa-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNodeConfigurationDeployment [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8eaa-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="c8eaa-106">ByJobId</span></span>
```
Get-AzAutomationDscNodeConfigurationDeployment -JobId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8eaa-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c8eaa-107">DESCRIPTION</span></span>
<span data-ttu-id="c8eaa-108">A **Get-AzAutomationDscNodeConfigurationDeployment parancsmag** egy APS–kívánt államkonfigurációt (DSC) telepít az Azure Automationben.</span><span class="sxs-lookup"><span data-stu-id="c8eaa-108">The **Get-AzAutomationDscNodeConfigurationDeployment** cmdlet deploys an APS Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="c8eaa-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c8eaa-109">EXAMPLES</span></span>

### <span data-ttu-id="c8eaa-110">1. példa: Csomópont-konfiguráció beállítása</span><span class="sxs-lookup"><span data-stu-id="c8eaa-110">Example 1: Get a node configuration deployment</span></span>
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

<span data-ttu-id="c8eaa-111">A fenti parancs a "Config01.Node1" nevű DSC-csomópont-konfigurációt telepíti a Csomópontnevek adott kétdimenziós tömbjéhez.</span><span class="sxs-lookup"><span data-stu-id="c8eaa-111">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="c8eaa-112">A telepítés szakaszos módon történik.</span><span class="sxs-lookup"><span data-stu-id="c8eaa-112">The deployment happens in a staged manner.</span></span>

## <span data-ttu-id="c8eaa-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c8eaa-113">PARAMETERS</span></span>

### <span data-ttu-id="c8eaa-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c8eaa-114">-AutomationAccountName</span></span>
<span data-ttu-id="c8eaa-115">Annak az automatizálási fióknak a nevét adja meg, amely a parancsmag által lefordított DSC-konfigurációt tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="c8eaa-115">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="c8eaa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8eaa-116">-DefaultProfile</span></span>
<span data-ttu-id="c8eaa-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c8eaa-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c8eaa-118">-EndTime</span><span class="sxs-lookup"><span data-stu-id="c8eaa-118">-EndTime</span></span>
<span data-ttu-id="c8eaa-119">Záró időpont szűrője.</span><span class="sxs-lookup"><span data-stu-id="c8eaa-119">End time filter.</span></span>

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

### <span data-ttu-id="c8eaa-120">-JobId</span><span class="sxs-lookup"><span data-stu-id="c8eaa-120">-JobId</span></span>
<span data-ttu-id="c8eaa-121">Egy meglévő üzembe helyezési feladat feladatazonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c8eaa-121">Specifies the Job id of an existing deployment job.</span></span>

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

### <span data-ttu-id="c8eaa-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8eaa-122">-ResourceGroupName</span></span>
<span data-ttu-id="c8eaa-123">Annak az erőforráscsoportnak a nevét adja meg, amelyben ez a parancsmag konfigurációt fordít.</span><span class="sxs-lookup"><span data-stu-id="c8eaa-123">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="c8eaa-124">-StartTime</span><span class="sxs-lookup"><span data-stu-id="c8eaa-124">-StartTime</span></span>
<span data-ttu-id="c8eaa-125">Kezdési idő szűrője</span><span class="sxs-lookup"><span data-stu-id="c8eaa-125">Start time filter.</span></span>

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

### <span data-ttu-id="c8eaa-126">-Állapot</span><span class="sxs-lookup"><span data-stu-id="c8eaa-126">-Status</span></span>
<span data-ttu-id="c8eaa-127">A Feladat szűrő állapota.</span><span class="sxs-lookup"><span data-stu-id="c8eaa-127">Status of the Job filter.</span></span>

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

### <span data-ttu-id="c8eaa-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8eaa-128">CommonParameters</span></span>
<span data-ttu-id="c8eaa-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8eaa-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8eaa-130">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8eaa-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8eaa-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c8eaa-131">INPUTS</span></span>

### <span data-ttu-id="c8eaa-132">System.Guid</span><span class="sxs-lookup"><span data-stu-id="c8eaa-132">System.Guid</span></span>

### <span data-ttu-id="c8eaa-133">System.String</span><span class="sxs-lookup"><span data-stu-id="c8eaa-133">System.String</span></span>

## <span data-ttu-id="c8eaa-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c8eaa-134">OUTPUTS</span></span>

### <span data-ttu-id="c8eaa-135">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="c8eaa-135">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="c8eaa-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c8eaa-136">NOTES</span></span>

## <span data-ttu-id="c8eaa-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c8eaa-137">RELATED LINKS</span></span>

[<span data-ttu-id="c8eaa-138">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="c8eaa-138">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="c8eaa-139">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="c8eaa-139">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="c8eaa-140">Start-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="c8eaa-140">Start-AzAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="c8eaa-141">Stop-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="c8eaa-141">Stop-AzAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="c8eaa-142">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="c8eaa-142">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md)
