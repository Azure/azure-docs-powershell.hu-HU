---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/remove-azeventhubiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubIPRule.md
ms.openlocfilehash: c8a42bd69cc253d66fede2339f4080558e2f07cb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935770"
---
# <span data-ttu-id="65849-101">Remove-AzEventHubIPRule</span><span class="sxs-lookup"><span data-stu-id="65849-101">Remove-AzEventHubIPRule</span></span>

## <span data-ttu-id="65849-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65849-102">SYNOPSIS</span></span>
<span data-ttu-id="65849-103">Egyetlen IP-szabály eltávolítása a megadott Namespace NetworkRuleSet szolgáltatásba</span><span class="sxs-lookup"><span data-stu-id="65849-103">Remove a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="65849-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="65849-104">SYNTAX</span></span>

### <span data-ttu-id="65849-105">IPRulePropertiesParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="65849-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Remove-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65849-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="65849-106">IPRuleInputObjectParameterSet</span></span>
```
Remove-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="65849-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="65849-107">DESCRIPTION</span></span>
<span data-ttu-id="65849-108">Egyetlen IP-szabály eltávolítása a megadott Namespace NetworkRuleSet szolgáltatásba</span><span class="sxs-lookup"><span data-stu-id="65849-108">Remove a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="65849-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="65849-109">EXAMPLES</span></span>

### <span data-ttu-id="65849-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="65849-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubIPRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -IpMask "11.22.33.44"
```

<span data-ttu-id="65849-111">A megadott névtér NetworkRuleSet-ének IpMask-ének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="65849-111">Removes IpMask of the NetworkRuleSet of the given namespace</span></span>

## <span data-ttu-id="65849-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="65849-112">PARAMETERS</span></span>

### <span data-ttu-id="65849-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="65849-113">-AsJob</span></span>
<span data-ttu-id="65849-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="65849-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="65849-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65849-115">-DefaultProfile</span></span>
<span data-ttu-id="65849-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="65849-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65849-117">-IpMask</span><span class="sxs-lookup"><span data-stu-id="65849-117">-IpMask</span></span>
<span data-ttu-id="65849-118">Alhálózati erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="65849-118">Subnet Resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: IPRulePropertiesParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65849-119">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="65849-119">-IpRuleObject</span></span>
<span data-ttu-id="65849-120">IPRule Configuration Object</span><span class="sxs-lookup"><span data-stu-id="65849-120">IPRule Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes
Parameter Sets: IPRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65849-121">-Name</span><span class="sxs-lookup"><span data-stu-id="65849-121">-Name</span></span>
<span data-ttu-id="65849-122">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="65849-122">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65849-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="65849-123">-PassThru</span></span>
<span data-ttu-id="65849-124">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="65849-124">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="65849-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65849-125">-ResourceGroupName</span></span>
<span data-ttu-id="65849-126">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="65849-126">Resource Group Name</span></span>

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

### <span data-ttu-id="65849-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="65849-127">-Confirm</span></span>
<span data-ttu-id="65849-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="65849-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65849-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65849-129">-WhatIf</span></span>
<span data-ttu-id="65849-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="65849-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65849-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="65849-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65849-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65849-132">CommonParameters</span></span>
<span data-ttu-id="65849-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65849-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="65849-134">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65849-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65849-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="65849-135">INPUTS</span></span>

### <span data-ttu-id="65849-136">System.String</span><span class="sxs-lookup"><span data-stu-id="65849-136">System.String</span></span>

### <span data-ttu-id="65849-137">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="65849-137">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="65849-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="65849-138">OUTPUTS</span></span>

### <span data-ttu-id="65849-139">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="65849-139">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="65849-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="65849-140">NOTES</span></span>

## <span data-ttu-id="65849-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="65849-141">RELATED LINKS</span></span>