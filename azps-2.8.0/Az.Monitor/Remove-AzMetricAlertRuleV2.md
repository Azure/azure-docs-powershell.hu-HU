---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azmetricalertrulev2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzMetricAlertRuleV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzMetricAlertRuleV2.md
ms.openlocfilehash: 4a5863573b207d3c1319b48f6ca00ab11a7b56a4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837736"
---
# <span data-ttu-id="ab484-101">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="ab484-101">Remove-AzMetricAlertRuleV2</span></span>

## <span data-ttu-id="ab484-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ab484-102">SYNOPSIS</span></span>
<span data-ttu-id="ab484-103">A v2 (nem klasszikus) metrikus figyelmeztetési szabály eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="ab484-103">Removes a V2 (non-classic) metric alert rule.</span></span>

## <span data-ttu-id="ab484-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ab484-104">SYNTAX</span></span>

### <span data-ttu-id="ab484-105">ByMetricRuleResourceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ab484-105">ByMetricRuleResourceName (Default)</span></span>
```
Remove-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab484-106">ByMetricRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="ab484-106">ByMetricRuleResourceId</span></span>
```
Remove-AzMetricAlertRuleV2 -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab484-107">ByRuleObject</span><span class="sxs-lookup"><span data-stu-id="ab484-107">ByRuleObject</span></span>
```
Remove-AzMetricAlertRuleV2 -InputObject <PSMetricAlertRuleV2> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab484-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ab484-108">DESCRIPTION</span></span>
<span data-ttu-id="ab484-109">A **Remove-AzMetricAlertRuleV2** parancsmag eltávolít egy figyelmeztetési szabályt.</span><span class="sxs-lookup"><span data-stu-id="ab484-109">The **Remove-AzMetricAlertRuleV2** cmdlet removes an alert rule.</span></span> <span data-ttu-id="ab484-110">Ez a parancsmag végrehajtja a ShouldProcess mintát, azaz a felhasználó megerősítését kérheti az erőforrás tényleges létrehozása, módosítása vagy eltávolítása előtt.</span><span class="sxs-lookup"><span data-stu-id="ab484-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="ab484-111">Példák</span><span class="sxs-lookup"><span data-stu-id="ab484-111">EXAMPLES</span></span>

### <span data-ttu-id="ab484-112">1. példa: figyelmeztetési szabály eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="ab484-112">Example 1: Remove an alert rule by name</span></span>

```powershell
PS C:\> Remove-AzMetricAlertRuleV2 -ResourceGroupName xxxxRG -Name PsSdk -PassThru
True
```

<span data-ttu-id="ab484-113">Ez a parancs eltávolítja a PsSdk nevű riasztási szabályt.</span><span class="sxs-lookup"><span data-stu-id="ab484-113">This command removes the alert rule named PsSdk</span></span>

### <span data-ttu-id="ab484-114">2. példa: figyelmeztetési szabály eltávolítása AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="ab484-114">Example 2: Remove an alert rule by ID</span></span>

```powershell
PS C:\>Remove-AzMetricAlertRuleV2 -ResourceId /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertRG/providers/microsoft.insights/metricAlerts/myAlertRule
```

<span data-ttu-id="ab484-115">Ez a parancs eltávolítja az erőforrás-AZONOSÍTÓval rendelkező figyelmeztetési szabályt. `/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertRG/providers/microsoft.insights/metricAlerts/myAlertRule`</span><span class="sxs-lookup"><span data-stu-id="ab484-115">This command removes the alert rule with resource ID `/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertRG/providers/microsoft.insights/metricAlerts/myAlertRule`</span></span>

### <span data-ttu-id="ab484-116">3. példa: értesítés kérése és eltávolítása</span><span class="sxs-lookup"><span data-stu-id="ab484-116">Example 3: Get an alert and remove it</span></span>

```powershell
PS c:\>Get-AzMetricAlertRuleV2 -ResourceGroupName alertstest -Name sampleAlertRule |Remove-AzMetricAlertRuleV2
```

<span data-ttu-id="ab484-117">Ez a parancs riasztást kap, és eltávolítja azt.</span><span class="sxs-lookup"><span data-stu-id="ab484-117">This command gets an alert and removes it.</span></span>

## <span data-ttu-id="ab484-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ab484-118">PARAMETERS</span></span>

### <span data-ttu-id="ab484-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ab484-119">-AsJob</span></span>
<span data-ttu-id="ab484-120">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="ab484-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ab484-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab484-121">-DefaultProfile</span></span>
<span data-ttu-id="ab484-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ab484-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab484-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ab484-123">-InputObject</span></span>
<span data-ttu-id="ab484-124">A metrikus szabály objektum</span><span class="sxs-lookup"><span data-stu-id="ab484-124">The Metric rule object</span></span>

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

### <span data-ttu-id="ab484-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ab484-125">-Name</span></span>
<span data-ttu-id="ab484-126">A metrikus figyelmeztetési szabály neve</span><span class="sxs-lookup"><span data-stu-id="ab484-126">The name of metric alert rule</span></span>

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

### <span data-ttu-id="ab484-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ab484-127">-PassThru</span></span>
<span data-ttu-id="ab484-128">Sikeres törlés esetén igaz értéket ad vissza.</span><span class="sxs-lookup"><span data-stu-id="ab484-128">Return true upon successful deletion.</span></span>

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

### <span data-ttu-id="ab484-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab484-129">-ResourceGroupName</span></span>
<span data-ttu-id="ab484-130">A ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab484-130">The ResourceGroupName</span></span>

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

### <span data-ttu-id="ab484-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ab484-131">-ResourceId</span></span>
<span data-ttu-id="ab484-132">A RuleResourceId</span><span class="sxs-lookup"><span data-stu-id="ab484-132">The RuleResourceId</span></span>

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

### <span data-ttu-id="ab484-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ab484-133">-Confirm</span></span>
<span data-ttu-id="ab484-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ab484-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab484-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab484-135">-WhatIf</span></span>
<span data-ttu-id="ab484-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ab484-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab484-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ab484-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab484-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab484-138">CommonParameters</span></span>
<span data-ttu-id="ab484-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ab484-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab484-140">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ab484-140">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab484-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab484-141">INPUTS</span></span>

### <span data-ttu-id="ab484-142">System. String</span><span class="sxs-lookup"><span data-stu-id="ab484-142">System.String</span></span>

### <span data-ttu-id="ab484-143">Microsoft. Azure. commands. OutputClasses. PSMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="ab484-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span></span>

## <span data-ttu-id="ab484-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab484-144">OUTPUTS</span></span>

### <span data-ttu-id="ab484-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ab484-145">System.Boolean</span></span>

## <span data-ttu-id="ab484-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ab484-146">NOTES</span></span>

## <span data-ttu-id="ab484-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ab484-147">RELATED LINKS</span></span>
