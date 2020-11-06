---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: F6B24F96-6016-4645-9F92-F584B73657D5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/set-azurermschedulerservicebustopicjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerServiceBusTopicJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerServiceBusTopicJob.md
ms.openlocfilehash: 7da7382359202f3856309c24a3ea484bd9b3e9e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493019"
---
# <span data-ttu-id="b76eb-101">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="b76eb-101">Set-AzureRmSchedulerServiceBusTopicJob</span></span>

## <span data-ttu-id="b76eb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b76eb-102">SYNOPSIS</span></span>
<span data-ttu-id="b76eb-103">Egy szolgáltatási busz témakörének módosítása.</span><span class="sxs-lookup"><span data-stu-id="b76eb-103">Modifies a service bus topic job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b76eb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b76eb-104">SYNTAX</span></span>

```
Set-AzureRmSchedulerServiceBusTopicJob -ResourceGroupName <String> -JobCollectionName <String>
 -JobName <String> -ServiceBusTopicPath <String> -ServiceBusNamespace <String>
 -ServiceBusTransportType <String> -ServiceBusMessage <String> -ServiceBusSasKeyName <String>
 -ServiceBusSasKeyValue <String> [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b76eb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b76eb-105">DESCRIPTION</span></span>
<span data-ttu-id="b76eb-106">A **set-AzureRmSchedulerServiceBusTopicJob** parancsmag az Azure Scheduler szolgáltatásban módosítja a szolgáltatási busz témakört.</span><span class="sxs-lookup"><span data-stu-id="b76eb-106">The **Set-AzureRmSchedulerServiceBusTopicJob** cmdlet modifies a service bus topic job in Azure Scheduler.</span></span>

<span data-ttu-id="b76eb-107">Ez a parancsmag a *ErrorActionType* paraméter alapján támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="b76eb-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="b76eb-108">A dinamikus paraméterek elérhetővé válnak a többi paraméter-érték alapján.</span><span class="sxs-lookup"><span data-stu-id="b76eb-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="b76eb-109">Ha meg szeretné ismerni a dinamikus paraméterek nevét a többi paraméter megadása után, írjon be egy kötőjelet (-), majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="b76eb-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="b76eb-110">Ha kihagyja a kötelező paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="b76eb-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="b76eb-111">Példák</span><span class="sxs-lookup"><span data-stu-id="b76eb-111">EXAMPLES</span></span>

## <span data-ttu-id="b76eb-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b76eb-112">PARAMETERS</span></span>

### <span data-ttu-id="b76eb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b76eb-113">-DefaultProfile</span></span>
<span data-ttu-id="b76eb-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b76eb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b76eb-115">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="b76eb-115">-EndTime</span></span>
<span data-ttu-id="b76eb-116">A projekthez tartozó **datetime** -objektum záró időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b76eb-116">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="b76eb-117">Ha **datetime** típusú objektumot szeretne beolvasni, használja az Get-Date parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="b76eb-117">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="b76eb-118">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="b76eb-118">-ErrorActionType</span></span>
<span data-ttu-id="b76eb-119">A feladat hibaérték-beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="b76eb-119">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="b76eb-120">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="b76eb-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b76eb-121">Http</span><span class="sxs-lookup"><span data-stu-id="b76eb-121">Http</span></span> 
- <span data-ttu-id="b76eb-122">Https</span><span class="sxs-lookup"><span data-stu-id="b76eb-122">Https</span></span> 
- <span data-ttu-id="b76eb-123">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="b76eb-123">StorageQueue</span></span> 
- <span data-ttu-id="b76eb-124">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="b76eb-124">ServiceBusQueue</span></span> 
- <span data-ttu-id="b76eb-125">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="b76eb-125">ServiceBusTopic</span></span>

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

### <span data-ttu-id="b76eb-126">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="b76eb-126">-ExecutionCount</span></span>
<span data-ttu-id="b76eb-127">Itt adhatja meg, hogy hányszor fusson a feladat.</span><span class="sxs-lookup"><span data-stu-id="b76eb-127">Specifies how many times the job runs.</span></span>
<span data-ttu-id="b76eb-128">Alapértelmezés szerint a feladat határozatlan ideig ismétlődik.</span><span class="sxs-lookup"><span data-stu-id="b76eb-128">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="b76eb-129">-Gyakoriság</span><span class="sxs-lookup"><span data-stu-id="b76eb-129">-Frequency</span></span>
<span data-ttu-id="b76eb-130">A feladat maximális gyakoriságát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b76eb-130">Specifies a maximum frequency for the job.</span></span>
<span data-ttu-id="b76eb-131">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="b76eb-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b76eb-132">Perces</span><span class="sxs-lookup"><span data-stu-id="b76eb-132">Minute</span></span> 
- <span data-ttu-id="b76eb-133">Óra</span><span class="sxs-lookup"><span data-stu-id="b76eb-133">Hour</span></span> 
- <span data-ttu-id="b76eb-134">Nap</span><span class="sxs-lookup"><span data-stu-id="b76eb-134">Day</span></span> 
- <span data-ttu-id="b76eb-135">Héten</span><span class="sxs-lookup"><span data-stu-id="b76eb-135">Week</span></span> 
- <span data-ttu-id="b76eb-136">Hónap</span><span class="sxs-lookup"><span data-stu-id="b76eb-136">Month</span></span>

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

### <span data-ttu-id="b76eb-137">-Intervallum</span><span class="sxs-lookup"><span data-stu-id="b76eb-137">-Interval</span></span>
<span data-ttu-id="b76eb-138">A feladat ismétlődésének intervallumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b76eb-138">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="b76eb-139">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="b76eb-139">-JobCollectionName</span></span>
<span data-ttu-id="b76eb-140">Annak a feladatnak a neve, amelyhez a projekt tartozik.</span><span class="sxs-lookup"><span data-stu-id="b76eb-140">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="b76eb-141">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="b76eb-141">-JobName</span></span>
<span data-ttu-id="b76eb-142">Annak a feladatnak a nevét adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="b76eb-142">Specifies the name of the job that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="b76eb-143">-JobState</span><span class="sxs-lookup"><span data-stu-id="b76eb-143">-JobState</span></span>
<span data-ttu-id="b76eb-144">A feladat állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b76eb-144">Specifies the state of the job.</span></span>
<span data-ttu-id="b76eb-145">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="b76eb-145">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b76eb-146">Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="b76eb-146">Enabled</span></span> 
- <span data-ttu-id="b76eb-147">Tiltva</span><span class="sxs-lookup"><span data-stu-id="b76eb-147">Disabled</span></span>

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

### <span data-ttu-id="b76eb-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b76eb-148">-ResourceGroupName</span></span>
<span data-ttu-id="b76eb-149">Azt az erőforráscsoport-csoportot adja meg, amelyhez a projekt tartozik.</span><span class="sxs-lookup"><span data-stu-id="b76eb-149">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="b76eb-150">-ServiceBusMessage</span><span class="sxs-lookup"><span data-stu-id="b76eb-150">-ServiceBusMessage</span></span>
<span data-ttu-id="b76eb-151">A szolgáltatás buszjának témáját tartalmazó üzenetet adja meg.</span><span class="sxs-lookup"><span data-stu-id="b76eb-151">Specifies a service bus topic message.</span></span>

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

### <span data-ttu-id="b76eb-152">-ServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="b76eb-152">-ServiceBusNamespace</span></span>
<span data-ttu-id="b76eb-153">A szolgáltatás busz-névteret adja meg.</span><span class="sxs-lookup"><span data-stu-id="b76eb-153">Specifies a service bus namespace.</span></span>

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

### <span data-ttu-id="b76eb-154">-ServiceBusSasKeyName</span><span class="sxs-lookup"><span data-stu-id="b76eb-154">-ServiceBusSasKeyName</span></span>
<span data-ttu-id="b76eb-155">Egy megosztott Access-aláírási kulcs nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b76eb-155">Specifies a shared access signature key name.</span></span>

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

### <span data-ttu-id="b76eb-156">-ServiceBusSasKeyValue</span><span class="sxs-lookup"><span data-stu-id="b76eb-156">-ServiceBusSasKeyValue</span></span>
<span data-ttu-id="b76eb-157">A megosztott hozzáférés-aláírási kulcs értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b76eb-157">Specifies a shared access signature key value.</span></span>

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

### <span data-ttu-id="b76eb-158">-ServiceBusTopicPath</span><span class="sxs-lookup"><span data-stu-id="b76eb-158">-ServiceBusTopicPath</span></span>
<span data-ttu-id="b76eb-159">A szolgáltatás buszja témakör elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b76eb-159">Specifies a service bus topic path.</span></span>

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

### <span data-ttu-id="b76eb-160">-ServiceBusTransportType</span><span class="sxs-lookup"><span data-stu-id="b76eb-160">-ServiceBusTransportType</span></span>
<span data-ttu-id="b76eb-161">A szolgáltatás busz-átviteli típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b76eb-161">Specifies a service bus transport type.</span></span>
<span data-ttu-id="b76eb-162">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="b76eb-162">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b76eb-163">NetMessaging</span><span class="sxs-lookup"><span data-stu-id="b76eb-163">NetMessaging</span></span>
- <span data-ttu-id="b76eb-164">AMQP</span><span class="sxs-lookup"><span data-stu-id="b76eb-164">AMQP</span></span>

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

### <span data-ttu-id="b76eb-165">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="b76eb-165">-StartTime</span></span>
<span data-ttu-id="b76eb-166">A projekthez tartozó **datetime** -objektum kezdési időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b76eb-166">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="b76eb-167">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b76eb-167">-Confirm</span></span>
<span data-ttu-id="b76eb-168">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b76eb-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b76eb-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b76eb-169">-WhatIf</span></span>
<span data-ttu-id="b76eb-170">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b76eb-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b76eb-171">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b76eb-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b76eb-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b76eb-172">CommonParameters</span></span>
<span data-ttu-id="b76eb-173">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b76eb-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b76eb-174">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b76eb-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b76eb-175">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b76eb-175">INPUTS</span></span>

### <span data-ttu-id="b76eb-176">Nincs</span><span class="sxs-lookup"><span data-stu-id="b76eb-176">None</span></span>
<span data-ttu-id="b76eb-177">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="b76eb-177">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b76eb-178">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b76eb-178">OUTPUTS</span></span>

### <span data-ttu-id="b76eb-179">Microsoft. Azure. Command. Scheduler. models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="b76eb-179">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="b76eb-180">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b76eb-180">NOTES</span></span>

## <span data-ttu-id="b76eb-181">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b76eb-181">RELATED LINKS</span></span>

[<span data-ttu-id="b76eb-182">Új – AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="b76eb-182">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="b76eb-183">Új – AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="b76eb-183">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="b76eb-184">Új – AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="b76eb-184">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="b76eb-185">Új – AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="b76eb-185">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="b76eb-186">Új – AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="b76eb-186">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="b76eb-187">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="b76eb-187">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="b76eb-188">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="b76eb-188">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="b76eb-189">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="b76eb-189">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="b76eb-190">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="b76eb-190">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


