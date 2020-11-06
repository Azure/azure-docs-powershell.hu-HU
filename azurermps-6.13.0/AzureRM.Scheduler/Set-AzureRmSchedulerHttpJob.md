---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: D9FA686C-48BB-48A1-926C-56B8151F8F82
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/set-azurermschedulerhttpjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerHttpJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerHttpJob.md
ms.openlocfilehash: 2810a73e54151d8227a115aa71f486d09811def8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493933"
---
# <span data-ttu-id="a3036-101">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="a3036-101">Set-AzureRmSchedulerHttpJob</span></span>

## <span data-ttu-id="a3036-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a3036-102">SYNOPSIS</span></span>
<span data-ttu-id="a3036-103">Ütemező HTTP-feladat módosítása</span><span class="sxs-lookup"><span data-stu-id="a3036-103">Modifies a Scheduler HTTP job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a3036-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a3036-104">SYNTAX</span></span>

```
Set-AzureRmSchedulerHttpJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 [-Method <String>] [-Uri <Uri>] [-RequestBody <String>] [-Headers <Hashtable>]
 [-HttpAuthenticationType <String>] [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3036-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a3036-105">DESCRIPTION</span></span>
<span data-ttu-id="a3036-106">A **set-AzureRmSchedulerHttpJob** PARANCSMAG a http-feladatot az Azure Scheduler-ban módosítja.</span><span class="sxs-lookup"><span data-stu-id="a3036-106">The **Set-AzureRmSchedulerHttpJob** cmdlet modifies an HTTP job in Azure Scheduler.</span></span>
<span data-ttu-id="a3036-107">Ez a parancsmag a *ErrorActionType* és a *HttpAuthenticationType* paraméterek alapján támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="a3036-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* and *HttpAuthenticationType* parameters.</span></span>
<span data-ttu-id="a3036-108">A dinamikus paraméterek elérhetővé válnak a többi paraméter-érték alapján.</span><span class="sxs-lookup"><span data-stu-id="a3036-108">Dynamic parameters become available based on other parameter values.</span></span>
<span data-ttu-id="a3036-109">Ha meg szeretné ismerni a dinamikus paraméterek nevét a többi paraméter megadása után, írjon be egy kötőjelet (-), majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="a3036-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="a3036-110">Ha kihagyja a kötelező paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="a3036-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="a3036-111">Példák</span><span class="sxs-lookup"><span data-stu-id="a3036-111">EXAMPLES</span></span>

## <span data-ttu-id="a3036-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a3036-112">PARAMETERS</span></span>

### <span data-ttu-id="a3036-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3036-113">-DefaultProfile</span></span>
<span data-ttu-id="a3036-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a3036-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3036-115">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="a3036-115">-EndTime</span></span>
<span data-ttu-id="a3036-116">A projekthez tartozó **datetime** -objektum záró időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a3036-116">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="a3036-117">Ha **datetime** típusú objektumot szeretne beolvasni, használja az Get-Date parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="a3036-117">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="a3036-118">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="a3036-118">-ErrorActionType</span></span>
<span data-ttu-id="a3036-119">A feladat hibaérték-beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="a3036-119">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="a3036-120">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="a3036-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a3036-121">Http</span><span class="sxs-lookup"><span data-stu-id="a3036-121">Http</span></span> 
- <span data-ttu-id="a3036-122">Https</span><span class="sxs-lookup"><span data-stu-id="a3036-122">Https</span></span> 
- <span data-ttu-id="a3036-123">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="a3036-123">StorageQueue</span></span> 
- <span data-ttu-id="a3036-124">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="a3036-124">ServiceBusQueue</span></span> 
- <span data-ttu-id="a3036-125">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="a3036-125">ServiceBusTopic</span></span>

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

### <span data-ttu-id="a3036-126">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="a3036-126">-ExecutionCount</span></span>
<span data-ttu-id="a3036-127">Itt adhatja meg, hogy hányszor fusson a feladat.</span><span class="sxs-lookup"><span data-stu-id="a3036-127">Specifies how many times the job runs.</span></span>
<span data-ttu-id="a3036-128">Alapértelmezés szerint a feladat határozatlan ideig ismétlődik.</span><span class="sxs-lookup"><span data-stu-id="a3036-128">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="a3036-129">-Gyakoriság</span><span class="sxs-lookup"><span data-stu-id="a3036-129">-Frequency</span></span>
<span data-ttu-id="a3036-130">A feladat maximális gyakoriságát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a3036-130">Specifies the maximum frequency for the job.</span></span>
<span data-ttu-id="a3036-131">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="a3036-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a3036-132">Perces</span><span class="sxs-lookup"><span data-stu-id="a3036-132">Minute</span></span> 
- <span data-ttu-id="a3036-133">Óra</span><span class="sxs-lookup"><span data-stu-id="a3036-133">Hour</span></span> 
- <span data-ttu-id="a3036-134">Nap</span><span class="sxs-lookup"><span data-stu-id="a3036-134">Day</span></span> 
- <span data-ttu-id="a3036-135">Héten</span><span class="sxs-lookup"><span data-stu-id="a3036-135">Week</span></span> 
- <span data-ttu-id="a3036-136">Hónap</span><span class="sxs-lookup"><span data-stu-id="a3036-136">Month</span></span>

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

### <span data-ttu-id="a3036-137">– Fejlécek</span><span class="sxs-lookup"><span data-stu-id="a3036-137">-Headers</span></span>
<span data-ttu-id="a3036-138">A fejléceket tartalmazó kivonatoló táblát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a3036-138">Specifies a hash table that contains headers.</span></span>

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

### <span data-ttu-id="a3036-139">-HttpAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="a3036-139">-HttpAuthenticationType</span></span>
<span data-ttu-id="a3036-140">A HTTP-hitelesítési típust adja meg.</span><span class="sxs-lookup"><span data-stu-id="a3036-140">Specifies the HTTP authentication type.</span></span>
<span data-ttu-id="a3036-141">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="a3036-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a3036-142">Nincs</span><span class="sxs-lookup"><span data-stu-id="a3036-142">None</span></span> 
- <span data-ttu-id="a3036-143">ClientCertificate</span><span class="sxs-lookup"><span data-stu-id="a3036-143">ClientCertificate</span></span> 
- <span data-ttu-id="a3036-144">ActiveDirectoryOAuth</span><span class="sxs-lookup"><span data-stu-id="a3036-144">ActiveDirectoryOAuth</span></span> 
- <span data-ttu-id="a3036-145">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="a3036-145">Basic</span></span>

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

### <span data-ttu-id="a3036-146">-Intervallum</span><span class="sxs-lookup"><span data-stu-id="a3036-146">-Interval</span></span>
<span data-ttu-id="a3036-147">A feladat ismétlődésének intervallumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a3036-147">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="a3036-148">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="a3036-148">-JobCollectionName</span></span>
<span data-ttu-id="a3036-149">Annak a feladatnak a neve, amelyhez a projekt tartozik.</span><span class="sxs-lookup"><span data-stu-id="a3036-149">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="a3036-150">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="a3036-150">-JobName</span></span>
<span data-ttu-id="a3036-151">Annak a feladatnak a nevét adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="a3036-151">Specifies the name of the job that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="a3036-152">-JobState</span><span class="sxs-lookup"><span data-stu-id="a3036-152">-JobState</span></span>
<span data-ttu-id="a3036-153">A feladat állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a3036-153">Specifies the state of the job.</span></span>
<span data-ttu-id="a3036-154">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="a3036-154">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a3036-155">Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="a3036-155">Enabled</span></span> 
- <span data-ttu-id="a3036-156">Tiltva</span><span class="sxs-lookup"><span data-stu-id="a3036-156">Disabled</span></span>

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

### <span data-ttu-id="a3036-157">-Módszer</span><span class="sxs-lookup"><span data-stu-id="a3036-157">-Method</span></span>
<span data-ttu-id="a3036-158">A tevékenységhez tartozó Művelettípus metódusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a3036-158">Specifies the method for the action types for this job.</span></span>
<span data-ttu-id="a3036-159">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="a3036-159">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a3036-160">BESZERZÉSE</span><span class="sxs-lookup"><span data-stu-id="a3036-160">GET</span></span> 
- <span data-ttu-id="a3036-161">HELYEZNI</span><span class="sxs-lookup"><span data-stu-id="a3036-161">PUT</span></span> 
- <span data-ttu-id="a3036-162">POST</span><span class="sxs-lookup"><span data-stu-id="a3036-162">POST</span></span> 
- <span data-ttu-id="a3036-163">TÖRLÉSE</span><span class="sxs-lookup"><span data-stu-id="a3036-163">DELETE</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GET, PUT, POST, DELETE

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3036-164">-RequestBody</span><span class="sxs-lookup"><span data-stu-id="a3036-164">-RequestBody</span></span>
<span data-ttu-id="a3036-165">A feladatok elvégzéséhez és KÖZZÉTÉTELéhez szükséges törzs értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a3036-165">Specifies the value of the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="a3036-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3036-166">-ResourceGroupName</span></span>
<span data-ttu-id="a3036-167">Azt az erőforráscsoport-csoportot adja meg, amelyhez a projekt tartozik.</span><span class="sxs-lookup"><span data-stu-id="a3036-167">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="a3036-168">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="a3036-168">-StartTime</span></span>
<span data-ttu-id="a3036-169">A projekthez tartozó **datetime** -objektum kezdési időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a3036-169">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="a3036-170">-URI</span><span class="sxs-lookup"><span data-stu-id="a3036-170">-Uri</span></span>
<span data-ttu-id="a3036-171">A projektfeladat URI-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a3036-171">Specifies a URI for the job action.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3036-172">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a3036-172">-Confirm</span></span>
<span data-ttu-id="a3036-173">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a3036-173">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3036-174">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3036-174">-WhatIf</span></span>
<span data-ttu-id="a3036-175">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a3036-175">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3036-176">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a3036-176">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3036-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3036-177">CommonParameters</span></span>
<span data-ttu-id="a3036-178">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a3036-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3036-179">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3036-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3036-180">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a3036-180">INPUTS</span></span>

### <span data-ttu-id="a3036-181">System. String</span><span class="sxs-lookup"><span data-stu-id="a3036-181">System.String</span></span>

### <span data-ttu-id="a3036-182">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a3036-182">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a3036-183">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a3036-183">OUTPUTS</span></span>

### <span data-ttu-id="a3036-184">Microsoft. Azure. Command. Scheduler. models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="a3036-184">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="a3036-185">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a3036-185">NOTES</span></span>

## <span data-ttu-id="a3036-186">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a3036-186">RELATED LINKS</span></span>

[<span data-ttu-id="a3036-187">Új – AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="a3036-187">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="a3036-188">Új – AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="a3036-188">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="a3036-189">Új – AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="a3036-189">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="a3036-190">Új – AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="a3036-190">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="a3036-191">Új – AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="a3036-191">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="a3036-192">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="a3036-192">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="a3036-193">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="a3036-193">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="a3036-194">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="a3036-194">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="a3036-195">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="a3036-195">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


