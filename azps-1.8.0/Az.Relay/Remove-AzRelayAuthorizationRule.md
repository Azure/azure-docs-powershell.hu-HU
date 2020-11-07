---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/remove-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayAuthorizationRule.md
ms.openlocfilehash: 8523fd6698e2fcdc4212b68a93269d60bc642628
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669501"
---
# <span data-ttu-id="b855a-101">Remove-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b855a-101">Remove-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="b855a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b855a-102">SYNOPSIS</span></span>
<span data-ttu-id="b855a-103">Eltávolítja egy HybridConnection engedélyezési szabályát az adott továbbító entitásokból (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="b855a-103">Removes the authorization rule of a HybridConnection from the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="b855a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b855a-104">SYNTAX</span></span>

### <span data-ttu-id="b855a-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b855a-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b855a-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="b855a-106">WcfRelayAuthorizationRuleSet</span></span>
```
Remove-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b855a-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="b855a-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Remove-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b855a-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b855a-108">DESCRIPTION</span></span>
<span data-ttu-id="b855a-109">A **Remove-AzRelayAuthorizationRule** parancsmag eltávolítja a megadott továbbítóügynök engedélyezési szabályait (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="b855a-109">The **Remove-AzRelayAuthorizationRule** cmdlet removes the authorization rule of the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="b855a-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b855a-110">EXAMPLES</span></span>

### <span data-ttu-id="b855a-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b855a-111">Example 1</span></span>
```
PS C:\> Remove-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1
```

<span data-ttu-id="b855a-112">Eltávolítja a névtér engedélyezési szabályát `AuthoRule1` `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="b855a-112">Removes the authorization rule `AuthoRule1` of the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="b855a-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="b855a-113">Example 2</span></span>
```
PS C:\> Remove-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWcfRelay -Name AuthoRule1
```

<span data-ttu-id="b855a-114">Eltávolítja a `AuthoRule1` névtérből származó WcfRelay engedélyezési szabályát `TestWcfRelay` `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="b855a-114">Removes the authorization rule `AuthoRule1` of the WcfRelay `TestWcfRelay` from the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="b855a-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="b855a-115">Example 3</span></span>
```
PS C:\> Remove-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
```

<span data-ttu-id="b855a-116">Eltávolítja a `AuthoRule1` névtérből származó HybridConnection engedélyezési szabályát `TestHybridConnection` `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="b855a-116">Removes the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="b855a-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b855a-117">PARAMETERS</span></span>

### <span data-ttu-id="b855a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b855a-118">-DefaultProfile</span></span>
<span data-ttu-id="b855a-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b855a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b855a-120">-Force</span><span class="sxs-lookup"><span data-stu-id="b855a-120">-Force</span></span>
<span data-ttu-id="b855a-121">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b855a-121">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b855a-122">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="b855a-122">-HybridConnection</span></span>
<span data-ttu-id="b855a-123">HybridConnection neve</span><span class="sxs-lookup"><span data-stu-id="b855a-123">HybridConnection Name.</span></span>

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

### <span data-ttu-id="b855a-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b855a-124">-Name</span></span>
<span data-ttu-id="b855a-125">AuthorizationRule neve</span><span class="sxs-lookup"><span data-stu-id="b855a-125">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="b855a-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b855a-126">-Namespace</span></span>
<span data-ttu-id="b855a-127">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="b855a-127">Namespace Name.</span></span>

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

### <span data-ttu-id="b855a-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b855a-128">-PassThru</span></span>
<span data-ttu-id="b855a-129">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="b855a-129">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b855a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b855a-130">-ResourceGroupName</span></span>
<span data-ttu-id="b855a-131">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="b855a-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="b855a-132">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="b855a-132">-WcfRelay</span></span>
<span data-ttu-id="b855a-133">WcfRelay neve</span><span class="sxs-lookup"><span data-stu-id="b855a-133">WcfRelay Name.</span></span>

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

### <span data-ttu-id="b855a-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b855a-134">-Confirm</span></span>
<span data-ttu-id="b855a-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b855a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b855a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b855a-136">-WhatIf</span></span>
<span data-ttu-id="b855a-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b855a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b855a-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b855a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b855a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b855a-139">CommonParameters</span></span>
<span data-ttu-id="b855a-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b855a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b855a-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b855a-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b855a-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b855a-142">INPUTS</span></span>

### <span data-ttu-id="b855a-143">System. String</span><span class="sxs-lookup"><span data-stu-id="b855a-143">System.String</span></span>

## <span data-ttu-id="b855a-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b855a-144">OUTPUTS</span></span>

### <span data-ttu-id="b855a-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b855a-145">System.Boolean</span></span>

## <span data-ttu-id="b855a-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b855a-146">NOTES</span></span>

## <span data-ttu-id="b855a-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b855a-147">RELATED LINKS</span></span>
