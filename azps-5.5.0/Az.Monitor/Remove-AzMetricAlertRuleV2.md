---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azmetricalertrulev2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzMetricAlertRuleV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzMetricAlertRuleV2.md
ms.openlocfilehash: d2b34063f5ece370d52b8a4c3c0dab35cff77c54
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147338"
---
# <span data-ttu-id="d4042-101">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="d4042-101">Remove-AzMetricAlertRuleV2</span></span>

## <span data-ttu-id="d4042-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4042-102">SYNOPSIS</span></span>
<span data-ttu-id="d4042-103">Eltávolít egy V2 -es (nem klasszikus) metrikus riasztási szabályt.</span><span class="sxs-lookup"><span data-stu-id="d4042-103">Removes a V2 (non-classic) metric alert rule.</span></span>

## <span data-ttu-id="d4042-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d4042-104">SYNTAX</span></span>

### <span data-ttu-id="d4042-105">ByMetricRuleResourceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d4042-105">ByMetricRuleResourceName (Default)</span></span>
```
Remove-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4042-106">ByMetricRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="d4042-106">ByMetricRuleResourceId</span></span>
```
Remove-AzMetricAlertRuleV2 -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4042-107">ByRuleObject</span><span class="sxs-lookup"><span data-stu-id="d4042-107">ByRuleObject</span></span>
```
Remove-AzMetricAlertRuleV2 -InputObject <PSMetricAlertRuleV2> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4042-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d4042-108">DESCRIPTION</span></span>
<span data-ttu-id="d4042-109">Az **Remove-AzMetricAlertRuleV2** parancsmag eltávolít egy riasztási szabályt.</span><span class="sxs-lookup"><span data-stu-id="d4042-109">The **Remove-AzMetricAlertRuleV2** cmdlet removes an alert rule.</span></span> <span data-ttu-id="d4042-110">Ez a parancsmag implementálja a ShouldProcess mintát, azaz megerősítést kérhet a felhasználótól, mielőtt ténylegesen létrehozza, módosítja vagy eltávolítja az erőforrást.</span><span class="sxs-lookup"><span data-stu-id="d4042-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="d4042-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d4042-111">EXAMPLES</span></span>

### <span data-ttu-id="d4042-112">1. példa: Értesítési szabály eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="d4042-112">Example 1: Remove an alert rule by name</span></span>

```powershell
PS C:\> Remove-AzMetricAlertRuleV2 -ResourceGroupName xxxxRG -Name PsSdk -PassThru
True
```

<span data-ttu-id="d4042-113">Ez a parancs eltávolítja a PsSdk nevű riasztási szabályt</span><span class="sxs-lookup"><span data-stu-id="d4042-113">This command removes the alert rule named PsSdk</span></span>

### <span data-ttu-id="d4042-114">2. példa: Értesítési szabály eltávolítása azonosító alapján</span><span class="sxs-lookup"><span data-stu-id="d4042-114">Example 2: Remove an alert rule by ID</span></span>

```powershell
PS C:\>Remove-AzMetricAlertRuleV2 -ResourceId /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertRG/providers/microsoft.insights/metricAlerts/myAlertRule
```

<span data-ttu-id="d4042-115">Ez a parancs eltávolítja a riasztási szabályt az erőforrás-azonosítóval `/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertRG/providers/microsoft.insights/metricAlerts/myAlertRule`</span><span class="sxs-lookup"><span data-stu-id="d4042-115">This command removes the alert rule with resource ID `/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertRG/providers/microsoft.insights/metricAlerts/myAlertRule`</span></span>

### <span data-ttu-id="d4042-116">3. példa: Értesítés lekérte és eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d4042-116">Example 3: Get an alert and remove it</span></span>

```powershell
PS c:\>Get-AzMetricAlertRuleV2 -ResourceGroupName alertstest -Name sampleAlertRule |Remove-AzMetricAlertRuleV2
```

<span data-ttu-id="d4042-117">Ez a parancs figyelmeztetést kap, és eltávolítja azt.</span><span class="sxs-lookup"><span data-stu-id="d4042-117">This command gets an alert and removes it.</span></span>

## <span data-ttu-id="d4042-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d4042-118">PARAMETERS</span></span>

### <span data-ttu-id="d4042-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d4042-119">-AsJob</span></span>
<span data-ttu-id="d4042-120">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="d4042-120">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4042-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4042-121">-DefaultProfile</span></span>
<span data-ttu-id="d4042-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d4042-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4042-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d4042-123">-InputObject</span></span>
<span data-ttu-id="d4042-124">A Metrikus szabály objektum</span><span class="sxs-lookup"><span data-stu-id="d4042-124">The Metric rule object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2
Parameter Sets: ByRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d4042-125">-Name</span><span class="sxs-lookup"><span data-stu-id="d4042-125">-Name</span></span>
<span data-ttu-id="d4042-126">A metrikus riasztási szabály neve</span><span class="sxs-lookup"><span data-stu-id="d4042-126">The name of metric alert rule</span></span>

```yaml
Type: System.String
Parameter Sets: ByMetricRuleResourceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4042-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d4042-127">-PassThru</span></span>
<span data-ttu-id="d4042-128">Sikeres törléskor a return true (igaz) érték.</span><span class="sxs-lookup"><span data-stu-id="d4042-128">Return true upon successful deletion.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4042-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4042-129">-ResourceGroupName</span></span>
<span data-ttu-id="d4042-130">A ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4042-130">The ResourceGroupName</span></span>

```yaml
Type: System.String
Parameter Sets: ByMetricRuleResourceName
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4042-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d4042-131">-ResourceId</span></span>
<span data-ttu-id="d4042-132">The RuleResourceId</span><span class="sxs-lookup"><span data-stu-id="d4042-132">The RuleResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: ByMetricRuleResourceId
Aliases: RuleResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4042-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d4042-133">-Confirm</span></span>
<span data-ttu-id="d4042-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d4042-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4042-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4042-135">-WhatIf</span></span>
<span data-ttu-id="d4042-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d4042-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4042-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d4042-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4042-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4042-138">CommonParameters</span></span>
<span data-ttu-id="d4042-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4042-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4042-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d4042-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4042-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d4042-141">INPUTS</span></span>

### <span data-ttu-id="d4042-142">System.String</span><span class="sxs-lookup"><span data-stu-id="d4042-142">System.String</span></span>

### <span data-ttu-id="d4042-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="d4042-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span></span>

## <span data-ttu-id="d4042-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d4042-144">OUTPUTS</span></span>

### <span data-ttu-id="d4042-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d4042-145">System.Boolean</span></span>

## <span data-ttu-id="d4042-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d4042-146">NOTES</span></span>

## <span data-ttu-id="d4042-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d4042-147">RELATED LINKS</span></span>
