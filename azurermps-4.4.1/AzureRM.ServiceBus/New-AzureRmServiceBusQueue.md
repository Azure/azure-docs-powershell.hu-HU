---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueue.md
ms.openlocfilehash: 4538bb39c085a2e7152a146d5e93e08a0c09f5de
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493360"
---
# <span data-ttu-id="5fcab-101">New-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="5fcab-101">New-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="5fcab-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5fcab-102">SYNOPSIS</span></span>
<span data-ttu-id="5fcab-103">Létrehoz egy szolgáltatás busz-várólistáját a megadott Service Bus névtérben.</span><span class="sxs-lookup"><span data-stu-id="5fcab-103">Creates a Service Bus queue in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5fcab-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5fcab-104">SYNTAX</span></span>

```
New-AzureRmServiceBusQueue -ResourceGroupName <String> -Namespace <String> -Name <String>
 -EnablePartitioning <Boolean> [-LockDuration <String>] [-AutoDeleteOnIdle <String>]
 [-DefaultMessageTimeToLive <String>] [-DuplicateDetectionHistoryTimeWindow <String>]
 [-EnableBatchedOperations <Boolean>] [-DeadLetteringOnMessageExpiration <Boolean>] [-EnableExpress <Boolean>]
 [-IsAnonymousAccessible <Boolean>] [-MaxDeliveryCount <Int32>] [-MaxSizeInMegabytes <Int64>]
 [-MessageCount <Int64>] [-RequiresDuplicateDetection <Boolean>] [-RequiresSession <Boolean>]
 [-SizeInBytes <Int64>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5fcab-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5fcab-105">DESCRIPTION</span></span>
<span data-ttu-id="5fcab-106">A **New-AzureRmServiceBusQueue** parancsmag létrehoz egy szolgáltatás busz-várólistáját a megadott Service Bus névtérben.</span><span class="sxs-lookup"><span data-stu-id="5fcab-106">The **New-AzureRmServiceBusQueue** cmdlet creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="5fcab-107">Példák</span><span class="sxs-lookup"><span data-stu-id="5fcab-107">EXAMPLES</span></span>

### <span data-ttu-id="5fcab-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5fcab-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -EnablePartitioning $True
```

<span data-ttu-id="5fcab-109">Új szervizsorok-várólistát hoz létre `SB-Queue_exampl1` a megadott szolgáltatási busz névtérben `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="5fcab-109">Creates a new Service Bus queue `SB-Queue_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="5fcab-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5fcab-110">PARAMETERS</span></span>

### <span data-ttu-id="5fcab-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="5fcab-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="5fcab-112">A [időszak](https://msdn.microsoft.com/library/system.timespan.aspx) üresjárati intervallumát adja meg, amely után a rendszer automatikusan törli a várólistát.</span><span class="sxs-lookup"><span data-stu-id="5fcab-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the queue is automatically deleted.</span></span> <span data-ttu-id="5fcab-113">A minimális időtartam 5 perc.</span><span class="sxs-lookup"><span data-stu-id="5fcab-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="5fcab-114">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="5fcab-114">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="5fcab-115">Meghatározza, hogy az üzenetek deadlettered-e a lejárat során.</span><span class="sxs-lookup"><span data-stu-id="5fcab-115">Specifies whether messages are deadlettered on expiration.</span></span>

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

### <span data-ttu-id="5fcab-116">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="5fcab-116">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="5fcab-117">Az alapértelmezett üzenet időpontját adja meg (TTL).</span><span class="sxs-lookup"><span data-stu-id="5fcab-117">Specifies the default message time-to-live (TTL).</span></span>

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

### <span data-ttu-id="5fcab-118">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="5fcab-118">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="5fcab-119">A duplikáltelem-észlelési előzmények időablakát adja meg, a [időszak](https://msdn.microsoft.com/library/system.timespan.aspx) valuethat határozza meg a duplikáltelem-észlelési előzmények időtartamát.</span><span class="sxs-lookup"><span data-stu-id="5fcab-119">Specifies the duplicate detection history time window, a [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) valuethat defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="5fcab-120">Az alapértelmezett érték 10 perc.</span><span class="sxs-lookup"><span data-stu-id="5fcab-120">The default value is 10 minutes.</span></span>

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

### <span data-ttu-id="5fcab-121">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="5fcab-121">-EnableBatchedOperations</span></span>
<span data-ttu-id="5fcab-122">Megadja, hogy engedélyezve vannak-e a kiszolgálóoldali kötegelt műveletek.</span><span class="sxs-lookup"><span data-stu-id="5fcab-122">Specifies whether server-side batched operations are enabled.</span></span>

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

### <span data-ttu-id="5fcab-123">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="5fcab-123">-EnableExpress</span></span>
<span data-ttu-id="5fcab-124">Megadja, hogy engedélyezve vannak-e az Express-entitások.</span><span class="sxs-lookup"><span data-stu-id="5fcab-124">Specifies whether Express Entities are enabled.</span></span> <span data-ttu-id="5fcab-125">Az Express-várólisták átmenetileg tárolják az üzenetet a memóriában, mielőtt állandó tárterületre írom azt.</span><span class="sxs-lookup"><span data-stu-id="5fcab-125">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

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

### <span data-ttu-id="5fcab-126">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="5fcab-126">-EnablePartitioning</span></span>
<span data-ttu-id="5fcab-127">Megadja, hogy engedélyezve van-e a EnablePartitioning.</span><span class="sxs-lookup"><span data-stu-id="5fcab-127">Specifies whether EnablePartitioning is enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 
Accepted values: TRUE, FALSE

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fcab-128">-IsAnonymousAccessible</span><span class="sxs-lookup"><span data-stu-id="5fcab-128">-IsAnonymousAccessible</span></span>
<span data-ttu-id="5fcab-129">Azt adja meg, hogy az üzenet névtelenül érhető-e el.</span><span class="sxs-lookup"><span data-stu-id="5fcab-129">Specifies whether the message is anonymously accessible.</span></span>

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

### <span data-ttu-id="5fcab-130">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="5fcab-130">-LockDuration</span></span>
<span data-ttu-id="5fcab-131">A zárolás időtartamát adja meg.</span><span class="sxs-lookup"><span data-stu-id="5fcab-131">Specifies the lock duration.</span></span>

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

### <span data-ttu-id="5fcab-132">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="5fcab-132">-MaxDeliveryCount</span></span>
<span data-ttu-id="5fcab-133">A maximális kézbesítési számot adja meg.</span><span class="sxs-lookup"><span data-stu-id="5fcab-133">Specifies the maximum delivery count.</span></span> <span data-ttu-id="5fcab-134">Ezt követően az üzenet automatikusan deadlettered a kézbesítések száma után.</span><span class="sxs-lookup"><span data-stu-id="5fcab-134">A message is automatically deadlettered after this number of deliveries.</span></span>

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

### <span data-ttu-id="5fcab-135">-MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="5fcab-135">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="5fcab-136">A várólista maximális méretét adja meg megabájtban, ami a várólista számára lefoglalt memória mérete.</span><span class="sxs-lookup"><span data-stu-id="5fcab-136">Specifies the maximum size of the queue in megabytes, which is the size of memory allocated for the queue.</span></span>

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

### <span data-ttu-id="5fcab-137">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="5fcab-137">-MessageCount</span></span>
<span data-ttu-id="5fcab-138">A várólistában lévő üzenetek számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="5fcab-138">Specifies the number of messages in the queue.</span></span>

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

### <span data-ttu-id="5fcab-139">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="5fcab-139">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="5fcab-140">Meghatározza, hogy a várólistán duplikált elemek észlelése szükséges-e.</span><span class="sxs-lookup"><span data-stu-id="5fcab-140">Specifies whether the queue requires duplicate detection.</span></span>

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

### <span data-ttu-id="5fcab-141">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="5fcab-141">-RequiresSession</span></span>
<span data-ttu-id="5fcab-142">Megadja, hogy a várólista támogatja-e a munkameneteket.</span><span class="sxs-lookup"><span data-stu-id="5fcab-142">Specifies whether this queue supports sessions.</span></span>

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

### <span data-ttu-id="5fcab-143">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="5fcab-143">-SizeInBytes</span></span>
<span data-ttu-id="5fcab-144">A várólista mérete bájtban kifejezve</span><span class="sxs-lookup"><span data-stu-id="5fcab-144">The size of the queue in bytes.</span></span>

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

### <span data-ttu-id="5fcab-145">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5fcab-145">-Confirm</span></span>
<span data-ttu-id="5fcab-146">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5fcab-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5fcab-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fcab-147">-WhatIf</span></span>
<span data-ttu-id="5fcab-148">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5fcab-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5fcab-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5fcab-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5fcab-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fcab-150">-DefaultProfile</span></span>
<span data-ttu-id="5fcab-151">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5fcab-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5fcab-152">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5fcab-152">-Name</span></span>
<span data-ttu-id="5fcab-153">Várólista neve</span><span class="sxs-lookup"><span data-stu-id="5fcab-153">Queue Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fcab-154">-Namespace</span><span class="sxs-lookup"><span data-stu-id="5fcab-154">-Namespace</span></span>
<span data-ttu-id="5fcab-155">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="5fcab-155">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fcab-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fcab-156">-ResourceGroupName</span></span>
<span data-ttu-id="5fcab-157">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="5fcab-157">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fcab-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fcab-158">CommonParameters</span></span>
<span data-ttu-id="5fcab-159">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5fcab-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fcab-160">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fcab-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fcab-161">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5fcab-161">INPUTS</span></span>

### <span data-ttu-id="5fcab-162">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5fcab-162">-ResourceGroup</span></span>
 <span data-ttu-id="5fcab-163">System. String</span><span class="sxs-lookup"><span data-stu-id="5fcab-163">System.String</span></span>

### <span data-ttu-id="5fcab-164">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="5fcab-164">-NamespaceName</span></span>
 <span data-ttu-id="5fcab-165">System. String</span><span class="sxs-lookup"><span data-stu-id="5fcab-165">System.String</span></span>

### <span data-ttu-id="5fcab-166">-QueueName</span><span class="sxs-lookup"><span data-stu-id="5fcab-166">-QueueName</span></span>
 <span data-ttu-id="5fcab-167">System. String</span><span class="sxs-lookup"><span data-stu-id="5fcab-167">System.String</span></span>

### <span data-ttu-id="5fcab-168">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="5fcab-168">-EnablePartitioning</span></span>
 <span data-ttu-id="5fcab-169">System. Boolean?</span><span class="sxs-lookup"><span data-stu-id="5fcab-169">System.Boolean?</span></span>

## <span data-ttu-id="5fcab-170">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5fcab-170">OUTPUTS</span></span>

### <span data-ttu-id="5fcab-171">Microsoft. Azure. Command. ServiceBus. models. QueueAttributes</span><span class="sxs-lookup"><span data-stu-id="5fcab-171">Microsoft.Azure.Commands.ServiceBus.Models.QueueAttributes</span></span>
<span data-ttu-id="5fcab-172">Név: SB-Queue_exampl1 hely: West US LockDuration: AccessedAt: AutoDeleteOnIdle: 10675199.02:48:05.4775807 EntityAvailabilityStatus: CreatedAt: 1/20/2017 2:51:36-es DefaultMessageTimeToLive: 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow: EnableBatchedOperations: true DeadLetteringOnMessageExpiration: false EnableExpress: false EnablePartitioning: true IsAnonymousAccessible: false MaxDeliveryCount: MaxSizeInMegabytes: 16384 MessageCount: CountDetails: RequiresDuplicateDetection: RequiresSession: SizeInBytes: false SupportOrdering: false UpdatedAt: True: Active 1/20/2017 2:51:37</span><span class="sxs-lookup"><span data-stu-id="5fcab-172">Name                                : SB-Queue_exampl1 Location                            : West US LockDuration                        : AccessedAt                          : AutoDeleteOnIdle                    : 10675199.02:48:05.4775807 EntityAvailabilityStatus            : CreatedAt                           : 1/20/2017 2:51:36 AM DefaultMessageTimeToLive            : 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow : EnableBatchedOperations             : True DeadLetteringOnMessageExpiration    : False EnableExpress                       : False EnablePartitioning                  : True IsAnonymousAccessible               : False MaxDeliveryCount                    : MaxSizeInMegabytes                  : 16384 MessageCount                        : CountDetails                        : RequiresDuplicateDetection          : False RequiresSession                     : False SizeInBytes                         : Status                              : Active SupportOrdering                     : False UpdatedAt                           : 1/20/2017 2:51:37 AM</span></span>

## <span data-ttu-id="5fcab-173">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5fcab-173">NOTES</span></span>

## <span data-ttu-id="5fcab-174">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5fcab-174">RELATED LINKS</span></span>

