---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: 2C8C98B8-7A3B-4F24-BDF1-0B7B81049956
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/set-azurermschedulerservicebusqueuejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerServiceBusQueueJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerServiceBusQueueJob.md
ms.openlocfilehash: bbc2661f585dacc5537583d8282c76e6fdcd7562
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679255"
---
# <span data-ttu-id="413d3-101">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="413d3-101">Set-AzureRmSchedulerServiceBusQueueJob</span></span>

## <span data-ttu-id="413d3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="413d3-102">SYNOPSIS</span></span>
<span data-ttu-id="413d3-103">A szolgáltatás busz-várólista-feladatát módosítja.</span><span class="sxs-lookup"><span data-stu-id="413d3-103">Modifies a service bus queue job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="413d3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="413d3-104">SYNTAX</span></span>

```
Set-AzureRmSchedulerServiceBusQueueJob -ResourceGroupName <String> -JobCollectionName <String>
 -JobName <String> [-ServiceBusQueueName <String>] -ServiceBusNamespace <String>
 -ServiceBusTransportType <String> -ServiceBusMessage <String> -ServiceBusSasKeyName <String>
 -ServiceBusSasKeyValue <String> [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="413d3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="413d3-105">DESCRIPTION</span></span>
<span data-ttu-id="413d3-106">A **set-AzureRmSchedulerServiceBusQueueJob** parancsmag az Azure Scheduler szolgáltatásban módosítja a szolgáltatás busz-várólistájának feladatát.</span><span class="sxs-lookup"><span data-stu-id="413d3-106">The **Set-AzureRmSchedulerServiceBusQueueJob** cmdlet modifies a service bus queue job in Azure Scheduler.</span></span>

<span data-ttu-id="413d3-107">Ez a parancsmag a *ErrorActionType* paraméter alapján támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="413d3-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="413d3-108">A dinamikus paraméterek elérhetővé válnak a többi paraméter-érték alapján.</span><span class="sxs-lookup"><span data-stu-id="413d3-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="413d3-109">Ha meg szeretné ismerni a dinamikus paraméterek nevét a többi paraméter megadása után, írjon be egy kötőjelet (-), majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="413d3-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="413d3-110">Ha kihagyja a kötelező paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="413d3-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="413d3-111">Példák</span><span class="sxs-lookup"><span data-stu-id="413d3-111">EXAMPLES</span></span>

## <span data-ttu-id="413d3-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="413d3-112">PARAMETERS</span></span>

### <span data-ttu-id="413d3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="413d3-113">-DefaultProfile</span></span>
<span data-ttu-id="413d3-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="413d3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="413d3-115">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="413d3-115">-EndTime</span></span>
<span data-ttu-id="413d3-116">A projekthez tartozó **datetime** -objektum záró időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="413d3-116">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="413d3-117">Ha **datetime** típusú objektumot szeretne beolvasni, használja az Get-Date parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="413d3-117">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="413d3-118">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="413d3-118">-ErrorActionType</span></span>
<span data-ttu-id="413d3-119">A feladat hibaérték-beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="413d3-119">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="413d3-120">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="413d3-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="413d3-121">Http</span><span class="sxs-lookup"><span data-stu-id="413d3-121">Http</span></span> 
- <span data-ttu-id="413d3-122">Https</span><span class="sxs-lookup"><span data-stu-id="413d3-122">Https</span></span> 
- <span data-ttu-id="413d3-123">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="413d3-123">StorageQueue</span></span> 
- <span data-ttu-id="413d3-124">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="413d3-124">ServiceBusQueue</span></span> 
- <span data-ttu-id="413d3-125">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="413d3-125">ServiceBusTopic</span></span>

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

### <span data-ttu-id="413d3-126">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="413d3-126">-ExecutionCount</span></span>
<span data-ttu-id="413d3-127">Itt adhatja meg, hogy hányszor fusson a feladat.</span><span class="sxs-lookup"><span data-stu-id="413d3-127">Specifies how many times the job runs.</span></span>
<span data-ttu-id="413d3-128">Alapértelmezés szerint a feladat határozatlan ideig ismétlődik.</span><span class="sxs-lookup"><span data-stu-id="413d3-128">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="413d3-129">-Gyakoriság</span><span class="sxs-lookup"><span data-stu-id="413d3-129">-Frequency</span></span>
<span data-ttu-id="413d3-130">A feladat gyakoriságát adja meg.</span><span class="sxs-lookup"><span data-stu-id="413d3-130">Specifies a frequency for the job.</span></span>
<span data-ttu-id="413d3-131">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="413d3-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="413d3-132">Perces</span><span class="sxs-lookup"><span data-stu-id="413d3-132">Minute</span></span> 
- <span data-ttu-id="413d3-133">Óra</span><span class="sxs-lookup"><span data-stu-id="413d3-133">Hour</span></span> 
- <span data-ttu-id="413d3-134">Nap</span><span class="sxs-lookup"><span data-stu-id="413d3-134">Day</span></span> 
- <span data-ttu-id="413d3-135">Héten</span><span class="sxs-lookup"><span data-stu-id="413d3-135">Week</span></span> 
- <span data-ttu-id="413d3-136">Hónap</span><span class="sxs-lookup"><span data-stu-id="413d3-136">Month</span></span>

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

### <span data-ttu-id="413d3-137">-Intervallum</span><span class="sxs-lookup"><span data-stu-id="413d3-137">-Interval</span></span>
<span data-ttu-id="413d3-138">A feladat ismétlődésének intervallumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="413d3-138">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="413d3-139">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="413d3-139">-JobCollectionName</span></span>
<span data-ttu-id="413d3-140">Annak a feladatnak a neve, amelyhez a projekt tartozik.</span><span class="sxs-lookup"><span data-stu-id="413d3-140">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="413d3-141">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="413d3-141">-JobName</span></span>
<span data-ttu-id="413d3-142">Annak a feladatnak a nevét adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="413d3-142">Specifies the name of the job that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="413d3-143">-JobState</span><span class="sxs-lookup"><span data-stu-id="413d3-143">-JobState</span></span>
<span data-ttu-id="413d3-144">A feladat állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="413d3-144">Specifies the state of the job.</span></span>
<span data-ttu-id="413d3-145">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="413d3-145">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="413d3-146">Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="413d3-146">Enabled</span></span> 
- <span data-ttu-id="413d3-147">Tiltva</span><span class="sxs-lookup"><span data-stu-id="413d3-147">Disabled</span></span>

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

### <span data-ttu-id="413d3-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="413d3-148">-ResourceGroupName</span></span>
<span data-ttu-id="413d3-149">Azt az erőforráscsoport-csoportot adja meg, amelyhez a projekt tartozik.</span><span class="sxs-lookup"><span data-stu-id="413d3-149">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="413d3-150">-ServiceBusMessage</span><span class="sxs-lookup"><span data-stu-id="413d3-150">-ServiceBusMessage</span></span>
<span data-ttu-id="413d3-151">A szolgáltatás busz várólistájának üzenetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="413d3-151">Specifies a service bus queue message.</span></span>

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

### <span data-ttu-id="413d3-152">-ServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="413d3-152">-ServiceBusNamespace</span></span>
<span data-ttu-id="413d3-153">A szolgáltatás busz-névteret adja meg.</span><span class="sxs-lookup"><span data-stu-id="413d3-153">Specifies a service bus namespace.</span></span>

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

### <span data-ttu-id="413d3-154">-ServiceBusQueueName</span><span class="sxs-lookup"><span data-stu-id="413d3-154">-ServiceBusQueueName</span></span>
<span data-ttu-id="413d3-155">A szolgáltatás buszjának várólista-nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="413d3-155">Specifies a service bus queue name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="413d3-156">-ServiceBusSasKeyName</span><span class="sxs-lookup"><span data-stu-id="413d3-156">-ServiceBusSasKeyName</span></span>
<span data-ttu-id="413d3-157">Egy megosztott Access-aláírási kulcs nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="413d3-157">Specifies a shared access signature key name.</span></span>

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

### <span data-ttu-id="413d3-158">-ServiceBusSasKeyValue</span><span class="sxs-lookup"><span data-stu-id="413d3-158">-ServiceBusSasKeyValue</span></span>
<span data-ttu-id="413d3-159">A megosztott hozzáférés-aláírási kulcs értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="413d3-159">Specifies a shared access signature key value.</span></span>

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

### <span data-ttu-id="413d3-160">-ServiceBusTransportType</span><span class="sxs-lookup"><span data-stu-id="413d3-160">-ServiceBusTransportType</span></span>
<span data-ttu-id="413d3-161">A szolgáltatás busz-átviteli típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="413d3-161">Specifies a service bus transport type.</span></span>
<span data-ttu-id="413d3-162">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="413d3-162">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="413d3-163">NetMessaging</span><span class="sxs-lookup"><span data-stu-id="413d3-163">NetMessaging</span></span> 
- <span data-ttu-id="413d3-164">AMQP</span><span class="sxs-lookup"><span data-stu-id="413d3-164">AMQP</span></span>

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

### <span data-ttu-id="413d3-165">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="413d3-165">-StartTime</span></span>
<span data-ttu-id="413d3-166">A projekthez tartozó **datetime** -objektum kezdési időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="413d3-166">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="413d3-167">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="413d3-167">-Confirm</span></span>
<span data-ttu-id="413d3-168">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="413d3-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="413d3-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="413d3-169">-WhatIf</span></span>
<span data-ttu-id="413d3-170">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="413d3-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="413d3-171">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="413d3-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="413d3-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="413d3-172">CommonParameters</span></span>
<span data-ttu-id="413d3-173">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="413d3-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="413d3-174">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="413d3-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="413d3-175">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="413d3-175">INPUTS</span></span>

### <span data-ttu-id="413d3-176">Nincs</span><span class="sxs-lookup"><span data-stu-id="413d3-176">None</span></span>
<span data-ttu-id="413d3-177">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="413d3-177">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="413d3-178">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="413d3-178">OUTPUTS</span></span>

### <span data-ttu-id="413d3-179">Microsoft. Azure. Command. Scheduler. models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="413d3-179">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="413d3-180">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="413d3-180">NOTES</span></span>

## <span data-ttu-id="413d3-181">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="413d3-181">RELATED LINKS</span></span>

[<span data-ttu-id="413d3-182">Új – AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="413d3-182">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="413d3-183">Új – AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="413d3-183">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="413d3-184">Új – AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="413d3-184">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="413d3-185">Új – AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="413d3-185">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="413d3-186">Új – AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="413d3-186">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="413d3-187">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="413d3-187">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="413d3-188">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="413d3-188">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="413d3-189">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="413d3-189">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="413d3-190">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="413d3-190">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


