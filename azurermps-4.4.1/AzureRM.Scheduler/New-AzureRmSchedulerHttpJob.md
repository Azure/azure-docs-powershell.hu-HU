---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: E00D42D6-707A-479E-9964-C5B80D3DAA6A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerHttpJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerHttpJob.md
ms.openlocfilehash: 5fc591ff5d24211b8af464dab46bfb81360f83e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679335"
---
# <span data-ttu-id="e2386-101">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="e2386-101">New-AzureRmSchedulerHttpJob</span></span>

## <span data-ttu-id="e2386-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e2386-102">SYNOPSIS</span></span>
<span data-ttu-id="e2386-103">HTTP-feladatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="e2386-103">Creates an HTTP job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2386-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e2386-104">SYNTAX</span></span>

```
New-AzureRmSchedulerHttpJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 -Method <String> -Uri <Uri> [-RequestBody <String>] [-Headers <Hashtable>] [-HttpAuthenticationType <String>]
 [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>] [-EndTime <DateTime>]
 [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2386-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e2386-105">DESCRIPTION</span></span>
<span data-ttu-id="e2386-106">A **New-AzureRmSchedulerHttpJob** parancsmag http-feladatot hoz létre az Azure schedulerben.</span><span class="sxs-lookup"><span data-stu-id="e2386-106">The **New-AzureRmSchedulerHttpJob** cmdlet creates an HTTP job in Azure Scheduler.</span></span>

<span data-ttu-id="e2386-107">Ez a parancsmag a *ErrorActionType* és a *HttpAuthenticationType* paraméterek alapján támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="e2386-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* and *HttpAuthenticationType* parameters.</span></span>
<span data-ttu-id="e2386-108">A dinamikus paraméterek elérhetővé válnak a többi paraméter-érték alapján.</span><span class="sxs-lookup"><span data-stu-id="e2386-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="e2386-109">Ha meg szeretné ismerni a dinamikus paraméterek nevét a többi paraméter megadása után, írjon be egy kötőjelet (-), majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="e2386-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="e2386-110">Ha kihagyja a kötelező paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="e2386-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="e2386-111">Példák</span><span class="sxs-lookup"><span data-stu-id="e2386-111">EXAMPLES</span></span>

## <span data-ttu-id="e2386-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e2386-112">PARAMETERS</span></span>

### <span data-ttu-id="e2386-113">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="e2386-113">-EndTime</span></span>
<span data-ttu-id="e2386-114">A projekthez tartozó **datetime** -objektum záró időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e2386-114">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="e2386-115">Ha **datetime** típusú objektumot szeretne beolvasni, használja az Get-Date parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="e2386-115">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="e2386-116">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="e2386-116">-ErrorActionType</span></span>
<span data-ttu-id="e2386-117">A feladat hibaérték-beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="e2386-117">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="e2386-118">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="e2386-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e2386-119">Http</span><span class="sxs-lookup"><span data-stu-id="e2386-119">Http</span></span> 
- <span data-ttu-id="e2386-120">Https</span><span class="sxs-lookup"><span data-stu-id="e2386-120">Https</span></span> 
- <span data-ttu-id="e2386-121">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="e2386-121">StorageQueue</span></span> 
- <span data-ttu-id="e2386-122">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="e2386-122">ServiceBusQueue</span></span> 
- <span data-ttu-id="e2386-123">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="e2386-123">ServiceBusTopic</span></span>

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

### <span data-ttu-id="e2386-124">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="e2386-124">-ExecutionCount</span></span>
<span data-ttu-id="e2386-125">Itt adhatja meg, hogy hányszor fusson a feladat.</span><span class="sxs-lookup"><span data-stu-id="e2386-125">Specifies how many times the job runs.</span></span>
<span data-ttu-id="e2386-126">Alapértelmezés szerint a feladat határozatlan ideig ismétlődik.</span><span class="sxs-lookup"><span data-stu-id="e2386-126">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="e2386-127">-Gyakoriság</span><span class="sxs-lookup"><span data-stu-id="e2386-127">-Frequency</span></span>
<span data-ttu-id="e2386-128">A feladat maximális gyakoriságát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e2386-128">Specifies a maximum frequency for the job.</span></span>
<span data-ttu-id="e2386-129">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="e2386-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e2386-130">Perces</span><span class="sxs-lookup"><span data-stu-id="e2386-130">Minute</span></span> 
- <span data-ttu-id="e2386-131">Óra</span><span class="sxs-lookup"><span data-stu-id="e2386-131">Hour</span></span> 
- <span data-ttu-id="e2386-132">Nap</span><span class="sxs-lookup"><span data-stu-id="e2386-132">Day</span></span> 
- <span data-ttu-id="e2386-133">Héten</span><span class="sxs-lookup"><span data-stu-id="e2386-133">Week</span></span> 
- <span data-ttu-id="e2386-134">Hónap</span><span class="sxs-lookup"><span data-stu-id="e2386-134">Month</span></span>

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

### <span data-ttu-id="e2386-135">– Fejlécek</span><span class="sxs-lookup"><span data-stu-id="e2386-135">-Headers</span></span>
<span data-ttu-id="e2386-136">A fejléceket tartalmazó kivonatoló táblát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e2386-136">Specifies a hash table that contains headers.</span></span>

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

### <span data-ttu-id="e2386-137">-HttpAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="e2386-137">-HttpAuthenticationType</span></span>
<span data-ttu-id="e2386-138">A HTTP-hitelesítési típust adja meg.</span><span class="sxs-lookup"><span data-stu-id="e2386-138">Specifies the HTTP authentication type.</span></span>
<span data-ttu-id="e2386-139">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="e2386-139">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e2386-140">Nincs</span><span class="sxs-lookup"><span data-stu-id="e2386-140">None</span></span> 
- <span data-ttu-id="e2386-141">ClientCertificate</span><span class="sxs-lookup"><span data-stu-id="e2386-141">ClientCertificate</span></span> 
- <span data-ttu-id="e2386-142">ActiveDirectoryOAuth</span><span class="sxs-lookup"><span data-stu-id="e2386-142">ActiveDirectoryOAuth</span></span> 
- <span data-ttu-id="e2386-143">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="e2386-143">Basic</span></span>

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

### <span data-ttu-id="e2386-144">-Intervallum</span><span class="sxs-lookup"><span data-stu-id="e2386-144">-Interval</span></span>
<span data-ttu-id="e2386-145">A feladat ismétlődésének intervallumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e2386-145">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="e2386-146">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="e2386-146">-JobCollectionName</span></span>
<span data-ttu-id="e2386-147">Annak a feladatnak a neve, amelyhez a projekt tartozik.</span><span class="sxs-lookup"><span data-stu-id="e2386-147">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="e2386-148">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="e2386-148">-JobName</span></span>
<span data-ttu-id="e2386-149">A feladat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e2386-149">Specifies a name for the job.</span></span>

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

### <span data-ttu-id="e2386-150">-JobState</span><span class="sxs-lookup"><span data-stu-id="e2386-150">-JobState</span></span>
<span data-ttu-id="e2386-151">A feladat állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e2386-151">Specifies the state of the job.</span></span>
<span data-ttu-id="e2386-152">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="e2386-152">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e2386-153">Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="e2386-153">Enabled</span></span> 
- <span data-ttu-id="e2386-154">Tiltva</span><span class="sxs-lookup"><span data-stu-id="e2386-154">Disabled</span></span>

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

### <span data-ttu-id="e2386-155">-Módszer</span><span class="sxs-lookup"><span data-stu-id="e2386-155">-Method</span></span>
<span data-ttu-id="e2386-156">A feladathoz tartozó Művelettípus metódusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e2386-156">Specifies the method for the action types for the job.</span></span>
<span data-ttu-id="e2386-157">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="e2386-157">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e2386-158">BESZERZÉSE</span><span class="sxs-lookup"><span data-stu-id="e2386-158">GET</span></span> 
- <span data-ttu-id="e2386-159">HELYEZNI</span><span class="sxs-lookup"><span data-stu-id="e2386-159">PUT</span></span> 
- <span data-ttu-id="e2386-160">POST</span><span class="sxs-lookup"><span data-stu-id="e2386-160">POST</span></span> 
- <span data-ttu-id="e2386-161">TÖRLÉSE</span><span class="sxs-lookup"><span data-stu-id="e2386-161">DELETE</span></span>

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

### <span data-ttu-id="e2386-162">-RequestBody</span><span class="sxs-lookup"><span data-stu-id="e2386-162">-RequestBody</span></span>
<span data-ttu-id="e2386-163">A feladatok elvégzéséhez és KÖZZÉTÉTELéhez szükséges törzs értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e2386-163">Specifies the value of the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="e2386-164">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2386-164">-ResourceGroupName</span></span>
<span data-ttu-id="e2386-165">Azt az erőforráscsoport-csoportot adja meg, amelyhez a projekt tartozik.</span><span class="sxs-lookup"><span data-stu-id="e2386-165">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="e2386-166">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="e2386-166">-StartTime</span></span>
<span data-ttu-id="e2386-167">A projekthez tartozó **datetime** -objektum kezdési időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e2386-167">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="e2386-168">-URI</span><span class="sxs-lookup"><span data-stu-id="e2386-168">-Uri</span></span>
<span data-ttu-id="e2386-169">A projektfeladat URI-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e2386-169">Specifies a URI for the job action.</span></span>

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

### <span data-ttu-id="e2386-170">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e2386-170">-Confirm</span></span>
<span data-ttu-id="e2386-171">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e2386-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2386-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2386-172">-WhatIf</span></span>
<span data-ttu-id="e2386-173">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e2386-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2386-174">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e2386-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2386-175">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2386-175">-DefaultProfile</span></span>
<span data-ttu-id="e2386-176">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e2386-176">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2386-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2386-177">CommonParameters</span></span>
<span data-ttu-id="e2386-178">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e2386-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2386-179">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2386-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2386-180">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e2386-180">INPUTS</span></span>

## <span data-ttu-id="e2386-181">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e2386-181">OUTPUTS</span></span>

### <span data-ttu-id="e2386-182">Microsoft. Azure. Command. Scheduler. models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="e2386-182">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="e2386-183">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e2386-183">NOTES</span></span>

## <span data-ttu-id="e2386-184">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e2386-184">RELATED LINKS</span></span>

[<span data-ttu-id="e2386-185">Új – AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="e2386-185">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="e2386-186">Új – AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="e2386-186">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="e2386-187">Új – AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="e2386-187">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="e2386-188">Új – AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="e2386-188">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="e2386-189">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="e2386-189">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="e2386-190">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="e2386-190">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="e2386-191">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="e2386-191">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="e2386-192">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="e2386-192">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="e2386-193">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="e2386-193">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


