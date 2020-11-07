---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: FBAE5F75-1E28-4F1C-A9ED-20075FFD4AC7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/add-azurermwebtestalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmWebtestAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmWebtestAlertRule.md
ms.openlocfilehash: 08d84c1f5e71c18a47e48bda1e39ce37ed0cb026
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672726"
---
# <span data-ttu-id="ae3fb-101">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="ae3fb-101">Add-AzureRmWebtestAlertRule</span></span>

## <span data-ttu-id="ae3fb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ae3fb-102">SYNOPSIS</span></span>
<span data-ttu-id="ae3fb-103">Webteszt figyelmeztetési szabály hozzáadása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="ae3fb-103">Adds or updates a webtest alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae3fb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ae3fb-104">SYNTAX</span></span>

```
Add-AzureRmWebtestAlertRule -MetricName <String> -TargetResourceUri <String> -WindowSize <TimeSpan>
 -FailedLocationCount <Int32> [-MetricNamespace <String>] -Location <String> [-Description <String>]
 [-DisableRule] -ResourceGroupName <String> -Name <String>
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae3fb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ae3fb-105">DESCRIPTION</span></span>
<span data-ttu-id="ae3fb-106">Az **Add-AzureRmWebtestAlertRule** parancsmag metrikát, eseményt vagy webteszt típust ad hozzá vagy frissít egy figyelmeztetési szabályhoz.</span><span class="sxs-lookup"><span data-stu-id="ae3fb-106">The **Add-AzureRmWebtestAlertRule** cmdlet adds or updates an alert rule of either metric, event, or webtest type.</span></span>
<span data-ttu-id="ae3fb-107">A hozzáadott szabály erőforrás-csoporthoz van társítva, és nevet tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="ae3fb-107">The added rule is associated to a resource group and has a name.</span></span>
<span data-ttu-id="ae3fb-108">Ez a parancsmag végrehajtja a ShouldProcess mintát, azaz a felhasználó megerősítését kérheti az erőforrás tényleges létrehozása, módosítása vagy eltávolítása előtt.</span><span class="sxs-lookup"><span data-stu-id="ae3fb-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="ae3fb-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ae3fb-109">EXAMPLES</span></span>

### <span data-ttu-id="ae3fb-110">Példa 1: webteszt figyelmeztetési szabály hozzáadása</span><span class="sxs-lookup"><span data-stu-id="ae3fb-110">Example 1: Add a webtest alert rule</span></span>
```
PS C:\>Add-AzureRmWebtestAlertRule -Name "webtestRule" -Location "East US" -ResourceGroup "Default-Web-EastUS" -WindowSize 00:05:00 -MetricName "metric" -TargetResourceUri ":/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourcegroups/Default-Web-WestUS/providers/microsoft.insights/webtests/leowebtestr1-webtestr1" -Description "Nice Webtest rule" -Failed 3
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="ae3fb-111">Ez a parancs webteszt-figyelmeztetési szabályt ad hozzá vagy frissít.</span><span class="sxs-lookup"><span data-stu-id="ae3fb-111">This command adds or updates a webtest alert rule.</span></span>

## <span data-ttu-id="ae3fb-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ae3fb-112">PARAMETERS</span></span>

### <span data-ttu-id="ae3fb-113">-Műveletek</span><span class="sxs-lookup"><span data-stu-id="ae3fb-113">-Action</span></span>
<span data-ttu-id="ae3fb-114">A műveletek vesszővel elválasztott listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ae3fb-114">Specifies a comma-separated list of actions.</span></span>

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

### <span data-ttu-id="ae3fb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae3fb-115">-DefaultProfile</span></span>
<span data-ttu-id="ae3fb-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ae3fb-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae3fb-117">-Leírás</span><span class="sxs-lookup"><span data-stu-id="ae3fb-117">-Description</span></span>
<span data-ttu-id="ae3fb-118">A szabály leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="ae3fb-118">Specifies a description of the rule.</span></span>

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

### <span data-ttu-id="ae3fb-119">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="ae3fb-119">-DisableRule</span></span>
<span data-ttu-id="ae3fb-120">Letiltja a szabályt.</span><span class="sxs-lookup"><span data-stu-id="ae3fb-120">Disables the rule.</span></span>
<span data-ttu-id="ae3fb-121">Ha nem adja meg ezt a paramétert, a szabály engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="ae3fb-121">If you do not specify this parameter, the rule is enabled.</span></span>

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

### <span data-ttu-id="ae3fb-122">-FailedLocationCount</span><span class="sxs-lookup"><span data-stu-id="ae3fb-122">-FailedLocationCount</span></span>
<span data-ttu-id="ae3fb-123">A webteszt szabályok sikertelen helyének számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ae3fb-123">Specifies the failed location count for the webtest rules.</span></span>
<span data-ttu-id="ae3fb-124">Ez hasonló a más típusú szabályokban szereplő küszöbértékhez.</span><span class="sxs-lookup"><span data-stu-id="ae3fb-124">This is similar to the threshold in the other types of rules.</span></span>

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

### <span data-ttu-id="ae3fb-125">-Hely</span><span class="sxs-lookup"><span data-stu-id="ae3fb-125">-Location</span></span>
<span data-ttu-id="ae3fb-126">A szabály helyének meghatározása.</span><span class="sxs-lookup"><span data-stu-id="ae3fb-126">Specifies the location where the rule is defined.</span></span>

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

### <span data-ttu-id="ae3fb-127">-MetricName</span><span class="sxs-lookup"><span data-stu-id="ae3fb-127">-MetricName</span></span>
<span data-ttu-id="ae3fb-128">A metrika nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ae3fb-128">Specifies the name of the metric.</span></span>

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

### <span data-ttu-id="ae3fb-129">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="ae3fb-129">-MetricNamespace</span></span>
<span data-ttu-id="ae3fb-130">A szabály metrikus névterét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ae3fb-130">Specifies the metric namespace for rule.</span></span>

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

### <span data-ttu-id="ae3fb-131">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ae3fb-131">-Name</span></span>
<span data-ttu-id="ae3fb-132">A szabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ae3fb-132">Specifies the name of the rule.</span></span>

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

### <span data-ttu-id="ae3fb-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae3fb-133">-ResourceGroupName</span></span>
<span data-ttu-id="ae3fb-134">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ae3fb-134">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="ae3fb-135">-TargetResourceUri</span><span class="sxs-lookup"><span data-stu-id="ae3fb-135">-TargetResourceUri</span></span>
<span data-ttu-id="ae3fb-136">A webteszt erőforrás-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ae3fb-136">Specifies the resource ID of the webtest.</span></span>

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

### <span data-ttu-id="ae3fb-137">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="ae3fb-137">-WindowSize</span></span>
<span data-ttu-id="ae3fb-138">A szabály időablakának méretét adja meg az adatainak számításához.</span><span class="sxs-lookup"><span data-stu-id="ae3fb-138">Specifies the time window size for the rule to compute its data.</span></span>

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

### <span data-ttu-id="ae3fb-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ae3fb-139">-Confirm</span></span>
<span data-ttu-id="ae3fb-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ae3fb-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae3fb-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae3fb-141">-WhatIf</span></span>
<span data-ttu-id="ae3fb-142">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ae3fb-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ae3fb-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ae3fb-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae3fb-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae3fb-144">CommonParameters</span></span>
<span data-ttu-id="ae3fb-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ae3fb-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae3fb-146">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae3fb-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae3fb-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ae3fb-147">INPUTS</span></span>

### <span data-ttu-id="ae3fb-148">System. String</span><span class="sxs-lookup"><span data-stu-id="ae3fb-148">System.String</span></span>

### <span data-ttu-id="ae3fb-149">System. időszak</span><span class="sxs-lookup"><span data-stu-id="ae3fb-149">System.TimeSpan</span></span>

### <span data-ttu-id="ae3fb-150">System. Int32</span><span class="sxs-lookup"><span data-stu-id="ae3fb-150">System.Int32</span></span>

### <span data-ttu-id="ae3fb-151">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ae3fb-151">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="ae3fb-152">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Management. monitor. Management. models. RuleAction, Microsoft. Azure. commands. ininsights, Version = 5.1.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="ae3fb-152">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction, Microsoft.Azure.Commands.Insights, Version=5.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="ae3fb-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ae3fb-153">OUTPUTS</span></span>

### <span data-ttu-id="ae3fb-154">Microsoft. Azure. commands. OutputClasses. PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="ae3fb-154">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="ae3fb-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ae3fb-155">NOTES</span></span>

## <span data-ttu-id="ae3fb-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ae3fb-156">RELATED LINKS</span></span>

[<span data-ttu-id="ae3fb-157">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="ae3fb-157">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="ae3fb-158">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="ae3fb-158">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="ae3fb-159">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="ae3fb-159">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="ae3fb-160">Új – AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="ae3fb-160">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)


