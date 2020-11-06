---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: 52987702-D101-4D5D-852D-2809374292F4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerServiceBusQueueJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerServiceBusQueueJob.md
ms.openlocfilehash: a61d745cb748d27baf7b07b6b4389077e50aaa24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501623"
---
# <span data-ttu-id="10192-101">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="10192-101">New-AzureRmSchedulerServiceBusQueueJob</span></span>

## <span data-ttu-id="10192-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="10192-102">SYNOPSIS</span></span>
<span data-ttu-id="10192-103">Létrehoz egy Service Bus Queue-feladatot.</span><span class="sxs-lookup"><span data-stu-id="10192-103">Creates a service bus queue job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10192-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="10192-104">SYNTAX</span></span>

```
New-AzureRmSchedulerServiceBusQueueJob -ResourceGroupName <String> -JobCollectionName <String>
 -JobName <String> -ServiceBusQueueName <String> -ServiceBusNamespace <String>
 -ServiceBusTransportType <String> -ServiceBusMessage <String> -ServiceBusSasKeyName <String>
 -ServiceBusSasKeyValue <String> [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10192-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="10192-105">DESCRIPTION</span></span>
<span data-ttu-id="10192-106">A **New-AzureRmSchedulerServiceBusQueueJob** parancsmag létrehoz egy szolgáltatás-várólistás feladatot az Azure schedulerben.</span><span class="sxs-lookup"><span data-stu-id="10192-106">The **New-AzureRmSchedulerServiceBusQueueJob** cmdlet creates a service bus queue job in Azure Scheduler.</span></span>

<span data-ttu-id="10192-107">Ez a parancsmag a *ErrorActionType* paraméter alapján támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="10192-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="10192-108">A dinamikus paraméterek elérhetővé válnak a többi paraméter-érték alapján.</span><span class="sxs-lookup"><span data-stu-id="10192-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="10192-109">Ha meg szeretné ismerni a dinamikus paraméterek nevét a többi paraméter megadása után, írjon be egy kötőjelet (-), majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="10192-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="10192-110">Ha kihagyja a kötelező paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="10192-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="10192-111">Példák</span><span class="sxs-lookup"><span data-stu-id="10192-111">EXAMPLES</span></span>

## <span data-ttu-id="10192-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="10192-112">PARAMETERS</span></span>

### <span data-ttu-id="10192-113">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="10192-113">-EndTime</span></span>
<span data-ttu-id="10192-114">A projekthez tartozó **datetime** -objektum záró időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="10192-114">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="10192-115">Ha **datetime** típusú objektumot szeretne beolvasni, használja az Get-Date parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="10192-115">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="10192-116">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="10192-116">-ErrorActionType</span></span>
<span data-ttu-id="10192-117">A feladat hibaérték-beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="10192-117">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="10192-118">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="10192-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="10192-119">Http</span><span class="sxs-lookup"><span data-stu-id="10192-119">Http</span></span> 
- <span data-ttu-id="10192-120">Https</span><span class="sxs-lookup"><span data-stu-id="10192-120">Https</span></span> 
- <span data-ttu-id="10192-121">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="10192-121">StorageQueue</span></span> 
- <span data-ttu-id="10192-122">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="10192-122">ServiceBusQueue</span></span> 
- <span data-ttu-id="10192-123">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="10192-123">ServiceBusTopic</span></span>

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

### <span data-ttu-id="10192-124">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="10192-124">-ExecutionCount</span></span>
<span data-ttu-id="10192-125">Itt adhatja meg, hogy hányszor fusson a feladat.</span><span class="sxs-lookup"><span data-stu-id="10192-125">Specifies how many times the job runs.</span></span>
<span data-ttu-id="10192-126">Alapértelmezés szerint a feladat határozatlan ideig ismétlődik.</span><span class="sxs-lookup"><span data-stu-id="10192-126">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="10192-127">-Gyakoriság</span><span class="sxs-lookup"><span data-stu-id="10192-127">-Frequency</span></span>
<span data-ttu-id="10192-128">A feladat gyakoriságát adja meg.</span><span class="sxs-lookup"><span data-stu-id="10192-128">Specifies a frequency for the job.</span></span>
<span data-ttu-id="10192-129">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="10192-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="10192-130">Perces</span><span class="sxs-lookup"><span data-stu-id="10192-130">Minute</span></span> 
- <span data-ttu-id="10192-131">Óra</span><span class="sxs-lookup"><span data-stu-id="10192-131">Hour</span></span> 
- <span data-ttu-id="10192-132">Nap</span><span class="sxs-lookup"><span data-stu-id="10192-132">Day</span></span> 
- <span data-ttu-id="10192-133">Héten</span><span class="sxs-lookup"><span data-stu-id="10192-133">Week</span></span> 
- <span data-ttu-id="10192-134">Hónap</span><span class="sxs-lookup"><span data-stu-id="10192-134">Month</span></span>

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

### <span data-ttu-id="10192-135">-Intervallum</span><span class="sxs-lookup"><span data-stu-id="10192-135">-Interval</span></span>
<span data-ttu-id="10192-136">A feladat ismétlődésének intervallumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="10192-136">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="10192-137">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="10192-137">-JobCollectionName</span></span>
<span data-ttu-id="10192-138">Annak a feladatnak a neve, amelyhez a projekt tartozik.</span><span class="sxs-lookup"><span data-stu-id="10192-138">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="10192-139">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="10192-139">-JobName</span></span>
<span data-ttu-id="10192-140">A feladat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="10192-140">Specifies a name for the job.</span></span>

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

### <span data-ttu-id="10192-141">-JobState</span><span class="sxs-lookup"><span data-stu-id="10192-141">-JobState</span></span>
<span data-ttu-id="10192-142">A feladat állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="10192-142">Specifies the state of the job.</span></span>
<span data-ttu-id="10192-143">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="10192-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="10192-144">Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="10192-144">Enabled</span></span> 
- <span data-ttu-id="10192-145">Tiltva</span><span class="sxs-lookup"><span data-stu-id="10192-145">Disabled</span></span>

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

### <span data-ttu-id="10192-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10192-146">-ResourceGroupName</span></span>
<span data-ttu-id="10192-147">Azt az erőforráscsoport-csoportot adja meg, amelyhez a projekt tartozik.</span><span class="sxs-lookup"><span data-stu-id="10192-147">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="10192-148">-ServiceBusMessage</span><span class="sxs-lookup"><span data-stu-id="10192-148">-ServiceBusMessage</span></span>
<span data-ttu-id="10192-149">A szolgáltatás busz várólistájának üzenetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="10192-149">Specifies a service bus queue message.</span></span>

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

### <span data-ttu-id="10192-150">-ServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="10192-150">-ServiceBusNamespace</span></span>
<span data-ttu-id="10192-151">A szolgáltatás busz-névteret adja meg.</span><span class="sxs-lookup"><span data-stu-id="10192-151">Specifies a service bus namespace.</span></span>

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

### <span data-ttu-id="10192-152">-ServiceBusQueueName</span><span class="sxs-lookup"><span data-stu-id="10192-152">-ServiceBusQueueName</span></span>
<span data-ttu-id="10192-153">A szolgáltatás buszjának várólista-nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="10192-153">Specifies a service bus queue name.</span></span>

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

### <span data-ttu-id="10192-154">-ServiceBusSasKeyName</span><span class="sxs-lookup"><span data-stu-id="10192-154">-ServiceBusSasKeyName</span></span>
<span data-ttu-id="10192-155">Egy megosztott Access-aláírási kulcs nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="10192-155">Specifies a shared access signature key name.</span></span>

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

### <span data-ttu-id="10192-156">-ServiceBusSasKeyValue</span><span class="sxs-lookup"><span data-stu-id="10192-156">-ServiceBusSasKeyValue</span></span>
<span data-ttu-id="10192-157">A megosztott hozzáférés-aláírási kulcs értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="10192-157">Specifies a shared access signature key value.</span></span>

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

### <span data-ttu-id="10192-158">-ServiceBusTransportType</span><span class="sxs-lookup"><span data-stu-id="10192-158">-ServiceBusTransportType</span></span>
<span data-ttu-id="10192-159">A szolgáltatás busz-átviteli típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="10192-159">Specifies a service bus transport type.</span></span>
<span data-ttu-id="10192-160">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="10192-160">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="10192-161">NetMessaging</span><span class="sxs-lookup"><span data-stu-id="10192-161">NetMessaging</span></span> 
- <span data-ttu-id="10192-162">AMQP</span><span class="sxs-lookup"><span data-stu-id="10192-162">AMQP</span></span>

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

### <span data-ttu-id="10192-163">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="10192-163">-StartTime</span></span>
<span data-ttu-id="10192-164">A projekthez tartozó **datetime** -objektum kezdési időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="10192-164">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="10192-165">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="10192-165">-Confirm</span></span>
<span data-ttu-id="10192-166">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="10192-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10192-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10192-167">-WhatIf</span></span>
<span data-ttu-id="10192-168">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="10192-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10192-169">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="10192-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10192-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10192-170">-DefaultProfile</span></span>
<span data-ttu-id="10192-171">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="10192-171">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10192-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10192-172">CommonParameters</span></span>
<span data-ttu-id="10192-173">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="10192-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10192-174">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10192-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10192-175">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="10192-175">INPUTS</span></span>

## <span data-ttu-id="10192-176">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="10192-176">OUTPUTS</span></span>

### <span data-ttu-id="10192-177">Microsoft. Azure. Command. Scheduler. models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="10192-177">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="10192-178">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="10192-178">NOTES</span></span>

## <span data-ttu-id="10192-179">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="10192-179">RELATED LINKS</span></span>

[<span data-ttu-id="10192-180">Új – AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="10192-180">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="10192-181">Új – AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="10192-181">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="10192-182">Új – AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="10192-182">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="10192-183">Új – AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="10192-183">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="10192-184">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="10192-184">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="10192-185">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="10192-185">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="10192-186">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="10192-186">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="10192-187">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="10192-187">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="10192-188">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="10192-188">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


