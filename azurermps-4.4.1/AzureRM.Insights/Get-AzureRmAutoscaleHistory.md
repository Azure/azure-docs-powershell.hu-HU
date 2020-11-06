---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A70F4C03-E842-45D5-9323-DC5B14B569F1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmAutoscaleHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmAutoscaleHistory.md
ms.openlocfilehash: 12907bc7dbe7507dd12dbda13f0eb2ca722eaec3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504931"
---
# <span data-ttu-id="fe931-101">Get-AzureRmAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="fe931-101">Get-AzureRmAutoscaleHistory</span></span>

## <span data-ttu-id="fe931-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fe931-102">SYNOPSIS</span></span>
<span data-ttu-id="fe931-103">Megkapja az autoscale előzményeit.</span><span class="sxs-lookup"><span data-stu-id="fe931-103">Gets the Autoscale history.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe931-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fe931-104">SYNTAX</span></span>

```
Get-AzureRmAutoscaleHistory [-ResourceId <String>] [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Status <String>] [-Caller <String>] [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fe931-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fe931-105">DESCRIPTION</span></span>
<span data-ttu-id="fe931-106">A **Get-AzureRmAutoscaleHistory** parancsmag az automéretarányos beállítással kapcsolatos események előzményeit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="fe931-106">The **Get-AzureRmAutoscaleHistory** cmdlet gets the history of events related to an Autoscale setting.</span></span>

## <span data-ttu-id="fe931-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fe931-107">EXAMPLES</span></span>

### <span data-ttu-id="fe931-108">Példa 1: az előfizetéshez társított összes esemény beolvasása</span><span class="sxs-lookup"><span data-stu-id="fe931-108">Example 1: Get all events associated with a subscription</span></span>
```
PS C:\>Get-AzureRmAutoscaleHistory -StartTime 2015-02-09T18:35:00 -EndTime 2015-02-09T18:40:00 -DetailedOutput
```

<span data-ttu-id="fe931-109">Ez a parancs beilleszti a jelenlegi előfizetéshez társított összes automéretarányos eseményt.</span><span class="sxs-lookup"><span data-stu-id="fe931-109">This command gets all of the Autoscale-related events associated with the current subscription.</span></span>

### <span data-ttu-id="fe931-110">2. példa: adott erőforrás GetAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="fe931-110">Example 2: GetAutoscaleHistory for a particular resource</span></span>
```
PS C:\>Get-AzureRmAutoscaleHistory -StartTime 2015-02-09T18:35:00 -EndTime 2015-02-09T18:40:00 -ResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.insights/autoscalesettings/DefaultServerFarm-Default-Web-EastUS" -DetailedOutput
Authorization        : 
Caller               : Microsoft.Insights/autoscaleSettings
Claims               :  http://schemas.xmlsoap.org/ws/2005/05/identity/claims/spn: Microsoft.Insights/autoscaleSettings
CorrelationId        : ac5b03ca-05d4-4811-9c27-0314a145f785
Description          : The autoscale engine attempting to scale resource '/subscriptions/a93fb07c-6c93-40be-bf3b-4f0deb
                       a10f4b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm'
                       from 1 instances count to 2 instances count. 
EventChannels        : Admin, Operation
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

<span data-ttu-id="fe931-111">Ez a parancs az erőforrás-AZONOSÍTÓval azonosított adott erőforráshoz tartozó összes automéretarányos eseményt megkapja (lényegében a ResourceUri).</span><span class="sxs-lookup"><span data-stu-id="fe931-111">This command gets all Autoscale-related events associated with a particular resource identified by the resource's ID (essentially, the ResourceUri).</span></span>

## <span data-ttu-id="fe931-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fe931-112">PARAMETERS</span></span>

### <span data-ttu-id="fe931-113">-Hívó</span><span class="sxs-lookup"><span data-stu-id="fe931-113">-Caller</span></span>
<span data-ttu-id="fe931-114">A hívót adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe931-114">Specifies a caller.</span></span>

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

### <span data-ttu-id="fe931-115">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="fe931-115">-DetailedOutput</span></span>
<span data-ttu-id="fe931-116">Jelzi, hogy ez a művelet a részletes kimenetet is tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="fe931-116">Indicates that this operation included detailed output.</span></span>
<span data-ttu-id="fe931-117">Ha nem adja meg ezt a paramétert, a program összesíti a kimenetet.</span><span class="sxs-lookup"><span data-stu-id="fe931-117">If you do not specify this parameter, the output is summarized.</span></span>

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

### <span data-ttu-id="fe931-118">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="fe931-118">-EndTime</span></span>
<span data-ttu-id="fe931-119">A lekérdezés befejezési időpontját adja meg helyi időben.</span><span class="sxs-lookup"><span data-stu-id="fe931-119">Specifies the end time of the query in local time.</span></span>
<span data-ttu-id="fe931-120">Az alapértelmezett időpont az aktuális idő.</span><span class="sxs-lookup"><span data-stu-id="fe931-120">The default is the current time.</span></span>

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

### <span data-ttu-id="fe931-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fe931-121">-ResourceId</span></span>
<span data-ttu-id="fe931-122">Annak az erőforrásnak az AZONOSÍTÓját adja meg, amelyhez az automéretarány beállítás van társítva.</span><span class="sxs-lookup"><span data-stu-id="fe931-122">Specifies the resource ID to which the autoscale setting is associated.</span></span>

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

### <span data-ttu-id="fe931-123">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="fe931-123">-StartTime</span></span>
<span data-ttu-id="fe931-124">A lekérdezés kezdési időpontját adja meg helyi időben.</span><span class="sxs-lookup"><span data-stu-id="fe931-124">Specifies the start time of the query in local time.</span></span>
<span data-ttu-id="fe931-125">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="fe931-125">This parameter is optional.</span></span>
<span data-ttu-id="fe931-126">Az alapértelmezett időpont az aktuális helyi idő, egy óra mínusz.</span><span class="sxs-lookup"><span data-stu-id="fe931-126">The default is the current local time minus one hour.</span></span>

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

### <span data-ttu-id="fe931-127">-Állapot</span><span class="sxs-lookup"><span data-stu-id="fe931-127">-Status</span></span>
<span data-ttu-id="fe931-128">Az állapot szerinti szűrést adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe931-128">Specifies a filter by status.</span></span>
<span data-ttu-id="fe931-129">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="fe931-129">This parameter is optional.</span></span>
<span data-ttu-id="fe931-130">A hiba egy üres karakterlánc (azaz nincs szűrő)</span><span class="sxs-lookup"><span data-stu-id="fe931-130">The fault is an empty string (i.e. no filter)</span></span>

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

### <span data-ttu-id="fe931-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe931-131">-DefaultProfile</span></span>
<span data-ttu-id="fe931-132">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fe931-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe931-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe931-133">CommonParameters</span></span>
<span data-ttu-id="fe931-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fe931-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe931-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe931-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe931-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fe931-136">INPUTS</span></span>

## <span data-ttu-id="fe931-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fe931-137">OUTPUTS</span></span>

### <span data-ttu-id="fe931-138">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. detekintés. OutputClasses. IPSEventData]</span><span class="sxs-lookup"><span data-stu-id="fe931-138">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSEventData]</span></span>

## <span data-ttu-id="fe931-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fe931-139">NOTES</span></span>

## <span data-ttu-id="fe931-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fe931-140">RELATED LINKS</span></span>

[<span data-ttu-id="fe931-141">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="fe931-141">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="fe931-142">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="fe931-142">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="fe931-143">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="fe931-143">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)


