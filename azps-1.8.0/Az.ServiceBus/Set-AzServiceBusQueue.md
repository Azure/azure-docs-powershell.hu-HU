---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusQueue.md
ms.openlocfilehash: 4206e29ad56e1d7b48b9d87a66b8a85960c4707e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669141"
---
# <span data-ttu-id="d1bd5-101">Set-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="d1bd5-101">Set-AzServiceBusQueue</span></span>

## <span data-ttu-id="d1bd5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d1bd5-102">SYNOPSIS</span></span>
<span data-ttu-id="d1bd5-103">Frissíti a szolgáltatás busz-várólistájának leírását a megadott Service Bus névtérben.</span><span class="sxs-lookup"><span data-stu-id="d1bd5-103">Updates the description of a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="d1bd5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d1bd5-104">SYNTAX</span></span>

```
Set-AzServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject] <PSQueueAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d1bd5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d1bd5-105">DESCRIPTION</span></span>
<span data-ttu-id="d1bd5-106">A **set-AzServiceBusQueue** parancsmag frissíti a szolgáltatás busz-várólistájának leírását a megadott Service Bus névtérben.</span><span class="sxs-lookup"><span data-stu-id="d1bd5-106">The **Set-AzServiceBusQueue** cmdlet updates the description for the Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="d1bd5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d1bd5-107">EXAMPLES</span></span>

### <span data-ttu-id="d1bd5-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d1bd5-108">Example 1</span></span>
```
PS C:\> $QueueObj = Get-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1

PS C:\> $QueueObj.DeadLetteringOnMessageExpiration = $True
PS C:\> $QueueObj.SupportOrdering = $True

PS C:\> Set-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1 -QueueObj $QueueObj

Id                                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroupName}/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/SB-Queue_exampl1
Name                                : SB-Queue_exampl1
LockDuration                        : PT1M
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : P10675199DT2H48M5.4775807S
CreatedAt                           : 1/1/0001 12:00:00 AM
DefaultMessageTimeToLive            : P10675199DT2H48M5.4775807S
DuplicateDetectionHistoryTimeWindow : PT10M
DeadLetteringOnMessageExpiration    : True
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
UpdatedAt                           : 1/1/0001 12:00:00 AM
ForwardTo                           :
ForwardDeadLetteredMessagesTo       :
EnableBatchedOperations             : False
```

<span data-ttu-id="d1bd5-109">Frissíti a megadott várólistát egy új leírással a megadott névtérben.</span><span class="sxs-lookup"><span data-stu-id="d1bd5-109">Updates the specified queue with a new description in the specified namespace.</span></span> <span data-ttu-id="d1bd5-110">Ez a példa frissíti a **DeadLetteringOnMessageExpiration** tulajdonságot **true** értékre, és a **SupportOrdering** **true** értékre.</span><span class="sxs-lookup"><span data-stu-id="d1bd5-110">This example updates the **DeadLetteringOnMessageExpiration** property to **true** and **SupportOrdering** to **true**.</span></span>

## <span data-ttu-id="d1bd5-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d1bd5-111">PARAMETERS</span></span>

### <span data-ttu-id="d1bd5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1bd5-112">-DefaultProfile</span></span>
<span data-ttu-id="d1bd5-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d1bd5-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1bd5-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d1bd5-114">-InputObject</span></span>
<span data-ttu-id="d1bd5-115">ServiceBus definíciója</span><span class="sxs-lookup"><span data-stu-id="d1bd5-115">ServiceBus definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes
Parameter Sets: (All)
Aliases: QueueObj

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1bd5-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d1bd5-116">-Name</span></span>
<span data-ttu-id="d1bd5-117">Várólista neve</span><span class="sxs-lookup"><span data-stu-id="d1bd5-117">Queue Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1bd5-118">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d1bd5-118">-Namespace</span></span>
<span data-ttu-id="d1bd5-119">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="d1bd5-119">Namespace Name.</span></span>

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

### <span data-ttu-id="d1bd5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1bd5-120">-ResourceGroupName</span></span>
<span data-ttu-id="d1bd5-121">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="d1bd5-121">The name of the resource group</span></span>

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

### <span data-ttu-id="d1bd5-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d1bd5-122">-Confirm</span></span>
<span data-ttu-id="d1bd5-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d1bd5-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1bd5-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1bd5-124">-WhatIf</span></span>
<span data-ttu-id="d1bd5-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d1bd5-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1bd5-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d1bd5-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1bd5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1bd5-127">CommonParameters</span></span>
<span data-ttu-id="d1bd5-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d1bd5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1bd5-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1bd5-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1bd5-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d1bd5-130">INPUTS</span></span>

### <span data-ttu-id="d1bd5-131">System. String</span><span class="sxs-lookup"><span data-stu-id="d1bd5-131">System.String</span></span>

### <span data-ttu-id="d1bd5-132">Microsoft. Azure. Command. ServiceBus. models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="d1bd5-132">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="d1bd5-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d1bd5-133">OUTPUTS</span></span>

### <span data-ttu-id="d1bd5-134">Microsoft. Azure. Command. ServiceBus. models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="d1bd5-134">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="d1bd5-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d1bd5-135">NOTES</span></span>

## <span data-ttu-id="d1bd5-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d1bd5-136">RELATED LINKS</span></span>
