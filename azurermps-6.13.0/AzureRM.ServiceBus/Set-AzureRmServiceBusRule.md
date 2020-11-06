---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusRule.md
ms.openlocfilehash: cb6200156b68524119df86e24d812b97bcd250e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495647"
---
# <span data-ttu-id="7cd1f-101">Set-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="7cd1f-101">Set-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="7cd1f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7cd1f-102">SYNOPSIS</span></span>
<span data-ttu-id="7cd1f-103">Frissíti a megadott szabály leírását a megadott előfizetéshez.</span><span class="sxs-lookup"><span data-stu-id="7cd1f-103">Updates the specified rule description for the given subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7cd1f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7cd1f-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-InputObject] <PSRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7cd1f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7cd1f-105">DESCRIPTION</span></span>
<span data-ttu-id="7cd1f-106">A **set-AzureRmServiceBusRule** parancsmag frissíti az adott előfizetés meghatározott szabályának leírását.</span><span class="sxs-lookup"><span data-stu-id="7cd1f-106">The **Set-AzureRmServiceBusRule** cmdlet updates the description for the specified rule of the given subscription.</span></span>

## <span data-ttu-id="7cd1f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7cd1f-107">EXAMPLES</span></span>

### <span data-ttu-id="7cd1f-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7cd1f-108">Example 1</span></span>
```
PS C:\> $getRule = Get-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
PS C:\> $getRule.SqlFilter.SqlExpression = "mysqlexpression='condition'"
PS C:\> $setRule = Set-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -InputObject $getRule
```

<span data-ttu-id="7cd1f-109">a témakörben szereplő előfizetéshez tartozó sqlexpression **mysqlexpression = "Condition" ("feltétel"** ) frissítése `SBEule` `SBSubscription``SBTopic`</span><span class="sxs-lookup"><span data-stu-id="7cd1f-109">updates the sqlexpression **mysqlexpression='condition'** of the rule `SBEule` of the subscription `SBSubscription` in Topic `SBTopic`</span></span>

## <span data-ttu-id="7cd1f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7cd1f-110">PARAMETERS</span></span>

### <span data-ttu-id="7cd1f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cd1f-111">-DefaultProfile</span></span>
<span data-ttu-id="7cd1f-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7cd1f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd1f-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7cd1f-113">-InputObject</span></span>
<span data-ttu-id="7cd1f-114">ServiceBus szabályok definíciója</span><span class="sxs-lookup"><span data-stu-id="7cd1f-114">ServiceBus Rules definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cd1f-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7cd1f-115">-Name</span></span>
<span data-ttu-id="7cd1f-116">Szabály neve.</span><span class="sxs-lookup"><span data-stu-id="7cd1f-116">Rule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd1f-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7cd1f-117">-Namespace</span></span>
<span data-ttu-id="7cd1f-118">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="7cd1f-118">Namespace Name.</span></span>

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

### <span data-ttu-id="7cd1f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cd1f-119">-ResourceGroupName</span></span>
<span data-ttu-id="7cd1f-120">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="7cd1f-120">The name of the resource group</span></span>

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

### <span data-ttu-id="7cd1f-121">-Előfizetés</span><span class="sxs-lookup"><span data-stu-id="7cd1f-121">-Subscription</span></span>
<span data-ttu-id="7cd1f-122">Előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="7cd1f-122">Subscription Name.</span></span>

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

### <span data-ttu-id="7cd1f-123">-Topic</span><span class="sxs-lookup"><span data-stu-id="7cd1f-123">-Topic</span></span>
<span data-ttu-id="7cd1f-124">A téma neve</span><span class="sxs-lookup"><span data-stu-id="7cd1f-124">Topic Name.</span></span>

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

### <span data-ttu-id="7cd1f-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7cd1f-125">-Confirm</span></span>
<span data-ttu-id="7cd1f-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7cd1f-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd1f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cd1f-127">-WhatIf</span></span>
<span data-ttu-id="7cd1f-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7cd1f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cd1f-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7cd1f-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd1f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cd1f-130">CommonParameters</span></span>
<span data-ttu-id="7cd1f-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7cd1f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cd1f-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cd1f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cd1f-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7cd1f-133">INPUTS</span></span>

### <span data-ttu-id="7cd1f-134">System. String</span><span class="sxs-lookup"><span data-stu-id="7cd1f-134">System.String</span></span>

### <span data-ttu-id="7cd1f-135">Microsoft. Azure. Command. ServiceBus. models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="7cd1f-135">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="7cd1f-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7cd1f-136">OUTPUTS</span></span>

### <span data-ttu-id="7cd1f-137">Microsoft. Azure. Command. ServiceBus. models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="7cd1f-137">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="7cd1f-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7cd1f-138">NOTES</span></span>

## <span data-ttu-id="7cd1f-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7cd1f-139">RELATED LINKS</span></span>
