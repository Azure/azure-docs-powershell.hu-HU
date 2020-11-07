---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/export-azurermloganalyticrequestratebyinterval
schema: 2.0.0
ms.openlocfilehash: 4e55da6a5f0fbacab9b7af834c2729a2f79c1995
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848929"
---
# <span data-ttu-id="7e282-101">Export-AzureRmLogAnalyticRequestRateByInterval</span><span class="sxs-lookup"><span data-stu-id="7e282-101">Export-AzureRmLogAnalyticRequestRateByInterval</span></span>

## <span data-ttu-id="7e282-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7e282-102">SYNOPSIS</span></span>
<span data-ttu-id="7e282-103">Az adott időablakban az előfizetés API-kéréseit megjelenítő naplók exportálása a szabályozási tevékenységekre.</span><span class="sxs-lookup"><span data-stu-id="7e282-103">Export logs that show Api requests made by this subscription in the given time window to show throttling activities.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e282-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7e282-104">SYNTAX</span></span>

```
Export-AzureRmLogAnalyticRequestRateByInterval  [-Location] <String> [-FromTime] <DateTime> [-ToTime] <DateTime>
 [-BlobContainerSasUri] <String> [-IntervalLength] <IntervalInMins>
 [-GroupByOperationName] [-GroupByThrottlePolicy] [-GroupByResourceName] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e282-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7e282-105">DESCRIPTION</span></span>
<span data-ttu-id="7e282-106">Az exportált Microsoft. számítási API-hívásokat a siker, a kudarc vagy a szabályozási intervallum szerint elválasztva összesíti a függvény.</span><span class="sxs-lookup"><span data-stu-id="7e282-106">This exports aggregated numbers of Microsoft.Compute API calls separated by Success, Failure, or Throttled displayed in time intervals.</span></span>
<span data-ttu-id="7e282-107">A naplók további három paraméterrel csoportosíthatók: GroupByOperationName, GroupByThrottlePolicy vagy GroupByResourceName.</span><span class="sxs-lookup"><span data-stu-id="7e282-107">The logs can be further grouped by three parameters: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="7e282-108">Felhívjuk a figyelmét arra, hogy a parancsmag csak a CRP-naplókat gyűjti össze.</span><span class="sxs-lookup"><span data-stu-id="7e282-108">Note that this cmdlet collects only CRP logs.</span></span>

## <span data-ttu-id="7e282-109">Példák</span><span class="sxs-lookup"><span data-stu-id="7e282-109">EXAMPLES</span></span>

### <span data-ttu-id="7e282-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7e282-110">Example 1</span></span>
```
PS C:\> Export-AzureRmLogAnalyticRequestRateByInterval -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -IntervalLength ThirtyMins -GroupByOperationName
```

<span data-ttu-id="7e282-111">Ez a parancs a Microsoft. számítási API-hívások eredményes, sikertelen vagy fojtási, 2018-02-20T17:54:14 és 2018-02-22T17:22:17 a megadott SAS-URI-azonosítóval, a műveleti név alapján összesítve.</span><span class="sxs-lookup"><span data-stu-id="7e282-111">This command stores the aggregated numbers of Microsoft.Compute API calls separated by Success, Failure, or Throttled between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

## <span data-ttu-id="7e282-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7e282-112">PARAMETERS</span></span>

### <span data-ttu-id="7e282-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7e282-113">-AsJob</span></span>
<span data-ttu-id="7e282-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="7e282-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e282-115">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="7e282-115">-BlobContainerSasUri</span></span>
<span data-ttu-id="7e282-116">A naplózási blob-tároló SAS URI-ja, amelyre a LogAnalytics API a kimeneti naplókat írja be.</span><span class="sxs-lookup"><span data-stu-id="7e282-116">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e282-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e282-117">-DefaultProfile</span></span>
<span data-ttu-id="7e282-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7e282-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e282-119">-FromTime</span><span class="sxs-lookup"><span data-stu-id="7e282-119">-FromTime</span></span>
<span data-ttu-id="7e282-120">A lekérdezés időpontjában</span><span class="sxs-lookup"><span data-stu-id="7e282-120">From time of the query</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e282-121">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="7e282-121">-GroupByOperationName</span></span>
<span data-ttu-id="7e282-122">Lekérdezés eredményének csoportosítása operáció nevével</span><span class="sxs-lookup"><span data-stu-id="7e282-122">Group query result by Operation Name.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e282-123">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="7e282-123">-GroupByResourceName</span></span>
<span data-ttu-id="7e282-124">Lekérdezési eredmény csoportosítása erőforrás neve szerint</span><span class="sxs-lookup"><span data-stu-id="7e282-124">Group query result by Resource Name.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e282-125">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="7e282-125">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="7e282-126">A lekérdezés eredményének csoportosítása a szabályozási házirend alapján.</span><span class="sxs-lookup"><span data-stu-id="7e282-126">Group query result by Throttle Policy applied.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e282-127">-IntervalLength</span><span class="sxs-lookup"><span data-stu-id="7e282-127">-IntervalLength</span></span>
<span data-ttu-id="7e282-128">A LogAnalytics létrehozásához használt időközi érték percben.</span><span class="sxs-lookup"><span data-stu-id="7e282-128">Interval value in minutes used to create LogAnalytics call rate logs.</span></span>

```yaml
Type: IntervalInMins
Parameter Sets: (All)
Aliases: 
Accepted values: ThreeMins, FiveMins, ThirtyMins, SixtyMins

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e282-129">-Hely</span><span class="sxs-lookup"><span data-stu-id="7e282-129">-Location</span></span>
<span data-ttu-id="7e282-130">Az a hely, amelyre a naplózási analitikus lekérdezés van lekérdezve.</span><span class="sxs-lookup"><span data-stu-id="7e282-130">The location upon which log analytic is queried.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e282-131">-ToTime</span><span class="sxs-lookup"><span data-stu-id="7e282-131">-ToTime</span></span>
<span data-ttu-id="7e282-132">A lekérdezés időpontjának időpontja</span><span class="sxs-lookup"><span data-stu-id="7e282-132">To time of the query</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e282-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7e282-133">-Confirm</span></span>
<span data-ttu-id="7e282-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7e282-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e282-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e282-135">-WhatIf</span></span>
<span data-ttu-id="7e282-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7e282-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e282-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7e282-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e282-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e282-138">CommonParameters</span></span>
<span data-ttu-id="7e282-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7e282-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e282-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e282-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e282-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7e282-141">INPUTS</span></span>

### <span data-ttu-id="7e282-142">System. String</span><span class="sxs-lookup"><span data-stu-id="7e282-142">System.String</span></span>

## <span data-ttu-id="7e282-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7e282-143">OUTPUTS</span></span>

### <span data-ttu-id="7e282-144">Microsoft. Azure. commands. számítási. Automation. models. PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="7e282-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="7e282-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7e282-145">NOTES</span></span>

## <span data-ttu-id="7e282-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7e282-146">RELATED LINKS</span></span>

