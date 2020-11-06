---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: FBAE5F75-1E28-4F1C-A9ED-20075FFD4AC7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmWebtestAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmWebtestAlertRule.md
ms.openlocfilehash: 52b3d39aef4c117fe8b26bb35f1bf50143e5fec5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504951"
---
# <span data-ttu-id="c4951-101">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="c4951-101">Add-AzureRmWebtestAlertRule</span></span>

## <span data-ttu-id="c4951-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c4951-102">SYNOPSIS</span></span>
<span data-ttu-id="c4951-103">Webteszt figyelmeztetési szabály hozzáadása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="c4951-103">Adds or updates a webtest alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4951-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c4951-104">SYNTAX</span></span>

```
Add-AzureRmWebtestAlertRule -MetricName <String> -TargetResourceUri <String> -WindowSize <TimeSpan>
 -FailedLocationCount <Int32> [-MetricNamespace <String>] -Location <String> [-Description <String>]
 [-DisableRule] -ResourceGroup <String> -Name <String>
 [-Actions <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4951-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c4951-105">DESCRIPTION</span></span>
<span data-ttu-id="c4951-106">Az **Add-AzureRmWebtestAlertRule** parancsmag metrikát, eseményt vagy webteszt típust ad hozzá vagy frissít egy figyelmeztetési szabályhoz.</span><span class="sxs-lookup"><span data-stu-id="c4951-106">The **Add-AzureRmWebtestAlertRule** cmdlet adds or updates an alert rule of either metric, event, or webtest type.</span></span>
<span data-ttu-id="c4951-107">A hozzáadott szabály erőforrás-csoporthoz van társítva, és nevet tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="c4951-107">The added rule is associated to a resource group and has a name.</span></span>

## <span data-ttu-id="c4951-108">Példák</span><span class="sxs-lookup"><span data-stu-id="c4951-108">EXAMPLES</span></span>

### <span data-ttu-id="c4951-109">Példa 1: webteszt figyelmeztetési szabály hozzáadása</span><span class="sxs-lookup"><span data-stu-id="c4951-109">Example 1: Add a webtest alert rule</span></span>
```
PS C:\>Add-AzureRmWebtestAlertRule -Name "webtestRule" -Location "East US" -ResourceGroup "Default-Web-EastUS" -WindowSize 00:05:00 -MetricName "metric" -TargetResourceUri ":/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourcegroups/Default-Web-WestUS/providers/microsoft.insights/webtests/leowebtestr1-webtestr1" -Description "Nice Webtest rule" -Failed 3
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="c4951-110">Ez a parancs webteszt-figyelmeztetési szabályt ad hozzá vagy frissít.</span><span class="sxs-lookup"><span data-stu-id="c4951-110">This command adds or updates a webtest alert rule.</span></span>

## <span data-ttu-id="c4951-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c4951-111">PARAMETERS</span></span>

### <span data-ttu-id="c4951-112">-Műveletek</span><span class="sxs-lookup"><span data-stu-id="c4951-112">-Actions</span></span>
<span data-ttu-id="c4951-113">A műveletek vesszővel elválasztott listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c4951-113">Specifies a comma-separated list of actions.</span></span>

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

### <span data-ttu-id="c4951-114">-Leírás</span><span class="sxs-lookup"><span data-stu-id="c4951-114">-Description</span></span>
<span data-ttu-id="c4951-115">A szabály leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="c4951-115">Specifies a description of the rule.</span></span>

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

### <span data-ttu-id="c4951-116">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="c4951-116">-DisableRule</span></span>
<span data-ttu-id="c4951-117">Letiltja a szabályt.</span><span class="sxs-lookup"><span data-stu-id="c4951-117">Disables the rule.</span></span>
<span data-ttu-id="c4951-118">Ha nem adja meg ezt a paramétert, a szabály engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="c4951-118">If you do not specify this parameter, the rule is enabled.</span></span>

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

### <span data-ttu-id="c4951-119">-FailedLocationCount</span><span class="sxs-lookup"><span data-stu-id="c4951-119">-FailedLocationCount</span></span>
<span data-ttu-id="c4951-120">A webteszt szabályok sikertelen helyének számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="c4951-120">Specifies the failed location count for the webtest rules.</span></span>
<span data-ttu-id="c4951-121">Ez hasonló a más típusú szabályokban szereplő küszöbértékhez.</span><span class="sxs-lookup"><span data-stu-id="c4951-121">This is similar to the threshold in the other types of rules.</span></span>

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

### <span data-ttu-id="c4951-122">-Hely</span><span class="sxs-lookup"><span data-stu-id="c4951-122">-Location</span></span>
<span data-ttu-id="c4951-123">A szabály helyének meghatározása.</span><span class="sxs-lookup"><span data-stu-id="c4951-123">Specifies the location where the rule is defined.</span></span>

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

### <span data-ttu-id="c4951-124">-MetricName</span><span class="sxs-lookup"><span data-stu-id="c4951-124">-MetricName</span></span>
<span data-ttu-id="c4951-125">A metrika nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c4951-125">Specifies the name of the metric.</span></span>

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

### <span data-ttu-id="c4951-126">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="c4951-126">-MetricNamespace</span></span>
<span data-ttu-id="c4951-127">A szabály metrikus névterét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c4951-127">Specifies the metric namespace for rule.</span></span>

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

### <span data-ttu-id="c4951-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c4951-128">-Name</span></span>
<span data-ttu-id="c4951-129">A szabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c4951-129">Specifies the name of the rule.</span></span>

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

### <span data-ttu-id="c4951-130">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c4951-130">-ResourceGroup</span></span>
<span data-ttu-id="c4951-131">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c4951-131">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="c4951-132">-TargetResourceUri</span><span class="sxs-lookup"><span data-stu-id="c4951-132">-TargetResourceUri</span></span>
<span data-ttu-id="c4951-133">A webteszt erőforrás-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c4951-133">Specifies the resource ID of the webtest.</span></span>

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

### <span data-ttu-id="c4951-134">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="c4951-134">-WindowSize</span></span>
<span data-ttu-id="c4951-135">A szabály időablakának méretét adja meg az adatainak számításához.</span><span class="sxs-lookup"><span data-stu-id="c4951-135">Specifies the time window size for the rule to compute its data.</span></span>

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

### <span data-ttu-id="c4951-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4951-136">-DefaultProfile</span></span>
<span data-ttu-id="c4951-137">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c4951-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4951-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4951-138">CommonParameters</span></span>
<span data-ttu-id="c4951-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c4951-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4951-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4951-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4951-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c4951-141">INPUTS</span></span>

## <span data-ttu-id="c4951-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c4951-142">OUTPUTS</span></span>

### <span data-ttu-id="c4951-143">Microsoft. Azure. commands. OutputClasses. PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="c4951-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="c4951-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c4951-144">NOTES</span></span>

## <span data-ttu-id="c4951-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c4951-145">RELATED LINKS</span></span>

[<span data-ttu-id="c4951-146">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="c4951-146">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="c4951-147">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="c4951-147">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="c4951-148">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="c4951-148">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="c4951-149">Új – AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="c4951-149">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)


