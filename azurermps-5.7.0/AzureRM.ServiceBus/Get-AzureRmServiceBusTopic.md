---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopic.md
ms.openlocfilehash: 56f41802687938bf7575049eadc59ab7b049ac2e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679701"
---
# <span data-ttu-id="06c34-101">Get-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="06c34-101">Get-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="06c34-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="06c34-102">SYNOPSIS</span></span>
<span data-ttu-id="06c34-103">A megadott szolgáltatási busz témakör leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="06c34-103">Returns a description for the specified Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06c34-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="06c34-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06c34-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="06c34-105">DESCRIPTION</span></span>
<span data-ttu-id="06c34-106">A **Get-AzureRmServiceBusTopic** parancsmag a megadott szolgáltatási busz névterének leírását adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="06c34-106">The **Get-AzureRmServiceBusTopic** cmdlet returns a topic description for the specified Service Bus namespace.</span></span>

## <span data-ttu-id="06c34-107">Példák</span><span class="sxs-lookup"><span data-stu-id="06c34-107">EXAMPLES</span></span>

### <span data-ttu-id="06c34-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="06c34-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1

Name                                : SB-Topic_exampl1
Id                                  : /subscriptions/{subscription id}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/S
                                      B-Topic_exampl1
Type                                : Microsoft.ServiceBus/Topic
AccessedAt                          : 1/20/2017 3:18:54 AM
AutoDeleteOnIdle                    : 10675199.02:48:05.4775807
CreatedAt                           : 1/20/2017 3:16:41 AM
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
DefaultMessageTimeToLive            : 10675199.02:48:05.4775807
DuplicateDetectionHistoryTimeWindow : 
EnableBatchedOperations             : True
EnableExpress                       : False
EnablePartitioning                  : True
MaxSizeInMegabytes                  : 16384
RequiresDuplicateDetection          : False
SizeInBytes                         : 0
Status                              : Active
SubscriptionCount                   : 1
SupportOrdering                     : False
UpdatedAt                           : 1/20/2017 3:16:43 AM
```
<span data-ttu-id="06c34-109">A megadott, a szolgáltatás busz névteréhez tartozó témakör leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="06c34-109">Returns the description of the specified topic for the given Service Bus namespace.</span></span>

## <span data-ttu-id="06c34-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="06c34-110">PARAMETERS</span></span>

### <span data-ttu-id="06c34-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06c34-111">-DefaultProfile</span></span>
<span data-ttu-id="06c34-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="06c34-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06c34-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="06c34-113">-Name</span></span>
<span data-ttu-id="06c34-114">A téma neve</span><span class="sxs-lookup"><span data-stu-id="06c34-114">Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TopicName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06c34-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="06c34-115">-Namespace</span></span>
<span data-ttu-id="06c34-116">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="06c34-116">Namespace Name.</span></span>

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

### <span data-ttu-id="06c34-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06c34-117">-ResourceGroupName</span></span>
<span data-ttu-id="06c34-118">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="06c34-118">The name of the resource group</span></span>

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

### <span data-ttu-id="06c34-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06c34-119">CommonParameters</span></span>
<span data-ttu-id="06c34-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="06c34-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06c34-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06c34-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06c34-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="06c34-122">INPUTS</span></span>

### <span data-ttu-id="06c34-123">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="06c34-123">-ResourceGroup</span></span>
 <span data-ttu-id="06c34-124">System. String</span><span class="sxs-lookup"><span data-stu-id="06c34-124">System.String</span></span>
 

### <span data-ttu-id="06c34-125">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="06c34-125">-NamespaceName</span></span>
 <span data-ttu-id="06c34-126">System. String</span><span class="sxs-lookup"><span data-stu-id="06c34-126">System.String</span></span>
 

### <span data-ttu-id="06c34-127">-TopicName</span><span class="sxs-lookup"><span data-stu-id="06c34-127">-TopicName</span></span>
 <span data-ttu-id="06c34-128">System. String</span><span class="sxs-lookup"><span data-stu-id="06c34-128">System.String</span></span>

## <span data-ttu-id="06c34-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="06c34-129">OUTPUTS</span></span>

### <span data-ttu-id="06c34-130">Microsoft. Azure. Command. ServiceBus. models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="06c34-130">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="06c34-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="06c34-131">NOTES</span></span>

## <span data-ttu-id="06c34-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="06c34-132">RELATED LINKS</span></span>

