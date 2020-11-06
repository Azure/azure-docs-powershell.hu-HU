---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule.md
ms.openlocfilehash: 993de4da39f27a54be97de9fb7befe065fdd70f2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498004"
---
# <span data-ttu-id="35f91-101">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="35f91-101">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span></span>

## <span data-ttu-id="35f91-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="35f91-102">SYNOPSIS</span></span>
<span data-ttu-id="35f91-103">A DSC csomópontok konfigurációjának beállítása az automatizálási ütemtervben.</span><span class="sxs-lookup"><span data-stu-id="35f91-103">Gets a DSC Node configuration deployment job schedule in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35f91-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="35f91-104">SYNTAX</span></span>

### <span data-ttu-id="35f91-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="35f91-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35f91-106">ByJobScheduleId</span><span class="sxs-lookup"><span data-stu-id="35f91-106">ByJobScheduleId</span></span>
```
Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule -JobScheduleId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35f91-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="35f91-107">DESCRIPTION</span></span>
<span data-ttu-id="35f91-108">A **Get-AzureRmAutomationDscNodeConfigurationDeployment** parancsmag az Azure-alapú csomópont-konfiguráció (DSC) csomópont-konfigurációját telepíti az Azure automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="35f91-108">The **Get-AzureRmAutomationDscNodeConfigurationDeployment** cmdlet deployes an APS Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="35f91-109">Példák</span><span class="sxs-lookup"><span data-stu-id="35f91-109">EXAMPLES</span></span>

### <span data-ttu-id="35f91-110">1. példa: a bevezetési ütemtervek beszerzése</span><span class="sxs-lookup"><span data-stu-id="35f91-110">Example 1: Get all the deployment schedules</span></span>
```
PS C:\> Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule `
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

### <span data-ttu-id="35f91-111">2. példa: a bevezetési ütemterv beszerzése</span><span class="sxs-lookup"><span data-stu-id="35f91-111">Example 2: Get a deployment schedule</span></span>
```
PS C:\> $js= Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule `
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

<span data-ttu-id="35f91-112">A fenti parancs az "Config01. Node1" nevű DSC csomópont-konfigurációt telepíti a csomópontok nevének adott kétdimenziós sorába.</span><span class="sxs-lookup"><span data-stu-id="35f91-112">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="35f91-113">A telepítés szakaszos módon történik.</span><span class="sxs-lookup"><span data-stu-id="35f91-113">The deployment happens in a staged manner.</span></span>

## <span data-ttu-id="35f91-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="35f91-114">PARAMETERS</span></span>

### <span data-ttu-id="35f91-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35f91-115">-ResourceGroupName</span></span>
<span data-ttu-id="35f91-116">Annak a csoportnak a nevét adja meg, amelyben a parancsmag egy konfigurációt összeállít.</span><span class="sxs-lookup"><span data-stu-id="35f91-116">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="35f91-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="35f91-117">-AutomationAccountName</span></span>
<span data-ttu-id="35f91-118">Annak az automatizálási fióknak a nevét adja meg, amely a parancsmag által lefordított DSC-konfigurációt tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="35f91-118">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="35f91-119">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="35f91-119">-JobScheduleId</span></span>
<span data-ttu-id="35f91-120">A meglévő ütemezett központi telepítés feladatának projekt-ütemezési azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="35f91-120">Specifies the Job Schedule id of an existing scheduled deployment job.</span></span>

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

### <span data-ttu-id="35f91-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35f91-121">-DefaultProfile</span></span>
<span data-ttu-id="35f91-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="35f91-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35f91-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35f91-123">CommonParameters</span></span>
<span data-ttu-id="35f91-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="35f91-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35f91-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35f91-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35f91-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="35f91-126">INPUTS</span></span>

## <span data-ttu-id="35f91-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="35f91-127">OUTPUTS</span></span>

### <span data-ttu-id="35f91-128">Microsoft. Azure. Command. Automation. Model. NodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="35f91-128">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeploymentSchedule</span></span>

## <span data-ttu-id="35f91-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="35f91-129">NOTES</span></span>

## <span data-ttu-id="35f91-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="35f91-130">RELATED LINKS</span></span>

[<span data-ttu-id="35f91-131">Start-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="35f91-131">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)

[<span data-ttu-id="35f91-132">Importálás – AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="35f91-132">Import-AzureRmAutomationDscNodeConfiguration</span></span>](./Import-AzureRmAutomationDscNodeConfiguration.md)

[<span data-ttu-id="35f91-133">Start-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="35f91-133">Start-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="35f91-134">Stop-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="35f91-134">Stop-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="35f91-135">Get-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="35f91-135">Get-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzureRmAutomationDscNodeConfigurationDeployment.md)
