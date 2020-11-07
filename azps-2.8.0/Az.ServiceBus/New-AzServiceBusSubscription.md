---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusSubscription.md
ms.openlocfilehash: 2ed5d3345730e631b3f7668ca4b05f3decc04f06
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838806"
---
# <span data-ttu-id="140d0-101">New-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="140d0-101">New-AzServiceBusSubscription</span></span>

## <span data-ttu-id="140d0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="140d0-102">SYNOPSIS</span></span>
<span data-ttu-id="140d0-103">Előfizetést hoz létre a megadott buszjárati témakörhöz.</span><span class="sxs-lookup"><span data-stu-id="140d0-103">Creates a subscription to the specified Service Bus topic.</span></span>

## <span data-ttu-id="140d0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="140d0-104">SYNTAX</span></span>

```
New-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [-AutoDeleteOnIdle <String>] [-DefaultMessageTimeToLive <String>]
 [-DeadLetteringOnMessageExpiration <Boolean>] [-DeadLetteringOnFilterEvaluationExceptions]
 [-EnableBatchedOperations <Boolean>] [-LockDuration <String>] [-MaxDeliveryCount <Int32>]
 [-RequiresSession <Boolean>] [-ForwardTo <String>] [-ForwardDeadLetteredMessagesTo <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="140d0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="140d0-105">DESCRIPTION</span></span>
<span data-ttu-id="140d0-106">A **New-AzServiceBusSubscription** parancsmag új előfizetést hoz létre a megadott buszjárati témakörhöz.</span><span class="sxs-lookup"><span data-stu-id="140d0-106">The **New-AzServiceBusSubscription** cmdlet creates a new subscription to the specified Service Bus topic.</span></span>

## <span data-ttu-id="140d0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="140d0-107">EXAMPLES</span></span>

### <span data-ttu-id="140d0-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="140d0-108">Example 1</span></span>
```
PS C:\> New-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1

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

<span data-ttu-id="140d0-109">Az előfizetést hozza létre `SB-TopicSubscription-Example1` a megadott buszjárati témakörhöz `SB-Topic_exampl1` .</span><span class="sxs-lookup"><span data-stu-id="140d0-109">Creates the subscription `SB-TopicSubscription-Example1` for the specified Service Bus topic `SB-Topic_exampl1`.</span></span>

## <span data-ttu-id="140d0-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="140d0-110">PARAMETERS</span></span>

### <span data-ttu-id="140d0-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="140d0-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="140d0-112">A [időszak](https://msdn.microsoft.com/library/system.timespan.aspx) üresjárati intervallumát adja meg, amely után az előfizetés automatikusan törlődik.</span><span class="sxs-lookup"><span data-stu-id="140d0-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the subscription is automatically deleted.</span></span> <span data-ttu-id="140d0-113">A minimális időtartam 5 perc.</span><span class="sxs-lookup"><span data-stu-id="140d0-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="140d0-114">-DeadLetteringOnFilterEvaluationExceptions</span><span class="sxs-lookup"><span data-stu-id="140d0-114">-DeadLetteringOnFilterEvaluationExceptions</span></span>
<span data-ttu-id="140d0-115">Az az érték, amely azt jelzi, hogy az előfizetéshez tartozik-e a szűrő kiértékelésének kivételeinek támogatása.</span><span class="sxs-lookup"><span data-stu-id="140d0-115">Value that indicates whether a subscription has dead letter support on filter evaluation exceptions.</span></span>

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

### <span data-ttu-id="140d0-116">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="140d0-116">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="140d0-117">Az üzenet lejárata halott betűkkel</span><span class="sxs-lookup"><span data-stu-id="140d0-117">Dead Lettering On Message Expiration</span></span>

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

### <span data-ttu-id="140d0-118">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="140d0-118">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="140d0-119">Időszak az élő értékre.</span><span class="sxs-lookup"><span data-stu-id="140d0-119">Timespan to live value.</span></span>
<span data-ttu-id="140d0-120">Ez az az időtartam, amely után az üzenet lejár, attól kezdve, hogy mikor küldi el az üzenetet a szolgáltatás Buszjának.</span><span class="sxs-lookup"><span data-stu-id="140d0-120">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>
<span data-ttu-id="140d0-121">Ez az alapértelmezett érték akkor használható, ha a TimeToLive nem egy üzeneten van beállítva.</span><span class="sxs-lookup"><span data-stu-id="140d0-121">This is the default value used when TimeToLive is not set on a message itself.</span></span>
<span data-ttu-id="140d0-122">Standard = időszak. Max és Basic = 14 nap</span><span class="sxs-lookup"><span data-stu-id="140d0-122">For Standard = Timespan.Max and Basic = 14 days</span></span>

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

### <span data-ttu-id="140d0-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="140d0-123">-DefaultProfile</span></span>
<span data-ttu-id="140d0-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="140d0-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="140d0-125">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="140d0-125">-EnableBatchedOperations</span></span>
<span data-ttu-id="140d0-126">Kötegelt műveletek engedélyezése – érték, amely azt jelzi, hogy engedélyezve van-e a kiszolgálóoldali kötegelt műveletek</span><span class="sxs-lookup"><span data-stu-id="140d0-126">Enable Batched Operations - value that indicates whether server-side batched operations are enabled</span></span>

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

### <span data-ttu-id="140d0-127">-ForwardDeadLetteredMessagesTo</span><span class="sxs-lookup"><span data-stu-id="140d0-127">-ForwardDeadLetteredMessagesTo</span></span>
<span data-ttu-id="140d0-128">A várólista vagy a téma neve a halotti üzenet továbbításához</span><span class="sxs-lookup"><span data-stu-id="140d0-128">Queue/Topic name to forward the Dead Letter message</span></span>

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

### <span data-ttu-id="140d0-129">-ForwardTo</span><span class="sxs-lookup"><span data-stu-id="140d0-129">-ForwardTo</span></span>
<span data-ttu-id="140d0-130">A várólista vagy a téma neve az üzenetek továbbításához</span><span class="sxs-lookup"><span data-stu-id="140d0-130">Queue/Topic name to forward the messages</span></span>

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

### <span data-ttu-id="140d0-131">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="140d0-131">-LockDuration</span></span>
<span data-ttu-id="140d0-132">Zárolás időtartama</span><span class="sxs-lookup"><span data-stu-id="140d0-132">Lock Duration</span></span>

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

### <span data-ttu-id="140d0-133">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="140d0-133">-MaxDeliveryCount</span></span>
<span data-ttu-id="140d0-134">MaxDeliveryCount – a kézbesítés maximális száma.</span><span class="sxs-lookup"><span data-stu-id="140d0-134">MaxDeliveryCount - the maximum delivery count.</span></span>
<span data-ttu-id="140d0-135">Ezt követően az üzenet automatikusan deadlettered a kézbesítések száma után.</span><span class="sxs-lookup"><span data-stu-id="140d0-135">A message is automatically deadlettered after this number of deliveries.</span></span>

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

### <span data-ttu-id="140d0-136">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="140d0-136">-Name</span></span>
<span data-ttu-id="140d0-137">Előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="140d0-137">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="140d0-138">-Namespace</span><span class="sxs-lookup"><span data-stu-id="140d0-138">-Namespace</span></span>
<span data-ttu-id="140d0-139">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="140d0-139">Namespace Name</span></span>

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

### <span data-ttu-id="140d0-140">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="140d0-140">-RequiresSession</span></span>
<span data-ttu-id="140d0-141">RequiresSession – az az érték, amely azt jelzi, hogy a várólistán ismétlődő észlelés szükséges.</span><span class="sxs-lookup"><span data-stu-id="140d0-141">RequiresSession - the value indicating if this queue requires duplicate detection.</span></span>

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

### <span data-ttu-id="140d0-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="140d0-142">-ResourceGroupName</span></span>
<span data-ttu-id="140d0-143">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="140d0-143">The name of the resource group</span></span>

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

### <span data-ttu-id="140d0-144">-Topic</span><span class="sxs-lookup"><span data-stu-id="140d0-144">-Topic</span></span>
<span data-ttu-id="140d0-145">Téma neve</span><span class="sxs-lookup"><span data-stu-id="140d0-145">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="140d0-146">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="140d0-146">-Confirm</span></span>
<span data-ttu-id="140d0-147">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="140d0-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="140d0-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="140d0-148">-WhatIf</span></span>
<span data-ttu-id="140d0-149">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="140d0-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="140d0-150">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="140d0-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="140d0-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="140d0-151">CommonParameters</span></span>
<span data-ttu-id="140d0-152">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="140d0-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="140d0-153">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="140d0-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="140d0-154">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="140d0-154">INPUTS</span></span>

### <span data-ttu-id="140d0-155">System. String</span><span class="sxs-lookup"><span data-stu-id="140d0-155">System.String</span></span>

### <span data-ttu-id="140d0-156">System. null ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="140d0-156">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="140d0-157">System. null ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="140d0-157">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="140d0-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="140d0-158">OUTPUTS</span></span>

### <span data-ttu-id="140d0-159">Microsoft. Azure. Command. ServiceBus. models. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="140d0-159">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="140d0-160">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="140d0-160">NOTES</span></span>

## <span data-ttu-id="140d0-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="140d0-161">RELATED LINKS</span></span>
