---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusSubscription.md
ms.openlocfilehash: 2bff80a8f04dada3625eaa5b0a16287bb37c6a13
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194852"
---
# <span data-ttu-id="f29f8-101">Set-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="f29f8-101">Set-AzServiceBusSubscription</span></span>

## <span data-ttu-id="f29f8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f29f8-102">SYNOPSIS</span></span>
<span data-ttu-id="f29f8-103">Az előfizetések leírását frissíti a megadott szolgáltatási busz névtérben lévő buszjáratok témakörében.</span><span class="sxs-lookup"><span data-stu-id="f29f8-103">Updates a subscription description for a Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="f29f8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f29f8-104">SYNTAX</span></span>

```
Set-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-InputObject] <PSSubscriptionAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f29f8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f29f8-105">DESCRIPTION</span></span>
<span data-ttu-id="f29f8-106">A **set-AzServiceBusSubscription** parancsmag frissíti a megadott Service Bus-névtérben a szolgáltatás buszjának előfizetése leírását.</span><span class="sxs-lookup"><span data-stu-id="f29f8-106">The **Set-AzServiceBusSubscription** cmdlet updates the description of the subscription for the Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="f29f8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f29f8-107">EXAMPLES</span></span>

### <span data-ttu-id="f29f8-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f29f8-108">Example 1</span></span>
```
PS C:\> $subscriptionObj = Get-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1

PS C:\> $subscriptionObj.DeadLetteringOnMessageExpiration = $True
PS C:\> $subscriptionObj.MaxDeliveryCount = 9

Name                                      : SB-TopicSubscription-Example1
AccessedAt                                : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                          : 10675199.02:48:05.4775807
CountDetails                              : 
CreatedAt                                 : 1/20/2017 9:59:15 PM
DefaultMessageTimeToLive                  : 10675199.02:48:05.4775807
DeadLetteringOnMessageExpiration          : True
EnableBatchedOperations                   : True
LockDuration                              : 00:01:00
MaxDeliveryCount                          : 9
MessageCount                              : 0
RequiresSession                           : False
Status                                    : Active
UpdatedAt                                 : 1/20/2017 9:59:15 PM
PS C:\> Set-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionObj $subscriptionObj
```

<span data-ttu-id="f29f8-109">Frissíti a megadott előfizetéshez tartozó leírást az adott témához.</span><span class="sxs-lookup"><span data-stu-id="f29f8-109">Updates the description for the specified subscription to the given topic.</span></span> <span data-ttu-id="f29f8-110">Ebben a példában a **DeadLetteringOnMessageExpiration** tulajdonságot a **true** értékre frissíti, a **MaxDeliveryCount** pedig a 9-es értékre.</span><span class="sxs-lookup"><span data-stu-id="f29f8-110">This example updates the **DeadLetteringOnMessageExpiration** property to **true** and **MaxDeliveryCount** to 9.</span></span>

## <span data-ttu-id="f29f8-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f29f8-111">PARAMETERS</span></span>

### <span data-ttu-id="f29f8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f29f8-112">-DefaultProfile</span></span>
<span data-ttu-id="f29f8-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f29f8-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f29f8-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f29f8-114">-InputObject</span></span>
<span data-ttu-id="f29f8-115">ServiceBus-előfizetés definíciója</span><span class="sxs-lookup"><span data-stu-id="f29f8-115">ServiceBus Subscription definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes
Parameter Sets: (All)
Aliases: SubscriptionObj

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f29f8-116">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f29f8-116">-Namespace</span></span>
<span data-ttu-id="f29f8-117">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="f29f8-117">Namespace Name.</span></span>

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

### <span data-ttu-id="f29f8-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f29f8-118">-ResourceGroupName</span></span>
<span data-ttu-id="f29f8-119">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="f29f8-119">The name of the resource group</span></span>

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

### <span data-ttu-id="f29f8-120">-Topic</span><span class="sxs-lookup"><span data-stu-id="f29f8-120">-Topic</span></span>
<span data-ttu-id="f29f8-121">A téma neve</span><span class="sxs-lookup"><span data-stu-id="f29f8-121">Topic Name.</span></span>

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

### <span data-ttu-id="f29f8-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f29f8-122">-Confirm</span></span>
<span data-ttu-id="f29f8-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f29f8-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f29f8-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f29f8-124">-WhatIf</span></span>
<span data-ttu-id="f29f8-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f29f8-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f29f8-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f29f8-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f29f8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f29f8-127">CommonParameters</span></span>
<span data-ttu-id="f29f8-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f29f8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f29f8-129">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f29f8-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f29f8-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f29f8-130">INPUTS</span></span>

### <span data-ttu-id="f29f8-131">System. String</span><span class="sxs-lookup"><span data-stu-id="f29f8-131">System.String</span></span>

### <span data-ttu-id="f29f8-132">Microsoft. Azure. Command. ServiceBus. models. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="f29f8-132">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="f29f8-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f29f8-133">OUTPUTS</span></span>

### <span data-ttu-id="f29f8-134">Microsoft. Azure. Command. ServiceBus. models. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="f29f8-134">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="f29f8-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f29f8-135">NOTES</span></span>

## <span data-ttu-id="f29f8-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f29f8-136">RELATED LINKS</span></span>