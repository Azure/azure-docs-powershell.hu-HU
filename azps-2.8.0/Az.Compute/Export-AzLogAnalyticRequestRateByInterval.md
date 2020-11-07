---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/export-azloganalyticrequestratebyinterval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticRequestRateByInterval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticRequestRateByInterval.md
ms.openlocfilehash: 0c76a4fe34e99de8a0cb13759f7247ae3a643302
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667492"
---
# <span data-ttu-id="cd76c-101">Export-AzLogAnalyticRequestRateByInterval</span><span class="sxs-lookup"><span data-stu-id="cd76c-101">Export-AzLogAnalyticRequestRateByInterval</span></span>

## <span data-ttu-id="cd76c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cd76c-102">SYNOPSIS</span></span>
<span data-ttu-id="cd76c-103">Az adott időablakban az előfizetés API-kéréseit megjelenítő naplók exportálása a szabályozási tevékenységekre.</span><span class="sxs-lookup"><span data-stu-id="cd76c-103">Export logs that show Api requests made by this subscription in the given time window to show throttling activities.</span></span>

## <span data-ttu-id="cd76c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cd76c-104">SYNTAX</span></span>

```
Export-AzLogAnalyticRequestRateByInterval [-Location] <String> [-FromTime] <DateTime> [-ToTime] <DateTime>
 [-BlobContainerSasUri] <String> [-IntervalLength] <IntervalInMins> [-GroupByOperationName]
 [-GroupByResourceName] [-GroupByThrottlePolicy] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd76c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cd76c-105">DESCRIPTION</span></span>
<span data-ttu-id="cd76c-106">Statisztikai adatforgalom exportálása az előfizetés hívásait a Microsoft. az API kiszámítása a siker, a kudarc vagy a szabályozott állapot szerint előre meghatározott időintervallumokban</span><span class="sxs-lookup"><span data-stu-id="cd76c-106">Exports statistical data about the subscription's calls to the Microsoft.Compute API by Success, Failure, or Throttled status, in predefined time intervals.</span></span> <span data-ttu-id="cd76c-107">A naplók további három paraméterrel csoportosíthatók: GroupByOperationName, GroupByThrottlePolicy vagy GroupByResourceName.</span><span class="sxs-lookup"><span data-stu-id="cd76c-107">The logs can be further grouped by three parameters: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="cd76c-108">Fontos tudni, hogy ez a parancsmag csak az erőforrás-szolgáltatói naplók kiszámítását gyűjti; Ezenkívül a lemez-és a pillanatkép-erőforrástípusok adatai még nem érhetők el.</span><span class="sxs-lookup"><span data-stu-id="cd76c-108">Note that this cmdlet collects only Compute Resource Provider logs; moreover, data about the Disk and Snapshot resource types is not yet available.</span></span>

<span data-ttu-id="cd76c-109">A számítási erőforrás szolgáltató API-szabályozásának áttekintése a következő témakörben található: https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits .</span><span class="sxs-lookup"><span data-stu-id="cd76c-109">For an overview of the Compute Resource Provider's API throttling, see https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits.</span></span> 

## <span data-ttu-id="cd76c-110">Példák</span><span class="sxs-lookup"><span data-stu-id="cd76c-110">EXAMPLES</span></span>

### <span data-ttu-id="cd76c-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="cd76c-111">Example 1</span></span>
```
PS C:\> Export-AzLogAnalyticRequestRateByInterval -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -IntervalLength ThirtyMins -GroupByOperationName
```

<span data-ttu-id="cd76c-112">Ez a parancs a Microsoft. számítási API-hívások eredményes, sikertelen vagy fojtási, 2018-02-20T17:54:14 és 2018-02-22T17:22:17 a megadott SAS-URI-azonosítóval, a műveleti név alapján összesítve.</span><span class="sxs-lookup"><span data-stu-id="cd76c-112">This command stores the aggregated numbers of Microsoft.Compute API calls separated by Success, Failure, or Throttled between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

## <span data-ttu-id="cd76c-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cd76c-113">PARAMETERS</span></span>

### <span data-ttu-id="cd76c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd76c-114">-AsJob</span></span>
<span data-ttu-id="cd76c-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="cd76c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cd76c-116">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="cd76c-116">-BlobContainerSasUri</span></span>
<span data-ttu-id="cd76c-117">A naplózási blob-tároló SAS URI-ja, amelyre a LogAnalytics API a kimeneti naplókat írja be.</span><span class="sxs-lookup"><span data-stu-id="cd76c-117">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd76c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd76c-118">-DefaultProfile</span></span>
<span data-ttu-id="cd76c-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cd76c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd76c-120">-FromTime</span><span class="sxs-lookup"><span data-stu-id="cd76c-120">-FromTime</span></span>
<span data-ttu-id="cd76c-121">A lekérdezés időpontjában</span><span class="sxs-lookup"><span data-stu-id="cd76c-121">From time of the query</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd76c-122">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="cd76c-122">-GroupByOperationName</span></span>
<span data-ttu-id="cd76c-123">Lekérdezés eredményének csoportosítása operáció nevével</span><span class="sxs-lookup"><span data-stu-id="cd76c-123">Group query result by Operation Name.</span></span>

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

### <span data-ttu-id="cd76c-124">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="cd76c-124">-GroupByResourceName</span></span>
<span data-ttu-id="cd76c-125">Lekérdezési eredmény csoportosítása erőforrás neve szerint</span><span class="sxs-lookup"><span data-stu-id="cd76c-125">Group query result by Resource Name.</span></span>

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

### <span data-ttu-id="cd76c-126">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="cd76c-126">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="cd76c-127">A lekérdezés eredményének csoportosítása a szabályozási házirend alapján.</span><span class="sxs-lookup"><span data-stu-id="cd76c-127">Group query result by Throttle Policy applied.</span></span>

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

### <span data-ttu-id="cd76c-128">-IntervalLength</span><span class="sxs-lookup"><span data-stu-id="cd76c-128">-IntervalLength</span></span>
<span data-ttu-id="cd76c-129">A LogAnalytics létrehozásához használt időközi érték percben.</span><span class="sxs-lookup"><span data-stu-id="cd76c-129">Interval value in minutes used to create LogAnalytics call rate logs.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.IntervalInMins
Parameter Sets: (All)
Aliases:
Accepted values: ThreeMins, FiveMins, ThirtyMins, SixtyMins

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd76c-130">-Hely</span><span class="sxs-lookup"><span data-stu-id="cd76c-130">-Location</span></span>
<span data-ttu-id="cd76c-131">Az a hely, amelyre a naplózási analitikus lekérdezés van lekérdezve.</span><span class="sxs-lookup"><span data-stu-id="cd76c-131">The location upon which log analytic is queried.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd76c-132">-Várva</span><span class="sxs-lookup"><span data-stu-id="cd76c-132">-NoWait</span></span>
<span data-ttu-id="cd76c-133">Elindítja a műveletet, és a művelet befejezése előtt azonnal visszaküldi a műveletet.</span><span class="sxs-lookup"><span data-stu-id="cd76c-133">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="cd76c-134">Ha meg szeretné állapítani, hogy sikerült-e végrehajtani a műveletet, használjon más mechanizmust.</span><span class="sxs-lookup"><span data-stu-id="cd76c-134">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="cd76c-135">-ToTime</span><span class="sxs-lookup"><span data-stu-id="cd76c-135">-ToTime</span></span>
<span data-ttu-id="cd76c-136">A lekérdezés időpontjának időpontja</span><span class="sxs-lookup"><span data-stu-id="cd76c-136">To time of the query</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd76c-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cd76c-137">-Confirm</span></span>
<span data-ttu-id="cd76c-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cd76c-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd76c-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd76c-139">-WhatIf</span></span>
<span data-ttu-id="cd76c-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cd76c-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd76c-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cd76c-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd76c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd76c-142">CommonParameters</span></span>
<span data-ttu-id="cd76c-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cd76c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd76c-144">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="cd76c-144">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd76c-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd76c-145">INPUTS</span></span>

### <span data-ttu-id="cd76c-146">System. String</span><span class="sxs-lookup"><span data-stu-id="cd76c-146">System.String</span></span>

## <span data-ttu-id="cd76c-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd76c-147">OUTPUTS</span></span>

### <span data-ttu-id="cd76c-148">Microsoft. Azure. commands. számítási. Automation. models. PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="cd76c-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="cd76c-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cd76c-149">NOTES</span></span>

## <span data-ttu-id="cd76c-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cd76c-150">RELATED LINKS</span></span>
