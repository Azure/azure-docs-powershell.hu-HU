---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusQueue.md
ms.openlocfilehash: 367d5b9184e98b9559d0f2f09696c2cf9905a854
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296762"
---
# <span data-ttu-id="e0605-101">Get-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="e0605-101">Get-AzServiceBusQueue</span></span>

## <span data-ttu-id="e0605-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e0605-102">SYNOPSIS</span></span>
<span data-ttu-id="e0605-103">A megadott szolgáltatás busz-várólistájának leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="e0605-103">Returns a description for the specified Service Bus queue.</span></span>

## <span data-ttu-id="e0605-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e0605-104">SYNTAX</span></span>

```
Get-AzServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0605-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e0605-105">DESCRIPTION</span></span>
<span data-ttu-id="e0605-106">A megadott szolgáltatás busz-várólistájának leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="e0605-106">Returns a description for the specified Service Bus queue.</span></span>

## <span data-ttu-id="e0605-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e0605-107">EXAMPLES</span></span>

### <span data-ttu-id="e0605-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e0605-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1

Id                                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroupName}/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/SB-Queue_example1
Name                                : SB-Queue_example1
LockDuration                        : PT1M
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : P10675199DT2H48M5.4775807S
CreatedAt                           : 10/11/2018 12:37:11 AM
DefaultMessageTimeToLive            : P10675199DT2H48M5.4775807S
DuplicateDetectionHistoryTimeWindow : PT10M
DeadLetteringOnMessageExpiration    : False
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
UpdatedAt                           : 10/11/2018 12:37:11 AM
ForwardTo                           :
ForwardDeadLetteredMessagesTo       :
EnableBatchedOperations             : False
```

<span data-ttu-id="e0605-109">A várólista leírását számítja ki.</span><span class="sxs-lookup"><span data-stu-id="e0605-109">Returns the description of the queue.</span></span>

### <span data-ttu-id="e0605-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="e0605-110">Example 2</span></span>
```
PS C:\> Get-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="e0605-111">A megadott névtérhez tartozó várólisták listáját adja vissza, alapértelmezés szerint az 100-várólisták lesznek visszaadva, ha több mint 100 várólistát ad vissza, kérjük, használja a-MaxCount paramétert.</span><span class="sxs-lookup"><span data-stu-id="e0605-111">Returns list of queues for given namespace, By default 100 queues will be returned, if more than 100 queues to be returned, please use -MaxCount Parameter.</span></span>

### <span data-ttu-id="e0605-112">3. példa</span><span class="sxs-lookup"><span data-stu-id="e0605-112">Example 3</span></span>
```
PS C:\> Get-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -MaxCount 150
```

<span data-ttu-id="e0605-113">Az első 150-várólisták listáját adja meg az adott névtérhez.</span><span class="sxs-lookup"><span data-stu-id="e0605-113">Returns list of first 150 queues for given namespace</span></span>

## <span data-ttu-id="e0605-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e0605-114">PARAMETERS</span></span>

### <span data-ttu-id="e0605-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0605-115">-DefaultProfile</span></span>
<span data-ttu-id="e0605-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e0605-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0605-117">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="e0605-117">-MaxCount</span></span>
<span data-ttu-id="e0605-118">Adja meg, hogy legfeljebb hány várólistát szeretne visszaadni.</span><span class="sxs-lookup"><span data-stu-id="e0605-118">Determine the maximum number of Queues to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0605-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e0605-119">-Name</span></span>
<span data-ttu-id="e0605-120">Várólista neve</span><span class="sxs-lookup"><span data-stu-id="e0605-120">Queue Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0605-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e0605-121">-Namespace</span></span>
<span data-ttu-id="e0605-122">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="e0605-122">Namespace Name</span></span>

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

### <span data-ttu-id="e0605-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0605-123">-ResourceGroupName</span></span>
<span data-ttu-id="e0605-124">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="e0605-124">The name of the resource group</span></span>

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

### <span data-ttu-id="e0605-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0605-125">CommonParameters</span></span>
<span data-ttu-id="e0605-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e0605-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0605-127">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0605-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0605-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0605-128">INPUTS</span></span>

### <span data-ttu-id="e0605-129">System. String</span><span class="sxs-lookup"><span data-stu-id="e0605-129">System.String</span></span>

## <span data-ttu-id="e0605-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0605-130">OUTPUTS</span></span>

### <span data-ttu-id="e0605-131">Microsoft. Azure. Command. ServiceBus. models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="e0605-131">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="e0605-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e0605-132">NOTES</span></span>

## <span data-ttu-id="e0605-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e0605-133">RELATED LINKS</span></span>
