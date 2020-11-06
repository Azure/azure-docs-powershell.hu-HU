---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: 52987702-D101-4D5D-852D-2809374292F4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/new-azurermschedulerservicebusqueuejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerServiceBusQueueJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerServiceBusQueueJob.md
ms.openlocfilehash: 0382362c16ba65aa194029677cf8ca846e93db54
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492748"
---
# <span data-ttu-id="9d404-101">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="9d404-101">New-AzureRmSchedulerServiceBusQueueJob</span></span>

## <span data-ttu-id="9d404-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9d404-102">SYNOPSIS</span></span>
<span data-ttu-id="9d404-103">Létrehoz egy Service Bus Queue-feladatot.</span><span class="sxs-lookup"><span data-stu-id="9d404-103">Creates a service bus queue job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d404-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9d404-104">SYNTAX</span></span>

```
New-AzureRmSchedulerServiceBusQueueJob -ResourceGroupName <String> -JobCollectionName <String>
 -JobName <String> -ServiceBusQueueName <String> -ServiceBusNamespace <String>
 -ServiceBusTransportType <String> -ServiceBusMessage <String> -ServiceBusSasKeyName <String>
 -ServiceBusSasKeyValue <String> [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d404-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9d404-105">DESCRIPTION</span></span>
<span data-ttu-id="9d404-106">A **New-AzureRmSchedulerServiceBusQueueJob** parancsmag létrehoz egy szolgáltatás-várólistás feladatot az Azure schedulerben.</span><span class="sxs-lookup"><span data-stu-id="9d404-106">The **New-AzureRmSchedulerServiceBusQueueJob** cmdlet creates a service bus queue job in Azure Scheduler.</span></span>
<span data-ttu-id="9d404-107">Ez a parancsmag a *ErrorActionType* paraméter alapján támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="9d404-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="9d404-108">A dinamikus paraméterek elérhetővé válnak a többi paraméter-érték alapján.</span><span class="sxs-lookup"><span data-stu-id="9d404-108">Dynamic parameters become available based on other parameter values.</span></span>
<span data-ttu-id="9d404-109">Ha meg szeretné ismerni a dinamikus paraméterek nevét a többi paraméter megadása után, írjon be egy kötőjelet (-), majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="9d404-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="9d404-110">Ha kihagyja a kötelező paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="9d404-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="9d404-111">Példák</span><span class="sxs-lookup"><span data-stu-id="9d404-111">EXAMPLES</span></span>

## <span data-ttu-id="9d404-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9d404-112">PARAMETERS</span></span>

### <span data-ttu-id="9d404-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d404-113">-DefaultProfile</span></span>
<span data-ttu-id="9d404-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9d404-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d404-115">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="9d404-115">-EndTime</span></span>
<span data-ttu-id="9d404-116">A projekthez tartozó **datetime** -objektum záró időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="9d404-116">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="9d404-117">Ha **datetime** típusú objektumot szeretne beolvasni, használja az Get-Date parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="9d404-117">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d404-118">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="9d404-118">-ErrorActionType</span></span>
<span data-ttu-id="9d404-119">A feladat hibaérték-beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="9d404-119">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="9d404-120">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="9d404-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9d404-121">Http</span><span class="sxs-lookup"><span data-stu-id="9d404-121">Http</span></span> 
- <span data-ttu-id="9d404-122">Https</span><span class="sxs-lookup"><span data-stu-id="9d404-122">Https</span></span> 
- <span data-ttu-id="9d404-123">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="9d404-123">StorageQueue</span></span> 
- <span data-ttu-id="9d404-124">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="9d404-124">ServiceBusQueue</span></span> 
- <span data-ttu-id="9d404-125">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="9d404-125">ServiceBusTopic</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https, StorageQueue, ServiceBusQueue, ServiceBusTopic

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d404-126">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="9d404-126">-ExecutionCount</span></span>
<span data-ttu-id="9d404-127">Itt adhatja meg, hogy hányszor fusson a feladat.</span><span class="sxs-lookup"><span data-stu-id="9d404-127">Specifies how many times the job runs.</span></span>
<span data-ttu-id="9d404-128">Alapértelmezés szerint a feladat határozatlan ideig ismétlődik.</span><span class="sxs-lookup"><span data-stu-id="9d404-128">By default, a job recurs indefinitely.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d404-129">-Gyakoriság</span><span class="sxs-lookup"><span data-stu-id="9d404-129">-Frequency</span></span>
<span data-ttu-id="9d404-130">A feladat gyakoriságát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9d404-130">Specifies a frequency for the job.</span></span>
<span data-ttu-id="9d404-131">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="9d404-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9d404-132">Perces</span><span class="sxs-lookup"><span data-stu-id="9d404-132">Minute</span></span> 
- <span data-ttu-id="9d404-133">Óra</span><span class="sxs-lookup"><span data-stu-id="9d404-133">Hour</span></span> 
- <span data-ttu-id="9d404-134">Nap</span><span class="sxs-lookup"><span data-stu-id="9d404-134">Day</span></span> 
- <span data-ttu-id="9d404-135">Héten</span><span class="sxs-lookup"><span data-stu-id="9d404-135">Week</span></span> 
- <span data-ttu-id="9d404-136">Hónap</span><span class="sxs-lookup"><span data-stu-id="9d404-136">Month</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Minute, Hour, Day, Week, Month

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d404-137">-Intervallum</span><span class="sxs-lookup"><span data-stu-id="9d404-137">-Interval</span></span>
<span data-ttu-id="9d404-138">A feladat ismétlődésének intervallumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9d404-138">Specifies an interval of recurrence for the job.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d404-139">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="9d404-139">-JobCollectionName</span></span>
<span data-ttu-id="9d404-140">Annak a feladatnak a neve, amelyhez a projekt tartozik.</span><span class="sxs-lookup"><span data-stu-id="9d404-140">Specifies the name of the job collection to which the job belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d404-141">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="9d404-141">-JobName</span></span>
<span data-ttu-id="9d404-142">A feladat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9d404-142">Specifies a name for the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d404-143">-JobState</span><span class="sxs-lookup"><span data-stu-id="9d404-143">-JobState</span></span>
<span data-ttu-id="9d404-144">A feladat állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9d404-144">Specifies the state of the job.</span></span>
<span data-ttu-id="9d404-145">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="9d404-145">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9d404-146">Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="9d404-146">Enabled</span></span> 
- <span data-ttu-id="9d404-147">Tiltva</span><span class="sxs-lookup"><span data-stu-id="9d404-147">Disabled</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d404-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d404-148">-ResourceGroupName</span></span>
<span data-ttu-id="9d404-149">Azt az erőforráscsoport-csoportot adja meg, amelyhez a projekt tartozik.</span><span class="sxs-lookup"><span data-stu-id="9d404-149">Specifies the resource group to which the job belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d404-150">-ServiceBusMessage</span><span class="sxs-lookup"><span data-stu-id="9d404-150">-ServiceBusMessage</span></span>
<span data-ttu-id="9d404-151">A szolgáltatás busz várólistájának üzenetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9d404-151">Specifies a service bus queue message.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d404-152">-ServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="9d404-152">-ServiceBusNamespace</span></span>
<span data-ttu-id="9d404-153">A szolgáltatás busz-névteret adja meg.</span><span class="sxs-lookup"><span data-stu-id="9d404-153">Specifies a service bus namespace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d404-154">-ServiceBusQueueName</span><span class="sxs-lookup"><span data-stu-id="9d404-154">-ServiceBusQueueName</span></span>
<span data-ttu-id="9d404-155">A szolgáltatás buszjának várólista-nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9d404-155">Specifies a service bus queue name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d404-156">-ServiceBusSasKeyName</span><span class="sxs-lookup"><span data-stu-id="9d404-156">-ServiceBusSasKeyName</span></span>
<span data-ttu-id="9d404-157">Egy megosztott Access-aláírási kulcs nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9d404-157">Specifies a shared access signature key name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d404-158">-ServiceBusSasKeyValue</span><span class="sxs-lookup"><span data-stu-id="9d404-158">-ServiceBusSasKeyValue</span></span>
<span data-ttu-id="9d404-159">A megosztott hozzáférés-aláírási kulcs értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9d404-159">Specifies a shared access signature key value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d404-160">-ServiceBusTransportType</span><span class="sxs-lookup"><span data-stu-id="9d404-160">-ServiceBusTransportType</span></span>
<span data-ttu-id="9d404-161">A szolgáltatás busz-átviteli típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9d404-161">Specifies a service bus transport type.</span></span>
<span data-ttu-id="9d404-162">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="9d404-162">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9d404-163">NetMessaging</span><span class="sxs-lookup"><span data-stu-id="9d404-163">NetMessaging</span></span> 
- <span data-ttu-id="9d404-164">AMQP</span><span class="sxs-lookup"><span data-stu-id="9d404-164">AMQP</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NetMessaging, AMQP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d404-165">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="9d404-165">-StartTime</span></span>
<span data-ttu-id="9d404-166">A projekthez tartozó **datetime** -objektum kezdési időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="9d404-166">Specifies the start time, as a **DateTime** object, for the job.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d404-167">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9d404-167">-Confirm</span></span>
<span data-ttu-id="9d404-168">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9d404-168">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d404-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d404-169">-WhatIf</span></span>
<span data-ttu-id="9d404-170">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9d404-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d404-171">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9d404-171">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d404-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d404-172">CommonParameters</span></span>
<span data-ttu-id="9d404-173">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9d404-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d404-174">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d404-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d404-175">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9d404-175">INPUTS</span></span>

### <span data-ttu-id="9d404-176">System. String</span><span class="sxs-lookup"><span data-stu-id="9d404-176">System.String</span></span>

## <span data-ttu-id="9d404-177">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9d404-177">OUTPUTS</span></span>

### <span data-ttu-id="9d404-178">Microsoft. Azure. Command. Scheduler. models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="9d404-178">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="9d404-179">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9d404-179">NOTES</span></span>

## <span data-ttu-id="9d404-180">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9d404-180">RELATED LINKS</span></span>

[<span data-ttu-id="9d404-181">Új – AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="9d404-181">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="9d404-182">Új – AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="9d404-182">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="9d404-183">Új – AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="9d404-183">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="9d404-184">Új – AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="9d404-184">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="9d404-185">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="9d404-185">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="9d404-186">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="9d404-186">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="9d404-187">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="9d404-187">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="9d404-188">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="9d404-188">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="9d404-189">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="9d404-189">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


