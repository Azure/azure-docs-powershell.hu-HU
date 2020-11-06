---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: 2C8C98B8-7A3B-4F24-BDF1-0B7B81049956
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerServiceBusQueueJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerServiceBusQueueJob.md
ms.openlocfilehash: 6928347ab5d78a25d53636f73413f772b9beea4d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504732"
---
# <span data-ttu-id="a8992-101">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="a8992-101">Set-AzureRmSchedulerServiceBusQueueJob</span></span>

## <span data-ttu-id="a8992-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a8992-102">SYNOPSIS</span></span>
<span data-ttu-id="a8992-103">A szolgáltatás busz-várólista-feladatát módosítja.</span><span class="sxs-lookup"><span data-stu-id="a8992-103">Modifies a service bus queue job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8992-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a8992-104">SYNTAX</span></span>

```
Set-AzureRmSchedulerServiceBusQueueJob -ResourceGroupName <String> -JobCollectionName <String>
 -JobName <String> [-ServiceBusQueueName <String>] -ServiceBusNamespace <String>
 -ServiceBusTransportType <String> -ServiceBusMessage <String> -ServiceBusSasKeyName <String>
 -ServiceBusSasKeyValue <String> [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8992-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a8992-105">DESCRIPTION</span></span>
<span data-ttu-id="a8992-106">A **set-AzureRmSchedulerServiceBusQueueJob** parancsmag az Azure Scheduler szolgáltatásban módosítja a szolgáltatás busz-várólistájának feladatát.</span><span class="sxs-lookup"><span data-stu-id="a8992-106">The **Set-AzureRmSchedulerServiceBusQueueJob** cmdlet modifies a service bus queue job in Azure Scheduler.</span></span>

<span data-ttu-id="a8992-107">Ez a parancsmag a *ErrorActionType* paraméter alapján támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="a8992-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="a8992-108">A dinamikus paraméterek elérhetővé válnak a többi paraméter-érték alapján.</span><span class="sxs-lookup"><span data-stu-id="a8992-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="a8992-109">Ha meg szeretné ismerni a dinamikus paraméterek nevét a többi paraméter megadása után, írjon be egy kötőjelet (-), majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="a8992-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="a8992-110">Ha kihagyja a kötelező paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="a8992-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="a8992-111">Példák</span><span class="sxs-lookup"><span data-stu-id="a8992-111">EXAMPLES</span></span>

## <span data-ttu-id="a8992-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a8992-112">PARAMETERS</span></span>

### <span data-ttu-id="a8992-113">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="a8992-113">-EndTime</span></span>
<span data-ttu-id="a8992-114">A projekthez tartozó **datetime** -objektum záró időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8992-114">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="a8992-115">Ha **datetime** típusú objektumot szeretne beolvasni, használja az Get-Date parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="a8992-115">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="a8992-116">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="a8992-116">-ErrorActionType</span></span>
<span data-ttu-id="a8992-117">A feladat hibaérték-beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8992-117">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="a8992-118">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="a8992-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a8992-119">Http</span><span class="sxs-lookup"><span data-stu-id="a8992-119">Http</span></span> 
- <span data-ttu-id="a8992-120">Https</span><span class="sxs-lookup"><span data-stu-id="a8992-120">Https</span></span> 
- <span data-ttu-id="a8992-121">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="a8992-121">StorageQueue</span></span> 
- <span data-ttu-id="a8992-122">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="a8992-122">ServiceBusQueue</span></span> 
- <span data-ttu-id="a8992-123">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="a8992-123">ServiceBusTopic</span></span>

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

### <span data-ttu-id="a8992-124">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="a8992-124">-ExecutionCount</span></span>
<span data-ttu-id="a8992-125">Itt adhatja meg, hogy hányszor fusson a feladat.</span><span class="sxs-lookup"><span data-stu-id="a8992-125">Specifies how many times the job runs.</span></span>
<span data-ttu-id="a8992-126">Alapértelmezés szerint a feladat határozatlan ideig ismétlődik.</span><span class="sxs-lookup"><span data-stu-id="a8992-126">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="a8992-127">-Gyakoriság</span><span class="sxs-lookup"><span data-stu-id="a8992-127">-Frequency</span></span>
<span data-ttu-id="a8992-128">A feladat gyakoriságát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8992-128">Specifies a frequency for the job.</span></span>
<span data-ttu-id="a8992-129">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="a8992-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a8992-130">Perces</span><span class="sxs-lookup"><span data-stu-id="a8992-130">Minute</span></span> 
- <span data-ttu-id="a8992-131">Óra</span><span class="sxs-lookup"><span data-stu-id="a8992-131">Hour</span></span> 
- <span data-ttu-id="a8992-132">Nap</span><span class="sxs-lookup"><span data-stu-id="a8992-132">Day</span></span> 
- <span data-ttu-id="a8992-133">Héten</span><span class="sxs-lookup"><span data-stu-id="a8992-133">Week</span></span> 
- <span data-ttu-id="a8992-134">Hónap</span><span class="sxs-lookup"><span data-stu-id="a8992-134">Month</span></span>

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

### <span data-ttu-id="a8992-135">-Intervallum</span><span class="sxs-lookup"><span data-stu-id="a8992-135">-Interval</span></span>
<span data-ttu-id="a8992-136">A feladat ismétlődésének intervallumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8992-136">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="a8992-137">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="a8992-137">-JobCollectionName</span></span>
<span data-ttu-id="a8992-138">Annak a feladatnak a neve, amelyhez a projekt tartozik.</span><span class="sxs-lookup"><span data-stu-id="a8992-138">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="a8992-139">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="a8992-139">-JobName</span></span>
<span data-ttu-id="a8992-140">Annak a feladatnak a nevét adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="a8992-140">Specifies the name of the job that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="a8992-141">-JobState</span><span class="sxs-lookup"><span data-stu-id="a8992-141">-JobState</span></span>
<span data-ttu-id="a8992-142">A feladat állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8992-142">Specifies the state of the job.</span></span>
<span data-ttu-id="a8992-143">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="a8992-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a8992-144">Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="a8992-144">Enabled</span></span> 
- <span data-ttu-id="a8992-145">Tiltva</span><span class="sxs-lookup"><span data-stu-id="a8992-145">Disabled</span></span>

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

### <span data-ttu-id="a8992-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8992-146">-ResourceGroupName</span></span>
<span data-ttu-id="a8992-147">Azt az erőforráscsoport-csoportot adja meg, amelyhez a projekt tartozik.</span><span class="sxs-lookup"><span data-stu-id="a8992-147">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="a8992-148">-ServiceBusMessage</span><span class="sxs-lookup"><span data-stu-id="a8992-148">-ServiceBusMessage</span></span>
<span data-ttu-id="a8992-149">A szolgáltatás busz várólistájának üzenetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8992-149">Specifies a service bus queue message.</span></span>

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

### <span data-ttu-id="a8992-150">-ServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="a8992-150">-ServiceBusNamespace</span></span>
<span data-ttu-id="a8992-151">A szolgáltatás busz-névteret adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8992-151">Specifies a service bus namespace.</span></span>

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

### <span data-ttu-id="a8992-152">-ServiceBusQueueName</span><span class="sxs-lookup"><span data-stu-id="a8992-152">-ServiceBusQueueName</span></span>
<span data-ttu-id="a8992-153">A szolgáltatás buszjának várólista-nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8992-153">Specifies a service bus queue name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8992-154">-ServiceBusSasKeyName</span><span class="sxs-lookup"><span data-stu-id="a8992-154">-ServiceBusSasKeyName</span></span>
<span data-ttu-id="a8992-155">Egy megosztott Access-aláírási kulcs nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8992-155">Specifies a shared access signature key name.</span></span>

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

### <span data-ttu-id="a8992-156">-ServiceBusSasKeyValue</span><span class="sxs-lookup"><span data-stu-id="a8992-156">-ServiceBusSasKeyValue</span></span>
<span data-ttu-id="a8992-157">A megosztott hozzáférés-aláírási kulcs értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8992-157">Specifies a shared access signature key value.</span></span>

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

### <span data-ttu-id="a8992-158">-ServiceBusTransportType</span><span class="sxs-lookup"><span data-stu-id="a8992-158">-ServiceBusTransportType</span></span>
<span data-ttu-id="a8992-159">A szolgáltatás busz-átviteli típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8992-159">Specifies a service bus transport type.</span></span>
<span data-ttu-id="a8992-160">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="a8992-160">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a8992-161">NetMessaging</span><span class="sxs-lookup"><span data-stu-id="a8992-161">NetMessaging</span></span> 
- <span data-ttu-id="a8992-162">AMQP</span><span class="sxs-lookup"><span data-stu-id="a8992-162">AMQP</span></span>

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

### <span data-ttu-id="a8992-163">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="a8992-163">-StartTime</span></span>
<span data-ttu-id="a8992-164">A projekthez tartozó **datetime** -objektum kezdési időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8992-164">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="a8992-165">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a8992-165">-Confirm</span></span>
<span data-ttu-id="a8992-166">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a8992-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8992-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8992-167">-WhatIf</span></span>
<span data-ttu-id="a8992-168">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a8992-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8992-169">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a8992-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8992-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8992-170">-DefaultProfile</span></span>
<span data-ttu-id="a8992-171">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a8992-171">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8992-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8992-172">CommonParameters</span></span>
<span data-ttu-id="a8992-173">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a8992-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8992-174">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8992-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8992-175">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a8992-175">INPUTS</span></span>

## <span data-ttu-id="a8992-176">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a8992-176">OUTPUTS</span></span>

### <span data-ttu-id="a8992-177">Microsoft. Azure. Command. Scheduler. models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="a8992-177">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="a8992-178">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a8992-178">NOTES</span></span>

## <span data-ttu-id="a8992-179">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a8992-179">RELATED LINKS</span></span>

[<span data-ttu-id="a8992-180">Új – AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="a8992-180">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="a8992-181">Új – AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="a8992-181">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="a8992-182">Új – AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="a8992-182">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="a8992-183">Új – AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="a8992-183">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="a8992-184">Új – AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="a8992-184">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="a8992-185">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="a8992-185">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="a8992-186">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="a8992-186">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="a8992-187">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="a8992-187">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="a8992-188">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="a8992-188">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


