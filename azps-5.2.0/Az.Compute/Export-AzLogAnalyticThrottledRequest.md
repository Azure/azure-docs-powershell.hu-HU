---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/export-azloganalyticthrottledrequest
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticThrottledRequest.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticThrottledRequest.md
ms.openlocfilehash: 79bf599b22796181c2f433f186e0e4bde8094773
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330137"
---
# <span data-ttu-id="7fa46-101">Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="7fa46-101">Export-AzLogAnalyticThrottledRequest</span></span>

## <span data-ttu-id="7fa46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7fa46-102">SYNOPSIS</span></span>
<span data-ttu-id="7fa46-103">Export logs that show total throttled Api requests for this subscription in the given time window.</span><span class="sxs-lookup"><span data-stu-id="7fa46-103">Export logs that show total throttled Api requests for this subscription in the given time window.</span></span>

## <span data-ttu-id="7fa46-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7fa46-104">SYNTAX</span></span>

```
Export-AzLogAnalyticThrottledRequest [-Location] <String> [-FromTime] <DateTime> [-ToTime] <DateTime>
 [-BlobContainerSasUri] <String> [-GroupByOperationName] [-GroupByResourceName] [-GroupByThrottlePolicy]
 [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7fa46-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7fa46-105">DESCRIPTION</span></span>
<span data-ttu-id="7fa46-106">Ez exportálja a leszámolt Microsoft.Compute API-hívások teljes számát.</span><span class="sxs-lookup"><span data-stu-id="7fa46-106">This exports the total number of throttled Microsoft.Compute API calls.</span></span>
<span data-ttu-id="7fa46-107">A naplók további összesítése három lehetőséggel lehetséges: GroupByOperationName, GroupByThrottlePolicy vagy GroupByResourceName.</span><span class="sxs-lookup"><span data-stu-id="7fa46-107">The logs can be further aggregated by three options: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="7fa46-108">Ne feledje, hogy ez a parancsmag csak a CRP-naplókat gyűjti.</span><span class="sxs-lookup"><span data-stu-id="7fa46-108">Note that this cmdlet collects only CRP logs.</span></span>

<span data-ttu-id="7fa46-109">A Számítási erőforrás-szolgáltató API-szabályozásának áttekintése: https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits .</span><span class="sxs-lookup"><span data-stu-id="7fa46-109">For an overview of the Compute Resource Provider's API throttling, see https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits.</span></span> 

## <span data-ttu-id="7fa46-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7fa46-110">EXAMPLES</span></span>

### <span data-ttu-id="7fa46-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="7fa46-111">Example 1</span></span>
```
PS C:\> Export-AzLogAnalyticThrottledRequest -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -GroupByOperationName
```

<span data-ttu-id="7fa46-112">Ez a parancs a 2018–02–20T17:54:14 és a 2018-02-22T17:54:17 közötti összes leszámolt Microsoft.Compute API-hívást tárolja a műveletnévvel összesítve a megadott SAS URI-ban.</span><span class="sxs-lookup"><span data-stu-id="7fa46-112">This command stores the total throttled Microsoft.Compute API calls between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

## <span data-ttu-id="7fa46-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7fa46-113">PARAMETERS</span></span>

### <span data-ttu-id="7fa46-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7fa46-114">-AsJob</span></span>
<span data-ttu-id="7fa46-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="7fa46-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7fa46-116">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="7fa46-116">-BlobContainerSasUri</span></span>
<span data-ttu-id="7fa46-117">A naplózási blobtároló SAS Uri-ja, amelybe a LogAnalytics Api kimeneti naplókat ír.</span><span class="sxs-lookup"><span data-stu-id="7fa46-117">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

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

### <span data-ttu-id="7fa46-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fa46-118">-DefaultProfile</span></span>
<span data-ttu-id="7fa46-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7fa46-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7fa46-120">-FromTime</span><span class="sxs-lookup"><span data-stu-id="7fa46-120">-FromTime</span></span>
<span data-ttu-id="7fa46-121">A lekérdezés időtől</span><span class="sxs-lookup"><span data-stu-id="7fa46-121">From time of the query</span></span>

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

### <span data-ttu-id="7fa46-122">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="7fa46-122">-GroupByOperationName</span></span>
<span data-ttu-id="7fa46-123">A csoportlekérdezés eredménye műveletnév szerint.</span><span class="sxs-lookup"><span data-stu-id="7fa46-123">Group query result by Operation Name.</span></span>

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

### <span data-ttu-id="7fa46-124">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="7fa46-124">-GroupByResourceName</span></span>
<span data-ttu-id="7fa46-125">A csoportlekérdezés eredménye erőforrásnév szerint.</span><span class="sxs-lookup"><span data-stu-id="7fa46-125">Group query result by Resource Name.</span></span>

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

### <span data-ttu-id="7fa46-126">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="7fa46-126">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="7fa46-127">A csoportlekérdezés eredménye a szabálysértés által alkalmazva.</span><span class="sxs-lookup"><span data-stu-id="7fa46-127">Group query result by Throttle Policy applied.</span></span>

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

### <span data-ttu-id="7fa46-128">-Location</span><span class="sxs-lookup"><span data-stu-id="7fa46-128">-Location</span></span>
<span data-ttu-id="7fa46-129">A napló analytic lekérdezésének helye.</span><span class="sxs-lookup"><span data-stu-id="7fa46-129">The location upon which log analytic is queried.</span></span>

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

### <span data-ttu-id="7fa46-130">-NoWait</span><span class="sxs-lookup"><span data-stu-id="7fa46-130">-NoWait</span></span>
<span data-ttu-id="7fa46-131">Elindítja a műveletet, és azonnal, a művelet befejezése előtt visszatér.</span><span class="sxs-lookup"><span data-stu-id="7fa46-131">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="7fa46-132">Ha meg szeretné állapítani, hogy a művelet sikeresen befejeződött-e, használjon más mechanizmust.</span><span class="sxs-lookup"><span data-stu-id="7fa46-132">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="7fa46-133">-ToTime</span><span class="sxs-lookup"><span data-stu-id="7fa46-133">-ToTime</span></span>
<span data-ttu-id="7fa46-134">A lekérdezés ideje</span><span class="sxs-lookup"><span data-stu-id="7fa46-134">To time of the query</span></span>

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

### <span data-ttu-id="7fa46-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7fa46-135">-Confirm</span></span>
<span data-ttu-id="7fa46-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7fa46-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7fa46-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fa46-137">-WhatIf</span></span>
<span data-ttu-id="7fa46-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7fa46-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7fa46-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7fa46-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7fa46-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fa46-140">CommonParameters</span></span>
<span data-ttu-id="7fa46-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fa46-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fa46-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7fa46-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fa46-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7fa46-143">INPUTS</span></span>

### <span data-ttu-id="7fa46-144">System.String</span><span class="sxs-lookup"><span data-stu-id="7fa46-144">System.String</span></span>

## <span data-ttu-id="7fa46-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7fa46-145">OUTPUTS</span></span>

### <span data-ttu-id="7fa46-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="7fa46-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="7fa46-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7fa46-147">NOTES</span></span>

## <span data-ttu-id="7fa46-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7fa46-148">RELATED LINKS</span></span>
