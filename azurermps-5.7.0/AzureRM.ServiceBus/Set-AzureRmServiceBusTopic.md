---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusTopic.md
ms.openlocfilehash: 92c26b2b92257de7cdd3bbbb0d602d45d8ea1d1c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494335"
---
# <span data-ttu-id="ba4f2-101">Set-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="ba4f2-101">Set-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="ba4f2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ba4f2-102">SYNOPSIS</span></span>
<span data-ttu-id="ba4f2-103">A megadott szolgáltatási busz névtérben frissíti a szolgáltatás busz témakörének leírását.</span><span class="sxs-lookup"><span data-stu-id="ba4f2-103">Updates the description of a Service Bus topic in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba4f2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ba4f2-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject] <TopicAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ba4f2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ba4f2-105">DESCRIPTION</span></span>
<span data-ttu-id="ba4f2-106">A **set-AzureRmServiceBusTopic** parancsmag a megadott szolgáltatási busz névtérben frissíti a szolgáltatási busz témakör Leírás objektumát.</span><span class="sxs-lookup"><span data-stu-id="ba4f2-106">The **Set-AzureRmServiceBusTopic** cmdlet updates a description object for a Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="ba4f2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ba4f2-107">EXAMPLES</span></span>

### <span data-ttu-id="ba4f2-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ba4f2-108">Example 1</span></span>
```
PS C:\> $topicObj = Get-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1

PS C:\> $topicObj.EnableExpress = $True

PS C:\> Set-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -TopicObj $topicObj

Name                                : SB-Topic_exampl1
Id                                  : /subscriptions/{subscription id}d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-
                                      Topic_exampl1
Type                                : Microsoft.ServiceBus/Topic
AccessedAt                          : 1/20/2017 3:18:54 AM
AutoDeleteOnIdle                    : 10675199.02:48:05.4775807
CreatedAt                           : 1/20/2017 3:16:41 AM
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
DefaultMessageTimeToLive            : 10675199.02:48:05.4775807
DuplicateDetectionHistoryTimeWindow : 
EnableBatchedOperations             : True
EnableExpress                       : True
EnablePartitioning                  : True
MaxSizeInMegabytes                  : 16384
RequiresDuplicateDetection          : False
SizeInBytes                         : 0
Status                              : Active
SubscriptionCount                   : 1
SupportOrdering                     : False
UpdatedAt                           : 1/20/2017 7:12:16 PM
```
<span data-ttu-id="ba4f2-109">Frissíti a megadott témakört egy új leírással a megadott névtérben.</span><span class="sxs-lookup"><span data-stu-id="ba4f2-109">Updates the specified topic with a new description in the specified namespace.</span></span> <span data-ttu-id="ba4f2-110">Ez a példa frissíti a **EnableExpress** tulajdonságot **true** értékre.</span><span class="sxs-lookup"><span data-stu-id="ba4f2-110">This example updates the **EnableExpress** property to **true**.</span></span> 

## <span data-ttu-id="ba4f2-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ba4f2-111">PARAMETERS</span></span>

### <span data-ttu-id="ba4f2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba4f2-112">-DefaultProfile</span></span>
<span data-ttu-id="ba4f2-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ba4f2-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba4f2-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ba4f2-114">-InputObject</span></span>
<span data-ttu-id="ba4f2-115">A ServiceBus témakör definíciója.</span><span class="sxs-lookup"><span data-stu-id="ba4f2-115">ServiceBus Topic definition.</span></span>

```yaml
Type: PSTopicAttributes
Parameter Sets: (All)
Aliases: TopicObj

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba4f2-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ba4f2-116">-Name</span></span>
<span data-ttu-id="ba4f2-117">A téma neve</span><span class="sxs-lookup"><span data-stu-id="ba4f2-117">Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba4f2-118">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ba4f2-118">-Namespace</span></span>
<span data-ttu-id="ba4f2-119">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="ba4f2-119">Namespace Name.</span></span>

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

### <span data-ttu-id="ba4f2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba4f2-120">-ResourceGroupName</span></span>
<span data-ttu-id="ba4f2-121">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="ba4f2-121">The name of the resource group</span></span>

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

### <span data-ttu-id="ba4f2-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ba4f2-122">-Confirm</span></span>
<span data-ttu-id="ba4f2-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ba4f2-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba4f2-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba4f2-124">-WhatIf</span></span>
<span data-ttu-id="ba4f2-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ba4f2-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba4f2-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ba4f2-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba4f2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba4f2-127">CommonParameters</span></span>
<span data-ttu-id="ba4f2-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ba4f2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba4f2-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba4f2-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba4f2-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ba4f2-130">INPUTS</span></span>

### <span data-ttu-id="ba4f2-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ba4f2-131">-ResourceGroup</span></span>
 <span data-ttu-id="ba4f2-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ba4f2-132">System.String</span></span>

### <span data-ttu-id="ba4f2-133">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="ba4f2-133">-NamespaceName</span></span>
 <span data-ttu-id="ba4f2-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ba4f2-134">System.String</span></span>

### <span data-ttu-id="ba4f2-135">-TopicName</span><span class="sxs-lookup"><span data-stu-id="ba4f2-135">-TopicName</span></span>
 <span data-ttu-id="ba4f2-136">System. String</span><span class="sxs-lookup"><span data-stu-id="ba4f2-136">System.String</span></span>

### <span data-ttu-id="ba4f2-137">-TopicObj</span><span class="sxs-lookup"><span data-stu-id="ba4f2-137">-TopicObj</span></span>
 <span data-ttu-id="ba4f2-138">Microsoft. Azure. Command. ServiceBus. models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="ba4f2-138">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="ba4f2-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ba4f2-139">OUTPUTS</span></span>

### <span data-ttu-id="ba4f2-140">Microsoft. Azure. Command. ServiceBus. models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="ba4f2-140">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="ba4f2-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ba4f2-141">NOTES</span></span>

## <span data-ttu-id="ba4f2-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ba4f2-142">RELATED LINKS</span></span>

