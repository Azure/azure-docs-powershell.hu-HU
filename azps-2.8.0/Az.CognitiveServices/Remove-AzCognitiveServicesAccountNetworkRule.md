---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/remove-azcognitiveservicesaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccountNetworkRule.md
ms.openlocfilehash: 6fef24ebef8417be786896547d43f16b54ea0675
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667535"
---
# <span data-ttu-id="a9f25-101">Remove-AzCognitiveServicesAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a9f25-101">Remove-AzCognitiveServicesAccountNetworkRule</span></span>

## <span data-ttu-id="a9f25-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a9f25-102">SYNOPSIS</span></span>
<span data-ttu-id="a9f25-103">IpRules vagy VirtualNetworkRules eltávolítása a kognitív szolgáltatások fiók NetWorkRule tulajdonságáról</span><span class="sxs-lookup"><span data-stu-id="a9f25-103">Remove IpRules or VirtualNetworkRules from the NetWorkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="a9f25-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a9f25-104">SYNTAX</span></span>

### <span data-ttu-id="a9f25-105">NetWorkRuleString (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a9f25-105">NetWorkRuleString (Default)</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a9f25-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="a9f25-106">IpRuleObject</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IpRule <PSIpRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9f25-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="a9f25-107">NetworkRuleObject</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a9f25-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="a9f25-108">IpRuleString</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IpAddressOrRange <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a9f25-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="a9f25-109">DESCRIPTION</span></span>
<span data-ttu-id="a9f25-110">A **Remove-AzCognitiveServicesAccountNetworkRule** parancsmag eltávolítja a IpRules vagy az VirtualNetworkRules-t a kognitív szolgáltatások fiók NetWorkRule tulajdonságból.</span><span class="sxs-lookup"><span data-stu-id="a9f25-110">The **Remove-AzCognitiveServicesAccountNetworkRule** cmdlet removes IpRules or VirtualNetworkRules from the NetWorkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="a9f25-111">Példák</span><span class="sxs-lookup"><span data-stu-id="a9f25-111">EXAMPLES</span></span>

### <span data-ttu-id="a9f25-112">1. példa: több IpRules eltávolítása a IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="a9f25-112">Example 1: Remove several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpAddressOrRange "10.0.0.0/24,28.1.0.0/16"
```

<span data-ttu-id="a9f25-113">Ez a parancs több IpRules távolít el a IPAddressOrRange.</span><span class="sxs-lookup"><span data-stu-id="a9f25-113">This command remove several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="a9f25-114">2. példa: VirtualNetworkRule eltávolítása a VirtualNetworkRule objektum bevitelével JSON-val</span><span class="sxs-lookup"><span data-stu-id="a9f25-114">Example 2: Remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON</span></span>
```
PS C:\>Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -VirtualNetworkRules (@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1"})
```

<span data-ttu-id="a9f25-115">Ez a parancs eltávolítja a VirtualNetworkRule a VirtualNetworkRule objektum bevitelével a JSON-szal.</span><span class="sxs-lookup"><span data-stu-id="a9f25-115">This command remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON.</span></span>

### <span data-ttu-id="a9f25-116">3. példa: az első IpRule eltávolítása a csővezetéktel</span><span class="sxs-lookup"><span data-stu-id="a9f25-116">Example 3: Remove first IpRule with pipeline</span></span>
```
PS C:\>(Get-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount").IpRules[0] | Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount"
```

<span data-ttu-id="a9f25-117">Ez a parancs eltávolítja az első IpRule a futószalagról.</span><span class="sxs-lookup"><span data-stu-id="a9f25-117">This command remove first IpRule with pipeline.</span></span>

### <span data-ttu-id="a9f25-118">4. példa: több VirtualNetworkRules eltávolítása a VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="a9f25-118">Example 4: Remove several VirtualNetworkRules with VirtualNetworkResourceID</span></span>
```
PS C:\>Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -VirtualNetworkResourceId "/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1","/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2"
```

<span data-ttu-id="a9f25-119">Ez a parancs több VirtualNetworkRules távolít el a VirtualNetworkResourceID.</span><span class="sxs-lookup"><span data-stu-id="a9f25-119">This command remove several VirtualNetworkRules with VirtualNetworkResourceID.</span></span> 

## <span data-ttu-id="a9f25-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a9f25-120">PARAMETERS</span></span>

### <span data-ttu-id="a9f25-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9f25-121">-DefaultProfile</span></span>
<span data-ttu-id="a9f25-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a9f25-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9f25-123">-IpAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="a9f25-123">-IpAddressOrRange</span></span>
<span data-ttu-id="a9f25-124">A kognitív szolgáltatások fiók NetworkRule IpRules IpAddressOrRange karakterláncban.</span><span class="sxs-lookup"><span data-stu-id="a9f25-124">Cognitive Services Account NetworkRule IpRules IpAddressOrRange in string.</span></span>

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

### <span data-ttu-id="a9f25-125">-IpRule</span><span class="sxs-lookup"><span data-stu-id="a9f25-125">-IpRule</span></span>
<span data-ttu-id="a9f25-126">A kognitív szolgáltatások fiók NetworkRule IpRules.</span><span class="sxs-lookup"><span data-stu-id="a9f25-126">Cognitive Services Account NetworkRule IpRules.</span></span>

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

### <span data-ttu-id="a9f25-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a9f25-127">-Name</span></span>
<span data-ttu-id="a9f25-128">A kognitív szolgáltatások fiók neve.</span><span class="sxs-lookup"><span data-stu-id="a9f25-128">Cognitive Services Account Name.</span></span>

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

### <span data-ttu-id="a9f25-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9f25-129">-ResourceGroupName</span></span>
<span data-ttu-id="a9f25-130">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="a9f25-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="a9f25-131">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="a9f25-131">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="a9f25-132">A kognitív szolgáltatások fiók NetworkRule VirtualNetworkRules VirtualNetworkResourceId karakterláncban.</span><span class="sxs-lookup"><span data-stu-id="a9f25-132">Cognitive Services Account NetworkRule VirtualNetworkRules VirtualNetworkResourceId in string.</span></span>

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

### <span data-ttu-id="a9f25-133">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a9f25-133">-VirtualNetworkRule</span></span>
<span data-ttu-id="a9f25-134">A kognitív szolgáltatások fiók NetworkRule VirtualNetworkRules.</span><span class="sxs-lookup"><span data-stu-id="a9f25-134">Cognitive Services Account NetworkRule VirtualNetworkRules.</span></span>

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

### <span data-ttu-id="a9f25-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a9f25-135">-Confirm</span></span>
<span data-ttu-id="a9f25-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a9f25-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9f25-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9f25-137">-WhatIf</span></span>
<span data-ttu-id="a9f25-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a9f25-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9f25-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a9f25-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9f25-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9f25-140">CommonParameters</span></span>
<span data-ttu-id="a9f25-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a9f25-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9f25-142">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a9f25-142">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9f25-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a9f25-143">INPUTS</span></span>

### <span data-ttu-id="a9f25-144">System. String</span><span class="sxs-lookup"><span data-stu-id="a9f25-144">System.String</span></span>

### <span data-ttu-id="a9f25-145">Microsoft. Azure. Command. Management. CognitiveServices. models. PSIpRule []</span><span class="sxs-lookup"><span data-stu-id="a9f25-145">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span></span>

### <span data-ttu-id="a9f25-146">Microsoft. Azure. Command. Management. CognitiveServices. models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="a9f25-146">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="a9f25-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a9f25-147">OUTPUTS</span></span>

### <span data-ttu-id="a9f25-148">Microsoft. Azure. Command. Management. CognitiveServices. models. PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a9f25-148">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="a9f25-149">Microsoft. Azure. Command. Management. CognitiveServices. models. PSIpRule</span><span class="sxs-lookup"><span data-stu-id="a9f25-149">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule</span></span>

## <span data-ttu-id="a9f25-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a9f25-150">NOTES</span></span>

## <span data-ttu-id="a9f25-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a9f25-151">RELATED LINKS</span></span>
