---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/export-azloganalyticthrottledrequest
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticThrottledRequest.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticThrottledRequest.md
ms.openlocfilehash: 79bf599b22796181c2f433f186e0e4bde8094773
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014645"
---
# <span data-ttu-id="a471a-101">Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="a471a-101">Export-AzLogAnalyticThrottledRequest</span></span>

## <span data-ttu-id="a471a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a471a-102">SYNOPSIS</span></span>
<span data-ttu-id="a471a-103">Olyan naplók exportálása, amelyek az adott időablakban az előfizetéshez tartozó összes szabályozott API-kérést megjelenítik.</span><span class="sxs-lookup"><span data-stu-id="a471a-103">Export logs that show total throttled Api requests for this subscription in the given time window.</span></span>

## <span data-ttu-id="a471a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a471a-104">SYNTAX</span></span>

```
Export-AzLogAnalyticThrottledRequest [-Location] <String> [-FromTime] <DateTime> [-ToTime] <DateTime>
 [-BlobContainerSasUri] <String> [-GroupByOperationName] [-GroupByResourceName] [-GroupByThrottlePolicy]
 [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a471a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a471a-105">DESCRIPTION</span></span>
<span data-ttu-id="a471a-106">Ezzel exportálja a Microsoft. számítási API-hívások teljes számát.</span><span class="sxs-lookup"><span data-stu-id="a471a-106">This exports the total number of throttled Microsoft.Compute API calls.</span></span>
<span data-ttu-id="a471a-107">A naplókat a következő három beállítással lehet összesíteni: GroupByOperationName, GroupByThrottlePolicy vagy GroupByResourceName.</span><span class="sxs-lookup"><span data-stu-id="a471a-107">The logs can be further aggregated by three options: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="a471a-108">Felhívjuk a figyelmét arra, hogy a parancsmag csak a CRP-naplókat gyűjti össze.</span><span class="sxs-lookup"><span data-stu-id="a471a-108">Note that this cmdlet collects only CRP logs.</span></span>

<span data-ttu-id="a471a-109">A számítási erőforrás szolgáltató API-szabályozásának áttekintése a következő témakörben található: https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits .</span><span class="sxs-lookup"><span data-stu-id="a471a-109">For an overview of the Compute Resource Provider's API throttling, see https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits.</span></span> 

## <span data-ttu-id="a471a-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a471a-110">EXAMPLES</span></span>

### <span data-ttu-id="a471a-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a471a-111">Example 1</span></span>
```
PS C:\> Export-AzLogAnalyticThrottledRequest -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -GroupByOperationName
```

<span data-ttu-id="a471a-112">Ebben a parancsban a Microsoft. számítási API-hívások száma a 2018-02-20T17:54:14 és 2018-02-22T17:54:17 a megadott SAS-URI-ban, a műveleti név alapján összesítve.</span><span class="sxs-lookup"><span data-stu-id="a471a-112">This command stores the total throttled Microsoft.Compute API calls between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

## <span data-ttu-id="a471a-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a471a-113">PARAMETERS</span></span>

### <span data-ttu-id="a471a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a471a-114">-AsJob</span></span>
<span data-ttu-id="a471a-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="a471a-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a471a-116">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="a471a-116">-BlobContainerSasUri</span></span>
<span data-ttu-id="a471a-117">A naplózási blob-tároló SAS URI-ja, amelyre a LogAnalytics API a kimeneti naplókat írja be.</span><span class="sxs-lookup"><span data-stu-id="a471a-117">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

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

### <span data-ttu-id="a471a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a471a-118">-DefaultProfile</span></span>
<span data-ttu-id="a471a-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a471a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a471a-120">-FromTime</span><span class="sxs-lookup"><span data-stu-id="a471a-120">-FromTime</span></span>
<span data-ttu-id="a471a-121">A lekérdezés időpontjában</span><span class="sxs-lookup"><span data-stu-id="a471a-121">From time of the query</span></span>

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

### <span data-ttu-id="a471a-122">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="a471a-122">-GroupByOperationName</span></span>
<span data-ttu-id="a471a-123">Lekérdezés eredményének csoportosítása operáció nevével</span><span class="sxs-lookup"><span data-stu-id="a471a-123">Group query result by Operation Name.</span></span>

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

### <span data-ttu-id="a471a-124">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="a471a-124">-GroupByResourceName</span></span>
<span data-ttu-id="a471a-125">Lekérdezési eredmény csoportosítása erőforrás neve szerint</span><span class="sxs-lookup"><span data-stu-id="a471a-125">Group query result by Resource Name.</span></span>

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

### <span data-ttu-id="a471a-126">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="a471a-126">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="a471a-127">A lekérdezés eredményének csoportosítása a szabályozási házirend alapján.</span><span class="sxs-lookup"><span data-stu-id="a471a-127">Group query result by Throttle Policy applied.</span></span>

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

### <span data-ttu-id="a471a-128">-Hely</span><span class="sxs-lookup"><span data-stu-id="a471a-128">-Location</span></span>
<span data-ttu-id="a471a-129">Az a hely, amelyre a naplózási analitikus lekérdezés van lekérdezve.</span><span class="sxs-lookup"><span data-stu-id="a471a-129">The location upon which log analytic is queried.</span></span>

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

### <span data-ttu-id="a471a-130">-Várva</span><span class="sxs-lookup"><span data-stu-id="a471a-130">-NoWait</span></span>
<span data-ttu-id="a471a-131">Elindítja a műveletet, és a művelet befejezése előtt azonnal visszaküldi a műveletet.</span><span class="sxs-lookup"><span data-stu-id="a471a-131">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="a471a-132">Ha meg szeretné állapítani, hogy sikerült-e végrehajtani a műveletet, használjon más mechanizmust.</span><span class="sxs-lookup"><span data-stu-id="a471a-132">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="a471a-133">-ToTime</span><span class="sxs-lookup"><span data-stu-id="a471a-133">-ToTime</span></span>
<span data-ttu-id="a471a-134">A lekérdezés időpontjának időpontja</span><span class="sxs-lookup"><span data-stu-id="a471a-134">To time of the query</span></span>

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

### <span data-ttu-id="a471a-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a471a-135">-Confirm</span></span>
<span data-ttu-id="a471a-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a471a-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a471a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a471a-137">-WhatIf</span></span>
<span data-ttu-id="a471a-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a471a-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a471a-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a471a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a471a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a471a-140">CommonParameters</span></span>
<span data-ttu-id="a471a-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a471a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a471a-142">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a471a-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a471a-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a471a-143">INPUTS</span></span>

### <span data-ttu-id="a471a-144">System. String</span><span class="sxs-lookup"><span data-stu-id="a471a-144">System.String</span></span>

## <span data-ttu-id="a471a-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a471a-145">OUTPUTS</span></span>

### <span data-ttu-id="a471a-146">Microsoft. Azure. commands. számítási. Automation. models. PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="a471a-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="a471a-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a471a-147">NOTES</span></span>

## <span data-ttu-id="a471a-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a471a-148">RELATED LINKS</span></span>
