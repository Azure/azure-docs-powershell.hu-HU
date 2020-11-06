---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: D9FA686C-48BB-48A1-926C-56B8151F8F82
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/set-azurermschedulerhttpjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerHttpJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerHttpJob.md
ms.openlocfilehash: 9f43780cc7684c897b7b6d42e381e47f6ff8e106
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501399"
---
# <span data-ttu-id="4059c-101">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="4059c-101">Set-AzureRmSchedulerHttpJob</span></span>

## <span data-ttu-id="4059c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4059c-102">SYNOPSIS</span></span>
<span data-ttu-id="4059c-103">Ütemező HTTP-feladat módosítása</span><span class="sxs-lookup"><span data-stu-id="4059c-103">Modifies a Scheduler HTTP job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4059c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4059c-104">SYNTAX</span></span>

```
Set-AzureRmSchedulerHttpJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 [-Method <String>] [-Uri <Uri>] [-RequestBody <String>] [-Headers <Hashtable>]
 [-HttpAuthenticationType <String>] [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4059c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4059c-105">DESCRIPTION</span></span>
<span data-ttu-id="4059c-106">A **set-AzureRmSchedulerHttpJob** PARANCSMAG a http-feladatot az Azure Scheduler-ban módosítja.</span><span class="sxs-lookup"><span data-stu-id="4059c-106">The **Set-AzureRmSchedulerHttpJob** cmdlet modifies an HTTP job in Azure Scheduler.</span></span>

<span data-ttu-id="4059c-107">Ez a parancsmag a *ErrorActionType* és a *HttpAuthenticationType* paraméterek alapján támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="4059c-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* and *HttpAuthenticationType* parameters.</span></span>
<span data-ttu-id="4059c-108">A dinamikus paraméterek elérhetővé válnak a többi paraméter-érték alapján.</span><span class="sxs-lookup"><span data-stu-id="4059c-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="4059c-109">Ha meg szeretné ismerni a dinamikus paraméterek nevét a többi paraméter megadása után, írjon be egy kötőjelet (-), majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="4059c-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="4059c-110">Ha kihagyja a kötelező paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="4059c-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="4059c-111">Példák</span><span class="sxs-lookup"><span data-stu-id="4059c-111">EXAMPLES</span></span>

## <span data-ttu-id="4059c-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4059c-112">PARAMETERS</span></span>

### <span data-ttu-id="4059c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4059c-113">-DefaultProfile</span></span>
<span data-ttu-id="4059c-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4059c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4059c-115">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="4059c-115">-EndTime</span></span>
<span data-ttu-id="4059c-116">A projekthez tartozó **datetime** -objektum záró időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4059c-116">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="4059c-117">Ha **datetime** típusú objektumot szeretne beolvasni, használja az Get-Date parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="4059c-117">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="4059c-118">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="4059c-118">-ErrorActionType</span></span>
<span data-ttu-id="4059c-119">A feladat hibaérték-beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="4059c-119">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="4059c-120">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="4059c-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4059c-121">Http</span><span class="sxs-lookup"><span data-stu-id="4059c-121">Http</span></span> 
- <span data-ttu-id="4059c-122">Https</span><span class="sxs-lookup"><span data-stu-id="4059c-122">Https</span></span> 
- <span data-ttu-id="4059c-123">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="4059c-123">StorageQueue</span></span> 
- <span data-ttu-id="4059c-124">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="4059c-124">ServiceBusQueue</span></span> 
- <span data-ttu-id="4059c-125">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="4059c-125">ServiceBusTopic</span></span>

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

### <span data-ttu-id="4059c-126">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="4059c-126">-ExecutionCount</span></span>
<span data-ttu-id="4059c-127">Itt adhatja meg, hogy hányszor fusson a feladat.</span><span class="sxs-lookup"><span data-stu-id="4059c-127">Specifies how many times the job runs.</span></span>
<span data-ttu-id="4059c-128">Alapértelmezés szerint a feladat határozatlan ideig ismétlődik.</span><span class="sxs-lookup"><span data-stu-id="4059c-128">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="4059c-129">-Gyakoriság</span><span class="sxs-lookup"><span data-stu-id="4059c-129">-Frequency</span></span>
<span data-ttu-id="4059c-130">A feladat maximális gyakoriságát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4059c-130">Specifies the maximum frequency for the job.</span></span>
<span data-ttu-id="4059c-131">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="4059c-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4059c-132">Perces</span><span class="sxs-lookup"><span data-stu-id="4059c-132">Minute</span></span> 
- <span data-ttu-id="4059c-133">Óra</span><span class="sxs-lookup"><span data-stu-id="4059c-133">Hour</span></span> 
- <span data-ttu-id="4059c-134">Nap</span><span class="sxs-lookup"><span data-stu-id="4059c-134">Day</span></span> 
- <span data-ttu-id="4059c-135">Héten</span><span class="sxs-lookup"><span data-stu-id="4059c-135">Week</span></span> 
- <span data-ttu-id="4059c-136">Hónap</span><span class="sxs-lookup"><span data-stu-id="4059c-136">Month</span></span>

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

### <span data-ttu-id="4059c-137">– Fejlécek</span><span class="sxs-lookup"><span data-stu-id="4059c-137">-Headers</span></span>
<span data-ttu-id="4059c-138">A fejléceket tartalmazó kivonatoló táblát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4059c-138">Specifies a hash table that contains headers.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4059c-139">-HttpAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="4059c-139">-HttpAuthenticationType</span></span>
<span data-ttu-id="4059c-140">A HTTP-hitelesítési típust adja meg.</span><span class="sxs-lookup"><span data-stu-id="4059c-140">Specifies the HTTP authentication type.</span></span>
<span data-ttu-id="4059c-141">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="4059c-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4059c-142">Nincs</span><span class="sxs-lookup"><span data-stu-id="4059c-142">None</span></span> 
- <span data-ttu-id="4059c-143">ClientCertificate</span><span class="sxs-lookup"><span data-stu-id="4059c-143">ClientCertificate</span></span> 
- <span data-ttu-id="4059c-144">ActiveDirectoryOAuth</span><span class="sxs-lookup"><span data-stu-id="4059c-144">ActiveDirectoryOAuth</span></span> 
- <span data-ttu-id="4059c-145">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="4059c-145">Basic</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: None, ClientCertificate, ActiveDirectoryOAuth, Basic

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4059c-146">-Intervallum</span><span class="sxs-lookup"><span data-stu-id="4059c-146">-Interval</span></span>
<span data-ttu-id="4059c-147">A feladat ismétlődésének intervallumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4059c-147">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="4059c-148">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="4059c-148">-JobCollectionName</span></span>
<span data-ttu-id="4059c-149">Annak a feladatnak a neve, amelyhez a projekt tartozik.</span><span class="sxs-lookup"><span data-stu-id="4059c-149">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="4059c-150">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="4059c-150">-JobName</span></span>
<span data-ttu-id="4059c-151">Annak a feladatnak a nevét adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="4059c-151">Specifies the name of the job that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="4059c-152">-JobState</span><span class="sxs-lookup"><span data-stu-id="4059c-152">-JobState</span></span>
<span data-ttu-id="4059c-153">A feladat állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4059c-153">Specifies the state of the job.</span></span>
<span data-ttu-id="4059c-154">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="4059c-154">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4059c-155">Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="4059c-155">Enabled</span></span> 
- <span data-ttu-id="4059c-156">Tiltva</span><span class="sxs-lookup"><span data-stu-id="4059c-156">Disabled</span></span>

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

### <span data-ttu-id="4059c-157">-Módszer</span><span class="sxs-lookup"><span data-stu-id="4059c-157">-Method</span></span>
<span data-ttu-id="4059c-158">A tevékenységhez tartozó Művelettípus metódusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4059c-158">Specifies the method for the action types for this job.</span></span>
<span data-ttu-id="4059c-159">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="4059c-159">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4059c-160">BESZERZÉSE</span><span class="sxs-lookup"><span data-stu-id="4059c-160">GET</span></span> 
- <span data-ttu-id="4059c-161">HELYEZNI</span><span class="sxs-lookup"><span data-stu-id="4059c-161">PUT</span></span> 
- <span data-ttu-id="4059c-162">POST</span><span class="sxs-lookup"><span data-stu-id="4059c-162">POST</span></span> 
- <span data-ttu-id="4059c-163">TÖRLÉSE</span><span class="sxs-lookup"><span data-stu-id="4059c-163">DELETE</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: GET, PUT, POST, DELETE

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4059c-164">-RequestBody</span><span class="sxs-lookup"><span data-stu-id="4059c-164">-RequestBody</span></span>
<span data-ttu-id="4059c-165">A feladatok elvégzéséhez és KÖZZÉTÉTELéhez szükséges törzs értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4059c-165">Specifies the value of the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="4059c-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4059c-166">-ResourceGroupName</span></span>
<span data-ttu-id="4059c-167">Azt az erőforráscsoport-csoportot adja meg, amelyhez a projekt tartozik.</span><span class="sxs-lookup"><span data-stu-id="4059c-167">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="4059c-168">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="4059c-168">-StartTime</span></span>
<span data-ttu-id="4059c-169">A projekthez tartozó **datetime** -objektum kezdési időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4059c-169">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="4059c-170">-URI</span><span class="sxs-lookup"><span data-stu-id="4059c-170">-Uri</span></span>
<span data-ttu-id="4059c-171">A projektfeladat URI-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4059c-171">Specifies a URI for the job action.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4059c-172">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4059c-172">-Confirm</span></span>
<span data-ttu-id="4059c-173">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4059c-173">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4059c-174">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4059c-174">-WhatIf</span></span>
<span data-ttu-id="4059c-175">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4059c-175">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4059c-176">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4059c-176">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4059c-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4059c-177">CommonParameters</span></span>
<span data-ttu-id="4059c-178">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4059c-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4059c-179">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4059c-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4059c-180">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4059c-180">INPUTS</span></span>

### <span data-ttu-id="4059c-181">Nincs</span><span class="sxs-lookup"><span data-stu-id="4059c-181">None</span></span>
<span data-ttu-id="4059c-182">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="4059c-182">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4059c-183">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4059c-183">OUTPUTS</span></span>

### <span data-ttu-id="4059c-184">Microsoft. Azure. Command. Scheduler. models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="4059c-184">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="4059c-185">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4059c-185">NOTES</span></span>

## <span data-ttu-id="4059c-186">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4059c-186">RELATED LINKS</span></span>

[<span data-ttu-id="4059c-187">Új – AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="4059c-187">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="4059c-188">Új – AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="4059c-188">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="4059c-189">Új – AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="4059c-189">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="4059c-190">Új – AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="4059c-190">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="4059c-191">Új – AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="4059c-191">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="4059c-192">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="4059c-192">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="4059c-193">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="4059c-193">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="4059c-194">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="4059c-194">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="4059c-195">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="4059c-195">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


