---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/new-azurermrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayAuthorizationRule.md
ms.openlocfilehash: daa2d1539a97b7aff7348fe8e603179c857c73db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679719"
---
# <span data-ttu-id="2b417-101">New-AzureRmRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="2b417-101">New-AzureRmRelayAuthorizationRule</span></span>

## <span data-ttu-id="2b417-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2b417-102">SYNOPSIS</span></span>
<span data-ttu-id="2b417-103">Új engedélyezési szabály létrehozása a megadott továbbítóügynök számára (névtér/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="2b417-103">Creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b417-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2b417-104">SYNTAX</span></span>

### <span data-ttu-id="2b417-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2b417-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b417-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="2b417-106">WcfRelayAuthorizationRuleSet</span></span>
```
New-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2b417-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="2b417-107">HybridConnectionAuthorizationRuleSet</span></span>
```
New-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b417-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="2b417-108">DESCRIPTION</span></span>
<span data-ttu-id="2b417-109">A **New-AzureRmRelayAuthorizationRule** parancsmag új engedélyezési szabályt hoz létre a megadott továbbítóügynökök (Namespace/WcfRelay/HybridConnection) számára.</span><span class="sxs-lookup"><span data-stu-id="2b417-109">The **New-AzureRmRelayAuthorizationRule** cmdlet creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="2b417-110">Példák</span><span class="sxs-lookup"><span data-stu-id="2b417-110">EXAMPLES</span></span>

### <span data-ttu-id="2b417-111">Példa 1 – névtér</span><span class="sxs-lookup"><span data-stu-id="2b417-111">Example 1 - Namespace</span></span>
```
PS C:\>New-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -Rights "Listen"
```

<span data-ttu-id="2b417-112">`AuthoRule1`A névtér **figyelési** jogosultságait hozza létre `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="2b417-112">Creates `AuthoRule1` with **Listen** rights for the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="2b417-113">Példa 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="2b417-113">Example 2 - WcfRelay</span></span>
```
PS C:\>New-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -Rights "Listen"
```

<span data-ttu-id="2b417-114">Engedélyezési szabály létrehozása `AuthoRule1` a WcfRelay **figyelési** jogaival `TestWCFRelay1`</span><span class="sxs-lookup"><span data-stu-id="2b417-114">Creates authorization rule `AuthoRule1` with **Listen** rights for the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="2b417-115">Példa: 3 – HybridConnection</span><span class="sxs-lookup"><span data-stu-id="2b417-115">Example 3 - HybridConnection</span></span>
```
PS C:\>New-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -Rights "Listen"
```

<span data-ttu-id="2b417-116">`AuthoRule1`A névtér **figyelési** jogosultságait hozza létre `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="2b417-116">Creates `AuthoRule1` with **Listen** rights for the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="2b417-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2b417-117">PARAMETERS</span></span>

### <span data-ttu-id="2b417-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b417-118">-DefaultProfile</span></span>
<span data-ttu-id="2b417-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2b417-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b417-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="2b417-120">-HybridConnection</span></span>
<span data-ttu-id="2b417-121">HybridConnection neve</span><span class="sxs-lookup"><span data-stu-id="2b417-121">HybridConnection Name.</span></span>

```yaml
Type: String
Parameter Sets: HybridConnectionAuthorizationRuleSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b417-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2b417-122">-Name</span></span>
<span data-ttu-id="2b417-123">AuthorizationRule neve</span><span class="sxs-lookup"><span data-stu-id="2b417-123">AuthorizationRule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b417-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2b417-124">-Namespace</span></span>
<span data-ttu-id="2b417-125">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="2b417-125">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b417-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b417-126">-ResourceGroupName</span></span>
<span data-ttu-id="2b417-127">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="2b417-127">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b417-128">– Jogok</span><span class="sxs-lookup"><span data-stu-id="2b417-128">-Rights</span></span>
<span data-ttu-id="2b417-129">Jogok (például "Figyelj", "Küldés", "kezelés")</span><span class="sxs-lookup"><span data-stu-id="2b417-129">Rights, e.g. "Listen","Send","Manage"</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 
Accepted values: Listen, Send, Manage

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b417-130">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="2b417-130">-WcfRelay</span></span>
<span data-ttu-id="2b417-131">WcfRelay neve</span><span class="sxs-lookup"><span data-stu-id="2b417-131">WcfRelay Name.</span></span>

```yaml
Type: String
Parameter Sets: WcfRelayAuthorizationRuleSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b417-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2b417-132">-Confirm</span></span>
<span data-ttu-id="2b417-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2b417-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b417-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b417-134">-WhatIf</span></span>
<span data-ttu-id="2b417-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2b417-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b417-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2b417-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b417-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b417-137">CommonParameters</span></span>
<span data-ttu-id="2b417-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2b417-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b417-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b417-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b417-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2b417-140">INPUTS</span></span>

### <span data-ttu-id="2b417-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b417-141">-ResourceGroupName</span></span>
 <span data-ttu-id="2b417-142">System. String</span><span class="sxs-lookup"><span data-stu-id="2b417-142">System.String</span></span> 

### <span data-ttu-id="2b417-143">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2b417-143">-Namespace</span></span>
 <span data-ttu-id="2b417-144">System. String</span><span class="sxs-lookup"><span data-stu-id="2b417-144">System.String</span></span> 
 

### <span data-ttu-id="2b417-145">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="2b417-145">-WcfRelay</span></span>
 <span data-ttu-id="2b417-146">System. String</span><span class="sxs-lookup"><span data-stu-id="2b417-146">System.String</span></span> 

### <span data-ttu-id="2b417-147">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="2b417-147">-HybridConnection</span></span>
 <span data-ttu-id="2b417-148">System. String</span><span class="sxs-lookup"><span data-stu-id="2b417-148">System.String</span></span> 
 

### <span data-ttu-id="2b417-149">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2b417-149">-Name</span></span>
 <span data-ttu-id="2b417-150">System. String</span><span class="sxs-lookup"><span data-stu-id="2b417-150">System.String</span></span>
 

### <span data-ttu-id="2b417-151">– Jogok</span><span class="sxs-lookup"><span data-stu-id="2b417-151">-Rights</span></span>
 <span data-ttu-id="2b417-152">System. string []</span><span class="sxs-lookup"><span data-stu-id="2b417-152">System.String []</span></span>

## <span data-ttu-id="2b417-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2b417-153">OUTPUTS</span></span>

### <span data-ttu-id="2b417-154">Microsoft. Azure. Command. Relay. models. AuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="2b417-154">Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleAttributes</span></span>

### <span data-ttu-id="2b417-155">Példa 1 – névtér</span><span class="sxs-lookup"><span data-stu-id="2b417-155">Example 1 - Namespace</span></span>
<span data-ttu-id="2b417-156">Jogok: {Listen} név: AuthoRule1 Type: Microsoft. Relay/AuthorizationRules ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="2b417-156">Rights : {Listen} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1</span></span>

### <span data-ttu-id="2b417-157">Példa 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="2b417-157">Example 2 - WcfRelay</span></span>
<span data-ttu-id="2b417-158">Jogok: {Listen} név: AuthoRule1 Type: Microsoft. Relay/AuthorizationRules ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="2b417-158">Rights : {Listen} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1</span></span>

### <span data-ttu-id="2b417-159">Példa: 3 – HybridConnection</span><span class="sxs-lookup"><span data-stu-id="2b417-159">Example 3 - HybridConnection</span></span>
<span data-ttu-id="2b417-160">Jogok: {Listen} név: AuthoRule1 Type: Microsoft. Relay/AuthorizationRules ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="2b417-160">Rights : {Listen} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1</span></span>

## <span data-ttu-id="2b417-161">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2b417-161">NOTES</span></span>

## <span data-ttu-id="2b417-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2b417-162">RELATED LINKS</span></span>

