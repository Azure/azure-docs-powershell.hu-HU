---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/set-azcontainerregistrynetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Set-AzContainerRegistryNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Set-AzContainerRegistryNetworkRuleSet.md
ms.openlocfilehash: 4a2292b0b573a5357466f3b240ba3b6df7cf0a1e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360498"
---
# <span data-ttu-id="da349-101">Set-AzContainerRegistryNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="da349-101">Set-AzContainerRegistryNetworkRuleSet</span></span>

## <span data-ttu-id="da349-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da349-102">SYNOPSIS</span></span>
<span data-ttu-id="da349-103">Hozzon létre vagy frissítsen egy hálózati szabálykészletet.</span><span class="sxs-lookup"><span data-stu-id="da349-103">Create or update a network rule set.</span></span> <span data-ttu-id="da349-104">A szabálykészlet csak a "Prémium" beállításjegyzékre alkalmazható.</span><span class="sxs-lookup"><span data-stu-id="da349-104">Rule set can only be applied to "Premium" registry.</span></span>

## <span data-ttu-id="da349-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="da349-105">SYNTAX</span></span>

### <span data-ttu-id="da349-106">AddAddNetworkRuleWithoutInputObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="da349-106">AddAddNetworkRuleWithoutInputObject (Default)</span></span>
```
Set-AzContainerRegistryNetworkRuleSet -DefaultAction <String> [-NetworkRule <IPSNetworkRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da349-107">AddNetworkRuleWithInputObject</span><span class="sxs-lookup"><span data-stu-id="da349-107">AddNetworkRuleWithInputObject</span></span>
```
Set-AzContainerRegistryNetworkRuleSet [-DefaultAction <String>] [-NetworkRule <IPSNetworkRule[]>]
 -InputObject <PSNetworkRuleSet> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da349-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="da349-108">DESCRIPTION</span></span>
<span data-ttu-id="da349-109">Hálózati szabálykészlet létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="da349-109">Create or update a network rule set</span></span>

## <span data-ttu-id="da349-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="da349-110">EXAMPLES</span></span>

### <span data-ttu-id="da349-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="da349-111">Example 1</span></span>
```powershell
PS C:\> $subnet = New-AzVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix "10.0.1.0/24" -ServiceEndpoint "Microsoft.ContainerRegistry"
PS C:\> $vnet = New-AzVirtualNetwork -Name $VnetName -ResourceGroupName $resourceGroupName -Location $location -AddressPrefix "10.0.0.0/16" -Subnet $subnet
PS C:\> $rule = New-AzContainerRegistryNetworkRule -VirtualNetworkRule -VirtualNetworkResourceId $vnet.Subnets[0].Id
PS C:\> $set = Set-AzContainerRegistryNetworkRuleSet -DefaultAction "Allow" -NetworkRule $rule
```

<span data-ttu-id="da349-112">Hozzon létre egy új hálózati szabálykészletet.</span><span class="sxs-lookup"><span data-stu-id="da349-112">Create a new network rule set.</span></span>

## <span data-ttu-id="da349-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da349-113">PARAMETERS</span></span>

### <span data-ttu-id="da349-114">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="da349-114">-DefaultAction</span></span>
<span data-ttu-id="da349-115">Az alapértelmezett művelet lehet "Allow" (Megengedve) vagy "Deny" (Elutasítás)</span><span class="sxs-lookup"><span data-stu-id="da349-115">Default action, could be 'Allow' or 'Deny'</span></span>

```yaml
Type: System.String
Parameter Sets: AddAddNetworkRuleWithoutInputObject
Aliases:
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AddNetworkRuleWithInputObject
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da349-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da349-116">-DefaultProfile</span></span>
<span data-ttu-id="da349-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="da349-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da349-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="da349-118">-InputObject</span></span>
<span data-ttu-id="da349-119">Input PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="da349-119">Input PSNetworkRuleSet</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.Models.PSNetworkRuleSet
Parameter Sets: AddNetworkRuleWithInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da349-120">-NetworkRule</span><span class="sxs-lookup"><span data-stu-id="da349-120">-NetworkRule</span></span>
<span data-ttu-id="da349-121">Hálózati szabályok listája</span><span class="sxs-lookup"><span data-stu-id="da349-121">List of Network rules</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.Models.IPSNetworkRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da349-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da349-122">CommonParameters</span></span>
<span data-ttu-id="da349-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da349-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da349-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="da349-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da349-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="da349-125">INPUTS</span></span>

### <span data-ttu-id="da349-126">System.String</span><span class="sxs-lookup"><span data-stu-id="da349-126">System.String</span></span>

### <span data-ttu-id="da349-127">Microsoft.Azure.Commands.ContainerRegistry.Models.IPSNetworkRule</span><span class="sxs-lookup"><span data-stu-id="da349-127">Microsoft.Azure.Commands.ContainerRegistry.Models.IPSNetworkRule</span></span>

## <span data-ttu-id="da349-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="da349-128">OUTPUTS</span></span>

### <span data-ttu-id="da349-129">Microsoft.Azure.Commands.ContainerRegistry.Models.PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="da349-129">Microsoft.Azure.Commands.ContainerRegistry.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="da349-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="da349-130">NOTES</span></span>

## <span data-ttu-id="da349-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="da349-131">RELATED LINKS</span></span>
