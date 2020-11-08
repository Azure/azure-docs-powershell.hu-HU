---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusTopic.md
ms.openlocfilehash: 8e8fe04476e66db6b45372879ac3176f9d492acc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014304"
---
# <span data-ttu-id="8464e-101">Set-AzServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="8464e-101">Set-AzServiceBusTopic</span></span>

## <span data-ttu-id="8464e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8464e-102">SYNOPSIS</span></span>
<span data-ttu-id="8464e-103">A megadott szolgáltatási busz névtérben frissíti a szolgáltatás busz témakörének leírását.</span><span class="sxs-lookup"><span data-stu-id="8464e-103">Updates the description of a Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="8464e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8464e-104">SYNTAX</span></span>

```
Set-AzServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject] <PSTopicAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8464e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8464e-105">DESCRIPTION</span></span>
<span data-ttu-id="8464e-106">A **set-AzServiceBusTopic** parancsmag a megadott szolgáltatási busz névtérben frissíti a szolgáltatási busz témakör Leírás objektumát.</span><span class="sxs-lookup"><span data-stu-id="8464e-106">The **Set-AzServiceBusTopic** cmdlet updates a description object for a Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="8464e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8464e-107">EXAMPLES</span></span>

### <span data-ttu-id="8464e-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8464e-108">Example 1</span></span>
```
PS C:\> $topicObj = Get-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-ExampleStandard -TopicName SB-Topic_exampl1

PS C:\> $topicObj.EnableExpress = $True

PS C:\> Set-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-ExampleStandard -TopicName SB-Topic_exampl1 -TopicObj $topicObj

Name                                : SB-Topic_example1
Id                                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroupName}/providers/Microsoft.ServiceBus/namespaces/SB-ExampleStandard/topics/SB-Topic_example1
Type                                : Microsoft.ServiceBus/Namespaces/Topics
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : P10675199DT2H48M5.4775807S
CreatedAt                           : 10/12/2018 12:01:28 AM
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
DefaultMessageTimeToLive            : P10675199DT2H48M5.4775807S
DuplicateDetectionHistoryTimeWindow : PT10M
EnableBatchedOperations             : True
EnableExpress                       : False
EnablePartitioning                  : True
MaxSizeInMegabytes                  : 81920
RequiresDuplicateDetection          : False
SizeInBytes                         : 0
Status                              : Active
SubscriptionCount                   : 0
SupportOrdering                     : False
UpdatedAt                           : 10/12/2018 12:01:29 AM
```

<span data-ttu-id="8464e-109">Frissíti a megadott témakört egy új leírással a megadott névtérben.</span><span class="sxs-lookup"><span data-stu-id="8464e-109">Updates the specified topic with a new description in the specified namespace.</span></span> <span data-ttu-id="8464e-110">Ez a példa frissíti a **EnableExpress** tulajdonságot **true** értékre.</span><span class="sxs-lookup"><span data-stu-id="8464e-110">This example updates the **EnableExpress** property to **true**.</span></span> 

## <span data-ttu-id="8464e-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8464e-111">PARAMETERS</span></span>

### <span data-ttu-id="8464e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8464e-112">-DefaultProfile</span></span>
<span data-ttu-id="8464e-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8464e-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8464e-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8464e-114">-InputObject</span></span>
<span data-ttu-id="8464e-115">A ServiceBus témakör definíciója.</span><span class="sxs-lookup"><span data-stu-id="8464e-115">ServiceBus Topic definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes
Parameter Sets: (All)
Aliases: TopicObj

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8464e-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8464e-116">-Name</span></span>
<span data-ttu-id="8464e-117">A téma neve</span><span class="sxs-lookup"><span data-stu-id="8464e-117">Topic Name.</span></span>

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

### <span data-ttu-id="8464e-118">-Namespace</span><span class="sxs-lookup"><span data-stu-id="8464e-118">-Namespace</span></span>
<span data-ttu-id="8464e-119">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="8464e-119">Namespace Name.</span></span>

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

### <span data-ttu-id="8464e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8464e-120">-ResourceGroupName</span></span>
<span data-ttu-id="8464e-121">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="8464e-121">The name of the resource group</span></span>

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

### <span data-ttu-id="8464e-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8464e-122">-Confirm</span></span>
<span data-ttu-id="8464e-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8464e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8464e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8464e-124">-WhatIf</span></span>
<span data-ttu-id="8464e-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8464e-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8464e-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8464e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8464e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8464e-127">CommonParameters</span></span>
<span data-ttu-id="8464e-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8464e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8464e-129">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8464e-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8464e-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8464e-130">INPUTS</span></span>

### <span data-ttu-id="8464e-131">System. String</span><span class="sxs-lookup"><span data-stu-id="8464e-131">System.String</span></span>

### <span data-ttu-id="8464e-132">Microsoft. Azure. Command. ServiceBus. models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="8464e-132">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="8464e-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8464e-133">OUTPUTS</span></span>

### <span data-ttu-id="8464e-134">Microsoft. Azure. Command. ServiceBus. models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="8464e-134">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="8464e-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8464e-135">NOTES</span></span>

## <span data-ttu-id="8464e-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8464e-136">RELATED LINKS</span></span>
