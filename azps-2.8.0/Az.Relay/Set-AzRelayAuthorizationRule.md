---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/set-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayAuthorizationRule.md
ms.openlocfilehash: ed95b9aa2e914d8f7c37132c372c4c1acaeafca1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838960"
---
# <span data-ttu-id="b41be-101">Set-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b41be-101">Set-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="b41be-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b41be-102">SYNOPSIS</span></span>
<span data-ttu-id="b41be-103">Frissíti a megadott engedélyezési szabály leírását az adott továbbítóügynök (Namespace/WcfRelay/HybridConnection) esetében.</span><span class="sxs-lookup"><span data-stu-id="b41be-103">Updates the specified authorization rule description for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="b41be-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b41be-104">SYNTAX</span></span>

### <span data-ttu-id="b41be-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b41be-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b41be-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="b41be-106">WcfRelayAuthorizationRuleSet</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> [[-InputObject] <PSAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b41be-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="b41be-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> [[-InputObject] <PSAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b41be-108">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b41be-108">AuthoRuleInputObjectSet</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b41be-109">AuthoRulePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="b41be-109">AuthoRulePropertiesSet</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Name] <String> [-Rights] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b41be-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="b41be-110">DESCRIPTION</span></span>
<span data-ttu-id="b41be-111">A **set-AzRelayAuthorizationRule** parancsmag a megadott továbbítóügynökök (Namespace/WcfRelay/HybridConnection) megadott engedélyezési szabályának leírását frissíti.</span><span class="sxs-lookup"><span data-stu-id="b41be-111">The **Set-AzRelayAuthorizationRule** cmdlet updates the description for the specified authorization rule of the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="b41be-112">Példák</span><span class="sxs-lookup"><span data-stu-id="b41be-112">EXAMPLES</span></span>

### <span data-ttu-id="b41be-113">Példa 1,1-névtér a InputObject</span><span class="sxs-lookup"><span data-stu-id="b41be-113">Example 1.1 - Namespace with InputObject</span></span>
```
PS C:\>
PS C:\> $getAutoRule = Get-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -AuthorizationRuleName
 AuthoRule1
PS C:\> $getAutoRule.Rights.Add("Send")
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -AuthorizationRule AuthoRule1 -InputObject $getAutoRule

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1
```

<span data-ttu-id="b41be-114">A névtérben lévő engedélyezési szabály hozzáférési jogát hozzáadja a **küldéshez** `AuthoRule1` `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="b41be-114">Adds **Send** from the access rights of the authorization rule `AuthoRule1` in namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="b41be-115">Példa 1,2-névtér a Rights paraméterrel</span><span class="sxs-lookup"><span data-stu-id="b41be-115">Example 1.2 - Namespace with Rights parameter</span></span>
```
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -AuthorizationRule AuthoRule1 -Rights "Send"

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1
```

<span data-ttu-id="b41be-116">A névtérben lévő engedélyezési szabály hozzáférési jogát hozzáadja a **küldéshez** `AuthoRule1` `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="b41be-116">Adds **Send** from the access rights of the authorization rule `AuthoRule1` in namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="b41be-117">Példa 2,1-WcfRelay a InputObject</span><span class="sxs-lookup"><span data-stu-id="b41be-117">Example 2.1 - WcfRelay with InputObject</span></span>
```
PS C:\> $getWcfRelayAutho = Get-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1
PS C:\> $getWcfRelayAutho.Rights.Add("Send")
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -InputObject $getWcfRelayAutho

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1
```

<span data-ttu-id="b41be-118">A WcfRelay engedélyezési szabályának hozzáférési jogát hozzáadja a **küldéshez** `AuthoRule1` `TestWCFRelay1` .</span><span class="sxs-lookup"><span data-stu-id="b41be-118">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="b41be-119">Példa 2,2-WcfRelay a Rights paraméterrel</span><span class="sxs-lookup"><span data-stu-id="b41be-119">Example 2.2 - WcfRelay with Rights parameter</span></span>
```
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -Rights "Send"

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1
```

<span data-ttu-id="b41be-120">A WcfRelay engedélyezési szabályának hozzáférési jogát hozzáadja a **küldéshez** `AuthoRule1` `TestWCFRelay1` .</span><span class="sxs-lookup"><span data-stu-id="b41be-120">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="b41be-121">Példa 3,1-HybridConnection a InputObject</span><span class="sxs-lookup"><span data-stu-id="b41be-121">Example 3.1 - HybridConnection with InputObject</span></span>
```
PS C:\> $GetHybirdAutho = Get-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
PS C:\> $GetHybirdAutho.Rights.Add("Send")
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -InputObject $GetHybirdAutho

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="b41be-122">A HybridConnection engedélyezési szabályának hozzáférési jogát hozzáadja a **küldéshez** `AuthoRule1` `TestHybridConnection` .</span><span class="sxs-lookup"><span data-stu-id="b41be-122">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection`.</span></span>

### <span data-ttu-id="b41be-123">Példa 3,2-HybridConnection a Rights paraméterrel</span><span class="sxs-lookup"><span data-stu-id="b41be-123">Example 3.2 - HybridConnection with Rights parameter</span></span>
```
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -Rights "Send"

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="b41be-124">A HybridConnection engedélyezési szabályának hozzáférési jogát hozzáadja a **küldéshez** `AuthoRule1` `TestHybridConnection` .</span><span class="sxs-lookup"><span data-stu-id="b41be-124">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection`.</span></span>

## <span data-ttu-id="b41be-125">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b41be-125">PARAMETERS</span></span>

### <span data-ttu-id="b41be-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b41be-126">-DefaultProfile</span></span>
<span data-ttu-id="b41be-127">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b41be-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b41be-128">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="b41be-128">-HybridConnection</span></span>
<span data-ttu-id="b41be-129">HybridConnection neve</span><span class="sxs-lookup"><span data-stu-id="b41be-129">HybridConnection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: HybridConnectionAuthorizationRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b41be-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b41be-130">-InputObject</span></span>
<span data-ttu-id="b41be-131">Továbbító AuthorizationRule objektum</span><span class="sxs-lookup"><span data-stu-id="b41be-131">Relay AuthorizationRule Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b41be-132">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b41be-132">-Name</span></span>
<span data-ttu-id="b41be-133">AuthorizationRule neve</span><span class="sxs-lookup"><span data-stu-id="b41be-133">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b41be-134">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b41be-134">-Namespace</span></span>
<span data-ttu-id="b41be-135">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="b41be-135">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b41be-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b41be-136">-ResourceGroupName</span></span>
<span data-ttu-id="b41be-137">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="b41be-137">Resource Group Name.</span></span>

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

### <span data-ttu-id="b41be-138">– Jogok</span><span class="sxs-lookup"><span data-stu-id="b41be-138">-Rights</span></span>
<span data-ttu-id="b41be-139">Jogok, például @ ("Figyelj", "Küldés", "kezelés")</span><span class="sxs-lookup"><span data-stu-id="b41be-139">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: System.String[]
Parameter Sets: NamespaceAuthorizationRuleSet, WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: AuthoRulePropertiesSet
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b41be-140">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="b41be-140">-WcfRelay</span></span>
<span data-ttu-id="b41be-141">WcfRelay neve</span><span class="sxs-lookup"><span data-stu-id="b41be-141">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b41be-142">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b41be-142">-Confirm</span></span>
<span data-ttu-id="b41be-143">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b41be-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b41be-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b41be-144">-WhatIf</span></span>
<span data-ttu-id="b41be-145">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b41be-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b41be-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b41be-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b41be-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b41be-147">CommonParameters</span></span>
<span data-ttu-id="b41be-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b41be-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b41be-149">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b41be-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b41be-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b41be-150">INPUTS</span></span>

### <span data-ttu-id="b41be-151">System. String</span><span class="sxs-lookup"><span data-stu-id="b41be-151">System.String</span></span>

### <span data-ttu-id="b41be-152">Microsoft. Azure. Command. Relay. models. PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="b41be-152">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

### <span data-ttu-id="b41be-153">System. string []</span><span class="sxs-lookup"><span data-stu-id="b41be-153">System.String[]</span></span>

## <span data-ttu-id="b41be-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b41be-154">OUTPUTS</span></span>

### <span data-ttu-id="b41be-155">Microsoft. Azure. Command. Relay. models. PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="b41be-155">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="b41be-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b41be-156">NOTES</span></span>

## <span data-ttu-id="b41be-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b41be-157">RELATED LINKS</span></span>
