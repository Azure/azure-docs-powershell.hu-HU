---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusRule.md
ms.openlocfilehash: d667049fb512545aebfd9681b3ad3d9f44651951
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181390"
---
# <span data-ttu-id="59467-101">New-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="59467-101">New-AzServiceBusRule</span></span>

## <span data-ttu-id="59467-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="59467-102">SYNOPSIS</span></span>
<span data-ttu-id="59467-103">Új szabály létrehozása a témakör adott előfizetéséhez.</span><span class="sxs-lookup"><span data-stu-id="59467-103">Creates a new rule for a given Subscription of Topic.</span></span> 

## <span data-ttu-id="59467-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="59467-104">SYNTAX</span></span>

### <span data-ttu-id="59467-105">RulePropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="59467-105">RulePropertiesSet (Default)</span></span>
```
New-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59467-106">RuleActionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="59467-106">RuleActionPropertiesSet</span></span>
```
New-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> -ActionSqlExpression <String>
 [-RequiresPreprocessing] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59467-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="59467-107">DESCRIPTION</span></span>
<span data-ttu-id="59467-108">A **New-AzServiceBusRule** parancsmag új szabályt hoz létre az adott előfizetéshez.</span><span class="sxs-lookup"><span data-stu-id="59467-108">The **New-AzServiceBusRule** cmdlet Creates a new rule for given subscription.</span></span>

## <span data-ttu-id="59467-109">Példák</span><span class="sxs-lookup"><span data-stu-id="59467-109">EXAMPLES</span></span>

### <span data-ttu-id="59467-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="59467-110">Example 1</span></span>
```
PS C:\> New-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'"
```

<span data-ttu-id="59467-111">A New-AzServiceBusRule parancsmag új szabályt hoz létre a megadott előfizetéshez.</span><span class="sxs-lookup"><span data-stu-id="59467-111">The New-AzServiceBusRule cmdlet creates a new rule for the specified Subscription.</span></span>

### <span data-ttu-id="59467-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="59467-112">Example 2</span></span>
```
PS C:\> New-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'" -ActionSqlExpression "SET myAction='test'" -RequiresPreprocessing
```

<span data-ttu-id="59467-113">Az New-AzServiceBusRule parancsmag új szabályt hoz létre a megadott előfizetéshez a ActionFilter.</span><span class="sxs-lookup"><span data-stu-id="59467-113">The New-AzServiceBusRule cmdlet creates a new rule for the specified Subscription with ActionFilter.</span></span>

## <span data-ttu-id="59467-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="59467-114">PARAMETERS</span></span>

### <span data-ttu-id="59467-115">-ActionSqlExpression</span><span class="sxs-lookup"><span data-stu-id="59467-115">-ActionSqlExpression</span></span>
<span data-ttu-id="59467-116">A műveleti SqlFilter kifejezés</span><span class="sxs-lookup"><span data-stu-id="59467-116">Action SqlFilter Expression</span></span>

```yaml
Type: System.String
Parameter Sets: RuleActionPropertiesSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59467-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59467-117">-DefaultProfile</span></span>
<span data-ttu-id="59467-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="59467-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59467-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="59467-119">-Name</span></span>
<span data-ttu-id="59467-120">Szabály neve</span><span class="sxs-lookup"><span data-stu-id="59467-120">Rule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59467-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="59467-121">-Namespace</span></span>
<span data-ttu-id="59467-122">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="59467-122">Namespace Name</span></span>

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

### <span data-ttu-id="59467-123">-RequiresPreprocessing</span><span class="sxs-lookup"><span data-stu-id="59467-123">-RequiresPreprocessing</span></span>
<span data-ttu-id="59467-124">Előfeldolgozást igénylő művelet</span><span class="sxs-lookup"><span data-stu-id="59467-124">Action Requires Preprocessing</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RuleActionPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59467-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59467-125">-ResourceGroupName</span></span>
<span data-ttu-id="59467-126">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="59467-126">The name of the resource group</span></span>

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

### <span data-ttu-id="59467-127">-SqlExpression</span><span class="sxs-lookup"><span data-stu-id="59467-127">-SqlExpression</span></span>
<span data-ttu-id="59467-128">SQL-szűrési kifejezés</span><span class="sxs-lookup"><span data-stu-id="59467-128">Sql Filter Expression</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59467-129">-Előfizetés</span><span class="sxs-lookup"><span data-stu-id="59467-129">-Subscription</span></span>
<span data-ttu-id="59467-130">Előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="59467-130">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59467-131">-Topic</span><span class="sxs-lookup"><span data-stu-id="59467-131">-Topic</span></span>
<span data-ttu-id="59467-132">Téma neve</span><span class="sxs-lookup"><span data-stu-id="59467-132">Topic Name</span></span>

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

### <span data-ttu-id="59467-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="59467-133">-Confirm</span></span>
<span data-ttu-id="59467-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="59467-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59467-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59467-135">-WhatIf</span></span>
<span data-ttu-id="59467-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="59467-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59467-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="59467-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59467-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59467-138">CommonParameters</span></span>
<span data-ttu-id="59467-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="59467-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59467-140">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59467-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59467-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="59467-141">INPUTS</span></span>

### <span data-ttu-id="59467-142">System. String</span><span class="sxs-lookup"><span data-stu-id="59467-142">System.String</span></span>

## <span data-ttu-id="59467-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="59467-143">OUTPUTS</span></span>

### <span data-ttu-id="59467-144">Microsoft. Azure. Command. ServiceBus. models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="59467-144">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="59467-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="59467-145">NOTES</span></span>

## <span data-ttu-id="59467-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="59467-146">RELATED LINKS</span></span>
