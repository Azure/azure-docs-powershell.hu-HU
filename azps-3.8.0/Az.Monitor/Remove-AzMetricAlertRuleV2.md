---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azmetricalertrulev2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzMetricAlertRuleV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzMetricAlertRuleV2.md
ms.openlocfilehash: d2b34063f5ece370d52b8a4c3c0dab35cff77c54
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845106"
---
# <span data-ttu-id="40e20-101">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="40e20-101">Remove-AzMetricAlertRuleV2</span></span>

## <span data-ttu-id="40e20-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="40e20-102">SYNOPSIS</span></span>
<span data-ttu-id="40e20-103">A v2 (nem klasszikus) metrikus figyelmeztetési szabály eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="40e20-103">Removes a V2 (non-classic) metric alert rule.</span></span>

## <span data-ttu-id="40e20-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="40e20-104">SYNTAX</span></span>

### <span data-ttu-id="40e20-105">ByMetricRuleResourceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="40e20-105">ByMetricRuleResourceName (Default)</span></span>
```
Remove-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40e20-106">ByMetricRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="40e20-106">ByMetricRuleResourceId</span></span>
```
Remove-AzMetricAlertRuleV2 -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40e20-107">ByRuleObject</span><span class="sxs-lookup"><span data-stu-id="40e20-107">ByRuleObject</span></span>
```
Remove-AzMetricAlertRuleV2 -InputObject <PSMetricAlertRuleV2> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40e20-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="40e20-108">DESCRIPTION</span></span>
<span data-ttu-id="40e20-109">A **Remove-AzMetricAlertRuleV2** parancsmag eltávolít egy figyelmeztetési szabályt.</span><span class="sxs-lookup"><span data-stu-id="40e20-109">The **Remove-AzMetricAlertRuleV2** cmdlet removes an alert rule.</span></span> <span data-ttu-id="40e20-110">Ez a parancsmag végrehajtja a ShouldProcess mintát, azaz a felhasználó megerősítését kérheti az erőforrás tényleges létrehozása, módosítása vagy eltávolítása előtt.</span><span class="sxs-lookup"><span data-stu-id="40e20-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="40e20-111">Példák</span><span class="sxs-lookup"><span data-stu-id="40e20-111">EXAMPLES</span></span>

### <span data-ttu-id="40e20-112">1. példa: figyelmeztetési szabály eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="40e20-112">Example 1: Remove an alert rule by name</span></span>

```powershell
PS C:\> Remove-AzMetricAlertRuleV2 -ResourceGroupName xxxxRG -Name PsSdk -PassThru
True
```

<span data-ttu-id="40e20-113">Ez a parancs eltávolítja a PsSdk nevű riasztási szabályt.</span><span class="sxs-lookup"><span data-stu-id="40e20-113">This command removes the alert rule named PsSdk</span></span>

### <span data-ttu-id="40e20-114">2. példa: figyelmeztetési szabály eltávolítása AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="40e20-114">Example 2: Remove an alert rule by ID</span></span>

```powershell
PS C:\>Remove-AzMetricAlertRuleV2 -ResourceId /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertRG/providers/microsoft.insights/metricAlerts/myAlertRule
```

<span data-ttu-id="40e20-115">Ez a parancs eltávolítja az erőforrás-AZONOSÍTÓval rendelkező figyelmeztetési szabályt. `/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertRG/providers/microsoft.insights/metricAlerts/myAlertRule`</span><span class="sxs-lookup"><span data-stu-id="40e20-115">This command removes the alert rule with resource ID `/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertRG/providers/microsoft.insights/metricAlerts/myAlertRule`</span></span>

### <span data-ttu-id="40e20-116">3. példa: értesítés kérése és eltávolítása</span><span class="sxs-lookup"><span data-stu-id="40e20-116">Example 3: Get an alert and remove it</span></span>

```powershell
PS c:\>Get-AzMetricAlertRuleV2 -ResourceGroupName alertstest -Name sampleAlertRule |Remove-AzMetricAlertRuleV2
```

<span data-ttu-id="40e20-117">Ez a parancs riasztást kap, és eltávolítja azt.</span><span class="sxs-lookup"><span data-stu-id="40e20-117">This command gets an alert and removes it.</span></span>

## <span data-ttu-id="40e20-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="40e20-118">PARAMETERS</span></span>

### <span data-ttu-id="40e20-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="40e20-119">-AsJob</span></span>
<span data-ttu-id="40e20-120">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="40e20-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="40e20-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40e20-121">-DefaultProfile</span></span>
<span data-ttu-id="40e20-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="40e20-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40e20-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="40e20-123">-InputObject</span></span>
<span data-ttu-id="40e20-124">A metrikus szabály objektum</span><span class="sxs-lookup"><span data-stu-id="40e20-124">The Metric rule object</span></span>

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

### <span data-ttu-id="40e20-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="40e20-125">-Name</span></span>
<span data-ttu-id="40e20-126">A metrikus figyelmeztetési szabály neve</span><span class="sxs-lookup"><span data-stu-id="40e20-126">The name of metric alert rule</span></span>

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

### <span data-ttu-id="40e20-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="40e20-127">-PassThru</span></span>
<span data-ttu-id="40e20-128">Sikeres törlés esetén igaz értéket ad vissza.</span><span class="sxs-lookup"><span data-stu-id="40e20-128">Return true upon successful deletion.</span></span>

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

### <span data-ttu-id="40e20-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40e20-129">-ResourceGroupName</span></span>
<span data-ttu-id="40e20-130">A ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40e20-130">The ResourceGroupName</span></span>

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

### <span data-ttu-id="40e20-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="40e20-131">-ResourceId</span></span>
<span data-ttu-id="40e20-132">A RuleResourceId</span><span class="sxs-lookup"><span data-stu-id="40e20-132">The RuleResourceId</span></span>

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

### <span data-ttu-id="40e20-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="40e20-133">-Confirm</span></span>
<span data-ttu-id="40e20-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="40e20-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40e20-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40e20-135">-WhatIf</span></span>
<span data-ttu-id="40e20-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="40e20-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40e20-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="40e20-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40e20-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40e20-138">CommonParameters</span></span>
<span data-ttu-id="40e20-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="40e20-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40e20-140">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="40e20-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40e20-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="40e20-141">INPUTS</span></span>

### <span data-ttu-id="40e20-142">System. String</span><span class="sxs-lookup"><span data-stu-id="40e20-142">System.String</span></span>

### <span data-ttu-id="40e20-143">Microsoft. Azure. commands. OutputClasses. PSMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="40e20-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span></span>

## <span data-ttu-id="40e20-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="40e20-144">OUTPUTS</span></span>

### <span data-ttu-id="40e20-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="40e20-145">System.Boolean</span></span>

## <span data-ttu-id="40e20-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="40e20-146">NOTES</span></span>

## <span data-ttu-id="40e20-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="40e20-147">RELATED LINKS</span></span>
