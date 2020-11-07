---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayAuthorizationRule.md
ms.openlocfilehash: ed50beeddbb0e9d85457952b1fcc524d8ee2dcd5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846889"
---
# <span data-ttu-id="f8b79-101">New-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f8b79-101">New-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="f8b79-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f8b79-102">SYNOPSIS</span></span>
<span data-ttu-id="f8b79-103">Új engedélyezési szabály létrehozása a megadott továbbítóügynök számára (névtér/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="f8b79-103">Creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="f8b79-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f8b79-104">SYNTAX</span></span>

### <span data-ttu-id="f8b79-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f8b79-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8b79-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="f8b79-106">WcfRelayAuthorizationRuleSet</span></span>
```
New-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f8b79-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="f8b79-107">HybridConnectionAuthorizationRuleSet</span></span>
```
New-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f8b79-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f8b79-108">DESCRIPTION</span></span>
<span data-ttu-id="f8b79-109">A **New-AzRelayAuthorizationRule** parancsmag új engedélyezési szabályt hoz létre a megadott továbbítóügynökök (Namespace/WcfRelay/HybridConnection) számára.</span><span class="sxs-lookup"><span data-stu-id="f8b79-109">The **New-AzRelayAuthorizationRule** cmdlet creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="f8b79-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f8b79-110">EXAMPLES</span></span>

### <span data-ttu-id="f8b79-111">Példa 1 – névtér</span><span class="sxs-lookup"><span data-stu-id="f8b79-111">Example 1 - Namespace</span></span>
```
PS C:\>New-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1
```

<span data-ttu-id="f8b79-112">`AuthoRule1`A névtér **figyelési** jogosultságait hozza létre `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="f8b79-112">Creates `AuthoRule1` with **Listen** rights for the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="f8b79-113">Példa 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="f8b79-113">Example 2 - WcfRelay</span></span>
```
PS C:\>New-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1
```

<span data-ttu-id="f8b79-114">Engedélyezési szabály létrehozása `AuthoRule1` a WcfRelay **figyelési** jogaival `TestWCFRelay1`</span><span class="sxs-lookup"><span data-stu-id="f8b79-114">Creates authorization rule `AuthoRule1` with **Listen** rights for the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="f8b79-115">Példa: 3 – HybridConnection</span><span class="sxs-lookup"><span data-stu-id="f8b79-115">Example 3 - HybridConnection</span></span>
```
PS C:\>New-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="f8b79-116">`AuthoRule1`A hibrid kapcsolat **figyelési** jogát hozza létre `TestHybridConnection` .</span><span class="sxs-lookup"><span data-stu-id="f8b79-116">Creates `AuthoRule1` with **Listen** rights for the Hybrid Connection `TestHybridConnection`.</span></span>

## <span data-ttu-id="f8b79-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f8b79-117">PARAMETERS</span></span>

### <span data-ttu-id="f8b79-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8b79-118">-DefaultProfile</span></span>
<span data-ttu-id="f8b79-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f8b79-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8b79-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="f8b79-120">-HybridConnection</span></span>
<span data-ttu-id="f8b79-121">HybridConnection neve</span><span class="sxs-lookup"><span data-stu-id="f8b79-121">HybridConnection Name.</span></span>

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

### <span data-ttu-id="f8b79-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f8b79-122">-Name</span></span>
<span data-ttu-id="f8b79-123">AuthorizationRule neve</span><span class="sxs-lookup"><span data-stu-id="f8b79-123">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="f8b79-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f8b79-124">-Namespace</span></span>
<span data-ttu-id="f8b79-125">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="f8b79-125">Namespace Name.</span></span>

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

### <span data-ttu-id="f8b79-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8b79-126">-ResourceGroupName</span></span>
<span data-ttu-id="f8b79-127">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="f8b79-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="f8b79-128">– Jogok</span><span class="sxs-lookup"><span data-stu-id="f8b79-128">-Rights</span></span>
<span data-ttu-id="f8b79-129">Jogok (például "Figyelj", "Küldés", "kezelés")</span><span class="sxs-lookup"><span data-stu-id="f8b79-129">Rights, e.g. "Listen","Send","Manage"</span></span>

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

### <span data-ttu-id="f8b79-130">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="f8b79-130">-WcfRelay</span></span>
<span data-ttu-id="f8b79-131">WcfRelay neve</span><span class="sxs-lookup"><span data-stu-id="f8b79-131">WcfRelay Name.</span></span>

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

### <span data-ttu-id="f8b79-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f8b79-132">-Confirm</span></span>
<span data-ttu-id="f8b79-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f8b79-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8b79-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8b79-134">-WhatIf</span></span>
<span data-ttu-id="f8b79-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f8b79-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8b79-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f8b79-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8b79-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8b79-137">CommonParameters</span></span>
<span data-ttu-id="f8b79-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f8b79-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8b79-139">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8b79-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8b79-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f8b79-140">INPUTS</span></span>

### <span data-ttu-id="f8b79-141">System. String</span><span class="sxs-lookup"><span data-stu-id="f8b79-141">System.String</span></span>

### <span data-ttu-id="f8b79-142">System. string []</span><span class="sxs-lookup"><span data-stu-id="f8b79-142">System.String[]</span></span>

## <span data-ttu-id="f8b79-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f8b79-143">OUTPUTS</span></span>

### <span data-ttu-id="f8b79-144">Microsoft. Azure. Command. Relay. models. PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="f8b79-144">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="f8b79-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f8b79-145">NOTES</span></span>

## <span data-ttu-id="f8b79-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f8b79-146">RELATED LINKS</span></span>
