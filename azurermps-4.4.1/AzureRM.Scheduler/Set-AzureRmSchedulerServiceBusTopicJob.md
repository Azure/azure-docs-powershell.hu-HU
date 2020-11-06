---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: F6B24F96-6016-4645-9F92-F584B73657D5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerServiceBusTopicJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerServiceBusTopicJob.md
ms.openlocfilehash: a12cf84d90ecbcc948ac13745b38438766582aaf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503956"
---
# <span data-ttu-id="f9aea-101">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="f9aea-101">Set-AzureRmSchedulerServiceBusTopicJob</span></span>

## <span data-ttu-id="f9aea-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f9aea-102">SYNOPSIS</span></span>
<span data-ttu-id="f9aea-103">Egy szolgáltatási busz témakörének módosítása.</span><span class="sxs-lookup"><span data-stu-id="f9aea-103">Modifies a service bus topic job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9aea-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f9aea-104">SYNTAX</span></span>

```
Set-AzureRmSchedulerServiceBusTopicJob -ResourceGroupName <String> -JobCollectionName <String>
 -JobName <String> -ServiceBusTopicPath <String> -ServiceBusNamespace <String>
 -ServiceBusTransportType <String> -ServiceBusMessage <String> -ServiceBusSasKeyName <String>
 -ServiceBusSasKeyValue <String> [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9aea-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f9aea-105">DESCRIPTION</span></span>
<span data-ttu-id="f9aea-106">A **set-AzureRmSchedulerServiceBusTopicJob** parancsmag az Azure Scheduler szolgáltatásban módosítja a szolgáltatási busz témakört.</span><span class="sxs-lookup"><span data-stu-id="f9aea-106">The **Set-AzureRmSchedulerServiceBusTopicJob** cmdlet modifies a service bus topic job in Azure Scheduler.</span></span>

<span data-ttu-id="f9aea-107">Ez a parancsmag a *ErrorActionType* paraméter alapján támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="f9aea-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="f9aea-108">A dinamikus paraméterek elérhetővé válnak a többi paraméter-érték alapján.</span><span class="sxs-lookup"><span data-stu-id="f9aea-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="f9aea-109">Ha meg szeretné ismerni a dinamikus paraméterek nevét a többi paraméter megadása után, írjon be egy kötőjelet (-), majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="f9aea-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="f9aea-110">Ha kihagyja a kötelező paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="f9aea-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="f9aea-111">Példák</span><span class="sxs-lookup"><span data-stu-id="f9aea-111">EXAMPLES</span></span>

## <span data-ttu-id="f9aea-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f9aea-112">PARAMETERS</span></span>

### <span data-ttu-id="f9aea-113">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="f9aea-113">-EndTime</span></span>
<span data-ttu-id="f9aea-114">A projekthez tartozó **datetime** -objektum záró időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f9aea-114">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="f9aea-115">Ha **datetime** típusú objektumot szeretne beolvasni, használja az Get-Date parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="f9aea-115">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="f9aea-116">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="f9aea-116">-ErrorActionType</span></span>
<span data-ttu-id="f9aea-117">A feladat hibaérték-beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="f9aea-117">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="f9aea-118">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="f9aea-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f9aea-119">Http</span><span class="sxs-lookup"><span data-stu-id="f9aea-119">Http</span></span> 
- <span data-ttu-id="f9aea-120">Https</span><span class="sxs-lookup"><span data-stu-id="f9aea-120">Https</span></span> 
- <span data-ttu-id="f9aea-121">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="f9aea-121">StorageQueue</span></span> 
- <span data-ttu-id="f9aea-122">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="f9aea-122">ServiceBusQueue</span></span> 
- <span data-ttu-id="f9aea-123">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="f9aea-123">ServiceBusTopic</span></span>

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

### <span data-ttu-id="f9aea-124">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="f9aea-124">-ExecutionCount</span></span>
<span data-ttu-id="f9aea-125">Itt adhatja meg, hogy hányszor fusson a feladat.</span><span class="sxs-lookup"><span data-stu-id="f9aea-125">Specifies how many times the job runs.</span></span>
<span data-ttu-id="f9aea-126">Alapértelmezés szerint a feladat határozatlan ideig ismétlődik.</span><span class="sxs-lookup"><span data-stu-id="f9aea-126">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="f9aea-127">-Gyakoriság</span><span class="sxs-lookup"><span data-stu-id="f9aea-127">-Frequency</span></span>
<span data-ttu-id="f9aea-128">A feladat maximális gyakoriságát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f9aea-128">Specifies a maximum frequency for the job.</span></span>
<span data-ttu-id="f9aea-129">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="f9aea-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f9aea-130">Perces</span><span class="sxs-lookup"><span data-stu-id="f9aea-130">Minute</span></span> 
- <span data-ttu-id="f9aea-131">Óra</span><span class="sxs-lookup"><span data-stu-id="f9aea-131">Hour</span></span> 
- <span data-ttu-id="f9aea-132">Nap</span><span class="sxs-lookup"><span data-stu-id="f9aea-132">Day</span></span> 
- <span data-ttu-id="f9aea-133">Héten</span><span class="sxs-lookup"><span data-stu-id="f9aea-133">Week</span></span> 
- <span data-ttu-id="f9aea-134">Hónap</span><span class="sxs-lookup"><span data-stu-id="f9aea-134">Month</span></span>

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

### <span data-ttu-id="f9aea-135">-Intervallum</span><span class="sxs-lookup"><span data-stu-id="f9aea-135">-Interval</span></span>
<span data-ttu-id="f9aea-136">A feladat ismétlődésének intervallumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f9aea-136">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="f9aea-137">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="f9aea-137">-JobCollectionName</span></span>
<span data-ttu-id="f9aea-138">Annak a feladatnak a neve, amelyhez a projekt tartozik.</span><span class="sxs-lookup"><span data-stu-id="f9aea-138">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="f9aea-139">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="f9aea-139">-JobName</span></span>
<span data-ttu-id="f9aea-140">Annak a feladatnak a nevét adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="f9aea-140">Specifies the name of the job that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="f9aea-141">-JobState</span><span class="sxs-lookup"><span data-stu-id="f9aea-141">-JobState</span></span>
<span data-ttu-id="f9aea-142">A feladat állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f9aea-142">Specifies the state of the job.</span></span>
<span data-ttu-id="f9aea-143">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="f9aea-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f9aea-144">Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="f9aea-144">Enabled</span></span> 
- <span data-ttu-id="f9aea-145">Tiltva</span><span class="sxs-lookup"><span data-stu-id="f9aea-145">Disabled</span></span>

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

### <span data-ttu-id="f9aea-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9aea-146">-ResourceGroupName</span></span>
<span data-ttu-id="f9aea-147">Azt az erőforráscsoport-csoportot adja meg, amelyhez a projekt tartozik.</span><span class="sxs-lookup"><span data-stu-id="f9aea-147">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="f9aea-148">-ServiceBusMessage</span><span class="sxs-lookup"><span data-stu-id="f9aea-148">-ServiceBusMessage</span></span>
<span data-ttu-id="f9aea-149">A szolgáltatás buszjának témáját tartalmazó üzenetet adja meg.</span><span class="sxs-lookup"><span data-stu-id="f9aea-149">Specifies a service bus topic message.</span></span>

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

### <span data-ttu-id="f9aea-150">-ServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="f9aea-150">-ServiceBusNamespace</span></span>
<span data-ttu-id="f9aea-151">A szolgáltatás busz-névteret adja meg.</span><span class="sxs-lookup"><span data-stu-id="f9aea-151">Specifies a service bus namespace.</span></span>

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

### <span data-ttu-id="f9aea-152">-ServiceBusSasKeyName</span><span class="sxs-lookup"><span data-stu-id="f9aea-152">-ServiceBusSasKeyName</span></span>
<span data-ttu-id="f9aea-153">Egy megosztott Access-aláírási kulcs nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f9aea-153">Specifies a shared access signature key name.</span></span>

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

### <span data-ttu-id="f9aea-154">-ServiceBusSasKeyValue</span><span class="sxs-lookup"><span data-stu-id="f9aea-154">-ServiceBusSasKeyValue</span></span>
<span data-ttu-id="f9aea-155">A megosztott hozzáférés-aláírási kulcs értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f9aea-155">Specifies a shared access signature key value.</span></span>

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

### <span data-ttu-id="f9aea-156">-ServiceBusTopicPath</span><span class="sxs-lookup"><span data-stu-id="f9aea-156">-ServiceBusTopicPath</span></span>
<span data-ttu-id="f9aea-157">A szolgáltatás buszja témakör elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f9aea-157">Specifies a service bus topic path.</span></span>

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

### <span data-ttu-id="f9aea-158">-ServiceBusTransportType</span><span class="sxs-lookup"><span data-stu-id="f9aea-158">-ServiceBusTransportType</span></span>
<span data-ttu-id="f9aea-159">A szolgáltatás busz-átviteli típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f9aea-159">Specifies a service bus transport type.</span></span>
<span data-ttu-id="f9aea-160">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="f9aea-160">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f9aea-161">NetMessaging</span><span class="sxs-lookup"><span data-stu-id="f9aea-161">NetMessaging</span></span>
- <span data-ttu-id="f9aea-162">AMQP</span><span class="sxs-lookup"><span data-stu-id="f9aea-162">AMQP</span></span>

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

### <span data-ttu-id="f9aea-163">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="f9aea-163">-StartTime</span></span>
<span data-ttu-id="f9aea-164">A projekthez tartozó **datetime** -objektum kezdési időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f9aea-164">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="f9aea-165">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f9aea-165">-Confirm</span></span>
<span data-ttu-id="f9aea-166">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f9aea-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9aea-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9aea-167">-WhatIf</span></span>
<span data-ttu-id="f9aea-168">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f9aea-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9aea-169">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f9aea-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9aea-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9aea-170">-DefaultProfile</span></span>
<span data-ttu-id="f9aea-171">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f9aea-171">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9aea-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9aea-172">CommonParameters</span></span>
<span data-ttu-id="f9aea-173">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f9aea-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9aea-174">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9aea-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9aea-175">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f9aea-175">INPUTS</span></span>

## <span data-ttu-id="f9aea-176">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f9aea-176">OUTPUTS</span></span>

### <span data-ttu-id="f9aea-177">Microsoft. Azure. Command. Scheduler. models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="f9aea-177">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="f9aea-178">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f9aea-178">NOTES</span></span>

## <span data-ttu-id="f9aea-179">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f9aea-179">RELATED LINKS</span></span>

[<span data-ttu-id="f9aea-180">Új – AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="f9aea-180">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="f9aea-181">Új – AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="f9aea-181">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="f9aea-182">Új – AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="f9aea-182">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="f9aea-183">Új – AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="f9aea-183">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="f9aea-184">Új – AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="f9aea-184">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="f9aea-185">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="f9aea-185">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="f9aea-186">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="f9aea-186">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="f9aea-187">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="f9aea-187">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="f9aea-188">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="f9aea-188">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


