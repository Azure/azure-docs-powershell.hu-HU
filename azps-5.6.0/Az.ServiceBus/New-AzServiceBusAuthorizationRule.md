---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/new-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: 08560730438fe5bca85a78e8a7f75f427c07de0d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932242"
---
# <span data-ttu-id="cd6cf-101">New-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="cd6cf-101">New-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="cd6cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd6cf-102">SYNOPSIS</span></span>
<span data-ttu-id="cd6cf-103">Új engedélyezési szabályt hoz létre a megadott Service Bus névterhez, várólistához vagy témakörhez.</span><span class="sxs-lookup"><span data-stu-id="cd6cf-103">Creates a new authorization rule for the specified Service Bus given Namespace or Queue or Topic.</span></span>

## <span data-ttu-id="cd6cf-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cd6cf-104">SYNTAX</span></span>

### <span data-ttu-id="cd6cf-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cd6cf-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd6cf-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="cd6cf-106">QueueAuthorizationRuleSet</span></span>
```
New-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cd6cf-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="cd6cf-107">TopicAuthorizationRuleSet</span></span>
```
New-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cd6cf-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cd6cf-108">DESCRIPTION</span></span>
<span data-ttu-id="cd6cf-109">A **New-AzServiceBusAuthorizationRule** parancsmag létrehoz egy új engedélyezési szabályt a szolgáltatás-busz névterére vagy várólistájára vagy témájára.</span><span class="sxs-lookup"><span data-stu-id="cd6cf-109">The **New-AzServiceBusAuthorizationRule** cmdlet creates a new authorization rule for the specified Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="cd6cf-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cd6cf-110">EXAMPLES</span></span>

### <span data-ttu-id="cd6cf-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="cd6cf-111">Example 1</span></span>
```
PS C:\> New-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="cd6cf-112">A `AuthoRule1` **névtérhez hallgató és** küldési jogokkal hozza  `SB-Example1` létre.</span><span class="sxs-lookup"><span data-stu-id="cd6cf-112">Creates `AuthoRule1` with **Listen** and **Send** rights for the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="cd6cf-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="cd6cf-113">Example 2</span></span>
```
PS C:\> New-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="cd6cf-114">A `AuthoRule1` **várólistára vonatkozó Figyelt és** Küldés jogosultságokkal hozza  `SBQueue` létre.</span><span class="sxs-lookup"><span data-stu-id="cd6cf-114">Creates `AuthoRule1` with **Listen** and **Send** rights for the queue `SBQueue`.</span></span>

### <span data-ttu-id="cd6cf-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="cd6cf-115">Example 3</span></span>
```
PS C:\> New-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="cd6cf-116">A `AuthoRule1` témakör  **figyelt és** küldési jogokkal hozza `SBTopic` létre.</span><span class="sxs-lookup"><span data-stu-id="cd6cf-116">Creates `AuthoRule1` with **Listen** and **Send** rights for the topic `SBTopic`.</span></span>

## <span data-ttu-id="cd6cf-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cd6cf-117">PARAMETERS</span></span>

### <span data-ttu-id="cd6cf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd6cf-118">-DefaultProfile</span></span>
<span data-ttu-id="cd6cf-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cd6cf-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd6cf-120">-Name</span><span class="sxs-lookup"><span data-stu-id="cd6cf-120">-Name</span></span>
<span data-ttu-id="cd6cf-121">AuthorizationRule Name</span><span class="sxs-lookup"><span data-stu-id="cd6cf-121">AuthorizationRule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd6cf-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="cd6cf-122">-Namespace</span></span>
<span data-ttu-id="cd6cf-123">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="cd6cf-123">Namespace Name</span></span>

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

### <span data-ttu-id="cd6cf-124">-Queue</span><span class="sxs-lookup"><span data-stu-id="cd6cf-124">-Queue</span></span>
<span data-ttu-id="cd6cf-125">Várólistán lévő név</span><span class="sxs-lookup"><span data-stu-id="cd6cf-125">Queue Name</span></span>

```yaml
Type: System.String
Parameter Sets: QueueAuthorizationRuleSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd6cf-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd6cf-126">-ResourceGroupName</span></span>
<span data-ttu-id="cd6cf-127">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="cd6cf-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd6cf-128">-Rights</span><span class="sxs-lookup"><span data-stu-id="cd6cf-128">-Rights</span></span>
<span data-ttu-id="cd6cf-129">Jogok, például "Figyel", "Küldés", "Kezelés"</span><span class="sxs-lookup"><span data-stu-id="cd6cf-129">Rights, e.g. "Listen","Send","Manage"</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Listen, Send, Manage

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd6cf-130">-Topic</span><span class="sxs-lookup"><span data-stu-id="cd6cf-130">-Topic</span></span>
<span data-ttu-id="cd6cf-131">Témakör neve</span><span class="sxs-lookup"><span data-stu-id="cd6cf-131">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: TopicAuthorizationRuleSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd6cf-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cd6cf-132">-Confirm</span></span>
<span data-ttu-id="cd6cf-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="cd6cf-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd6cf-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd6cf-134">-WhatIf</span></span>
<span data-ttu-id="cd6cf-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="cd6cf-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd6cf-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cd6cf-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd6cf-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd6cf-137">CommonParameters</span></span>
<span data-ttu-id="cd6cf-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd6cf-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd6cf-139">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd6cf-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd6cf-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cd6cf-140">INPUTS</span></span>

### <span data-ttu-id="cd6cf-141">System.String</span><span class="sxs-lookup"><span data-stu-id="cd6cf-141">System.String</span></span>

### <span data-ttu-id="cd6cf-142">System.String[]</span><span class="sxs-lookup"><span data-stu-id="cd6cf-142">System.String[]</span></span>

## <span data-ttu-id="cd6cf-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd6cf-143">OUTPUTS</span></span>

### <span data-ttu-id="cd6cf-144">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="cd6cf-144">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="cd6cf-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cd6cf-145">NOTES</span></span>

## <span data-ttu-id="cd6cf-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cd6cf-146">RELATED LINKS</span></span>
