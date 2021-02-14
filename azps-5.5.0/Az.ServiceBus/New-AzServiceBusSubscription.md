---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusSubscription.md
ms.openlocfilehash: 53f91cb6904cb8c481a5379d5499805ffe82ce33
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208127"
---
# <span data-ttu-id="414fe-101">New-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="414fe-101">New-AzServiceBusSubscription</span></span>

## <span data-ttu-id="414fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="414fe-102">SYNOPSIS</span></span>
<span data-ttu-id="414fe-103">Létrehoz egy előfizetést a szolgáltatásbusz megadott témaköréhez.</span><span class="sxs-lookup"><span data-stu-id="414fe-103">Creates a subscription to the specified Service Bus topic.</span></span>

## <span data-ttu-id="414fe-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="414fe-104">SYNTAX</span></span>

```
New-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [-AutoDeleteOnIdle <String>] [-DefaultMessageTimeToLive <String>]
 [-DeadLetteringOnMessageExpiration <Boolean>] [-DeadLetteringOnFilterEvaluationExceptions]
 [-EnableBatchedOperations <Boolean>] [-LockDuration <String>] [-MaxDeliveryCount <Int32>]
 [-RequiresSession <Boolean>] [-ForwardTo <String>] [-ForwardDeadLetteredMessagesTo <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="414fe-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="414fe-105">DESCRIPTION</span></span>
<span data-ttu-id="414fe-106">A **New-AzServiceBusSubscription** parancsmag létrehoz egy új előfizetést a megadott Service Bus-témakörre.</span><span class="sxs-lookup"><span data-stu-id="414fe-106">The **New-AzServiceBusSubscription** cmdlet creates a new subscription to the specified Service Bus topic.</span></span>

## <span data-ttu-id="414fe-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="414fe-107">EXAMPLES</span></span>

### <span data-ttu-id="414fe-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="414fe-108">Example 1</span></span>
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

<span data-ttu-id="414fe-109">Létrehozza a megadott Service `SB-TopicSubscription-Example1` Bus-témakör `SB-Topic_exampl1` előfizetését.</span><span class="sxs-lookup"><span data-stu-id="414fe-109">Creates the subscription `SB-TopicSubscription-Example1` for the specified Service Bus topic `SB-Topic_exampl1`.</span></span>

## <span data-ttu-id="414fe-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="414fe-110">PARAMETERS</span></span>

### <span data-ttu-id="414fe-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="414fe-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="414fe-112">A [TimeSpan idle](https://msdn.microsoft.com/library/system.timespan.aspx) interval (IdőTartomány üresjárati idő) megadása, amely után az előfizetés automatikusan törlődik.</span><span class="sxs-lookup"><span data-stu-id="414fe-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the subscription is automatically deleted.</span></span> <span data-ttu-id="414fe-113">A minimális időtartam 5 perc.</span><span class="sxs-lookup"><span data-stu-id="414fe-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="414fe-114">-DeadLetteringOnFilterEvaluationExceptions</span><span class="sxs-lookup"><span data-stu-id="414fe-114">-DeadLetteringOnFilterEvaluationExceptions</span></span>
<span data-ttu-id="414fe-115">Érték, amely azt jelzi, hogy egy előfizetésben a szűrőértékelési kivételek esetén támogatottak-e az elhalt levélek.</span><span class="sxs-lookup"><span data-stu-id="414fe-115">Value that indicates whether a subscription has dead letter support on filter evaluation exceptions.</span></span>

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

### <span data-ttu-id="414fe-116">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="414fe-116">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="414fe-117">Dead Lettering On Message Expiration</span><span class="sxs-lookup"><span data-stu-id="414fe-117">Dead Lettering On Message Expiration</span></span>

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

### <span data-ttu-id="414fe-118">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="414fe-118">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="414fe-119">Időkorrekta az élő értékhez</span><span class="sxs-lookup"><span data-stu-id="414fe-119">Timespan to live value.</span></span>
<span data-ttu-id="414fe-120">Ez az az időtartam, amely után az üzenet lejár, attól kezdve, hogy az üzenetet elküldik a szolgáltatásbusznak.</span><span class="sxs-lookup"><span data-stu-id="414fe-120">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>
<span data-ttu-id="414fe-121">Ez az alapértelmezett érték, amikor a TimeToLive nincs beállítva az üzeneten.</span><span class="sxs-lookup"><span data-stu-id="414fe-121">This is the default value used when TimeToLive is not set on a message itself.</span></span>
<span data-ttu-id="414fe-122">Normál = Timespan.Max és Basic = 14 nap</span><span class="sxs-lookup"><span data-stu-id="414fe-122">For Standard = Timespan.Max and Basic = 14 days</span></span>

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

### <span data-ttu-id="414fe-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="414fe-123">-DefaultProfile</span></span>
<span data-ttu-id="414fe-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="414fe-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="414fe-125">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="414fe-125">-EnableBatchedOperations</span></span>
<span data-ttu-id="414fe-126">A batched Operations engedélyezése – érték, amely azt jelzi, hogy engedélyezettek-e a kiszolgálóoldali köteges műveletek</span><span class="sxs-lookup"><span data-stu-id="414fe-126">Enable Batched Operations - value that indicates whether server-side batched operations are enabled</span></span>

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

### <span data-ttu-id="414fe-127">-ForwardDeadLetteredMessagesTo</span><span class="sxs-lookup"><span data-stu-id="414fe-127">-ForwardDeadLetteredMessagesTo</span></span>
<span data-ttu-id="414fe-128">Queue/Topic name to forward the Dead Letter message</span><span class="sxs-lookup"><span data-stu-id="414fe-128">Queue/Topic name to forward the Dead Letter message</span></span>

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

### <span data-ttu-id="414fe-129">-ForwardTo</span><span class="sxs-lookup"><span data-stu-id="414fe-129">-ForwardTo</span></span>
<span data-ttu-id="414fe-130">Az üzenetek továbbítása várólistán vagy témakörben</span><span class="sxs-lookup"><span data-stu-id="414fe-130">Queue/Topic name to forward the messages</span></span>

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

### <span data-ttu-id="414fe-131">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="414fe-131">-LockDuration</span></span>
<span data-ttu-id="414fe-132">Zárolás időtartama</span><span class="sxs-lookup"><span data-stu-id="414fe-132">Lock Duration</span></span>

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

### <span data-ttu-id="414fe-133">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="414fe-133">-MaxDeliveryCount</span></span>
<span data-ttu-id="414fe-134">MaxDeliveryCount – a maximális kézbesítési szám.</span><span class="sxs-lookup"><span data-stu-id="414fe-134">MaxDeliveryCount - the maximum delivery count.</span></span>
<span data-ttu-id="414fe-135">Ennyi kézbesítés után az üzenetek automatikusan elhalnak.</span><span class="sxs-lookup"><span data-stu-id="414fe-135">A message is automatically deadlettered after this number of deliveries.</span></span>

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

### <span data-ttu-id="414fe-136">-Name</span><span class="sxs-lookup"><span data-stu-id="414fe-136">-Name</span></span>
<span data-ttu-id="414fe-137">Előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="414fe-137">Subscription Name</span></span>

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

### <span data-ttu-id="414fe-138">-Namespace</span><span class="sxs-lookup"><span data-stu-id="414fe-138">-Namespace</span></span>
<span data-ttu-id="414fe-139">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="414fe-139">Namespace Name</span></span>

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

### <span data-ttu-id="414fe-140">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="414fe-140">-RequiresSession</span></span>
<span data-ttu-id="414fe-141">RequiresSession - the value indicating if this queue requires duplicate detection.</span><span class="sxs-lookup"><span data-stu-id="414fe-141">RequiresSession - the value indicating if this queue requires duplicate detection.</span></span>

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

### <span data-ttu-id="414fe-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="414fe-142">-ResourceGroupName</span></span>
<span data-ttu-id="414fe-143">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="414fe-143">The name of the resource group</span></span>

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

### <span data-ttu-id="414fe-144">-Topic</span><span class="sxs-lookup"><span data-stu-id="414fe-144">-Topic</span></span>
<span data-ttu-id="414fe-145">Témakör neve</span><span class="sxs-lookup"><span data-stu-id="414fe-145">Topic Name</span></span>

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

### <span data-ttu-id="414fe-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="414fe-146">-Confirm</span></span>
<span data-ttu-id="414fe-147">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="414fe-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="414fe-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="414fe-148">-WhatIf</span></span>
<span data-ttu-id="414fe-149">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="414fe-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="414fe-150">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="414fe-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="414fe-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="414fe-151">CommonParameters</span></span>
<span data-ttu-id="414fe-152">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="414fe-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="414fe-153">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="414fe-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="414fe-154">INPUTS</span><span class="sxs-lookup"><span data-stu-id="414fe-154">INPUTS</span></span>

### <span data-ttu-id="414fe-155">System.String</span><span class="sxs-lookup"><span data-stu-id="414fe-155">System.String</span></span>

### <span data-ttu-id="414fe-156">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="414fe-156">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="414fe-157">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="414fe-157">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="414fe-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="414fe-158">OUTPUTS</span></span>

### <span data-ttu-id="414fe-159">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="414fe-159">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="414fe-160">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="414fe-160">NOTES</span></span>

## <span data-ttu-id="414fe-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="414fe-161">RELATED LINKS</span></span>
