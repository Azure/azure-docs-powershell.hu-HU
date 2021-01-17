---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistrynetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryNetworkRule.md
ms.openlocfilehash: f60f85a14df42043352af1b71f0455983e03061a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357796"
---
# <span data-ttu-id="a8bd4-101">New-AzContainerRegistryNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a8bd4-101">New-AzContainerRegistryNetworkRule</span></span>

## <span data-ttu-id="a8bd4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8bd4-102">SYNOPSIS</span></span>
<span data-ttu-id="a8bd4-103">Hozzon létre egy hálózati szabályt.</span><span class="sxs-lookup"><span data-stu-id="a8bd4-103">Create a network rule.</span></span>

## <span data-ttu-id="a8bd4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a8bd4-104">SYNTAX</span></span>

### <span data-ttu-id="a8bd4-105">ByVirtualNetworkRule (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a8bd4-105">ByVirtualNetworkRule (Default)</span></span>
```
New-AzContainerRegistryNetworkRule [-Action <String>] [-VirtualNetworkRule] -VirtualNetworkResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8bd4-106">ByIPRule</span><span class="sxs-lookup"><span data-stu-id="a8bd4-106">ByIPRule</span></span>
```
New-AzContainerRegistryNetworkRule [-Action <String>] [-IPRule] -IPAddressOrRange <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8bd4-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a8bd4-107">DESCRIPTION</span></span>
<span data-ttu-id="a8bd4-108">Hozzon létre egy hálózati szabályobjektumot az aktuális PowerShell-munkamenetben.</span><span class="sxs-lookup"><span data-stu-id="a8bd4-108">Create a network rule object in current powershell session.</span></span>

## <span data-ttu-id="a8bd4-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a8bd4-109">EXAMPLES</span></span>

### <span data-ttu-id="a8bd4-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="a8bd4-110">Example 1</span></span>
```powershell
PS C:\> $subnet = New-AzVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix "10.0.1.0/24" -ServiceEndpoint "Microsoft.ContainerRegistry"
PS C:\> $vnet = New-AzVirtualNetwork -Name $VnetName -ResourceGroupName $resourceGroupName -Location $location -AddressPrefix "10.0.0.0/16" -Subnet $subnet
PS C:\> $rule = New-AzContainerRegistryNetworkRule -VirtualNetworkRule -VirtualNetworkResourceId $vnet.Subnets[0].Id
```

<span data-ttu-id="a8bd4-111">Virtuálisnetwork szabálykészlet létrehozása.</span><span class="sxs-lookup"><span data-stu-id="a8bd4-111">Create virtualnetwork rule set.</span></span>

## <span data-ttu-id="a8bd4-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a8bd4-112">PARAMETERS</span></span>

### <span data-ttu-id="a8bd4-113">-Művelet</span><span class="sxs-lookup"><span data-stu-id="a8bd4-113">-Action</span></span>
<span data-ttu-id="a8bd4-114">A hálózati szabály művelete.</span><span class="sxs-lookup"><span data-stu-id="a8bd4-114">The action of network rule.</span></span>

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

### <span data-ttu-id="a8bd4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8bd4-115">-DefaultProfile</span></span>
<span data-ttu-id="a8bd4-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a8bd4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8bd4-117">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="a8bd4-117">-IPAddressOrRange</span></span>
<span data-ttu-id="a8bd4-118">Az IP- vagy IP-tartomány CIDR formátumban való megadása.</span><span class="sxs-lookup"><span data-stu-id="a8bd4-118">Specifies the IP or IP range in CIDR format.</span></span>
<span data-ttu-id="a8bd4-119">Csak IPV4-cím engedélyezett.</span><span class="sxs-lookup"><span data-stu-id="a8bd4-119">Only IPV4 address is allowed.</span></span>

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

### <span data-ttu-id="a8bd4-120">-IPRule</span><span class="sxs-lookup"><span data-stu-id="a8bd4-120">-IPRule</span></span>
<span data-ttu-id="a8bd4-121">Adja meg, hogy létre kell hoznia az IPRule protokollt.</span><span class="sxs-lookup"><span data-stu-id="a8bd4-121">Indicate to create IPRule.</span></span>

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

### <span data-ttu-id="a8bd4-122">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="a8bd4-122">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="a8bd4-123">Egy alhálózat erőforrás-azonosítója, például: /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworks/{vnetName}/alhálózatok/{alnetName}.</span><span class="sxs-lookup"><span data-stu-id="a8bd4-123">Resource ID of a subnet, for example: /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworks/{vnetName}/subnets/{subnetName}.</span></span>

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

### <span data-ttu-id="a8bd4-124">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a8bd4-124">-VirtualNetworkRule</span></span>
<span data-ttu-id="a8bd4-125">A VirtualNetworkRule létrehozására utal.</span><span class="sxs-lookup"><span data-stu-id="a8bd4-125">Indicate to create VirtualNetworkRule.</span></span>

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

### <span data-ttu-id="a8bd4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8bd4-126">CommonParameters</span></span>
<span data-ttu-id="a8bd4-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8bd4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8bd4-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a8bd4-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8bd4-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a8bd4-129">INPUTS</span></span>

### <span data-ttu-id="a8bd4-130">System.String</span><span class="sxs-lookup"><span data-stu-id="a8bd4-130">System.String</span></span>

## <span data-ttu-id="a8bd4-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a8bd4-131">OUTPUTS</span></span>

### <span data-ttu-id="a8bd4-132">Microsoft.Azure.Commands.ContainerRegistry.Models.IPSNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a8bd4-132">Microsoft.Azure.Commands.ContainerRegistry.Models.IPSNetworkRule</span></span>

## <span data-ttu-id="a8bd4-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a8bd4-133">NOTES</span></span>

## <span data-ttu-id="a8bd4-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a8bd4-134">RELATED LINKS</span></span>
