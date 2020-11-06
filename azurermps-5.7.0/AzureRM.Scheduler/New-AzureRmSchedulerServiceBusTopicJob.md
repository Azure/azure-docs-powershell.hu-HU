---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: 2B9FEEDB-09AA-40B6-B42C-F9090F54EB3B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/new-azurermschedulerservicebustopicjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerServiceBusTopicJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerServiceBusTopicJob.md
ms.openlocfilehash: ecd801cff6a6cc67a4187e7f89b26e8b5edb3784
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498835"
---
# <span data-ttu-id="2785d-101">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="2785d-101">New-AzureRmSchedulerServiceBusTopicJob</span></span>

## <span data-ttu-id="2785d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2785d-102">SYNOPSIS</span></span>
<span data-ttu-id="2785d-103">Létrehoz egy szolgáltatás busz-témakört.</span><span class="sxs-lookup"><span data-stu-id="2785d-103">Creates a service bus topic job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2785d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2785d-104">SYNTAX</span></span>

```
New-AzureRmSchedulerServiceBusTopicJob -ResourceGroupName <String> -JobCollectionName <String>
 -JobName <String> -ServiceBusTopicPath <String> -ServiceBusNamespace <String>
 -ServiceBusTransportType <String> -ServiceBusMessage <String> -ServiceBusSasKeyName <String>
 -ServiceBusSasKeyValue <String> [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2785d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2785d-105">DESCRIPTION</span></span>
<span data-ttu-id="2785d-106">A **New-AzureRmSchedulerServiceBusTopicJob** parancsmag az Azure Scheduler szolgáltatásban létrehoz egy szolgáltatási busz témakört.</span><span class="sxs-lookup"><span data-stu-id="2785d-106">The **New-AzureRmSchedulerServiceBusTopicJob** cmdlet creates a service bus topic job in Azure Scheduler.</span></span>

<span data-ttu-id="2785d-107">Ez a parancsmag a *ErrorActionType* paraméter alapján támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="2785d-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="2785d-108">A dinamikus paraméterek elérhetővé válnak a többi paraméter-érték alapján.</span><span class="sxs-lookup"><span data-stu-id="2785d-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="2785d-109">Ha meg szeretné ismerni a dinamikus paraméterek nevét a többi paraméter megadása után, írjon be egy kötőjelet (-), majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="2785d-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="2785d-110">Ha kihagyja a kötelező paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="2785d-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="2785d-111">Példák</span><span class="sxs-lookup"><span data-stu-id="2785d-111">EXAMPLES</span></span>

## <span data-ttu-id="2785d-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2785d-112">PARAMETERS</span></span>

### <span data-ttu-id="2785d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2785d-113">-DefaultProfile</span></span>
<span data-ttu-id="2785d-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2785d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2785d-115">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="2785d-115">-EndTime</span></span>
<span data-ttu-id="2785d-116">A projekthez tartozó **datetime** -objektum záró időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2785d-116">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="2785d-117">Ha **datetime** típusú objektumot szeretne beolvasni, használja az Get-Date parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="2785d-117">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="2785d-118">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="2785d-118">-ErrorActionType</span></span>
<span data-ttu-id="2785d-119">A feladat hibaérték-beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="2785d-119">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="2785d-120">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="2785d-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2785d-121">Http</span><span class="sxs-lookup"><span data-stu-id="2785d-121">Http</span></span> 
- <span data-ttu-id="2785d-122">Https</span><span class="sxs-lookup"><span data-stu-id="2785d-122">Https</span></span> 
- <span data-ttu-id="2785d-123">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="2785d-123">StorageQueue</span></span> 
- <span data-ttu-id="2785d-124">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="2785d-124">ServiceBusQueue</span></span> 
- <span data-ttu-id="2785d-125">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="2785d-125">ServiceBusTopic</span></span>

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

### <span data-ttu-id="2785d-126">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="2785d-126">-ExecutionCount</span></span>
<span data-ttu-id="2785d-127">Itt adhatja meg, hogy hányszor fusson a feladat.</span><span class="sxs-lookup"><span data-stu-id="2785d-127">Specifies how many times the job runs.</span></span>
<span data-ttu-id="2785d-128">Alapértelmezés szerint a feladat határozatlan ideig ismétlődik.</span><span class="sxs-lookup"><span data-stu-id="2785d-128">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="2785d-129">-Gyakoriság</span><span class="sxs-lookup"><span data-stu-id="2785d-129">-Frequency</span></span>
<span data-ttu-id="2785d-130">A feladat maximális gyakoriságát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2785d-130">Specifies a maximum frequency for the job.</span></span>
<span data-ttu-id="2785d-131">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="2785d-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2785d-132">Perces</span><span class="sxs-lookup"><span data-stu-id="2785d-132">Minute</span></span> 
- <span data-ttu-id="2785d-133">Óra</span><span class="sxs-lookup"><span data-stu-id="2785d-133">Hour</span></span> 
- <span data-ttu-id="2785d-134">Nap</span><span class="sxs-lookup"><span data-stu-id="2785d-134">Day</span></span> 
- <span data-ttu-id="2785d-135">Héten</span><span class="sxs-lookup"><span data-stu-id="2785d-135">Week</span></span> 
- <span data-ttu-id="2785d-136">Hónap</span><span class="sxs-lookup"><span data-stu-id="2785d-136">Month</span></span>

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

### <span data-ttu-id="2785d-137">-Intervallum</span><span class="sxs-lookup"><span data-stu-id="2785d-137">-Interval</span></span>
<span data-ttu-id="2785d-138">A feladat ismétlődésének intervallumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2785d-138">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="2785d-139">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="2785d-139">-JobCollectionName</span></span>
<span data-ttu-id="2785d-140">Annak a feladatnak a neve, amelyhez a projekt tartozik.</span><span class="sxs-lookup"><span data-stu-id="2785d-140">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="2785d-141">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="2785d-141">-JobName</span></span>
<span data-ttu-id="2785d-142">A feladat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2785d-142">Specifies a name for the job.</span></span>

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

### <span data-ttu-id="2785d-143">-JobState</span><span class="sxs-lookup"><span data-stu-id="2785d-143">-JobState</span></span>
<span data-ttu-id="2785d-144">A feladat állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2785d-144">Specifies the state of the job.</span></span>
<span data-ttu-id="2785d-145">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="2785d-145">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2785d-146">Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="2785d-146">Enabled</span></span> 
- <span data-ttu-id="2785d-147">Tiltva</span><span class="sxs-lookup"><span data-stu-id="2785d-147">Disabled</span></span>

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

### <span data-ttu-id="2785d-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2785d-148">-ResourceGroupName</span></span>
<span data-ttu-id="2785d-149">Azt az erőforráscsoport-csoportot adja meg, amelyhez a projekt tartozik.</span><span class="sxs-lookup"><span data-stu-id="2785d-149">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="2785d-150">-ServiceBusMessage</span><span class="sxs-lookup"><span data-stu-id="2785d-150">-ServiceBusMessage</span></span>
<span data-ttu-id="2785d-151">A szolgáltatás buszjának témáját tartalmazó üzenetet adja meg.</span><span class="sxs-lookup"><span data-stu-id="2785d-151">Specifies a service bus topic message.</span></span>

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

### <span data-ttu-id="2785d-152">-ServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="2785d-152">-ServiceBusNamespace</span></span>
<span data-ttu-id="2785d-153">A szolgáltatás busz-névteret adja meg.</span><span class="sxs-lookup"><span data-stu-id="2785d-153">Specifies a service bus namespace.</span></span>

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

### <span data-ttu-id="2785d-154">-ServiceBusSasKeyName</span><span class="sxs-lookup"><span data-stu-id="2785d-154">-ServiceBusSasKeyName</span></span>
<span data-ttu-id="2785d-155">Egy megosztott Access-aláírási kulcs nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2785d-155">Specifies a shared access signature key name.</span></span>

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

### <span data-ttu-id="2785d-156">-ServiceBusSasKeyValue</span><span class="sxs-lookup"><span data-stu-id="2785d-156">-ServiceBusSasKeyValue</span></span>
<span data-ttu-id="2785d-157">A megosztott hozzáférés-aláírási kulcs értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2785d-157">Specifies a shared access signature key value.</span></span>

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

### <span data-ttu-id="2785d-158">-ServiceBusTopicPath</span><span class="sxs-lookup"><span data-stu-id="2785d-158">-ServiceBusTopicPath</span></span>
<span data-ttu-id="2785d-159">A szolgáltatás buszja témakör elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2785d-159">Specifies a service bus topic path.</span></span>

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

### <span data-ttu-id="2785d-160">-ServiceBusTransportType</span><span class="sxs-lookup"><span data-stu-id="2785d-160">-ServiceBusTransportType</span></span>
<span data-ttu-id="2785d-161">A szolgáltatás busz-átviteli típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2785d-161">Specifies a service bus transport type.</span></span>
<span data-ttu-id="2785d-162">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="2785d-162">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2785d-163">NetMessaging</span><span class="sxs-lookup"><span data-stu-id="2785d-163">NetMessaging</span></span>
- <span data-ttu-id="2785d-164">AMQP</span><span class="sxs-lookup"><span data-stu-id="2785d-164">AMQP</span></span>

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

### <span data-ttu-id="2785d-165">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="2785d-165">-StartTime</span></span>
<span data-ttu-id="2785d-166">A projekthez tartozó **datetime** -objektum kezdési időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2785d-166">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="2785d-167">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2785d-167">-Confirm</span></span>
<span data-ttu-id="2785d-168">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2785d-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2785d-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2785d-169">-WhatIf</span></span>
<span data-ttu-id="2785d-170">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2785d-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2785d-171">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2785d-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2785d-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2785d-172">CommonParameters</span></span>
<span data-ttu-id="2785d-173">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2785d-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2785d-174">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2785d-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2785d-175">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2785d-175">INPUTS</span></span>

### <span data-ttu-id="2785d-176">Nincs</span><span class="sxs-lookup"><span data-stu-id="2785d-176">None</span></span>
<span data-ttu-id="2785d-177">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="2785d-177">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2785d-178">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2785d-178">OUTPUTS</span></span>

### <span data-ttu-id="2785d-179">Microsoft. Azure. Command. Scheduler. models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="2785d-179">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="2785d-180">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2785d-180">NOTES</span></span>

## <span data-ttu-id="2785d-181">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2785d-181">RELATED LINKS</span></span>

[<span data-ttu-id="2785d-182">Új – AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="2785d-182">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="2785d-183">Új – AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="2785d-183">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="2785d-184">Új – AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="2785d-184">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="2785d-185">Új – AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="2785d-185">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="2785d-186">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="2785d-186">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="2785d-187">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="2785d-187">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="2785d-188">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="2785d-188">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="2785d-189">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="2785d-189">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="2785d-190">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="2785d-190">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


