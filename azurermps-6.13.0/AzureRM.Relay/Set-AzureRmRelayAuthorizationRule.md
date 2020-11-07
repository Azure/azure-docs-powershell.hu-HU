---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/set-azurermrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayAuthorizationRule.md
ms.openlocfilehash: d4d3dc0ffc3606cbf37bed040e6cf4e805d72482
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680622"
---
# <span data-ttu-id="16a2c-101">Set-AzureRmRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="16a2c-101">Set-AzureRmRelayAuthorizationRule</span></span>

## <span data-ttu-id="16a2c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="16a2c-102">SYNOPSIS</span></span>
<span data-ttu-id="16a2c-103">Frissíti a megadott engedélyezési szabály leírását az adott továbbítóügynök (Namespace/WcfRelay/HybridConnection) esetében.</span><span class="sxs-lookup"><span data-stu-id="16a2c-103">Updates the specified authorization rule description for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16a2c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="16a2c-104">SYNTAX</span></span>

### <span data-ttu-id="16a2c-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="16a2c-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <AuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16a2c-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="16a2c-106">WcfRelayAuthorizationRuleSet</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> [[-InputObject] <AuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16a2c-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="16a2c-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [-Name] <String> [[-InputObject] <AuthorizationRuleAttributes>]
 [[-Rights] <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16a2c-108">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="16a2c-108">AuthoRuleInputObjectSet</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <AuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="16a2c-109">AuthoRulePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="16a2c-109">AuthoRulePropertiesSet</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Name] <String> [-Rights] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16a2c-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="16a2c-110">DESCRIPTION</span></span>
<span data-ttu-id="16a2c-111">A **set-AzureRmRelayAuthorizationRule** parancsmag a megadott továbbítóügynökök (Namespace/WcfRelay/HybridConnection) megadott engedélyezési szabályának leírását frissíti.</span><span class="sxs-lookup"><span data-stu-id="16a2c-111">The **Set-AzureRmRelayAuthorizationRule** cmdlet updates the description for the specified authorization rule of the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="16a2c-112">Példák</span><span class="sxs-lookup"><span data-stu-id="16a2c-112">EXAMPLES</span></span>

### <span data-ttu-id="16a2c-113">Példa 1,1-névtér a InputObject</span><span class="sxs-lookup"><span data-stu-id="16a2c-113">Example 1.1 - Namespace with InputObject</span></span>
```
PS C:\>
PS C:\> $getAutoRule = Get-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -AuthorizationRuleName
 AuthoRule1
PS C:\> $getAutoRule.Rights.Add("Send")
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -AuthorizationRule AuthoRule1 -InputObject $getAutoRule

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1
```

<span data-ttu-id="16a2c-114">A névtérben lévő engedélyezési szabály hozzáférési jogát hozzáadja a **küldéshez** `AuthoRule1` `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="16a2c-114">Adds **Send** from the access rights of the authorization rule `AuthoRule1` in namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="16a2c-115">Példa 1,2-névtér a Rights paraméterrel</span><span class="sxs-lookup"><span data-stu-id="16a2c-115">Example 1.2 - Namespace with Rights parameter</span></span>
```
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -AuthorizationRule AuthoRule1 -Rights "Send"

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1
```

<span data-ttu-id="16a2c-116">A névtérben lévő engedélyezési szabály hozzáférési jogát hozzáadja a **küldéshez** `AuthoRule1` `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="16a2c-116">Adds **Send** from the access rights of the authorization rule `AuthoRule1` in namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="16a2c-117">Példa 2,1-WcfRelay a InputObject</span><span class="sxs-lookup"><span data-stu-id="16a2c-117">Example 2.1 - WcfRelay with InputObject</span></span>
```
PS C:\> $getWcfRelayAutho = Get-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1
PS C:\> $getWcfRelayAutho.Rights.Add("Send")
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -InputObject $getWcfRelayAutho

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1
```

<span data-ttu-id="16a2c-118">A WcfRelay engedélyezési szabályának hozzáférési jogát hozzáadja a **küldéshez** `AuthoRule1` `TestWCFRelay1` .</span><span class="sxs-lookup"><span data-stu-id="16a2c-118">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="16a2c-119">Példa 2,2-WcfRelay a Rights paraméterrel</span><span class="sxs-lookup"><span data-stu-id="16a2c-119">Example 2.2 - WcfRelay with Rights parameter</span></span>
```
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -Rights "Send"

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1
```

<span data-ttu-id="16a2c-120">A WcfRelay engedélyezési szabályának hozzáférési jogát hozzáadja a **küldéshez** `AuthoRule1` `TestWCFRelay1` .</span><span class="sxs-lookup"><span data-stu-id="16a2c-120">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="16a2c-121">Példa 3,1-HybridConnection a InputObject</span><span class="sxs-lookup"><span data-stu-id="16a2c-121">Example 3.1 - HybridConnection with InputObject</span></span>
```
PS C:\> $GetHybirdAutho = Get-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
PS C:\> $GetHybirdAutho.Rights.Add("Send")
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -InputObject $GetHybirdAutho

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="16a2c-122">A HybridConnection engedélyezési szabályának hozzáférési jogát hozzáadja a **küldéshez** `AuthoRule1` `TestHybridConnection` .</span><span class="sxs-lookup"><span data-stu-id="16a2c-122">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection`.</span></span>

### <span data-ttu-id="16a2c-123">Példa 3,2-HybridConnection a Rights paraméterrel</span><span class="sxs-lookup"><span data-stu-id="16a2c-123">Example 3.2 - HybridConnection with Rights parameter</span></span>
```
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -Rights "Send"

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="16a2c-124">A HybridConnection engedélyezési szabályának hozzáférési jogát hozzáadja a **küldéshez** `AuthoRule1` `TestHybridConnection` .</span><span class="sxs-lookup"><span data-stu-id="16a2c-124">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection`.</span></span>

## <span data-ttu-id="16a2c-125">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="16a2c-125">PARAMETERS</span></span>

### <span data-ttu-id="16a2c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16a2c-126">-DefaultProfile</span></span>
<span data-ttu-id="16a2c-127">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="16a2c-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16a2c-128">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="16a2c-128">-HybridConnection</span></span>
<span data-ttu-id="16a2c-129">HybridConnection neve</span><span class="sxs-lookup"><span data-stu-id="16a2c-129">HybridConnection Name.</span></span>

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

### <span data-ttu-id="16a2c-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16a2c-130">-InputObject</span></span>
<span data-ttu-id="16a2c-131">Továbbító AuthorizationRule objektum</span><span class="sxs-lookup"><span data-stu-id="16a2c-131">Relay AuthorizationRule Object.</span></span>

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

### <span data-ttu-id="16a2c-132">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="16a2c-132">-Name</span></span>
<span data-ttu-id="16a2c-133">AuthorizationRule neve</span><span class="sxs-lookup"><span data-stu-id="16a2c-133">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="16a2c-134">-Namespace</span><span class="sxs-lookup"><span data-stu-id="16a2c-134">-Namespace</span></span>
<span data-ttu-id="16a2c-135">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="16a2c-135">Namespace Name.</span></span>

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

### <span data-ttu-id="16a2c-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16a2c-136">-ResourceGroupName</span></span>
<span data-ttu-id="16a2c-137">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="16a2c-137">Resource Group Name.</span></span>

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

### <span data-ttu-id="16a2c-138">– Jogok</span><span class="sxs-lookup"><span data-stu-id="16a2c-138">-Rights</span></span>
<span data-ttu-id="16a2c-139">Jogok, például @ ("Figyelj", "Küldés", "kezelés")</span><span class="sxs-lookup"><span data-stu-id="16a2c-139">Rights, e.g. @("Listen","Send","Manage")</span></span>

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

### <span data-ttu-id="16a2c-140">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="16a2c-140">-WcfRelay</span></span>
<span data-ttu-id="16a2c-141">WcfRelay neve</span><span class="sxs-lookup"><span data-stu-id="16a2c-141">WcfRelay Name.</span></span>

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

### <span data-ttu-id="16a2c-142">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="16a2c-142">-Confirm</span></span>
<span data-ttu-id="16a2c-143">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="16a2c-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16a2c-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16a2c-144">-WhatIf</span></span>
<span data-ttu-id="16a2c-145">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="16a2c-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16a2c-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="16a2c-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16a2c-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16a2c-147">CommonParameters</span></span>
<span data-ttu-id="16a2c-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="16a2c-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="16a2c-149">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16a2c-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16a2c-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="16a2c-150">INPUTS</span></span>

### <span data-ttu-id="16a2c-151">System. String</span><span class="sxs-lookup"><span data-stu-id="16a2c-151">System.String</span></span>
<span data-ttu-id="16a2c-152">Microsoft. Azure. commands. Relay. models. PSAuthorizationRuleAttributes System. string []</span><span class="sxs-lookup"><span data-stu-id="16a2c-152">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes System.String[]</span></span>


## <span data-ttu-id="16a2c-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="16a2c-153">OUTPUTS</span></span>

### <span data-ttu-id="16a2c-154">Microsoft. Azure. Command. Relay. models. PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="16a2c-154">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>


## <span data-ttu-id="16a2c-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="16a2c-155">NOTES</span></span>

## <span data-ttu-id="16a2c-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="16a2c-156">RELATED LINKS</span></span>
