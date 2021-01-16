---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/remove-azcognitiveservicesaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccountNetworkRule.md
ms.openlocfilehash: 2faf890cda0c87d15704a14f9c4ae12c5b3d81c2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326853"
---
# <span data-ttu-id="e4149-101">Remove-AzCognitiveServicesAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e4149-101">Remove-AzCognitiveServicesAccountNetworkRule</span></span>

## <span data-ttu-id="e4149-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4149-102">SYNOPSIS</span></span>
<span data-ttu-id="e4149-103">IpRules vagy VirtualNetworkRules eltávolítása a Kognitív Szolgáltatások-fiók NetWorkRule tulajdonságában</span><span class="sxs-lookup"><span data-stu-id="e4149-103">Remove IpRules or VirtualNetworkRules from the NetWorkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="e4149-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e4149-104">SYNTAX</span></span>

### <span data-ttu-id="e4149-105">NetWorkRuleString (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e4149-105">NetWorkRuleString (Default)</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e4149-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="e4149-106">IpRuleObject</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IpRule <PSIpRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4149-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="e4149-107">NetworkRuleObject</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e4149-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="e4149-108">IpRuleString</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IpAddressOrRange <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e4149-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e4149-109">DESCRIPTION</span></span>
<span data-ttu-id="e4149-110">A **Remove-AzCognitiveServicesAccountNetworkRule** parancsmag eltávolítja az IpRules vagy a VirtualNetworkRules tartományt a Kognitív Szolgáltatások-fiók NetWorkRule tulajdonságában.</span><span class="sxs-lookup"><span data-stu-id="e4149-110">The **Remove-AzCognitiveServicesAccountNetworkRule** cmdlet removes IpRules or VirtualNetworkRules from the NetWorkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="e4149-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e4149-111">EXAMPLES</span></span>

### <span data-ttu-id="e4149-112">1. példa: Több IpRules eltávolítása IPAddressOrRange-val</span><span class="sxs-lookup"><span data-stu-id="e4149-112">Example 1: Remove several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpAddressOrRange "10.0.0.0/24,28.1.0.0/16"
```

<span data-ttu-id="e4149-113">Ez a parancs eltávolít több IPRules ipAddressOrRange-t.</span><span class="sxs-lookup"><span data-stu-id="e4149-113">This command remove several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="e4149-114">2. példa: VirtualNetworkRule eltávolítása VirtualNetworkRule objektumbemenettel JSON-nal</span><span class="sxs-lookup"><span data-stu-id="e4149-114">Example 2: Remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON</span></span>
```
PS C:\>Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -VirtualNetworkRules (@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1"})
```

<span data-ttu-id="e4149-115">Ez a parancs eltávolítja a VirtualNetworkRule-et VirtualNetworkRule objektum-bevitelsel JSON-nal.</span><span class="sxs-lookup"><span data-stu-id="e4149-115">This command remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON.</span></span>

### <span data-ttu-id="e4149-116">3. példa: Az első IpRule eltávolítása a prognózissal</span><span class="sxs-lookup"><span data-stu-id="e4149-116">Example 3: Remove first IpRule with pipeline</span></span>
```
PS C:\>(Get-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount").IpRules[0] | Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount"
```

<span data-ttu-id="e4149-117">Ez a parancs eltávolítja a prognózissal együtt az első IpRule-et.</span><span class="sxs-lookup"><span data-stu-id="e4149-117">This command remove first IpRule with pipeline.</span></span>

### <span data-ttu-id="e4149-118">4. példa: Több VirtualNetworkRules eltávolítása VirtualNetworkResourceID értékekkel</span><span class="sxs-lookup"><span data-stu-id="e4149-118">Example 4: Remove several VirtualNetworkRules with VirtualNetworkResourceID</span></span>
```
PS C:\>Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -VirtualNetworkResourceId "/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1","/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2"
```

<span data-ttu-id="e4149-119">Ez a parancs eltávolít több VirtualNetworkRulest VirtualNetworkResourceID értékekkel.</span><span class="sxs-lookup"><span data-stu-id="e4149-119">This command remove several VirtualNetworkRules with VirtualNetworkResourceID.</span></span> 

## <span data-ttu-id="e4149-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e4149-120">PARAMETERS</span></span>

### <span data-ttu-id="e4149-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4149-121">-DefaultProfile</span></span>
<span data-ttu-id="e4149-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e4149-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4149-123">-IpAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="e4149-123">-IpAddressOrRange</span></span>
<span data-ttu-id="e4149-124">Cognitive Services Account NetworkRule IpRules IpAddressOrRange in string.</span><span class="sxs-lookup"><span data-stu-id="e4149-124">Cognitive Services Account NetworkRule IpRules IpAddressOrRange in string.</span></span>

```yaml
Type: System.String[]
Parameter Sets: IpRuleString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4149-125">-IpRule</span><span class="sxs-lookup"><span data-stu-id="e4149-125">-IpRule</span></span>
<span data-ttu-id="e4149-126">Cognitive Services Account NetworkRule IpRules.</span><span class="sxs-lookup"><span data-stu-id="e4149-126">Cognitive Services Account NetworkRule IpRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]
Parameter Sets: IpRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4149-127">-Name</span><span class="sxs-lookup"><span data-stu-id="e4149-127">-Name</span></span>
<span data-ttu-id="e4149-128">Kognitív szolgáltatások fiókneve.</span><span class="sxs-lookup"><span data-stu-id="e4149-128">Cognitive Services Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4149-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4149-129">-ResourceGroupName</span></span>
<span data-ttu-id="e4149-130">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e4149-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="e4149-131">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="e4149-131">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="e4149-132">Cognitive Services Account NetworkRule VirtualNetworkRules VirtualNetworkResourceId in string.</span><span class="sxs-lookup"><span data-stu-id="e4149-132">Cognitive Services Account NetworkRule VirtualNetworkRules VirtualNetworkResourceId in string.</span></span>

```yaml
Type: System.String[]
Parameter Sets: NetWorkRuleString
Aliases: SubnetId, VirtualNetworkId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4149-133">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e4149-133">-VirtualNetworkRule</span></span>
<span data-ttu-id="e4149-134">Cognitive Services Account NetworkRule VirtualNetworkRules.</span><span class="sxs-lookup"><span data-stu-id="e4149-134">Cognitive Services Account NetworkRule VirtualNetworkRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]
Parameter Sets: NetworkRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4149-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e4149-135">-Confirm</span></span>
<span data-ttu-id="e4149-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e4149-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4149-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4149-137">-WhatIf</span></span>
<span data-ttu-id="e4149-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e4149-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4149-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e4149-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4149-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4149-140">CommonParameters</span></span>
<span data-ttu-id="e4149-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4149-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4149-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e4149-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4149-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e4149-143">INPUTS</span></span>

### <span data-ttu-id="e4149-144">System.String</span><span class="sxs-lookup"><span data-stu-id="e4149-144">System.String</span></span>

### <span data-ttu-id="e4149-145">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span><span class="sxs-lookup"><span data-stu-id="e4149-145">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span></span>

### <span data-ttu-id="e4149-146">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span><span class="sxs-lookup"><span data-stu-id="e4149-146">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="e4149-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e4149-147">OUTPUTS</span></span>

### <span data-ttu-id="e4149-148">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e4149-148">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="e4149-149">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule</span><span class="sxs-lookup"><span data-stu-id="e4149-149">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule</span></span>

## <span data-ttu-id="e4149-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e4149-150">NOTES</span></span>

## <span data-ttu-id="e4149-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e4149-151">RELATED LINKS</span></span>
