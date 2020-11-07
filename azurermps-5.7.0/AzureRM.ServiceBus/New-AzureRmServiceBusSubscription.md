---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusSubscription.md
ms.openlocfilehash: 54753001be0a754cf9416e1b2ec53fd81647d8d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93678927"
---
# <span data-ttu-id="c333b-101">New-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="c333b-101">New-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="c333b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c333b-102">SYNOPSIS</span></span>
<span data-ttu-id="c333b-103">Előfizetést hoz létre a megadott buszjárati témakörhöz.</span><span class="sxs-lookup"><span data-stu-id="c333b-103">Creates a subscription to the specified Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c333b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c333b-104">SYNTAX</span></span>

```
New-AzureRmServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [-AutoDeleteOnIdle <String>] [-DefaultMessageTimeToLive <String>]
 [-DeadLetteringOnMessageExpiration <Boolean>] [-DeadLetteringOnFilterEvaluationExceptions]
 [-EnableBatchedOperations <Boolean>] [-LockDuration <String>] [-MaxDeliveryCount <Int32>]
 [-RequiresSession <Boolean>] [-ForwardTo <String>] [-ForwardDeadLetteredMessagesTo <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c333b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c333b-105">DESCRIPTION</span></span>
<span data-ttu-id="c333b-106">A **New-AzureRmServiceBusSubscription** parancsmag új előfizetést hoz létre a megadott buszjárati témakörhöz.</span><span class="sxs-lookup"><span data-stu-id="c333b-106">The **New-AzureRmServiceBusSubscription** cmdlet creates a new subscription to the specified Service Bus topic.</span></span>

## <span data-ttu-id="c333b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c333b-107">EXAMPLES</span></span>

### <span data-ttu-id="c333b-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c333b-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1

Name                                      : SB-TopicSubscription-Example1
AccessedAt                                : 1/20/2017 3:18:54 AM
AutoDeleteOnIdle                          : 10675199.02:48:05.4775807
CountDetails                              : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
CreatedAt                                 : 1/20/2017 3:18:52 AM
DefaultMessageTimeToLive                  : 10675199.02:48:05.4775807
DeadLetteringOnMessageExpiration          : False
EnableBatchedOperations                   : True
LockDuration                              : 00:01:00
MaxDeliveryCount                          : 10
MessageCount                              : 0
RequiresSession                           : False
Status                                    : Active
UpdatedAt                                 : 1/20/2017 3:18:54 AM
```
<span data-ttu-id="c333b-109">Az előfizetést hozza létre `SB-TopicSubscription-Example1` a megadott buszjárati témakörhöz `SB-Topic_exampl1` .</span><span class="sxs-lookup"><span data-stu-id="c333b-109">Creates the subscription `SB-TopicSubscription-Example1` for the specified Service Bus topic `SB-Topic_exampl1`.</span></span>

## <span data-ttu-id="c333b-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c333b-110">PARAMETERS</span></span>

### <span data-ttu-id="c333b-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="c333b-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="c333b-112">A [időszak](https://msdn.microsoft.com/library/system.timespan.aspx) üresjárati intervallumát adja meg, amely után az előfizetés automatikusan törlődik.</span><span class="sxs-lookup"><span data-stu-id="c333b-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the subscription is automatically deleted.</span></span> <span data-ttu-id="c333b-113">A minimális időtartam 5 perc.</span><span class="sxs-lookup"><span data-stu-id="c333b-113">The minimum duration is 5 minutes.</span></span>


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

### <span data-ttu-id="c333b-114">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c333b-114">-Confirm</span></span>
<span data-ttu-id="c333b-115">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c333b-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c333b-116">-DeadLetteringOnFilterEvaluationExceptions</span><span class="sxs-lookup"><span data-stu-id="c333b-116">-DeadLetteringOnFilterEvaluationExceptions</span></span>
<span data-ttu-id="c333b-117">Az az érték, amely azt jelzi, hogy az előfizetéshez tartozik-e a szűrő kiértékelésének kivételeinek támogatása.</span><span class="sxs-lookup"><span data-stu-id="c333b-117">Value that indicates whether a subscription has dead letter support on filter evaluation exceptions.</span></span>

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

### <span data-ttu-id="c333b-118">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="c333b-118">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="c333b-119">Az üzenet lejárata halott betűkkel</span><span class="sxs-lookup"><span data-stu-id="c333b-119">Dead Lettering On Message Expiration</span></span>

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

### <span data-ttu-id="c333b-120">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="c333b-120">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="c333b-121">Időszak az élő értékre.</span><span class="sxs-lookup"><span data-stu-id="c333b-121">Timespan to live value.</span></span>
<span data-ttu-id="c333b-122">Ez az az időtartam, amely után az üzenet lejár, attól kezdve, hogy mikor küldi el az üzenetet a szolgáltatás Buszjának.</span><span class="sxs-lookup"><span data-stu-id="c333b-122">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>
<span data-ttu-id="c333b-123">Ez az alapértelmezett érték akkor használható, ha a TimeToLive nem egy üzeneten van beállítva.</span><span class="sxs-lookup"><span data-stu-id="c333b-123">This is the default value used when TimeToLive is not set on a message itself.</span></span>
<span data-ttu-id="c333b-124">A standard = időszak. Max és az Basic = 14 Dyas</span><span class="sxs-lookup"><span data-stu-id="c333b-124">For Standard = Timespan.Max and Basic = 14 dyas</span></span>

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

### <span data-ttu-id="c333b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c333b-125">-DefaultProfile</span></span>
<span data-ttu-id="c333b-126">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c333b-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c333b-127">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="c333b-127">-EnableBatchedOperations</span></span>
<span data-ttu-id="c333b-128">Kötegelt műveletek engedélyezése – érték, amely azt jelzi, hogy engedélyezve van-e a kiszolgálóoldali kötegelt műveletek</span><span class="sxs-lookup"><span data-stu-id="c333b-128">Enable Batched Operations - value that indicates whether server-side batched operations are enabled</span></span>

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

### <span data-ttu-id="c333b-129">-ForwardDeadLetteredMessagesTo</span><span class="sxs-lookup"><span data-stu-id="c333b-129">-ForwardDeadLetteredMessagesTo</span></span>
<span data-ttu-id="c333b-130">A várólista vagy a téma neve a halotti üzenet továbbításához</span><span class="sxs-lookup"><span data-stu-id="c333b-130">Queue/Topic name to forward the Dead Letter message</span></span>

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

### <span data-ttu-id="c333b-131">-ForwardTo</span><span class="sxs-lookup"><span data-stu-id="c333b-131">-ForwardTo</span></span>
<span data-ttu-id="c333b-132">A várólista vagy a téma neve az üzenetek továbbításához</span><span class="sxs-lookup"><span data-stu-id="c333b-132">Queue/Topic name to forward the messages</span></span>

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

### <span data-ttu-id="c333b-133">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="c333b-133">-LockDuration</span></span>
<span data-ttu-id="c333b-134">Zárolás időtartama</span><span class="sxs-lookup"><span data-stu-id="c333b-134">Lock Duration</span></span>

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

### <span data-ttu-id="c333b-135">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="c333b-135">-MaxDeliveryCount</span></span>
<span data-ttu-id="c333b-136">MaxDeliveryCount – a kézbesítés maximális száma.</span><span class="sxs-lookup"><span data-stu-id="c333b-136">MaxDeliveryCount - the maximum delivery count.</span></span>
<span data-ttu-id="c333b-137">Ezt követően az üzenet automatikusan deadlettered a kézbesítések száma után.</span><span class="sxs-lookup"><span data-stu-id="c333b-137">A message is automatically deadlettered after this number of deliveries.</span></span>

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

### <span data-ttu-id="c333b-138">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c333b-138">-Name</span></span>
<span data-ttu-id="c333b-139">Előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="c333b-139">Subscription Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c333b-140">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c333b-140">-Namespace</span></span>
<span data-ttu-id="c333b-141">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="c333b-141">Namespace Name</span></span>

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

### <span data-ttu-id="c333b-142">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="c333b-142">-RequiresSession</span></span>
<span data-ttu-id="c333b-143">RequiresSession – az az érték, amely azt jelzi, hogy a várólistán ismétlődő észlelés szükséges.</span><span class="sxs-lookup"><span data-stu-id="c333b-143">RequiresSession - the value indicating if this queue requires duplicate detection.</span></span>

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

### <span data-ttu-id="c333b-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c333b-144">-ResourceGroupName</span></span>
<span data-ttu-id="c333b-145">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="c333b-145">The name of the resource group</span></span>

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

### <span data-ttu-id="c333b-146">-Topic</span><span class="sxs-lookup"><span data-stu-id="c333b-146">-Topic</span></span>
<span data-ttu-id="c333b-147">Téma neve</span><span class="sxs-lookup"><span data-stu-id="c333b-147">Topic Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c333b-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c333b-148">-WhatIf</span></span>
<span data-ttu-id="c333b-149">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c333b-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c333b-150">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c333b-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c333b-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c333b-151">CommonParameters</span></span>
<span data-ttu-id="c333b-152">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c333b-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="c333b-153">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c333b-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c333b-154">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c333b-154">INPUTS</span></span>

### <span data-ttu-id="c333b-155">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c333b-155">-ResourceGroup</span></span>
 <span data-ttu-id="c333b-156">System. String</span><span class="sxs-lookup"><span data-stu-id="c333b-156">System.String</span></span>
 

### <span data-ttu-id="c333b-157">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="c333b-157">-NamespaceName</span></span>
 <span data-ttu-id="c333b-158">System. String</span><span class="sxs-lookup"><span data-stu-id="c333b-158">System.String</span></span>
 

### <span data-ttu-id="c333b-159">-TopicName</span><span class="sxs-lookup"><span data-stu-id="c333b-159">-TopicName</span></span>
 <span data-ttu-id="c333b-160">System. String</span><span class="sxs-lookup"><span data-stu-id="c333b-160">System.String</span></span>
 

### <span data-ttu-id="c333b-161">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="c333b-161">-SubscriptionName</span></span>
 <span data-ttu-id="c333b-162">System. String</span><span class="sxs-lookup"><span data-stu-id="c333b-162">System.String</span></span>


## <span data-ttu-id="c333b-163">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c333b-163">OUTPUTS</span></span>

### <span data-ttu-id="c333b-164">Microsoft. Azure. Command. ServiceBus. models. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="c333b-164">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>


## <span data-ttu-id="c333b-165">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c333b-165">NOTES</span></span>

## <span data-ttu-id="c333b-166">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c333b-166">RELATED LINKS</span></span>
