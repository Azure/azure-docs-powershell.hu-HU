---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueue.md
ms.openlocfilehash: d90d93548e46f3586319b0acf96319fe24e298af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503959"
---
# <span data-ttu-id="92365-101">Get-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="92365-101">Get-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="92365-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="92365-102">SYNOPSIS</span></span>
<span data-ttu-id="92365-103">A megadott szolgáltatás busz-várólistájának leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="92365-103">Returns a description for the specified Service Bus queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92365-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="92365-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusQueue -ResourceGroupName <String> -Namespace <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92365-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="92365-105">DESCRIPTION</span></span>
<span data-ttu-id="92365-106">A **Get-AzureRmServiceBusQueue** parancsmag a megadott szolgáltatási busz várólistájának leírását adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="92365-106">The **Get-AzureRmServiceBusQueue** cmdlet returns a description of the specified Service Bus queue.</span></span>

## <span data-ttu-id="92365-107">Példák</span><span class="sxs-lookup"><span data-stu-id="92365-107">EXAMPLES</span></span>

### <span data-ttu-id="92365-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="92365-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1
```

<span data-ttu-id="92365-109">A várólista leírását számítja ki.</span><span class="sxs-lookup"><span data-stu-id="92365-109">Returns the description of the queue.</span></span> 

## <span data-ttu-id="92365-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="92365-110">PARAMETERS</span></span>

### <span data-ttu-id="92365-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92365-111">-DefaultProfile</span></span>
<span data-ttu-id="92365-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="92365-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92365-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="92365-113">-Name</span></span>
<span data-ttu-id="92365-114">Várólista neve</span><span class="sxs-lookup"><span data-stu-id="92365-114">Queue Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92365-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="92365-115">-Namespace</span></span>
<span data-ttu-id="92365-116">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="92365-116">Namespace Name.</span></span>

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

### <span data-ttu-id="92365-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92365-117">-ResourceGroupName</span></span>
<span data-ttu-id="92365-118">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="92365-118">The name of the resource group</span></span>

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

### <span data-ttu-id="92365-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92365-119">CommonParameters</span></span>
<span data-ttu-id="92365-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="92365-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92365-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92365-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92365-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="92365-122">INPUTS</span></span>

### <span data-ttu-id="92365-123">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="92365-123">-ResourceGroup</span></span>
 <span data-ttu-id="92365-124">System. String</span><span class="sxs-lookup"><span data-stu-id="92365-124">System.String</span></span>
 

### <span data-ttu-id="92365-125">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="92365-125">-NamespaceName</span></span>
 <span data-ttu-id="92365-126">System. String</span><span class="sxs-lookup"><span data-stu-id="92365-126">System.String</span></span>
 

### <span data-ttu-id="92365-127">-QueueName</span><span class="sxs-lookup"><span data-stu-id="92365-127">-QueueName</span></span>
 <span data-ttu-id="92365-128">System. String</span><span class="sxs-lookup"><span data-stu-id="92365-128">System.String</span></span> 

## <span data-ttu-id="92365-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="92365-129">OUTPUTS</span></span>

### <span data-ttu-id="92365-130">Microsoft. Azure. Command. ServiceBus. models. QueueAttributes</span><span class="sxs-lookup"><span data-stu-id="92365-130">Microsoft.Azure.Commands.ServiceBus.Models.QueueAttributes</span></span>
<span data-ttu-id="92365-131">LockDuration: AccessedAt: 1/1/0001 12:00:00 AM AutoDeleteOnIdle: 10675199.02:48:05.4775807 EntityAvailabilityStatus: CreatedAt: 1/20/2017 2:51:35 AM DefaultMessageTimeToLive: 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow: EnableBatchedOperations: true DeadLetteringOnMessageExpiration: false EnableExpress: false EnablePartitioning: true IsAnonymousAccessible: true MaxDeliveryCount: false MaxSizeInMegabytes: MessageCount: 16384 CountDetails: ServiceBus: Microsoft. Azure. Management. MessageCountDetails. models. RequiresDuplicateDetection. RequiresSession. SizeInBytes: false SupportOrdering: false UpdatedAt:/Subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/default-ServiceBus-WestUS/Providers/Microsoft.ServiceBus/Namespaces/SB-example1/Queues/S: Active ServiceBus: FALSE: 1/20/2017 2:51:37 am Id: SB-Queue_example1 Queue_example1</span><span class="sxs-lookup"><span data-stu-id="92365-131">LockDuration                        : AccessedAt                          : 1/1/0001 12:00:00 AM AutoDeleteOnIdle                    : 10675199.02:48:05.4775807 EntityAvailabilityStatus            : CreatedAt                           : 1/20/2017 2:51:35 AM DefaultMessageTimeToLive            : 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow : EnableBatchedOperations             : True DeadLetteringOnMessageExpiration    : False EnableExpress                       : False EnablePartitioning                  : True IsAnonymousAccessible               : False MaxDeliveryCount                    : MaxSizeInMegabytes                  : 16384 MessageCount                        : CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails RequiresDuplicateDetection          : False RequiresSession                     : False SizeInBytes                         : Status                              : Active SupportOrdering                     : False UpdatedAt                           : 1/20/2017 2:51:37 AM Id                                  : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/S B-Queue_example1 Name                                : SB-Queue_example1 Type                                : Microsoft.ServiceBus/Queues Location                            : West US</span></span>

## <span data-ttu-id="92365-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="92365-132">NOTES</span></span>

## <span data-ttu-id="92365-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="92365-133">RELATED LINKS</span></span>

