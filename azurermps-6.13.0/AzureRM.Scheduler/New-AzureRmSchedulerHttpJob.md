---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: E00D42D6-707A-479E-9964-C5B80D3DAA6A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/new-azurermschedulerhttpjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerHttpJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerHttpJob.md
ms.openlocfilehash: 1d0c66d3442d6db03897140849f5713d3107f8d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503363"
---
# <span data-ttu-id="bddb8-101">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="bddb8-101">New-AzureRmSchedulerHttpJob</span></span>

## <span data-ttu-id="bddb8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bddb8-102">SYNOPSIS</span></span>
<span data-ttu-id="bddb8-103">HTTP-feladatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="bddb8-103">Creates an HTTP job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bddb8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bddb8-104">SYNTAX</span></span>

```
New-AzureRmSchedulerHttpJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 -Method <String> -Uri <Uri> [-RequestBody <String>] [-Headers <Hashtable>] [-HttpAuthenticationType <String>]
 [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>] [-EndTime <DateTime>]
 [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bddb8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bddb8-105">DESCRIPTION</span></span>
<span data-ttu-id="bddb8-106">A **New-AzureRmSchedulerHttpJob** parancsmag http-feladatot hoz létre az Azure schedulerben.</span><span class="sxs-lookup"><span data-stu-id="bddb8-106">The **New-AzureRmSchedulerHttpJob** cmdlet creates an HTTP job in Azure Scheduler.</span></span>
<span data-ttu-id="bddb8-107">Ez a parancsmag a *ErrorActionType* és a *HttpAuthenticationType* paraméterek alapján támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="bddb8-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* and *HttpAuthenticationType* parameters.</span></span>
<span data-ttu-id="bddb8-108">A dinamikus paraméterek elérhetővé válnak a többi paraméter-érték alapján.</span><span class="sxs-lookup"><span data-stu-id="bddb8-108">Dynamic parameters become available based on other parameter values.</span></span>
<span data-ttu-id="bddb8-109">Ha meg szeretné ismerni a dinamikus paraméterek nevét a többi paraméter megadása után, írjon be egy kötőjelet (-), majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="bddb8-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="bddb8-110">Ha kihagyja a kötelező paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="bddb8-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="bddb8-111">Példák</span><span class="sxs-lookup"><span data-stu-id="bddb8-111">EXAMPLES</span></span>

## <span data-ttu-id="bddb8-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bddb8-112">PARAMETERS</span></span>

### <span data-ttu-id="bddb8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bddb8-113">-DefaultProfile</span></span>
<span data-ttu-id="bddb8-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bddb8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bddb8-115">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="bddb8-115">-EndTime</span></span>
<span data-ttu-id="bddb8-116">A projekthez tartozó **datetime** -objektum záró időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="bddb8-116">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="bddb8-117">Ha **datetime** típusú objektumot szeretne beolvasni, használja az Get-Date parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="bddb8-117">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="bddb8-118">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="bddb8-118">-ErrorActionType</span></span>
<span data-ttu-id="bddb8-119">A feladat hibaérték-beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="bddb8-119">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="bddb8-120">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="bddb8-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bddb8-121">Http</span><span class="sxs-lookup"><span data-stu-id="bddb8-121">Http</span></span> 
- <span data-ttu-id="bddb8-122">Https</span><span class="sxs-lookup"><span data-stu-id="bddb8-122">Https</span></span> 
- <span data-ttu-id="bddb8-123">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="bddb8-123">StorageQueue</span></span> 
- <span data-ttu-id="bddb8-124">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="bddb8-124">ServiceBusQueue</span></span> 
- <span data-ttu-id="bddb8-125">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="bddb8-125">ServiceBusTopic</span></span>

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

### <span data-ttu-id="bddb8-126">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="bddb8-126">-ExecutionCount</span></span>
<span data-ttu-id="bddb8-127">Itt adhatja meg, hogy hányszor fusson a feladat.</span><span class="sxs-lookup"><span data-stu-id="bddb8-127">Specifies how many times the job runs.</span></span>
<span data-ttu-id="bddb8-128">Alapértelmezés szerint a feladat határozatlan ideig ismétlődik.</span><span class="sxs-lookup"><span data-stu-id="bddb8-128">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="bddb8-129">-Gyakoriság</span><span class="sxs-lookup"><span data-stu-id="bddb8-129">-Frequency</span></span>
<span data-ttu-id="bddb8-130">A feladat maximális gyakoriságát adja meg.</span><span class="sxs-lookup"><span data-stu-id="bddb8-130">Specifies a maximum frequency for the job.</span></span>
<span data-ttu-id="bddb8-131">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="bddb8-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bddb8-132">Perces</span><span class="sxs-lookup"><span data-stu-id="bddb8-132">Minute</span></span> 
- <span data-ttu-id="bddb8-133">Óra</span><span class="sxs-lookup"><span data-stu-id="bddb8-133">Hour</span></span> 
- <span data-ttu-id="bddb8-134">Nap</span><span class="sxs-lookup"><span data-stu-id="bddb8-134">Day</span></span> 
- <span data-ttu-id="bddb8-135">Héten</span><span class="sxs-lookup"><span data-stu-id="bddb8-135">Week</span></span> 
- <span data-ttu-id="bddb8-136">Hónap</span><span class="sxs-lookup"><span data-stu-id="bddb8-136">Month</span></span>

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

### <span data-ttu-id="bddb8-137">– Fejlécek</span><span class="sxs-lookup"><span data-stu-id="bddb8-137">-Headers</span></span>
<span data-ttu-id="bddb8-138">A fejléceket tartalmazó kivonatoló táblát adja meg.</span><span class="sxs-lookup"><span data-stu-id="bddb8-138">Specifies a hash table that contains headers.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bddb8-139">-HttpAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="bddb8-139">-HttpAuthenticationType</span></span>
<span data-ttu-id="bddb8-140">A HTTP-hitelesítési típust adja meg.</span><span class="sxs-lookup"><span data-stu-id="bddb8-140">Specifies the HTTP authentication type.</span></span>
<span data-ttu-id="bddb8-141">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="bddb8-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bddb8-142">Nincs</span><span class="sxs-lookup"><span data-stu-id="bddb8-142">None</span></span> 
- <span data-ttu-id="bddb8-143">ClientCertificate</span><span class="sxs-lookup"><span data-stu-id="bddb8-143">ClientCertificate</span></span> 
- <span data-ttu-id="bddb8-144">ActiveDirectoryOAuth</span><span class="sxs-lookup"><span data-stu-id="bddb8-144">ActiveDirectoryOAuth</span></span> 
- <span data-ttu-id="bddb8-145">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="bddb8-145">Basic</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: None, ClientCertificate, ActiveDirectoryOAuth, Basic

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bddb8-146">-Intervallum</span><span class="sxs-lookup"><span data-stu-id="bddb8-146">-Interval</span></span>
<span data-ttu-id="bddb8-147">A feladat ismétlődésének intervallumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="bddb8-147">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="bddb8-148">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="bddb8-148">-JobCollectionName</span></span>
<span data-ttu-id="bddb8-149">Annak a feladatnak a neve, amelyhez a projekt tartozik.</span><span class="sxs-lookup"><span data-stu-id="bddb8-149">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="bddb8-150">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="bddb8-150">-JobName</span></span>
<span data-ttu-id="bddb8-151">A feladat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bddb8-151">Specifies a name for the job.</span></span>

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

### <span data-ttu-id="bddb8-152">-JobState</span><span class="sxs-lookup"><span data-stu-id="bddb8-152">-JobState</span></span>
<span data-ttu-id="bddb8-153">A feladat állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="bddb8-153">Specifies the state of the job.</span></span>
<span data-ttu-id="bddb8-154">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="bddb8-154">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bddb8-155">Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="bddb8-155">Enabled</span></span> 
- <span data-ttu-id="bddb8-156">Tiltva</span><span class="sxs-lookup"><span data-stu-id="bddb8-156">Disabled</span></span>

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

### <span data-ttu-id="bddb8-157">-Módszer</span><span class="sxs-lookup"><span data-stu-id="bddb8-157">-Method</span></span>
<span data-ttu-id="bddb8-158">A feladathoz tartozó Művelettípus metódusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="bddb8-158">Specifies the method for the action types for the job.</span></span>
<span data-ttu-id="bddb8-159">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="bddb8-159">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bddb8-160">BESZERZÉSE</span><span class="sxs-lookup"><span data-stu-id="bddb8-160">GET</span></span> 
- <span data-ttu-id="bddb8-161">HELYEZNI</span><span class="sxs-lookup"><span data-stu-id="bddb8-161">PUT</span></span> 
- <span data-ttu-id="bddb8-162">POST</span><span class="sxs-lookup"><span data-stu-id="bddb8-162">POST</span></span> 
- <span data-ttu-id="bddb8-163">TÖRLÉSE</span><span class="sxs-lookup"><span data-stu-id="bddb8-163">DELETE</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GET, PUT, POST, DELETE

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bddb8-164">-RequestBody</span><span class="sxs-lookup"><span data-stu-id="bddb8-164">-RequestBody</span></span>
<span data-ttu-id="bddb8-165">A feladatok elvégzéséhez és KÖZZÉTÉTELéhez szükséges törzs értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bddb8-165">Specifies the value of the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="bddb8-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bddb8-166">-ResourceGroupName</span></span>
<span data-ttu-id="bddb8-167">Azt az erőforráscsoport-csoportot adja meg, amelyhez a projekt tartozik.</span><span class="sxs-lookup"><span data-stu-id="bddb8-167">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="bddb8-168">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="bddb8-168">-StartTime</span></span>
<span data-ttu-id="bddb8-169">A projekthez tartozó **datetime** -objektum kezdési időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="bddb8-169">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="bddb8-170">-URI</span><span class="sxs-lookup"><span data-stu-id="bddb8-170">-Uri</span></span>
<span data-ttu-id="bddb8-171">A projektfeladat URI-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="bddb8-171">Specifies a URI for the job action.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bddb8-172">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bddb8-172">-Confirm</span></span>
<span data-ttu-id="bddb8-173">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bddb8-173">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bddb8-174">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bddb8-174">-WhatIf</span></span>
<span data-ttu-id="bddb8-175">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bddb8-175">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bddb8-176">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bddb8-176">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bddb8-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bddb8-177">CommonParameters</span></span>
<span data-ttu-id="bddb8-178">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bddb8-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bddb8-179">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bddb8-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bddb8-180">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bddb8-180">INPUTS</span></span>

### <span data-ttu-id="bddb8-181">System. String</span><span class="sxs-lookup"><span data-stu-id="bddb8-181">System.String</span></span>

### <span data-ttu-id="bddb8-182">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="bddb8-182">System.Collections.Hashtable</span></span>

## <span data-ttu-id="bddb8-183">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bddb8-183">OUTPUTS</span></span>

### <span data-ttu-id="bddb8-184">Microsoft. Azure. Command. Scheduler. models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="bddb8-184">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="bddb8-185">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bddb8-185">NOTES</span></span>

## <span data-ttu-id="bddb8-186">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bddb8-186">RELATED LINKS</span></span>

[<span data-ttu-id="bddb8-187">Új – AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="bddb8-187">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="bddb8-188">Új – AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="bddb8-188">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="bddb8-189">Új – AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="bddb8-189">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="bddb8-190">Új – AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="bddb8-190">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="bddb8-191">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="bddb8-191">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="bddb8-192">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="bddb8-192">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="bddb8-193">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="bddb8-193">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="bddb8-194">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="bddb8-194">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="bddb8-195">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="bddb8-195">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


