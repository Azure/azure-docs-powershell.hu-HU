---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusQueue.md
ms.openlocfilehash: 785685981c38248fba944cc9e3809a2de1f32e71
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495253"
---
# <span data-ttu-id="6464f-101">Set-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="6464f-101">Set-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="6464f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6464f-102">SYNOPSIS</span></span>
<span data-ttu-id="6464f-103">Frissíti a szolgáltatás busz-várólistájának leírását a megadott Service Bus névtérben.</span><span class="sxs-lookup"><span data-stu-id="6464f-103">Updates the description of a Service Bus queue in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6464f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6464f-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject] <QueueAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6464f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6464f-105">DESCRIPTION</span></span>
<span data-ttu-id="6464f-106">A **set-AzureRmServiceBusQueue** parancsmag frissíti a szolgáltatás busz-várólistájának leírását a megadott Service Bus névtérben.</span><span class="sxs-lookup"><span data-stu-id="6464f-106">The **Set-AzureRmServiceBusQueue** cmdlet updates the description for the Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="6464f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6464f-107">EXAMPLES</span></span>

### <span data-ttu-id="6464f-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6464f-108">Example 1</span></span>
```
PS C:\> $QueueObj = Get-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1

PS C:\> $QueueObj.DeadLetteringOnMessageExpiration = $True
PS C:\> $QueueObj.SupportOrdering = $True

PS C:\> Set-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -QueueObj $QueueObj

Name                                : SB-Queue_exampl1
LockDuration                        : 
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : 10675199.02:48:05.4775807
CreatedAt                           : 1/20/2017 2:51:34 AM
DefaultMessageTimeToLive            : 10675199.02:48:05.4775807
DuplicateDetectionHistoryTimeWindow : 
DeadLetteringOnMessageExpiration    : False
EnableExpress                       : False
EnablePartitioning                  : True
MaxDeliveryCount                    : 
MaxSizeInMegabytes                  : 16384
MessageCount                        : 
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
RequiresDuplicateDetection          : False
RequiresSession                     : False
SizeInBytes                         : 
Status                              : Active
UpdatedAt                           : 1/20/2017 6:16:18 PM
```

<span data-ttu-id="6464f-109">Frissíti a megadott várólistát egy új leírással a megadott névtérben.</span><span class="sxs-lookup"><span data-stu-id="6464f-109">Updates the specified queue with a new description in the specified namespace.</span></span> <span data-ttu-id="6464f-110">Ez a példa frissíti a **DeadLetteringOnMessageExpiration** tulajdonságot **true** értékre, és a **SupportOrdering** **true** értékre.</span><span class="sxs-lookup"><span data-stu-id="6464f-110">This example updates the **DeadLetteringOnMessageExpiration** property to **true** and **SupportOrdering** to **true**.</span></span>

## <span data-ttu-id="6464f-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6464f-111">PARAMETERS</span></span>

### <span data-ttu-id="6464f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6464f-112">-DefaultProfile</span></span>
<span data-ttu-id="6464f-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6464f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6464f-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6464f-114">-InputObject</span></span>
<span data-ttu-id="6464f-115">ServiceBus definíciója</span><span class="sxs-lookup"><span data-stu-id="6464f-115">ServiceBus definition.</span></span>

```yaml
Type: PSQueueAttributes
Parameter Sets: (All)
Aliases: QueueObj

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6464f-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6464f-116">-Name</span></span>
<span data-ttu-id="6464f-117">Várólista neve</span><span class="sxs-lookup"><span data-stu-id="6464f-117">Queue Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6464f-118">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6464f-118">-Namespace</span></span>
<span data-ttu-id="6464f-119">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="6464f-119">Namespace Name.</span></span>

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

### <span data-ttu-id="6464f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6464f-120">-ResourceGroupName</span></span>
<span data-ttu-id="6464f-121">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="6464f-121">The name of the resource group</span></span>

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

### <span data-ttu-id="6464f-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6464f-122">-Confirm</span></span>
<span data-ttu-id="6464f-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6464f-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6464f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6464f-124">-WhatIf</span></span>
<span data-ttu-id="6464f-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6464f-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6464f-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6464f-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6464f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6464f-127">CommonParameters</span></span>
<span data-ttu-id="6464f-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6464f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6464f-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6464f-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6464f-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6464f-130">INPUTS</span></span>

### <span data-ttu-id="6464f-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6464f-131">-ResourceGroup</span></span>
 <span data-ttu-id="6464f-132">System. String</span><span class="sxs-lookup"><span data-stu-id="6464f-132">System.String</span></span>

### <span data-ttu-id="6464f-133">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="6464f-133">-NamespaceName</span></span>
 <span data-ttu-id="6464f-134">System. String</span><span class="sxs-lookup"><span data-stu-id="6464f-134">System.String</span></span>

### <span data-ttu-id="6464f-135">-QueueName</span><span class="sxs-lookup"><span data-stu-id="6464f-135">-QueueName</span></span>
 <span data-ttu-id="6464f-136">System. String</span><span class="sxs-lookup"><span data-stu-id="6464f-136">System.String</span></span>

### <span data-ttu-id="6464f-137">-QueueObj</span><span class="sxs-lookup"><span data-stu-id="6464f-137">-QueueObj</span></span>
 <span data-ttu-id="6464f-138">Microsoft. Azure. Command. ServiceBus. models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="6464f-138">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="6464f-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6464f-139">OUTPUTS</span></span>

### <span data-ttu-id="6464f-140">Microsoft. Azure. Command. ServiceBus. models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="6464f-140">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="6464f-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6464f-141">NOTES</span></span>

## <span data-ttu-id="6464f-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6464f-142">RELATED LINKS</span></span>

