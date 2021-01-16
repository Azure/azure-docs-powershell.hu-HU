---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: da981d38f0833adc276a114c42def5d19322e0d9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357375"
---
# <span data-ttu-id="c00d5-101">Set-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c00d5-101">Set-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="c00d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c00d5-102">SYNOPSIS</span></span>
<span data-ttu-id="c00d5-103">Frissíti a szolgáltatási-busz névterének vagy várólistájának vagy témájának engedélyezési szabályának megadott leírását.</span><span class="sxs-lookup"><span data-stu-id="c00d5-103">Updates the specified authorization rule description for the given Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="c00d5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c00d5-104">SYNTAX</span></span>

### <span data-ttu-id="c00d5-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c00d5-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c00d5-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="c00d5-106">QueueAuthorizationRuleSet</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c00d5-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="c00d5-107">TopicAuthorizationRuleSet</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c00d5-108">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c00d5-108">AuthoRuleInputObjectSet</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSSharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c00d5-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c00d5-109">DESCRIPTION</span></span>
<span data-ttu-id="c00d5-110">A **Set-AzServiceBusAuthorizationRule** parancsmag frissíti a megadott engedélyezési szabály leírását a szolgáltatásbusz adott névterében vagy várólistáján vagy témakörében.</span><span class="sxs-lookup"><span data-stu-id="c00d5-110">The **Set-AzServiceBusAuthorizationRule** cmdlet updates the description for the specified authorization rule in the given Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="c00d5-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c00d5-111">EXAMPLES</span></span>

### <span data-ttu-id="c00d5-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="c00d5-112">Example 1</span></span>
```powershell
PS C:\> $authRuleObj = Get-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="c00d5-113">Eltávolítja a **Manage** billentyűt a névtér engedélyezési szabályának `AuthoRule1` hozzáférési `SB-Example1` jogaiból.</span><span class="sxs-lookup"><span data-stu-id="c00d5-113">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in namespace `SB-Example1`.</span></span>

### <span data-ttu-id="c00d5-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="c00d5-114">Example 2</span></span>
```powershell
PS C:\> $authRuleObj = Get-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="c00d5-115">Eltávolítja a **Kezelés** elérést a várólistán lévő engedélyezési `AuthoRule1` szabály hozzáférési jogosultságaiból. `SBQueue`</span><span class="sxs-lookup"><span data-stu-id="c00d5-115">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in queue `SBQueue`.</span></span>

### <span data-ttu-id="c00d5-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="c00d5-116">Example 3</span></span>
```powershell
PS C:\> $authRuleObj = Get-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="c00d5-117">Eltávolítja a **Kezelés** elérést a témakörben található engedélyezési szabály `AuthoRule1` hozzáférési jogosultságaiból. `SBTopic`</span><span class="sxs-lookup"><span data-stu-id="c00d5-117">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in topic `SBTopic`.</span></span>

## <span data-ttu-id="c00d5-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c00d5-118">PARAMETERS</span></span>

### <span data-ttu-id="c00d5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c00d5-119">-DefaultProfile</span></span>
<span data-ttu-id="c00d5-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c00d5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c00d5-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c00d5-121">-InputObject</span></span>
<span data-ttu-id="c00d5-122">ServiceBus AuthorizationRule objektum</span><span class="sxs-lookup"><span data-stu-id="c00d5-122">ServiceBus AuthorizationRule Object</span></span>

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

### <span data-ttu-id="c00d5-123">-Name</span><span class="sxs-lookup"><span data-stu-id="c00d5-123">-Name</span></span>
<span data-ttu-id="c00d5-124">AuthorizationRule Name</span><span class="sxs-lookup"><span data-stu-id="c00d5-124">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="c00d5-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c00d5-125">-Namespace</span></span>
<span data-ttu-id="c00d5-126">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="c00d5-126">Namespace Name</span></span>

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

### <span data-ttu-id="c00d5-127">-Queue</span><span class="sxs-lookup"><span data-stu-id="c00d5-127">-Queue</span></span>
<span data-ttu-id="c00d5-128">Várólistán lévő név</span><span class="sxs-lookup"><span data-stu-id="c00d5-128">Queue Name</span></span>

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

### <span data-ttu-id="c00d5-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c00d5-129">-ResourceGroupName</span></span>
<span data-ttu-id="c00d5-130">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="c00d5-130">Resource Group Name</span></span>

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

### <span data-ttu-id="c00d5-131">-Rights</span><span class="sxs-lookup"><span data-stu-id="c00d5-131">-Rights</span></span>
<span data-ttu-id="c00d5-132">Jogok, például @("Hallgatás","Küldés","Kezelés")</span><span class="sxs-lookup"><span data-stu-id="c00d5-132">Rights, e.g. @("Listen","Send","Manage")</span></span>

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

### <span data-ttu-id="c00d5-133">-Topic</span><span class="sxs-lookup"><span data-stu-id="c00d5-133">-Topic</span></span>
<span data-ttu-id="c00d5-134">Témakör neve</span><span class="sxs-lookup"><span data-stu-id="c00d5-134">Topic Name</span></span>

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

### <span data-ttu-id="c00d5-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c00d5-135">-Confirm</span></span>
<span data-ttu-id="c00d5-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c00d5-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c00d5-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c00d5-137">-WhatIf</span></span>
<span data-ttu-id="c00d5-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c00d5-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c00d5-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c00d5-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c00d5-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c00d5-140">CommonParameters</span></span>
<span data-ttu-id="c00d5-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c00d5-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c00d5-142">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c00d5-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c00d5-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c00d5-143">INPUTS</span></span>

### <span data-ttu-id="c00d5-144">System.String</span><span class="sxs-lookup"><span data-stu-id="c00d5-144">System.String</span></span>

### <span data-ttu-id="c00d5-145">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="c00d5-145">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

### <span data-ttu-id="c00d5-146">System.String[]</span><span class="sxs-lookup"><span data-stu-id="c00d5-146">System.String[]</span></span>

## <span data-ttu-id="c00d5-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c00d5-147">OUTPUTS</span></span>

### <span data-ttu-id="c00d5-148">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="c00d5-148">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="c00d5-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c00d5-149">NOTES</span></span>

## <span data-ttu-id="c00d5-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c00d5-150">RELATED LINKS</span></span>
