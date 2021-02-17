---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzActionRule.md
ms.openlocfilehash: 59ce466233e4997f54ed8f29835e7e64d455fb86
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100159858"
---
# <span data-ttu-id="aeddb-101">Get-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="aeddb-101">Get-AzActionRule</span></span>

## <span data-ttu-id="aeddb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aeddb-102">SYNOPSIS</span></span>
<span data-ttu-id="aeddb-103">A műveletszabályokkal kapcsolatos információk lekérte</span><span class="sxs-lookup"><span data-stu-id="aeddb-103">Get Action Rules Information</span></span>

## <span data-ttu-id="aeddb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="aeddb-104">SYNTAX</span></span>

### <span data-ttu-id="aeddb-105">ListActionRules (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="aeddb-105">ListActionRules (Default)</span></span>
```
Get-AzActionRule [-Name <String>] [-ResourceGroupName <String>] [-TargetResourceType <String>]
 [-TargetResourceGroup <String>] [-MonitorService <String>] [-Severity <String>] [-ImpactedScope <String>]
 [-AlertRuleId <String>] [-Description <String>] [-ActionGroup <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aeddb-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="aeddb-106">ResourceId</span></span>
```
Get-AzActionRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aeddb-107">ActionRuleByName</span><span class="sxs-lookup"><span data-stu-id="aeddb-107">ActionRuleByName</span></span>
```
Get-AzActionRule -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="aeddb-108">ListActionRulesByTargetResourceId</span><span class="sxs-lookup"><span data-stu-id="aeddb-108">ListActionRulesByTargetResourceId</span></span>
```
Get-AzActionRule [-Name <String>] [-ResourceGroupName <String>] [-TargetResourceId <String>]
 [-MonitorService <String>] [-Severity <String>] [-ImpactedScope <String>] [-AlertRuleId <String>]
 [-Description <String>] [-ActionGroup <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aeddb-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="aeddb-109">DESCRIPTION</span></span>
<span data-ttu-id="aeddb-110">**A Get-AzActionRule** parancsmag beállítja a műveletszabályokat.</span><span class="sxs-lookup"><span data-stu-id="aeddb-110">**Get-AzActionRule** cmdlet gets action rules configured.</span></span>

## <span data-ttu-id="aeddb-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="aeddb-111">EXAMPLES</span></span>

### <span data-ttu-id="aeddb-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="aeddb-112">Example 1</span></span>
```powershell
PS C:\> Get-AzActionRule -ResourceGroupName "test-rg" -Severity "Sev2" -MonitorService "Platform"
```

<span data-ttu-id="aeddb-113">List all action rules configured in resource group test-rg filtered on Sev2 severity and Platform Monitor Service.</span><span class="sxs-lookup"><span data-stu-id="aeddb-113">List all action rules configured in resource group test-rg filtered on Sev2 severity and Platform Monitor Service.</span></span> <span data-ttu-id="aeddb-114">A Format-List a listában található egyes műveletszabályokkal kapcsolatos részleteket.</span><span class="sxs-lookup"><span data-stu-id="aeddb-114">Use Format-List to get the details of each action rule in list.</span></span>

### <span data-ttu-id="aeddb-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="aeddb-115">Example 2</span></span>
```powershell
PS C:\> Get-AzActionRule -ResourceGroupName "test-rg" -Name "Test-Action-Rule" | Format-List
```

<span data-ttu-id="aeddb-116">Szerezze be a "Test-Action-Rule" nevű műveletszabályt a test-rg erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="aeddb-116">Get the action rule with name Test-Action-Rule in test-rg resource group.</span></span>

## <span data-ttu-id="aeddb-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aeddb-117">PARAMETERS</span></span>

### <span data-ttu-id="aeddb-118">-ActionGroup</span><span class="sxs-lookup"><span data-stu-id="aeddb-118">-ActionGroup</span></span>
<span data-ttu-id="aeddb-119">Műveletcsoport</span><span class="sxs-lookup"><span data-stu-id="aeddb-119">Action group</span></span>

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

### <span data-ttu-id="aeddb-120">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="aeddb-120">-AlertRuleId</span></span>
<span data-ttu-id="aeddb-121">Szűrés riasztási szabályazonosító alapján</span><span class="sxs-lookup"><span data-stu-id="aeddb-121">Filter on Alert Rule Id</span></span>

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

### <span data-ttu-id="aeddb-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aeddb-122">-DefaultProfile</span></span>
<span data-ttu-id="aeddb-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="aeddb-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aeddb-124">-Leírás</span><span class="sxs-lookup"><span data-stu-id="aeddb-124">-Description</span></span>
<span data-ttu-id="aeddb-125">Az intelligens csoportazonosítóval rendelkező összes riasztás szűrése</span><span class="sxs-lookup"><span data-stu-id="aeddb-125">Filter all the alerts having the Smart Group Id</span></span>

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

### <span data-ttu-id="aeddb-126">-ImpactedScope</span><span class="sxs-lookup"><span data-stu-id="aeddb-126">-ImpactedScope</span></span>
<span data-ttu-id="aeddb-127">Szűrés az érintett hatókör alapján</span><span class="sxs-lookup"><span data-stu-id="aeddb-127">Filter on Impacted scope</span></span>

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

### <span data-ttu-id="aeddb-128">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="aeddb-128">-MonitorService</span></span>
<span data-ttu-id="aeddb-129">Szűrés a Moniter szolgáltatáson</span><span class="sxs-lookup"><span data-stu-id="aeddb-129">Filter on Moniter Service</span></span>

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

### <span data-ttu-id="aeddb-130">-Name</span><span class="sxs-lookup"><span data-stu-id="aeddb-130">-Name</span></span>
<span data-ttu-id="aeddb-131">A műveletszabály neve.</span><span class="sxs-lookup"><span data-stu-id="aeddb-131">Name of action rule.</span></span>

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

### <span data-ttu-id="aeddb-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aeddb-132">-ResourceGroupName</span></span>
<span data-ttu-id="aeddb-133">Az erőforráscsoport neve, amelyben a műveletszabály található.</span><span class="sxs-lookup"><span data-stu-id="aeddb-133">Resource Group Name in which action rule resides.</span></span>

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

### <span data-ttu-id="aeddb-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aeddb-134">-ResourceId</span></span>
<span data-ttu-id="aeddb-135">A Műveletszabály lekérte erőforrás-azonosító szerint.</span><span class="sxs-lookup"><span data-stu-id="aeddb-135">Get Action rule by resource id.</span></span>

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

### <span data-ttu-id="aeddb-136">-Súlyosság</span><span class="sxs-lookup"><span data-stu-id="aeddb-136">-Severity</span></span>
<span data-ttu-id="aeddb-137">Szűrő a riasztás súlyossága alapján</span><span class="sxs-lookup"><span data-stu-id="aeddb-137">Filter on Severity of alert</span></span>

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

### <span data-ttu-id="aeddb-138">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="aeddb-138">-TargetResourceGroup</span></span>
<span data-ttu-id="aeddb-139">Szűrő a riasztás célforrásának Erőforráscsoport neve alapján</span><span class="sxs-lookup"><span data-stu-id="aeddb-139">Filter on Resource group name of the target resource of alert.</span></span>

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

### <span data-ttu-id="aeddb-140">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="aeddb-140">-TargetResourceId</span></span>
<span data-ttu-id="aeddb-141">Szűrő a riasztás célforrásának erőforrás-azonosítója alapján</span><span class="sxs-lookup"><span data-stu-id="aeddb-141">Filter on Resource Id of the target resource of alert.</span></span>

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

### <span data-ttu-id="aeddb-142">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="aeddb-142">-TargetResourceType</span></span>
<span data-ttu-id="aeddb-143">Szűrés a riasztás célforrásának erőforrástípusa alapján</span><span class="sxs-lookup"><span data-stu-id="aeddb-143">Filter on Resource type of the target resource of alert.</span></span>

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

### <span data-ttu-id="aeddb-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aeddb-144">CommonParameters</span></span>
<span data-ttu-id="aeddb-145">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aeddb-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aeddb-146">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aeddb-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aeddb-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aeddb-147">INPUTS</span></span>

### <span data-ttu-id="aeddb-148">Nincs</span><span class="sxs-lookup"><span data-stu-id="aeddb-148">None</span></span>

## <span data-ttu-id="aeddb-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aeddb-149">OUTPUTS</span></span>

### <span data-ttu-id="aeddb-150">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="aeddb-150">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="aeddb-151">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="aeddb-151">NOTES</span></span>

## <span data-ttu-id="aeddb-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aeddb-152">RELATED LINKS</span></span>
