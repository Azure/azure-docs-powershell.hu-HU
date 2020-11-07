---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubIPRule.md
ms.openlocfilehash: 00213d4829d4b389f19a01ad9748517608657136
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845610"
---
# <span data-ttu-id="953d4-101">Remove-AzEventHubIPRule</span><span class="sxs-lookup"><span data-stu-id="953d4-101">Remove-AzEventHubIPRule</span></span>

## <span data-ttu-id="953d4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="953d4-102">SYNOPSIS</span></span>
<span data-ttu-id="953d4-103">Egyetlen IP-szabály eltávolítása a megadott névtér NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="953d4-103">Remove a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="953d4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="953d4-104">SYNTAX</span></span>

### <span data-ttu-id="953d4-105">IPRulePropertiesParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="953d4-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Remove-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="953d4-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="953d4-106">IPRuleInputObjectParameterSet</span></span>
```
Remove-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="953d4-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="953d4-107">DESCRIPTION</span></span>
<span data-ttu-id="953d4-108">Egyetlen IP-szabály eltávolítása a megadott névtér NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="953d4-108">Remove a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="953d4-109">Példák</span><span class="sxs-lookup"><span data-stu-id="953d4-109">EXAMPLES</span></span>

### <span data-ttu-id="953d4-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="953d4-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubIPRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -IpMask "11.22.33.44"
```

<span data-ttu-id="953d4-111">A megadott névtér NetworkRuleSet IpMask eltávolítása</span><span class="sxs-lookup"><span data-stu-id="953d4-111">Removes IpMask of the NetworkRuleSet of the given namespace</span></span>

## <span data-ttu-id="953d4-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="953d4-112">PARAMETERS</span></span>

### <span data-ttu-id="953d4-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="953d4-113">-AsJob</span></span>
<span data-ttu-id="953d4-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="953d4-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="953d4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="953d4-115">-DefaultProfile</span></span>
<span data-ttu-id="953d4-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="953d4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="953d4-117">-IpMask</span><span class="sxs-lookup"><span data-stu-id="953d4-117">-IpMask</span></span>
<span data-ttu-id="953d4-118">Alhálózati erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="953d4-118">Subnet Resource ID</span></span>

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

### <span data-ttu-id="953d4-119">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="953d4-119">-IpRuleObject</span></span>
<span data-ttu-id="953d4-120">IPRule konfigurációs objektum</span><span class="sxs-lookup"><span data-stu-id="953d4-120">IPRule Configuration Object</span></span>

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

### <span data-ttu-id="953d4-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="953d4-121">-Name</span></span>
<span data-ttu-id="953d4-122">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="953d4-122">Namespace Name</span></span>

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

### <span data-ttu-id="953d4-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="953d4-123">-PassThru</span></span>
<span data-ttu-id="953d4-124">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="953d4-124">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="953d4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="953d4-125">-ResourceGroupName</span></span>
<span data-ttu-id="953d4-126">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="953d4-126">Resource Group Name</span></span>

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

### <span data-ttu-id="953d4-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="953d4-127">-Confirm</span></span>
<span data-ttu-id="953d4-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="953d4-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="953d4-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="953d4-129">-WhatIf</span></span>
<span data-ttu-id="953d4-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="953d4-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="953d4-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="953d4-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="953d4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="953d4-132">CommonParameters</span></span>
<span data-ttu-id="953d4-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="953d4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="953d4-134">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="953d4-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="953d4-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="953d4-135">INPUTS</span></span>

### <span data-ttu-id="953d4-136">System. String</span><span class="sxs-lookup"><span data-stu-id="953d4-136">System.String</span></span>

### <span data-ttu-id="953d4-137">Microsoft. Azure. Command. EventHub. models. PSNWRuleSetIpRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="953d4-137">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="953d4-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="953d4-138">OUTPUTS</span></span>

### <span data-ttu-id="953d4-139">Microsoft. Azure. Command. EventHub. models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="953d4-139">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="953d4-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="953d4-140">NOTES</span></span>

## <span data-ttu-id="953d4-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="953d4-141">RELATED LINKS</span></span>