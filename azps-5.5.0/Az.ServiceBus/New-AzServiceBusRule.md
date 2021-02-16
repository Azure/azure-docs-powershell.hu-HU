---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusRule.md
ms.openlocfilehash: d667049fb512545aebfd9681b3ad3d9f44651951
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100168883"
---
# <span data-ttu-id="8e7c4-101">New-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="8e7c4-101">New-AzServiceBusRule</span></span>

## <span data-ttu-id="8e7c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e7c4-102">SYNOPSIS</span></span>
<span data-ttu-id="8e7c4-103">Új szabályt hoz létre egy adott témakör-előfizetéshez.</span><span class="sxs-lookup"><span data-stu-id="8e7c4-103">Creates a new rule for a given Subscription of Topic.</span></span> 

## <span data-ttu-id="8e7c4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8e7c4-104">SYNTAX</span></span>

### <span data-ttu-id="8e7c4-105">RulePropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8e7c4-105">RulePropertiesSet (Default)</span></span>
```
New-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e7c4-106">RuleActionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="8e7c4-106">RuleActionPropertiesSet</span></span>
```
New-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> -ActionSqlExpression <String>
 [-RequiresPreprocessing] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e7c4-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8e7c4-107">DESCRIPTION</span></span>
<span data-ttu-id="8e7c4-108">A **New-AzServiceBusRule** parancsmag Létrehoz egy új szabályt az adott előfizetéshez.</span><span class="sxs-lookup"><span data-stu-id="8e7c4-108">The **New-AzServiceBusRule** cmdlet Creates a new rule for given subscription.</span></span>

## <span data-ttu-id="8e7c4-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8e7c4-109">EXAMPLES</span></span>

### <span data-ttu-id="8e7c4-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="8e7c4-110">Example 1</span></span>
```
PS C:\> New-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'"
```

<span data-ttu-id="8e7c4-111">A New-AzServiceBusRule parancsmag létrehoz egy új szabályt a megadott Előfizetéshez.</span><span class="sxs-lookup"><span data-stu-id="8e7c4-111">The New-AzServiceBusRule cmdlet creates a new rule for the specified Subscription.</span></span>

### <span data-ttu-id="8e7c4-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="8e7c4-112">Example 2</span></span>
```
PS C:\> New-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'" -ActionSqlExpression "SET myAction='test'" -RequiresPreprocessing
```

<span data-ttu-id="8e7c4-113">A New-AzServiceBusRule parancsmag létrehoz egy új szabályt a megadott ActionFilter-előfizetéshez.</span><span class="sxs-lookup"><span data-stu-id="8e7c4-113">The New-AzServiceBusRule cmdlet creates a new rule for the specified Subscription with ActionFilter.</span></span>

## <span data-ttu-id="8e7c4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e7c4-114">PARAMETERS</span></span>

### <span data-ttu-id="8e7c4-115">-ActionSqlExpression</span><span class="sxs-lookup"><span data-stu-id="8e7c4-115">-ActionSqlExpression</span></span>
<span data-ttu-id="8e7c4-116">Action SqlFilter Expression</span><span class="sxs-lookup"><span data-stu-id="8e7c4-116">Action SqlFilter Expression</span></span>

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

### <span data-ttu-id="8e7c4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e7c4-117">-DefaultProfile</span></span>
<span data-ttu-id="8e7c4-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8e7c4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e7c4-119">-Name</span><span class="sxs-lookup"><span data-stu-id="8e7c4-119">-Name</span></span>
<span data-ttu-id="8e7c4-120">Szabály neve</span><span class="sxs-lookup"><span data-stu-id="8e7c4-120">Rule Name</span></span>

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

### <span data-ttu-id="8e7c4-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="8e7c4-121">-Namespace</span></span>
<span data-ttu-id="8e7c4-122">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="8e7c4-122">Namespace Name</span></span>

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

### <span data-ttu-id="8e7c4-123">-RequiresPreprocessing</span><span class="sxs-lookup"><span data-stu-id="8e7c4-123">-RequiresPreprocessing</span></span>
<span data-ttu-id="8e7c4-124">A művelethez előfeldolgozás szükséges</span><span class="sxs-lookup"><span data-stu-id="8e7c4-124">Action Requires Preprocessing</span></span>

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

### <span data-ttu-id="8e7c4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e7c4-125">-ResourceGroupName</span></span>
<span data-ttu-id="8e7c4-126">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="8e7c4-126">The name of the resource group</span></span>

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

### <span data-ttu-id="8e7c4-127">-SqlExpression</span><span class="sxs-lookup"><span data-stu-id="8e7c4-127">-SqlExpression</span></span>
<span data-ttu-id="8e7c4-128">Sql Filter Expression</span><span class="sxs-lookup"><span data-stu-id="8e7c4-128">Sql Filter Expression</span></span>

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

### <span data-ttu-id="8e7c4-129">-Előfizetés</span><span class="sxs-lookup"><span data-stu-id="8e7c4-129">-Subscription</span></span>
<span data-ttu-id="8e7c4-130">Előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="8e7c4-130">Subscription Name</span></span>

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

### <span data-ttu-id="8e7c4-131">-Topic</span><span class="sxs-lookup"><span data-stu-id="8e7c4-131">-Topic</span></span>
<span data-ttu-id="8e7c4-132">Témakör neve</span><span class="sxs-lookup"><span data-stu-id="8e7c4-132">Topic Name</span></span>

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

### <span data-ttu-id="8e7c4-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8e7c4-133">-Confirm</span></span>
<span data-ttu-id="8e7c4-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8e7c4-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e7c4-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e7c4-135">-WhatIf</span></span>
<span data-ttu-id="8e7c4-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8e7c4-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e7c4-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8e7c4-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e7c4-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e7c4-138">CommonParameters</span></span>
<span data-ttu-id="8e7c4-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e7c4-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e7c4-140">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e7c4-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e7c4-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8e7c4-141">INPUTS</span></span>

### <span data-ttu-id="8e7c4-142">System.String</span><span class="sxs-lookup"><span data-stu-id="8e7c4-142">System.String</span></span>

## <span data-ttu-id="8e7c4-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e7c4-143">OUTPUTS</span></span>

### <span data-ttu-id="8e7c4-144">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="8e7c4-144">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="8e7c4-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8e7c4-145">NOTES</span></span>

## <span data-ttu-id="8e7c4-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8e7c4-146">RELATED LINKS</span></span>
