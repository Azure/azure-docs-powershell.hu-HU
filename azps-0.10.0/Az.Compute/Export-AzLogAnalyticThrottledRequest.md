---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/export-AzLogAnalyticThrottledRequest
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Export-AzLogAnalyticThrottledRequest.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Export-AzLogAnalyticThrottledRequest.md
ms.openlocfilehash: 45f0a75b07d0fae07092ffbe2b23f42cfa6d707a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844681"
---
# <span data-ttu-id="71361-101">Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="71361-101">Export-AzLogAnalyticThrottledRequest</span></span>

## <span data-ttu-id="71361-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="71361-102">SYNOPSIS</span></span>
<span data-ttu-id="71361-103">Olyan naplók exportálása, amelyek az adott időablakban az előfizetéshez tartozó összes szabályozott API-kérést megjelenítik.</span><span class="sxs-lookup"><span data-stu-id="71361-103">Export logs that show total throttled Api requests for this subscription in the given time window.</span></span>

## <span data-ttu-id="71361-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="71361-104">SYNTAX</span></span>

```
Export-AzLogAnalyticThrottledRequest [-Location] <String> [-FromTime] <DateTime> [-ToTime] <DateTime>
 [-BlobContainerSasUri] <String>
 [-GroupByOperationName]  [-GroupByThrottlePolicy] [-GroupByResourceName] 
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="71361-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="71361-105">DESCRIPTION</span></span>
<span data-ttu-id="71361-106">Ezzel exportálja a Microsoft. számítási API-hívások teljes számát.</span><span class="sxs-lookup"><span data-stu-id="71361-106">This exports the total number of throttled Microsoft.Compute API calls.</span></span>
<span data-ttu-id="71361-107">A naplókat a következő három beállítással lehet összesíteni: GroupByOperationName, GroupByThrottlePolicy vagy GroupByResourceName.</span><span class="sxs-lookup"><span data-stu-id="71361-107">The logs can be further aggregated by three options: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="71361-108">Felhívjuk a figyelmét arra, hogy a parancsmag csak a CRP-naplókat gyűjti össze.</span><span class="sxs-lookup"><span data-stu-id="71361-108">Note that this cmdlet collects only CRP logs.</span></span>

## <span data-ttu-id="71361-109">Példák</span><span class="sxs-lookup"><span data-stu-id="71361-109">EXAMPLES</span></span>

### <span data-ttu-id="71361-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="71361-110">Example 1</span></span>
```
PS C:\> Export-AzLogAnalyticThrottledRequest -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -GroupByOperationName
```

<span data-ttu-id="71361-111">Ebben a parancsban a Microsoft. számítási API-hívások száma a 2018-02-20T17:54:14 és 2018-02-22T17:54:17 a megadott SAS-URI-ban, a műveleti név alapján összesítve.</span><span class="sxs-lookup"><span data-stu-id="71361-111">This command stores the total throttled Microsoft.Compute API calls between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

## <span data-ttu-id="71361-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="71361-112">PARAMETERS</span></span>

### <span data-ttu-id="71361-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="71361-113">-AsJob</span></span>
<span data-ttu-id="71361-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="71361-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="71361-115">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="71361-115">-BlobContainerSasUri</span></span>
<span data-ttu-id="71361-116">A naplózási blob-tároló SAS URI-ja, amelyre a LogAnalytics API a kimeneti naplókat írja be.</span><span class="sxs-lookup"><span data-stu-id="71361-116">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

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

### <span data-ttu-id="71361-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71361-117">-DefaultProfile</span></span>
<span data-ttu-id="71361-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="71361-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71361-119">-FromTime</span><span class="sxs-lookup"><span data-stu-id="71361-119">-FromTime</span></span>
<span data-ttu-id="71361-120">A lekérdezés időpontjában</span><span class="sxs-lookup"><span data-stu-id="71361-120">From time of the query</span></span>

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

### <span data-ttu-id="71361-121">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="71361-121">-GroupByOperationName</span></span>
<span data-ttu-id="71361-122">Lekérdezés eredményének csoportosítása operáció nevével</span><span class="sxs-lookup"><span data-stu-id="71361-122">Group query result by Operation Name.</span></span>

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

### <span data-ttu-id="71361-123">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="71361-123">-GroupByResourceName</span></span>
<span data-ttu-id="71361-124">Lekérdezési eredmény csoportosítása erőforrás neve szerint</span><span class="sxs-lookup"><span data-stu-id="71361-124">Group query result by Resource Name.</span></span>

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

### <span data-ttu-id="71361-125">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="71361-125">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="71361-126">A lekérdezés eredményének csoportosítása a szabályozási házirend alapján.</span><span class="sxs-lookup"><span data-stu-id="71361-126">Group query result by Throttle Policy applied.</span></span>

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

### <span data-ttu-id="71361-127">-Hely</span><span class="sxs-lookup"><span data-stu-id="71361-127">-Location</span></span>
<span data-ttu-id="71361-128">Az a hely, amelyre a naplózási analitikus lekérdezés van lekérdezve.</span><span class="sxs-lookup"><span data-stu-id="71361-128">The location upon which log analytic is queried.</span></span>

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

### <span data-ttu-id="71361-129">-ToTime</span><span class="sxs-lookup"><span data-stu-id="71361-129">-ToTime</span></span>
<span data-ttu-id="71361-130">A lekérdezés időpontjának időpontja</span><span class="sxs-lookup"><span data-stu-id="71361-130">To time of the query</span></span>

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

### <span data-ttu-id="71361-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="71361-131">-Confirm</span></span>
<span data-ttu-id="71361-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="71361-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71361-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71361-133">-WhatIf</span></span>
<span data-ttu-id="71361-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="71361-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71361-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="71361-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71361-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71361-136">CommonParameters</span></span>
<span data-ttu-id="71361-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="71361-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71361-138">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71361-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71361-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="71361-139">INPUTS</span></span>

### <span data-ttu-id="71361-140">System. String</span><span class="sxs-lookup"><span data-stu-id="71361-140">System.String</span></span>

## <span data-ttu-id="71361-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="71361-141">OUTPUTS</span></span>

### <span data-ttu-id="71361-142">Microsoft. Azure. commands. számítási. Automation. models. PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="71361-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="71361-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="71361-143">NOTES</span></span>

## <span data-ttu-id="71361-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="71361-144">RELATED LINKS</span></span>

