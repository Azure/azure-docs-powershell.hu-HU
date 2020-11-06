---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: 5563B6E8-805B-463B-AF78-4F5750F5CDEA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerStorageQueueJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerStorageQueueJob.md
ms.openlocfilehash: ba8d917c33f2ab7ac6c82db303df08c01c648bf2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501616"
---
# <span data-ttu-id="281a7-101">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="281a7-101">New-AzureRmSchedulerStorageQueueJob</span></span>

## <span data-ttu-id="281a7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="281a7-102">SYNOPSIS</span></span>
<span data-ttu-id="281a7-103">Létrehoz egy tárolási várólista-feladatot.</span><span class="sxs-lookup"><span data-stu-id="281a7-103">Creates a storage queue job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="281a7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="281a7-104">SYNTAX</span></span>

```
New-AzureRmSchedulerStorageQueueJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 -StorageQueueAccount <String> -StorageQueueName <String> -StorageSASToken <String>
 -StorageQueueMessage <String> [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="281a7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="281a7-105">DESCRIPTION</span></span>
<span data-ttu-id="281a7-106">A **New-AzureRmSchedulerStorageQueueJob** parancsmag létrehoz egy tárterület-várólistás feladatot az Azure schedulerben.</span><span class="sxs-lookup"><span data-stu-id="281a7-106">The **New-AzureRmSchedulerStorageQueueJob** cmdlet creates a storage queue job in Azure Scheduler.</span></span>

<span data-ttu-id="281a7-107">Ez a parancsmag a *ErrorActionType* paraméter alapján támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="281a7-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="281a7-108">A dinamikus paraméterek elérhetővé válnak a többi paraméter-érték alapján.</span><span class="sxs-lookup"><span data-stu-id="281a7-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="281a7-109">Ha meg szeretné ismerni a dinamikus paraméterek nevét a többi paraméter megadása után, írjon be egy kötőjelet (-), majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="281a7-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="281a7-110">Ha kihagyja a kötelező paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="281a7-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="281a7-111">Példák</span><span class="sxs-lookup"><span data-stu-id="281a7-111">EXAMPLES</span></span>

## <span data-ttu-id="281a7-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="281a7-112">PARAMETERS</span></span>

### <span data-ttu-id="281a7-113">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="281a7-113">-EndTime</span></span>
<span data-ttu-id="281a7-114">A projekthez tartozó **datetime** -objektum záró időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="281a7-114">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="281a7-115">Ha **datetime** típusú objektumot szeretne beolvasni, használja az Get-Date parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="281a7-115">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="281a7-116">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="281a7-116">-ErrorActionType</span></span>
<span data-ttu-id="281a7-117">A feladat hibaérték-beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="281a7-117">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="281a7-118">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="281a7-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="281a7-119">Http</span><span class="sxs-lookup"><span data-stu-id="281a7-119">Http</span></span> 
- <span data-ttu-id="281a7-120">Https</span><span class="sxs-lookup"><span data-stu-id="281a7-120">Https</span></span> 
- <span data-ttu-id="281a7-121">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="281a7-121">StorageQueue</span></span> 
- <span data-ttu-id="281a7-122">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="281a7-122">ServiceBusQueue</span></span> 
- <span data-ttu-id="281a7-123">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="281a7-123">ServiceBusTopic</span></span>

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

### <span data-ttu-id="281a7-124">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="281a7-124">-ExecutionCount</span></span>
<span data-ttu-id="281a7-125">Itt adhatja meg, hogy hányszor fusson a feladat.</span><span class="sxs-lookup"><span data-stu-id="281a7-125">Specifies how many times the job runs.</span></span>
<span data-ttu-id="281a7-126">Alapértelmezés szerint a feladat határozatlan ideig ismétlődik.</span><span class="sxs-lookup"><span data-stu-id="281a7-126">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="281a7-127">-Gyakoriság</span><span class="sxs-lookup"><span data-stu-id="281a7-127">-Frequency</span></span>
<span data-ttu-id="281a7-128">A feladat gyakoriságát adja meg.</span><span class="sxs-lookup"><span data-stu-id="281a7-128">Specifies a frequency for the job.</span></span>
<span data-ttu-id="281a7-129">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="281a7-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="281a7-130">Perces</span><span class="sxs-lookup"><span data-stu-id="281a7-130">Minute</span></span> 
- <span data-ttu-id="281a7-131">Óra</span><span class="sxs-lookup"><span data-stu-id="281a7-131">Hour</span></span> 
- <span data-ttu-id="281a7-132">Nap</span><span class="sxs-lookup"><span data-stu-id="281a7-132">Day</span></span> 
- <span data-ttu-id="281a7-133">Héten</span><span class="sxs-lookup"><span data-stu-id="281a7-133">Week</span></span> 
- <span data-ttu-id="281a7-134">Hónap</span><span class="sxs-lookup"><span data-stu-id="281a7-134">Month</span></span>

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

### <span data-ttu-id="281a7-135">-Intervallum</span><span class="sxs-lookup"><span data-stu-id="281a7-135">-Interval</span></span>
<span data-ttu-id="281a7-136">A feladat ismétlődésének intervallumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="281a7-136">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="281a7-137">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="281a7-137">-JobCollectionName</span></span>
<span data-ttu-id="281a7-138">Annak a feladatnak a neve, amelyhez a projekt tartozik.</span><span class="sxs-lookup"><span data-stu-id="281a7-138">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="281a7-139">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="281a7-139">-JobName</span></span>
<span data-ttu-id="281a7-140">A feladat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="281a7-140">Specifies a name for the job.</span></span>

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

### <span data-ttu-id="281a7-141">-JobState</span><span class="sxs-lookup"><span data-stu-id="281a7-141">-JobState</span></span>
<span data-ttu-id="281a7-142">A feladat állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="281a7-142">Specifies the state of the job.</span></span>
<span data-ttu-id="281a7-143">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="281a7-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="281a7-144">Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="281a7-144">Enabled</span></span> 
- <span data-ttu-id="281a7-145">Tiltva</span><span class="sxs-lookup"><span data-stu-id="281a7-145">Disabled</span></span>

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

### <span data-ttu-id="281a7-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="281a7-146">-ResourceGroupName</span></span>
<span data-ttu-id="281a7-147">Azt az erőforráscsoport-csoportot adja meg, amelyhez a projekt tartozik.</span><span class="sxs-lookup"><span data-stu-id="281a7-147">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="281a7-148">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="281a7-148">-StartTime</span></span>
<span data-ttu-id="281a7-149">A projekthez tartozó **datetime** -objektum kezdési időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="281a7-149">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="281a7-150">-StorageQueueAccount</span><span class="sxs-lookup"><span data-stu-id="281a7-150">-StorageQueueAccount</span></span>
<span data-ttu-id="281a7-151">A tárolási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="281a7-151">Specifies a storage account name.</span></span>

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

### <span data-ttu-id="281a7-152">-StorageQueueMessage</span><span class="sxs-lookup"><span data-stu-id="281a7-152">-StorageQueueMessage</span></span>
<span data-ttu-id="281a7-153">A tárolási feladat várólistájának üzenetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="281a7-153">Specifies a queue message for the storage job.</span></span>

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

### <span data-ttu-id="281a7-154">-StorageQueueName</span><span class="sxs-lookup"><span data-stu-id="281a7-154">-StorageQueueName</span></span>
<span data-ttu-id="281a7-155">A tárolási várólista nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="281a7-155">Specifies a storage queue name.</span></span>

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

### <span data-ttu-id="281a7-156">-StorageSASToken</span><span class="sxs-lookup"><span data-stu-id="281a7-156">-StorageSASToken</span></span>
<span data-ttu-id="281a7-157">A tárterület-várólistához tartozó megosztott hozzáférés-aláírási tokent adja meg.</span><span class="sxs-lookup"><span data-stu-id="281a7-157">Specifies a shared access signature token for a storage queue.</span></span>

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

### <span data-ttu-id="281a7-158">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="281a7-158">-Confirm</span></span>
<span data-ttu-id="281a7-159">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="281a7-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="281a7-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="281a7-160">-WhatIf</span></span>
<span data-ttu-id="281a7-161">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="281a7-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="281a7-162">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="281a7-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="281a7-163">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="281a7-163">-DefaultProfile</span></span>
<span data-ttu-id="281a7-164">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="281a7-164">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="281a7-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="281a7-165">CommonParameters</span></span>
<span data-ttu-id="281a7-166">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="281a7-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="281a7-167">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="281a7-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="281a7-168">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="281a7-168">INPUTS</span></span>

## <span data-ttu-id="281a7-169">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="281a7-169">OUTPUTS</span></span>

### <span data-ttu-id="281a7-170">Microsoft. Azure. Command. Scheduler. models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="281a7-170">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="281a7-171">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="281a7-171">NOTES</span></span>

## <span data-ttu-id="281a7-172">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="281a7-172">RELATED LINKS</span></span>

[<span data-ttu-id="281a7-173">Új – AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="281a7-173">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="281a7-174">Új – AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="281a7-174">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="281a7-175">Új – AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="281a7-175">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="281a7-176">Új – AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="281a7-176">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="281a7-177">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="281a7-177">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="281a7-178">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="281a7-178">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="281a7-179">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="281a7-179">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="281a7-180">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="281a7-180">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="281a7-181">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="281a7-181">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


