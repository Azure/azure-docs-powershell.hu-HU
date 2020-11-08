---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusSubscription.md
ms.openlocfilehash: a2a535dd9607b3018b7fe215f152bbeeb01b8858
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185686"
---
# <span data-ttu-id="81f2e-101">Get-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="81f2e-101">Get-AzServiceBusSubscription</span></span>

## <span data-ttu-id="81f2e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="81f2e-102">SYNOPSIS</span></span>
<span data-ttu-id="81f2e-103">A megadott témakör előfizetési leírását adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="81f2e-103">Returns a subscription description for the specified topic.</span></span>

## <span data-ttu-id="81f2e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="81f2e-104">SYNTAX</span></span>

```
Get-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81f2e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="81f2e-105">DESCRIPTION</span></span>
<span data-ttu-id="81f2e-106">A **Get-AzServiceBusSubscription** parancsmag az előfizetési leírását adja eredményül a megadott buszjárati témakörhöz.</span><span class="sxs-lookup"><span data-stu-id="81f2e-106">The **Get-AzServiceBusSubscription** cmdlet returns a subscription description for the specified Service Bus topic.</span></span>

## <span data-ttu-id="81f2e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="81f2e-107">EXAMPLES</span></span>

### <span data-ttu-id="81f2e-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="81f2e-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1

Name                                      : SB-TopicSubscription-Example1
AccessedAt                                : 1/20/2017 3:18:54 AM
AutoDeleteOnIdle                          : 10675199.02:48:05.4775807
CountDetails                              : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
CreatedAt                                 : 1/20/2017 3:18:52 AM
DefaultMessageTimeToLive                  : 10675199.02:48:05.4775807
DeadLetteringOnMessageExpiration          : False
EnableBatchedOperations                   : True
LockDuration                              : 00:01:00
MaxDeliveryCount                          : 10
MessageCount                              : 0
RequiresSession                           : False
Status                                    : Active
UpdatedAt                                 : 1/20/2017 3:18:54 AM
```

<span data-ttu-id="81f2e-109">A megadott szervizsor-témakör előfizetési leírását adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="81f2e-109">Returns a subscription description for the specified Service Bus topic.</span></span>

### <span data-ttu-id="81f2e-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="81f2e-110">Example 2</span></span>
```
PS C:\> Get-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="81f2e-111">Az előfizetések listáját adja meg a megadott szolgáltatási busz témakörben.</span><span class="sxs-lookup"><span data-stu-id="81f2e-111">Returns list of subscriptions for specified Service Bus topic.</span></span> <span data-ttu-id="81f2e-112">Alapértelmezés szerint az 100-előfizetések eredményül kerülnek, az előfizetések száma esetén használja a-MaxCount paramétert.</span><span class="sxs-lookup"><span data-stu-id="81f2e-112">By default 100 subscriptions will be returned, for number of subscriptions please use -MaxCount Parameter</span></span>

### <span data-ttu-id="81f2e-113">3. példa</span><span class="sxs-lookup"><span data-stu-id="81f2e-113">Example 3</span></span>
```
PS C:\> Get-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -MaxCount 150
```

<span data-ttu-id="81f2e-114">Az első 150-előfizetések listáját adja eredményül a megadott szolgáltatási busz témakörben.</span><span class="sxs-lookup"><span data-stu-id="81f2e-114">Returns list of first 150 subscriptions for specified Service Bus topic.</span></span>

## <span data-ttu-id="81f2e-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="81f2e-115">PARAMETERS</span></span>

### <span data-ttu-id="81f2e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81f2e-116">-DefaultProfile</span></span>
<span data-ttu-id="81f2e-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="81f2e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81f2e-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="81f2e-118">-MaxCount</span></span>
<span data-ttu-id="81f2e-119">Adja meg, hogy legfeljebb hány előfizetést adhat vissza.</span><span class="sxs-lookup"><span data-stu-id="81f2e-119">Determine the maximum number of Subscriptions to return.</span></span>

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

### <span data-ttu-id="81f2e-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="81f2e-120">-Name</span></span>
<span data-ttu-id="81f2e-121">Előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="81f2e-121">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81f2e-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="81f2e-122">-Namespace</span></span>
<span data-ttu-id="81f2e-123">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="81f2e-123">Namespace Name</span></span>

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

### <span data-ttu-id="81f2e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81f2e-124">-ResourceGroupName</span></span>
<span data-ttu-id="81f2e-125">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="81f2e-125">The name of the resource group</span></span>

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

### <span data-ttu-id="81f2e-126">-Topic</span><span class="sxs-lookup"><span data-stu-id="81f2e-126">-Topic</span></span>
<span data-ttu-id="81f2e-127">Téma neve</span><span class="sxs-lookup"><span data-stu-id="81f2e-127">Topic Name</span></span>

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

### <span data-ttu-id="81f2e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81f2e-128">CommonParameters</span></span>
<span data-ttu-id="81f2e-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="81f2e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81f2e-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81f2e-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81f2e-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="81f2e-131">INPUTS</span></span>

### <span data-ttu-id="81f2e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="81f2e-132">System.String</span></span>

## <span data-ttu-id="81f2e-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="81f2e-133">OUTPUTS</span></span>

### <span data-ttu-id="81f2e-134">Microsoft. Azure. Command. ServiceBus. models. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="81f2e-134">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="81f2e-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="81f2e-135">NOTES</span></span>

## <span data-ttu-id="81f2e-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="81f2e-136">RELATED LINKS</span></span>
