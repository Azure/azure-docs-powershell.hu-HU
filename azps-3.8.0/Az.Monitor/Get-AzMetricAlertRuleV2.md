---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azmetricalertrulev2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetricAlertRuleV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetricAlertRuleV2.md
ms.openlocfilehash: d809a7d01e6b4d477a72d26df11d73e87678d7e0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847514"
---
# <span data-ttu-id="2d917-101">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="2d917-101">Get-AzMetricAlertRuleV2</span></span>

## <span data-ttu-id="2d917-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2d917-102">SYNOPSIS</span></span>
<span data-ttu-id="2d917-103">A v2 (nem klasszikus) metrikus figyelmeztetési szabályok</span><span class="sxs-lookup"><span data-stu-id="2d917-103">Gets V2 (non-classic) metric alert rules</span></span>

## <span data-ttu-id="2d917-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2d917-104">SYNTAX</span></span>

### <span data-ttu-id="2d917-105">ByResourceGroupName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2d917-105">ByResourceGroupName (Default)</span></span>
```
Get-AzMetricAlertRuleV2 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2d917-106">ByRuleName</span><span class="sxs-lookup"><span data-stu-id="2d917-106">ByRuleName</span></span>
```
Get-AzMetricAlertRuleV2 -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2d917-107">ByRuleId</span><span class="sxs-lookup"><span data-stu-id="2d917-107">ByRuleId</span></span>
```
Get-AzMetricAlertRuleV2 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d917-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="2d917-108">DESCRIPTION</span></span>
<span data-ttu-id="2d917-109">A **Get-AzMetricAlertRuleV2** parancsmag metrikus figyelmeztetési szabályt kap a nevében vagy az URI-ban, illetve egy adott erőforráscsoport vagy előfizetéshez tartozó összes metrikus figyelmeztetési szabály alapján.</span><span class="sxs-lookup"><span data-stu-id="2d917-109">The **Get-AzMetricAlertRuleV2** cmdlet gets a metric alert rule by its name or URI, or all metric alert rules from a specified resource group or subscription.</span></span>

## <span data-ttu-id="2d917-110">Példák</span><span class="sxs-lookup"><span data-stu-id="2d917-110">EXAMPLES</span></span>

### <span data-ttu-id="2d917-111">Példa 1: az összes metrikus figyelmeztetési szabály beolvasása a jelenlegi előfizetésben</span><span class="sxs-lookup"><span data-stu-id="2d917-111">Example 1: Get all metric alert rules in current subscription</span></span>
```powershell
PS C:\>Get-AzMetricAlertRuleV2
TargetResourceId     : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricResourceGroup/providers/Microsoft.KeyVault/vaults/GenevaRPKeyVault
Criteria             : {Metric1}
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/sampleresourcegroup/providers/microsoft.insights/actiongroups/scnewactiongroup}
ResourceGroup        : metricResourceGroup
Description          : fdafda
Severity             : 3
Enabled              : True
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricResourceGroup/providers/Microsoft.KeyVault/vaults/GenevaRPKeyVault}
EvaluationFrequency  : 00:01:00
WindowSize           : 00:05:00
TargetResourceType   :
TargetResourceRegion :
AutoMitigate         :
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricResourceGroup/providers/microsoft.insights/metricAlerts/Rule1
Name                 : Rule1
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 : {}

Criteria             : {Metric1}
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/sampleresourcegroup/providers/microsoft.insights/actiongroups/scnewactiongroup}
ResourceGroup        : SampleResourceGroup
Description          : Testing 1 minute granuarity
Severity             : 3
Enabled              : True
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/SampleResourceGroup/providers/Microsoft.Compute/virtualMachines/SCCMDemo4}
EvaluationFrequency  : 00:01:00
WindowSize           : 00:01:00
TargetResourceType   : Microsoft.Compute/virtualMachines
TargetResourceRegion : eastus
AutoMitigate         : True
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/SampleResourceGroup/providers/microsoft.insights/metricAlerts/Rule2
Name                 : Rule2
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 : {}
```

<span data-ttu-id="2d917-112">Ez a parancs az aktuális előfizetéshez tartozó összes metrikus figyelmeztetési szabályt megkapja.</span><span class="sxs-lookup"><span data-stu-id="2d917-112">This command gets all the metric alert rules in the current subscription.</span></span>

### <span data-ttu-id="2d917-113">2. példa: egy erőforráscsoport minden metrikus figyelmeztetési szabályának beolvasása</span><span class="sxs-lookup"><span data-stu-id="2d917-113">Example 2: Get all metric alert rules in a resource group</span></span>

```powershell
PS C:\>Get-AzMetricAlertRuleV2 -ResourceGroupName metricAlertsRG
Criteria             : {Metric1}
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/pr
                       oviders/microsoft.insights/actiongroups/emails}
ResourceGroup        : metricAlertsRG
Description          : Test Classic VM alert - CPU Usage
Severity             : 3
Enabled              : True
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertsRG/providers/Micr
                       osoft.ClassicCompute/virtualMachines/VM1}
EvaluationFrequency  : 00:01:00
WindowSize           : 00:05:00
TargetResourceType   : Microsoft.ClassicCompute/virtualMachines
TargetResourceRegion : southcentralus
AutoMitigate         : True
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertsRG/providers/micro
                       soft.insights/metricAlerts/Test%20Classic%20VM%20alert%20-%20CPU%20Usage
Name                 : Test Classic VM alert - CPU Usage
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 : {}
```

<span data-ttu-id="2d917-114">Ez a parancs a metricAlertsRG nevű erőforráscsoport metrikus figyelmeztetési szabályait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="2d917-114">This command gets all the metric alert rules in the resource group named metricAlertsRG.</span></span>

### <span data-ttu-id="2d917-115">3. példa: metrikus figyelmeztetési szabály beszerzése név szerint</span><span class="sxs-lookup"><span data-stu-id="2d917-115">Example 3: Get a metric alert rule by name</span></span>

```powershell
PS C:\> Get-AzMetricAlertRuleV2 -ResourceGroupName metricAlertsRG -Name PS3182019

Criteria             : {metric1}
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/providers/microsoft.insights/actiongroups/demo}
ResourceGroup        : metricAlertsRG
Description          : This is description 
Severity             : 1
Enabled              : True
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertsRG/providers/Microsoft.Compute/virtualMachines/VM1,
                       /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertsRG/providers/Microsoft.Compute/virtualMachines/VM2}
EvaluationFrequency  : 00:05:00
WindowSize           : 00:05:00
TargetResourceType   : Microsoft.Compute/virtualMachines
TargetResourceRegion : eastus
AutoMitigate         :
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertsRG/providers/Microsoft.Insights/metricAlerts/PS3182019
Name                 : PS3182019
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 :
```

<span data-ttu-id="2d917-116">Ez a parancs a PS3182019 nevű metrikus riasztási szabályt a metricAlertsRG nevű erőforráscsoportben kapja meg.</span><span class="sxs-lookup"><span data-stu-id="2d917-116">This command gets the metric alert rule named PS3182019 in the resource group named metricAlertsRG.</span></span>

### <span data-ttu-id="2d917-117">Példa 4: metrikus figyelmeztetési szabály beszerzése ruleID szerint</span><span class="sxs-lookup"><span data-stu-id="2d917-117">Example 4: Get a metric alert rule by ruleID</span></span>

```powershell
PS C:\>Get-AzMetricAlertRuleV2 -ResourceId /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/SampleResourceGroup/providers/microsoft.insights/metricAlerts/MyMetricAlertRule
TargetResourceId     : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/SampleResourceGroup/providers/microsoft.insights/components/alertstestFunction
Criteria             : {Metric1}
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/providers/microsoft.insights/actiongroups/emails}
ResourceGroup        : SampleResourceGroup
Description          : Test Description
Severity             : 3
Enabled              : True
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/SampleResourceGroup/providers/microsoft.insights/components/alertstestFunction}
EvaluationFrequency  : 00:01:00
WindowSize           : 00:05:00
TargetResourceType   : 
TargetResourceRegion : 
AutoMitigate         : 
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/SampleResourceGroup/providers/microsoft.insights/metricAlerts/MyMetricAlertRule
Name                 : MyMetricAlertRule
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 :
```

<span data-ttu-id="2d917-118">Ez a parancs a metrika figyelmeztetési szabályát a megadott erőforrás-AZONOSÍTÓval kapja meg.</span><span class="sxs-lookup"><span data-stu-id="2d917-118">This command gets the metric alert rule with the given resource ID.</span></span>

## <span data-ttu-id="2d917-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2d917-119">PARAMETERS</span></span>

### <span data-ttu-id="2d917-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d917-120">-DefaultProfile</span></span>
<span data-ttu-id="2d917-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2d917-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d917-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2d917-122">-Name</span></span>
<span data-ttu-id="2d917-123">A metrikus figyelmeztetési szabály neve</span><span class="sxs-lookup"><span data-stu-id="2d917-123">The Name of metric alert rule</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d917-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d917-124">-ResourceGroupName</span></span>
<span data-ttu-id="2d917-125">A ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d917-125">The ResourceGroupName</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupName
Aliases: ResourceGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByRuleName
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d917-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2d917-126">-ResourceId</span></span>
<span data-ttu-id="2d917-127">A metrika-figyelmeztetési szabály azonosítójának szabálya</span><span class="sxs-lookup"><span data-stu-id="2d917-127">The Rule Id of metric alert rule</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d917-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d917-128">CommonParameters</span></span>
<span data-ttu-id="2d917-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2d917-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d917-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2d917-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d917-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2d917-131">INPUTS</span></span>

### <span data-ttu-id="2d917-132">System. String</span><span class="sxs-lookup"><span data-stu-id="2d917-132">System.String</span></span>

## <span data-ttu-id="2d917-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2d917-133">OUTPUTS</span></span>

### <span data-ttu-id="2d917-134">Microsoft. Azure. commands. OutputClasses. PSMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="2d917-134">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span></span>

## <span data-ttu-id="2d917-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2d917-135">NOTES</span></span>

## <span data-ttu-id="2d917-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2d917-136">RELATED LINKS</span></span>