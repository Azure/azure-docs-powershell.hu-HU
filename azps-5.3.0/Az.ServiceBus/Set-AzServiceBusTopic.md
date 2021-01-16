---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusTopic.md
ms.openlocfilehash: 8e8fe04476e66db6b45372879ac3176f9d492acc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479601"
---
# <span data-ttu-id="afcff-101">Set-AzServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="afcff-101">Set-AzServiceBusTopic</span></span>

## <span data-ttu-id="afcff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="afcff-102">SYNOPSIS</span></span>
<span data-ttu-id="afcff-103">Frissíti a Szolgáltatásbusz témakör leírását a megadott Service Bus névterében.</span><span class="sxs-lookup"><span data-stu-id="afcff-103">Updates the description of a Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="afcff-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="afcff-104">SYNTAX</span></span>

```
Set-AzServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject] <PSTopicAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="afcff-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="afcff-105">DESCRIPTION</span></span>
<span data-ttu-id="afcff-106">A **Set-AzServiceBusTopic** parancsmag frissíti a service bus témakör leírásobjektumát a megadott Service Bus névterében.</span><span class="sxs-lookup"><span data-stu-id="afcff-106">The **Set-AzServiceBusTopic** cmdlet updates a description object for a Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="afcff-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="afcff-107">EXAMPLES</span></span>

### <span data-ttu-id="afcff-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="afcff-108">Example 1</span></span>
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

<span data-ttu-id="afcff-109">Frissíti a megadott témakört egy új leírással a megadott névtérben.</span><span class="sxs-lookup"><span data-stu-id="afcff-109">Updates the specified topic with a new description in the specified namespace.</span></span> <span data-ttu-id="afcff-110">Ebben a példában igaz értékre frissíti az **EnableExpress** **tulajdonságot.**</span><span class="sxs-lookup"><span data-stu-id="afcff-110">This example updates the **EnableExpress** property to **true**.</span></span> 

## <span data-ttu-id="afcff-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="afcff-111">PARAMETERS</span></span>

### <span data-ttu-id="afcff-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afcff-112">-DefaultProfile</span></span>
<span data-ttu-id="afcff-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="afcff-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="afcff-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="afcff-114">-InputObject</span></span>
<span data-ttu-id="afcff-115">ServiceBus-témakör definíciója.</span><span class="sxs-lookup"><span data-stu-id="afcff-115">ServiceBus Topic definition.</span></span>

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

### <span data-ttu-id="afcff-116">-Name</span><span class="sxs-lookup"><span data-stu-id="afcff-116">-Name</span></span>
<span data-ttu-id="afcff-117">Témakör neve.</span><span class="sxs-lookup"><span data-stu-id="afcff-117">Topic Name.</span></span>

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

### <span data-ttu-id="afcff-118">-Namespace</span><span class="sxs-lookup"><span data-stu-id="afcff-118">-Namespace</span></span>
<span data-ttu-id="afcff-119">Névtér neve.</span><span class="sxs-lookup"><span data-stu-id="afcff-119">Namespace Name.</span></span>

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

### <span data-ttu-id="afcff-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afcff-120">-ResourceGroupName</span></span>
<span data-ttu-id="afcff-121">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="afcff-121">The name of the resource group</span></span>

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

### <span data-ttu-id="afcff-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="afcff-122">-Confirm</span></span>
<span data-ttu-id="afcff-123">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="afcff-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afcff-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afcff-124">-WhatIf</span></span>
<span data-ttu-id="afcff-125">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="afcff-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afcff-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="afcff-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afcff-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afcff-127">CommonParameters</span></span>
<span data-ttu-id="afcff-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afcff-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afcff-129">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afcff-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afcff-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="afcff-130">INPUTS</span></span>

### <span data-ttu-id="afcff-131">System.String</span><span class="sxs-lookup"><span data-stu-id="afcff-131">System.String</span></span>

### <span data-ttu-id="afcff-132">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="afcff-132">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="afcff-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="afcff-133">OUTPUTS</span></span>

### <span data-ttu-id="afcff-134">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="afcff-134">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="afcff-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="afcff-135">NOTES</span></span>

## <span data-ttu-id="afcff-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="afcff-136">RELATED LINKS</span></span>
