---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 3BCEADF3-15DC-4033-A94A-4C8B4F5E7340
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappslotmetrics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotMetrics.md
ms.openlocfilehash: 9c4399146d99da6317c70fc08f7b01dc9679525a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494257"
---
# <span data-ttu-id="ef74a-101">Get-AzureRmWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="ef74a-101">Get-AzureRmWebAppSlotMetrics</span></span>

## <span data-ttu-id="ef74a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ef74a-102">SYNOPSIS</span></span>
<span data-ttu-id="ef74a-103">Egy Azure Web App-bővítőhely metrikáit kapja.</span><span class="sxs-lookup"><span data-stu-id="ef74a-103">Gets metrics for an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef74a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ef74a-104">SYNTAX</span></span>

### <span data-ttu-id="ef74a-105">S1</span><span class="sxs-lookup"><span data-stu-id="ef74a-105">S1</span></span>
```
Get-AzureRmWebAppSlotMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef74a-106">S2</span><span class="sxs-lookup"><span data-stu-id="ef74a-106">S2</span></span>
```
Get-AzureRmWebAppSlotMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ef74a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ef74a-107">DESCRIPTION</span></span>
<span data-ttu-id="ef74a-108">A **Get-AzureRmWebAppSlotMetrics** webalkalmazás-metrikákat kap a megadott bővítőhelyhez.</span><span class="sxs-lookup"><span data-stu-id="ef74a-108">The **Get-AzureRmWebAppSlotMetrics** gets Web App metrics for the specified slot.</span></span>

## <span data-ttu-id="ef74a-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ef74a-109">EXAMPLES</span></span>

### <span data-ttu-id="ef74a-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ef74a-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["Requests"]
```

<span data-ttu-id="ef74a-111">Ez a parancs a megadott Web App percenkénti kérelmét kapja meg (PT1M-szavazási idő 1 perc) a Kezdés és a Befejezés időpontja között</span><span class="sxs-lookup"><span data-stu-id="ef74a-111">This command gets Request of the specified Web App per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="ef74a-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ef74a-112">PARAMETERS</span></span>

### <span data-ttu-id="ef74a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef74a-113">-DefaultProfile</span></span>
<span data-ttu-id="ef74a-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ef74a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef74a-115">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="ef74a-115">-EndTime</span></span>
<span data-ttu-id="ef74a-116">Befejezési időpont az UTC-ban</span><span class="sxs-lookup"><span data-stu-id="ef74a-116">End Time in UTC</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef74a-117">-Részletesség</span><span class="sxs-lookup"><span data-stu-id="ef74a-117">-Granularity</span></span>
<span data-ttu-id="ef74a-118">Granularitása</span><span class="sxs-lookup"><span data-stu-id="ef74a-118">Granularity</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef74a-119">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="ef74a-119">-InstanceDetails</span></span>
<span data-ttu-id="ef74a-120">Példány részletei</span><span class="sxs-lookup"><span data-stu-id="ef74a-120">Instance Details</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef74a-121">-Metrikák</span><span class="sxs-lookup"><span data-stu-id="ef74a-121">-Metrics</span></span>
<span data-ttu-id="ef74a-122">Metrikák</span><span class="sxs-lookup"><span data-stu-id="ef74a-122">Metrics</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef74a-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ef74a-123">-Name</span></span>
<span data-ttu-id="ef74a-124">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="ef74a-124">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef74a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef74a-125">-ResourceGroupName</span></span>
<span data-ttu-id="ef74a-126">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="ef74a-126">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef74a-127">-Slot</span><span class="sxs-lookup"><span data-stu-id="ef74a-127">-Slot</span></span>
<span data-ttu-id="ef74a-128">WebApp bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="ef74a-128">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef74a-129">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="ef74a-129">-StartTime</span></span>
<span data-ttu-id="ef74a-130">Kezdési időpont az UTC-ban</span><span class="sxs-lookup"><span data-stu-id="ef74a-130">Start Time in UTC</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef74a-131">-WebApp</span><span class="sxs-lookup"><span data-stu-id="ef74a-131">-WebApp</span></span>
<span data-ttu-id="ef74a-132">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="ef74a-132">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef74a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef74a-133">CommonParameters</span></span>
<span data-ttu-id="ef74a-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ef74a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef74a-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef74a-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef74a-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef74a-136">INPUTS</span></span>

### <span data-ttu-id="ef74a-137">Webhely</span><span class="sxs-lookup"><span data-stu-id="ef74a-137">Site</span></span>
<span data-ttu-id="ef74a-138">A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="ef74a-138">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="ef74a-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef74a-139">OUTPUTS</span></span>

## <span data-ttu-id="ef74a-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ef74a-140">NOTES</span></span>

## <span data-ttu-id="ef74a-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ef74a-141">RELATED LINKS</span></span>

[<span data-ttu-id="ef74a-142">Get-AzureRMAppServicePlanMetrics</span><span class="sxs-lookup"><span data-stu-id="ef74a-142">Get-AzureRMAppServicePlanMetrics</span></span>](./Get-AzureRmAppServicePlanMetrics.md)

[<span data-ttu-id="ef74a-143">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ef74a-143">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="ef74a-144">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ef74a-144">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)
