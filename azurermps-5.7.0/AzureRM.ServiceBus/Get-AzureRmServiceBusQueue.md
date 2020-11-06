---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueue.md
ms.openlocfilehash: 967bc5c3126a0976096b6c9d9b6b76af8f0ef43e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494339"
---
# <span data-ttu-id="51d31-101">Get-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="51d31-101">Get-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="51d31-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="51d31-102">SYNOPSIS</span></span>
<span data-ttu-id="51d31-103">A megadott szolgáltatás busz-várólistájának leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="51d31-103">Returns a description for the specified Service Bus queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51d31-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="51d31-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51d31-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="51d31-105">DESCRIPTION</span></span>
<span data-ttu-id="51d31-106">A **Get-AzureRmServiceBusQueue** parancsmag a megadott szolgáltatási busz várólistájának leírását adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="51d31-106">The **Get-AzureRmServiceBusQueue** cmdlet returns a description of the specified Service Bus queue.</span></span>

## <span data-ttu-id="51d31-107">Példák</span><span class="sxs-lookup"><span data-stu-id="51d31-107">EXAMPLES</span></span>

### <span data-ttu-id="51d31-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="51d31-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1

LockDuration                        : 
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : 10675199.02:48:05.4775807
CreatedAt                           : 1/20/2017 2:51:35 AM
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
UpdatedAt                           : 1/20/2017 2:51:37 AM
Id                                  : /subscriptions/{subscription id}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/S
                                      B-Queue_example1
Name                                : SB-Queue_example1
Type                                : Microsoft.ServiceBus/Queues

```

<span data-ttu-id="51d31-109">A várólista leírását számítja ki.</span><span class="sxs-lookup"><span data-stu-id="51d31-109">Returns the description of the queue.</span></span>

## <span data-ttu-id="51d31-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="51d31-110">PARAMETERS</span></span>

### <span data-ttu-id="51d31-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51d31-111">-DefaultProfile</span></span>
<span data-ttu-id="51d31-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="51d31-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51d31-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="51d31-113">-Name</span></span>
<span data-ttu-id="51d31-114">Várólista neve</span><span class="sxs-lookup"><span data-stu-id="51d31-114">Queue Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: QueueName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51d31-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="51d31-115">-Namespace</span></span>
<span data-ttu-id="51d31-116">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="51d31-116">Namespace Name.</span></span>

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

### <span data-ttu-id="51d31-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51d31-117">-ResourceGroupName</span></span>
<span data-ttu-id="51d31-118">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="51d31-118">The name of the resource group</span></span>

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

### <span data-ttu-id="51d31-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51d31-119">CommonParameters</span></span>
<span data-ttu-id="51d31-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="51d31-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51d31-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51d31-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51d31-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="51d31-122">INPUTS</span></span>

### <span data-ttu-id="51d31-123">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="51d31-123">-ResourceGroup</span></span>
 <span data-ttu-id="51d31-124">System. String</span><span class="sxs-lookup"><span data-stu-id="51d31-124">System.String</span></span>
 

### <span data-ttu-id="51d31-125">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="51d31-125">-NamespaceName</span></span>
 <span data-ttu-id="51d31-126">System. String</span><span class="sxs-lookup"><span data-stu-id="51d31-126">System.String</span></span>
 

### <span data-ttu-id="51d31-127">-QueueName</span><span class="sxs-lookup"><span data-stu-id="51d31-127">-QueueName</span></span>
 <span data-ttu-id="51d31-128">System. String</span><span class="sxs-lookup"><span data-stu-id="51d31-128">System.String</span></span> 

## <span data-ttu-id="51d31-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="51d31-129">OUTPUTS</span></span>

### <span data-ttu-id="51d31-130">Microsoft. Azure. Command. ServiceBus. models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="51d31-130">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="51d31-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="51d31-131">NOTES</span></span>

## <span data-ttu-id="51d31-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="51d31-132">RELATED LINKS</span></span>

