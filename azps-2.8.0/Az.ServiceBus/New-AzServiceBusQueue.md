---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusQueue.md
ms.openlocfilehash: 87679299d17cf3e92cf6a797050c14aa65055db2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838808"
---
# <span data-ttu-id="27b11-101">New-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="27b11-101">New-AzServiceBusQueue</span></span>

## <span data-ttu-id="27b11-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="27b11-102">SYNOPSIS</span></span>
<span data-ttu-id="27b11-103">Létrehoz egy szolgáltatás busz-várólistáját a megadott Service Bus névtérben.</span><span class="sxs-lookup"><span data-stu-id="27b11-103">Creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="27b11-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="27b11-104">SYNTAX</span></span>

```
New-AzServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-EnablePartitioning <Boolean>] [-LockDuration <String>] [-AutoDeleteOnIdle <String>]
 [-DefaultMessageTimeToLive <String>] [-DuplicateDetectionHistoryTimeWindow <String>]
 [-DeadLetteringOnMessageExpiration <Boolean>] [-EnableBatchedOperations] [-EnableExpress <Boolean>]
 [-MaxDeliveryCount <Int32>] [-MaxSizeInMegabytes <Int64>] [-MessageCount <Int64>]
 [-RequiresDuplicateDetection <Boolean>] [-RequiresSession <Boolean>] [-SizeInBytes <Int64>]
 [-ForwardTo <String>] [-ForwardDeadLetteredMessagesTo <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27b11-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="27b11-105">DESCRIPTION</span></span>
<span data-ttu-id="27b11-106">A **New-AzServiceBusQueue** parancsmag létrehoz egy szolgáltatás busz-várólistáját a megadott Service Bus névtérben.</span><span class="sxs-lookup"><span data-stu-id="27b11-106">The **New-AzServiceBusQueue** cmdlet creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="27b11-107">Példák</span><span class="sxs-lookup"><span data-stu-id="27b11-107">EXAMPLES</span></span>

### <span data-ttu-id="27b11-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="27b11-108">Example 1</span></span>
```
PS C:\> New-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1 -EnablePartitioning $True

Id                                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroupName}/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/SB-Queue_example1
Name                                : SB-Queue_example1
LockDuration                        : PT1M
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : P10675199DT2H48M5.4775807S
CreatedAt                           : 10/11/2018 12:37:11 AM
DefaultMessageTimeToLive            : P10675199DT2H48M5.4775807S
DuplicateDetectionHistoryTimeWindow : PT10M
DeadLetteringOnMessageExpiration    : False
EnableExpress                       : False
EnablePartitioning                  : False
MaxDeliveryCount                    : 10
MaxSizeInMegabytes                  : 81920
MessageCount                        : 0
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
RequiresDuplicateDetection          : False
RequiresSession                     : False
SizeInBytes                         : 0
Status                              : Active
UpdatedAt                           : 10/11/2018 12:37:12 AM
ForwardTo                           :
ForwardDeadLetteredMessagesTo       :
EnableBatchedOperations             : False
```

<span data-ttu-id="27b11-109">Új szervizsorok-várólistát hoz létre `SB-Queue_example1` a megadott szolgáltatási busz névtérben `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="27b11-109">Creates a new Service Bus queue `SB-Queue_example1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="27b11-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="27b11-110">PARAMETERS</span></span>

### <span data-ttu-id="27b11-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="27b11-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="27b11-112">A [időszak](https://msdn.microsoft.com/library/system.timespan.aspx) üresjárati intervallumát adja meg, amely után a rendszer automatikusan törli a várólistát.</span><span class="sxs-lookup"><span data-stu-id="27b11-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the queue is automatically deleted.</span></span> <span data-ttu-id="27b11-113">A minimális időtartam 5 perc.</span><span class="sxs-lookup"><span data-stu-id="27b11-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="27b11-114">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="27b11-114">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="27b11-115">Az üzenet lejárata halott betűkkel</span><span class="sxs-lookup"><span data-stu-id="27b11-115">Dead Lettering On Message Expiration</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27b11-116">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="27b11-116">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="27b11-117">Időszak az élő értékre.</span><span class="sxs-lookup"><span data-stu-id="27b11-117">Timespan to live value.</span></span>
<span data-ttu-id="27b11-118">Ez az az időtartam, amely után az üzenet lejár, attól kezdve, hogy mikor küldi el az üzenetet a szolgáltatás Buszjának.</span><span class="sxs-lookup"><span data-stu-id="27b11-118">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>
<span data-ttu-id="27b11-119">Ez az alapértelmezett érték akkor használható, ha a TimeToLive nem egy üzeneten van beállítva.</span><span class="sxs-lookup"><span data-stu-id="27b11-119">This is the default value used when TimeToLive is not set on a message itself.</span></span>
<span data-ttu-id="27b11-120">Standard = időszak. Max és Basic = 14 nap</span><span class="sxs-lookup"><span data-stu-id="27b11-120">For Standard = Timespan.Max and Basic = 14 days</span></span>

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

### <span data-ttu-id="27b11-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27b11-121">-DefaultProfile</span></span>
<span data-ttu-id="27b11-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="27b11-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27b11-123">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="27b11-123">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="27b11-124">A duplikáltelem-észlelési előzmények időablaka, egy [időszak](https://msdn.microsoft.com/library/system.timespan.aspx) érték, amely meghatározza a duplikáltelem-észlelési előzmények időtartamát.</span><span class="sxs-lookup"><span data-stu-id="27b11-124">Specifies the duplicate detection history time window, a [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) value that defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="27b11-125">Az alapértelmezett érték 10 perc.</span><span class="sxs-lookup"><span data-stu-id="27b11-125">The default value is 10 minutes.</span></span>

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

### <span data-ttu-id="27b11-126">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="27b11-126">-EnableBatchedOperations</span></span>
<span data-ttu-id="27b11-127">Kötegelt műveletek engedélyezése – érték, amely azt jelzi, hogy engedélyezve van-e a kiszolgálóoldali kötegelt műveletek</span><span class="sxs-lookup"><span data-stu-id="27b11-127">Enable Batched Operations - value that indicates whether server-side batched operations are enabled</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27b11-128">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="27b11-128">-EnableExpress</span></span>
<span data-ttu-id="27b11-129">EnableExpress – az a érték, amely azt jelzi, hogy engedélyezve vannak-e az Express-entitások.</span><span class="sxs-lookup"><span data-stu-id="27b11-129">EnableExpress - a value that indicates whether Express Entities are enabled.</span></span>
<span data-ttu-id="27b11-130">Az Express-várólisták átmenetileg tárolják az üzenetet a memóriában, mielőtt állandó tárterületre írom azt.</span><span class="sxs-lookup"><span data-stu-id="27b11-130">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27b11-131">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="27b11-131">-EnablePartitioning</span></span>
<span data-ttu-id="27b11-132">EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="27b11-132">EnablePartitioning</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27b11-133">-ForwardDeadLetteredMessagesTo</span><span class="sxs-lookup"><span data-stu-id="27b11-133">-ForwardDeadLetteredMessagesTo</span></span>
<span data-ttu-id="27b11-134">A várólista vagy a téma neve a halotti üzenet továbbításához</span><span class="sxs-lookup"><span data-stu-id="27b11-134">Queue/Topic name to forward the Dead Letter message</span></span>

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

### <span data-ttu-id="27b11-135">-ForwardTo</span><span class="sxs-lookup"><span data-stu-id="27b11-135">-ForwardTo</span></span>
<span data-ttu-id="27b11-136">A várólista vagy a téma neve az üzenetek továbbításához</span><span class="sxs-lookup"><span data-stu-id="27b11-136">Queue/Topic name to forward the messages</span></span>

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

### <span data-ttu-id="27b11-137">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="27b11-137">-LockDuration</span></span>
<span data-ttu-id="27b11-138">Zárolás időtartama</span><span class="sxs-lookup"><span data-stu-id="27b11-138">Lock Duration</span></span>

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

### <span data-ttu-id="27b11-139">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="27b11-139">-MaxDeliveryCount</span></span>
<span data-ttu-id="27b11-140">MaxDeliveryCount – a kézbesítés maximális száma.</span><span class="sxs-lookup"><span data-stu-id="27b11-140">MaxDeliveryCount - the maximum delivery count.</span></span>
<span data-ttu-id="27b11-141">Ezt követően az üzenet automatikusan deadlettered a kézbesítések száma után.</span><span class="sxs-lookup"><span data-stu-id="27b11-141">A message is automatically deadlettered after this number of deliveries.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27b11-142">-MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="27b11-142">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="27b11-143">MaxSizeInMegabytes – a várólista maximális mérete megabájtban, ami a várólistához lefoglalt memória mérete. Az alapértelmezett érték a 1024.</span><span class="sxs-lookup"><span data-stu-id="27b11-143">MaxSizeInMegabytes - the maximum size of the queue in megabytes, which is the size of memory allocated for the queue.Default is 1024.</span></span> <span data-ttu-id="27b11-144">A Max standard SKU esetében a 5120 és a prémium SKU a 81920, a megengedett értékek: 1024, 2048, 3072, 4096, 5120, 10240, 20480, 40960, 81920</span><span class="sxs-lookup"><span data-stu-id="27b11-144">Max for Standard SKU is 5120 and for Premium SKU is 81920, Allowed values : 1024, 2048, 3072, 4096, 5120, 10240, 20480, 40960, 81920</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27b11-145">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="27b11-145">-MessageCount</span></span>
<span data-ttu-id="27b11-146">MessageCount – a várólistán lévő üzenetek száma</span><span class="sxs-lookup"><span data-stu-id="27b11-146">MessageCount - the number of messages in the queue</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27b11-147">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="27b11-147">-Name</span></span>
<span data-ttu-id="27b11-148">Várólista neve</span><span class="sxs-lookup"><span data-stu-id="27b11-148">Queue Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27b11-149">-Namespace</span><span class="sxs-lookup"><span data-stu-id="27b11-149">-Namespace</span></span>
<span data-ttu-id="27b11-150">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="27b11-150">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27b11-151">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="27b11-151">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="27b11-152">RequiresDuplicateDetection – egy érték, amely azt jelzi, hogy a várólista támogatja-e a munkamenet fogalmát</span><span class="sxs-lookup"><span data-stu-id="27b11-152">RequiresDuplicateDetection - a value that indicates whether the queue supports the concept of session</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27b11-153">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="27b11-153">-RequiresSession</span></span>
<span data-ttu-id="27b11-154">RequiresSession – az az érték, amely azt jelzi, hogy a várólista munkameneteket használ</span><span class="sxs-lookup"><span data-stu-id="27b11-154">RequiresSession - the value indicating if this queue uses sessions</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27b11-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27b11-155">-ResourceGroupName</span></span>
<span data-ttu-id="27b11-156">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="27b11-156">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27b11-157">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="27b11-157">-SizeInBytes</span></span>
<span data-ttu-id="27b11-158">SizeInBytes – a várólista mérete bájtban kifejezve</span><span class="sxs-lookup"><span data-stu-id="27b11-158">SizeInBytes - the size of the queue in bytes</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27b11-159">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="27b11-159">-Confirm</span></span>
<span data-ttu-id="27b11-160">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="27b11-160">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27b11-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27b11-161">-WhatIf</span></span>
<span data-ttu-id="27b11-162">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="27b11-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27b11-163">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="27b11-163">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27b11-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27b11-164">CommonParameters</span></span>
<span data-ttu-id="27b11-165">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="27b11-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27b11-166">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27b11-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27b11-167">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="27b11-167">INPUTS</span></span>

### <span data-ttu-id="27b11-168">System. String</span><span class="sxs-lookup"><span data-stu-id="27b11-168">System.String</span></span>

### <span data-ttu-id="27b11-169">System. null ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="27b11-169">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="27b11-170">System. null ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="27b11-170">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="27b11-171">System. null ' 1 [[System. Int64, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="27b11-171">System.Nullable\`1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="27b11-172">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="27b11-172">OUTPUTS</span></span>

### <span data-ttu-id="27b11-173">Microsoft. Azure. Command. ServiceBus. models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="27b11-173">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="27b11-174">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="27b11-174">NOTES</span></span>

## <span data-ttu-id="27b11-175">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="27b11-175">RELATED LINKS</span></span>
