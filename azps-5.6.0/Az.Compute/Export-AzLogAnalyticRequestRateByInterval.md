---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/export-azloganalyticrequestratebyinterval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticRequestRateByInterval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticRequestRateByInterval.md
ms.openlocfilehash: feae2282f6b989b8d595b2a51cd147975e689174
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927321"
---
# <span data-ttu-id="1bea0-101">Export-AzLogAnalyticRequestRateByInterval</span><span class="sxs-lookup"><span data-stu-id="1bea0-101">Export-AzLogAnalyticRequestRateByInterval</span></span>

## <span data-ttu-id="1bea0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1bea0-102">SYNOPSIS</span></span>
<span data-ttu-id="1bea0-103">Olyan naplók exportálása, amelyek az előfizetés api-kérését mutatják a megadott időkeretben a szabályozási tevékenységek megtekintéséhez.</span><span class="sxs-lookup"><span data-stu-id="1bea0-103">Export logs that show Api requests made by this subscription in the given time window to show throttling activities.</span></span>

## <span data-ttu-id="1bea0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1bea0-104">SYNTAX</span></span>

```
Export-AzLogAnalyticRequestRateByInterval [-Location] <String> [-FromTime] <DateTime> [-ToTime] <DateTime>
 [-BlobContainerSasUri] <String> [-IntervalLength] <IntervalInMins> [-GroupByOperationName]
 [-GroupByResourceName] [-GroupByThrottlePolicy] [-GroupByApplicationId] [-GroupByUserAgent] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1bea0-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1bea0-105">DESCRIPTION</span></span>
<span data-ttu-id="1bea0-106">Az előfizetés hívásaira vonatkozó statisztikai adatokat exportálja a Microsoft.Compute API-ba siker, hiba vagy szabályozási állapot alapján, előre meghatározott időintervallumokban.</span><span class="sxs-lookup"><span data-stu-id="1bea0-106">Exports statistical data about the subscription's calls to the Microsoft.Compute API by Success, Failure, or Throttled status, in predefined time intervals.</span></span> <span data-ttu-id="1bea0-107">A naplók további öt paraméter szerint csoportosíthatóak: GroupByOperationName, GroupByThrottlePolicy, GroupByResourceName, GroupByUserAgent vagy GroupByApplicationId.</span><span class="sxs-lookup"><span data-stu-id="1bea0-107">The logs can be further grouped by five parameters: GroupByOperationName, GroupByThrottlePolicy, GroupByResourceName, GroupByUserAgent, or GroupByApplicationId.</span></span>
<span data-ttu-id="1bea0-108">Ne feledje, hogy ez a parancsmag csak a Számítási erőforrás-szolgáltató naplóit gyűjti; Ezenkívül a Lemez és a Pillanatfelvétel erőforrástípusról még nem állnak rendelkezésre adatok.</span><span class="sxs-lookup"><span data-stu-id="1bea0-108">Note that this cmdlet collects only Compute Resource Provider logs; moreover, data about the Disk and Snapshot resource types is not yet available.</span></span>

<span data-ttu-id="1bea0-109">A Számítási erőforrás-szolgáltató API-szabályozásának áttekintése: https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-request-limits .</span><span class="sxs-lookup"><span data-stu-id="1bea0-109">For an overview of the Compute Resource Provider's API throttling, see https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-request-limits.</span></span> 

## <span data-ttu-id="1bea0-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1bea0-110">EXAMPLES</span></span>

### <span data-ttu-id="1bea0-111">1. példa: A művelet neve alapján összesített rekordok exportálása</span><span class="sxs-lookup"><span data-stu-id="1bea0-111">Example 1: Export records aggregated by operation name</span></span>
```
PS C:\> Export-AzLogAnalyticRequestRateByInterval -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -IntervalLength ThirtyMins -GroupByOperationName
This command downloads a .csv file to the provided container. The format of the file is:

TIMESTAMP             operationName   TotalRequests SuccessfulRequests ThrottledRequests
---------             -------------   ------------- ------------------ -----------------
2/21/2018  7:00:00 PM <operationName> 10            10                 0
2/21/2018  7:30:00 PM <operationName> 8             8                  0
2/21/2018  9:00:00 PM <operationName> 9             9                  0

```

<span data-ttu-id="1bea0-112">Ez a parancs a Microsoft.Compute API-hívások összesített számát tárolja a 2018–2018–02–20T17:54:14 és 2018-02-22T17:54:17 közötti, a művelet neve alapján összesített SAS URI-val elválasztva.</span><span class="sxs-lookup"><span data-stu-id="1bea0-112">This command stores the aggregated numbers of Microsoft.Compute API calls separated by Success, Failure, or Throttled between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

### <span data-ttu-id="1bea0-113">2. példa: Alkalmazásazonosítóval összesített rekordok exportálása</span><span class="sxs-lookup"><span data-stu-id="1bea0-113">Example 2: Export records aggregated by application id</span></span>
```
PS C:\> Export-AzLogAnalyticRequestRateByInterval -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -IntervalLength ThirtyMins -GroupByApplicationId

This command downloads a .csv file to the provided container. The format of the file is:

TIMESTAMP             clientApplicationId   TotalRequests SuccessfulRequests ThrottledRequests
---------             -------------------   ------------- ------------------ -----------------
2/21/2018  7:00:00 PM <clientApplicationId> 10            10                 0
2/21/2018  7:30:00 PM <clientApplicationId> 8             8                  0
2/21/2018  9:00:00 PM <clientApplicationId> 9             9                  0

```

<span data-ttu-id="1bea0-114">Ez a parancs a Microsoft.Compute API-hívások összesített számát tárolja a 2018–2018–20T17:54:14 és a 2018-02-22T17:54:17 közötti, az adott SAS URI-val elválasztott, alkalmazásazonosítóval összesítve.</span><span class="sxs-lookup"><span data-stu-id="1bea0-114">This command stores the aggregated numbers of Microsoft.Compute API calls separated by Success, Failure, or Throttled between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by application id.</span></span> 

### <span data-ttu-id="1bea0-115">3. példa: Felhasználói ügynök által összesített rekordok exportálása</span><span class="sxs-lookup"><span data-stu-id="1bea0-115">Example 3: Export records aggregated by user agent</span></span>
```
PS C:\> Export-AzLogAnalyticRequestRateByInterval -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -IntervalLength ThirtyMins -GroupByUserAgent
This command downloads a .csv file to the provided container. The format of the file is:

TIMESTAMP             userAgent   TotalRequests SuccessfulRequests ThrottledRequests
---------             ---------   ------------- ------------------ -----------------
2/21/2018  7:00:00 PM <userAgent> 10            10                 0
2/21/2018  7:30:00 PM <userAgent> 8             8                  0
2/21/2018  9:00:00 PM <userAgent> 9             9                  0

```

<span data-ttu-id="1bea0-116">Ez a parancs a Microsoft.Compute API-hívások összesített számát tárolja a 2018–2018–02–20T17:54:14 és 2018-02-22T17:54:17 közötti, a felhasználói ügynök által összesített SAS URI-val elválasztva.</span><span class="sxs-lookup"><span data-stu-id="1bea0-116">This command stores the aggregated numbers of Microsoft.Compute API calls separated by Success, Failure, or Throttled between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by user agent.</span></span> 

## <span data-ttu-id="1bea0-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1bea0-117">PARAMETERS</span></span>

### <span data-ttu-id="1bea0-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1bea0-118">-AsJob</span></span>
<span data-ttu-id="1bea0-119">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="1bea0-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1bea0-120">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="1bea0-120">-BlobContainerSasUri</span></span>
<span data-ttu-id="1bea0-121">A naplózási blobtároló SAS Uri-ja, amelybe a LogAnalytics Api kimeneti naplókat ír.</span><span class="sxs-lookup"><span data-stu-id="1bea0-121">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

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

### <span data-ttu-id="1bea0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bea0-122">-DefaultProfile</span></span>
<span data-ttu-id="1bea0-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1bea0-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1bea0-124">-FromTime</span><span class="sxs-lookup"><span data-stu-id="1bea0-124">-FromTime</span></span>
<span data-ttu-id="1bea0-125">A lekérdezés időtől</span><span class="sxs-lookup"><span data-stu-id="1bea0-125">From time of the query</span></span>

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

### <span data-ttu-id="1bea0-126">-GroupByApplicationId</span><span class="sxs-lookup"><span data-stu-id="1bea0-126">-GroupByApplicationId</span></span>
<span data-ttu-id="1bea0-127">A csoportos lekérdezés eredménye alkalmazásazonosító alapján.</span><span class="sxs-lookup"><span data-stu-id="1bea0-127">Group query result by Application Id.</span></span>

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

### <span data-ttu-id="1bea0-128">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="1bea0-128">-GroupByOperationName</span></span>
<span data-ttu-id="1bea0-129">A csoportlekérdezés eredménye műveletnév szerint.</span><span class="sxs-lookup"><span data-stu-id="1bea0-129">Group query result by Operation Name.</span></span>

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

### <span data-ttu-id="1bea0-130">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="1bea0-130">-GroupByResourceName</span></span>
<span data-ttu-id="1bea0-131">A csoportlekérdezés eredménye erőforrásnév szerint.</span><span class="sxs-lookup"><span data-stu-id="1bea0-131">Group query result by Resource Name.</span></span>

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

### <span data-ttu-id="1bea0-132">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="1bea0-132">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="1bea0-133">A csoportlekérdezés eredménye a szabálysértés által alkalmazva.</span><span class="sxs-lookup"><span data-stu-id="1bea0-133">Group query result by Throttle Policy applied.</span></span>

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

### <span data-ttu-id="1bea0-134">-GroupByUserAgent</span><span class="sxs-lookup"><span data-stu-id="1bea0-134">-GroupByUserAgent</span></span>
<span data-ttu-id="1bea0-135">Group query result by UserAgent.</span><span class="sxs-lookup"><span data-stu-id="1bea0-135">Group query result by UserAgent.</span></span>

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

### <span data-ttu-id="1bea0-136">-IntervalLength</span><span class="sxs-lookup"><span data-stu-id="1bea0-136">-IntervalLength</span></span>
<span data-ttu-id="1bea0-137">Interval value in minutes used to create LogAnalytics call rate logs.</span><span class="sxs-lookup"><span data-stu-id="1bea0-137">Interval value in minutes used to create LogAnalytics call rate logs.</span></span>

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

### <span data-ttu-id="1bea0-138">-Location</span><span class="sxs-lookup"><span data-stu-id="1bea0-138">-Location</span></span>
<span data-ttu-id="1bea0-139">A napló analytic lekérdezésének helye.</span><span class="sxs-lookup"><span data-stu-id="1bea0-139">The location upon which log analytic is queried.</span></span>

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

### <span data-ttu-id="1bea0-140">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1bea0-140">-NoWait</span></span>
<span data-ttu-id="1bea0-141">Elindítja a műveletet, és azonnal, a művelet befejezése előtt visszatér.</span><span class="sxs-lookup"><span data-stu-id="1bea0-141">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="1bea0-142">Ha meg szeretné állapítani, hogy a művelet sikeresen befejeződött-e, használjon más mechanizmust.</span><span class="sxs-lookup"><span data-stu-id="1bea0-142">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="1bea0-143">-ToTime</span><span class="sxs-lookup"><span data-stu-id="1bea0-143">-ToTime</span></span>
<span data-ttu-id="1bea0-144">A lekérdezés ideje</span><span class="sxs-lookup"><span data-stu-id="1bea0-144">To time of the query</span></span>

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

### <span data-ttu-id="1bea0-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1bea0-145">-Confirm</span></span>
<span data-ttu-id="1bea0-146">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1bea0-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1bea0-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bea0-147">-WhatIf</span></span>
<span data-ttu-id="1bea0-148">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="1bea0-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1bea0-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1bea0-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1bea0-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bea0-150">CommonParameters</span></span>
<span data-ttu-id="1bea0-151">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bea0-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bea0-152">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1bea0-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bea0-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1bea0-153">INPUTS</span></span>

### <span data-ttu-id="1bea0-154">System.String</span><span class="sxs-lookup"><span data-stu-id="1bea0-154">System.String</span></span>

## <span data-ttu-id="1bea0-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1bea0-155">OUTPUTS</span></span>

### <span data-ttu-id="1bea0-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="1bea0-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="1bea0-157">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1bea0-157">NOTES</span></span>

## <span data-ttu-id="1bea0-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1bea0-158">RELATED LINKS</span></span>
