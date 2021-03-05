---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/new-azservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusQueue.md
ms.openlocfilehash: 1d197683e1459173d96958199ad08b437d1d9e04
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999781"
---
# <span data-ttu-id="84ef6-101">New-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="84ef6-101">New-AzServiceBusQueue</span></span>

## <span data-ttu-id="84ef6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84ef6-102">SYNOPSIS</span></span>
<span data-ttu-id="84ef6-103">Szolgáltatásbusz-várólistát hoz létre a szolgáltatásbusz névterében.</span><span class="sxs-lookup"><span data-stu-id="84ef6-103">Creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="84ef6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="84ef6-104">SYNTAX</span></span>

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

## <span data-ttu-id="84ef6-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="84ef6-105">DESCRIPTION</span></span>
<span data-ttu-id="84ef6-106">A **New-AzServiceBusQueue** parancsmag szolgáltatásibusz-várólistát hoz létre a szolgáltatásbusz megadott névterében.</span><span class="sxs-lookup"><span data-stu-id="84ef6-106">The **New-AzServiceBusQueue** cmdlet creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="84ef6-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="84ef6-107">EXAMPLES</span></span>

### <span data-ttu-id="84ef6-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="84ef6-108">Example 1</span></span>
```powershell
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

<span data-ttu-id="84ef6-109">Létrehoz egy új Service Bus várólistát a `SB-Queue_example1` megadott Service Bus névterében. `SB-Example1`</span><span class="sxs-lookup"><span data-stu-id="84ef6-109">Creates a new Service Bus queue `SB-Queue_example1` in the specified Service Bus namespace `SB-Example1`.</span></span>

### <span data-ttu-id="84ef6-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="84ef6-110">Example 2</span></span>

<span data-ttu-id="84ef6-111">Szolgáltatásbusz-várólistát hoz létre a szolgáltatásbusz névterében.</span><span class="sxs-lookup"><span data-stu-id="84ef6-111">Creates a Service Bus queue in the specified Service Bus namespace.</span></span> <span data-ttu-id="84ef6-112">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="84ef6-112">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzServiceBusQueue -EnablePartitioning $true -MaxSizeInMegabytes <Int64> -Name SB-Queue_example1 -Namespace SB-Example1 -ResourceGroupName Default-ServiceBus-WestUS
```

## <span data-ttu-id="84ef6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="84ef6-113">PARAMETERS</span></span>

### <span data-ttu-id="84ef6-114">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="84ef6-114">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="84ef6-115">Megadja az [IdőTartomány](https://msdn.microsoft.com/library/system.timespan.aspx) inaktív időszakát, amely után a várólistát automatikusan törli a rendszer.</span><span class="sxs-lookup"><span data-stu-id="84ef6-115">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the queue is automatically deleted.</span></span> <span data-ttu-id="84ef6-116">A minimális időtartam 5 perc.</span><span class="sxs-lookup"><span data-stu-id="84ef6-116">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="84ef6-117">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="84ef6-117">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="84ef6-118">Dead Lettering On Message Expiration</span><span class="sxs-lookup"><span data-stu-id="84ef6-118">Dead Lettering On Message Expiration</span></span>

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

### <span data-ttu-id="84ef6-119">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="84ef6-119">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="84ef6-120">Időkorrekta az élő értékhez</span><span class="sxs-lookup"><span data-stu-id="84ef6-120">Timespan to live value.</span></span>
<span data-ttu-id="84ef6-121">Ez az az időtartam, amely után az üzenet lejár, attól kezdve, hogy az üzenetet elküldik a szolgáltatásbusznak.</span><span class="sxs-lookup"><span data-stu-id="84ef6-121">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>
<span data-ttu-id="84ef6-122">Ez az alapértelmezett érték, amikor a TimeToLive nincs beállítva az üzeneten.</span><span class="sxs-lookup"><span data-stu-id="84ef6-122">This is the default value used when TimeToLive is not set on a message itself.</span></span>
<span data-ttu-id="84ef6-123">Normál = Timespan.Max és Basic = 14 nap</span><span class="sxs-lookup"><span data-stu-id="84ef6-123">For Standard = Timespan.Max and Basic = 14 days</span></span>

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

### <span data-ttu-id="84ef6-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84ef6-124">-DefaultProfile</span></span>
<span data-ttu-id="84ef6-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="84ef6-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84ef6-126">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="84ef6-126">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="84ef6-127">A duplikált észlelési előzmények időkeretét [(TimeSpan)](https://msdn.microsoft.com/library/system.timespan.aspx) adja meg, amely a duplikált észlelési előzmények időtartamát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="84ef6-127">Specifies the duplicate detection history time window, a [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) value that defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="84ef6-128">Az alapértelmezett érték 10 perc.</span><span class="sxs-lookup"><span data-stu-id="84ef6-128">The default value is 10 minutes.</span></span>

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

### <span data-ttu-id="84ef6-129">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="84ef6-129">-EnableBatchedOperations</span></span>
<span data-ttu-id="84ef6-130">A batched Operations engedélyezése – érték, amely azt jelzi, hogy engedélyezettek-e a kiszolgálóoldali köteges műveletek</span><span class="sxs-lookup"><span data-stu-id="84ef6-130">Enable Batched Operations - value that indicates whether server-side batched operations are enabled</span></span>

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

### <span data-ttu-id="84ef6-131">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="84ef6-131">-EnableExpress</span></span>
<span data-ttu-id="84ef6-132">EnableExpress – egy érték, amely azt jelzi, hogy engedélyezve vannak-e az Express entitások.</span><span class="sxs-lookup"><span data-stu-id="84ef6-132">EnableExpress - a value that indicates whether Express Entities are enabled.</span></span>
<span data-ttu-id="84ef6-133">Az expressz várólisták ideiglenesen a memóriában várakoztatják az üzeneteket, mielőtt állandó tárhelyre írják azt.</span><span class="sxs-lookup"><span data-stu-id="84ef6-133">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

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

### <span data-ttu-id="84ef6-134">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="84ef6-134">-EnablePartitioning</span></span>
<span data-ttu-id="84ef6-135">EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="84ef6-135">EnablePartitioning</span></span>

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

### <span data-ttu-id="84ef6-136">-ForwardDeadLetteredMessagesTo</span><span class="sxs-lookup"><span data-stu-id="84ef6-136">-ForwardDeadLetteredMessagesTo</span></span>
<span data-ttu-id="84ef6-137">Queue/Topic name to forward the Dead Letter message</span><span class="sxs-lookup"><span data-stu-id="84ef6-137">Queue/Topic name to forward the Dead Letter message</span></span>

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

### <span data-ttu-id="84ef6-138">-ForwardTo</span><span class="sxs-lookup"><span data-stu-id="84ef6-138">-ForwardTo</span></span>
<span data-ttu-id="84ef6-139">Az üzenetek továbbítása várólistán vagy témakörben</span><span class="sxs-lookup"><span data-stu-id="84ef6-139">Queue/Topic name to forward the messages</span></span>

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

### <span data-ttu-id="84ef6-140">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="84ef6-140">-LockDuration</span></span>
<span data-ttu-id="84ef6-141">Zárolás időtartama</span><span class="sxs-lookup"><span data-stu-id="84ef6-141">Lock Duration</span></span>

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

### <span data-ttu-id="84ef6-142">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="84ef6-142">-MaxDeliveryCount</span></span>
<span data-ttu-id="84ef6-143">MaxDeliveryCount – a maximális kézbesítési szám.</span><span class="sxs-lookup"><span data-stu-id="84ef6-143">MaxDeliveryCount - the maximum delivery count.</span></span>
<span data-ttu-id="84ef6-144">Ennyi kézbesítés után az üzenetek automatikusan elhalnak.</span><span class="sxs-lookup"><span data-stu-id="84ef6-144">A message is automatically deadlettered after this number of deliveries.</span></span>

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

### <span data-ttu-id="84ef6-145">-MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="84ef6-145">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="84ef6-146">MaxSizeInMegabytes – a várólista maximális mérete megabájtban, amely a várólistához kiosztott memória mérete. Az alapértelmezett érték 1024.</span><span class="sxs-lookup"><span data-stu-id="84ef6-146">MaxSizeInMegabytes - the maximum size of the queue in megabytes, which is the size of memory allocated for the queue.Default is 1024.</span></span> <span data-ttu-id="84ef6-147">A Normál termékváltozat max. értéke 5120, a prémium termékváltozat értéke pedig 81920, engedélyezett értékek: 1024, 2048, 3072, 4096, 5120, 10240, 20480, 40960, 81920</span><span class="sxs-lookup"><span data-stu-id="84ef6-147">Max for Standard SKU is 5120 and for Premium SKU is 81920, Allowed values : 1024, 2048, 3072, 4096, 5120, 10240, 20480, 40960, 81920</span></span>

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

### <span data-ttu-id="84ef6-148">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="84ef6-148">-MessageCount</span></span>
<span data-ttu-id="84ef6-149">MessageCount – a várólistán lévő üzenetek száma</span><span class="sxs-lookup"><span data-stu-id="84ef6-149">MessageCount - the number of messages in the queue</span></span>

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

### <span data-ttu-id="84ef6-150">-Name</span><span class="sxs-lookup"><span data-stu-id="84ef6-150">-Name</span></span>
<span data-ttu-id="84ef6-151">Várólistán lévő név</span><span class="sxs-lookup"><span data-stu-id="84ef6-151">Queue Name</span></span>

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

### <span data-ttu-id="84ef6-152">-Namespace</span><span class="sxs-lookup"><span data-stu-id="84ef6-152">-Namespace</span></span>
<span data-ttu-id="84ef6-153">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="84ef6-153">Namespace Name</span></span>

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

### <span data-ttu-id="84ef6-154">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="84ef6-154">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="84ef6-155">RequiresDuplicateDetection - a value that indicates that the queue supports the concept of session</span><span class="sxs-lookup"><span data-stu-id="84ef6-155">RequiresDuplicateDetection - a value that indicates whether the queue supports the concept of session</span></span>

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

### <span data-ttu-id="84ef6-156">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="84ef6-156">-RequiresSession</span></span>
<span data-ttu-id="84ef6-157">RequiresSession - the value indicating if this queue uses sessions</span><span class="sxs-lookup"><span data-stu-id="84ef6-157">RequiresSession - the value indicating if this queue uses sessions</span></span>

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

### <span data-ttu-id="84ef6-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84ef6-158">-ResourceGroupName</span></span>
<span data-ttu-id="84ef6-159">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="84ef6-159">The name of the resource group</span></span>

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

### <span data-ttu-id="84ef6-160">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="84ef6-160">-SizeInBytes</span></span>
<span data-ttu-id="84ef6-161">SizeInBytes – a várólisták mérete bájtban</span><span class="sxs-lookup"><span data-stu-id="84ef6-161">SizeInBytes - the size of the queue in bytes</span></span>

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

### <span data-ttu-id="84ef6-162">-Confirm</span><span class="sxs-lookup"><span data-stu-id="84ef6-162">-Confirm</span></span>
<span data-ttu-id="84ef6-163">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="84ef6-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84ef6-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84ef6-164">-WhatIf</span></span>
<span data-ttu-id="84ef6-165">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="84ef6-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84ef6-166">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="84ef6-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84ef6-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84ef6-167">CommonParameters</span></span>
<span data-ttu-id="84ef6-168">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84ef6-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84ef6-169">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84ef6-169">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84ef6-170">INPUTS</span><span class="sxs-lookup"><span data-stu-id="84ef6-170">INPUTS</span></span>

### <span data-ttu-id="84ef6-171">System.String</span><span class="sxs-lookup"><span data-stu-id="84ef6-171">System.String</span></span>

### <span data-ttu-id="84ef6-172">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="84ef6-172">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="84ef6-173">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="84ef6-173">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="84ef6-174">System.Nullable'1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="84ef6-174">System.Nullable\`1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="84ef6-175">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="84ef6-175">OUTPUTS</span></span>

### <span data-ttu-id="84ef6-176">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="84ef6-176">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="84ef6-177">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="84ef6-177">NOTES</span></span>

## <span data-ttu-id="84ef6-178">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="84ef6-178">RELATED LINKS</span></span>
