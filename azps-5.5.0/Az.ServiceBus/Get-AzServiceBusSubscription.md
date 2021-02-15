---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusSubscription.md
ms.openlocfilehash: a2a535dd9607b3018b7fe215f152bbeeb01b8858
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208158"
---
# <span data-ttu-id="0177b-101">Get-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="0177b-101">Get-AzServiceBusSubscription</span></span>

## <span data-ttu-id="0177b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0177b-102">SYNOPSIS</span></span>
<span data-ttu-id="0177b-103">A megadott témakör előfizetési leírását adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="0177b-103">Returns a subscription description for the specified topic.</span></span>

## <span data-ttu-id="0177b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0177b-104">SYNTAX</span></span>

```
Get-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0177b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0177b-105">DESCRIPTION</span></span>
<span data-ttu-id="0177b-106">A **Get-AzServiceBusSubscription** parancsmag az adott Service Bus-témakör előfizetési leírását adja vissza.</span><span class="sxs-lookup"><span data-stu-id="0177b-106">The **Get-AzServiceBusSubscription** cmdlet returns a subscription description for the specified Service Bus topic.</span></span>

## <span data-ttu-id="0177b-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0177b-107">EXAMPLES</span></span>

### <span data-ttu-id="0177b-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="0177b-108">Example 1</span></span>
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

<span data-ttu-id="0177b-109">A szolgáltatásbusz adott témakörének előfizetési leírását adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="0177b-109">Returns a subscription description for the specified Service Bus topic.</span></span>

### <span data-ttu-id="0177b-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="0177b-110">Example 2</span></span>
```
PS C:\> Get-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="0177b-111">Visszaadja a szolgáltatásbusz adott témaköréhez kapcsolódó előfizetések listáját.</span><span class="sxs-lookup"><span data-stu-id="0177b-111">Returns list of subscriptions for specified Service Bus topic.</span></span> <span data-ttu-id="0177b-112">Alapértelmezés szerint 100 előfizetést ad vissza a rendszer, az előfizetések száma esetén használja a -MaxCount Parameter paramétert.</span><span class="sxs-lookup"><span data-stu-id="0177b-112">By default 100 subscriptions will be returned, for number of subscriptions please use -MaxCount Parameter</span></span>

### <span data-ttu-id="0177b-113">3. példa</span><span class="sxs-lookup"><span data-stu-id="0177b-113">Example 3</span></span>
```
PS C:\> Get-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -MaxCount 150
```

<span data-ttu-id="0177b-114">Visszaadja a szolgáltatásbusszal kapcsolatos témakör első 150 előfizetésének listáját.</span><span class="sxs-lookup"><span data-stu-id="0177b-114">Returns list of first 150 subscriptions for specified Service Bus topic.</span></span>

## <span data-ttu-id="0177b-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0177b-115">PARAMETERS</span></span>

### <span data-ttu-id="0177b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0177b-116">-DefaultProfile</span></span>
<span data-ttu-id="0177b-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0177b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0177b-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="0177b-118">-MaxCount</span></span>
<span data-ttu-id="0177b-119">Határozza meg, hogy legfeljebb hány előfizetést kell visszahozni.</span><span class="sxs-lookup"><span data-stu-id="0177b-119">Determine the maximum number of Subscriptions to return.</span></span>

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

### <span data-ttu-id="0177b-120">-Name</span><span class="sxs-lookup"><span data-stu-id="0177b-120">-Name</span></span>
<span data-ttu-id="0177b-121">Előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="0177b-121">Subscription Name</span></span>

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

### <span data-ttu-id="0177b-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="0177b-122">-Namespace</span></span>
<span data-ttu-id="0177b-123">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="0177b-123">Namespace Name</span></span>

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

### <span data-ttu-id="0177b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0177b-124">-ResourceGroupName</span></span>
<span data-ttu-id="0177b-125">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="0177b-125">The name of the resource group</span></span>

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

### <span data-ttu-id="0177b-126">-Topic</span><span class="sxs-lookup"><span data-stu-id="0177b-126">-Topic</span></span>
<span data-ttu-id="0177b-127">Témakör neve</span><span class="sxs-lookup"><span data-stu-id="0177b-127">Topic Name</span></span>

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

### <span data-ttu-id="0177b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0177b-128">CommonParameters</span></span>
<span data-ttu-id="0177b-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0177b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0177b-130">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0177b-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0177b-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0177b-131">INPUTS</span></span>

### <span data-ttu-id="0177b-132">System.String</span><span class="sxs-lookup"><span data-stu-id="0177b-132">System.String</span></span>

## <span data-ttu-id="0177b-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0177b-133">OUTPUTS</span></span>

### <span data-ttu-id="0177b-134">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="0177b-134">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="0177b-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0177b-135">NOTES</span></span>

## <span data-ttu-id="0177b-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0177b-136">RELATED LINKS</span></span>
