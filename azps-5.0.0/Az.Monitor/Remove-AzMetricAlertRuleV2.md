---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azmetricalertrulev2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzMetricAlertRuleV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzMetricAlertRuleV2.md
ms.openlocfilehash: d2b34063f5ece370d52b8a4c3c0dab35cff77c54
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195612"
---
# <span data-ttu-id="48251-101">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="48251-101">Remove-AzMetricAlertRuleV2</span></span>

## <span data-ttu-id="48251-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="48251-102">SYNOPSIS</span></span>
<span data-ttu-id="48251-103">A v2 (nem klasszikus) metrikus figyelmeztetési szabály eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="48251-103">Removes a V2 (non-classic) metric alert rule.</span></span>

## <span data-ttu-id="48251-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="48251-104">SYNTAX</span></span>

### <span data-ttu-id="48251-105">ByMetricRuleResourceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="48251-105">ByMetricRuleResourceName (Default)</span></span>
```
Remove-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48251-106">ByMetricRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="48251-106">ByMetricRuleResourceId</span></span>
```
Remove-AzMetricAlertRuleV2 -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48251-107">ByRuleObject</span><span class="sxs-lookup"><span data-stu-id="48251-107">ByRuleObject</span></span>
```
Remove-AzMetricAlertRuleV2 -InputObject <PSMetricAlertRuleV2> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48251-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="48251-108">DESCRIPTION</span></span>
<span data-ttu-id="48251-109">A **Remove-AzMetricAlertRuleV2** parancsmag eltávolít egy figyelmeztetési szabályt.</span><span class="sxs-lookup"><span data-stu-id="48251-109">The **Remove-AzMetricAlertRuleV2** cmdlet removes an alert rule.</span></span> <span data-ttu-id="48251-110">Ez a parancsmag végrehajtja a ShouldProcess mintát, azaz a felhasználó megerősítését kérheti az erőforrás tényleges létrehozása, módosítása vagy eltávolítása előtt.</span><span class="sxs-lookup"><span data-stu-id="48251-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="48251-111">Példák</span><span class="sxs-lookup"><span data-stu-id="48251-111">EXAMPLES</span></span>

### <span data-ttu-id="48251-112">1. példa: figyelmeztetési szabály eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="48251-112">Example 1: Remove an alert rule by name</span></span>

```powershell
PS C:\> Remove-AzMetricAlertRuleV2 -ResourceGroupName xxxxRG -Name PsSdk -PassThru
True
```

<span data-ttu-id="48251-113">Ez a parancs eltávolítja a PsSdk nevű riasztási szabályt.</span><span class="sxs-lookup"><span data-stu-id="48251-113">This command removes the alert rule named PsSdk</span></span>

### <span data-ttu-id="48251-114">2. példa: figyelmeztetési szabály eltávolítása AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="48251-114">Example 2: Remove an alert rule by ID</span></span>

```powershell
PS C:\>Remove-AzMetricAlertRuleV2 -ResourceId /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertRG/providers/microsoft.insights/metricAlerts/myAlertRule
```

<span data-ttu-id="48251-115">Ez a parancs eltávolítja az erőforrás-AZONOSÍTÓval rendelkező figyelmeztetési szabályt. `/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertRG/providers/microsoft.insights/metricAlerts/myAlertRule`</span><span class="sxs-lookup"><span data-stu-id="48251-115">This command removes the alert rule with resource ID `/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertRG/providers/microsoft.insights/metricAlerts/myAlertRule`</span></span>

### <span data-ttu-id="48251-116">3. példa: értesítés kérése és eltávolítása</span><span class="sxs-lookup"><span data-stu-id="48251-116">Example 3: Get an alert and remove it</span></span>

```powershell
PS c:\>Get-AzMetricAlertRuleV2 -ResourceGroupName alertstest -Name sampleAlertRule |Remove-AzMetricAlertRuleV2
```

<span data-ttu-id="48251-117">Ez a parancs riasztást kap, és eltávolítja azt.</span><span class="sxs-lookup"><span data-stu-id="48251-117">This command gets an alert and removes it.</span></span>

## <span data-ttu-id="48251-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="48251-118">PARAMETERS</span></span>

### <span data-ttu-id="48251-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="48251-119">-AsJob</span></span>
<span data-ttu-id="48251-120">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="48251-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="48251-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48251-121">-DefaultProfile</span></span>
<span data-ttu-id="48251-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="48251-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48251-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="48251-123">-InputObject</span></span>
<span data-ttu-id="48251-124">A metrikus szabály objektum</span><span class="sxs-lookup"><span data-stu-id="48251-124">The Metric rule object</span></span>

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

### <span data-ttu-id="48251-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="48251-125">-Name</span></span>
<span data-ttu-id="48251-126">A metrikus figyelmeztetési szabály neve</span><span class="sxs-lookup"><span data-stu-id="48251-126">The name of metric alert rule</span></span>

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

### <span data-ttu-id="48251-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="48251-127">-PassThru</span></span>
<span data-ttu-id="48251-128">Sikeres törlés esetén igaz értéket ad vissza.</span><span class="sxs-lookup"><span data-stu-id="48251-128">Return true upon successful deletion.</span></span>

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

### <span data-ttu-id="48251-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48251-129">-ResourceGroupName</span></span>
<span data-ttu-id="48251-130">A ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48251-130">The ResourceGroupName</span></span>

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

### <span data-ttu-id="48251-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="48251-131">-ResourceId</span></span>
<span data-ttu-id="48251-132">A RuleResourceId</span><span class="sxs-lookup"><span data-stu-id="48251-132">The RuleResourceId</span></span>

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

### <span data-ttu-id="48251-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="48251-133">-Confirm</span></span>
<span data-ttu-id="48251-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="48251-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48251-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48251-135">-WhatIf</span></span>
<span data-ttu-id="48251-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="48251-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48251-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="48251-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48251-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48251-138">CommonParameters</span></span>
<span data-ttu-id="48251-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="48251-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48251-140">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="48251-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48251-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="48251-141">INPUTS</span></span>

### <span data-ttu-id="48251-142">System. String</span><span class="sxs-lookup"><span data-stu-id="48251-142">System.String</span></span>

### <span data-ttu-id="48251-143">Microsoft. Azure. commands. OutputClasses. PSMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="48251-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span></span>

## <span data-ttu-id="48251-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="48251-144">OUTPUTS</span></span>

### <span data-ttu-id="48251-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="48251-145">System.Boolean</span></span>

## <span data-ttu-id="48251-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="48251-146">NOTES</span></span>

## <span data-ttu-id="48251-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="48251-147">RELATED LINKS</span></span>
