---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/set-azcontainerregistrynetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Set-AzContainerRegistryNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Set-AzContainerRegistryNetworkRuleSet.md
ms.openlocfilehash: 4a2292b0b573a5357466f3b240ba3b6df7cf0a1e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185578"
---
# <span data-ttu-id="b9481-101">Set-AzContainerRegistryNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="b9481-101">Set-AzContainerRegistryNetworkRuleSet</span></span>

## <span data-ttu-id="b9481-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b9481-102">SYNOPSIS</span></span>
<span data-ttu-id="b9481-103">Hálózati szabálykészlet létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="b9481-103">Create or update a network rule set.</span></span> <span data-ttu-id="b9481-104">A szabály beállítása csak a "Prémium" rendszerleíró adatbázisra alkalmazható.</span><span class="sxs-lookup"><span data-stu-id="b9481-104">Rule set can only be applied to "Premium" registry.</span></span>

## <span data-ttu-id="b9481-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b9481-105">SYNTAX</span></span>

### <span data-ttu-id="b9481-106">AddAddNetworkRuleWithoutInputObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b9481-106">AddAddNetworkRuleWithoutInputObject (Default)</span></span>
```
Set-AzContainerRegistryNetworkRuleSet -DefaultAction <String> [-NetworkRule <IPSNetworkRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9481-107">AddNetworkRuleWithInputObject</span><span class="sxs-lookup"><span data-stu-id="b9481-107">AddNetworkRuleWithInputObject</span></span>
```
Set-AzContainerRegistryNetworkRuleSet [-DefaultAction <String>] [-NetworkRule <IPSNetworkRule[]>]
 -InputObject <PSNetworkRuleSet> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9481-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b9481-108">DESCRIPTION</span></span>
<span data-ttu-id="b9481-109">Hálózati szabálykészlet létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="b9481-109">Create or update a network rule set</span></span>

## <span data-ttu-id="b9481-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b9481-110">EXAMPLES</span></span>

### <span data-ttu-id="b9481-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b9481-111">Example 1</span></span>
```powershell
PS C:\> $subnet = New-AzVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix "10.0.1.0/24" -ServiceEndpoint "Microsoft.ContainerRegistry"
PS C:\> $vnet = New-AzVirtualNetwork -Name $VnetName -ResourceGroupName $resourceGroupName -Location $location -AddressPrefix "10.0.0.0/16" -Subnet $subnet
PS C:\> $rule = New-AzContainerRegistryNetworkRule -VirtualNetworkRule -VirtualNetworkResourceId $vnet.Subnets[0].Id
PS C:\> $set = Set-AzContainerRegistryNetworkRuleSet -DefaultAction "Allow" -NetworkRule $rule
```

<span data-ttu-id="b9481-112">Új hálózati szabálykészlet létrehozása</span><span class="sxs-lookup"><span data-stu-id="b9481-112">Create a new network rule set.</span></span>

## <span data-ttu-id="b9481-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b9481-113">PARAMETERS</span></span>

### <span data-ttu-id="b9481-114">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="b9481-114">-DefaultAction</span></span>
<span data-ttu-id="b9481-115">Alapértelmezett tevékenység, lehet "Allow" vagy "deny"</span><span class="sxs-lookup"><span data-stu-id="b9481-115">Default action, could be 'Allow' or 'Deny'</span></span>

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

### <span data-ttu-id="b9481-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9481-116">-DefaultProfile</span></span>
<span data-ttu-id="b9481-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b9481-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9481-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b9481-118">-InputObject</span></span>
<span data-ttu-id="b9481-119">Beviteli PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="b9481-119">Input PSNetworkRuleSet</span></span>

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

### <span data-ttu-id="b9481-120">-NetworkRule</span><span class="sxs-lookup"><span data-stu-id="b9481-120">-NetworkRule</span></span>
<span data-ttu-id="b9481-121">A hálózati szabályok listája</span><span class="sxs-lookup"><span data-stu-id="b9481-121">List of Network rules</span></span>

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

### <span data-ttu-id="b9481-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9481-122">CommonParameters</span></span>
<span data-ttu-id="b9481-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b9481-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9481-124">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b9481-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9481-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9481-125">INPUTS</span></span>

### <span data-ttu-id="b9481-126">System. String</span><span class="sxs-lookup"><span data-stu-id="b9481-126">System.String</span></span>

### <span data-ttu-id="b9481-127">Microsoft. Azure. Command. ContainerRegistry. models. IPSNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b9481-127">Microsoft.Azure.Commands.ContainerRegistry.Models.IPSNetworkRule</span></span>

## <span data-ttu-id="b9481-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9481-128">OUTPUTS</span></span>

### <span data-ttu-id="b9481-129">Microsoft. Azure. Command. ContainerRegistry. models. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="b9481-129">Microsoft.Azure.Commands.ContainerRegistry.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="b9481-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b9481-130">NOTES</span></span>

## <span data-ttu-id="b9481-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b9481-131">RELATED LINKS</span></span>
