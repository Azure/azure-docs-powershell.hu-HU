---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusSubscription.md
ms.openlocfilehash: 13e221c0205f07be81d01fd5011fa2d937b020a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680224"
---
# <span data-ttu-id="33dad-101">Set-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="33dad-101">Set-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="33dad-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="33dad-102">SYNOPSIS</span></span>
<span data-ttu-id="33dad-103">Az előfizetések leírását frissíti a megadott szolgáltatási busz névtérben lévő buszjáratok témakörében.</span><span class="sxs-lookup"><span data-stu-id="33dad-103">Updates a subscription description for a Service Bus topic in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33dad-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="33dad-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusSubscription -ResourceGroupName <String> -Namespace <String> -Topic <String>
 -InputObject <SubscriptionAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="33dad-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="33dad-105">DESCRIPTION</span></span>
<span data-ttu-id="33dad-106">A **set-AzureRmServiceBusSubscription** parancsmag frissíti a megadott Service Bus-névtérben a szolgáltatás buszjának előfizetése leírását.</span><span class="sxs-lookup"><span data-stu-id="33dad-106">The **Set-AzureRmServiceBusSubscription** cmdlet updates the description of the subscription for the Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="33dad-107">Példák</span><span class="sxs-lookup"><span data-stu-id="33dad-107">EXAMPLES</span></span>

### <span data-ttu-id="33dad-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="33dad-108">Example 1</span></span>
```
PS C:\> $subscriptionObj = Get-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1

PS C:\> $subscriptionObj.DeadLetteringOnMessageExpiration = $True
PS C:\> $subscriptionObj.MaxDeliveryCount = 9

PS C:\> Set-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionObj $subscriptionObj
```

<span data-ttu-id="33dad-109">Frissíti a megadott előfizetéshez tartozó leírást az adott témához.</span><span class="sxs-lookup"><span data-stu-id="33dad-109">Updates the description for the specified subscription to the given topic.</span></span> <span data-ttu-id="33dad-110">Ebben a példában a **DeadLetteringOnMessageExpiration** tulajdonságot a **true** értékre frissíti, a **MaxDeliveryCount** pedig a 9-es értékre.</span><span class="sxs-lookup"><span data-stu-id="33dad-110">This example updates the **DeadLetteringOnMessageExpiration** property to **true** and **MaxDeliveryCount** to 9.</span></span>

## <span data-ttu-id="33dad-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="33dad-111">PARAMETERS</span></span>

### <span data-ttu-id="33dad-112">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="33dad-112">-Confirm</span></span>
<span data-ttu-id="33dad-113">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="33dad-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33dad-114">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33dad-114">-WhatIf</span></span>
<span data-ttu-id="33dad-115">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="33dad-115">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33dad-116">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="33dad-116">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33dad-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33dad-117">-DefaultProfile</span></span>
<span data-ttu-id="33dad-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="33dad-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33dad-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="33dad-119">-InputObject</span></span>
<span data-ttu-id="33dad-120">ServiceBus-előfizetés definíciója</span><span class="sxs-lookup"><span data-stu-id="33dad-120">ServiceBus Subscription definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.SubscriptionAttributes
Parameter Sets: (All)
Aliases: SubscriptionObj

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33dad-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="33dad-121">-Namespace</span></span>
<span data-ttu-id="33dad-122">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="33dad-122">Namespace Name.</span></span>

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

### <span data-ttu-id="33dad-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33dad-123">-ResourceGroupName</span></span>
<span data-ttu-id="33dad-124">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="33dad-124">The name of the resource group</span></span>

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

### <span data-ttu-id="33dad-125">-Topic</span><span class="sxs-lookup"><span data-stu-id="33dad-125">-Topic</span></span>
<span data-ttu-id="33dad-126">A téma neve</span><span class="sxs-lookup"><span data-stu-id="33dad-126">Topic Name.</span></span>

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

### <span data-ttu-id="33dad-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33dad-127">CommonParameters</span></span>
<span data-ttu-id="33dad-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="33dad-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33dad-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33dad-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33dad-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="33dad-130">INPUTS</span></span>

### <span data-ttu-id="33dad-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="33dad-131">-ResourceGroup</span></span>
 <span data-ttu-id="33dad-132">System. String</span><span class="sxs-lookup"><span data-stu-id="33dad-132">System.String</span></span>

### <span data-ttu-id="33dad-133">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="33dad-133">-NamespaceName</span></span>
 <span data-ttu-id="33dad-134">System. String</span><span class="sxs-lookup"><span data-stu-id="33dad-134">System.String</span></span>

### <span data-ttu-id="33dad-135">-TopicName</span><span class="sxs-lookup"><span data-stu-id="33dad-135">-TopicName</span></span>
 <span data-ttu-id="33dad-136">System. String</span><span class="sxs-lookup"><span data-stu-id="33dad-136">System.String</span></span>

### <span data-ttu-id="33dad-137">-SubscriptionObj</span><span class="sxs-lookup"><span data-stu-id="33dad-137">-SubscriptionObj</span></span>
 <span data-ttu-id="33dad-138">Microsoft. Azure. Command. ServiceBus. models. SubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="33dad-138">Microsoft.Azure.Commands.ServiceBus.Models.SubscriptionAttributes</span></span>

## <span data-ttu-id="33dad-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="33dad-139">OUTPUTS</span></span>

### <span data-ttu-id="33dad-140">Microsoft. Azure. Command. ServiceBus. models. SubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="33dad-140">Microsoft.Azure.Commands.ServiceBus.Models.SubscriptionAttributes</span></span>
<span data-ttu-id="33dad-141">Név: SB-TopicSubscription-Example1: West US AccessedAt: 1/1/0001 12:00:00 AM AutoDeleteOnIdle: 10675199.02:48:05.4775807 CountDetails: CreatedAt: 1/20/2017 9:59:15 PM DefaultMessageTimeToLive: 10675199.02:48:05.4775807 DeadLetteringOnFilterEvaluationExceptions: true DeadLetteringOnMessageExpiration: true EnableBatchedOperations: true EntityAvailabilityStatus: true IsReadOnly: available LockDuration: MaxDeliveryCount: 00:01:00 MessageCount: 9 RequiresSession: 0 UpdatedAt: false Status: Active 1/20/2017 9:59:15:</span><span class="sxs-lookup"><span data-stu-id="33dad-141">Name                                      : SB-TopicSubscription-Example1 Location                                  : West US AccessedAt                                : 1/1/0001 12:00:00 AM AutoDeleteOnIdle                          : 10675199.02:48:05.4775807 CountDetails                              : CreatedAt                                 : 1/20/2017 9:59:15 PM DefaultMessageTimeToLive                  : 10675199.02:48:05.4775807 DeadLetteringOnFilterEvaluationExceptions : True DeadLetteringOnMessageExpiration          : True EnableBatchedOperations                   : True EntityAvailabilityStatus                  : Available IsReadOnly                                : LockDuration                              : 00:01:00 MaxDeliveryCount                          : 9 MessageCount                              : 0 RequiresSession                           : False Status                                    : Active UpdatedAt                                 : 1/20/2017 9:59:15 PM</span></span>

## <span data-ttu-id="33dad-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="33dad-142">NOTES</span></span>

## <span data-ttu-id="33dad-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="33dad-143">RELATED LINKS</span></span>

