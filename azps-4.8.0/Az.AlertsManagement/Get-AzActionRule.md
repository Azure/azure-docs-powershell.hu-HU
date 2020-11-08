---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzActionRule.md
ms.openlocfilehash: 59ce466233e4997f54ed8f29835e7e64d455fb86
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024998"
---
# <span data-ttu-id="86873-101">Get-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="86873-101">Get-AzActionRule</span></span>

## <span data-ttu-id="86873-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="86873-102">SYNOPSIS</span></span>
<span data-ttu-id="86873-103">A műveleti szabályok adatainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="86873-103">Get Action Rules Information</span></span>

## <span data-ttu-id="86873-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="86873-104">SYNTAX</span></span>

### <span data-ttu-id="86873-105">ListActionRules (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="86873-105">ListActionRules (Default)</span></span>
```
Get-AzActionRule [-Name <String>] [-ResourceGroupName <String>] [-TargetResourceType <String>]
 [-TargetResourceGroup <String>] [-MonitorService <String>] [-Severity <String>] [-ImpactedScope <String>]
 [-AlertRuleId <String>] [-Description <String>] [-ActionGroup <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="86873-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="86873-106">ResourceId</span></span>
```
Get-AzActionRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="86873-107">ActionRuleByName</span><span class="sxs-lookup"><span data-stu-id="86873-107">ActionRuleByName</span></span>
```
Get-AzActionRule -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="86873-108">ListActionRulesByTargetResourceId</span><span class="sxs-lookup"><span data-stu-id="86873-108">ListActionRulesByTargetResourceId</span></span>
```
Get-AzActionRule [-Name <String>] [-ResourceGroupName <String>] [-TargetResourceId <String>]
 [-MonitorService <String>] [-Severity <String>] [-ImpactedScope <String>] [-AlertRuleId <String>]
 [-Description <String>] [-ActionGroup <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="86873-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="86873-109">DESCRIPTION</span></span>
<span data-ttu-id="86873-110">A **Get-AzActionRule** parancsmag a beállított műveleti szabályokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="86873-110">**Get-AzActionRule** cmdlet gets action rules configured.</span></span>

## <span data-ttu-id="86873-111">Példák</span><span class="sxs-lookup"><span data-stu-id="86873-111">EXAMPLES</span></span>

### <span data-ttu-id="86873-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="86873-112">Example 1</span></span>
```powershell
PS C:\> Get-AzActionRule -ResourceGroupName "test-rg" -Severity "Sev2" -MonitorService "Platform"
```

<span data-ttu-id="86873-113">A Sev2 súlyossági és platform monitor szolgáltatással szűrt, az erőforráscsoport által kiszűrt összes műveleti szabály listáját jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="86873-113">List all action rules configured in resource group test-rg filtered on Sev2 severity and Platform Monitor Service.</span></span> <span data-ttu-id="86873-114">A Format-List használatával lekérheti az egyes műveleti szabályok listáját.</span><span class="sxs-lookup"><span data-stu-id="86873-114">Use Format-List to get the details of each action rule in list.</span></span>

### <span data-ttu-id="86873-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="86873-115">Example 2</span></span>
```powershell
PS C:\> Get-AzActionRule -ResourceGroupName "test-rg" -Name "Test-Action-Rule" | Format-List
```

<span data-ttu-id="86873-116">A műveleti szabály beszerzése: a név – műveleti szabály a teszt-RG erőforráscsoport területén.</span><span class="sxs-lookup"><span data-stu-id="86873-116">Get the action rule with name Test-Action-Rule in test-rg resource group.</span></span>

## <span data-ttu-id="86873-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="86873-117">PARAMETERS</span></span>

### <span data-ttu-id="86873-118">-ActionGroup</span><span class="sxs-lookup"><span data-stu-id="86873-118">-ActionGroup</span></span>
<span data-ttu-id="86873-119">Műveleti csoport</span><span class="sxs-lookup"><span data-stu-id="86873-119">Action group</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86873-120">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="86873-120">-AlertRuleId</span></span>
<span data-ttu-id="86873-121">Szűrés riasztási szabály azonosítójával</span><span class="sxs-lookup"><span data-stu-id="86873-121">Filter on Alert Rule Id</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86873-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86873-122">-DefaultProfile</span></span>
<span data-ttu-id="86873-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="86873-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86873-124">-Leírás</span><span class="sxs-lookup"><span data-stu-id="86873-124">-Description</span></span>
<span data-ttu-id="86873-125">Az intelligens csoport azonosítóját azonosító értesítések szűrése</span><span class="sxs-lookup"><span data-stu-id="86873-125">Filter all the alerts having the Smart Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86873-126">-ImpactedScope</span><span class="sxs-lookup"><span data-stu-id="86873-126">-ImpactedScope</span></span>
<span data-ttu-id="86873-127">Az érintett hatókör szűrése</span><span class="sxs-lookup"><span data-stu-id="86873-127">Filter on Impacted scope</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86873-128">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="86873-128">-MonitorService</span></span>
<span data-ttu-id="86873-129">Szűrés a moniter szolgáltatásban</span><span class="sxs-lookup"><span data-stu-id="86873-129">Filter on Moniter Service</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86873-130">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="86873-130">-Name</span></span>
<span data-ttu-id="86873-131">A műveleti szabály neve.</span><span class="sxs-lookup"><span data-stu-id="86873-131">Name of action rule.</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ActionRuleByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86873-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86873-132">-ResourceGroupName</span></span>
<span data-ttu-id="86873-133">Az erőforráscsoport neve, amelyben a műveleti szabály található.</span><span class="sxs-lookup"><span data-stu-id="86873-133">Resource Group Name in which action rule resides.</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ActionRuleByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86873-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="86873-134">-ResourceId</span></span>
<span data-ttu-id="86873-135">Műveletkérő szabály kérése erőforrás-azonosítóval</span><span class="sxs-lookup"><span data-stu-id="86873-135">Get Action rule by resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86873-136">-Súlyosság</span><span class="sxs-lookup"><span data-stu-id="86873-136">-Severity</span></span>
<span data-ttu-id="86873-137">Az értesítés súlyosságának szűrése</span><span class="sxs-lookup"><span data-stu-id="86873-137">Filter on Severity of alert</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86873-138">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="86873-138">-TargetResourceGroup</span></span>
<span data-ttu-id="86873-139">Szűrés a riasztás céljára szolgáló erőforrás erőforráscsoport nevében</span><span class="sxs-lookup"><span data-stu-id="86873-139">Filter on Resource group name of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86873-140">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="86873-140">-TargetResourceId</span></span>
<span data-ttu-id="86873-141">Szűri az értesítés cél erőforrásának erőforrás-azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="86873-141">Filter on Resource Id of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86873-142">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="86873-142">-TargetResourceType</span></span>
<span data-ttu-id="86873-143">Szűrés az értesítés cél erőforrásának erőforrás-típusára vonatkozóan</span><span class="sxs-lookup"><span data-stu-id="86873-143">Filter on Resource type of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86873-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86873-144">CommonParameters</span></span>
<span data-ttu-id="86873-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="86873-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86873-146">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="86873-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86873-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="86873-147">INPUTS</span></span>

### <span data-ttu-id="86873-148">Nincs</span><span class="sxs-lookup"><span data-stu-id="86873-148">None</span></span>

## <span data-ttu-id="86873-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="86873-149">OUTPUTS</span></span>

### <span data-ttu-id="86873-150">Microsoft. Azure. Command. AlertsManagement. OutputModels. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="86873-150">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="86873-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="86873-151">NOTES</span></span>

## <span data-ttu-id="86873-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="86873-152">RELATED LINKS</span></span>
