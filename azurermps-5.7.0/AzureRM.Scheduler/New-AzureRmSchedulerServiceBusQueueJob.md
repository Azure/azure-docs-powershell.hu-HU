---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: 52987702-D101-4D5D-852D-2809374292F4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/new-azurermschedulerservicebusqueuejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerServiceBusQueueJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerServiceBusQueueJob.md
ms.openlocfilehash: 7b6596d967d603a3dcecb3d20f9d2396fc00adf8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498836"
---
# <span data-ttu-id="7011b-101">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="7011b-101">New-AzureRmSchedulerServiceBusQueueJob</span></span>

## <span data-ttu-id="7011b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7011b-102">SYNOPSIS</span></span>
<span data-ttu-id="7011b-103">Létrehoz egy Service Bus Queue-feladatot.</span><span class="sxs-lookup"><span data-stu-id="7011b-103">Creates a service bus queue job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7011b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7011b-104">SYNTAX</span></span>

```
New-AzureRmSchedulerServiceBusQueueJob -ResourceGroupName <String> -JobCollectionName <String>
 -JobName <String> -ServiceBusQueueName <String> -ServiceBusNamespace <String>
 -ServiceBusTransportType <String> -ServiceBusMessage <String> -ServiceBusSasKeyName <String>
 -ServiceBusSasKeyValue <String> [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7011b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7011b-105">DESCRIPTION</span></span>
<span data-ttu-id="7011b-106">A **New-AzureRmSchedulerServiceBusQueueJob** parancsmag létrehoz egy szolgáltatás-várólistás feladatot az Azure schedulerben.</span><span class="sxs-lookup"><span data-stu-id="7011b-106">The **New-AzureRmSchedulerServiceBusQueueJob** cmdlet creates a service bus queue job in Azure Scheduler.</span></span>

<span data-ttu-id="7011b-107">Ez a parancsmag a *ErrorActionType* paraméter alapján támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="7011b-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="7011b-108">A dinamikus paraméterek elérhetővé válnak a többi paraméter-érték alapján.</span><span class="sxs-lookup"><span data-stu-id="7011b-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="7011b-109">Ha meg szeretné ismerni a dinamikus paraméterek nevét a többi paraméter megadása után, írjon be egy kötőjelet (-), majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="7011b-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="7011b-110">Ha kihagyja a kötelező paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="7011b-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="7011b-111">Példák</span><span class="sxs-lookup"><span data-stu-id="7011b-111">EXAMPLES</span></span>

## <span data-ttu-id="7011b-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7011b-112">PARAMETERS</span></span>

### <span data-ttu-id="7011b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7011b-113">-DefaultProfile</span></span>
<span data-ttu-id="7011b-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7011b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7011b-115">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="7011b-115">-EndTime</span></span>
<span data-ttu-id="7011b-116">A projekthez tartozó **datetime** -objektum záró időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7011b-116">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="7011b-117">Ha **datetime** típusú objektumot szeretne beolvasni, használja az Get-Date parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="7011b-117">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7011b-118">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="7011b-118">-ErrorActionType</span></span>
<span data-ttu-id="7011b-119">A feladat hibaérték-beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="7011b-119">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="7011b-120">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="7011b-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7011b-121">Http</span><span class="sxs-lookup"><span data-stu-id="7011b-121">Http</span></span> 
- <span data-ttu-id="7011b-122">Https</span><span class="sxs-lookup"><span data-stu-id="7011b-122">Https</span></span> 
- <span data-ttu-id="7011b-123">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="7011b-123">StorageQueue</span></span> 
- <span data-ttu-id="7011b-124">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="7011b-124">ServiceBusQueue</span></span> 
- <span data-ttu-id="7011b-125">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="7011b-125">ServiceBusTopic</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Https, StorageQueue, ServiceBusQueue, ServiceBusTopic

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7011b-126">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="7011b-126">-ExecutionCount</span></span>
<span data-ttu-id="7011b-127">Itt adhatja meg, hogy hányszor fusson a feladat.</span><span class="sxs-lookup"><span data-stu-id="7011b-127">Specifies how many times the job runs.</span></span>
<span data-ttu-id="7011b-128">Alapértelmezés szerint a feladat határozatlan ideig ismétlődik.</span><span class="sxs-lookup"><span data-stu-id="7011b-128">By default, a job recurs indefinitely.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7011b-129">-Gyakoriság</span><span class="sxs-lookup"><span data-stu-id="7011b-129">-Frequency</span></span>
<span data-ttu-id="7011b-130">A feladat gyakoriságát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7011b-130">Specifies a frequency for the job.</span></span>
<span data-ttu-id="7011b-131">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="7011b-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7011b-132">Perces</span><span class="sxs-lookup"><span data-stu-id="7011b-132">Minute</span></span> 
- <span data-ttu-id="7011b-133">Óra</span><span class="sxs-lookup"><span data-stu-id="7011b-133">Hour</span></span> 
- <span data-ttu-id="7011b-134">Nap</span><span class="sxs-lookup"><span data-stu-id="7011b-134">Day</span></span> 
- <span data-ttu-id="7011b-135">Héten</span><span class="sxs-lookup"><span data-stu-id="7011b-135">Week</span></span> 
- <span data-ttu-id="7011b-136">Hónap</span><span class="sxs-lookup"><span data-stu-id="7011b-136">Month</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Minute, Hour, Day, Week, Month

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7011b-137">-Intervallum</span><span class="sxs-lookup"><span data-stu-id="7011b-137">-Interval</span></span>
<span data-ttu-id="7011b-138">A feladat ismétlődésének intervallumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7011b-138">Specifies an interval of recurrence for the job.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7011b-139">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="7011b-139">-JobCollectionName</span></span>
<span data-ttu-id="7011b-140">Annak a feladatnak a neve, amelyhez a projekt tartozik.</span><span class="sxs-lookup"><span data-stu-id="7011b-140">Specifies the name of the job collection to which the job belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7011b-141">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="7011b-141">-JobName</span></span>
<span data-ttu-id="7011b-142">A feladat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7011b-142">Specifies a name for the job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7011b-143">-JobState</span><span class="sxs-lookup"><span data-stu-id="7011b-143">-JobState</span></span>
<span data-ttu-id="7011b-144">A feladat állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7011b-144">Specifies the state of the job.</span></span>
<span data-ttu-id="7011b-145">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="7011b-145">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7011b-146">Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="7011b-146">Enabled</span></span> 
- <span data-ttu-id="7011b-147">Tiltva</span><span class="sxs-lookup"><span data-stu-id="7011b-147">Disabled</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7011b-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7011b-148">-ResourceGroupName</span></span>
<span data-ttu-id="7011b-149">Azt az erőforráscsoport-csoportot adja meg, amelyhez a projekt tartozik.</span><span class="sxs-lookup"><span data-stu-id="7011b-149">Specifies the resource group to which the job belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7011b-150">-ServiceBusMessage</span><span class="sxs-lookup"><span data-stu-id="7011b-150">-ServiceBusMessage</span></span>
<span data-ttu-id="7011b-151">A szolgáltatás busz várólistájának üzenetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7011b-151">Specifies a service bus queue message.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7011b-152">-ServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="7011b-152">-ServiceBusNamespace</span></span>
<span data-ttu-id="7011b-153">A szolgáltatás busz-névteret adja meg.</span><span class="sxs-lookup"><span data-stu-id="7011b-153">Specifies a service bus namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7011b-154">-ServiceBusQueueName</span><span class="sxs-lookup"><span data-stu-id="7011b-154">-ServiceBusQueueName</span></span>
<span data-ttu-id="7011b-155">A szolgáltatás buszjának várólista-nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7011b-155">Specifies a service bus queue name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7011b-156">-ServiceBusSasKeyName</span><span class="sxs-lookup"><span data-stu-id="7011b-156">-ServiceBusSasKeyName</span></span>
<span data-ttu-id="7011b-157">Egy megosztott Access-aláírási kulcs nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7011b-157">Specifies a shared access signature key name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7011b-158">-ServiceBusSasKeyValue</span><span class="sxs-lookup"><span data-stu-id="7011b-158">-ServiceBusSasKeyValue</span></span>
<span data-ttu-id="7011b-159">A megosztott hozzáférés-aláírási kulcs értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7011b-159">Specifies a shared access signature key value.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7011b-160">-ServiceBusTransportType</span><span class="sxs-lookup"><span data-stu-id="7011b-160">-ServiceBusTransportType</span></span>
<span data-ttu-id="7011b-161">A szolgáltatás busz-átviteli típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7011b-161">Specifies a service bus transport type.</span></span>
<span data-ttu-id="7011b-162">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="7011b-162">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7011b-163">NetMessaging</span><span class="sxs-lookup"><span data-stu-id="7011b-163">NetMessaging</span></span> 
- <span data-ttu-id="7011b-164">AMQP</span><span class="sxs-lookup"><span data-stu-id="7011b-164">AMQP</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: NetMessaging, AMQP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7011b-165">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="7011b-165">-StartTime</span></span>
<span data-ttu-id="7011b-166">A projekthez tartozó **datetime** -objektum kezdési időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7011b-166">Specifies the start time, as a **DateTime** object, for the job.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7011b-167">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7011b-167">-Confirm</span></span>
<span data-ttu-id="7011b-168">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7011b-168">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7011b-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7011b-169">-WhatIf</span></span>
<span data-ttu-id="7011b-170">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7011b-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7011b-171">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7011b-171">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7011b-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7011b-172">CommonParameters</span></span>
<span data-ttu-id="7011b-173">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7011b-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7011b-174">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7011b-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7011b-175">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7011b-175">INPUTS</span></span>

### <span data-ttu-id="7011b-176">Nincs</span><span class="sxs-lookup"><span data-stu-id="7011b-176">None</span></span>
<span data-ttu-id="7011b-177">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="7011b-177">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7011b-178">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7011b-178">OUTPUTS</span></span>

### <span data-ttu-id="7011b-179">Microsoft. Azure. Command. Scheduler. models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="7011b-179">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="7011b-180">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7011b-180">NOTES</span></span>

## <span data-ttu-id="7011b-181">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7011b-181">RELATED LINKS</span></span>

[<span data-ttu-id="7011b-182">Új – AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="7011b-182">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="7011b-183">Új – AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="7011b-183">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="7011b-184">Új – AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="7011b-184">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="7011b-185">Új – AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="7011b-185">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="7011b-186">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="7011b-186">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="7011b-187">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="7011b-187">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="7011b-188">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="7011b-188">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="7011b-189">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="7011b-189">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="7011b-190">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="7011b-190">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


