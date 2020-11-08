---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/add-azcognitiveservicesaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Add-AzCognitiveServicesAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Add-AzCognitiveServicesAccountNetworkRule.md
ms.openlocfilehash: 039a3e4bf676f29d55f48e7e0883f5818e7367b7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194913"
---
# <span data-ttu-id="7209e-101">Add-AzCognitiveServicesAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="7209e-101">Add-AzCognitiveServicesAccountNetworkRule</span></span>

## <span data-ttu-id="7209e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7209e-102">SYNOPSIS</span></span>
<span data-ttu-id="7209e-103">IpRules vagy VirtualNetworkRules hozzáadása a kognitív szolgáltatások fiók NetworkRule tulajdonságához</span><span class="sxs-lookup"><span data-stu-id="7209e-103">Add IpRules or VirtualNetworkRules to the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="7209e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7209e-104">SYNTAX</span></span>

### <span data-ttu-id="7209e-105">NetWorkRuleString (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7209e-105">NetWorkRuleString (Default)</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7209e-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="7209e-106">IpRuleObject</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IpRule <PSIpRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7209e-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="7209e-107">NetworkRuleObject</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7209e-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="7209e-108">IpRuleString</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IpAddressOrRange <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7209e-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="7209e-109">DESCRIPTION</span></span>
<span data-ttu-id="7209e-110">A **Add-AzCognitiveServicesAccountNetworkRule** parancsmag IpRules vagy VirtualNetworkRules ad az NetworkRule tulajdonságának a kognitív Services-fiókban.</span><span class="sxs-lookup"><span data-stu-id="7209e-110">The **Add-AzCognitiveServicesAccountNetworkRule** cmdlet adds IpRules or VirtualNetworkRules to the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="7209e-111">Példák</span><span class="sxs-lookup"><span data-stu-id="7209e-111">EXAMPLES</span></span>

### <span data-ttu-id="7209e-112">1. példa: több IpRules hozzáadása a IpAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="7209e-112">Example 1: Add several IpRules with IpAddressOrRange</span></span>
```
PS C:\>Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpAddressOrRange "200.0.0.0/24","28.2.0.0/16"
```

<span data-ttu-id="7209e-113">Ez a parancs több IpRules adhat hozzá a IpAddressOrRange-hoz.</span><span class="sxs-lookup"><span data-stu-id="7209e-113">This command add several IpRules with IpAddressOrRange.</span></span>

### <span data-ttu-id="7209e-114">2. példa: VirtualNetworkRule hozzáadása a VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="7209e-114">Example 2: Add a VirtualNetworkRule with VirtualNetworkResourceID</span></span>
```
PS C:\>$subnet = Get-AzVirtualNetwork -ResourceGroupName "myResourceGroup" -Name "myvirtualnetwork" | Get-AzVirtualNetworkSubnetConfig
PS C:\>Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -VirtualNetworkResourceId $subnet[0].Id
```

<span data-ttu-id="7209e-115">Ezzel a paranccsal VirtualNetworkRule adhat hozzá a VirtualNetworkResourceID-hoz.</span><span class="sxs-lookup"><span data-stu-id="7209e-115">This command add a VirtualNetworkRule with VirtualNetworkResourceID.</span></span>

### <span data-ttu-id="7209e-116">3. példa: VirtualNetworkRules felvétele más fiókból származó VirtualNetworkRule-objektumokkal</span><span class="sxs-lookup"><span data-stu-id="7209e-116">Example 3: Add VirtualNetworkRules with VirtualNetworkRule Objects from another account</span></span>
```
PS C:\> $networkrule = Get-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount1"
PS C:\> Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount2" -VirtualNetworkRule $networkrule.VirtualNetworkRules
```

<span data-ttu-id="7209e-117">Ezzel a paranccsal VirtualNetworkRules adhat hozzá a VirtualNetworkRule-objektumokból egy másik fiókból.</span><span class="sxs-lookup"><span data-stu-id="7209e-117">This command add VirtualNetworkRules with VirtualNetworkRule Objects from another account.</span></span>

### <span data-ttu-id="7209e-118">4. példa: több IpRule hozzáadása IpRule-objektumokhoz, JSON-bevitel</span><span class="sxs-lookup"><span data-stu-id="7209e-118">Example 4: Add several IpRule with IpRule objects, input with JSON</span></span>
```
PS C:\>Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpRule (@{IpAddressOrRange="200.0.0.0/24"},@{IpAddressOrRange="28.2.0.0/16"})
```

<span data-ttu-id="7209e-119">Ez a parancs több IpRule adhat hozzá IpRule objektumokkal, a JSON-szal.</span><span class="sxs-lookup"><span data-stu-id="7209e-119">This command add several IpRule with IpRule objects, input with JSON.</span></span>

## <span data-ttu-id="7209e-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7209e-120">PARAMETERS</span></span>

### <span data-ttu-id="7209e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7209e-121">-DefaultProfile</span></span>
<span data-ttu-id="7209e-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7209e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7209e-123">-IpAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="7209e-123">-IpAddressOrRange</span></span>
<span data-ttu-id="7209e-124">A kognitív szolgáltatások fiók NetworkRule IpRules IpAddressOrRange karakterláncban.</span><span class="sxs-lookup"><span data-stu-id="7209e-124">Cognitive Services Account NetworkRule IpRules IpAddressOrRange in string.</span></span>

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

### <span data-ttu-id="7209e-125">-IpRule</span><span class="sxs-lookup"><span data-stu-id="7209e-125">-IpRule</span></span>
<span data-ttu-id="7209e-126">A kognitív szolgáltatások fiók NetworkRule IpRules.</span><span class="sxs-lookup"><span data-stu-id="7209e-126">Cognitive Services Account NetworkRule IpRules.</span></span>

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

### <span data-ttu-id="7209e-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7209e-127">-Name</span></span>
<span data-ttu-id="7209e-128">A kognitív szolgáltatások fiók neve.</span><span class="sxs-lookup"><span data-stu-id="7209e-128">Cognitive Services Account Name.</span></span>

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

### <span data-ttu-id="7209e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7209e-129">-ResourceGroupName</span></span>
<span data-ttu-id="7209e-130">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="7209e-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="7209e-131">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="7209e-131">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="7209e-132">A kognitív szolgáltatások fiók NetworkRule VirtualNetworkRules VirtualNetworkResourceId karakterláncban.</span><span class="sxs-lookup"><span data-stu-id="7209e-132">Cognitive Services Account NetworkRule VirtualNetworkRules VirtualNetworkResourceId in string.</span></span>

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

### <span data-ttu-id="7209e-133">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="7209e-133">-VirtualNetworkRule</span></span>
<span data-ttu-id="7209e-134">A kognitív szolgáltatások fiók NetworkRule VirtualNetworkRules.</span><span class="sxs-lookup"><span data-stu-id="7209e-134">Cognitive Services Account NetworkRule VirtualNetworkRules.</span></span>

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

### <span data-ttu-id="7209e-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7209e-135">-Confirm</span></span>
<span data-ttu-id="7209e-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7209e-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7209e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7209e-137">-WhatIf</span></span>
<span data-ttu-id="7209e-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7209e-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7209e-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7209e-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7209e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7209e-140">CommonParameters</span></span>
<span data-ttu-id="7209e-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7209e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7209e-142">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7209e-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7209e-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7209e-143">INPUTS</span></span>

### <span data-ttu-id="7209e-144">System. String</span><span class="sxs-lookup"><span data-stu-id="7209e-144">System.String</span></span>

### <span data-ttu-id="7209e-145">Microsoft. Azure. Command. Management. CognitiveServices. models. PSIpRule []</span><span class="sxs-lookup"><span data-stu-id="7209e-145">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span></span>

### <span data-ttu-id="7209e-146">Microsoft. Azure. Command. Management. CognitiveServices. models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="7209e-146">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="7209e-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7209e-147">OUTPUTS</span></span>

### <span data-ttu-id="7209e-148">Microsoft. Azure. Command. Management. CognitiveServices. models. PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="7209e-148">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="7209e-149">Microsoft. Azure. Command. Management. CognitiveServices. models. PSIpRule</span><span class="sxs-lookup"><span data-stu-id="7209e-149">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule</span></span>

## <span data-ttu-id="7209e-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7209e-150">NOTES</span></span>

## <span data-ttu-id="7209e-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7209e-151">RELATED LINKS</span></span>