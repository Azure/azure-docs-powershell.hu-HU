---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/powershell/module/az.cognitiveservices/add-azcognitiveservicesaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Add-AzCognitiveServicesAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Add-AzCognitiveServicesAccountNetworkRule.md
ms.openlocfilehash: fe2f405e07bc20437b9c0b47b8e551039b90b500
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925138"
---
# <span data-ttu-id="0ac51-101">Add-AzCognitiveServicesAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="0ac51-101">Add-AzCognitiveServicesAccountNetworkRule</span></span>

## <span data-ttu-id="0ac51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ac51-102">SYNOPSIS</span></span>
<span data-ttu-id="0ac51-103">IpRules vagy VirtualNetworkRules hozzáadása a Kognitív szolgáltatások fiók NetworkRule tulajdonságához</span><span class="sxs-lookup"><span data-stu-id="0ac51-103">Add IpRules or VirtualNetworkRules to the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="0ac51-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0ac51-104">SYNTAX</span></span>

### <span data-ttu-id="0ac51-105">NetWorkRuleString (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0ac51-105">NetWorkRuleString (Default)</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0ac51-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="0ac51-106">IpRuleObject</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IpRule <PSIpRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ac51-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="0ac51-107">NetworkRuleObject</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0ac51-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="0ac51-108">IpRuleString</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IpAddressOrRange <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0ac51-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0ac51-109">DESCRIPTION</span></span>
<span data-ttu-id="0ac51-110">The **Add-AzCognitiveServicesAccountNetworkRule cmdlet** adds IpRules or VirtualNetworkRules to the NetworkRule property of a Cognitive Services account</span><span class="sxs-lookup"><span data-stu-id="0ac51-110">The **Add-AzCognitiveServicesAccountNetworkRule** cmdlet adds IpRules or VirtualNetworkRules to the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="0ac51-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0ac51-111">EXAMPLES</span></span>

### <span data-ttu-id="0ac51-112">1. példa: Több IpRules hozzáadása az IpAddressOrRange-val</span><span class="sxs-lookup"><span data-stu-id="0ac51-112">Example 1: Add several IpRules with IpAddressOrRange</span></span>
```
PS C:\>Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpAddressOrRange "200.0.0.0/24","28.2.0.0/16"
```

<span data-ttu-id="0ac51-113">Ez a parancs több IpRules-t is hozzáad az IpAddressOrRange protokollal.</span><span class="sxs-lookup"><span data-stu-id="0ac51-113">This command add several IpRules with IpAddressOrRange.</span></span>

### <span data-ttu-id="0ac51-114">2. példa: VirtualNetworkRule hozzáadása VirtualNetworkResourceID-val</span><span class="sxs-lookup"><span data-stu-id="0ac51-114">Example 2: Add a VirtualNetworkRule with VirtualNetworkResourceID</span></span>
```
PS C:\>$subnet = Get-AzVirtualNetwork -ResourceGroupName "myResourceGroup" -Name "myvirtualnetwork" | Get-AzVirtualNetworkSubnetConfig
PS C:\>Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -VirtualNetworkResourceId $subnet[0].Id
```

<span data-ttu-id="0ac51-115">Ez a parancs virtualnetworkRule-t ad hozzá VirtualNetworkResourceID-val.</span><span class="sxs-lookup"><span data-stu-id="0ac51-115">This command add a VirtualNetworkRule with VirtualNetworkResourceID.</span></span>

### <span data-ttu-id="0ac51-116">3. példa: VirtualNetworkRules hozzáadása virtualnetworkrule-objektumokkal egy másik fiókból</span><span class="sxs-lookup"><span data-stu-id="0ac51-116">Example 3: Add VirtualNetworkRules with VirtualNetworkRule Objects from another account</span></span>
```
PS C:\> $networkrule = Get-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount1"
PS C:\> Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount2" -VirtualNetworkRule $networkrule.VirtualNetworkRules
```

<span data-ttu-id="0ac51-117">Ez a parancs hozzáadja a VirtualNetworkRules-t egy másik fiók VirtualNetworkRule-objektumaihoz.</span><span class="sxs-lookup"><span data-stu-id="0ac51-117">This command add VirtualNetworkRules with VirtualNetworkRule Objects from another account.</span></span>

### <span data-ttu-id="0ac51-118">4. példa: Több IpRule hozzáadása IpRule-objektumokkal, bevitel JSON-nal</span><span class="sxs-lookup"><span data-stu-id="0ac51-118">Example 4: Add several IpRule with IpRule objects, input with JSON</span></span>
```
PS C:\>Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpRule (@{IpAddressOrRange="200.0.0.0/24"},@{IpAddressOrRange="28.2.0.0/16"})
```

<span data-ttu-id="0ac51-119">Ez a parancs több IpRule-et ad hozzá IpRule-objektumokkal, és JSON-t ad meg.</span><span class="sxs-lookup"><span data-stu-id="0ac51-119">This command add several IpRule with IpRule objects, input with JSON.</span></span>

## <span data-ttu-id="0ac51-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0ac51-120">PARAMETERS</span></span>

### <span data-ttu-id="0ac51-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ac51-121">-DefaultProfile</span></span>
<span data-ttu-id="0ac51-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0ac51-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ac51-123">-IpAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="0ac51-123">-IpAddressOrRange</span></span>
<span data-ttu-id="0ac51-124">Cognitive Services Account NetworkRule IpRules IpAddressOrRange in string.</span><span class="sxs-lookup"><span data-stu-id="0ac51-124">Cognitive Services Account NetworkRule IpRules IpAddressOrRange in string.</span></span>

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

### <span data-ttu-id="0ac51-125">-IpRule</span><span class="sxs-lookup"><span data-stu-id="0ac51-125">-IpRule</span></span>
<span data-ttu-id="0ac51-126">Cognitive Services Account NetworkRule IpRules.</span><span class="sxs-lookup"><span data-stu-id="0ac51-126">Cognitive Services Account NetworkRule IpRules.</span></span>

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

### <span data-ttu-id="0ac51-127">-Name</span><span class="sxs-lookup"><span data-stu-id="0ac51-127">-Name</span></span>
<span data-ttu-id="0ac51-128">Kognitív szolgáltatások fiókneve.</span><span class="sxs-lookup"><span data-stu-id="0ac51-128">Cognitive Services Account Name.</span></span>

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

### <span data-ttu-id="0ac51-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ac51-129">-ResourceGroupName</span></span>
<span data-ttu-id="0ac51-130">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0ac51-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="0ac51-131">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="0ac51-131">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="0ac51-132">Cognitive Services Account NetworkRule VirtualNetworkRules VirtualNetworkResourceId in string.</span><span class="sxs-lookup"><span data-stu-id="0ac51-132">Cognitive Services Account NetworkRule VirtualNetworkRules VirtualNetworkResourceId in string.</span></span>

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

### <span data-ttu-id="0ac51-133">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="0ac51-133">-VirtualNetworkRule</span></span>
<span data-ttu-id="0ac51-134">Cognitive Services Account NetworkRule VirtualNetworkRules.</span><span class="sxs-lookup"><span data-stu-id="0ac51-134">Cognitive Services Account NetworkRule VirtualNetworkRules.</span></span>

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

### <span data-ttu-id="0ac51-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0ac51-135">-Confirm</span></span>
<span data-ttu-id="0ac51-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0ac51-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ac51-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ac51-137">-WhatIf</span></span>
<span data-ttu-id="0ac51-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0ac51-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ac51-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0ac51-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ac51-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ac51-140">CommonParameters</span></span>
<span data-ttu-id="0ac51-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ac51-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ac51-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0ac51-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ac51-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0ac51-143">INPUTS</span></span>

### <span data-ttu-id="0ac51-144">System.String</span><span class="sxs-lookup"><span data-stu-id="0ac51-144">System.String</span></span>

### <span data-ttu-id="0ac51-145">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span><span class="sxs-lookup"><span data-stu-id="0ac51-145">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span></span>

### <span data-ttu-id="0ac51-146">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span><span class="sxs-lookup"><span data-stu-id="0ac51-146">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="0ac51-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ac51-147">OUTPUTS</span></span>

### <span data-ttu-id="0ac51-148">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="0ac51-148">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="0ac51-149">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule</span><span class="sxs-lookup"><span data-stu-id="0ac51-149">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule</span></span>

## <span data-ttu-id="0ac51-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0ac51-150">NOTES</span></span>

## <span data-ttu-id="0ac51-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0ac51-151">RELATED LINKS</span></span>
