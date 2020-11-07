---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzActionRule.md
ms.openlocfilehash: f3904826ef41f271086d048183b8b2035d1b11e0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668194"
---
# <span data-ttu-id="391f3-101">Get-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="391f3-101">Get-AzActionRule</span></span>

## <span data-ttu-id="391f3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="391f3-102">SYNOPSIS</span></span>
<span data-ttu-id="391f3-103">A műveleti szabályok adatainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="391f3-103">Get Action Rules Information</span></span>

## <span data-ttu-id="391f3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="391f3-104">SYNTAX</span></span>

### <span data-ttu-id="391f3-105">ListActionRules (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="391f3-105">ListActionRules (Default)</span></span>
```
Get-AzActionRule [-Name <String>] [-ResourceGroupName <String>] [-TargetResourceType <String>]
 [-TargetResourceGroup <String>] [-MonitorService <String>] [-Severity <String>] [-ImpactedScope <String>]
 [-AlertRuleId <String>] [-Description <String>] [-ActionGroup <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="391f3-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="391f3-106">ResourceId</span></span>
```
Get-AzActionRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="391f3-107">ActionRuleByName</span><span class="sxs-lookup"><span data-stu-id="391f3-107">ActionRuleByName</span></span>
```
Get-AzActionRule -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="391f3-108">ListActionRulesByTargetResourceId</span><span class="sxs-lookup"><span data-stu-id="391f3-108">ListActionRulesByTargetResourceId</span></span>
```
Get-AzActionRule [-Name <String>] [-ResourceGroupName <String>] [-TargetResourceId <String>]
 [-MonitorService <String>] [-Severity <String>] [-ImpactedScope <String>] [-AlertRuleId <String>]
 [-Description <String>] [-ActionGroup <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="391f3-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="391f3-109">DESCRIPTION</span></span>
<span data-ttu-id="391f3-110">A **Get-AzActionRule** parancsmag a beállított műveleti szabályokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="391f3-110">**Get-AzActionRule** cmdlet gets action rules configured.</span></span>

## <span data-ttu-id="391f3-111">Példák</span><span class="sxs-lookup"><span data-stu-id="391f3-111">EXAMPLES</span></span>

### <span data-ttu-id="391f3-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="391f3-112">Example 1</span></span>
```powershell
PS C:\> Get-AzActionRule -ResourceGroupName "test-rg" -Severity "Sev2" -MonitorService "Platform"
```

<span data-ttu-id="391f3-113">A Sev2 súlyossági és platform monitor szolgáltatással szűrt, az erőforráscsoport által kiszűrt összes műveleti szabály listáját jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="391f3-113">List all action rules configured in resource group test-rg filtered on Sev2 severity and Platform Monitor Service.</span></span> <span data-ttu-id="391f3-114">A Format-List használatával lekérheti az egyes műveleti szabályok listáját.</span><span class="sxs-lookup"><span data-stu-id="391f3-114">Use Format-List to get the details of each action rule in list.</span></span>

### <span data-ttu-id="391f3-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="391f3-115">Example 2</span></span>
```powershell
PS C:\> Get-AzActionRule -ResourceGroupName "test-rg" -Name "Test-Action-Rule" | Format-List
```

<span data-ttu-id="391f3-116">A műveleti szabály beszerzése: a név – műveleti szabály a teszt-RG erőforráscsoport területén.</span><span class="sxs-lookup"><span data-stu-id="391f3-116">Get the action rule with name Test-Action-Rule in test-rg resource group.</span></span>

## <span data-ttu-id="391f3-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="391f3-117">PARAMETERS</span></span>

### <span data-ttu-id="391f3-118">-ActionGroup</span><span class="sxs-lookup"><span data-stu-id="391f3-118">-ActionGroup</span></span>
<span data-ttu-id="391f3-119">Műveleti csoport</span><span class="sxs-lookup"><span data-stu-id="391f3-119">Action group</span></span>

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

### <span data-ttu-id="391f3-120">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="391f3-120">-AlertRuleId</span></span>
<span data-ttu-id="391f3-121">Szűrés riasztási szabály azonosítójával</span><span class="sxs-lookup"><span data-stu-id="391f3-121">Filter on Alert Rule Id</span></span>

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

### <span data-ttu-id="391f3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="391f3-122">-DefaultProfile</span></span>
<span data-ttu-id="391f3-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="391f3-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="391f3-124">-Leírás</span><span class="sxs-lookup"><span data-stu-id="391f3-124">-Description</span></span>
<span data-ttu-id="391f3-125">Az intelligens csoport azonosítóját azonosító értesítések szűrése</span><span class="sxs-lookup"><span data-stu-id="391f3-125">Filter all the alerts having the Smart Group Id</span></span>

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

### <span data-ttu-id="391f3-126">-ImpactedScope</span><span class="sxs-lookup"><span data-stu-id="391f3-126">-ImpactedScope</span></span>
<span data-ttu-id="391f3-127">Az érintett hatókör szűrése</span><span class="sxs-lookup"><span data-stu-id="391f3-127">Filter on Impacted scope</span></span>

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

### <span data-ttu-id="391f3-128">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="391f3-128">-MonitorService</span></span>
<span data-ttu-id="391f3-129">Szűrés a moniter szolgáltatásban</span><span class="sxs-lookup"><span data-stu-id="391f3-129">Filter on Moniter Service</span></span>

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

### <span data-ttu-id="391f3-130">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="391f3-130">-Name</span></span>
<span data-ttu-id="391f3-131">A műveleti szabály neve.</span><span class="sxs-lookup"><span data-stu-id="391f3-131">Name of action rule.</span></span>

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

### <span data-ttu-id="391f3-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="391f3-132">-ResourceGroupName</span></span>
<span data-ttu-id="391f3-133">Az erőforráscsoport neve, amelyben a műveleti szabály található.</span><span class="sxs-lookup"><span data-stu-id="391f3-133">Resource Group Name in which action rule resides.</span></span>

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

### <span data-ttu-id="391f3-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="391f3-134">-ResourceId</span></span>
<span data-ttu-id="391f3-135">Műveletkérő szabály kérése az azonosító megadásával.</span><span class="sxs-lookup"><span data-stu-id="391f3-135">Get Action rule by resoure id.</span></span>

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

### <span data-ttu-id="391f3-136">-Súlyosság</span><span class="sxs-lookup"><span data-stu-id="391f3-136">-Severity</span></span>
<span data-ttu-id="391f3-137">Az értesítés súlyosságának szűrése</span><span class="sxs-lookup"><span data-stu-id="391f3-137">Filter on Severity of alert</span></span>

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

### <span data-ttu-id="391f3-138">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="391f3-138">-TargetResourceGroup</span></span>
<span data-ttu-id="391f3-139">Szűrés a riasztás céljára szolgáló erőforrás erőforráscsoport nevében</span><span class="sxs-lookup"><span data-stu-id="391f3-139">Filter on Resource group name of the target resource of alert.</span></span>

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

### <span data-ttu-id="391f3-140">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="391f3-140">-TargetResourceId</span></span>
<span data-ttu-id="391f3-141">Szűri az értesítés cél erőforrásának erőforrás-azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="391f3-141">Filter on Resource Id of the target resource of alert.</span></span>

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

### <span data-ttu-id="391f3-142">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="391f3-142">-TargetResourceType</span></span>
<span data-ttu-id="391f3-143">Szűrés az értesítés cél erőforrásának erőforrás-típusára vonatkozóan</span><span class="sxs-lookup"><span data-stu-id="391f3-143">Filter on Resource type of the target resource of alert.</span></span>

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

### <span data-ttu-id="391f3-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="391f3-144">CommonParameters</span></span>
<span data-ttu-id="391f3-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="391f3-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="391f3-146">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="391f3-146">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="391f3-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="391f3-147">INPUTS</span></span>

### <span data-ttu-id="391f3-148">Nincs</span><span class="sxs-lookup"><span data-stu-id="391f3-148">None</span></span>

## <span data-ttu-id="391f3-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="391f3-149">OUTPUTS</span></span>

### <span data-ttu-id="391f3-150">Microsoft. Azure. Command. AlertsManagement. OutputModels. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="391f3-150">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="391f3-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="391f3-151">NOTES</span></span>

## <span data-ttu-id="391f3-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="391f3-152">RELATED LINKS</span></span>
