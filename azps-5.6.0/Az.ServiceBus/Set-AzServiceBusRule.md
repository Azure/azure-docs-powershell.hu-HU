---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/set-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusRule.md
ms.openlocfilehash: 2caf2ccfe0d3428515812aa2dfeafc1237f820f5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933410"
---
# <span data-ttu-id="0d212-101">Set-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="0d212-101">Set-AzServiceBusRule</span></span>

## <span data-ttu-id="0d212-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d212-102">SYNOPSIS</span></span>
<span data-ttu-id="0d212-103">Frissíti az adott előfizetéshez megadott szabályleírást.</span><span class="sxs-lookup"><span data-stu-id="0d212-103">Updates the specified rule description for the given subscription.</span></span>

## <span data-ttu-id="0d212-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0d212-104">SYNTAX</span></span>

```
Set-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-InputObject] <PSRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d212-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0d212-105">DESCRIPTION</span></span>
<span data-ttu-id="0d212-106">A **Set-AzServiceBusRule** parancsmag frissíti a megadott előfizetési szabály leírását.</span><span class="sxs-lookup"><span data-stu-id="0d212-106">The **Set-AzServiceBusRule** cmdlet updates the description for the specified rule of the given subscription.</span></span>

## <span data-ttu-id="0d212-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0d212-107">EXAMPLES</span></span>

### <span data-ttu-id="0d212-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="0d212-108">Example 1</span></span>
```
PS C:\> $getRule = Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
PS C:\> $getRule.SqlFilter.SqlExpression = "mysqlexpression='condition'"
PS C:\> $setRule = Set-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -InputObject $getRule
```

<span data-ttu-id="0d212-109">Frissíti az előfizetés **szabályának mysqlexpression='condition'** sql-kifejezését a `SBRule` `SBSubscription` Topicban `SBTopic`</span><span class="sxs-lookup"><span data-stu-id="0d212-109">Updates the sql expression **mysqlexpression='condition'** of the rule `SBRule` of the subscription `SBSubscription` in Topic `SBTopic`</span></span>

## <span data-ttu-id="0d212-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0d212-110">PARAMETERS</span></span>

### <span data-ttu-id="0d212-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d212-111">-DefaultProfile</span></span>
<span data-ttu-id="0d212-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0d212-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d212-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0d212-113">-InputObject</span></span>
<span data-ttu-id="0d212-114">ServiceBus-szabályok definíciója.</span><span class="sxs-lookup"><span data-stu-id="0d212-114">ServiceBus Rules definition.</span></span>

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

### <span data-ttu-id="0d212-115">-Name</span><span class="sxs-lookup"><span data-stu-id="0d212-115">-Name</span></span>
<span data-ttu-id="0d212-116">Szabály neve.</span><span class="sxs-lookup"><span data-stu-id="0d212-116">Rule Name.</span></span>

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

### <span data-ttu-id="0d212-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="0d212-117">-Namespace</span></span>
<span data-ttu-id="0d212-118">Névtér neve.</span><span class="sxs-lookup"><span data-stu-id="0d212-118">Namespace Name.</span></span>

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

### <span data-ttu-id="0d212-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d212-119">-ResourceGroupName</span></span>
<span data-ttu-id="0d212-120">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="0d212-120">The name of the resource group</span></span>

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

### <span data-ttu-id="0d212-121">-Előfizetés</span><span class="sxs-lookup"><span data-stu-id="0d212-121">-Subscription</span></span>
<span data-ttu-id="0d212-122">Előfizetés neve.</span><span class="sxs-lookup"><span data-stu-id="0d212-122">Subscription Name.</span></span>

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

### <span data-ttu-id="0d212-123">-Topic</span><span class="sxs-lookup"><span data-stu-id="0d212-123">-Topic</span></span>
<span data-ttu-id="0d212-124">Témakör neve.</span><span class="sxs-lookup"><span data-stu-id="0d212-124">Topic Name.</span></span>

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

### <span data-ttu-id="0d212-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0d212-125">-Confirm</span></span>
<span data-ttu-id="0d212-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0d212-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d212-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d212-127">-WhatIf</span></span>
<span data-ttu-id="0d212-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0d212-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d212-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0d212-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d212-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d212-130">CommonParameters</span></span>
<span data-ttu-id="0d212-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d212-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d212-132">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d212-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d212-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0d212-133">INPUTS</span></span>

### <span data-ttu-id="0d212-134">System.String</span><span class="sxs-lookup"><span data-stu-id="0d212-134">System.String</span></span>

### <span data-ttu-id="0d212-135">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="0d212-135">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="0d212-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0d212-136">OUTPUTS</span></span>

### <span data-ttu-id="0d212-137">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="0d212-137">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="0d212-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0d212-138">NOTES</span></span>

## <span data-ttu-id="0d212-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0d212-139">RELATED LINKS</span></span>
