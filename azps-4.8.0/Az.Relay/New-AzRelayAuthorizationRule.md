---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayAuthorizationRule.md
ms.openlocfilehash: 39bba687e355b1742210fb0c37fc8f1a65d957a0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184694"
---
# <span data-ttu-id="8166f-101">New-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="8166f-101">New-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="8166f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8166f-102">SYNOPSIS</span></span>
<span data-ttu-id="8166f-103">Új engedélyezési szabály létrehozása a megadott továbbítóügynök számára (névtér/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="8166f-103">Creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="8166f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8166f-104">SYNTAX</span></span>

### <span data-ttu-id="8166f-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8166f-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8166f-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="8166f-106">WcfRelayAuthorizationRuleSet</span></span>
```
New-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8166f-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="8166f-107">HybridConnectionAuthorizationRuleSet</span></span>
```
New-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8166f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="8166f-108">DESCRIPTION</span></span>
<span data-ttu-id="8166f-109">A **New-AzRelayAuthorizationRule** parancsmag új engedélyezési szabályt hoz létre a megadott továbbítóügynökök (Namespace/WcfRelay/HybridConnection) számára.</span><span class="sxs-lookup"><span data-stu-id="8166f-109">The **New-AzRelayAuthorizationRule** cmdlet creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="8166f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="8166f-110">EXAMPLES</span></span>

### <span data-ttu-id="8166f-111">Példa 1: Namespace</span><span class="sxs-lookup"><span data-stu-id="8166f-111">Example 1: Namespace</span></span>
```powershell
PS C:\>New-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1
```

<span data-ttu-id="8166f-112">`AuthoRule1`A névtér **figyelési** jogosultságait hozza létre `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="8166f-112">Creates `AuthoRule1` with **Listen** rights for the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="8166f-113">2. példa: WcfRelay</span><span class="sxs-lookup"><span data-stu-id="8166f-113">Example 2: WcfRelay</span></span>
```powershell
PS C:\>New-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1
```

<span data-ttu-id="8166f-114">Engedélyezési szabály létrehozása `AuthoRule1` a WcfRelay **figyelési** jogaival `TestWCFRelay1`</span><span class="sxs-lookup"><span data-stu-id="8166f-114">Creates authorization rule `AuthoRule1` with **Listen** rights for the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="8166f-115">3. példa: HybridConnection</span><span class="sxs-lookup"><span data-stu-id="8166f-115">Example 3: HybridConnection</span></span>
```powershell
PS C:\>New-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="8166f-116">`AuthoRule1`A hibrid kapcsolat **figyelési** jogát hozza létre `TestHybridConnection` .</span><span class="sxs-lookup"><span data-stu-id="8166f-116">Creates `AuthoRule1` with **Listen** rights for the Hybrid Connection `TestHybridConnection`.</span></span>

## <span data-ttu-id="8166f-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8166f-117">PARAMETERS</span></span>

### <span data-ttu-id="8166f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8166f-118">-DefaultProfile</span></span>
<span data-ttu-id="8166f-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8166f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8166f-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="8166f-120">-HybridConnection</span></span>
<span data-ttu-id="8166f-121">HybridConnection neve</span><span class="sxs-lookup"><span data-stu-id="8166f-121">HybridConnection Name.</span></span>

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

### <span data-ttu-id="8166f-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8166f-122">-Name</span></span>
<span data-ttu-id="8166f-123">AuthorizationRule neve</span><span class="sxs-lookup"><span data-stu-id="8166f-123">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="8166f-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="8166f-124">-Namespace</span></span>
<span data-ttu-id="8166f-125">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="8166f-125">Namespace Name.</span></span>

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

### <span data-ttu-id="8166f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8166f-126">-ResourceGroupName</span></span>
<span data-ttu-id="8166f-127">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="8166f-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="8166f-128">– Jogok</span><span class="sxs-lookup"><span data-stu-id="8166f-128">-Rights</span></span>
<span data-ttu-id="8166f-129">Jogok (például "Figyelj", "Küldés", "kezelés")</span><span class="sxs-lookup"><span data-stu-id="8166f-129">Rights, e.g. "Listen","Send","Manage"</span></span>

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

### <span data-ttu-id="8166f-130">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="8166f-130">-WcfRelay</span></span>
<span data-ttu-id="8166f-131">WcfRelay neve</span><span class="sxs-lookup"><span data-stu-id="8166f-131">WcfRelay Name.</span></span>

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

### <span data-ttu-id="8166f-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8166f-132">-Confirm</span></span>
<span data-ttu-id="8166f-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8166f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8166f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8166f-134">-WhatIf</span></span>
<span data-ttu-id="8166f-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8166f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8166f-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8166f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8166f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8166f-137">CommonParameters</span></span>
<span data-ttu-id="8166f-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8166f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8166f-139">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8166f-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8166f-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8166f-140">INPUTS</span></span>

### <span data-ttu-id="8166f-141">System. String</span><span class="sxs-lookup"><span data-stu-id="8166f-141">System.String</span></span>

### <span data-ttu-id="8166f-142">System. string []</span><span class="sxs-lookup"><span data-stu-id="8166f-142">System.String[]</span></span>

## <span data-ttu-id="8166f-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8166f-143">OUTPUTS</span></span>

### <span data-ttu-id="8166f-144">Microsoft. Azure. Command. Relay. models. PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="8166f-144">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="8166f-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8166f-145">NOTES</span></span>

## <span data-ttu-id="8166f-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8166f-146">RELATED LINKS</span></span>
