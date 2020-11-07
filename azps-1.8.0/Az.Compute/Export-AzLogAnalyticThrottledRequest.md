---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/export-azloganalyticthrottledrequest
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticThrottledRequest.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticThrottledRequest.md
ms.openlocfilehash: 65a2dd49b0beee557f062201f27a7235c28d5283
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836807"
---
# <span data-ttu-id="cfd26-101">Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="cfd26-101">Export-AzLogAnalyticThrottledRequest</span></span>

## <span data-ttu-id="cfd26-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cfd26-102">SYNOPSIS</span></span>
<span data-ttu-id="cfd26-103">Olyan naplók exportálása, amelyek az adott időablakban az előfizetéshez tartozó összes szabályozott API-kérést megjelenítik.</span><span class="sxs-lookup"><span data-stu-id="cfd26-103">Export logs that show total throttled Api requests for this subscription in the given time window.</span></span>

## <span data-ttu-id="cfd26-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cfd26-104">SYNTAX</span></span>

```
Export-AzLogAnalyticThrottledRequest [-Location] <String> [-FromTime] <DateTime> [-ToTime] <DateTime>
 [-BlobContainerSasUri] <String> [-GroupByOperationName] [-GroupByResourceName] [-GroupByThrottlePolicy]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cfd26-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cfd26-105">DESCRIPTION</span></span>
<span data-ttu-id="cfd26-106">Ezzel exportálja a Microsoft. számítási API-hívások teljes számát.</span><span class="sxs-lookup"><span data-stu-id="cfd26-106">This exports the total number of throttled Microsoft.Compute API calls.</span></span>
<span data-ttu-id="cfd26-107">A naplókat a következő három beállítással lehet összesíteni: GroupByOperationName, GroupByThrottlePolicy vagy GroupByResourceName.</span><span class="sxs-lookup"><span data-stu-id="cfd26-107">The logs can be further aggregated by three options: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="cfd26-108">Felhívjuk a figyelmét arra, hogy a parancsmag csak a CRP-naplókat gyűjti össze.</span><span class="sxs-lookup"><span data-stu-id="cfd26-108">Note that this cmdlet collects only CRP logs.</span></span>

<span data-ttu-id="cfd26-109">A számítási erőforrás szolgáltató API-szabályozásának áttekintése a következő témakörben található: https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits .</span><span class="sxs-lookup"><span data-stu-id="cfd26-109">For an overview of the Compute Resource Provider's API throttling, see https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits.</span></span> 

## <span data-ttu-id="cfd26-110">Példák</span><span class="sxs-lookup"><span data-stu-id="cfd26-110">EXAMPLES</span></span>

### <span data-ttu-id="cfd26-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="cfd26-111">Example 1</span></span>
```
PS C:\> Export-AzLogAnalyticThrottledRequest -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -GroupByOperationName
```

<span data-ttu-id="cfd26-112">Ebben a parancsban a Microsoft. számítási API-hívások száma a 2018-02-20T17:54:14 és 2018-02-22T17:54:17 a megadott SAS-URI-ban, a műveleti név alapján összesítve.</span><span class="sxs-lookup"><span data-stu-id="cfd26-112">This command stores the total throttled Microsoft.Compute API calls between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

## <span data-ttu-id="cfd26-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cfd26-113">PARAMETERS</span></span>

### <span data-ttu-id="cfd26-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cfd26-114">-AsJob</span></span>
<span data-ttu-id="cfd26-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="cfd26-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cfd26-116">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="cfd26-116">-BlobContainerSasUri</span></span>
<span data-ttu-id="cfd26-117">A naplózási blob-tároló SAS URI-ja, amelyre a LogAnalytics API a kimeneti naplókat írja be.</span><span class="sxs-lookup"><span data-stu-id="cfd26-117">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

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

### <span data-ttu-id="cfd26-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfd26-118">-DefaultProfile</span></span>
<span data-ttu-id="cfd26-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cfd26-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cfd26-120">-FromTime</span><span class="sxs-lookup"><span data-stu-id="cfd26-120">-FromTime</span></span>
<span data-ttu-id="cfd26-121">A lekérdezés időpontjában</span><span class="sxs-lookup"><span data-stu-id="cfd26-121">From time of the query</span></span>

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

### <span data-ttu-id="cfd26-122">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="cfd26-122">-GroupByOperationName</span></span>
<span data-ttu-id="cfd26-123">Lekérdezés eredményének csoportosítása operáció nevével</span><span class="sxs-lookup"><span data-stu-id="cfd26-123">Group query result by Operation Name.</span></span>

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

### <span data-ttu-id="cfd26-124">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="cfd26-124">-GroupByResourceName</span></span>
<span data-ttu-id="cfd26-125">Lekérdezési eredmény csoportosítása erőforrás neve szerint</span><span class="sxs-lookup"><span data-stu-id="cfd26-125">Group query result by Resource Name.</span></span>

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

### <span data-ttu-id="cfd26-126">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="cfd26-126">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="cfd26-127">A lekérdezés eredményének csoportosítása a szabályozási házirend alapján.</span><span class="sxs-lookup"><span data-stu-id="cfd26-127">Group query result by Throttle Policy applied.</span></span>

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

### <span data-ttu-id="cfd26-128">-Hely</span><span class="sxs-lookup"><span data-stu-id="cfd26-128">-Location</span></span>
<span data-ttu-id="cfd26-129">Az a hely, amelyre a naplózási analitikus lekérdezés van lekérdezve.</span><span class="sxs-lookup"><span data-stu-id="cfd26-129">The location upon which log analytic is queried.</span></span>

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

### <span data-ttu-id="cfd26-130">-ToTime</span><span class="sxs-lookup"><span data-stu-id="cfd26-130">-ToTime</span></span>
<span data-ttu-id="cfd26-131">A lekérdezés időpontjának időpontja</span><span class="sxs-lookup"><span data-stu-id="cfd26-131">To time of the query</span></span>

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

### <span data-ttu-id="cfd26-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cfd26-132">-Confirm</span></span>
<span data-ttu-id="cfd26-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cfd26-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cfd26-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfd26-134">-WhatIf</span></span>
<span data-ttu-id="cfd26-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cfd26-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cfd26-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cfd26-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cfd26-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfd26-137">CommonParameters</span></span>
<span data-ttu-id="cfd26-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cfd26-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfd26-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfd26-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfd26-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cfd26-140">INPUTS</span></span>

### <span data-ttu-id="cfd26-141">System. String</span><span class="sxs-lookup"><span data-stu-id="cfd26-141">System.String</span></span>

## <span data-ttu-id="cfd26-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cfd26-142">OUTPUTS</span></span>

### <span data-ttu-id="cfd26-143">Microsoft. Azure. commands. számítási. Automation. models. PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="cfd26-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="cfd26-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cfd26-144">NOTES</span></span>

## <span data-ttu-id="cfd26-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cfd26-145">RELATED LINKS</span></span>
