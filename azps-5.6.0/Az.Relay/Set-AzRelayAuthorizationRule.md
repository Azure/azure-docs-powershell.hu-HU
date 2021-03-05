---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/set-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayAuthorizationRule.md
ms.openlocfilehash: 3165905cc86d2255670127cd90c015ce20096c14
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000422"
---
# <span data-ttu-id="13624-101">Set-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="13624-101">Set-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="13624-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13624-102">SYNOPSIS</span></span>
<span data-ttu-id="13624-103">Frissíti a megadott engedélyezési szabály leírását a megadott továbbítási entitásokhoz (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="13624-103">Updates the specified authorization rule description for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="13624-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="13624-104">SYNTAX</span></span>

### <span data-ttu-id="13624-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="13624-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13624-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="13624-106">WcfRelayAuthorizationRuleSet</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> [[-InputObject] <PSAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13624-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="13624-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> [[-InputObject] <PSAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13624-108">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="13624-108">AuthoRuleInputObjectSet</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="13624-109">AuthoRulePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="13624-109">AuthoRulePropertiesSet</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Name] <String> [-Rights] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13624-110">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="13624-110">DESCRIPTION</span></span>
<span data-ttu-id="13624-111">A **Set-AzRelayAuthorizationRule** parancsmag frissíti a megadott engedélyezési szabály leírását a megadott továbbítási entitásokhoz (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="13624-111">The **Set-AzRelayAuthorizationRule** cmdlet updates the description for the specified authorization rule of the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="13624-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="13624-112">EXAMPLES</span></span>

### <span data-ttu-id="13624-113">1.1. példa – Namespace with InputObject</span><span class="sxs-lookup"><span data-stu-id="13624-113">Example 1.1 - Namespace with InputObject</span></span>
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

<span data-ttu-id="13624-114">Hozzáadja a **Küldés** lehetőséget a névtér engedélyezési szabályának hozzáférési `AuthoRule1` `TestNameSpace-Relay1` jogaiból.</span><span class="sxs-lookup"><span data-stu-id="13624-114">Adds **Send** from the access rights of the authorization rule `AuthoRule1` in namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="13624-115">1.2. példa – Namespace with Rights paraméter</span><span class="sxs-lookup"><span data-stu-id="13624-115">Example 1.2 - Namespace with Rights parameter</span></span>
```
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -AuthorizationRule AuthoRule1 -Rights "Send"

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1
```

<span data-ttu-id="13624-116">Hozzáadja a **Küldés** lehetőséget a névtér engedélyezési szabályának hozzáférési `AuthoRule1` `TestNameSpace-Relay1` jogaiból.</span><span class="sxs-lookup"><span data-stu-id="13624-116">Adds **Send** from the access rights of the authorization rule `AuthoRule1` in namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="13624-117">2.1. példa – WcfRelay az InputObject értékekkel</span><span class="sxs-lookup"><span data-stu-id="13624-117">Example 2.1 - WcfRelay with InputObject</span></span>
```
PS C:\> $getWcfRelayAutho = Get-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1
PS C:\> $getWcfRelayAutho.Rights.Add("Send")
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -InputObject $getWcfRelayAutho

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1
```

<span data-ttu-id="13624-118">Hozzáadja a **Küldés** lehetőséget a `AuthoRule1` WcfRelay engedélyezési szabályának hozzáférési `TestWCFRelay1` jogaihoz.</span><span class="sxs-lookup"><span data-stu-id="13624-118">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="13624-119">2.2. példa – WcfRelay a Rights paraméterrel</span><span class="sxs-lookup"><span data-stu-id="13624-119">Example 2.2 - WcfRelay with Rights parameter</span></span>
```
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -Rights "Send"

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1
```

<span data-ttu-id="13624-120">Hozzáadja a **Küldés** lehetőséget a `AuthoRule1` WcfRelay engedélyezési szabályának hozzáférési `TestWCFRelay1` jogaihoz.</span><span class="sxs-lookup"><span data-stu-id="13624-120">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="13624-121">3.1. példa – Hibrid összekapcsolás az InputObjecttel</span><span class="sxs-lookup"><span data-stu-id="13624-121">Example 3.1 - HybridConnection with InputObject</span></span>
```
PS C:\> $GetHybirdAutho = Get-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
PS C:\> $GetHybirdAutho.Rights.Add("Send")
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -InputObject $GetHybirdAutho

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="13624-122">Hozzáadja a **Küldés** lehetőséget a HibridConnection engedélyezési szabályának `AuthoRule1` hozzáférési `TestHybridConnection` jogaihoz.</span><span class="sxs-lookup"><span data-stu-id="13624-122">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection`.</span></span>

### <span data-ttu-id="13624-123">3.2. példa – HybridConnection with Rights paraméter</span><span class="sxs-lookup"><span data-stu-id="13624-123">Example 3.2 - HybridConnection with Rights parameter</span></span>
```
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -Rights "Send"

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="13624-124">Hozzáadja a **Küldés** lehetőséget a HibridConnection engedélyezési szabályának `AuthoRule1` hozzáférési `TestHybridConnection` jogaihoz.</span><span class="sxs-lookup"><span data-stu-id="13624-124">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection`.</span></span>

## <span data-ttu-id="13624-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="13624-125">PARAMETERS</span></span>

### <span data-ttu-id="13624-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13624-126">-DefaultProfile</span></span>
<span data-ttu-id="13624-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="13624-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13624-128">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="13624-128">-HybridConnection</span></span>
<span data-ttu-id="13624-129">Hibrid összekapcsolás neve.</span><span class="sxs-lookup"><span data-stu-id="13624-129">HybridConnection Name.</span></span>

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

### <span data-ttu-id="13624-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="13624-130">-InputObject</span></span>
<span data-ttu-id="13624-131">Relay AuthorizationRule objektum.</span><span class="sxs-lookup"><span data-stu-id="13624-131">Relay AuthorizationRule Object.</span></span>

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

### <span data-ttu-id="13624-132">-Name</span><span class="sxs-lookup"><span data-stu-id="13624-132">-Name</span></span>
<span data-ttu-id="13624-133">AuthorizationRule Name (EngedélyezésiSzabály neve) stb.</span><span class="sxs-lookup"><span data-stu-id="13624-133">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="13624-134">-Namespace</span><span class="sxs-lookup"><span data-stu-id="13624-134">-Namespace</span></span>
<span data-ttu-id="13624-135">Névtér neve.</span><span class="sxs-lookup"><span data-stu-id="13624-135">Namespace Name.</span></span>

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

### <span data-ttu-id="13624-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13624-136">-ResourceGroupName</span></span>
<span data-ttu-id="13624-137">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="13624-137">Resource Group Name.</span></span>

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

### <span data-ttu-id="13624-138">-Rights</span><span class="sxs-lookup"><span data-stu-id="13624-138">-Rights</span></span>
<span data-ttu-id="13624-139">Jogok, például @("Hallgatás","Küldés","Kezelés")</span><span class="sxs-lookup"><span data-stu-id="13624-139">Rights, e.g. @("Listen","Send","Manage")</span></span>

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

### <span data-ttu-id="13624-140">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="13624-140">-WcfRelay</span></span>
<span data-ttu-id="13624-141">WcfRelay Name.</span><span class="sxs-lookup"><span data-stu-id="13624-141">WcfRelay Name.</span></span>

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

### <span data-ttu-id="13624-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="13624-142">-Confirm</span></span>
<span data-ttu-id="13624-143">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="13624-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13624-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13624-144">-WhatIf</span></span>
<span data-ttu-id="13624-145">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="13624-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13624-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="13624-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13624-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13624-147">CommonParameters</span></span>
<span data-ttu-id="13624-148">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13624-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13624-149">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13624-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13624-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="13624-150">INPUTS</span></span>

### <span data-ttu-id="13624-151">System.String</span><span class="sxs-lookup"><span data-stu-id="13624-151">System.String</span></span>

### <span data-ttu-id="13624-152">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="13624-152">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

### <span data-ttu-id="13624-153">System.String[]</span><span class="sxs-lookup"><span data-stu-id="13624-153">System.String[]</span></span>

## <span data-ttu-id="13624-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="13624-154">OUTPUTS</span></span>

### <span data-ttu-id="13624-155">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="13624-155">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="13624-156">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="13624-156">NOTES</span></span>

## <span data-ttu-id="13624-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="13624-157">RELATED LINKS</span></span>
