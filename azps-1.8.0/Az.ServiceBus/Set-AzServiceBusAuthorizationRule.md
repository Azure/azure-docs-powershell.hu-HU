---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: e9ab4d4d2fb2c60561d85582f2dda922ba9eaae1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669153"
---
# <span data-ttu-id="27791-101">Set-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="27791-101">Set-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="27791-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="27791-102">SYNOPSIS</span></span>
<span data-ttu-id="27791-103">Frissíti a megadott engedélyezési szabály leírását a megadott szolgáltatási busz névterében vagy a várólistában.</span><span class="sxs-lookup"><span data-stu-id="27791-103">Updates the specified authorization rule description for the given Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="27791-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="27791-104">SYNTAX</span></span>

### <span data-ttu-id="27791-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="27791-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27791-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="27791-106">QueueAuthorizationRuleSet</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27791-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="27791-107">TopicAuthorizationRuleSet</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27791-108">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="27791-108">AuthoRuleInputObjectSet</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSSharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27791-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="27791-109">DESCRIPTION</span></span>
<span data-ttu-id="27791-110">A **set-AzServiceBusAuthorizationRule** parancsmag frissíti a megadott engedélyezési szabály leírását a megadott szolgáltatási busz névterében vagy a várólistában vagy a témakörben.</span><span class="sxs-lookup"><span data-stu-id="27791-110">The **Set-AzServiceBusAuthorizationRule** cmdlet updates the description for the specified authorization rule in the given Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="27791-111">Példák</span><span class="sxs-lookup"><span data-stu-id="27791-111">EXAMPLES</span></span>

### <span data-ttu-id="27791-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="27791-112">Example 1</span></span>
```
PS C:\> $authRuleObj = Get-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="27791-113">Eltávolítja a **Manage** (névtér) engedélyezési szabályának hozzáférési jogát `AuthoRule1` `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="27791-113">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in namespace `SB-Example1`.</span></span>

### <span data-ttu-id="27791-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="27791-114">Example 2</span></span>
```
PS C:\> $authRuleObj = Get-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="27791-115">Eltávolítja a **kezelés** lehetőséget az engedélyezési szabálynak a várólistában való elérési jogáról `AuthoRule1` `SBQueue` .</span><span class="sxs-lookup"><span data-stu-id="27791-115">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in queue `SBQueue`.</span></span>

### <span data-ttu-id="27791-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="27791-116">Example 2</span></span>
```
PS C:\> $authRuleObj = Get-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="27791-117">Eltávolítja a **kezelés** lehetőséget a témakör engedélyezési szabályának hozzáférési jogaiból `AuthoRule1` `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="27791-117">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in topic `SBTopic`.</span></span>

## <span data-ttu-id="27791-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="27791-118">PARAMETERS</span></span>

### <span data-ttu-id="27791-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27791-119">-DefaultProfile</span></span>
<span data-ttu-id="27791-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="27791-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27791-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="27791-121">-InputObject</span></span>
<span data-ttu-id="27791-122">ServiceBus AuthorizationRule objektum</span><span class="sxs-lookup"><span data-stu-id="27791-122">ServiceBus AuthorizationRule Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases: AuthRuleObj

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: AuthRuleObj

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="27791-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="27791-123">-Name</span></span>
<span data-ttu-id="27791-124">AuthorizationRule neve</span><span class="sxs-lookup"><span data-stu-id="27791-124">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="27791-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="27791-125">-Namespace</span></span>
<span data-ttu-id="27791-126">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="27791-126">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27791-127">-Queue (várólista)</span><span class="sxs-lookup"><span data-stu-id="27791-127">-Queue</span></span>
<span data-ttu-id="27791-128">Várólista neve</span><span class="sxs-lookup"><span data-stu-id="27791-128">Queue Name</span></span>

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

### <span data-ttu-id="27791-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27791-129">-ResourceGroupName</span></span>
<span data-ttu-id="27791-130">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="27791-130">Resource Group Name</span></span>

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

### <span data-ttu-id="27791-131">– Jogok</span><span class="sxs-lookup"><span data-stu-id="27791-131">-Rights</span></span>
<span data-ttu-id="27791-132">Jogok, például @ ("Figyelj", "Küldés", "kezelés")</span><span class="sxs-lookup"><span data-stu-id="27791-132">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: System.String[]
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases:
Accepted values: Listen, Send, Manage

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27791-133">-Topic</span><span class="sxs-lookup"><span data-stu-id="27791-133">-Topic</span></span>
<span data-ttu-id="27791-134">Téma neve</span><span class="sxs-lookup"><span data-stu-id="27791-134">Topic Name</span></span>

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

### <span data-ttu-id="27791-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="27791-135">-Confirm</span></span>
<span data-ttu-id="27791-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="27791-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27791-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27791-137">-WhatIf</span></span>
<span data-ttu-id="27791-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="27791-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27791-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="27791-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27791-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27791-140">CommonParameters</span></span>
<span data-ttu-id="27791-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="27791-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27791-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27791-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27791-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="27791-143">INPUTS</span></span>

### <span data-ttu-id="27791-144">System. String</span><span class="sxs-lookup"><span data-stu-id="27791-144">System.String</span></span>

### <span data-ttu-id="27791-145">Microsoft. Azure. Command. ServiceBus. models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="27791-145">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

### <span data-ttu-id="27791-146">System. string []</span><span class="sxs-lookup"><span data-stu-id="27791-146">System.String[]</span></span>

## <span data-ttu-id="27791-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="27791-147">OUTPUTS</span></span>

### <span data-ttu-id="27791-148">Microsoft. Azure. Command. ServiceBus. models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="27791-148">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="27791-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="27791-149">NOTES</span></span>

## <span data-ttu-id="27791-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="27791-150">RELATED LINKS</span></span>
