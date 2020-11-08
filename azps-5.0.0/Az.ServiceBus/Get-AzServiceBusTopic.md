---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusTopic.md
ms.openlocfilehash: 3d688362932f61bdea9d685b98f2cba757288da2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187027"
---
# <span data-ttu-id="a4282-101">Get-AzServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="a4282-101">Get-AzServiceBusTopic</span></span>

## <span data-ttu-id="a4282-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a4282-102">SYNOPSIS</span></span>
<span data-ttu-id="a4282-103">A megadott szolgáltatási busz témakör leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="a4282-103">Returns a description for the specified Service Bus topic.</span></span>

## <span data-ttu-id="a4282-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a4282-104">SYNTAX</span></span>

```
Get-AzServiceBusTopic [-ResourceGroupName <String>] [-Namespace <String>] [-Name <String>]
 [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4282-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a4282-105">DESCRIPTION</span></span>
<span data-ttu-id="a4282-106">A **Get-AzServiceBusTopic** parancsmag a megadott szolgáltatási busz névterének leírását adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="a4282-106">The **Get-AzServiceBusTopic** cmdlet returns a topic description for the specified Service Bus namespace.</span></span>

## <span data-ttu-id="a4282-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a4282-107">EXAMPLES</span></span>

### <span data-ttu-id="a4282-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a4282-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1

Name                                : SB-Topic_example1
Id                                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroupName}/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_example1
Type                                : Microsoft.ServiceBus/Namespaces/Topics
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : P10675199DT2H48M5.4775807S
CreatedAt                           : 10/11/2018 11:51:24 PM
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
DefaultMessageTimeToLive            : P10675199DT2H48M5.4775807S
DuplicateDetectionHistoryTimeWindow : PT10M
EnableBatchedOperations             : True
EnableExpress                       : False
EnablePartitioning                  : False
MaxSizeInMegabytes                  : 81920
RequiresDuplicateDetection          : False
SizeInBytes                         : 0
Status                              : Active
SubscriptionCount                   : 0
SupportOrdering                     : True
UpdatedAt                           : 10/11/2018 11:51:24 PM
```

<span data-ttu-id="a4282-109">A megadott, a szolgáltatás busz névteréhez tartozó témakör leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="a4282-109">Returns the description of the specified topic for the given Service Bus namespace.</span></span>

### <span data-ttu-id="a4282-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="a4282-110">Example 2</span></span>
```
PS C:\> Get-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="a4282-111">A szolgáltatás busz névteréhez tartozó témakörök listáját adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="a4282-111">Returns list of topics for given Service Bus namespace.</span></span> <span data-ttu-id="a4282-112">Alapértelmezés szerint az 100-témaköröket a program visszaadja, ha több mint 100-témakört ad vissza, kérjük, használja a-MaxCount paramétert.</span><span class="sxs-lookup"><span data-stu-id="a4282-112">By default 100 topics will be returned, if more than 100 topics to be returned, please use -MaxCount Parameter.</span></span>

### <span data-ttu-id="a4282-113">3. példa</span><span class="sxs-lookup"><span data-stu-id="a4282-113">Example 3</span></span>
```
PS C:\> Get-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -MaxCount 150
```

<span data-ttu-id="a4282-114">Az első 150-témakörök listáját adja meg a szolgáltatás buszának névteréhez.</span><span class="sxs-lookup"><span data-stu-id="a4282-114">Returns list of first 150 topics for given Service Bus namespace.</span></span>

## <span data-ttu-id="a4282-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a4282-115">PARAMETERS</span></span>

### <span data-ttu-id="a4282-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4282-116">-DefaultProfile</span></span>
<span data-ttu-id="a4282-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a4282-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4282-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="a4282-118">-MaxCount</span></span>
<span data-ttu-id="a4282-119">Adja meg a visszaadott témakörök maximális számát.</span><span class="sxs-lookup"><span data-stu-id="a4282-119">Determine the maximum number of Topics to return.</span></span>

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

### <span data-ttu-id="a4282-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a4282-120">-Name</span></span>
<span data-ttu-id="a4282-121">Téma neve</span><span class="sxs-lookup"><span data-stu-id="a4282-121">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4282-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a4282-122">-Namespace</span></span>
<span data-ttu-id="a4282-123">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="a4282-123">Namespace Name</span></span>

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

### <span data-ttu-id="a4282-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4282-124">-ResourceGroupName</span></span>
<span data-ttu-id="a4282-125">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="a4282-125">The name of the resource group</span></span>

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

### <span data-ttu-id="a4282-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4282-126">CommonParameters</span></span>
<span data-ttu-id="a4282-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a4282-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4282-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4282-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4282-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4282-129">INPUTS</span></span>

### <span data-ttu-id="a4282-130">System. String</span><span class="sxs-lookup"><span data-stu-id="a4282-130">System.String</span></span>

## <span data-ttu-id="a4282-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4282-131">OUTPUTS</span></span>

### <span data-ttu-id="a4282-132">Microsoft. Azure. Command. ServiceBus. models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="a4282-132">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="a4282-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a4282-133">NOTES</span></span>

## <span data-ttu-id="a4282-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a4282-134">RELATED LINKS</span></span>
