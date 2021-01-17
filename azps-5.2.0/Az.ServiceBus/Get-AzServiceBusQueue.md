---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusQueue.md
ms.openlocfilehash: 367d5b9184e98b9559d0f2f09696c2cf9905a854
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372692"
---
# <span data-ttu-id="fb79d-101">Get-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="fb79d-101">Get-AzServiceBusQueue</span></span>

## <span data-ttu-id="fb79d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb79d-102">SYNOPSIS</span></span>
<span data-ttu-id="fb79d-103">A megadott szolgáltatásbusz-várólistához ad leírást.</span><span class="sxs-lookup"><span data-stu-id="fb79d-103">Returns a description for the specified Service Bus queue.</span></span>

## <span data-ttu-id="fb79d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fb79d-104">SYNTAX</span></span>

```
Get-AzServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb79d-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fb79d-105">DESCRIPTION</span></span>
<span data-ttu-id="fb79d-106">A megadott szolgáltatásbusz-várólistához ad leírást.</span><span class="sxs-lookup"><span data-stu-id="fb79d-106">Returns a description for the specified Service Bus queue.</span></span>

## <span data-ttu-id="fb79d-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fb79d-107">EXAMPLES</span></span>

### <span data-ttu-id="fb79d-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="fb79d-108">Example 1</span></span>
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

<span data-ttu-id="fb79d-109">A várólista leírását adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="fb79d-109">Returns the description of the queue.</span></span>

### <span data-ttu-id="fb79d-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="fb79d-110">Example 2</span></span>
```
PS C:\> Get-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="fb79d-111">Egy adott névtér várólistáinak listáját adja vissza. Alapértelmezés szerint 100 várólistát ad vissza, ha több mint 100 várólistát kell visszaadni, használja a -MaxCount Parameter paramétert.</span><span class="sxs-lookup"><span data-stu-id="fb79d-111">Returns list of queues for given namespace, By default 100 queues will be returned, if more than 100 queues to be returned, please use -MaxCount Parameter.</span></span>

### <span data-ttu-id="fb79d-112">3. példa</span><span class="sxs-lookup"><span data-stu-id="fb79d-112">Example 3</span></span>
```
PS C:\> Get-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -MaxCount 150
```

<span data-ttu-id="fb79d-113">Egy adott névtér első 150 várólistájának listáját adja vissza.</span><span class="sxs-lookup"><span data-stu-id="fb79d-113">Returns list of first 150 queues for given namespace</span></span>

## <span data-ttu-id="fb79d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fb79d-114">PARAMETERS</span></span>

### <span data-ttu-id="fb79d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb79d-115">-DefaultProfile</span></span>
<span data-ttu-id="fb79d-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fb79d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb79d-117">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="fb79d-117">-MaxCount</span></span>
<span data-ttu-id="fb79d-118">Határozza meg, hogy legfeljebb hány várólistát kell visszahozni.</span><span class="sxs-lookup"><span data-stu-id="fb79d-118">Determine the maximum number of Queues to return.</span></span>

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

### <span data-ttu-id="fb79d-119">-Name</span><span class="sxs-lookup"><span data-stu-id="fb79d-119">-Name</span></span>
<span data-ttu-id="fb79d-120">Várólistán lévő név</span><span class="sxs-lookup"><span data-stu-id="fb79d-120">Queue Name</span></span>

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

### <span data-ttu-id="fb79d-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="fb79d-121">-Namespace</span></span>
<span data-ttu-id="fb79d-122">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="fb79d-122">Namespace Name</span></span>

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

### <span data-ttu-id="fb79d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb79d-123">-ResourceGroupName</span></span>
<span data-ttu-id="fb79d-124">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="fb79d-124">The name of the resource group</span></span>

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

### <span data-ttu-id="fb79d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb79d-125">CommonParameters</span></span>
<span data-ttu-id="fb79d-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb79d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb79d-127">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb79d-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb79d-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fb79d-128">INPUTS</span></span>

### <span data-ttu-id="fb79d-129">System.String</span><span class="sxs-lookup"><span data-stu-id="fb79d-129">System.String</span></span>

## <span data-ttu-id="fb79d-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb79d-130">OUTPUTS</span></span>

### <span data-ttu-id="fb79d-131">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="fb79d-131">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="fb79d-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fb79d-132">NOTES</span></span>

## <span data-ttu-id="fb79d-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fb79d-133">RELATED LINKS</span></span>
