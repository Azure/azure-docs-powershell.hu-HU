---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A70F4C03-E842-45D5-9323-DC5B14B569F1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermautoscalehistory
schema: 2.0.0
ms.openlocfilehash: c149cf0d44bfe5fdeee953d36a7ea8244587ba36
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848314"
---
# <span data-ttu-id="45a16-101">Get-AzureRmAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="45a16-101">Get-AzureRmAutoscaleHistory</span></span>

## <span data-ttu-id="45a16-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="45a16-102">SYNOPSIS</span></span>
<span data-ttu-id="45a16-103">Megkapja az autoscale előzményeit.</span><span class="sxs-lookup"><span data-stu-id="45a16-103">Gets the Autoscale history.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45a16-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="45a16-104">SYNTAX</span></span>

```
Get-AzureRmAutoscaleHistory [-ResourceId <String>] [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Status <String>] [-Caller <String>] [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="45a16-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="45a16-105">DESCRIPTION</span></span>
<span data-ttu-id="45a16-106">A **Get-AzureRmAutoscaleHistory** parancsmag az automéretarányos beállítással kapcsolatos események előzményeit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="45a16-106">The **Get-AzureRmAutoscaleHistory** cmdlet gets the history of events related to an Autoscale setting.</span></span>

## <span data-ttu-id="45a16-107">Példák</span><span class="sxs-lookup"><span data-stu-id="45a16-107">EXAMPLES</span></span>

### <span data-ttu-id="45a16-108">Példa 1: az előfizetéshez társított összes esemény beolvasása</span><span class="sxs-lookup"><span data-stu-id="45a16-108">Example 1: Get all events associated with a subscription</span></span>
```
PS C:\>Get-AzureRmAutoscaleHistory -StartTime 2015-02-09T18:35:00 -EndTime 2015-02-09T18:40:00 -DetailedOutput
```

<span data-ttu-id="45a16-109">Ez a parancs beilleszti a jelenlegi előfizetéshez társított összes automéretarányos eseményt.</span><span class="sxs-lookup"><span data-stu-id="45a16-109">This command gets all of the Autoscale-related events associated with the current subscription.</span></span>

### <span data-ttu-id="45a16-110">2. példa: adott erőforrás GetAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="45a16-110">Example 2: GetAutoscaleHistory for a particular resource</span></span>
```
PS C:\>Get-AzureRmAutoscaleHistory -StartTime 2015-02-09T18:35:00 -EndTime 2015-02-09T18:40:00 -ResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.insights/autoscalesettings/DefaultServerFarm-Default-Web-EastUS" -DetailedOutput
Authorization        : 
Caller               : Microsoft.Insights/autoscaleSettings
Claims               :  http://schemas.xmlsoap.org/ws/2005/05/identity/claims/spn: Microsoft.Insights/autoscaleSettings
CorrelationId        : ac5b03ca-05d4-4811-9c27-0314a145f785
Description          : The autoscale engine attempting to scale resource '/subscriptions/a93fb07c-6c93-40be-bf3b-4f0deb
                       a10f4b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm'
                       from 1 instances count to 2 instances count. 
EventDataId          : c554f7ed-514c-449c-9338-13e15b4b56a3
EventName            : AutoscaleAction
EventSource          : microsoft.insights/autoscalesettings
EventTimestamp       : 2/10/2015 2:38:19 AM
HttpRequest          : 
Id                   : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/
                       microsoft.insights/autoscalesettings/DefaultServerFarm-Default-Web-EastUS/events/c554f7ed-514c-4
                       49c-9338-13e15b4b56a3/ticks/635591326997519815
Level                : Informational
OperationId          : ac5b03ca-05d4-4811-9c27-0314a145f785
OperationName        : ScaleUp
Properties           : 
Description    : The autoscale engine attempting to scale resource '/subscriptions/a93fb07c-6c93
                       -40be-bf3b-4f0deba10f4b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/De
                       faultServerFarm' from 1 instances count to 2 instances count. 
ResourceName   : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-
                       EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm
OldInstancesCount: 1
NewInstancesCount: 2
ActiveAutoscaleProfile: {
                         "Name": "No scheduled times",
                         "Capacity": {
                           "Minimum": "1",
                           "Maximum": "3",
                           "Default": "1"
                         },
                         "Rules": [
                           {
                             "MetricTrigger": {
                               "Name": "CpuPercentage",
                               "Namespace": "",
                               "Resource": "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-
                       Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm",
                               "ResourceLocation": "East US",
                               "TimeGrain": "PT1M",
                               "Statistic": "Average",
                               "TimeWindow": "PT45M",
                               "TimeAggregation": "Average",
                               "Operator": "GreaterThanOrEqual",
                               "Threshold": 14.0, 
                               "Source": "WebsiteDedicated:eastuswebspace:DefaultServerFarm"
                             },
                             "ScaleAction": {
                               "Direction": "Increase",
                               "Type": "ChangeCount",
                               "Value": "1",
                               "Cooldown": "PT5M"
                             }
                           },
                           {
                             "MetricTrigger": {
                               "Name": "CpuPercentage",
                               "Namespace": "",
                               "Resource": "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-
                       Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm",
                               "ResourceLocation": "East US",
                               "TimeGrain": "PT1M",
                               "Statistic": "Average",
                               "TimeWindow": "PT45M",
                               "TimeAggregation": "Average",
                               "Operator": "LessThanOrEqual",
                               "Threshold": 4.0, 
                               "Source": "WebsiteDedicated:eastuswebspace:DefaultServerFarm"
                             },
                             "ScaleAction": {
                               "Direction": "Decrease",
                               "Type": "ChangeCount",
                               "Value": "1",
                               "Cooldown": "PT2H"
                             }
                           },
                           {
                             "MetricTrigger": {
                               "Name": "BytesReceived",
                               "Namespace": "",
                               "Resource": "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-
                       Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm",
                               "ResourceLocation": "East US",
                               "TimeGrain": "PT1M",
                               "Statistic": "Average",
                               "TimeWindow": "PT10M",
                               "TimeAggregation": "Average",
                               "Operator": "LessThanOrEqual",
                               "Threshold": 50.0, 
                               "Source": "WebsiteDedicated:eastuswebspace:DefaultServerFarm"
                             },
                             "ScaleAction": {
                               "Direction": "Decrease",
                               "Type": "ChangeCount",
                               "Value": "1",
                               "Cooldown": "PT10M"
                             }
                           },
                           {
                             "MetricTrigger": {
                               "Name": "BytesReceived",
                               "Namespace": "",
                               "Resource": "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-
                       Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm",
                               "ResourceLocation": "East US",
                               "TimeGrain": "PT1M",
                               "Statistic": "Average",
                               "TimeWindow": "PT5M",
                               "TimeAggregation": "Average",
                               "Operator": "GreaterThanOrEqual",
                               "Threshold": 100.0, 
                               "Source": "WebsiteDedicated:eastuswebspace:DefaultServerFarm"
                             },
                             "ScaleAction": {
                               "Direction": "Increase",
                               "Type": "ChangeCount",
                               "Value": "1",
                               "Cooldown": "PT10M"
                             }
                           }
                         ] 
                       }
ResourceGroupName    : Default-Web-EastUS
ResourceProviderName : microsoft.insights
ResourceId           : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/
                       microsoft.insights/autoscalesettings/DefaultServerFarm-Default-Web-EastUS
Status               : Succeeded
SubmissionTimestamp  : 2/10/2015 2:38:19 AM
SubscriptionId       : b93fb07a-6f93-30be-bf3e-4f0deca15f4f
SubStatus            :
```

<span data-ttu-id="45a16-111">Ez a parancs az erőforrás-AZONOSÍTÓval azonosított adott erőforráshoz tartozó összes automéretarányos eseményt megkapja (lényegében a ResourceUri).</span><span class="sxs-lookup"><span data-stu-id="45a16-111">This command gets all Autoscale-related events associated with a particular resource identified by the resource's ID (essentially, the ResourceUri).</span></span>

## <span data-ttu-id="45a16-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="45a16-112">PARAMETERS</span></span>

### <span data-ttu-id="45a16-113">-Hívó</span><span class="sxs-lookup"><span data-stu-id="45a16-113">-Caller</span></span>
<span data-ttu-id="45a16-114">A hívót adja meg.</span><span class="sxs-lookup"><span data-stu-id="45a16-114">Specifies a caller.</span></span>

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

### <span data-ttu-id="45a16-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45a16-115">-DefaultProfile</span></span>
<span data-ttu-id="45a16-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="45a16-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="45a16-117">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="45a16-117">-DetailedOutput</span></span>
<span data-ttu-id="45a16-118">Jelzi, hogy ez a művelet a részletes kimenetet is tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="45a16-118">Indicates that this operation included detailed output.</span></span>
<span data-ttu-id="45a16-119">Ha nem adja meg ezt a paramétert, a program összesíti a kimenetet.</span><span class="sxs-lookup"><span data-stu-id="45a16-119">If you do not specify this parameter, the output is summarized.</span></span>

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

### <span data-ttu-id="45a16-120">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="45a16-120">-EndTime</span></span>
<span data-ttu-id="45a16-121">A lekérdezés befejezési időpontját adja meg helyi időben.</span><span class="sxs-lookup"><span data-stu-id="45a16-121">Specifies the end time of the query in local time.</span></span>
<span data-ttu-id="45a16-122">Az alapértelmezett időpont az aktuális idő.</span><span class="sxs-lookup"><span data-stu-id="45a16-122">The default is the current time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45a16-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="45a16-123">-ResourceId</span></span>
<span data-ttu-id="45a16-124">Annak az erőforrásnak az AZONOSÍTÓját adja meg, amelyhez az automéretarány beállítás van társítva.</span><span class="sxs-lookup"><span data-stu-id="45a16-124">Specifies the resource ID to which the autoscale setting is associated.</span></span>

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

### <span data-ttu-id="45a16-125">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="45a16-125">-StartTime</span></span>
<span data-ttu-id="45a16-126">A lekérdezés kezdési időpontját adja meg helyi időben.</span><span class="sxs-lookup"><span data-stu-id="45a16-126">Specifies the start time of the query in local time.</span></span>
<span data-ttu-id="45a16-127">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="45a16-127">This parameter is optional.</span></span>
<span data-ttu-id="45a16-128">Az alapértelmezett időpont az aktuális helyi idő, egy óra mínusz.</span><span class="sxs-lookup"><span data-stu-id="45a16-128">The default is the current local time minus one hour.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45a16-129">-Állapot</span><span class="sxs-lookup"><span data-stu-id="45a16-129">-Status</span></span>
<span data-ttu-id="45a16-130">Az állapot szerinti szűrést adja meg.</span><span class="sxs-lookup"><span data-stu-id="45a16-130">Specifies a filter by status.</span></span>
<span data-ttu-id="45a16-131">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="45a16-131">This parameter is optional.</span></span>
<span data-ttu-id="45a16-132">A hiba egy üres karakterlánc (azaz nincs szűrő)</span><span class="sxs-lookup"><span data-stu-id="45a16-132">The fault is an empty string (i.e. no filter)</span></span>

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

### <span data-ttu-id="45a16-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45a16-133">CommonParameters</span></span>
<span data-ttu-id="45a16-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="45a16-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45a16-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45a16-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45a16-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="45a16-136">INPUTS</span></span>

### <span data-ttu-id="45a16-137">System. String</span><span class="sxs-lookup"><span data-stu-id="45a16-137">System.String</span></span>

### <span data-ttu-id="45a16-138">System. null ' 1 [[System. DateTime, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="45a16-138">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="45a16-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="45a16-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="45a16-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="45a16-140">OUTPUTS</span></span>

### <span data-ttu-id="45a16-141">Microsoft. Azure. commands. OutputClasses. PSEventData</span><span class="sxs-lookup"><span data-stu-id="45a16-141">Microsoft.Azure.Commands.Insights.OutputClasses.PSEventData</span></span>

## <span data-ttu-id="45a16-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="45a16-142">NOTES</span></span>

## <span data-ttu-id="45a16-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="45a16-143">RELATED LINKS</span></span>

[<span data-ttu-id="45a16-144">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="45a16-144">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="45a16-145">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="45a16-145">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="45a16-146">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="45a16-146">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)

