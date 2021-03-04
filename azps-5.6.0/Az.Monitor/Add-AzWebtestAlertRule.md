---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: FBAE5F75-1E28-4F1C-A9ED-20075FFD4AC7
online version: https://docs.microsoft.com/powershell/module/az.monitor/add-azwebtestalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzWebtestAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzWebtestAlertRule.md
ms.openlocfilehash: 8f66117d4ae2909617a6215c1c154ba22d469b21
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932745"
---
# <span data-ttu-id="9f6c4-101">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="9f6c4-101">Add-AzWebtestAlertRule</span></span>

## <span data-ttu-id="9f6c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f6c4-102">SYNOPSIS</span></span>
<span data-ttu-id="9f6c4-103">Webteszt-riasztási szabály hozzáadása vagy frissítése.</span><span class="sxs-lookup"><span data-stu-id="9f6c4-103">Adds or updates a webtest alert rule.</span></span>

## <span data-ttu-id="9f6c4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9f6c4-104">SYNTAX</span></span>

```
Add-AzWebtestAlertRule -MetricName <String> -TargetResourceUri <String> -WindowSize <TimeSpan>
 -FailedLocationCount <Int32> [-MetricNamespace <String>] -Location <String> [-Description <String>]
 [-DisableRule] -ResourceGroupName <String> -Name <String>
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f6c4-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9f6c4-105">DESCRIPTION</span></span>
<span data-ttu-id="9f6c4-106">Az **Add-AzWebtestAlertRule** parancsmag hozzáad vagy frissíti a metrikus, esemény- vagy webteszttípusú riasztási szabályt.</span><span class="sxs-lookup"><span data-stu-id="9f6c4-106">The **Add-AzWebtestAlertRule** cmdlet adds or updates an alert rule of either metric, event, or webtest type.</span></span>
<span data-ttu-id="9f6c4-107">A hozzáadott szabály egy erőforráscsoporthoz van társítva, és neve is van.</span><span class="sxs-lookup"><span data-stu-id="9f6c4-107">The added rule is associated to a resource group and has a name.</span></span>
<span data-ttu-id="9f6c4-108">Ez a parancsmag implementálja a ShouldProcess mintát, azaz megerősítést kérhet a felhasználótól, mielőtt ténylegesen létrehozza, módosítja vagy eltávolítja az erőforrást.</span><span class="sxs-lookup"><span data-stu-id="9f6c4-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="9f6c4-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9f6c4-109">EXAMPLES</span></span>

### <span data-ttu-id="9f6c4-110">1. példa: Webtest riasztási szabály hozzáadása</span><span class="sxs-lookup"><span data-stu-id="9f6c4-110">Example 1: Add a webtest alert rule</span></span>
```
PS C:\>Add-AzWebtestAlertRule -Name "webtestRule" -Location "East US" -ResourceGroup "Default-Web-EastUS" -WindowSize 00:05:00 -MetricName "metric" -TargetResourceUri "/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourcegroups/Default-Web-WestUS/providers/microsoft.insights/webtests/leowebtestr1-webtestr1" -Description "Nice Webtest rule" -Failed 3
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="9f6c4-111">Ez a parancs webteszt-riasztási szabályt ad hozzá vagy frissíti.</span><span class="sxs-lookup"><span data-stu-id="9f6c4-111">This command adds or updates a webtest alert rule.</span></span>

## <span data-ttu-id="9f6c4-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9f6c4-112">PARAMETERS</span></span>

### <span data-ttu-id="9f6c4-113">-Művelet</span><span class="sxs-lookup"><span data-stu-id="9f6c4-113">-Action</span></span>
<span data-ttu-id="9f6c4-114">A műveletek vesszővel elválasztott listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="9f6c4-114">Specifies a comma-separated list of actions.</span></span>

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

### <span data-ttu-id="9f6c4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f6c4-115">-DefaultProfile</span></span>
<span data-ttu-id="9f6c4-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="9f6c4-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9f6c4-117">-Leírás</span><span class="sxs-lookup"><span data-stu-id="9f6c4-117">-Description</span></span>
<span data-ttu-id="9f6c4-118">Megadja a szabály leírását.</span><span class="sxs-lookup"><span data-stu-id="9f6c4-118">Specifies a description of the rule.</span></span>

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

### <span data-ttu-id="9f6c4-119">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="9f6c4-119">-DisableRule</span></span>
<span data-ttu-id="9f6c4-120">Letiltja a szabályt.</span><span class="sxs-lookup"><span data-stu-id="9f6c4-120">Disables the rule.</span></span>
<span data-ttu-id="9f6c4-121">Ha nem adja meg ezt a paramétert, a szabály engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="9f6c4-121">If you do not specify this parameter, the rule is enabled.</span></span>

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

### <span data-ttu-id="9f6c4-122">-FailedLocationCount</span><span class="sxs-lookup"><span data-stu-id="9f6c4-122">-FailedLocationCount</span></span>
<span data-ttu-id="9f6c4-123">A webtesztszabályok sikertelen helyszámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9f6c4-123">Specifies the failed location count for the webtest rules.</span></span>
<span data-ttu-id="9f6c4-124">Ez hasonló a többi szabálytípus küszöbértékének beállításhoz.</span><span class="sxs-lookup"><span data-stu-id="9f6c4-124">This is similar to the threshold in the other types of rules.</span></span>

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

### <span data-ttu-id="9f6c4-125">-Location</span><span class="sxs-lookup"><span data-stu-id="9f6c4-125">-Location</span></span>
<span data-ttu-id="9f6c4-126">Megadja azt a helyet, ahol a szabály definiálva van.</span><span class="sxs-lookup"><span data-stu-id="9f6c4-126">Specifies the location where the rule is defined.</span></span>

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

### <span data-ttu-id="9f6c4-127">-MetricName</span><span class="sxs-lookup"><span data-stu-id="9f6c4-127">-MetricName</span></span>
<span data-ttu-id="9f6c4-128">A metrika nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9f6c4-128">Specifies the name of the metric.</span></span>

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

### <span data-ttu-id="9f6c4-129">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="9f6c4-129">-MetricNamespace</span></span>
<span data-ttu-id="9f6c4-130">A szabály metrikus névterét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9f6c4-130">Specifies the metric namespace for rule.</span></span>

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

### <span data-ttu-id="9f6c4-131">-Name</span><span class="sxs-lookup"><span data-stu-id="9f6c4-131">-Name</span></span>
<span data-ttu-id="9f6c4-132">A szabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9f6c4-132">Specifies the name of the rule.</span></span>

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

### <span data-ttu-id="9f6c4-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f6c4-133">-ResourceGroupName</span></span>
<span data-ttu-id="9f6c4-134">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9f6c4-134">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="9f6c4-135">-TargetResourceUri</span><span class="sxs-lookup"><span data-stu-id="9f6c4-135">-TargetResourceUri</span></span>
<span data-ttu-id="9f6c4-136">A webteszt erőforrás-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="9f6c4-136">Specifies the resource ID of the webtest.</span></span>

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

### <span data-ttu-id="9f6c4-137">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="9f6c4-137">-WindowSize</span></span>
<span data-ttu-id="9f6c4-138">Megadja, hogy a szabály milyen időkeretet számolja ki az adatokkal.</span><span class="sxs-lookup"><span data-stu-id="9f6c4-138">Specifies the time window size for the rule to compute its data.</span></span>

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

### <span data-ttu-id="9f6c4-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9f6c4-139">-Confirm</span></span>
<span data-ttu-id="9f6c4-140">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9f6c4-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f6c4-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f6c4-141">-WhatIf</span></span>
<span data-ttu-id="9f6c4-142">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="9f6c4-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9f6c4-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9f6c4-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f6c4-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f6c4-144">CommonParameters</span></span>
<span data-ttu-id="9f6c4-145">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f6c4-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f6c4-146">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9f6c4-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f6c4-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9f6c4-147">INPUTS</span></span>

### <span data-ttu-id="9f6c4-148">System.String</span><span class="sxs-lookup"><span data-stu-id="9f6c4-148">System.String</span></span>

### <span data-ttu-id="9f6c4-149">System.TimeSpan</span><span class="sxs-lookup"><span data-stu-id="9f6c4-149">System.TimeSpan</span></span>

### <span data-ttu-id="9f6c4-150">System.Int32</span><span class="sxs-lookup"><span data-stu-id="9f6c4-150">System.Int32</span></span>

### <span data-ttu-id="9f6c4-151">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9f6c4-151">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="9f6c4-152">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="9f6c4-152">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="9f6c4-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9f6c4-153">OUTPUTS</span></span>

### <span data-ttu-id="9f6c4-154">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="9f6c4-154">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="9f6c4-155">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9f6c4-155">NOTES</span></span>

## <span data-ttu-id="9f6c4-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9f6c4-156">RELATED LINKS</span></span>

[<span data-ttu-id="9f6c4-157">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="9f6c4-157">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="9f6c4-158">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="9f6c4-158">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="9f6c4-159">Get-AzAlertHistory</span><span class="sxs-lookup"><span data-stu-id="9f6c4-159">Get-AzAlertHistory</span></span>](./Get-AzAlertHistory.md)

[<span data-ttu-id="9f6c4-160">New-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="9f6c4-160">New-AzAlertRuleWebhook</span></span>](./New-AzAlertRuleWebhook.md)


