---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/set-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusSubscription.md
ms.openlocfilehash: e19906f4a26f39929c62ffba89bd54092b4c961c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937353"
---
# <span data-ttu-id="e2d29-101">Set-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="e2d29-101">Set-AzServiceBusSubscription</span></span>

## <span data-ttu-id="e2d29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2d29-102">SYNOPSIS</span></span>
<span data-ttu-id="e2d29-103">Frissíti a Szolgáltatásbusz témakör előfizetési leírását a megadott Service Bus névterében.</span><span class="sxs-lookup"><span data-stu-id="e2d29-103">Updates a subscription description for a Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="e2d29-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e2d29-104">SYNTAX</span></span>

```
Set-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-InputObject] <PSSubscriptionAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e2d29-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e2d29-105">DESCRIPTION</span></span>
<span data-ttu-id="e2d29-106">A **Set-AzServiceBusSubscription** parancsmag frissíti a Service Bus témakör előfizetésének leírását a megadott Service Bus névterében.</span><span class="sxs-lookup"><span data-stu-id="e2d29-106">The **Set-AzServiceBusSubscription** cmdlet updates the description of the subscription for the Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="e2d29-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e2d29-107">EXAMPLES</span></span>

### <span data-ttu-id="e2d29-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="e2d29-108">Example 1</span></span>
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

<span data-ttu-id="e2d29-109">Frissíti a megadott előfizetés leírását a megadott témakörre.</span><span class="sxs-lookup"><span data-stu-id="e2d29-109">Updates the description for the specified subscription to the given topic.</span></span> <span data-ttu-id="e2d29-110">Ebben a példában **a DeadLetteringOnMessageExpiration** tulajdonságot **igaz,** **a MaxDeliveryCount** tulajdonságot pedig 9-re frissíti.</span><span class="sxs-lookup"><span data-stu-id="e2d29-110">This example updates the **DeadLetteringOnMessageExpiration** property to **true** and **MaxDeliveryCount** to 9.</span></span>

## <span data-ttu-id="e2d29-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e2d29-111">PARAMETERS</span></span>

### <span data-ttu-id="e2d29-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2d29-112">-DefaultProfile</span></span>
<span data-ttu-id="e2d29-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e2d29-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2d29-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2d29-114">-InputObject</span></span>
<span data-ttu-id="e2d29-115">ServiceBus-előfizetés definíciója.</span><span class="sxs-lookup"><span data-stu-id="e2d29-115">ServiceBus Subscription definition.</span></span>

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

### <span data-ttu-id="e2d29-116">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e2d29-116">-Namespace</span></span>
<span data-ttu-id="e2d29-117">Névtér neve.</span><span class="sxs-lookup"><span data-stu-id="e2d29-117">Namespace Name.</span></span>

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

### <span data-ttu-id="e2d29-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2d29-118">-ResourceGroupName</span></span>
<span data-ttu-id="e2d29-119">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="e2d29-119">The name of the resource group</span></span>

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

### <span data-ttu-id="e2d29-120">-Topic</span><span class="sxs-lookup"><span data-stu-id="e2d29-120">-Topic</span></span>
<span data-ttu-id="e2d29-121">Témakör neve.</span><span class="sxs-lookup"><span data-stu-id="e2d29-121">Topic Name.</span></span>

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

### <span data-ttu-id="e2d29-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e2d29-122">-Confirm</span></span>
<span data-ttu-id="e2d29-123">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e2d29-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2d29-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2d29-124">-WhatIf</span></span>
<span data-ttu-id="e2d29-125">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e2d29-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2d29-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e2d29-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2d29-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2d29-127">CommonParameters</span></span>
<span data-ttu-id="e2d29-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2d29-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2d29-129">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2d29-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2d29-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e2d29-130">INPUTS</span></span>

### <span data-ttu-id="e2d29-131">System.String</span><span class="sxs-lookup"><span data-stu-id="e2d29-131">System.String</span></span>

### <span data-ttu-id="e2d29-132">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="e2d29-132">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="e2d29-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e2d29-133">OUTPUTS</span></span>

### <span data-ttu-id="e2d29-134">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="e2d29-134">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="e2d29-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e2d29-135">NOTES</span></span>

## <span data-ttu-id="e2d29-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e2d29-136">RELATED LINKS</span></span>
