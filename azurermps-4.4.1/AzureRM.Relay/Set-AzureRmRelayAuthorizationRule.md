---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayAuthorizationRule.md
ms.openlocfilehash: 64c839140907b10d62b4f71025afab985d5ba736
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500776"
---
# <span data-ttu-id="dddfc-101">Set-AzureRmRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="dddfc-101">Set-AzureRmRelayAuthorizationRule</span></span>

## <span data-ttu-id="dddfc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dddfc-102">SYNOPSIS</span></span>
<span data-ttu-id="dddfc-103">Frissíti a megadott engedélyezési szabály leírását az adott továbbítóügynök (Namespace/WcfRelay/HybridConnection) esetében.</span><span class="sxs-lookup"><span data-stu-id="dddfc-103">Updates the specified authorization rule description for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dddfc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dddfc-104">SYNTAX</span></span>

### <span data-ttu-id="dddfc-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="dddfc-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <AuthorizationRuleAttributes>] [-Rights <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dddfc-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="dddfc-106">WcfRelayAuthorizationRuleSet</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> [-InputObject <AuthorizationRuleAttributes>] [-Rights <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dddfc-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="dddfc-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [-Name] <String> [-InputObject <AuthorizationRuleAttributes>]
 [-Rights <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dddfc-108">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="dddfc-108">AuthoRuleInputObjectSet</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 -InputObject <AuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dddfc-109">AuthoRulePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="dddfc-109">AuthoRulePropertiesSet</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Name] <String> -Rights <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dddfc-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="dddfc-110">DESCRIPTION</span></span>
<span data-ttu-id="dddfc-111">A **set-AzureRmRelayAuthorizationRule** parancsmag a megadott továbbítóügynökök (Namespace/WcfRelay/HybridConnection) megadott engedélyezési szabályának leírását frissíti.</span><span class="sxs-lookup"><span data-stu-id="dddfc-111">The **Set-AzureRmRelayAuthorizationRule** cmdlet updates the description for the specified authorization rule of the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="dddfc-112">Példák</span><span class="sxs-lookup"><span data-stu-id="dddfc-112">EXAMPLES</span></span>

### <span data-ttu-id="dddfc-113">Példa 1,1-névtér a InputObject</span><span class="sxs-lookup"><span data-stu-id="dddfc-113">Example 1.1 - Namespace with InputObject</span></span>
```
PS C:\>
PS C:\> $getAutoRule = Get-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -AuthorizationRuleName
 AuthoRule1
PS C:\> $getAutoRule.Rights.Add("Send")
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -AuthorizationRule AuthoRule1 -InputObject $getAutoRule
```

<span data-ttu-id="dddfc-114">A névtérben lévő engedélyezési szabály hozzáférési jogát hozzáadja a **küldéshez** `AuthoRule1` `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="dddfc-114">Adds **Send** from the access rights of the authorization rule `AuthoRule1` in namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="dddfc-115">Példa 1,2-névtér a Rights paraméterrel</span><span class="sxs-lookup"><span data-stu-id="dddfc-115">Example 1.2 - Namespace with Rights parameter</span></span>
```
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -AuthorizationRule AuthoRule1 -Rights "Send"
```

<span data-ttu-id="dddfc-116">A névtérben lévő engedélyezési szabály hozzáférési jogát hozzáadja a **küldéshez** `AuthoRule1` `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="dddfc-116">Adds **Send** from the access rights of the authorization rule `AuthoRule1` in namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="dddfc-117">Példa 2,1-WcfRelay a InputObject</span><span class="sxs-lookup"><span data-stu-id="dddfc-117">Example 2.1 - WcfRelay with InputObject</span></span>
```
PS C:\> $getWcfRelayAutho = Get-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1
PS C:\> $getWcfRelayAutho.Rights.Add("Send")
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -InputObject $getWcfRelayAutho
```

<span data-ttu-id="dddfc-118">A WcfRelay engedélyezési szabályának hozzáférési jogát hozzáadja a **küldéshez** `AuthoRule1` `TestWCFRelay1` .</span><span class="sxs-lookup"><span data-stu-id="dddfc-118">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="dddfc-119">Példa 2,2-WcfRelay a Rights paraméterrel</span><span class="sxs-lookup"><span data-stu-id="dddfc-119">Example 2.2 - WcfRelay with Rights parameter</span></span>
```
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -Rights "Send"
```

<span data-ttu-id="dddfc-120">A WcfRelay engedélyezési szabályának hozzáférési jogát hozzáadja a **küldéshez** `AuthoRule1` `TestWCFRelay1` .</span><span class="sxs-lookup"><span data-stu-id="dddfc-120">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="dddfc-121">Példa 3,1-HybridConnection a InputObject</span><span class="sxs-lookup"><span data-stu-id="dddfc-121">Example 3.1 - HybridConnection with InputObject</span></span>
```
PS C:\> $GetHybirdAutho = Get-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
PS C:\> $GetHybirdAutho.Rights.Add("Send")
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -InputObject $GetHybirdAutho
```

<span data-ttu-id="dddfc-122">A HybridConnection engedélyezési szabályának hozzáférési jogát hozzáadja a **küldéshez** `AuthoRule1` `TestHybridConnection` .</span><span class="sxs-lookup"><span data-stu-id="dddfc-122">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection`.</span></span>

### <span data-ttu-id="dddfc-123">Példa 3,2-HybridConnection a Rights paraméterrel</span><span class="sxs-lookup"><span data-stu-id="dddfc-123">Example 3.2 - HybridConnection with Rights parameter</span></span>
```
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -Rights "Send"
```

<span data-ttu-id="dddfc-124">A HybridConnection engedélyezési szabályának hozzáférési jogát hozzáadja a **küldéshez** `AuthoRule1` `TestHybridConnection` .</span><span class="sxs-lookup"><span data-stu-id="dddfc-124">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection`.</span></span>

## <span data-ttu-id="dddfc-125">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dddfc-125">PARAMETERS</span></span>

### <span data-ttu-id="dddfc-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="dddfc-126">-Confirm</span></span>
<span data-ttu-id="dddfc-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="dddfc-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dddfc-128">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="dddfc-128">-HybridConnection</span></span>
<span data-ttu-id="dddfc-129">HybridConnection neve</span><span class="sxs-lookup"><span data-stu-id="dddfc-129">HybridConnection Name.</span></span>

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

### <span data-ttu-id="dddfc-130">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dddfc-130">-Name</span></span>
<span data-ttu-id="dddfc-131">AuthorizationRule neve</span><span class="sxs-lookup"><span data-stu-id="dddfc-131">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="dddfc-132">-Namespace</span><span class="sxs-lookup"><span data-stu-id="dddfc-132">-Namespace</span></span>
<span data-ttu-id="dddfc-133">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="dddfc-133">Namespace Name.</span></span>

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

### <span data-ttu-id="dddfc-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dddfc-134">-ResourceGroupName</span></span>
<span data-ttu-id="dddfc-135">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="dddfc-135">Resource Group Name.</span></span>

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

### <span data-ttu-id="dddfc-136">– Jogok</span><span class="sxs-lookup"><span data-stu-id="dddfc-136">-Rights</span></span>
<span data-ttu-id="dddfc-137">Jogok, például @ ("Figyelj", "Küldés", "kezelés")</span><span class="sxs-lookup"><span data-stu-id="dddfc-137">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: System.String[]
Parameter Sets: NamespaceAuthorizationRuleSet, WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: AuthoRulePropertiesSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dddfc-138">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="dddfc-138">-WcfRelay</span></span>
<span data-ttu-id="dddfc-139">WcfRelay neve</span><span class="sxs-lookup"><span data-stu-id="dddfc-139">WcfRelay Name.</span></span>

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

### <span data-ttu-id="dddfc-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dddfc-140">-WhatIf</span></span>
<span data-ttu-id="dddfc-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="dddfc-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dddfc-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dddfc-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dddfc-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dddfc-143">-DefaultProfile</span></span>
<span data-ttu-id="dddfc-144">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dddfc-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dddfc-145">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dddfc-145">-InputObject</span></span>
<span data-ttu-id="dddfc-146">{{Fill InputObject Description}}</span><span class="sxs-lookup"><span data-stu-id="dddfc-146">{{Fill InputObject Description}}</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dddfc-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dddfc-147">CommonParameters</span></span>
<span data-ttu-id="dddfc-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dddfc-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dddfc-149">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dddfc-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dddfc-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dddfc-150">INPUTS</span></span>

### <span data-ttu-id="dddfc-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dddfc-151">-ResourceGroupName</span></span>
 <span data-ttu-id="dddfc-152">System. String</span><span class="sxs-lookup"><span data-stu-id="dddfc-152">System.String</span></span> 

### <span data-ttu-id="dddfc-153">-Namespace</span><span class="sxs-lookup"><span data-stu-id="dddfc-153">-Namespace</span></span>
 <span data-ttu-id="dddfc-154">System. String</span><span class="sxs-lookup"><span data-stu-id="dddfc-154">System.String</span></span> 
 

### <span data-ttu-id="dddfc-155">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="dddfc-155">-WcfRelay</span></span>
 <span data-ttu-id="dddfc-156">System. String</span><span class="sxs-lookup"><span data-stu-id="dddfc-156">System.String</span></span> 

### <span data-ttu-id="dddfc-157">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="dddfc-157">-HybridConnection</span></span>
 <span data-ttu-id="dddfc-158">System. String</span><span class="sxs-lookup"><span data-stu-id="dddfc-158">System.String</span></span> 
 

### <span data-ttu-id="dddfc-159">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dddfc-159">-Name</span></span>
 <span data-ttu-id="dddfc-160">System. String</span><span class="sxs-lookup"><span data-stu-id="dddfc-160">System.String</span></span>

### <span data-ttu-id="dddfc-161">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dddfc-161">-InputObject</span></span>
 <span data-ttu-id="dddfc-162">Microsoft. Azure. Command. Relay. models. AuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="dddfc-162">Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleAttributes</span></span>
 

### <span data-ttu-id="dddfc-163">– Jogok</span><span class="sxs-lookup"><span data-stu-id="dddfc-163">-Rights</span></span>
 <span data-ttu-id="dddfc-164">System. string []</span><span class="sxs-lookup"><span data-stu-id="dddfc-164">System.String []</span></span>

## <span data-ttu-id="dddfc-165">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dddfc-165">OUTPUTS</span></span>

### <span data-ttu-id="dddfc-166">Microsoft. Azure. Command. Relay. models. AuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="dddfc-166">Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleAttributes</span></span>

### <span data-ttu-id="dddfc-167">Példa 1 – névtér</span><span class="sxs-lookup"><span data-stu-id="dddfc-167">Example 1 - Namespace</span></span>
<span data-ttu-id="dddfc-168">Jogok: {figyelj, küldés} név: AuthoRule1 típusa: Microsoft. Relay/AuthorizationRules ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="dddfc-168">Rights : {Listen, Send} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1</span></span>

### <span data-ttu-id="dddfc-169">Példa 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="dddfc-169">Example 2 - WcfRelay</span></span>
<span data-ttu-id="dddfc-170">Jogok: {figyelj, küldés} név: AuthoRule1 típusa: Microsoft. Relay/AuthorizationRules ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="dddfc-170">Rights : {Listen, Send} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1</span></span>

### <span data-ttu-id="dddfc-171">Példa: 3 – HybridConnection</span><span class="sxs-lookup"><span data-stu-id="dddfc-171">Example 3 - HybridConnection</span></span>
<span data-ttu-id="dddfc-172">Jogok: {figyelj, küldés} név: AuthoRule1 típusa: Microsoft. Relay/AuthorizationRules ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="dddfc-172">Rights : {Listen, Send} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1</span></span>

## <span data-ttu-id="dddfc-173">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dddfc-173">NOTES</span></span>

## <span data-ttu-id="dddfc-174">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dddfc-174">RELATED LINKS</span></span>

