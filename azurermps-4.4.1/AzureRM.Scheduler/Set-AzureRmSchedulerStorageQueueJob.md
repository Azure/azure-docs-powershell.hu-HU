---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: 75AF57EE-C7C3-42DE-AFD7-4B5150EEDBB6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerStorageQueueJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerStorageQueueJob.md
ms.openlocfilehash: c752b4fd96ec001467e051fc01be24f592241182
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680233"
---
# <span data-ttu-id="d6743-101">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="d6743-101">Set-AzureRmSchedulerStorageQueueJob</span></span>

## <span data-ttu-id="d6743-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d6743-102">SYNOPSIS</span></span>
<span data-ttu-id="d6743-103">Módosította a tárolási várólista feladatát.</span><span class="sxs-lookup"><span data-stu-id="d6743-103">Modifies a storage queue job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6743-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d6743-104">SYNTAX</span></span>

```
Set-AzureRmSchedulerStorageQueueJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 [-StorageQueueAccount <String>] [-StorageQueueName <String>] [-StorageSASToken <String>]
 [-StorageQueueMessage <String>] [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6743-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d6743-105">DESCRIPTION</span></span>
<span data-ttu-id="d6743-106">A **set-AzureRmSchedulerStorageQueueJob** parancsmag az Azure Scheduler-ban módosítja a tárolási várólista feladatát.</span><span class="sxs-lookup"><span data-stu-id="d6743-106">The **Set-AzureRmSchedulerStorageQueueJob** cmdlet modifies a storage queue job in Azure Scheduler.</span></span>

<span data-ttu-id="d6743-107">Ez a parancsmag a *ErrorActionType* paraméter alapján támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="d6743-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="d6743-108">A dinamikus paraméterek elérhetővé válnak a többi paraméter-érték alapján.</span><span class="sxs-lookup"><span data-stu-id="d6743-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="d6743-109">Ha meg szeretné ismerni a dinamikus paraméterek nevét a többi paraméter megadása után, írjon be egy kötőjelet (-), majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="d6743-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="d6743-110">Ha kihagyja a kötelező paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="d6743-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="d6743-111">Példák</span><span class="sxs-lookup"><span data-stu-id="d6743-111">EXAMPLES</span></span>

## <span data-ttu-id="d6743-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d6743-112">PARAMETERS</span></span>

### <span data-ttu-id="d6743-113">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="d6743-113">-EndTime</span></span>
<span data-ttu-id="d6743-114">A projekthez tartozó **datetime** -objektum záró időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d6743-114">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="d6743-115">Ha **datetime** típusú objektumot szeretne beolvasni, használja az Get-Date parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="d6743-115">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="d6743-116">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="d6743-116">-ErrorActionType</span></span>
<span data-ttu-id="d6743-117">A feladat hibaérték-beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="d6743-117">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="d6743-118">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="d6743-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d6743-119">Http</span><span class="sxs-lookup"><span data-stu-id="d6743-119">Http</span></span> 
- <span data-ttu-id="d6743-120">Https</span><span class="sxs-lookup"><span data-stu-id="d6743-120">Https</span></span> 
- <span data-ttu-id="d6743-121">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="d6743-121">StorageQueue</span></span> 
- <span data-ttu-id="d6743-122">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="d6743-122">ServiceBusQueue</span></span> 
- <span data-ttu-id="d6743-123">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="d6743-123">ServiceBusTopic</span></span>

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

### <span data-ttu-id="d6743-124">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="d6743-124">-ExecutionCount</span></span>
<span data-ttu-id="d6743-125">Itt adhatja meg, hogy hányszor fusson a feladat.</span><span class="sxs-lookup"><span data-stu-id="d6743-125">Specifies how many times the job runs.</span></span>
<span data-ttu-id="d6743-126">Alapértelmezés szerint a feladat határozatlan ideig ismétlődik.</span><span class="sxs-lookup"><span data-stu-id="d6743-126">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="d6743-127">-Gyakoriság</span><span class="sxs-lookup"><span data-stu-id="d6743-127">-Frequency</span></span>
<span data-ttu-id="d6743-128">A feladat gyakoriságát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d6743-128">Specifies a frequency for the job.</span></span>
<span data-ttu-id="d6743-129">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="d6743-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d6743-130">Perces</span><span class="sxs-lookup"><span data-stu-id="d6743-130">Minute</span></span> 
- <span data-ttu-id="d6743-131">Óra</span><span class="sxs-lookup"><span data-stu-id="d6743-131">Hour</span></span> 
- <span data-ttu-id="d6743-132">Nap</span><span class="sxs-lookup"><span data-stu-id="d6743-132">Day</span></span> 
- <span data-ttu-id="d6743-133">Héten</span><span class="sxs-lookup"><span data-stu-id="d6743-133">Week</span></span> 
- <span data-ttu-id="d6743-134">Hónap</span><span class="sxs-lookup"><span data-stu-id="d6743-134">Month</span></span>

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

### <span data-ttu-id="d6743-135">-Intervallum</span><span class="sxs-lookup"><span data-stu-id="d6743-135">-Interval</span></span>
<span data-ttu-id="d6743-136">A feladat ismétlődésének intervallumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d6743-136">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="d6743-137">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="d6743-137">-JobCollectionName</span></span>
<span data-ttu-id="d6743-138">Annak a feladatnak a neve, amelyhez a projekt tartozik.</span><span class="sxs-lookup"><span data-stu-id="d6743-138">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="d6743-139">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="d6743-139">-JobName</span></span>
<span data-ttu-id="d6743-140">Annak a feladatnak a nevét adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="d6743-140">Specifies the name of the job that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="d6743-141">-JobState</span><span class="sxs-lookup"><span data-stu-id="d6743-141">-JobState</span></span>
<span data-ttu-id="d6743-142">A feladat állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d6743-142">Specifies the state of the job.</span></span>
<span data-ttu-id="d6743-143">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="d6743-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d6743-144">Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="d6743-144">Enabled</span></span> 
- <span data-ttu-id="d6743-145">Tiltva</span><span class="sxs-lookup"><span data-stu-id="d6743-145">Disabled</span></span>

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

### <span data-ttu-id="d6743-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6743-146">-ResourceGroupName</span></span>
<span data-ttu-id="d6743-147">Azt az erőforráscsoport-csoportot adja meg, amelyhez a projekt tartozik.</span><span class="sxs-lookup"><span data-stu-id="d6743-147">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="d6743-148">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="d6743-148">-StartTime</span></span>
<span data-ttu-id="d6743-149">A projekthez tartozó **datetime** -objektum kezdési időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d6743-149">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="d6743-150">-StorageQueueAccount</span><span class="sxs-lookup"><span data-stu-id="d6743-150">-StorageQueueAccount</span></span>
<span data-ttu-id="d6743-151">A tárolási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d6743-151">Specifies a storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6743-152">-StorageQueueMessage</span><span class="sxs-lookup"><span data-stu-id="d6743-152">-StorageQueueMessage</span></span>
<span data-ttu-id="d6743-153">A tárolási feladatok várólistájának üzenetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d6743-153">Specifies a queue message for storage job.</span></span>

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

### <span data-ttu-id="d6743-154">-StorageQueueName</span><span class="sxs-lookup"><span data-stu-id="d6743-154">-StorageQueueName</span></span>
<span data-ttu-id="d6743-155">A tárolási várólista nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d6743-155">Specifies a storage queue name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6743-156">-StorageSASToken</span><span class="sxs-lookup"><span data-stu-id="d6743-156">-StorageSASToken</span></span>
<span data-ttu-id="d6743-157">A tárterület-várólistához tartozó megosztott hozzáférés-aláírási tokent adja meg.</span><span class="sxs-lookup"><span data-stu-id="d6743-157">Specifies a shared access signature token for a storage queue.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6743-158">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d6743-158">-Confirm</span></span>
<span data-ttu-id="d6743-159">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d6743-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6743-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6743-160">-WhatIf</span></span>
<span data-ttu-id="d6743-161">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d6743-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6743-162">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d6743-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6743-163">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6743-163">-DefaultProfile</span></span>
<span data-ttu-id="d6743-164">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d6743-164">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6743-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6743-165">CommonParameters</span></span>
<span data-ttu-id="d6743-166">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d6743-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6743-167">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6743-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6743-168">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6743-168">INPUTS</span></span>

## <span data-ttu-id="d6743-169">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6743-169">OUTPUTS</span></span>

### <span data-ttu-id="d6743-170">Microsoft. Azure. Command. Scheduler. models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="d6743-170">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="d6743-171">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d6743-171">NOTES</span></span>

## <span data-ttu-id="d6743-172">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d6743-172">RELATED LINKS</span></span>

[<span data-ttu-id="d6743-173">Új – AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="d6743-173">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="d6743-174">Új – AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d6743-174">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="d6743-175">Új – AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="d6743-175">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="d6743-176">Új – AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="d6743-176">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="d6743-177">Új – AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="d6743-177">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="d6743-178">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="d6743-178">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="d6743-179">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d6743-179">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="d6743-180">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="d6743-180">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="d6743-181">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="d6743-181">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)


