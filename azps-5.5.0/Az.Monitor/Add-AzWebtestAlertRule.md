---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: FBAE5F75-1E28-4F1C-A9ED-20075FFD4AC7
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azwebtestalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzWebtestAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzWebtestAlertRule.md
ms.openlocfilehash: 043bb0e0b3c5fac61407eaca3d20c82ebe483037
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203544"
---
# <span data-ttu-id="e285b-101">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="e285b-101">Add-AzWebtestAlertRule</span></span>

## <span data-ttu-id="e285b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e285b-102">SYNOPSIS</span></span>
<span data-ttu-id="e285b-103">Webtesztriasztás szabály hozzáadása vagy frissítése.</span><span class="sxs-lookup"><span data-stu-id="e285b-103">Adds or updates a webtest alert rule.</span></span>

## <span data-ttu-id="e285b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e285b-104">SYNTAX</span></span>

```
Add-AzWebtestAlertRule -MetricName <String> -TargetResourceUri <String> -WindowSize <TimeSpan>
 -FailedLocationCount <Int32> [-MetricNamespace <String>] -Location <String> [-Description <String>]
 [-DisableRule] -ResourceGroupName <String> -Name <String>
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e285b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e285b-105">DESCRIPTION</span></span>
<span data-ttu-id="e285b-106">Az **Add-AzWebtestAlertRule** parancsmag hozzáad vagy frissíti a metrikus, esemény- vagy webteszttípusú riasztási szabályt.</span><span class="sxs-lookup"><span data-stu-id="e285b-106">The **Add-AzWebtestAlertRule** cmdlet adds or updates an alert rule of either metric, event, or webtest type.</span></span>
<span data-ttu-id="e285b-107">A hozzáadott szabály egy erőforráscsoporthoz van társítva, és neve is van.</span><span class="sxs-lookup"><span data-stu-id="e285b-107">The added rule is associated to a resource group and has a name.</span></span>
<span data-ttu-id="e285b-108">Ez a parancsmag implementálja a ShouldProcess mintát, azaz megerősítést kérhet a felhasználótól, mielőtt ténylegesen létrehozza, módosítja vagy eltávolítja az erőforrást.</span><span class="sxs-lookup"><span data-stu-id="e285b-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="e285b-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e285b-109">EXAMPLES</span></span>

### <span data-ttu-id="e285b-110">1. példa: Webtest riasztási szabály hozzáadása</span><span class="sxs-lookup"><span data-stu-id="e285b-110">Example 1: Add a webtest alert rule</span></span>
```
PS C:\>Add-AzWebtestAlertRule -Name "webtestRule" -Location "East US" -ResourceGroup "Default-Web-EastUS" -WindowSize 00:05:00 -MetricName "metric" -TargetResourceUri "/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourcegroups/Default-Web-WestUS/providers/microsoft.insights/webtests/leowebtestr1-webtestr1" -Description "Nice Webtest rule" -Failed 3
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="e285b-111">Ez a parancs webteszt-riasztási szabályt ad hozzá vagy frissíti.</span><span class="sxs-lookup"><span data-stu-id="e285b-111">This command adds or updates a webtest alert rule.</span></span>

## <span data-ttu-id="e285b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e285b-112">PARAMETERS</span></span>

### <span data-ttu-id="e285b-113">-Action</span><span class="sxs-lookup"><span data-stu-id="e285b-113">-Action</span></span>
<span data-ttu-id="e285b-114">Vesszővel elválasztott műveletlistát ad meg.</span><span class="sxs-lookup"><span data-stu-id="e285b-114">Specifies a comma-separated list of actions.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e285b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e285b-115">-DefaultProfile</span></span>
<span data-ttu-id="e285b-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e285b-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e285b-117">-Leírás</span><span class="sxs-lookup"><span data-stu-id="e285b-117">-Description</span></span>
<span data-ttu-id="e285b-118">Megadja a szabály leírását.</span><span class="sxs-lookup"><span data-stu-id="e285b-118">Specifies a description of the rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e285b-119">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="e285b-119">-DisableRule</span></span>
<span data-ttu-id="e285b-120">Letiltja a szabályt.</span><span class="sxs-lookup"><span data-stu-id="e285b-120">Disables the rule.</span></span>
<span data-ttu-id="e285b-121">Ha nem adja meg ezt a paramétert, a szabály engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="e285b-121">If you do not specify this parameter, the rule is enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e285b-122">-FailedLocationCount</span><span class="sxs-lookup"><span data-stu-id="e285b-122">-FailedLocationCount</span></span>
<span data-ttu-id="e285b-123">A webtesztszabályok sikertelen helyszámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e285b-123">Specifies the failed location count for the webtest rules.</span></span>
<span data-ttu-id="e285b-124">Ez a többi szabálytípus küszöbértéke.</span><span class="sxs-lookup"><span data-stu-id="e285b-124">This is similar to the threshold in the other types of rules.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e285b-125">-Location</span><span class="sxs-lookup"><span data-stu-id="e285b-125">-Location</span></span>
<span data-ttu-id="e285b-126">Megadja azt a helyet, ahol a szabály definiálva van.</span><span class="sxs-lookup"><span data-stu-id="e285b-126">Specifies the location where the rule is defined.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e285b-127">-MetricName</span><span class="sxs-lookup"><span data-stu-id="e285b-127">-MetricName</span></span>
<span data-ttu-id="e285b-128">A metrika nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e285b-128">Specifies the name of the metric.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e285b-129">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="e285b-129">-MetricNamespace</span></span>
<span data-ttu-id="e285b-130">A szabály metrikus névterét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e285b-130">Specifies the metric namespace for rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e285b-131">-Name</span><span class="sxs-lookup"><span data-stu-id="e285b-131">-Name</span></span>
<span data-ttu-id="e285b-132">A szabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e285b-132">Specifies the name of the rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e285b-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e285b-133">-ResourceGroupName</span></span>
<span data-ttu-id="e285b-134">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e285b-134">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e285b-135">-TargetResourceUri</span><span class="sxs-lookup"><span data-stu-id="e285b-135">-TargetResourceUri</span></span>
<span data-ttu-id="e285b-136">A webteszt erőforrás-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e285b-136">Specifies the resource ID of the webtest.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e285b-137">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="e285b-137">-WindowSize</span></span>
<span data-ttu-id="e285b-138">Megadja, hogy a szabály milyen időkeretet számolja ki az adatokkal.</span><span class="sxs-lookup"><span data-stu-id="e285b-138">Specifies the time window size for the rule to compute its data.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e285b-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e285b-139">-Confirm</span></span>
<span data-ttu-id="e285b-140">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e285b-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e285b-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e285b-141">-WhatIf</span></span>
<span data-ttu-id="e285b-142">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e285b-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e285b-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e285b-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e285b-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e285b-144">CommonParameters</span></span>
<span data-ttu-id="e285b-145">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e285b-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e285b-146">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e285b-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e285b-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e285b-147">INPUTS</span></span>

### <span data-ttu-id="e285b-148">System.String</span><span class="sxs-lookup"><span data-stu-id="e285b-148">System.String</span></span>

### <span data-ttu-id="e285b-149">System.TimeSpan</span><span class="sxs-lookup"><span data-stu-id="e285b-149">System.TimeSpan</span></span>

### <span data-ttu-id="e285b-150">System.Int32</span><span class="sxs-lookup"><span data-stu-id="e285b-150">System.Int32</span></span>

### <span data-ttu-id="e285b-151">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e285b-151">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="e285b-152">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="e285b-152">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="e285b-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e285b-153">OUTPUTS</span></span>

### <span data-ttu-id="e285b-154">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="e285b-154">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="e285b-155">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e285b-155">NOTES</span></span>

## <span data-ttu-id="e285b-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e285b-156">RELATED LINKS</span></span>

[<span data-ttu-id="e285b-157">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e285b-157">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="e285b-158">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="e285b-158">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="e285b-159">Get-AzAlertHistory</span><span class="sxs-lookup"><span data-stu-id="e285b-159">Get-AzAlertHistory</span></span>](./Get-AzAlertHistory.md)

[<span data-ttu-id="e285b-160">New-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="e285b-160">New-AzAlertRuleWebhook</span></span>](./New-AzAlertRuleWebhook.md)


