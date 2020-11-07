---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusRule.md
ms.openlocfilehash: 39cd0759f18c84f78a2e6a75f8e1c9b257fb9da9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680481"
---
# <span data-ttu-id="2f260-101">New-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="2f260-101">New-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="2f260-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2f260-102">SYNOPSIS</span></span>
<span data-ttu-id="2f260-103">Új szabály létrehozása a témakör adott előfizetéséhez.</span><span class="sxs-lookup"><span data-stu-id="2f260-103">Creates a new rule for a given Subscription of Topic.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f260-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2f260-104">SYNTAX</span></span>

```
New-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="2f260-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2f260-105">DESCRIPTION</span></span>
<span data-ttu-id="2f260-106">A **New-AzureRmServiceBusRule** parancsmag új szabályt hoz létre az adott előfizetéshez.</span><span class="sxs-lookup"><span data-stu-id="2f260-106">The **New-AzureRmServiceBusRule** cmdlet Creates a new rule for given subscription.</span></span>

## <span data-ttu-id="2f260-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2f260-107">EXAMPLES</span></span>

### <span data-ttu-id="2f260-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2f260-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'"
```

<span data-ttu-id="2f260-109">A **New-AzureRmServiceBusRule** parancsmag új szabályt hoz létre a megadott előfizetéshez.</span><span class="sxs-lookup"><span data-stu-id="2f260-109">The **New-AzureRmServiceBusRule** cmdlet creates a new rule for the specified Subscription.</span></span>

## <span data-ttu-id="2f260-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2f260-110">PARAMETERS</span></span>

### <span data-ttu-id="2f260-111">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2f260-111">-Confirm</span></span>
<span data-ttu-id="2f260-112">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2f260-112">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f260-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2f260-113">-Name</span></span>
<span data-ttu-id="2f260-114">Szabály neve</span><span class="sxs-lookup"><span data-stu-id="2f260-114">Rule Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f260-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2f260-115">-Namespace</span></span>
<span data-ttu-id="2f260-116">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="2f260-116">Namespace Name.</span></span>

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

### <span data-ttu-id="2f260-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f260-117">-ResourceGroupName</span></span>
<span data-ttu-id="2f260-118">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="2f260-118">The name of the resource group</span></span>

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

### <span data-ttu-id="2f260-119">-SqlExpression</span><span class="sxs-lookup"><span data-stu-id="2f260-119">-SqlExpression</span></span>
<span data-ttu-id="2f260-120">SQL szűrni kifejezés</span><span class="sxs-lookup"><span data-stu-id="2f260-120">Sql Fillter Expression</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f260-121">-Előfizetés</span><span class="sxs-lookup"><span data-stu-id="2f260-121">-Subscription</span></span>
<span data-ttu-id="2f260-122">Előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="2f260-122">Subscription Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f260-123">-Topic</span><span class="sxs-lookup"><span data-stu-id="2f260-123">-Topic</span></span>
<span data-ttu-id="2f260-124">A téma neve</span><span class="sxs-lookup"><span data-stu-id="2f260-124">Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f260-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f260-125">-WhatIf</span></span>
<span data-ttu-id="2f260-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2f260-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f260-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2f260-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="2f260-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f260-128">INPUTS</span></span>

### <span data-ttu-id="2f260-129">System. String</span><span class="sxs-lookup"><span data-stu-id="2f260-129">System.String</span></span>


## <span data-ttu-id="2f260-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f260-130">OUTPUTS</span></span>

### <span data-ttu-id="2f260-131">Microsoft. Azure. Command. ServiceBus. models. RulesAttributes</span><span class="sxs-lookup"><span data-stu-id="2f260-131">Microsoft.Azure.Commands.ServiceBus.Models.RulesAttributes</span></span>


## <span data-ttu-id="2f260-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2f260-132">NOTES</span></span>

## <span data-ttu-id="2f260-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2f260-133">RELATED LINKS</span></span>

