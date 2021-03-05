---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/new-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayAuthorizationRule.md
ms.openlocfilehash: d0faea052141420db88f58fd6513c2d6822f56c7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000566"
---
# <span data-ttu-id="db009-101">New-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="db009-101">New-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="db009-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db009-102">SYNOPSIS</span></span>
<span data-ttu-id="db009-103">Létrehoz egy új engedélyezési szabályt a megadott továbbítási entitásokhoz (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="db009-103">Creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="db009-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="db009-104">SYNTAX</span></span>

### <span data-ttu-id="db009-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="db009-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db009-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="db009-106">WcfRelayAuthorizationRuleSet</span></span>
```
New-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="db009-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="db009-107">HybridConnectionAuthorizationRuleSet</span></span>
```
New-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="db009-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="db009-108">DESCRIPTION</span></span>
<span data-ttu-id="db009-109">A **New-AzRelayAuthorizationRule** parancsmag létrehoz egy új engedélyezési szabályt a megadott továbbítási entitásokhoz (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="db009-109">The **New-AzRelayAuthorizationRule** cmdlet creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="db009-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="db009-110">EXAMPLES</span></span>

### <span data-ttu-id="db009-111">1. példa: Namespace</span><span class="sxs-lookup"><span data-stu-id="db009-111">Example 1: Namespace</span></span>
```powershell
PS C:\>New-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1
```

<span data-ttu-id="db009-112">A `AuthoRule1` **névtérhez hallgató** jogokat hoz `TestNameSpace-Relay1` létre.</span><span class="sxs-lookup"><span data-stu-id="db009-112">Creates `AuthoRule1` with **Listen** rights for the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="db009-113">2. példa: WcfRelay</span><span class="sxs-lookup"><span data-stu-id="db009-113">Example 2: WcfRelay</span></span>
```powershell
PS C:\>New-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1
```

<span data-ttu-id="db009-114">Engedélyezési szabályt `AuthoRule1`  hoz létre a WcfRelay figyelése `TestWCFRelay1` jogosultságokkal.</span><span class="sxs-lookup"><span data-stu-id="db009-114">Creates authorization rule `AuthoRule1` with **Listen** rights for the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="db009-115">3. példa: Hibrid összekapcsolás</span><span class="sxs-lookup"><span data-stu-id="db009-115">Example 3: HybridConnection</span></span>
```powershell
PS C:\>New-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="db009-116">A `AuthoRule1` hibrid **kapcsolathoz hallgató** jogokkal hozza `TestHybridConnection` létre.</span><span class="sxs-lookup"><span data-stu-id="db009-116">Creates `AuthoRule1` with **Listen** rights for the Hybrid Connection `TestHybridConnection`.</span></span>

## <span data-ttu-id="db009-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="db009-117">PARAMETERS</span></span>

### <span data-ttu-id="db009-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db009-118">-DefaultProfile</span></span>
<span data-ttu-id="db009-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="db009-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db009-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="db009-120">-HybridConnection</span></span>
<span data-ttu-id="db009-121">Hibrid összekapcsolás neve.</span><span class="sxs-lookup"><span data-stu-id="db009-121">HybridConnection Name.</span></span>

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

### <span data-ttu-id="db009-122">-Name</span><span class="sxs-lookup"><span data-stu-id="db009-122">-Name</span></span>
<span data-ttu-id="db009-123">AuthorizationRule Name (EngedélyezésiSzabály neve) stb.</span><span class="sxs-lookup"><span data-stu-id="db009-123">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="db009-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="db009-124">-Namespace</span></span>
<span data-ttu-id="db009-125">Névtér neve.</span><span class="sxs-lookup"><span data-stu-id="db009-125">Namespace Name.</span></span>

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

### <span data-ttu-id="db009-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db009-126">-ResourceGroupName</span></span>
<span data-ttu-id="db009-127">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="db009-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="db009-128">-Rights</span><span class="sxs-lookup"><span data-stu-id="db009-128">-Rights</span></span>
<span data-ttu-id="db009-129">Jogok, például "Figyel", "Küldés", "Kezelés"</span><span class="sxs-lookup"><span data-stu-id="db009-129">Rights, e.g. "Listen","Send","Manage"</span></span>

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

### <span data-ttu-id="db009-130">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="db009-130">-WcfRelay</span></span>
<span data-ttu-id="db009-131">WcfRelay Name.</span><span class="sxs-lookup"><span data-stu-id="db009-131">WcfRelay Name.</span></span>

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

### <span data-ttu-id="db009-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="db009-132">-Confirm</span></span>
<span data-ttu-id="db009-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="db009-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db009-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db009-134">-WhatIf</span></span>
<span data-ttu-id="db009-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="db009-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db009-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="db009-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db009-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db009-137">CommonParameters</span></span>
<span data-ttu-id="db009-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db009-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db009-139">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db009-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db009-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="db009-140">INPUTS</span></span>

### <span data-ttu-id="db009-141">System.String</span><span class="sxs-lookup"><span data-stu-id="db009-141">System.String</span></span>

### <span data-ttu-id="db009-142">System.String[]</span><span class="sxs-lookup"><span data-stu-id="db009-142">System.String[]</span></span>

## <span data-ttu-id="db009-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="db009-143">OUTPUTS</span></span>

### <span data-ttu-id="db009-144">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="db009-144">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="db009-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="db009-145">NOTES</span></span>

## <span data-ttu-id="db009-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="db009-146">RELATED LINKS</span></span>
