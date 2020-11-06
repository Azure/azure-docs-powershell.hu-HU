---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: E00D42D6-707A-479E-9964-C5B80D3DAA6A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/new-azurermschedulerhttpjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerHttpJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerHttpJob.md
ms.openlocfilehash: a3fdbb3732def98bbf885cb58bf6f00dcb61eb4b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493020"
---
# <span data-ttu-id="41559-101">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="41559-101">New-AzureRmSchedulerHttpJob</span></span>

## <span data-ttu-id="41559-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="41559-102">SYNOPSIS</span></span>
<span data-ttu-id="41559-103">HTTP-feladatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="41559-103">Creates an HTTP job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41559-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="41559-104">SYNTAX</span></span>

```
New-AzureRmSchedulerHttpJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 -Method <String> -Uri <Uri> [-RequestBody <String>] [-Headers <Hashtable>] [-HttpAuthenticationType <String>]
 [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>] [-EndTime <DateTime>]
 [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41559-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="41559-105">DESCRIPTION</span></span>
<span data-ttu-id="41559-106">A **New-AzureRmSchedulerHttpJob** parancsmag http-feladatot hoz létre az Azure schedulerben.</span><span class="sxs-lookup"><span data-stu-id="41559-106">The **New-AzureRmSchedulerHttpJob** cmdlet creates an HTTP job in Azure Scheduler.</span></span>

<span data-ttu-id="41559-107">Ez a parancsmag a *ErrorActionType* és a *HttpAuthenticationType* paraméterek alapján támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="41559-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* and *HttpAuthenticationType* parameters.</span></span>
<span data-ttu-id="41559-108">A dinamikus paraméterek elérhetővé válnak a többi paraméter-érték alapján.</span><span class="sxs-lookup"><span data-stu-id="41559-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="41559-109">Ha meg szeretné ismerni a dinamikus paraméterek nevét a többi paraméter megadása után, írjon be egy kötőjelet (-), majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="41559-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="41559-110">Ha kihagyja a kötelező paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="41559-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="41559-111">Példák</span><span class="sxs-lookup"><span data-stu-id="41559-111">EXAMPLES</span></span>

## <span data-ttu-id="41559-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="41559-112">PARAMETERS</span></span>

### <span data-ttu-id="41559-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41559-113">-DefaultProfile</span></span>
<span data-ttu-id="41559-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="41559-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41559-115">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="41559-115">-EndTime</span></span>
<span data-ttu-id="41559-116">A projekthez tartozó **datetime** -objektum záró időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="41559-116">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="41559-117">Ha **datetime** típusú objektumot szeretne beolvasni, használja az Get-Date parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="41559-117">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="41559-118">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="41559-118">-ErrorActionType</span></span>
<span data-ttu-id="41559-119">A feladat hibaérték-beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="41559-119">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="41559-120">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="41559-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="41559-121">Http</span><span class="sxs-lookup"><span data-stu-id="41559-121">Http</span></span> 
- <span data-ttu-id="41559-122">Https</span><span class="sxs-lookup"><span data-stu-id="41559-122">Https</span></span> 
- <span data-ttu-id="41559-123">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="41559-123">StorageQueue</span></span> 
- <span data-ttu-id="41559-124">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="41559-124">ServiceBusQueue</span></span> 
- <span data-ttu-id="41559-125">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="41559-125">ServiceBusTopic</span></span>

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

### <span data-ttu-id="41559-126">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="41559-126">-ExecutionCount</span></span>
<span data-ttu-id="41559-127">Itt adhatja meg, hogy hányszor fusson a feladat.</span><span class="sxs-lookup"><span data-stu-id="41559-127">Specifies how many times the job runs.</span></span>
<span data-ttu-id="41559-128">Alapértelmezés szerint a feladat határozatlan ideig ismétlődik.</span><span class="sxs-lookup"><span data-stu-id="41559-128">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="41559-129">-Gyakoriság</span><span class="sxs-lookup"><span data-stu-id="41559-129">-Frequency</span></span>
<span data-ttu-id="41559-130">A feladat maximális gyakoriságát adja meg.</span><span class="sxs-lookup"><span data-stu-id="41559-130">Specifies a maximum frequency for the job.</span></span>
<span data-ttu-id="41559-131">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="41559-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="41559-132">Perces</span><span class="sxs-lookup"><span data-stu-id="41559-132">Minute</span></span> 
- <span data-ttu-id="41559-133">Óra</span><span class="sxs-lookup"><span data-stu-id="41559-133">Hour</span></span> 
- <span data-ttu-id="41559-134">Nap</span><span class="sxs-lookup"><span data-stu-id="41559-134">Day</span></span> 
- <span data-ttu-id="41559-135">Héten</span><span class="sxs-lookup"><span data-stu-id="41559-135">Week</span></span> 
- <span data-ttu-id="41559-136">Hónap</span><span class="sxs-lookup"><span data-stu-id="41559-136">Month</span></span>

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

### <span data-ttu-id="41559-137">– Fejlécek</span><span class="sxs-lookup"><span data-stu-id="41559-137">-Headers</span></span>
<span data-ttu-id="41559-138">A fejléceket tartalmazó kivonatoló táblát adja meg.</span><span class="sxs-lookup"><span data-stu-id="41559-138">Specifies a hash table that contains headers.</span></span>

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

### <span data-ttu-id="41559-139">-HttpAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="41559-139">-HttpAuthenticationType</span></span>
<span data-ttu-id="41559-140">A HTTP-hitelesítési típust adja meg.</span><span class="sxs-lookup"><span data-stu-id="41559-140">Specifies the HTTP authentication type.</span></span>
<span data-ttu-id="41559-141">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="41559-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="41559-142">Nincs</span><span class="sxs-lookup"><span data-stu-id="41559-142">None</span></span> 
- <span data-ttu-id="41559-143">ClientCertificate</span><span class="sxs-lookup"><span data-stu-id="41559-143">ClientCertificate</span></span> 
- <span data-ttu-id="41559-144">ActiveDirectoryOAuth</span><span class="sxs-lookup"><span data-stu-id="41559-144">ActiveDirectoryOAuth</span></span> 
- <span data-ttu-id="41559-145">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="41559-145">Basic</span></span>

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

### <span data-ttu-id="41559-146">-Intervallum</span><span class="sxs-lookup"><span data-stu-id="41559-146">-Interval</span></span>
<span data-ttu-id="41559-147">A feladat ismétlődésének intervallumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="41559-147">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="41559-148">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="41559-148">-JobCollectionName</span></span>
<span data-ttu-id="41559-149">Annak a feladatnak a neve, amelyhez a projekt tartozik.</span><span class="sxs-lookup"><span data-stu-id="41559-149">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="41559-150">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="41559-150">-JobName</span></span>
<span data-ttu-id="41559-151">A feladat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="41559-151">Specifies a name for the job.</span></span>

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

### <span data-ttu-id="41559-152">-JobState</span><span class="sxs-lookup"><span data-stu-id="41559-152">-JobState</span></span>
<span data-ttu-id="41559-153">A feladat állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="41559-153">Specifies the state of the job.</span></span>
<span data-ttu-id="41559-154">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="41559-154">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="41559-155">Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="41559-155">Enabled</span></span> 
- <span data-ttu-id="41559-156">Tiltva</span><span class="sxs-lookup"><span data-stu-id="41559-156">Disabled</span></span>

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

### <span data-ttu-id="41559-157">-Módszer</span><span class="sxs-lookup"><span data-stu-id="41559-157">-Method</span></span>
<span data-ttu-id="41559-158">A feladathoz tartozó Művelettípus metódusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="41559-158">Specifies the method for the action types for the job.</span></span>
<span data-ttu-id="41559-159">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="41559-159">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="41559-160">BESZERZÉSE</span><span class="sxs-lookup"><span data-stu-id="41559-160">GET</span></span> 
- <span data-ttu-id="41559-161">HELYEZNI</span><span class="sxs-lookup"><span data-stu-id="41559-161">PUT</span></span> 
- <span data-ttu-id="41559-162">POST</span><span class="sxs-lookup"><span data-stu-id="41559-162">POST</span></span> 
- <span data-ttu-id="41559-163">TÖRLÉSE</span><span class="sxs-lookup"><span data-stu-id="41559-163">DELETE</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: GET, PUT, POST, DELETE

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41559-164">-RequestBody</span><span class="sxs-lookup"><span data-stu-id="41559-164">-RequestBody</span></span>
<span data-ttu-id="41559-165">A feladatok elvégzéséhez és KÖZZÉTÉTELéhez szükséges törzs értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="41559-165">Specifies the value of the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="41559-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41559-166">-ResourceGroupName</span></span>
<span data-ttu-id="41559-167">Azt az erőforráscsoport-csoportot adja meg, amelyhez a projekt tartozik.</span><span class="sxs-lookup"><span data-stu-id="41559-167">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="41559-168">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="41559-168">-StartTime</span></span>
<span data-ttu-id="41559-169">A projekthez tartozó **datetime** -objektum kezdési időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="41559-169">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="41559-170">-URI</span><span class="sxs-lookup"><span data-stu-id="41559-170">-Uri</span></span>
<span data-ttu-id="41559-171">A projektfeladat URI-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="41559-171">Specifies a URI for the job action.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41559-172">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="41559-172">-Confirm</span></span>
<span data-ttu-id="41559-173">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="41559-173">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41559-174">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41559-174">-WhatIf</span></span>
<span data-ttu-id="41559-175">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="41559-175">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41559-176">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="41559-176">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41559-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41559-177">CommonParameters</span></span>
<span data-ttu-id="41559-178">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="41559-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41559-179">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41559-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41559-180">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="41559-180">INPUTS</span></span>

### <span data-ttu-id="41559-181">Nincs</span><span class="sxs-lookup"><span data-stu-id="41559-181">None</span></span>
<span data-ttu-id="41559-182">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="41559-182">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="41559-183">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="41559-183">OUTPUTS</span></span>

### <span data-ttu-id="41559-184">Microsoft. Azure. Command. Scheduler. models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="41559-184">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="41559-185">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="41559-185">NOTES</span></span>

## <span data-ttu-id="41559-186">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="41559-186">RELATED LINKS</span></span>

[<span data-ttu-id="41559-187">Új – AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="41559-187">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="41559-188">Új – AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="41559-188">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="41559-189">Új – AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="41559-189">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="41559-190">Új – AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="41559-190">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="41559-191">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="41559-191">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="41559-192">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="41559-192">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="41559-193">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="41559-193">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="41559-194">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="41559-194">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="41559-195">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="41559-195">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


