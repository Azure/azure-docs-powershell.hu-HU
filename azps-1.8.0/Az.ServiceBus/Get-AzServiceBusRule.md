---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusRule.md
ms.openlocfilehash: 0c23f4a46782e4ff30b48cde57706680c532e8f5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669196"
---
# <span data-ttu-id="f8105-101">Get-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="f8105-101">Get-AzServiceBusRule</span></span>

## <span data-ttu-id="f8105-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f8105-102">SYNOPSIS</span></span>
<span data-ttu-id="f8105-103">Új szabály létrehozása a témakör adott előfizetéséhez.</span><span class="sxs-lookup"><span data-stu-id="f8105-103">Creates a new rule for a given Subscription of Topic.</span></span> 

## <span data-ttu-id="f8105-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f8105-104">SYNTAX</span></span>

```
Get-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f8105-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f8105-105">DESCRIPTION</span></span>
<span data-ttu-id="f8105-106">A **Get-AzServiceBusRule** parancsmag a megadott szabály leírását az adott előfizetésben kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f8105-106">The **Get-AzServiceBusRule** cmdlet gets the description of the specified rule in the given subscription of topic.</span></span>

## <span data-ttu-id="f8105-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f8105-107">EXAMPLES</span></span>

### <span data-ttu-id="f8105-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f8105-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="f8105-109">Adott előfizetés megadott szabályának leírását adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="f8105-109">Returns the specified rule description for a specified subscription.</span></span>

### <span data-ttu-id="f8105-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="f8105-110">Example 2</span></span>
```
PS C:\> Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription
```

<span data-ttu-id="f8105-111">A megadott előfizetéshez tartozó szabály leírásainak listáját adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="f8105-111">Returns list of rule descriptions for a specified subscription.</span></span>  <span data-ttu-id="f8105-112">Alapértelmezés szerint az 100 szabályait adja vissza, ha több mint 100 szabályt ad vissza, használja a-MaxCount paramétert.</span><span class="sxs-lookup"><span data-stu-id="f8105-112">By default 100 rule will be returned, if more than 100 rule to be returned, please use -MaxCount Parameter.</span></span>

### <span data-ttu-id="f8105-113">3. példa</span><span class="sxs-lookup"><span data-stu-id="f8105-113">Example 3</span></span>
```
PS C:\> Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -MaxCount 150
```

<span data-ttu-id="f8105-114">A megadott előfizetéshez tartozó első 150-szabályok listáját adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="f8105-114">Returns list of first 150 rules descriptions for a specified subscription.</span></span>

## <span data-ttu-id="f8105-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f8105-115">PARAMETERS</span></span>

### <span data-ttu-id="f8105-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8105-116">-DefaultProfile</span></span>
<span data-ttu-id="f8105-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f8105-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8105-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="f8105-118">-MaxCount</span></span>
<span data-ttu-id="f8105-119">Adja meg a visszaadott szabályok maximális számát.</span><span class="sxs-lookup"><span data-stu-id="f8105-119">Determine the maximum number of Rules to return.</span></span>

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

### <span data-ttu-id="f8105-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f8105-120">-Name</span></span>
<span data-ttu-id="f8105-121">Szabály neve</span><span class="sxs-lookup"><span data-stu-id="f8105-121">Rule Name</span></span>

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

### <span data-ttu-id="f8105-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f8105-122">-Namespace</span></span>
<span data-ttu-id="f8105-123">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="f8105-123">Namespace Name</span></span>

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

### <span data-ttu-id="f8105-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8105-124">-ResourceGroupName</span></span>
<span data-ttu-id="f8105-125">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="f8105-125">The name of the resource group</span></span>

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

### <span data-ttu-id="f8105-126">-Előfizetés</span><span class="sxs-lookup"><span data-stu-id="f8105-126">-Subscription</span></span>
<span data-ttu-id="f8105-127">Előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="f8105-127">Subscription Name</span></span>

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

### <span data-ttu-id="f8105-128">-Topic</span><span class="sxs-lookup"><span data-stu-id="f8105-128">-Topic</span></span>
<span data-ttu-id="f8105-129">Téma neve</span><span class="sxs-lookup"><span data-stu-id="f8105-129">Topic Name</span></span>

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

### <span data-ttu-id="f8105-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8105-130">CommonParameters</span></span>
<span data-ttu-id="f8105-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f8105-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8105-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8105-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8105-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f8105-133">INPUTS</span></span>

### <span data-ttu-id="f8105-134">System. String</span><span class="sxs-lookup"><span data-stu-id="f8105-134">System.String</span></span>

## <span data-ttu-id="f8105-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f8105-135">OUTPUTS</span></span>

### <span data-ttu-id="f8105-136">Microsoft. Azure. Command. ServiceBus. models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="f8105-136">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="f8105-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f8105-137">NOTES</span></span>

## <span data-ttu-id="f8105-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f8105-138">RELATED LINKS</span></span>
