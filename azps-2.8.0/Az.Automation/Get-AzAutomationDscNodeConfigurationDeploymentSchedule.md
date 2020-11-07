---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscnodeconfigurationdeploymentschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md
ms.openlocfilehash: 2ae7f5099db2f9aee0c6f6e86e3dba690aa61454
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667856"
---
# <span data-ttu-id="b42e1-101">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="b42e1-101">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span></span>

## <span data-ttu-id="b42e1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b42e1-102">SYNOPSIS</span></span>
<span data-ttu-id="b42e1-103">A DSC csomópontok konfigurációjának beállítása az automatizálási ütemtervben.</span><span class="sxs-lookup"><span data-stu-id="b42e1-103">Gets a DSC Node configuration deployment job schedule in Automation.</span></span>

## <span data-ttu-id="b42e1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b42e1-104">SYNTAX</span></span>

### <span data-ttu-id="b42e1-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b42e1-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNodeConfigurationDeploymentSchedule [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b42e1-106">ByJobScheduleId</span><span class="sxs-lookup"><span data-stu-id="b42e1-106">ByJobScheduleId</span></span>
```
Get-AzAutomationDscNodeConfigurationDeploymentSchedule -JobScheduleId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b42e1-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b42e1-107">DESCRIPTION</span></span>
<span data-ttu-id="b42e1-108">A **Get-AzAutomationDscNodeConfigurationDeployment** parancsmag az Azure-alapú csomópont-konfiguráció (DSC) csomópont-konfigurációját telepíti az Azure automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="b42e1-108">The **Get-AzAutomationDscNodeConfigurationDeployment** cmdlet deploys an APS Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="b42e1-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b42e1-109">EXAMPLES</span></span>

### <span data-ttu-id="b42e1-110">1. példa: a bevezetési ütemtervek beszerzése</span><span class="sxs-lookup"><span data-stu-id="b42e1-110">Example 1: Get all the deployment schedules</span></span>
```
PS C:\> Get-AzAutomationDscNodeConfigurationDeploymentSchedule `
            -AutomationAccountName "Contoso01"  `
            -ResourceGroupName "ResourceGroup01"

ResourceGroupName     : ResourceGroup01
AutomationAccountName : Contoso01
JobScheduleId         : 2b1d7738-093d-4ff7-b87b-e4b2321319e5
JobSchedule           : Microsoft.Azure.Commands.Automation.Model.JobSchedule
RunbookName           : Deploy-NodeConfigurationToAutomationDscNodesV1

ResourceGroupName     : ResourceGroup01
AutomationAccountName : Contoso01
JobScheduleId         : e347dfc4-62fe-4ed6-adfb-55518c57b558
JobSchedule           : Microsoft.Azure.Commands.Automation.Model.JobSchedule
RunbookName           : Deploy-NodeConfigurationToAutomationDscNodesV1
```

### <span data-ttu-id="b42e1-111">2. példa: a bevezetési ütemterv beszerzése</span><span class="sxs-lookup"><span data-stu-id="b42e1-111">Example 2: Get a deployment schedule</span></span>
```
PS C:\> $js= Get-AzAutomationDscNodeConfigurationDeploymentSchedule `
                 -AutomationAccountName "Contoso01" `
                 -ResourceGroupName "ResourceGroup01" `
                 -JobScheduleId 2b1d7738-093d-4ff7-b87b-e4b2321319e5

PS C:\> $js

ResourceGroupName     : ResourceGroup01
AutomationAccountName : Contoso01
JobScheduleId         : 2b1d7738-093d-4ff7-b87b-e4b2321319e5
JobSchedule           : Microsoft.Azure.Commands.Automation.Model.JobSche
RunbookName           : Deploy-NodeConfigurationToAutomationDscNodesV1

PS C:\> $js.JobSchedule

ResourceGroupName     : ResourceGroup01
RunOn                 :
AutomationAccountName : Contoso01
JobScheduleId         : 2b1d7738-093d-4ff7-b87b-e4b2321319e5
RunbookName           : Deploy-NodeConfigurationToAutomationDscNodesV1
ScheduleName          : TestScheduleName
Parameters            : {AutomationAccountName, NodeConfigurationName, ResourceGroupName, ListOfNodeNames}
HybridWorker          :
```

<span data-ttu-id="b42e1-112">A fenti parancs az "Config01. Node1" nevű DSC csomópont-konfigurációt telepíti a csomópontok nevének adott kétdimenziós sorába.</span><span class="sxs-lookup"><span data-stu-id="b42e1-112">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="b42e1-113">A telepítés szakaszos módon történik.</span><span class="sxs-lookup"><span data-stu-id="b42e1-113">The deployment happens in a staged manner.</span></span>

## <span data-ttu-id="b42e1-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b42e1-114">PARAMETERS</span></span>

### <span data-ttu-id="b42e1-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b42e1-115">-AutomationAccountName</span></span>
<span data-ttu-id="b42e1-116">Annak az automatizálási fióknak a nevét adja meg, amely a parancsmag által lefordított DSC-konfigurációt tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="b42e1-116">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="b42e1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b42e1-117">-DefaultProfile</span></span>
<span data-ttu-id="b42e1-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b42e1-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b42e1-119">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="b42e1-119">-JobScheduleId</span></span>
<span data-ttu-id="b42e1-120">A meglévő ütemezett központi telepítés feladatának projekt-ütemezési azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b42e1-120">Specifies the Job Schedule id of an existing scheduled deployment job.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ByJobScheduleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b42e1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b42e1-121">-ResourceGroupName</span></span>
<span data-ttu-id="b42e1-122">Annak a csoportnak a nevét adja meg, amelyben a parancsmag egy konfigurációt összeállít.</span><span class="sxs-lookup"><span data-stu-id="b42e1-122">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="b42e1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b42e1-123">CommonParameters</span></span>
<span data-ttu-id="b42e1-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b42e1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b42e1-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b42e1-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b42e1-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b42e1-126">INPUTS</span></span>

### <span data-ttu-id="b42e1-127">System. GUID</span><span class="sxs-lookup"><span data-stu-id="b42e1-127">System.Guid</span></span>

### <span data-ttu-id="b42e1-128">System. String</span><span class="sxs-lookup"><span data-stu-id="b42e1-128">System.String</span></span>

## <span data-ttu-id="b42e1-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b42e1-129">OUTPUTS</span></span>

### <span data-ttu-id="b42e1-130">Microsoft. Azure. Command. Automation. Model. NodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="b42e1-130">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeploymentSchedule</span></span>

## <span data-ttu-id="b42e1-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b42e1-131">NOTES</span></span>

## <span data-ttu-id="b42e1-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b42e1-132">RELATED LINKS</span></span>

[<span data-ttu-id="b42e1-133">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="b42e1-133">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="b42e1-134">Importálás – AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="b42e1-134">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="b42e1-135">Start-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="b42e1-135">Start-AzAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="b42e1-136">Stop-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="b42e1-136">Stop-AzAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="b42e1-137">Get-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="b42e1-137">Get-AzAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzAutomationDscNodeConfigurationDeployment.md)
