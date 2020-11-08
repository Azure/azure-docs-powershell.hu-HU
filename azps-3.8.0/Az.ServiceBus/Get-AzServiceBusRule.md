---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusRule.md
ms.openlocfilehash: f4899d55919f8b3c08b36babc448f1594f4ac4c8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013735"
---
# <span data-ttu-id="9e7fd-101">Get-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="9e7fd-101">Get-AzServiceBusRule</span></span>

## <span data-ttu-id="9e7fd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9e7fd-102">SYNOPSIS</span></span>
<span data-ttu-id="9e7fd-103">Új szabály létrehozása a témakör adott előfizetéséhez.</span><span class="sxs-lookup"><span data-stu-id="9e7fd-103">Creates a new rule for a given Subscription of Topic.</span></span> 

## <span data-ttu-id="9e7fd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9e7fd-104">SYNTAX</span></span>

```
Get-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9e7fd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9e7fd-105">DESCRIPTION</span></span>
<span data-ttu-id="9e7fd-106">A **Get-AzServiceBusRule** parancsmag a megadott szabály leírását az adott előfizetésben kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9e7fd-106">The **Get-AzServiceBusRule** cmdlet gets the description of the specified rule in the given subscription of topic.</span></span>

## <span data-ttu-id="9e7fd-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9e7fd-107">EXAMPLES</span></span>

### <span data-ttu-id="9e7fd-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9e7fd-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="9e7fd-109">Adott előfizetés megadott szabályának leírását adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="9e7fd-109">Returns the specified rule description for a specified subscription.</span></span>

### <span data-ttu-id="9e7fd-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="9e7fd-110">Example 2</span></span>
```
PS C:\> Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription
```

<span data-ttu-id="9e7fd-111">A megadott előfizetéshez tartozó szabály leírásainak listáját adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="9e7fd-111">Returns list of rule descriptions for a specified subscription.</span></span>  <span data-ttu-id="9e7fd-112">Alapértelmezés szerint az 100 szabályait adja vissza, ha több mint 100 szabályt ad vissza, használja a-MaxCount paramétert.</span><span class="sxs-lookup"><span data-stu-id="9e7fd-112">By default 100 rule will be returned, if more than 100 rule to be returned, please use -MaxCount Parameter.</span></span>

### <span data-ttu-id="9e7fd-113">3. példa</span><span class="sxs-lookup"><span data-stu-id="9e7fd-113">Example 3</span></span>
```
PS C:\> Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -MaxCount 150
```

<span data-ttu-id="9e7fd-114">A megadott előfizetéshez tartozó első 150-szabályok listáját adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="9e7fd-114">Returns list of first 150 rules descriptions for a specified subscription.</span></span>

## <span data-ttu-id="9e7fd-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9e7fd-115">PARAMETERS</span></span>

### <span data-ttu-id="9e7fd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e7fd-116">-DefaultProfile</span></span>
<span data-ttu-id="9e7fd-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9e7fd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e7fd-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="9e7fd-118">-MaxCount</span></span>
<span data-ttu-id="9e7fd-119">Adja meg a visszaadott szabályok maximális számát.</span><span class="sxs-lookup"><span data-stu-id="9e7fd-119">Determine the maximum number of Rules to return.</span></span>

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

### <span data-ttu-id="9e7fd-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9e7fd-120">-Name</span></span>
<span data-ttu-id="9e7fd-121">Szabály neve</span><span class="sxs-lookup"><span data-stu-id="9e7fd-121">Rule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e7fd-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="9e7fd-122">-Namespace</span></span>
<span data-ttu-id="9e7fd-123">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="9e7fd-123">Namespace Name</span></span>

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

### <span data-ttu-id="9e7fd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e7fd-124">-ResourceGroupName</span></span>
<span data-ttu-id="9e7fd-125">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="9e7fd-125">The name of the resource group</span></span>

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

### <span data-ttu-id="9e7fd-126">-Előfizetés</span><span class="sxs-lookup"><span data-stu-id="9e7fd-126">-Subscription</span></span>
<span data-ttu-id="9e7fd-127">Előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="9e7fd-127">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e7fd-128">-Topic</span><span class="sxs-lookup"><span data-stu-id="9e7fd-128">-Topic</span></span>
<span data-ttu-id="9e7fd-129">Téma neve</span><span class="sxs-lookup"><span data-stu-id="9e7fd-129">Topic Name</span></span>

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

### <span data-ttu-id="9e7fd-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e7fd-130">CommonParameters</span></span>
<span data-ttu-id="9e7fd-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9e7fd-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e7fd-132">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e7fd-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e7fd-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9e7fd-133">INPUTS</span></span>

### <span data-ttu-id="9e7fd-134">System. String</span><span class="sxs-lookup"><span data-stu-id="9e7fd-134">System.String</span></span>

## <span data-ttu-id="9e7fd-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9e7fd-135">OUTPUTS</span></span>

### <span data-ttu-id="9e7fd-136">Microsoft. Azure. Command. ServiceBus. models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="9e7fd-136">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="9e7fd-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9e7fd-137">NOTES</span></span>

## <span data-ttu-id="9e7fd-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9e7fd-138">RELATED LINKS</span></span>
