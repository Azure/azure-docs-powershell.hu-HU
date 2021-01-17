---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubIPRule.md
ms.openlocfilehash: 00213d4829d4b389f19a01ad9748517608657136
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98353106"
---
# <span data-ttu-id="adbd0-101">Remove-AzEventHubIPRule</span><span class="sxs-lookup"><span data-stu-id="adbd0-101">Remove-AzEventHubIPRule</span></span>

## <span data-ttu-id="adbd0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="adbd0-102">SYNOPSIS</span></span>
<span data-ttu-id="adbd0-103">Egyetlen IP-szabály eltávolítása a megadott Namespace NetworkRuleSet szolgáltatásba</span><span class="sxs-lookup"><span data-stu-id="adbd0-103">Remove a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="adbd0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="adbd0-104">SYNTAX</span></span>

### <span data-ttu-id="adbd0-105">IPRulePropertiesParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="adbd0-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Remove-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="adbd0-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="adbd0-106">IPRuleInputObjectParameterSet</span></span>
```
Remove-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="adbd0-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="adbd0-107">DESCRIPTION</span></span>
<span data-ttu-id="adbd0-108">Egyetlen IP-szabály eltávolítása a megadott Namespace NetworkRuleSet szolgáltatásba</span><span class="sxs-lookup"><span data-stu-id="adbd0-108">Remove a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="adbd0-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="adbd0-109">EXAMPLES</span></span>

### <span data-ttu-id="adbd0-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="adbd0-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubIPRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -IpMask "11.22.33.44"
```

<span data-ttu-id="adbd0-111">A megadott névtér NetworkRuleSet-ének IpMask-ének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="adbd0-111">Removes IpMask of the NetworkRuleSet of the given namespace</span></span>

## <span data-ttu-id="adbd0-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="adbd0-112">PARAMETERS</span></span>

### <span data-ttu-id="adbd0-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="adbd0-113">-AsJob</span></span>
<span data-ttu-id="adbd0-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="adbd0-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="adbd0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adbd0-115">-DefaultProfile</span></span>
<span data-ttu-id="adbd0-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="adbd0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="adbd0-117">-IpMask</span><span class="sxs-lookup"><span data-stu-id="adbd0-117">-IpMask</span></span>
<span data-ttu-id="adbd0-118">Alhálózati erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="adbd0-118">Subnet Resource ID</span></span>

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

### <span data-ttu-id="adbd0-119">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="adbd0-119">-IpRuleObject</span></span>
<span data-ttu-id="adbd0-120">IPRule Configuration Object</span><span class="sxs-lookup"><span data-stu-id="adbd0-120">IPRule Configuration Object</span></span>

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

### <span data-ttu-id="adbd0-121">-Name</span><span class="sxs-lookup"><span data-stu-id="adbd0-121">-Name</span></span>
<span data-ttu-id="adbd0-122">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="adbd0-122">Namespace Name</span></span>

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

### <span data-ttu-id="adbd0-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="adbd0-123">-PassThru</span></span>
<span data-ttu-id="adbd0-124">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="adbd0-124">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="adbd0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adbd0-125">-ResourceGroupName</span></span>
<span data-ttu-id="adbd0-126">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="adbd0-126">Resource Group Name</span></span>

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

### <span data-ttu-id="adbd0-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="adbd0-127">-Confirm</span></span>
<span data-ttu-id="adbd0-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="adbd0-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="adbd0-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="adbd0-129">-WhatIf</span></span>
<span data-ttu-id="adbd0-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="adbd0-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="adbd0-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="adbd0-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="adbd0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adbd0-132">CommonParameters</span></span>
<span data-ttu-id="adbd0-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adbd0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="adbd0-134">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="adbd0-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adbd0-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="adbd0-135">INPUTS</span></span>

### <span data-ttu-id="adbd0-136">System.String</span><span class="sxs-lookup"><span data-stu-id="adbd0-136">System.String</span></span>

### <span data-ttu-id="adbd0-137">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="adbd0-137">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="adbd0-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="adbd0-138">OUTPUTS</span></span>

### <span data-ttu-id="adbd0-139">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="adbd0-139">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="adbd0-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="adbd0-140">NOTES</span></span>

## <span data-ttu-id="adbd0-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="adbd0-141">RELATED LINKS</span></span>