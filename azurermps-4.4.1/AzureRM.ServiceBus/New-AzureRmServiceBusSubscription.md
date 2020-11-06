---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusSubscription.md
ms.openlocfilehash: ea305b334e6efd4cb1c5af47db2a1b8817e7cab6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496855"
---
# <span data-ttu-id="4a1a0-101">New-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="4a1a0-101">New-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="4a1a0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4a1a0-102">SYNOPSIS</span></span>
<span data-ttu-id="4a1a0-103">Előfizetést hoz létre a megadott buszjárati témakörhöz.</span><span class="sxs-lookup"><span data-stu-id="4a1a0-103">Creates a subscription to the specified Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a1a0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4a1a0-104">SYNTAX</span></span>

```
New-AzureRmServiceBusSubscription -ResourceGroupName <String> -Namespace <String> -Topic <String>
 -Name <String> [-AutoDeleteOnIdle <String>] [-DefaultMessageTimeToLive <String>]
 [-DeadLetteringOnFilterEvaluationExceptions <Boolean>] [-DeadLetteringOnMessageExpiration <Boolean>]
 [-EnableBatchedOperations <Boolean>] [-IsReadOnly <Boolean>] [-LockDuration <String>]
 [-MaxDeliveryCount <Int32>] [-RequiresSession <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a1a0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4a1a0-105">DESCRIPTION</span></span>
<span data-ttu-id="4a1a0-106">A **New-AzureRmServiceBusSubscription** parancsmag új előfizetést hoz létre a megadott buszjárati témakörhöz.</span><span class="sxs-lookup"><span data-stu-id="4a1a0-106">The **New-AzureRmServiceBusSubscription** cmdlet creates a new subscription to the specified Service Bus topic.</span></span>

## <span data-ttu-id="4a1a0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4a1a0-107">EXAMPLES</span></span>

### <span data-ttu-id="4a1a0-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4a1a0-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1
```

<span data-ttu-id="4a1a0-109">Az előfizetést hozza létre `SB-TopicSubscription-Example1` a megadott buszjárati témakörhöz `SB-Topic_exampl1` .</span><span class="sxs-lookup"><span data-stu-id="4a1a0-109">Creates the subscription `SB-TopicSubscription-Example1` for the specified Service Bus topic `SB-Topic_exampl1`.</span></span>

## <span data-ttu-id="4a1a0-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4a1a0-110">PARAMETERS</span></span>

### <span data-ttu-id="4a1a0-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="4a1a0-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="4a1a0-112">A [időszak](https://msdn.microsoft.com/library/system.timespan.aspx) üresjárati intervallumát adja meg, amely után az előfizetés automatikusan törlődik.</span><span class="sxs-lookup"><span data-stu-id="4a1a0-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the subscription is automatically deleted.</span></span> <span data-ttu-id="4a1a0-113">A minimális időtartam 5 perc.</span><span class="sxs-lookup"><span data-stu-id="4a1a0-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="4a1a0-114">-DeadLetteringOnFilterEvaluationExceptions</span><span class="sxs-lookup"><span data-stu-id="4a1a0-114">-DeadLetteringOnFilterEvaluationExceptions</span></span>
<span data-ttu-id="4a1a0-115">Azt jelzi, hogy egy előfizetéshez tartozik-e halotti támogatás a szűrési kiértékelési kivételekhez.</span><span class="sxs-lookup"><span data-stu-id="4a1a0-115">Indicates if a subscription has dead letter support on Filter evaluation exceptions.</span></span>

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

### <span data-ttu-id="4a1a0-116">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="4a1a0-116">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="4a1a0-117">Azt jelzi, hogy az előfizetésnek van-e deadletter támogatása az üzenet lejáratakor.</span><span class="sxs-lookup"><span data-stu-id="4a1a0-117">Indicates if a subscription has deadletter support when a message expires.</span></span>

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

### <span data-ttu-id="4a1a0-118">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="4a1a0-118">-EnableBatchedOperations</span></span>
<span data-ttu-id="4a1a0-119">Azt jelzi, hogy engedélyezve vannak-e a kiszolgálóoldali kötegelt műveletek.</span><span class="sxs-lookup"><span data-stu-id="4a1a0-119">Indicates whether server-side batched operations are enabled.</span></span>

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

### <span data-ttu-id="4a1a0-120">-IsReadOnly</span><span class="sxs-lookup"><span data-stu-id="4a1a0-120">-IsReadOnly</span></span>
<span data-ttu-id="4a1a0-121">Azt jelzi, hogy az egyed leírása írásvédett-e</span><span class="sxs-lookup"><span data-stu-id="4a1a0-121">Indicates whether the entity description is read-only</span></span>

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

### <span data-ttu-id="4a1a0-122">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="4a1a0-122">-LockDuration</span></span>
<span data-ttu-id="4a1a0-123">Az előfizetéshez tartozó időtartam zárolásának időbeli intervallumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4a1a0-123">Specifies the lock duration time span for the subscription.</span></span>

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

### <span data-ttu-id="4a1a0-124">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="4a1a0-124">-MaxDeliveryCount</span></span>
<span data-ttu-id="4a1a0-125">A maximális kézbesítések számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4a1a0-125">Specifies the number of maximum deliveries.</span></span> <span data-ttu-id="4a1a0-126">Ezt követően az üzenet automatikusan deadlettered a kézbesítések száma után.</span><span class="sxs-lookup"><span data-stu-id="4a1a0-126">A message is automatically deadlettered after this number of deliveries.</span></span>

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

### <span data-ttu-id="4a1a0-127">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="4a1a0-127">-RequiresSession</span></span>
<span data-ttu-id="4a1a0-128">Annak megadása, hogy az előfizetés támogatja-e a munkamenetek fogalmát.</span><span class="sxs-lookup"><span data-stu-id="4a1a0-128">Specifies whether a subscription supports the concept of sessions.</span></span>

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

### <span data-ttu-id="4a1a0-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4a1a0-129">-Confirm</span></span>
<span data-ttu-id="4a1a0-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4a1a0-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a1a0-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a1a0-131">-WhatIf</span></span>
<span data-ttu-id="4a1a0-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4a1a0-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a1a0-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4a1a0-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a1a0-134">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="4a1a0-134">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="4a1a0-135">Időszak az élő értékre.</span><span class="sxs-lookup"><span data-stu-id="4a1a0-135">Timespan to live value.</span></span> <span data-ttu-id="4a1a0-136">Ez az az időtartam, amely után az üzenet lejár, attól kezdve, hogy mikor küldi el az üzenetet a szolgáltatás Buszjának.</span><span class="sxs-lookup"><span data-stu-id="4a1a0-136">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span> <span data-ttu-id="4a1a0-137">Ez az alapértelmezett érték akkor használható, ha a TimeToLive nem egy üzeneten van beállítva.</span><span class="sxs-lookup"><span data-stu-id="4a1a0-137">This is the default value used when TimeToLive is not set on a message itself.</span></span> <span data-ttu-id="4a1a0-138">A standard = időszak. Max és az Basic = 14 Dyas</span><span class="sxs-lookup"><span data-stu-id="4a1a0-138">For Standard = Timespan.Max and Basic = 14 dyas</span></span>

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

### <span data-ttu-id="4a1a0-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a1a0-139">-DefaultProfile</span></span>
<span data-ttu-id="4a1a0-140">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4a1a0-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a1a0-141">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4a1a0-141">-Name</span></span>
<span data-ttu-id="4a1a0-142">Előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="4a1a0-142">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a1a0-143">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4a1a0-143">-Namespace</span></span>
<span data-ttu-id="4a1a0-144">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="4a1a0-144">Namespace Name.</span></span>

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

### <span data-ttu-id="4a1a0-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a1a0-145">-ResourceGroupName</span></span>
<span data-ttu-id="4a1a0-146">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="4a1a0-146">The name of the resource group</span></span>

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

### <span data-ttu-id="4a1a0-147">-Topic</span><span class="sxs-lookup"><span data-stu-id="4a1a0-147">-Topic</span></span>
<span data-ttu-id="4a1a0-148">A téma neve</span><span class="sxs-lookup"><span data-stu-id="4a1a0-148">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a1a0-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a1a0-149">CommonParameters</span></span>
<span data-ttu-id="4a1a0-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4a1a0-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a1a0-151">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a1a0-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a1a0-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4a1a0-152">INPUTS</span></span>

### <span data-ttu-id="4a1a0-153">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4a1a0-153">-ResourceGroup</span></span>
 <span data-ttu-id="4a1a0-154">System. String</span><span class="sxs-lookup"><span data-stu-id="4a1a0-154">System.String</span></span>
 

### <span data-ttu-id="4a1a0-155">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="4a1a0-155">-NamespaceName</span></span>
 <span data-ttu-id="4a1a0-156">System. String</span><span class="sxs-lookup"><span data-stu-id="4a1a0-156">System.String</span></span>
 

### <span data-ttu-id="4a1a0-157">-TopicName</span><span class="sxs-lookup"><span data-stu-id="4a1a0-157">-TopicName</span></span>
 <span data-ttu-id="4a1a0-158">System. String</span><span class="sxs-lookup"><span data-stu-id="4a1a0-158">System.String</span></span>
 

### <span data-ttu-id="4a1a0-159">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="4a1a0-159">-SubscriptionName</span></span>
 <span data-ttu-id="4a1a0-160">System. String</span><span class="sxs-lookup"><span data-stu-id="4a1a0-160">System.String</span></span>

## <span data-ttu-id="4a1a0-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4a1a0-161">OUTPUTS</span></span>

### <span data-ttu-id="4a1a0-162">Microsoft. Azure. Command. ServiceBus. models. SubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="4a1a0-162">Microsoft.Azure.Commands.ServiceBus.Models.SubscriptionAttributes</span></span>
<span data-ttu-id="4a1a0-163">Name (név): SB-TopicSubscription-example1-es hely: Nyugat-amerikai AccessedAt: 1/20/2017 3:18:54 AM AutoDeleteOnIdle: 10675199.02:48:05.4775807 CountDetails: Microsoft. Azure. Management. ServiceBus. models. MessageCountDetails CreatedAt: 1/20/2017 3:18:52 AM DefaultMessageTimeToLive: AM 10675199.02:05.4775807:: DeadLetteringOnFilterEvaluationExceptions: DeadLetteringOnMessageExpiration: EnableBatchedOperations: EntityAvailabilityStatus: true IsReadOnly: false LockDuration: true MaxDeliveryCount: MessageCount: RequiresSession: 00:01:00 UpdatedAt: 10:1/20/2017 3:18:54</span><span class="sxs-lookup"><span data-stu-id="4a1a0-163">Name                                      : SB-TopicSubscription-Example1 Location                                  : West US AccessedAt                                : 1/20/2017 3:18:54 AM AutoDeleteOnIdle                          : 10675199.02:48:05.4775807 CountDetails                              : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails CreatedAt                                 : 1/20/2017 3:18:52 AM DefaultMessageTimeToLive                  : 10675199.02:48:05.4775807 DeadLetteringOnFilterEvaluationExceptions : True DeadLetteringOnMessageExpiration          : False EnableBatchedOperations                   : True EntityAvailabilityStatus                  : Available IsReadOnly                                : LockDuration                              : 00:01:00 MaxDeliveryCount                          : 10 MessageCount                              : 0 RequiresSession                           : False Status                                    : Active UpdatedAt                                 : 1/20/2017 3:18:54 AM</span></span>

## <span data-ttu-id="4a1a0-164">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4a1a0-164">NOTES</span></span>

## <span data-ttu-id="4a1a0-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4a1a0-165">RELATED LINKS</span></span>

