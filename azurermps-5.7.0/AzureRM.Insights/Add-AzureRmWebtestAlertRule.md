---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: FBAE5F75-1E28-4F1C-A9ED-20075FFD4AC7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/add-azurermwebtestalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmWebtestAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmWebtestAlertRule.md
ms.openlocfilehash: da395b66cb4d63593c097f214701365370e06b75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495349"
---
# <span data-ttu-id="7af80-101">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="7af80-101">Add-AzureRmWebtestAlertRule</span></span>

## <span data-ttu-id="7af80-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7af80-102">SYNOPSIS</span></span>
<span data-ttu-id="7af80-103">Webteszt figyelmeztetési szabály hozzáadása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="7af80-103">Adds or updates a webtest alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7af80-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7af80-104">SYNTAX</span></span>

```
Add-AzureRmWebtestAlertRule -MetricName <String> -TargetResourceUri <String> -WindowSize <TimeSpan>
 -FailedLocationCount <Int32> [-MetricNamespace <String>] -Location <String> [-Description <String>]
 [-DisableRule] -ResourceGroupName <String> -Name <String>
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Insights.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7af80-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7af80-105">DESCRIPTION</span></span>
<span data-ttu-id="7af80-106">Az **Add-AzureRmWebtestAlertRule** parancsmag metrikát, eseményt vagy webteszt típust ad hozzá vagy frissít egy figyelmeztetési szabályhoz.</span><span class="sxs-lookup"><span data-stu-id="7af80-106">The **Add-AzureRmWebtestAlertRule** cmdlet adds or updates an alert rule of either metric, event, or webtest type.</span></span>
<span data-ttu-id="7af80-107">A hozzáadott szabály erőforrás-csoporthoz van társítva, és nevet tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="7af80-107">The added rule is associated to a resource group and has a name.</span></span>
<span data-ttu-id="7af80-108">Ez a parancsmag végrehajtja a ShouldProcess mintát, azaz a felhasználó megerősítését kérheti az erőforrás tényleges létrehozása, módosítása vagy eltávolítása előtt.</span><span class="sxs-lookup"><span data-stu-id="7af80-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="7af80-109">Példák</span><span class="sxs-lookup"><span data-stu-id="7af80-109">EXAMPLES</span></span>

### <span data-ttu-id="7af80-110">Példa 1: webteszt figyelmeztetési szabály hozzáadása</span><span class="sxs-lookup"><span data-stu-id="7af80-110">Example 1: Add a webtest alert rule</span></span>
```
PS C:\>Add-AzureRmWebtestAlertRule -Name "webtestRule" -Location "East US" -ResourceGroup "Default-Web-EastUS" -WindowSize 00:05:00 -MetricName "metric" -TargetResourceUri ":/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourcegroups/Default-Web-WestUS/providers/microsoft.insights/webtests/leowebtestr1-webtestr1" -Description "Nice Webtest rule" -Failed 3
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="7af80-111">Ez a parancs webteszt-figyelmeztetési szabályt ad hozzá vagy frissít.</span><span class="sxs-lookup"><span data-stu-id="7af80-111">This command adds or updates a webtest alert rule.</span></span>

## <span data-ttu-id="7af80-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7af80-112">PARAMETERS</span></span>

### <span data-ttu-id="7af80-113">-Műveletek</span><span class="sxs-lookup"><span data-stu-id="7af80-113">-Action</span></span>
<span data-ttu-id="7af80-114">A műveletek vesszővel elválasztott listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7af80-114">Specifies a comma-separated list of actions.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]
Parameter Sets: (All)
Aliases: Actions

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7af80-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7af80-115">-DefaultProfile</span></span>
<span data-ttu-id="7af80-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7af80-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7af80-117">-Leírás</span><span class="sxs-lookup"><span data-stu-id="7af80-117">-Description</span></span>
<span data-ttu-id="7af80-118">A szabály leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="7af80-118">Specifies a description of the rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7af80-119">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="7af80-119">-DisableRule</span></span>
<span data-ttu-id="7af80-120">Letiltja a szabályt.</span><span class="sxs-lookup"><span data-stu-id="7af80-120">Disables the rule.</span></span>
<span data-ttu-id="7af80-121">Ha nem adja meg ezt a paramétert, a szabály engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="7af80-121">If you do not specify this parameter, the rule is enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7af80-122">-FailedLocationCount</span><span class="sxs-lookup"><span data-stu-id="7af80-122">-FailedLocationCount</span></span>
<span data-ttu-id="7af80-123">A webteszt szabályok sikertelen helyének számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7af80-123">Specifies the failed location count for the webtest rules.</span></span>
<span data-ttu-id="7af80-124">Ez hasonló a más típusú szabályokban szereplő küszöbértékhez.</span><span class="sxs-lookup"><span data-stu-id="7af80-124">This is similar to the threshold in the other types of rules.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7af80-125">-Hely</span><span class="sxs-lookup"><span data-stu-id="7af80-125">-Location</span></span>
<span data-ttu-id="7af80-126">A szabály helyének meghatározása.</span><span class="sxs-lookup"><span data-stu-id="7af80-126">Specifies the location where the rule is defined.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7af80-127">-MetricName</span><span class="sxs-lookup"><span data-stu-id="7af80-127">-MetricName</span></span>
<span data-ttu-id="7af80-128">A metrika nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7af80-128">Specifies the name of the metric.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7af80-129">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="7af80-129">-MetricNamespace</span></span>
<span data-ttu-id="7af80-130">A szabály metrikus névterét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7af80-130">Specifies the metric namespace for rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7af80-131">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7af80-131">-Name</span></span>
<span data-ttu-id="7af80-132">A szabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7af80-132">Specifies the name of the rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7af80-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7af80-133">-ResourceGroupName</span></span>
<span data-ttu-id="7af80-134">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7af80-134">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7af80-135">-TargetResourceUri</span><span class="sxs-lookup"><span data-stu-id="7af80-135">-TargetResourceUri</span></span>
<span data-ttu-id="7af80-136">A webteszt erőforrás-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7af80-136">Specifies the resource ID of the webtest.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7af80-137">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="7af80-137">-WindowSize</span></span>
<span data-ttu-id="7af80-138">A szabály időablakának méretét adja meg az adatainak számításához.</span><span class="sxs-lookup"><span data-stu-id="7af80-138">Specifies the time window size for the rule to compute its data.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7af80-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7af80-139">CommonParameters</span></span>
<span data-ttu-id="7af80-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7af80-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7af80-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7af80-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7af80-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7af80-142">INPUTS</span></span>

### <span data-ttu-id="7af80-143">Nincs</span><span class="sxs-lookup"><span data-stu-id="7af80-143">None</span></span>
<span data-ttu-id="7af80-144">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="7af80-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7af80-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7af80-145">OUTPUTS</span></span>

### <span data-ttu-id="7af80-146">Microsoft. Azure. commands. OutputClasses. PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="7af80-146">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="7af80-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7af80-147">NOTES</span></span>

## <span data-ttu-id="7af80-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7af80-148">RELATED LINKS</span></span>

[<span data-ttu-id="7af80-149">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="7af80-149">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="7af80-150">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="7af80-150">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="7af80-151">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="7af80-151">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="7af80-152">Új – AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="7af80-152">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)


