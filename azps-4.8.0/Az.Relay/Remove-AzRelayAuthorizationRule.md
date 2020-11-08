---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/remove-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayAuthorizationRule.md
ms.openlocfilehash: f99330a7611964e8db3d41f4ece56bb247c1c403
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025065"
---
# <span data-ttu-id="94f5c-101">Remove-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="94f5c-101">Remove-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="94f5c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="94f5c-102">SYNOPSIS</span></span>
<span data-ttu-id="94f5c-103">Eltávolítja egy HybridConnection engedélyezési szabályát az adott továbbító entitásokból (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="94f5c-103">Removes the authorization rule of a HybridConnection from the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="94f5c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="94f5c-104">SYNTAX</span></span>

### <span data-ttu-id="94f5c-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="94f5c-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94f5c-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="94f5c-106">WcfRelayAuthorizationRuleSet</span></span>
```
Remove-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="94f5c-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="94f5c-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Remove-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94f5c-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="94f5c-108">DESCRIPTION</span></span>
<span data-ttu-id="94f5c-109">A **Remove-AzRelayAuthorizationRule** parancsmag eltávolítja a megadott továbbítóügynök engedélyezési szabályait (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="94f5c-109">The **Remove-AzRelayAuthorizationRule** cmdlet removes the authorization rule of the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="94f5c-110">Példák</span><span class="sxs-lookup"><span data-stu-id="94f5c-110">EXAMPLES</span></span>

### <span data-ttu-id="94f5c-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="94f5c-111">Example 1</span></span>
```
PS C:\> Remove-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1
```

<span data-ttu-id="94f5c-112">Eltávolítja a névtér engedélyezési szabályát `AuthoRule1` `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="94f5c-112">Removes the authorization rule `AuthoRule1` of the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="94f5c-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="94f5c-113">Example 2</span></span>
```
PS C:\> Remove-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWcfRelay -Name AuthoRule1
```

<span data-ttu-id="94f5c-114">Eltávolítja a `AuthoRule1` névtérből származó WcfRelay engedélyezési szabályát `TestWcfRelay` `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="94f5c-114">Removes the authorization rule `AuthoRule1` of the WcfRelay `TestWcfRelay` from the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="94f5c-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="94f5c-115">Example 3</span></span>
```
PS C:\> Remove-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
```

<span data-ttu-id="94f5c-116">Eltávolítja a `AuthoRule1` névtérből származó HybridConnection engedélyezési szabályát `TestHybridConnection` `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="94f5c-116">Removes the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="94f5c-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="94f5c-117">PARAMETERS</span></span>

### <span data-ttu-id="94f5c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94f5c-118">-DefaultProfile</span></span>
<span data-ttu-id="94f5c-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="94f5c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94f5c-120">-Force</span><span class="sxs-lookup"><span data-stu-id="94f5c-120">-Force</span></span>
<span data-ttu-id="94f5c-121">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="94f5c-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="94f5c-122">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="94f5c-122">-HybridConnection</span></span>
<span data-ttu-id="94f5c-123">HybridConnection neve</span><span class="sxs-lookup"><span data-stu-id="94f5c-123">HybridConnection Name.</span></span>

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

### <span data-ttu-id="94f5c-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="94f5c-124">-Name</span></span>
<span data-ttu-id="94f5c-125">AuthorizationRule neve</span><span class="sxs-lookup"><span data-stu-id="94f5c-125">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="94f5c-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="94f5c-126">-Namespace</span></span>
<span data-ttu-id="94f5c-127">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="94f5c-127">Namespace Name.</span></span>

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

### <span data-ttu-id="94f5c-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="94f5c-128">-PassThru</span></span>
<span data-ttu-id="94f5c-129">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="94f5c-129">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="94f5c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94f5c-130">-ResourceGroupName</span></span>
<span data-ttu-id="94f5c-131">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="94f5c-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="94f5c-132">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="94f5c-132">-WcfRelay</span></span>
<span data-ttu-id="94f5c-133">WcfRelay neve</span><span class="sxs-lookup"><span data-stu-id="94f5c-133">WcfRelay Name.</span></span>

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

### <span data-ttu-id="94f5c-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="94f5c-134">-Confirm</span></span>
<span data-ttu-id="94f5c-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="94f5c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94f5c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94f5c-136">-WhatIf</span></span>
<span data-ttu-id="94f5c-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="94f5c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94f5c-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="94f5c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94f5c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94f5c-139">CommonParameters</span></span>
<span data-ttu-id="94f5c-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="94f5c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94f5c-141">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94f5c-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94f5c-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="94f5c-142">INPUTS</span></span>

### <span data-ttu-id="94f5c-143">System. String</span><span class="sxs-lookup"><span data-stu-id="94f5c-143">System.String</span></span>

## <span data-ttu-id="94f5c-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="94f5c-144">OUTPUTS</span></span>

### <span data-ttu-id="94f5c-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="94f5c-145">System.Boolean</span></span>

## <span data-ttu-id="94f5c-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="94f5c-146">NOTES</span></span>

## <span data-ttu-id="94f5c-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="94f5c-147">RELATED LINKS</span></span>
