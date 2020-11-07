---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusRule.md
ms.openlocfilehash: 4fb10e2bb438cbc4f40936f9f9ead5c0bb36d861
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680225"
---
# <span data-ttu-id="0d8c3-101">Set-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="0d8c3-101">Set-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="0d8c3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0d8c3-102">SYNOPSIS</span></span>
<span data-ttu-id="0d8c3-103">Frissíti a megadott szabály leírását a megadott előfizetéshez.</span><span class="sxs-lookup"><span data-stu-id="0d8c3-103">Updates the specified rule description for the given subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d8c3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0d8c3-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-InputObject] <RulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d8c3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0d8c3-105">DESCRIPTION</span></span>
<span data-ttu-id="0d8c3-106">A **set-AzureRmServiceBusRule** parancsmag frissíti az adott előfizetés meghatározott szabályának leírását.</span><span class="sxs-lookup"><span data-stu-id="0d8c3-106">The **Set-AzureRmServiceBusRule** cmdlet updates the description for the specified rule of the given subscription.</span></span>

## <span data-ttu-id="0d8c3-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0d8c3-107">EXAMPLES</span></span>

### <span data-ttu-id="0d8c3-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="0d8c3-108">Example 1</span></span>
```
PS C:\> $getRule = Get-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
PS C:\> $getRule.SqlFilter.SqlExpression = "mysqlexpression='condition'"
PS C:\> $setRule = Set-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -InputObject $getRule
```

<span data-ttu-id="0d8c3-109">a témakörben szereplő előfizetéshez tartozó sqlexpression **mysqlexpression = "Condition" ("feltétel"** ) frissítése `SBEule` `SBSubscription``SBTopic`</span><span class="sxs-lookup"><span data-stu-id="0d8c3-109">updates the sqlexpression **mysqlexpression='condition'** of the rule `SBEule` of the subscription `SBSubscription` in Topic `SBTopic`</span></span>

## <span data-ttu-id="0d8c3-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0d8c3-110">PARAMETERS</span></span>

### <span data-ttu-id="0d8c3-111">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0d8c3-111">-Confirm</span></span>
<span data-ttu-id="0d8c3-112">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0d8c3-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d8c3-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0d8c3-113">-InputObject</span></span>
<span data-ttu-id="0d8c3-114">ServiceBus szabályok definíciója</span><span class="sxs-lookup"><span data-stu-id="0d8c3-114">ServiceBus Rules definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.RulesAttributes
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d8c3-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0d8c3-115">-Name</span></span>
<span data-ttu-id="0d8c3-116">Szabály neve.</span><span class="sxs-lookup"><span data-stu-id="0d8c3-116">Rule Name.</span></span>

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

### <span data-ttu-id="0d8c3-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="0d8c3-117">-Namespace</span></span>
<span data-ttu-id="0d8c3-118">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="0d8c3-118">Namespace Name.</span></span>

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

### <span data-ttu-id="0d8c3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d8c3-119">-ResourceGroupName</span></span>
<span data-ttu-id="0d8c3-120">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="0d8c3-120">The name of the resource group</span></span>

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

### <span data-ttu-id="0d8c3-121">-Előfizetés</span><span class="sxs-lookup"><span data-stu-id="0d8c3-121">-Subscription</span></span>
<span data-ttu-id="0d8c3-122">Előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="0d8c3-122">Subscription Name.</span></span>

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

### <span data-ttu-id="0d8c3-123">-Topic</span><span class="sxs-lookup"><span data-stu-id="0d8c3-123">-Topic</span></span>
<span data-ttu-id="0d8c3-124">A téma neve</span><span class="sxs-lookup"><span data-stu-id="0d8c3-124">Topic Name.</span></span>

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

### <span data-ttu-id="0d8c3-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d8c3-125">-WhatIf</span></span>
<span data-ttu-id="0d8c3-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0d8c3-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d8c3-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0d8c3-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d8c3-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d8c3-128">-DefaultProfile</span></span>
<span data-ttu-id="0d8c3-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0d8c3-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d8c3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d8c3-130">CommonParameters</span></span>
<span data-ttu-id="0d8c3-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0d8c3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d8c3-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d8c3-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d8c3-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0d8c3-133">INPUTS</span></span>

### <span data-ttu-id="0d8c3-134">System. String</span><span class="sxs-lookup"><span data-stu-id="0d8c3-134">System.String</span></span>
<span data-ttu-id="0d8c3-135">Microsoft. Azure. Command. ServiceBus. models. RulesAttributes</span><span class="sxs-lookup"><span data-stu-id="0d8c3-135">Microsoft.Azure.Commands.ServiceBus.Models.RulesAttributes</span></span>

## <span data-ttu-id="0d8c3-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0d8c3-136">OUTPUTS</span></span>

### <span data-ttu-id="0d8c3-137">Microsoft. Azure. Command. ServiceBus. models. RulesAttributes</span><span class="sxs-lookup"><span data-stu-id="0d8c3-137">Microsoft.Azure.Commands.ServiceBus.Models.RulesAttributes</span></span>

## <span data-ttu-id="0d8c3-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0d8c3-138">NOTES</span></span>

## <span data-ttu-id="0d8c3-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0d8c3-139">RELATED LINKS</span></span>

