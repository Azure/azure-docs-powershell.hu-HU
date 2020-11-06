---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayAuthorizationRule.md
ms.openlocfilehash: 9e4eecad543346efa60dfb0b9a20e31c47a59036
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494713"
---
# <span data-ttu-id="4b5f5-101">New-AzureRmRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="4b5f5-101">New-AzureRmRelayAuthorizationRule</span></span>

## <span data-ttu-id="4b5f5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4b5f5-102">SYNOPSIS</span></span>
<span data-ttu-id="4b5f5-103">Új engedélyezési szabály létrehozása a megadott továbbítóügynök számára (névtér/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="4b5f5-103">Creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b5f5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4b5f5-104">SYNTAX</span></span>

### <span data-ttu-id="4b5f5-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4b5f5-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b5f5-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="4b5f5-106">WcfRelayAuthorizationRuleSet</span></span>
```
New-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4b5f5-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="4b5f5-107">HybridConnectionAuthorizationRuleSet</span></span>
```
New-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b5f5-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="4b5f5-108">DESCRIPTION</span></span>
<span data-ttu-id="4b5f5-109">A **New-AzureRmRelayAuthorizationRule** parancsmag új engedélyezési szabályt hoz létre a megadott továbbítóügynökök (Namespace/WcfRelay/HybridConnection) számára.</span><span class="sxs-lookup"><span data-stu-id="4b5f5-109">The **New-AzureRmRelayAuthorizationRule** cmdlet creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="4b5f5-110">Példák</span><span class="sxs-lookup"><span data-stu-id="4b5f5-110">EXAMPLES</span></span>

### <span data-ttu-id="4b5f5-111">Példa 1 – névtér</span><span class="sxs-lookup"><span data-stu-id="4b5f5-111">Example 1 - Namespace</span></span>
```
PS C:\>New-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -Rights "Listen"
```

<span data-ttu-id="4b5f5-112">`AuthoRule1`A névtér **figyelési** jogosultságait hozza létre `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="4b5f5-112">Creates `AuthoRule1` with **Listen** rights for the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="4b5f5-113">Példa 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="4b5f5-113">Example 2 - WcfRelay</span></span>
```
PS C:\>New-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -Rights "Listen"
```

<span data-ttu-id="4b5f5-114">Engedélyezési szabály létrehozása `AuthoRule1` a WcfRelay **figyelési** jogaival `TestWCFRelay1`</span><span class="sxs-lookup"><span data-stu-id="4b5f5-114">Creates authorization rule `AuthoRule1` with **Listen** rights for the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="4b5f5-115">Példa: 3 – HybridConnection</span><span class="sxs-lookup"><span data-stu-id="4b5f5-115">Example 3 - HybridConnection</span></span>
```
PS C:\>New-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -Rights "Listen"
```

<span data-ttu-id="4b5f5-116">`AuthoRule1`A névtér **figyelési** jogosultságait hozza létre `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="4b5f5-116">Creates `AuthoRule1` with **Listen** rights for the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="4b5f5-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4b5f5-117">PARAMETERS</span></span>

### <span data-ttu-id="4b5f5-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4b5f5-118">-Confirm</span></span>
<span data-ttu-id="4b5f5-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4b5f5-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b5f5-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="4b5f5-120">-HybridConnection</span></span>
<span data-ttu-id="4b5f5-121">HybridConnection neve</span><span class="sxs-lookup"><span data-stu-id="4b5f5-121">HybridConnection Name.</span></span>

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

### <span data-ttu-id="4b5f5-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4b5f5-122">-Name</span></span>
<span data-ttu-id="4b5f5-123">AuthorizationRule neve</span><span class="sxs-lookup"><span data-stu-id="4b5f5-123">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="4b5f5-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4b5f5-124">-Namespace</span></span>
<span data-ttu-id="4b5f5-125">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="4b5f5-125">Namespace Name.</span></span>

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

### <span data-ttu-id="4b5f5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b5f5-126">-ResourceGroupName</span></span>
<span data-ttu-id="4b5f5-127">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="4b5f5-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="4b5f5-128">– Jogok</span><span class="sxs-lookup"><span data-stu-id="4b5f5-128">-Rights</span></span>
<span data-ttu-id="4b5f5-129">Jogok (például "Figyelj", "Küldés", "kezelés")</span><span class="sxs-lookup"><span data-stu-id="4b5f5-129">Rights, e.g. "Listen","Send","Manage"</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b5f5-130">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="4b5f5-130">-WcfRelay</span></span>
<span data-ttu-id="4b5f5-131">WcfRelay neve</span><span class="sxs-lookup"><span data-stu-id="4b5f5-131">WcfRelay Name.</span></span>

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

### <span data-ttu-id="4b5f5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b5f5-132">-WhatIf</span></span>
<span data-ttu-id="4b5f5-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4b5f5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b5f5-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4b5f5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b5f5-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b5f5-135">-DefaultProfile</span></span>
<span data-ttu-id="4b5f5-136">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4b5f5-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b5f5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b5f5-137">CommonParameters</span></span>
<span data-ttu-id="4b5f5-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4b5f5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b5f5-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b5f5-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b5f5-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4b5f5-140">INPUTS</span></span>

### <span data-ttu-id="4b5f5-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b5f5-141">-ResourceGroupName</span></span>
 <span data-ttu-id="4b5f5-142">System. String</span><span class="sxs-lookup"><span data-stu-id="4b5f5-142">System.String</span></span> 

### <span data-ttu-id="4b5f5-143">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4b5f5-143">-Namespace</span></span>
 <span data-ttu-id="4b5f5-144">System. String</span><span class="sxs-lookup"><span data-stu-id="4b5f5-144">System.String</span></span> 
 

### <span data-ttu-id="4b5f5-145">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="4b5f5-145">-WcfRelay</span></span>
 <span data-ttu-id="4b5f5-146">System. String</span><span class="sxs-lookup"><span data-stu-id="4b5f5-146">System.String</span></span> 

### <span data-ttu-id="4b5f5-147">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="4b5f5-147">-HybridConnection</span></span>
 <span data-ttu-id="4b5f5-148">System. String</span><span class="sxs-lookup"><span data-stu-id="4b5f5-148">System.String</span></span> 
 

### <span data-ttu-id="4b5f5-149">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4b5f5-149">-Name</span></span>
 <span data-ttu-id="4b5f5-150">System. String</span><span class="sxs-lookup"><span data-stu-id="4b5f5-150">System.String</span></span>
 

### <span data-ttu-id="4b5f5-151">– Jogok</span><span class="sxs-lookup"><span data-stu-id="4b5f5-151">-Rights</span></span>
 <span data-ttu-id="4b5f5-152">System. string []</span><span class="sxs-lookup"><span data-stu-id="4b5f5-152">System.String []</span></span>

## <span data-ttu-id="4b5f5-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4b5f5-153">OUTPUTS</span></span>

### <span data-ttu-id="4b5f5-154">Microsoft. Azure. Command. Relay. models. AuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="4b5f5-154">Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleAttributes</span></span>

### <span data-ttu-id="4b5f5-155">Példa 1 – névtér</span><span class="sxs-lookup"><span data-stu-id="4b5f5-155">Example 1 - Namespace</span></span>
<span data-ttu-id="4b5f5-156">Jogok: {Listen} név: AuthoRule1 Type: Microsoft. Relay/AuthorizationRules ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="4b5f5-156">Rights : {Listen} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1</span></span>

### <span data-ttu-id="4b5f5-157">Példa 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="4b5f5-157">Example 2 - WcfRelay</span></span>
<span data-ttu-id="4b5f5-158">Jogok: {Listen} név: AuthoRule1 Type: Microsoft. Relay/AuthorizationRules ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="4b5f5-158">Rights : {Listen} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1</span></span>

### <span data-ttu-id="4b5f5-159">Példa: 3 – HybridConnection</span><span class="sxs-lookup"><span data-stu-id="4b5f5-159">Example 3 - HybridConnection</span></span>
<span data-ttu-id="4b5f5-160">Jogok: {Listen} név: AuthoRule1 Type: Microsoft. Relay/AuthorizationRules ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="4b5f5-160">Rights : {Listen} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1</span></span>

## <span data-ttu-id="4b5f5-161">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4b5f5-161">NOTES</span></span>

## <span data-ttu-id="4b5f5-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4b5f5-162">RELATED LINKS</span></span>

