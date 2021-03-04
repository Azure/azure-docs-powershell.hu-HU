---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/powershell/module/az.alertsmanagement/get-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzActionRule.md
ms.openlocfilehash: c90c4ba559bfe6e453a984546217692181f40597
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923137"
---
# <span data-ttu-id="e5f36-101">Get-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="e5f36-101">Get-AzActionRule</span></span>

## <span data-ttu-id="e5f36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5f36-102">SYNOPSIS</span></span>
<span data-ttu-id="e5f36-103">A műveletszabályokkal kapcsolatos információk lekérte</span><span class="sxs-lookup"><span data-stu-id="e5f36-103">Get Action Rules Information</span></span>

## <span data-ttu-id="e5f36-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e5f36-104">SYNTAX</span></span>

### <span data-ttu-id="e5f36-105">ListActionRules (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e5f36-105">ListActionRules (Default)</span></span>
```
Get-AzActionRule [-Name <String>] [-ResourceGroupName <String>] [-TargetResourceType <String>]
 [-TargetResourceGroup <String>] [-MonitorService <String>] [-Severity <String>] [-ImpactedScope <String>]
 [-AlertRuleId <String>] [-Description <String>] [-ActionGroup <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5f36-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5f36-106">ResourceId</span></span>
```
Get-AzActionRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5f36-107">ActionRuleByName</span><span class="sxs-lookup"><span data-stu-id="e5f36-107">ActionRuleByName</span></span>
```
Get-AzActionRule -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e5f36-108">ListActionRulesByTargetResourceId</span><span class="sxs-lookup"><span data-stu-id="e5f36-108">ListActionRulesByTargetResourceId</span></span>
```
Get-AzActionRule [-Name <String>] [-ResourceGroupName <String>] [-TargetResourceId <String>]
 [-MonitorService <String>] [-Severity <String>] [-ImpactedScope <String>] [-AlertRuleId <String>]
 [-Description <String>] [-ActionGroup <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e5f36-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e5f36-109">DESCRIPTION</span></span>
<span data-ttu-id="e5f36-110">**A Get-AzActionRule** parancsmag beállítja a műveletszabályokat.</span><span class="sxs-lookup"><span data-stu-id="e5f36-110">**Get-AzActionRule** cmdlet gets action rules configured.</span></span>

## <span data-ttu-id="e5f36-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e5f36-111">EXAMPLES</span></span>

### <span data-ttu-id="e5f36-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="e5f36-112">Example 1</span></span>
```powershell
PS C:\> Get-AzActionRule -ResourceGroupName "test-rg" -Severity "Sev2" -MonitorService "Platform"
```

<span data-ttu-id="e5f36-113">List all action rules configured in resource group test-rg filtered on Sev2 severity and Platform Monitor Service.</span><span class="sxs-lookup"><span data-stu-id="e5f36-113">List all action rules configured in resource group test-rg filtered on Sev2 severity and Platform Monitor Service.</span></span> <span data-ttu-id="e5f36-114">A Format-List a listában található egyes műveletszabályokkal kapcsolatos részleteket.</span><span class="sxs-lookup"><span data-stu-id="e5f36-114">Use Format-List to get the details of each action rule in list.</span></span>

### <span data-ttu-id="e5f36-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="e5f36-115">Example 2</span></span>
```powershell
PS C:\> Get-AzActionRule -ResourceGroupName "test-rg" -Name "Test-Action-Rule" | Format-List
```

<span data-ttu-id="e5f36-116">A "Test-Action-Rule" nevű műveletszabály lekérte a test-rg erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="e5f36-116">Get the action rule with name Test-Action-Rule in test-rg resource group.</span></span>

## <span data-ttu-id="e5f36-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e5f36-117">PARAMETERS</span></span>

### <span data-ttu-id="e5f36-118">-ActionGroup</span><span class="sxs-lookup"><span data-stu-id="e5f36-118">-ActionGroup</span></span>
<span data-ttu-id="e5f36-119">Műveletcsoport</span><span class="sxs-lookup"><span data-stu-id="e5f36-119">Action group</span></span>

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

### <span data-ttu-id="e5f36-120">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="e5f36-120">-AlertRuleId</span></span>
<span data-ttu-id="e5f36-121">Szűrés riasztási szabályazonosító alapján</span><span class="sxs-lookup"><span data-stu-id="e5f36-121">Filter on Alert Rule Id</span></span>

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

### <span data-ttu-id="e5f36-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5f36-122">-DefaultProfile</span></span>
<span data-ttu-id="e5f36-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e5f36-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5f36-124">-Leírás</span><span class="sxs-lookup"><span data-stu-id="e5f36-124">-Description</span></span>
<span data-ttu-id="e5f36-125">Az intelligens csoportazonosítóval rendelkező összes riasztás szűrése</span><span class="sxs-lookup"><span data-stu-id="e5f36-125">Filter all the alerts having the Smart Group Id</span></span>

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

### <span data-ttu-id="e5f36-126">-ImpactedScope</span><span class="sxs-lookup"><span data-stu-id="e5f36-126">-ImpactedScope</span></span>
<span data-ttu-id="e5f36-127">Szűrés az érintett hatókör alapján</span><span class="sxs-lookup"><span data-stu-id="e5f36-127">Filter on Impacted scope</span></span>

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

### <span data-ttu-id="e5f36-128">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="e5f36-128">-MonitorService</span></span>
<span data-ttu-id="e5f36-129">Szűrés a Moniter szolgáltatáson</span><span class="sxs-lookup"><span data-stu-id="e5f36-129">Filter on Moniter Service</span></span>

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

### <span data-ttu-id="e5f36-130">-Name</span><span class="sxs-lookup"><span data-stu-id="e5f36-130">-Name</span></span>
<span data-ttu-id="e5f36-131">A műveletszabály neve.</span><span class="sxs-lookup"><span data-stu-id="e5f36-131">Name of action rule.</span></span>

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

### <span data-ttu-id="e5f36-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5f36-132">-ResourceGroupName</span></span>
<span data-ttu-id="e5f36-133">Az erőforráscsoport neve, amelyben a műveletszabály található.</span><span class="sxs-lookup"><span data-stu-id="e5f36-133">Resource Group Name in which action rule resides.</span></span>

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

### <span data-ttu-id="e5f36-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5f36-134">-ResourceId</span></span>
<span data-ttu-id="e5f36-135">A Műveletszabály lekérte erőforrás-azonosító szerint.</span><span class="sxs-lookup"><span data-stu-id="e5f36-135">Get Action rule by resource id.</span></span>

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

### <span data-ttu-id="e5f36-136">-Súlyosság</span><span class="sxs-lookup"><span data-stu-id="e5f36-136">-Severity</span></span>
<span data-ttu-id="e5f36-137">Szűrő a riasztás súlyossága alapján</span><span class="sxs-lookup"><span data-stu-id="e5f36-137">Filter on Severity of alert</span></span>

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

### <span data-ttu-id="e5f36-138">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e5f36-138">-TargetResourceGroup</span></span>
<span data-ttu-id="e5f36-139">Szűrő a riasztás célforrásának Erőforráscsoport neve alapján</span><span class="sxs-lookup"><span data-stu-id="e5f36-139">Filter on Resource group name of the target resource of alert.</span></span>

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

### <span data-ttu-id="e5f36-140">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="e5f36-140">-TargetResourceId</span></span>
<span data-ttu-id="e5f36-141">Szűrő a riasztás célforrásának erőforrás-azonosítója alapján</span><span class="sxs-lookup"><span data-stu-id="e5f36-141">Filter on Resource Id of the target resource of alert.</span></span>

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

### <span data-ttu-id="e5f36-142">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="e5f36-142">-TargetResourceType</span></span>
<span data-ttu-id="e5f36-143">Szűrés a riasztás célforrásának erőforrástípusa alapján</span><span class="sxs-lookup"><span data-stu-id="e5f36-143">Filter on Resource type of the target resource of alert.</span></span>

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

### <span data-ttu-id="e5f36-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5f36-144">CommonParameters</span></span>
<span data-ttu-id="e5f36-145">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5f36-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5f36-146">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e5f36-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5f36-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e5f36-147">INPUTS</span></span>

### <span data-ttu-id="e5f36-148">Nincs</span><span class="sxs-lookup"><span data-stu-id="e5f36-148">None</span></span>

## <span data-ttu-id="e5f36-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e5f36-149">OUTPUTS</span></span>

### <span data-ttu-id="e5f36-150">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="e5f36-150">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="e5f36-151">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e5f36-151">NOTES</span></span>

## <span data-ttu-id="e5f36-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e5f36-152">RELATED LINKS</span></span>
