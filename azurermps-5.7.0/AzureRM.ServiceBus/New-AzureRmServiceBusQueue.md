---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueue.md
ms.openlocfilehash: 8e1b1cd39e30bcbe2ccc9f46b5ab39511e4de58f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93678928"
---
# <span data-ttu-id="dd8dc-101">New-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="dd8dc-101">New-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="dd8dc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dd8dc-102">SYNOPSIS</span></span>
<span data-ttu-id="dd8dc-103">Létrehoz egy szolgáltatás busz-várólistáját a megadott Service Bus névtérben.</span><span class="sxs-lookup"><span data-stu-id="dd8dc-103">Creates a Service Bus queue in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd8dc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dd8dc-104">SYNTAX</span></span>

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

## <span data-ttu-id="dd8dc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="dd8dc-105">DESCRIPTION</span></span>
<span data-ttu-id="dd8dc-106">A **New-AzureRmServiceBusQueue** parancsmag létrehoz egy szolgáltatás busz-várólistáját a megadott Service Bus névtérben.</span><span class="sxs-lookup"><span data-stu-id="dd8dc-106">The **New-AzureRmServiceBusQueue** cmdlet creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="dd8dc-107">Példák</span><span class="sxs-lookup"><span data-stu-id="dd8dc-107">EXAMPLES</span></span>

### <span data-ttu-id="dd8dc-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="dd8dc-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -EnablePartitioning $True

Name                                : SB-Queue_exampl1
LockDuration                        : 
AccessedAt                          : 
AutoDeleteOnIdle                    : 10675199.02:48:05.4775807
CreatedAt                           : 1/20/2017 2:51:36 AM
DefaultMessageTimeToLive            : 10675199.02:48:05.4775807
DuplicateDetectionHistoryTimeWindow : 
DeadLetteringOnMessageExpiration    : False
EnableExpress                       : False
EnablePartitioning                  : True
MaxDeliveryCount                    : 
MaxSizeInMegabytes                  : 16384
MessageCount                        : 
CountDetails                        : 
RequiresDuplicateDetection          : False
RequiresSession                     : False
SizeInBytes                         : 
Status                              : Active
UpdatedAt                           : 1/20/2017 2:51:37 AM
```
<span data-ttu-id="dd8dc-109">Új szervizsorok-várólistát hoz létre `SB-Queue_exampl1` a megadott szolgáltatási busz névtérben `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="dd8dc-109">Creates a new Service Bus queue `SB-Queue_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="dd8dc-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dd8dc-110">PARAMETERS</span></span>

### <span data-ttu-id="dd8dc-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="dd8dc-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="dd8dc-112">A [időszak](https://msdn.microsoft.com/library/system.timespan.aspx) üresjárati intervallumát adja meg, amely után a rendszer automatikusan törli a várólistát.</span><span class="sxs-lookup"><span data-stu-id="dd8dc-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the queue is automatically deleted.</span></span> <span data-ttu-id="dd8dc-113">A minimális időtartam 5 perc.</span><span class="sxs-lookup"><span data-stu-id="dd8dc-113">The minimum duration is 5 minutes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd8dc-114">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="dd8dc-114">-Confirm</span></span>
<span data-ttu-id="dd8dc-115">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="dd8dc-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd8dc-116">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="dd8dc-116">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="dd8dc-117">Az üzenet lejárata halott betűkkel</span><span class="sxs-lookup"><span data-stu-id="dd8dc-117">Dead Lettering On Message Expiration</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd8dc-118">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="dd8dc-118">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="dd8dc-119">Időszak az élő értékre.</span><span class="sxs-lookup"><span data-stu-id="dd8dc-119">Timespan to live value.</span></span>
<span data-ttu-id="dd8dc-120">Ez az az időtartam, amely után az üzenet lejár, attól kezdve, hogy mikor küldi el az üzenetet a szolgáltatás Buszjának.</span><span class="sxs-lookup"><span data-stu-id="dd8dc-120">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>
<span data-ttu-id="dd8dc-121">Ez az alapértelmezett érték akkor használható, ha a TimeToLive nem egy üzeneten van beállítva.</span><span class="sxs-lookup"><span data-stu-id="dd8dc-121">This is the default value used when TimeToLive is not set on a message itself.</span></span>
<span data-ttu-id="dd8dc-122">A standard = időszak. Max és az Basic = 14 Dyas</span><span class="sxs-lookup"><span data-stu-id="dd8dc-122">For Standard = Timespan.Max and Basic = 14 dyas</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd8dc-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd8dc-123">-DefaultProfile</span></span>
<span data-ttu-id="dd8dc-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dd8dc-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd8dc-125">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="dd8dc-125">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="dd8dc-126">A duplikáltelem-észlelési előzmények időablakát adja meg, a [időszak](https://msdn.microsoft.com/library/system.timespan.aspx) valuethat határozza meg a duplikáltelem-észlelési előzmények időtartamát.</span><span class="sxs-lookup"><span data-stu-id="dd8dc-126">Specifies the duplicate detection history time window, a [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) valuethat defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="dd8dc-127">Az alapértelmezett érték 10 perc.</span><span class="sxs-lookup"><span data-stu-id="dd8dc-127">The default value is 10 minutes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd8dc-128">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="dd8dc-128">-EnableBatchedOperations</span></span>
<span data-ttu-id="dd8dc-129">Kötegelt műveletek engedélyezése – érték, amely azt jelzi, hogy engedélyezve van-e a kiszolgálóoldali kötegelt műveletek</span><span class="sxs-lookup"><span data-stu-id="dd8dc-129">Enable Batched Operations - value that indicates whether server-side batched operations are enabled</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd8dc-130">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="dd8dc-130">-EnableExpress</span></span>
<span data-ttu-id="dd8dc-131">EnableExpress – az a érték, amely azt jelzi, hogy engedélyezve vannak-e az Express-entitások.</span><span class="sxs-lookup"><span data-stu-id="dd8dc-131">EnableExpress - a value that indicates whether Express Entities are enabled.</span></span>
<span data-ttu-id="dd8dc-132">Az Express-várólisták átmenetileg tárolják az üzenetet a memóriában, mielőtt állandó tárterületre írom azt.</span><span class="sxs-lookup"><span data-stu-id="dd8dc-132">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd8dc-133">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="dd8dc-133">-EnablePartitioning</span></span>
<span data-ttu-id="dd8dc-134">EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="dd8dc-134">EnablePartitioning</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd8dc-135">-ForwardDeadLetteredMessagesTo</span><span class="sxs-lookup"><span data-stu-id="dd8dc-135">-ForwardDeadLetteredMessagesTo</span></span>
<span data-ttu-id="dd8dc-136">A várólista vagy a téma neve a halotti üzenet továbbításához</span><span class="sxs-lookup"><span data-stu-id="dd8dc-136">Queue/Topic name to forward the Dead Letter message</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd8dc-137">-ForwardTo</span><span class="sxs-lookup"><span data-stu-id="dd8dc-137">-ForwardTo</span></span>
<span data-ttu-id="dd8dc-138">A várólista vagy a téma neve az üzenetek továbbításához</span><span class="sxs-lookup"><span data-stu-id="dd8dc-138">Queue/Topic name to forward the messages</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd8dc-139">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="dd8dc-139">-LockDuration</span></span>
<span data-ttu-id="dd8dc-140">Zárolás időtartama</span><span class="sxs-lookup"><span data-stu-id="dd8dc-140">Lock Duration</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd8dc-141">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="dd8dc-141">-MaxDeliveryCount</span></span>
<span data-ttu-id="dd8dc-142">MaxDeliveryCount – a kézbesítés maximális száma.</span><span class="sxs-lookup"><span data-stu-id="dd8dc-142">MaxDeliveryCount - the maximum delivery count.</span></span>
<span data-ttu-id="dd8dc-143">Ezt követően az üzenet automatikusan deadlettered a kézbesítések száma után.</span><span class="sxs-lookup"><span data-stu-id="dd8dc-143">A message is automatically deadlettered after this number of deliveries.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd8dc-144">-MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="dd8dc-144">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="dd8dc-145">MaxSizeInMegabytes – a várólista maximális mérete megabájtban, ami a várólistához lefoglalt memória mérete.</span><span class="sxs-lookup"><span data-stu-id="dd8dc-145">MaxSizeInMegabytes - the maximum size of the queue in megabytes, which is the size of memory allocated for the queue.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd8dc-146">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="dd8dc-146">-MessageCount</span></span>
<span data-ttu-id="dd8dc-147">MessageCount – a várólistán lévő üzenetek száma</span><span class="sxs-lookup"><span data-stu-id="dd8dc-147">MessageCount - the number of messages in the queue</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd8dc-148">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dd8dc-148">-Name</span></span>
<span data-ttu-id="dd8dc-149">Várólista neve</span><span class="sxs-lookup"><span data-stu-id="dd8dc-149">Queue Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd8dc-150">-Namespace</span><span class="sxs-lookup"><span data-stu-id="dd8dc-150">-Namespace</span></span>
<span data-ttu-id="dd8dc-151">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="dd8dc-151">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd8dc-152">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="dd8dc-152">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="dd8dc-153">RequiresDuplicateDetection – egy érték, amely azt jelzi, hogy a várólista támogatja-e a munkamenet fogalmát</span><span class="sxs-lookup"><span data-stu-id="dd8dc-153">RequiresDuplicateDetection - a value that indicates whether the queue supports the concept of session</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd8dc-154">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="dd8dc-154">-RequiresSession</span></span>
<span data-ttu-id="dd8dc-155">RequiresSession – annak az értéknek az értéke, ha ez a várólista ismétlődő észlelést követel meg</span><span class="sxs-lookup"><span data-stu-id="dd8dc-155">RequiresSession - the value indicating if this queue requires duplicate detection</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd8dc-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd8dc-156">-ResourceGroupName</span></span>
<span data-ttu-id="dd8dc-157">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="dd8dc-157">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd8dc-158">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="dd8dc-158">-SizeInBytes</span></span>
<span data-ttu-id="dd8dc-159">SizeInBytes – a várólista mérete bájtban kifejezve</span><span class="sxs-lookup"><span data-stu-id="dd8dc-159">SizeInBytes - the size of the queue in bytes</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd8dc-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd8dc-160">-WhatIf</span></span>
<span data-ttu-id="dd8dc-161">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="dd8dc-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd8dc-162">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dd8dc-162">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd8dc-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd8dc-163">CommonParameters</span></span>
<span data-ttu-id="dd8dc-164">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dd8dc-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="dd8dc-165">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd8dc-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd8dc-166">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dd8dc-166">INPUTS</span></span>

### <span data-ttu-id="dd8dc-167">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="dd8dc-167">-ResourceGroup</span></span>
 <span data-ttu-id="dd8dc-168">System. String</span><span class="sxs-lookup"><span data-stu-id="dd8dc-168">System.String</span></span>

### <span data-ttu-id="dd8dc-169">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="dd8dc-169">-NamespaceName</span></span>
 <span data-ttu-id="dd8dc-170">System. String</span><span class="sxs-lookup"><span data-stu-id="dd8dc-170">System.String</span></span>

### <span data-ttu-id="dd8dc-171">-QueueName</span><span class="sxs-lookup"><span data-stu-id="dd8dc-171">-QueueName</span></span>
 <span data-ttu-id="dd8dc-172">System. String</span><span class="sxs-lookup"><span data-stu-id="dd8dc-172">System.String</span></span>

### <span data-ttu-id="dd8dc-173">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="dd8dc-173">-EnablePartitioning</span></span>
 <span data-ttu-id="dd8dc-174">System. Boolean?</span><span class="sxs-lookup"><span data-stu-id="dd8dc-174">System.Boolean?</span></span>


## <span data-ttu-id="dd8dc-175">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dd8dc-175">OUTPUTS</span></span>

### <span data-ttu-id="dd8dc-176">Microsoft. Azure. Command. ServiceBus. models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="dd8dc-176">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>


## <span data-ttu-id="dd8dc-177">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dd8dc-177">NOTES</span></span>

## <span data-ttu-id="dd8dc-178">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dd8dc-178">RELATED LINKS</span></span>
