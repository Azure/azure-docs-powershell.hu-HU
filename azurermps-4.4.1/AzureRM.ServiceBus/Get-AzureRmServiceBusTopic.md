---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopic.md
ms.openlocfilehash: 273a8ec4bcbf5ffcc7619d3fe663d6256e4851d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493363"
---
# <span data-ttu-id="fc244-101">Get-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="fc244-101">Get-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="fc244-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fc244-102">SYNOPSIS</span></span>
<span data-ttu-id="fc244-103">A megadott szolgáltatási busz témakör leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="fc244-103">Returns a description for the specified Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc244-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fc244-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusTopic -ResourceGroupName <String> -Namespace <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc244-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fc244-105">DESCRIPTION</span></span>
<span data-ttu-id="fc244-106">A **Get-AzureRmServiceBusTopic** parancsmag a megadott szolgáltatási busz névterének leírását adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="fc244-106">The **Get-AzureRmServiceBusTopic** cmdlet returns a topic description for the specified Service Bus namespace.</span></span>

## <span data-ttu-id="fc244-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fc244-107">EXAMPLES</span></span>

### <span data-ttu-id="fc244-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fc244-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="fc244-109">A megadott, a szolgáltatás busz névteréhez tartozó témakör leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="fc244-109">Returns the description of the specified topic for the given Service Bus namespace.</span></span>

## <span data-ttu-id="fc244-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fc244-110">PARAMETERS</span></span>

### <span data-ttu-id="fc244-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc244-111">-DefaultProfile</span></span>
<span data-ttu-id="fc244-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fc244-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc244-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fc244-113">-Name</span></span>
<span data-ttu-id="fc244-114">A téma neve</span><span class="sxs-lookup"><span data-stu-id="fc244-114">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc244-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="fc244-115">-Namespace</span></span>
<span data-ttu-id="fc244-116">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="fc244-116">Namespace Name.</span></span>

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

### <span data-ttu-id="fc244-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc244-117">-ResourceGroupName</span></span>
<span data-ttu-id="fc244-118">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="fc244-118">The name of the resource group</span></span>

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

### <span data-ttu-id="fc244-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc244-119">CommonParameters</span></span>
<span data-ttu-id="fc244-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fc244-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc244-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc244-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc244-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc244-122">INPUTS</span></span>

### <span data-ttu-id="fc244-123">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="fc244-123">-ResourceGroup</span></span>
 <span data-ttu-id="fc244-124">System. String</span><span class="sxs-lookup"><span data-stu-id="fc244-124">System.String</span></span>
 

### <span data-ttu-id="fc244-125">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="fc244-125">-NamespaceName</span></span>
 <span data-ttu-id="fc244-126">System. String</span><span class="sxs-lookup"><span data-stu-id="fc244-126">System.String</span></span>
 

### <span data-ttu-id="fc244-127">-TopicName</span><span class="sxs-lookup"><span data-stu-id="fc244-127">-TopicName</span></span>
 <span data-ttu-id="fc244-128">System. String</span><span class="sxs-lookup"><span data-stu-id="fc244-128">System.String</span></span>

## <span data-ttu-id="fc244-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc244-129">OUTPUTS</span></span>

### <span data-ttu-id="fc244-130">Microsoft. Azure. Command. ServiceBus. models. TopicAttributes</span><span class="sxs-lookup"><span data-stu-id="fc244-130">Microsoft.Azure.Commands.ServiceBus.Models.TopicAttributes</span></span>
<span data-ttu-id="fc244-131">Név: SB-Topic_exampl1 hely: Nyugat-amerikai azonosító:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/S B-Topic_exampl1 típusa: Microsoft. ServiceBus/topic AccessedAt: 1/20/2017 3:18:54 AM AutoDeleteOnIdle: 10675199.02:48:05.4775807 EntityAvailabilityStatus: CreatedAt: 1/20/2017 3:16:41 AM CountDetails: Microsoft. Azure. Management. ServiceBus. models. MessageCountDetails DefaultMessageTimeToLive: 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow: EnableBatchedOperations: true EnableExpress: false EnablePartitioning: true EnableSubscriptionPartitioning: false FilteringMessagesBeforePublishing: false IsAnonymousAccessible: false IsExpress: false MaxSizeInMegabytes: false RequiresDuplicateDetection: 16384 SizeInBytes: false SubscriptionCount: 0 Status: Active SupportOrdering: 1 UpdatedAt: FALSE: 1/20/2017 3:16:43</span><span class="sxs-lookup"><span data-stu-id="fc244-131">Name                                : SB-Topic_exampl1 Location                            : West US Id                                  : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/S B-Topic_exampl1 Type                                : Microsoft.ServiceBus/Topic AccessedAt                          : 1/20/2017 3:18:54 AM AutoDeleteOnIdle                    : 10675199.02:48:05.4775807 EntityAvailabilityStatus            : CreatedAt                           : 1/20/2017 3:16:41 AM CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails DefaultMessageTimeToLive            : 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow : EnableBatchedOperations             : True EnableExpress                       : False EnablePartitioning                  : True EnableSubscriptionPartitioning      : False FilteringMessagesBeforePublishing   : False IsAnonymousAccessible               : False IsExpress                           : False MaxSizeInMegabytes                  : 16384 RequiresDuplicateDetection          : False SizeInBytes                         : 0 Status                              : Active SubscriptionCount                   : 1 SupportOrdering                     : False UpdatedAt                           : 1/20/2017 3:16:43 AM</span></span>

## <span data-ttu-id="fc244-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fc244-132">NOTES</span></span>

## <span data-ttu-id="fc244-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fc244-133">RELATED LINKS</span></span>

