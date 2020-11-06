---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueue.md
ms.openlocfilehash: 29e2c0f04dff07e76907ee67c3e012c2b67c1582
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499396"
---
# <span data-ttu-id="3170f-101">New-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="3170f-101">New-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="3170f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3170f-102">SYNOPSIS</span></span>
<span data-ttu-id="3170f-103">Létrehoz egy szolgáltatás busz-várólistáját a megadott Service Bus névtérben.</span><span class="sxs-lookup"><span data-stu-id="3170f-103">Creates a Service Bus queue in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3170f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3170f-104">SYNTAX</span></span>

```
New-AzureRmServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-EnablePartitioning <Boolean>] [-LockDuration <String>] [-AutoDeleteOnIdle <String>]
 [-DefaultMessageTimeToLive <String>] [-DuplicateDetectionHistoryTimeWindow <String>]
 [-DeadLetteringOnMessageExpiration <Boolean>] [-EnableBatchedOperations] [-EnableExpress <Boolean>]
 [-MaxDeliveryCount <Int32>] [-MaxSizeInMegabytes <Int64>] [-MessageCount <Int64>]
 [-RequiresDuplicateDetection <Boolean>] [-RequiresSession <Boolean>] [-SizeInBytes <Int64>]
 [-ForwardTo <String>] [-ForwardDeadLetteredMessagesTo <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3170f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3170f-105">DESCRIPTION</span></span>
<span data-ttu-id="3170f-106">A **New-AzureRmServiceBusQueue** parancsmag létrehoz egy szolgáltatás busz-várólistáját a megadott Service Bus névtérben.</span><span class="sxs-lookup"><span data-stu-id="3170f-106">The **New-AzureRmServiceBusQueue** cmdlet creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="3170f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3170f-107">EXAMPLES</span></span>

### <span data-ttu-id="3170f-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3170f-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1 -EnablePartitioning $True

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

<span data-ttu-id="3170f-109">Új szervizsorok-várólistát hoz létre `SB-Queue_example1` a megadott szolgáltatási busz névtérben `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="3170f-109">Creates a new Service Bus queue `SB-Queue_example1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="3170f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3170f-110">PARAMETERS</span></span>

### <span data-ttu-id="3170f-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="3170f-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="3170f-112">A [időszak](https://msdn.microsoft.com/library/system.timespan.aspx) üresjárati intervallumát adja meg, amely után a rendszer automatikusan törli a várólistát.</span><span class="sxs-lookup"><span data-stu-id="3170f-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the queue is automatically deleted.</span></span> <span data-ttu-id="3170f-113">A minimális időtartam 5 perc.</span><span class="sxs-lookup"><span data-stu-id="3170f-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="3170f-114">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="3170f-114">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="3170f-115">Az üzenet lejárata halott betűkkel</span><span class="sxs-lookup"><span data-stu-id="3170f-115">Dead Lettering On Message Expiration</span></span>

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

### <span data-ttu-id="3170f-116">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="3170f-116">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="3170f-117">Időszak az élő értékre.</span><span class="sxs-lookup"><span data-stu-id="3170f-117">Timespan to live value.</span></span>
<span data-ttu-id="3170f-118">Ez az az időtartam, amely után az üzenet lejár, attól kezdve, hogy mikor küldi el az üzenetet a szolgáltatás Buszjának.</span><span class="sxs-lookup"><span data-stu-id="3170f-118">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>
<span data-ttu-id="3170f-119">Ez az alapértelmezett érték akkor használható, ha a TimeToLive nem egy üzeneten van beállítva.</span><span class="sxs-lookup"><span data-stu-id="3170f-119">This is the default value used when TimeToLive is not set on a message itself.</span></span>
<span data-ttu-id="3170f-120">A standard = időszak. Max és az Basic = 14 Dyas</span><span class="sxs-lookup"><span data-stu-id="3170f-120">For Standard = Timespan.Max and Basic = 14 dyas</span></span>

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

### <span data-ttu-id="3170f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3170f-121">-DefaultProfile</span></span>
<span data-ttu-id="3170f-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3170f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3170f-123">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="3170f-123">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="3170f-124">A duplikáltelem-észlelési előzmények időablakát adja meg, a [időszak](https://msdn.microsoft.com/library/system.timespan.aspx) valuethat határozza meg a duplikáltelem-észlelési előzmények időtartamát.</span><span class="sxs-lookup"><span data-stu-id="3170f-124">Specifies the duplicate detection history time window, a [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) valuethat defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="3170f-125">Az alapértelmezett érték 10 perc.</span><span class="sxs-lookup"><span data-stu-id="3170f-125">The default value is 10 minutes.</span></span>

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

### <span data-ttu-id="3170f-126">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="3170f-126">-EnableBatchedOperations</span></span>
<span data-ttu-id="3170f-127">Kötegelt műveletek engedélyezése – érték, amely azt jelzi, hogy engedélyezve van-e a kiszolgálóoldali kötegelt műveletek</span><span class="sxs-lookup"><span data-stu-id="3170f-127">Enable Batched Operations - value that indicates whether server-side batched operations are enabled</span></span>

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

### <span data-ttu-id="3170f-128">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="3170f-128">-EnableExpress</span></span>
<span data-ttu-id="3170f-129">EnableExpress – az a érték, amely azt jelzi, hogy engedélyezve vannak-e az Express-entitások.</span><span class="sxs-lookup"><span data-stu-id="3170f-129">EnableExpress - a value that indicates whether Express Entities are enabled.</span></span>
<span data-ttu-id="3170f-130">Az Express-várólisták átmenetileg tárolják az üzenetet a memóriában, mielőtt állandó tárterületre írom azt.</span><span class="sxs-lookup"><span data-stu-id="3170f-130">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

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

### <span data-ttu-id="3170f-131">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="3170f-131">-EnablePartitioning</span></span>
<span data-ttu-id="3170f-132">EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="3170f-132">EnablePartitioning</span></span>

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

### <span data-ttu-id="3170f-133">-ForwardDeadLetteredMessagesTo</span><span class="sxs-lookup"><span data-stu-id="3170f-133">-ForwardDeadLetteredMessagesTo</span></span>
<span data-ttu-id="3170f-134">A várólista vagy a téma neve a halotti üzenet továbbításához</span><span class="sxs-lookup"><span data-stu-id="3170f-134">Queue/Topic name to forward the Dead Letter message</span></span>

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

### <span data-ttu-id="3170f-135">-ForwardTo</span><span class="sxs-lookup"><span data-stu-id="3170f-135">-ForwardTo</span></span>
<span data-ttu-id="3170f-136">A várólista vagy a téma neve az üzenetek továbbításához</span><span class="sxs-lookup"><span data-stu-id="3170f-136">Queue/Topic name to forward the messages</span></span>

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

### <span data-ttu-id="3170f-137">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="3170f-137">-LockDuration</span></span>
<span data-ttu-id="3170f-138">Zárolás időtartama</span><span class="sxs-lookup"><span data-stu-id="3170f-138">Lock Duration</span></span>

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

### <span data-ttu-id="3170f-139">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="3170f-139">-MaxDeliveryCount</span></span>
<span data-ttu-id="3170f-140">MaxDeliveryCount – a kézbesítés maximális száma.</span><span class="sxs-lookup"><span data-stu-id="3170f-140">MaxDeliveryCount - the maximum delivery count.</span></span>
<span data-ttu-id="3170f-141">Ezt követően az üzenet automatikusan deadlettered a kézbesítések száma után.</span><span class="sxs-lookup"><span data-stu-id="3170f-141">A message is automatically deadlettered after this number of deliveries.</span></span>

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

### <span data-ttu-id="3170f-142">-MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="3170f-142">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="3170f-143">MaxSizeInMegabytes – a várólista maximális mérete megabájtban, ami a várólistához lefoglalt memória mérete.</span><span class="sxs-lookup"><span data-stu-id="3170f-143">MaxSizeInMegabytes - the maximum size of the queue in megabytes, which is the size of memory allocated for the queue.</span></span>

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

### <span data-ttu-id="3170f-144">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="3170f-144">-MessageCount</span></span>
<span data-ttu-id="3170f-145">MessageCount – a várólistán lévő üzenetek száma</span><span class="sxs-lookup"><span data-stu-id="3170f-145">MessageCount - the number of messages in the queue</span></span>

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

### <span data-ttu-id="3170f-146">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3170f-146">-Name</span></span>
<span data-ttu-id="3170f-147">Várólista neve</span><span class="sxs-lookup"><span data-stu-id="3170f-147">Queue Name</span></span>

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

### <span data-ttu-id="3170f-148">-Namespace</span><span class="sxs-lookup"><span data-stu-id="3170f-148">-Namespace</span></span>
<span data-ttu-id="3170f-149">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="3170f-149">Namespace Name</span></span>

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

### <span data-ttu-id="3170f-150">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="3170f-150">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="3170f-151">RequiresDuplicateDetection – egy érték, amely azt jelzi, hogy a várólista támogatja-e a munkamenet fogalmát</span><span class="sxs-lookup"><span data-stu-id="3170f-151">RequiresDuplicateDetection - a value that indicates whether the queue supports the concept of session</span></span>

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

### <span data-ttu-id="3170f-152">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="3170f-152">-RequiresSession</span></span>
<span data-ttu-id="3170f-153">RequiresSession – annak az értéknek az értéke, ha ez a várólista ismétlődő észlelést követel meg</span><span class="sxs-lookup"><span data-stu-id="3170f-153">RequiresSession - the value indicating if this queue requires duplicate detection</span></span>

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

### <span data-ttu-id="3170f-154">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3170f-154">-ResourceGroupName</span></span>
<span data-ttu-id="3170f-155">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="3170f-155">The name of the resource group</span></span>

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

### <span data-ttu-id="3170f-156">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="3170f-156">-SizeInBytes</span></span>
<span data-ttu-id="3170f-157">SizeInBytes – a várólista mérete bájtban kifejezve</span><span class="sxs-lookup"><span data-stu-id="3170f-157">SizeInBytes - the size of the queue in bytes</span></span>

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

### <span data-ttu-id="3170f-158">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3170f-158">-Confirm</span></span>
<span data-ttu-id="3170f-159">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3170f-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3170f-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3170f-160">-WhatIf</span></span>
<span data-ttu-id="3170f-161">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3170f-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3170f-162">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3170f-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3170f-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3170f-163">CommonParameters</span></span>
<span data-ttu-id="3170f-164">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3170f-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3170f-165">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3170f-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3170f-166">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3170f-166">INPUTS</span></span>

### <span data-ttu-id="3170f-167">System. String</span><span class="sxs-lookup"><span data-stu-id="3170f-167">System.String</span></span>

### <span data-ttu-id="3170f-168">System. null ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="3170f-168">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="3170f-169">System. null ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="3170f-169">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="3170f-170">System. null ' 1 [[System. Int64, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="3170f-170">System.Nullable\`1[[System.Int64, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="3170f-171">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3170f-171">OUTPUTS</span></span>

### <span data-ttu-id="3170f-172">Microsoft. Azure. Command. ServiceBus. models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="3170f-172">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="3170f-173">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3170f-173">NOTES</span></span>

## <span data-ttu-id="3170f-174">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3170f-174">RELATED LINKS</span></span>
