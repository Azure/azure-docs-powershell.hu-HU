---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/set-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayAuthorizationRule.md
ms.openlocfilehash: 4ca8156e80a827c9916def7ef749cfa9abb9389a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181442"
---
# <span data-ttu-id="2e665-101">Set-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="2e665-101">Set-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="2e665-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2e665-102">SYNOPSIS</span></span>
<span data-ttu-id="2e665-103">Frissíti a megadott engedélyezési szabály leírását az adott továbbítóügynök (Namespace/WcfRelay/HybridConnection) esetében.</span><span class="sxs-lookup"><span data-stu-id="2e665-103">Updates the specified authorization rule description for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="2e665-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2e665-104">SYNTAX</span></span>

### <span data-ttu-id="2e665-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2e665-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e665-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="2e665-106">WcfRelayAuthorizationRuleSet</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> [[-InputObject] <PSAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e665-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="2e665-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> [[-InputObject] <PSAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e665-108">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2e665-108">AuthoRuleInputObjectSet</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2e665-109">AuthoRulePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="2e665-109">AuthoRulePropertiesSet</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Name] <String> [-Rights] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e665-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="2e665-110">DESCRIPTION</span></span>
<span data-ttu-id="2e665-111">A **set-AzRelayAuthorizationRule** parancsmag a megadott továbbítóügynökök (Namespace/WcfRelay/HybridConnection) megadott engedélyezési szabályának leírását frissíti.</span><span class="sxs-lookup"><span data-stu-id="2e665-111">The **Set-AzRelayAuthorizationRule** cmdlet updates the description for the specified authorization rule of the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="2e665-112">Példák</span><span class="sxs-lookup"><span data-stu-id="2e665-112">EXAMPLES</span></span>

### <span data-ttu-id="2e665-113">Példa 1,1-névtér a InputObject</span><span class="sxs-lookup"><span data-stu-id="2e665-113">Example 1.1 - Namespace with InputObject</span></span>
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

<span data-ttu-id="2e665-114">A névtérben lévő engedélyezési szabály hozzáférési jogát hozzáadja a **küldéshez** `AuthoRule1` `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="2e665-114">Adds **Send** from the access rights of the authorization rule `AuthoRule1` in namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="2e665-115">Példa 1,2-névtér a Rights paraméterrel</span><span class="sxs-lookup"><span data-stu-id="2e665-115">Example 1.2 - Namespace with Rights parameter</span></span>
```
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -AuthorizationRule AuthoRule1 -Rights "Send"

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1
```

<span data-ttu-id="2e665-116">A névtérben lévő engedélyezési szabály hozzáférési jogát hozzáadja a **küldéshez** `AuthoRule1` `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="2e665-116">Adds **Send** from the access rights of the authorization rule `AuthoRule1` in namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="2e665-117">Példa 2,1-WcfRelay a InputObject</span><span class="sxs-lookup"><span data-stu-id="2e665-117">Example 2.1 - WcfRelay with InputObject</span></span>
```
PS C:\> $getWcfRelayAutho = Get-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1
PS C:\> $getWcfRelayAutho.Rights.Add("Send")
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -InputObject $getWcfRelayAutho

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1
```

<span data-ttu-id="2e665-118">A WcfRelay engedélyezési szabályának hozzáférési jogát hozzáadja a **küldéshez** `AuthoRule1` `TestWCFRelay1` .</span><span class="sxs-lookup"><span data-stu-id="2e665-118">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="2e665-119">Példa 2,2-WcfRelay a Rights paraméterrel</span><span class="sxs-lookup"><span data-stu-id="2e665-119">Example 2.2 - WcfRelay with Rights parameter</span></span>
```
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -Rights "Send"

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1
```

<span data-ttu-id="2e665-120">A WcfRelay engedélyezési szabályának hozzáférési jogát hozzáadja a **küldéshez** `AuthoRule1` `TestWCFRelay1` .</span><span class="sxs-lookup"><span data-stu-id="2e665-120">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="2e665-121">Példa 3,1-HybridConnection a InputObject</span><span class="sxs-lookup"><span data-stu-id="2e665-121">Example 3.1 - HybridConnection with InputObject</span></span>
```
PS C:\> $GetHybirdAutho = Get-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
PS C:\> $GetHybirdAutho.Rights.Add("Send")
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -InputObject $GetHybirdAutho

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="2e665-122">A HybridConnection engedélyezési szabályának hozzáférési jogát hozzáadja a **küldéshez** `AuthoRule1` `TestHybridConnection` .</span><span class="sxs-lookup"><span data-stu-id="2e665-122">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection`.</span></span>

### <span data-ttu-id="2e665-123">Példa 3,2-HybridConnection a Rights paraméterrel</span><span class="sxs-lookup"><span data-stu-id="2e665-123">Example 3.2 - HybridConnection with Rights parameter</span></span>
```
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -Rights "Send"

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="2e665-124">A HybridConnection engedélyezési szabályának hozzáférési jogát hozzáadja a **küldéshez** `AuthoRule1` `TestHybridConnection` .</span><span class="sxs-lookup"><span data-stu-id="2e665-124">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection`.</span></span>

## <span data-ttu-id="2e665-125">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2e665-125">PARAMETERS</span></span>

### <span data-ttu-id="2e665-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e665-126">-DefaultProfile</span></span>
<span data-ttu-id="2e665-127">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2e665-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e665-128">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="2e665-128">-HybridConnection</span></span>
<span data-ttu-id="2e665-129">HybridConnection neve</span><span class="sxs-lookup"><span data-stu-id="2e665-129">HybridConnection Name.</span></span>

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

### <span data-ttu-id="2e665-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2e665-130">-InputObject</span></span>
<span data-ttu-id="2e665-131">Továbbító AuthorizationRule objektum</span><span class="sxs-lookup"><span data-stu-id="2e665-131">Relay AuthorizationRule Object.</span></span>

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

### <span data-ttu-id="2e665-132">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2e665-132">-Name</span></span>
<span data-ttu-id="2e665-133">AuthorizationRule neve</span><span class="sxs-lookup"><span data-stu-id="2e665-133">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="2e665-134">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2e665-134">-Namespace</span></span>
<span data-ttu-id="2e665-135">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="2e665-135">Namespace Name.</span></span>

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

### <span data-ttu-id="2e665-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e665-136">-ResourceGroupName</span></span>
<span data-ttu-id="2e665-137">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="2e665-137">Resource Group Name.</span></span>

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

### <span data-ttu-id="2e665-138">– Jogok</span><span class="sxs-lookup"><span data-stu-id="2e665-138">-Rights</span></span>
<span data-ttu-id="2e665-139">Jogok, például @ ("Figyelj", "Küldés", "kezelés")</span><span class="sxs-lookup"><span data-stu-id="2e665-139">Rights, e.g. @("Listen","Send","Manage")</span></span>

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

### <span data-ttu-id="2e665-140">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="2e665-140">-WcfRelay</span></span>
<span data-ttu-id="2e665-141">WcfRelay neve</span><span class="sxs-lookup"><span data-stu-id="2e665-141">WcfRelay Name.</span></span>

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

### <span data-ttu-id="2e665-142">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2e665-142">-Confirm</span></span>
<span data-ttu-id="2e665-143">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2e665-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e665-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e665-144">-WhatIf</span></span>
<span data-ttu-id="2e665-145">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2e665-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e665-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2e665-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e665-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e665-147">CommonParameters</span></span>
<span data-ttu-id="2e665-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2e665-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e665-149">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e665-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e665-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e665-150">INPUTS</span></span>

### <span data-ttu-id="2e665-151">System. String</span><span class="sxs-lookup"><span data-stu-id="2e665-151">System.String</span></span>

### <span data-ttu-id="2e665-152">Microsoft. Azure. Command. Relay. models. PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="2e665-152">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

### <span data-ttu-id="2e665-153">System. string []</span><span class="sxs-lookup"><span data-stu-id="2e665-153">System.String[]</span></span>

## <span data-ttu-id="2e665-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e665-154">OUTPUTS</span></span>

### <span data-ttu-id="2e665-155">Microsoft. Azure. Command. Relay. models. PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="2e665-155">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="2e665-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2e665-156">NOTES</span></span>

## <span data-ttu-id="2e665-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2e665-157">RELATED LINKS</span></span>
