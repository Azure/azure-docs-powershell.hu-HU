---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistrynetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryNetworkRule.md
ms.openlocfilehash: f60f85a14df42043352af1b71f0455983e03061a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296378"
---
# <span data-ttu-id="6f5fe-101">New-AzContainerRegistryNetworkRule</span><span class="sxs-lookup"><span data-stu-id="6f5fe-101">New-AzContainerRegistryNetworkRule</span></span>

## <span data-ttu-id="6f5fe-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6f5fe-102">SYNOPSIS</span></span>
<span data-ttu-id="6f5fe-103">Hozzon létre egy hálózati szabályt.</span><span class="sxs-lookup"><span data-stu-id="6f5fe-103">Create a network rule.</span></span>

## <span data-ttu-id="6f5fe-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6f5fe-104">SYNTAX</span></span>

### <span data-ttu-id="6f5fe-105">ByVirtualNetworkRule (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6f5fe-105">ByVirtualNetworkRule (Default)</span></span>
```
New-AzContainerRegistryNetworkRule [-Action <String>] [-VirtualNetworkRule] -VirtualNetworkResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f5fe-106">ByIPRule</span><span class="sxs-lookup"><span data-stu-id="6f5fe-106">ByIPRule</span></span>
```
New-AzContainerRegistryNetworkRule [-Action <String>] [-IPRule] -IPAddressOrRange <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f5fe-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="6f5fe-107">DESCRIPTION</span></span>
<span data-ttu-id="6f5fe-108">Hálózatbeállítási objektum létrehozása az aktuális PowerShell-munkamenetben.</span><span class="sxs-lookup"><span data-stu-id="6f5fe-108">Create a network rule object in current powershell session.</span></span>

## <span data-ttu-id="6f5fe-109">Példák</span><span class="sxs-lookup"><span data-stu-id="6f5fe-109">EXAMPLES</span></span>

### <span data-ttu-id="6f5fe-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6f5fe-110">Example 1</span></span>
```powershell
PS C:\> $subnet = New-AzVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix "10.0.1.0/24" -ServiceEndpoint "Microsoft.ContainerRegistry"
PS C:\> $vnet = New-AzVirtualNetwork -Name $VnetName -ResourceGroupName $resourceGroupName -Location $location -AddressPrefix "10.0.0.0/16" -Subnet $subnet
PS C:\> $rule = New-AzContainerRegistryNetworkRule -VirtualNetworkRule -VirtualNetworkResourceId $vnet.Subnets[0].Id
```

<span data-ttu-id="6f5fe-111">Virtualnetwork-szabálykészlet létrehozása</span><span class="sxs-lookup"><span data-stu-id="6f5fe-111">Create virtualnetwork rule set.</span></span>

## <span data-ttu-id="6f5fe-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6f5fe-112">PARAMETERS</span></span>

### <span data-ttu-id="6f5fe-113">-Műveletek</span><span class="sxs-lookup"><span data-stu-id="6f5fe-113">-Action</span></span>
<span data-ttu-id="6f5fe-114">A hálózati szabály tevékenysége.</span><span class="sxs-lookup"><span data-stu-id="6f5fe-114">The action of network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f5fe-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f5fe-115">-DefaultProfile</span></span>
<span data-ttu-id="6f5fe-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6f5fe-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f5fe-117">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="6f5fe-117">-IPAddressOrRange</span></span>
<span data-ttu-id="6f5fe-118">Az IP-vagy IP-tartományok CIDR formátumban.</span><span class="sxs-lookup"><span data-stu-id="6f5fe-118">Specifies the IP or IP range in CIDR format.</span></span>
<span data-ttu-id="6f5fe-119">Csak az IPV4-cím engedélyezett.</span><span class="sxs-lookup"><span data-stu-id="6f5fe-119">Only IPV4 address is allowed.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIPRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f5fe-120">-IPRule</span><span class="sxs-lookup"><span data-stu-id="6f5fe-120">-IPRule</span></span>
<span data-ttu-id="6f5fe-121">Adja meg a IPRule létrehozását.</span><span class="sxs-lookup"><span data-stu-id="6f5fe-121">Indicate to create IPRule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByIPRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f5fe-122">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="6f5fe-122">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="6f5fe-123">Egy alhálózat erőforrás-azonosítója, például:/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworks/{vnetName}/subnets/{subnetName}.</span><span class="sxs-lookup"><span data-stu-id="6f5fe-123">Resource ID of a subnet, for example: /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworks/{vnetName}/subnets/{subnetName}.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualNetworkRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f5fe-124">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="6f5fe-124">-VirtualNetworkRule</span></span>
<span data-ttu-id="6f5fe-125">Adja meg a VirtualNetworkRule létrehozását.</span><span class="sxs-lookup"><span data-stu-id="6f5fe-125">Indicate to create VirtualNetworkRule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByVirtualNetworkRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f5fe-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f5fe-126">CommonParameters</span></span>
<span data-ttu-id="6f5fe-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6f5fe-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f5fe-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6f5fe-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f5fe-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6f5fe-129">INPUTS</span></span>

### <span data-ttu-id="6f5fe-130">System. String</span><span class="sxs-lookup"><span data-stu-id="6f5fe-130">System.String</span></span>

## <span data-ttu-id="6f5fe-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6f5fe-131">OUTPUTS</span></span>

### <span data-ttu-id="6f5fe-132">Microsoft. Azure. Command. ContainerRegistry. models. IPSNetworkRule</span><span class="sxs-lookup"><span data-stu-id="6f5fe-132">Microsoft.Azure.Commands.ContainerRegistry.Models.IPSNetworkRule</span></span>

## <span data-ttu-id="6f5fe-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6f5fe-133">NOTES</span></span>

## <span data-ttu-id="6f5fe-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6f5fe-134">RELATED LINKS</span></span>
