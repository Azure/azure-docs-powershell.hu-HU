---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusRule.md
ms.openlocfilehash: b86b9629062515afb1ee70e7c7372cbc7687bfa5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017604"
---
# <span data-ttu-id="62ed9-101">Set-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="62ed9-101">Set-AzServiceBusRule</span></span>

## <span data-ttu-id="62ed9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="62ed9-102">SYNOPSIS</span></span>
<span data-ttu-id="62ed9-103">Frissíti a megadott szabály leírását a megadott előfizetéshez.</span><span class="sxs-lookup"><span data-stu-id="62ed9-103">Updates the specified rule description for the given subscription.</span></span>

## <span data-ttu-id="62ed9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="62ed9-104">SYNTAX</span></span>

```
Set-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-InputObject] <PSRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62ed9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="62ed9-105">DESCRIPTION</span></span>
<span data-ttu-id="62ed9-106">A **set-AzServiceBusRule** parancsmag frissíti az adott előfizetés meghatározott szabályának leírását.</span><span class="sxs-lookup"><span data-stu-id="62ed9-106">The **Set-AzServiceBusRule** cmdlet updates the description for the specified rule of the given subscription.</span></span>

## <span data-ttu-id="62ed9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="62ed9-107">EXAMPLES</span></span>

### <span data-ttu-id="62ed9-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="62ed9-108">Example 1</span></span>
```
PS C:\> $getRule = Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
PS C:\> $getRule.SqlFilter.SqlExpression = "mysqlexpression='condition'"
PS C:\> $setRule = Set-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -InputObject $getRule
```

<span data-ttu-id="62ed9-109">Az előfizetéshez tartozó szabály SQL Expression **mysqlexpression = "Condition" ("feltétel")** frissítése a `SBRule` `SBSubscription` témakörben `SBTopic`</span><span class="sxs-lookup"><span data-stu-id="62ed9-109">Updates the sql expression **mysqlexpression='condition'** of the rule `SBRule` of the subscription `SBSubscription` in Topic `SBTopic`</span></span>

## <span data-ttu-id="62ed9-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="62ed9-110">PARAMETERS</span></span>

### <span data-ttu-id="62ed9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62ed9-111">-DefaultProfile</span></span>
<span data-ttu-id="62ed9-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="62ed9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62ed9-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="62ed9-113">-InputObject</span></span>
<span data-ttu-id="62ed9-114">ServiceBus szabályok definíciója</span><span class="sxs-lookup"><span data-stu-id="62ed9-114">ServiceBus Rules definition.</span></span>

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

### <span data-ttu-id="62ed9-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="62ed9-115">-Name</span></span>
<span data-ttu-id="62ed9-116">Szabály neve.</span><span class="sxs-lookup"><span data-stu-id="62ed9-116">Rule Name.</span></span>

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

### <span data-ttu-id="62ed9-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="62ed9-117">-Namespace</span></span>
<span data-ttu-id="62ed9-118">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="62ed9-118">Namespace Name.</span></span>

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

### <span data-ttu-id="62ed9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62ed9-119">-ResourceGroupName</span></span>
<span data-ttu-id="62ed9-120">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="62ed9-120">The name of the resource group</span></span>

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

### <span data-ttu-id="62ed9-121">-Előfizetés</span><span class="sxs-lookup"><span data-stu-id="62ed9-121">-Subscription</span></span>
<span data-ttu-id="62ed9-122">Előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="62ed9-122">Subscription Name.</span></span>

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

### <span data-ttu-id="62ed9-123">-Topic</span><span class="sxs-lookup"><span data-stu-id="62ed9-123">-Topic</span></span>
<span data-ttu-id="62ed9-124">A téma neve</span><span class="sxs-lookup"><span data-stu-id="62ed9-124">Topic Name.</span></span>

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

### <span data-ttu-id="62ed9-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="62ed9-125">-Confirm</span></span>
<span data-ttu-id="62ed9-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="62ed9-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62ed9-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62ed9-127">-WhatIf</span></span>
<span data-ttu-id="62ed9-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="62ed9-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62ed9-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="62ed9-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62ed9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62ed9-130">CommonParameters</span></span>
<span data-ttu-id="62ed9-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="62ed9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62ed9-132">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62ed9-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62ed9-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="62ed9-133">INPUTS</span></span>

### <span data-ttu-id="62ed9-134">System. String</span><span class="sxs-lookup"><span data-stu-id="62ed9-134">System.String</span></span>

### <span data-ttu-id="62ed9-135">Microsoft. Azure. Command. ServiceBus. models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="62ed9-135">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="62ed9-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="62ed9-136">OUTPUTS</span></span>

### <span data-ttu-id="62ed9-137">Microsoft. Azure. Command. ServiceBus. models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="62ed9-137">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="62ed9-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="62ed9-138">NOTES</span></span>

## <span data-ttu-id="62ed9-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="62ed9-139">RELATED LINKS</span></span>
