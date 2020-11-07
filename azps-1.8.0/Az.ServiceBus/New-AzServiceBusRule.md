---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusRule.md
ms.openlocfilehash: 869bfdaa7ff772980b7acf1caee6c7d6a8784d37
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669180"
---
# <span data-ttu-id="eb8ca-101">New-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="eb8ca-101">New-AzServiceBusRule</span></span>

## <span data-ttu-id="eb8ca-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="eb8ca-102">SYNOPSIS</span></span>
<span data-ttu-id="eb8ca-103">Új szabály létrehozása a témakör adott előfizetéséhez.</span><span class="sxs-lookup"><span data-stu-id="eb8ca-103">Creates a new rule for a given Subscription of Topic.</span></span> 

## <span data-ttu-id="eb8ca-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="eb8ca-104">SYNTAX</span></span>

### <span data-ttu-id="eb8ca-105">RulePropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="eb8ca-105">RulePropertiesSet (Default)</span></span>
```
New-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb8ca-106">RuleActionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="eb8ca-106">RuleActionPropertiesSet</span></span>
```
New-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> -ActionSqlExpression <String>
 [-RequiresPreprocessing] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb8ca-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="eb8ca-107">DESCRIPTION</span></span>
<span data-ttu-id="eb8ca-108">A **New-AzServiceBusRule** parancsmag új szabályt hoz létre az adott előfizetéshez.</span><span class="sxs-lookup"><span data-stu-id="eb8ca-108">The **New-AzServiceBusRule** cmdlet Creates a new rule for given subscription.</span></span>

## <span data-ttu-id="eb8ca-109">Példák</span><span class="sxs-lookup"><span data-stu-id="eb8ca-109">EXAMPLES</span></span>

### <span data-ttu-id="eb8ca-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="eb8ca-110">Example 1</span></span>
```
PS C:\> New-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'"
```

<span data-ttu-id="eb8ca-111">A New-AzServiceBusRule parancsmag új szabályt hoz létre a megadott előfizetéshez.</span><span class="sxs-lookup"><span data-stu-id="eb8ca-111">The New-AzServiceBusRule cmdlet creates a new rule for the specified Subscription.</span></span>

### <span data-ttu-id="eb8ca-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="eb8ca-112">Example 2</span></span>
```
PS C:\> New-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'" -ActionSqlExpression "SET myAction='test'" -RequiresPreprocessing
```

<span data-ttu-id="eb8ca-113">Az New-AzServiceBusRule parancsmag új szabályt hoz létre a megadott előfizetéshez a ActionFilter.</span><span class="sxs-lookup"><span data-stu-id="eb8ca-113">The New-AzServiceBusRule cmdlet creates a new rule for the specified Subscription with ActionFilter.</span></span>

## <span data-ttu-id="eb8ca-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="eb8ca-114">PARAMETERS</span></span>

### <span data-ttu-id="eb8ca-115">-ActionSqlExpression</span><span class="sxs-lookup"><span data-stu-id="eb8ca-115">-ActionSqlExpression</span></span>
<span data-ttu-id="eb8ca-116">A műveleti SqlFillter kifejezés</span><span class="sxs-lookup"><span data-stu-id="eb8ca-116">Action SqlFillter Expression</span></span>

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

### <span data-ttu-id="eb8ca-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb8ca-117">-DefaultProfile</span></span>
<span data-ttu-id="eb8ca-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="eb8ca-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb8ca-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="eb8ca-119">-Name</span></span>
<span data-ttu-id="eb8ca-120">Szabály neve</span><span class="sxs-lookup"><span data-stu-id="eb8ca-120">Rule Name</span></span>

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

### <span data-ttu-id="eb8ca-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="eb8ca-121">-Namespace</span></span>
<span data-ttu-id="eb8ca-122">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="eb8ca-122">Namespace Name</span></span>

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

### <span data-ttu-id="eb8ca-123">-RequiresPreprocessing</span><span class="sxs-lookup"><span data-stu-id="eb8ca-123">-RequiresPreprocessing</span></span>
<span data-ttu-id="eb8ca-124">Előfeldolgozást igénylő művelet</span><span class="sxs-lookup"><span data-stu-id="eb8ca-124">Action Requires Preprocessing</span></span>

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

### <span data-ttu-id="eb8ca-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb8ca-125">-ResourceGroupName</span></span>
<span data-ttu-id="eb8ca-126">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="eb8ca-126">The name of the resource group</span></span>

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

### <span data-ttu-id="eb8ca-127">-SqlExpression</span><span class="sxs-lookup"><span data-stu-id="eb8ca-127">-SqlExpression</span></span>
<span data-ttu-id="eb8ca-128">SQL szűrni kifejezés</span><span class="sxs-lookup"><span data-stu-id="eb8ca-128">Sql Fillter Expression</span></span>

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

### <span data-ttu-id="eb8ca-129">-Előfizetés</span><span class="sxs-lookup"><span data-stu-id="eb8ca-129">-Subscription</span></span>
<span data-ttu-id="eb8ca-130">Előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="eb8ca-130">Subscription Name</span></span>

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

### <span data-ttu-id="eb8ca-131">-Topic</span><span class="sxs-lookup"><span data-stu-id="eb8ca-131">-Topic</span></span>
<span data-ttu-id="eb8ca-132">Téma neve</span><span class="sxs-lookup"><span data-stu-id="eb8ca-132">Topic Name</span></span>

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

### <span data-ttu-id="eb8ca-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="eb8ca-133">-Confirm</span></span>
<span data-ttu-id="eb8ca-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="eb8ca-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb8ca-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb8ca-135">-WhatIf</span></span>
<span data-ttu-id="eb8ca-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="eb8ca-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb8ca-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="eb8ca-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb8ca-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb8ca-138">CommonParameters</span></span>
<span data-ttu-id="eb8ca-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="eb8ca-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb8ca-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb8ca-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb8ca-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="eb8ca-141">INPUTS</span></span>

### <span data-ttu-id="eb8ca-142">System. String</span><span class="sxs-lookup"><span data-stu-id="eb8ca-142">System.String</span></span>

## <span data-ttu-id="eb8ca-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eb8ca-143">OUTPUTS</span></span>

### <span data-ttu-id="eb8ca-144">Microsoft. Azure. Command. ServiceBus. models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="eb8ca-144">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="eb8ca-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="eb8ca-145">NOTES</span></span>

## <span data-ttu-id="eb8ca-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eb8ca-146">RELATED LINKS</span></span>
