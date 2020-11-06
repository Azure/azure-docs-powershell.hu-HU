---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusQueue.md
ms.openlocfilehash: cd291e6c33dd08668c7a78f2c739f65c576e2f0d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503943"
---
# <span data-ttu-id="14b5f-101">Set-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="14b5f-101">Set-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="14b5f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="14b5f-102">SYNOPSIS</span></span>
<span data-ttu-id="14b5f-103">Frissíti a szolgáltatás busz-várólistájának leírását a megadott Service Bus névtérben.</span><span class="sxs-lookup"><span data-stu-id="14b5f-103">Updates the description of a Service Bus queue in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14b5f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="14b5f-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusQueue -ResourceGroupName <String> -Namespace <String> -Name <String>
 -InputObject <QueueAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="14b5f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="14b5f-105">DESCRIPTION</span></span>
<span data-ttu-id="14b5f-106">A **set-AzureRmServiceBusQueue** parancsmag frissíti a szolgáltatás busz-várólistájának leírását a megadott Service Bus névtérben.</span><span class="sxs-lookup"><span data-stu-id="14b5f-106">The **Set-AzureRmServiceBusQueue** cmdlet updates the description for the Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="14b5f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="14b5f-107">EXAMPLES</span></span>

### <span data-ttu-id="14b5f-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="14b5f-108">Example 1</span></span>
```
PS C:\> $QueueObj = Get-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1

PS C:\> $QueueObj.DeadLetteringOnMessageExpiration = $True
PS C:\> $QueueObj.SupportOrdering = $True

PS C:\> Set-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -QueueObj $QueueObj
```

<span data-ttu-id="14b5f-109">Frissíti a megadott várólistát egy új leírással a megadott névtérben.</span><span class="sxs-lookup"><span data-stu-id="14b5f-109">Updates the specified queue with a new description in the specified namespace.</span></span> <span data-ttu-id="14b5f-110">Ez a példa frissíti a **DeadLetteringOnMessageExpiration** tulajdonságot **true** értékre, és a **SupportOrdering** **true** értékre.</span><span class="sxs-lookup"><span data-stu-id="14b5f-110">This example updates the **DeadLetteringOnMessageExpiration** property to **true** and **SupportOrdering** to **true**.</span></span>

## <span data-ttu-id="14b5f-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="14b5f-111">PARAMETERS</span></span>

### <span data-ttu-id="14b5f-112">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="14b5f-112">-Confirm</span></span>
<span data-ttu-id="14b5f-113">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="14b5f-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14b5f-114">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14b5f-114">-WhatIf</span></span>
<span data-ttu-id="14b5f-115">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="14b5f-115">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14b5f-116">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="14b5f-116">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14b5f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14b5f-117">-DefaultProfile</span></span>
<span data-ttu-id="14b5f-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="14b5f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14b5f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="14b5f-119">-InputObject</span></span>
<span data-ttu-id="14b5f-120">ServiceBus definíciója</span><span class="sxs-lookup"><span data-stu-id="14b5f-120">ServiceBus definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.QueueAttributes
Parameter Sets: (All)
Aliases: QueueObj

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14b5f-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="14b5f-121">-Name</span></span>
<span data-ttu-id="14b5f-122">Várólista neve</span><span class="sxs-lookup"><span data-stu-id="14b5f-122">Queue Name.</span></span>

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

### <span data-ttu-id="14b5f-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="14b5f-123">-Namespace</span></span>
<span data-ttu-id="14b5f-124">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="14b5f-124">Namespace Name.</span></span>

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

### <span data-ttu-id="14b5f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14b5f-125">-ResourceGroupName</span></span>
<span data-ttu-id="14b5f-126">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="14b5f-126">The name of the resource group</span></span>

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

### <span data-ttu-id="14b5f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14b5f-127">CommonParameters</span></span>
<span data-ttu-id="14b5f-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="14b5f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14b5f-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14b5f-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14b5f-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="14b5f-130">INPUTS</span></span>

### <span data-ttu-id="14b5f-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="14b5f-131">-ResourceGroup</span></span>
 <span data-ttu-id="14b5f-132">System. String</span><span class="sxs-lookup"><span data-stu-id="14b5f-132">System.String</span></span>

### <span data-ttu-id="14b5f-133">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="14b5f-133">-NamespaceName</span></span>
 <span data-ttu-id="14b5f-134">System. String</span><span class="sxs-lookup"><span data-stu-id="14b5f-134">System.String</span></span>

### <span data-ttu-id="14b5f-135">-QueueName</span><span class="sxs-lookup"><span data-stu-id="14b5f-135">-QueueName</span></span>
 <span data-ttu-id="14b5f-136">System. String</span><span class="sxs-lookup"><span data-stu-id="14b5f-136">System.String</span></span>

### <span data-ttu-id="14b5f-137">-QueueObj</span><span class="sxs-lookup"><span data-stu-id="14b5f-137">-QueueObj</span></span>
 <span data-ttu-id="14b5f-138">Microsoft. Azure. Command. ServiceBus. models. QueueAttributes</span><span class="sxs-lookup"><span data-stu-id="14b5f-138">Microsoft.Azure.Commands.ServiceBus.Models.QueueAttributes</span></span>

## <span data-ttu-id="14b5f-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="14b5f-139">OUTPUTS</span></span>

### <span data-ttu-id="14b5f-140">Microsoft. Azure. Command. ServiceBus. models. QueueAttributes</span><span class="sxs-lookup"><span data-stu-id="14b5f-140">Microsoft.Azure.Commands.ServiceBus.Models.QueueAttributes</span></span>
<span data-ttu-id="14b5f-141">Név: SB-Queue_exampl1 hely: West US LockDuration: AccessedAt: 1/1/0001 12:00:00 AM AutoDeleteOnIdle: 10675199.02:48:05.4775807 EntityAvailabilityStatus: CreatedAt: 1/20/2017 2:51:34-es DefaultMessageTimeToLive: 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow: EnableBatchedOperations: true DeadLetteringOnMessageExpiration: false EnableExpress: false EnablePartitioning: false IsAnonymousAccessible: true MaxDeliveryCount: true MaxSizeInMegabytes: false MessageCount: CountDetails: ServiceBus: MessageCountDetails:. RequiresDuplicateDetection. RequiresSession. 16384 SizeInBytes. SupportOrdering. UpdatedAt: FALSE: FALSE:: Active: false 1/20/2017 6:16:18</span><span class="sxs-lookup"><span data-stu-id="14b5f-141">Name                                : SB-Queue_exampl1 Location                            : West US LockDuration                        : AccessedAt                          : 1/1/0001 12:00:00 AM AutoDeleteOnIdle                    : 10675199.02:48:05.4775807 EntityAvailabilityStatus            : CreatedAt                           : 1/20/2017 2:51:34 AM DefaultMessageTimeToLive            : 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow : EnableBatchedOperations             : True DeadLetteringOnMessageExpiration    : False EnableExpress                       : False EnablePartitioning                  : True IsAnonymousAccessible               : False MaxDeliveryCount                    : MaxSizeInMegabytes                  : 16384 MessageCount                        : CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails RequiresDuplicateDetection          : False RequiresSession                     : False SizeInBytes                         : Status                              : Active SupportOrdering                     : False UpdatedAt                           : 1/20/2017 6:16:18 PM</span></span>

## <span data-ttu-id="14b5f-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="14b5f-142">NOTES</span></span>

## <span data-ttu-id="14b5f-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="14b5f-143">RELATED LINKS</span></span>

