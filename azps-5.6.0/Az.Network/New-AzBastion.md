---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azbastion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzBastion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzBastion.md
ms.openlocfilehash: a9faa6f118dafb8e2c7513a475e8eabb7361409e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939513"
---
# <span data-ttu-id="d44f8-101">New-AzBastion</span><span class="sxs-lookup"><span data-stu-id="d44f8-101">New-AzBastion</span></span>

## <span data-ttu-id="d44f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d44f8-102">SYNOPSIS</span></span>
<span data-ttu-id="d44f8-103">Egy bastion erőforrást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d44f8-103">Creates a bastion resource.</span></span>

## <span data-ttu-id="d44f8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d44f8-104">SYNTAX</span></span>

### <span data-ttu-id="d44f8-105">ByPublicIpAddressByVirtualNetwork (default)</span><span class="sxs-lookup"><span data-stu-id="d44f8-105">ByPublicIpAddressByVirtualNetwork (Default)</span></span>
```
New-AzBastion -ResourceGroupName <String> -Name <String> -PublicIpAddress <PSPublicIpAddress>
 -VirtualNetwork <PSVirtualNetwork> [-AsJob] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d44f8-106">ByPublicIpAddressByVirtualNetworkRGNameByVirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="d44f8-106">ByPublicIpAddressByVirtualNetworkRGNameByVirtualNetworkName</span></span>
```
New-AzBastion -ResourceGroupName <String> -Name <String> -PublicIpAddress <PSPublicIpAddress>
 -VirtualNetworkRgName <String> -VirtualNetworkName <String> [-AsJob] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d44f8-107">ByPublicIpAddressByVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="d44f8-107">ByPublicIpAddressByVirtualNetworkId</span></span>
```
New-AzBastion -ResourceGroupName <String> -Name <String> -PublicIpAddress <PSPublicIpAddress>
 -VirtualNetworkId <String> [-AsJob] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d44f8-108">ByPublicIpAddressIdByVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d44f8-108">ByPublicIpAddressIdByVirtualNetwork</span></span>
```
New-AzBastion -ResourceGroupName <String> -Name <String> -PublicIpAddressId <String>
 -VirtualNetwork <PSVirtualNetwork> [-AsJob] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d44f8-109">ByPublicIpAddressIdByVirtualNetworkRGNameByVirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="d44f8-109">ByPublicIpAddressIdByVirtualNetworkRGNameByVirtualNetworkName</span></span>
```
New-AzBastion -ResourceGroupName <String> -Name <String> -PublicIpAddressId <String>
 -VirtualNetworkRgName <String> -VirtualNetworkName <String> [-AsJob] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d44f8-110">ByPublicIpAddressIdByVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="d44f8-110">ByPublicIpAddressIdByVirtualNetworkId</span></span>
```
New-AzBastion -ResourceGroupName <String> -Name <String> -PublicIpAddressId <String> -VirtualNetworkId <String>
 [-AsJob] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d44f8-111">ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d44f8-111">ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetwork</span></span>
```
New-AzBastion -ResourceGroupName <String> -Name <String> -PublicIpAddressRgName <String>
 -PublicIpAddressName <String> -VirtualNetwork <PSVirtualNetwork> [-AsJob] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d44f8-112">ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetworkRGNameByVirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="d44f8-112">ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetworkRGNameByVirtualNetworkName</span></span>
```
New-AzBastion -ResourceGroupName <String> -Name <String> -PublicIpAddressRgName <String>
 -PublicIpAddressName <String> -VirtualNetworkRgName <String> -VirtualNetworkName <String> [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d44f8-113">ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="d44f8-113">ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetworkId</span></span>
```
New-AzBastion -ResourceGroupName <String> -Name <String> -PublicIpAddressRgName <String>
 -PublicIpAddressName <String> -VirtualNetworkId <String> [-AsJob] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d44f8-114">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d44f8-114">DESCRIPTION</span></span>
<span data-ttu-id="d44f8-115">Egy bastion erőforrást hoz létre. Ehhez szükség lesz egy nyilvános IP-címre és egy VirtualNetwork hálózatra.</span><span class="sxs-lookup"><span data-stu-id="d44f8-115">Creates a bastion resource.This will need a Public Ip Address and a VirtualNetwork.</span></span> <span data-ttu-id="d44f8-116">Ebben a VirtualNetworkben azureBastionSubnet nevű alhálózatnak kell lennie. A nemi ip-címet a Sku Standard szabványsal kell létrehozni.</span><span class="sxs-lookup"><span data-stu-id="d44f8-116">There must be a subnet with name AzureBastionSubnet in this VirtualNetwork.The Pubic Ip Address must be created with Sku Standard.</span></span>

## <span data-ttu-id="d44f8-117">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d44f8-117">EXAMPLES</span></span>

### <span data-ttu-id="d44f8-118">1. példa</span><span class="sxs-lookup"><span data-stu-id="d44f8-118">Example 1</span></span>
```powershell
$subnetName = "AzureBastionSubnet"
$subnet = New-AzVirtualNetworkSubnetConfig -Name $subnetName -AddressPrefix 10.0.0.0/24
$vnet = New-AzVirtualNetwork -Name "TestVnet" -ResourceGroupName "BastionPowershellTest" -Location "westeurope" -AddressPrefix 10.0.0.0/16 -Subnet $subnet
$publicip = New-AzPublicIpAddress -ResourceGroupName "BastionPowershellTest" -name "Test-Ip" -location "westeurope" -AllocationMethod Dynamic -Sku Standard
$bastion = New-AzBastion -ResourceGroupName "BastionPowershellTest" â€“Name "test-Bastion2" -PublicIpAddress $publicip -VirtualNetwork $vnet

IpConfigurations     : {IpConf}
DnsName              : bst-a9ca868f-ddab-4a50-9f45-a443ea8a0187.bastion.azure.com
ProvisioningState    : Succeeded
IpConfigurationsText : [
                         {
                           "Subnet": {
                             "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/BastionPowershellTest/providers/Microsoft.Network/virtualNetworks/TestVnet/subnets/AzureBastionSubnet"
                           },
                           "PublicIpAddress": {
                             "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/BastionPowershellTest/providers/Microsoft.Network/publicIPAddresses/Test-Ip"
                           },
                           "ProvisioningState": "Succeeded",
                           "PrivateIpAllocationMethod": "Dynamic",
                           "Name": "IpConf",
                           "Etag": "W/\"ed810ccd-b3f6-4e22-891e-b0ed0a26d6dd\"",
                           "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/BastionPowershellTest/providers/Microsoft.Network/bastionHosts/test-Bastion2/bastionHostIpConfigurations/IpConf"
                         }
                       ]
ResourceGroupName    : BastionPowershellTest
Location             : westeurope
ResourceGuid         :
Type                 : Microsoft.Network/bastionHosts
Tag                  :
TagsTable            :
Name                 : test-Bastion2
Etag                 : W/"ed810ccd-b3f6-4e22-891e-b0ed0a26d6dd"
Id                   : /subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/BastionPowershellTest/providers/Microsoft.Network/bastionHosts/test-Bastion2

This example creates a bastion attached to virtual network "vnet" in the same resource group as the bastion.
There must be a subnet with name AzureBastionSubnet in this vnet.
The Ip Address must be created with Sku Standard.
```

### <span data-ttu-id="d44f8-119">2. példa</span><span class="sxs-lookup"><span data-stu-id="d44f8-119">Example 2</span></span>
```powershell
$vnet = Get-AzVirtualNetwork -ResourceGroupName "BastionPowershellTest" -Name "testVnet2"
Add-AzVirtualNetworkSubnetConfig -Name "AzureBastionSubnet" -VirtualNetwork $vnet -AddressPrefix "10.0.0.0/24"
$vnet| Set-AzVirtualNetwork
New-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion2" -PublicIpAddressRgName "BastionPowershellTest" -PublicIpAddressName "testIp2" -VirtualNetworkRgName "BastionPowershellTest" -VirtualNetworkName "testVnet2"

IpConfigurations     : {IpConf}
DnsName              : bst-53757658-c4fd-4908-b1a7-0849e555d489.bastion.azure.com
ProvisioningState    : Succeeded
IpConfigurationsText : [
                         {
                           "Name": "IpConf",
                           "Etag": "W/\"7460e5f6-ad41-438b-a595-a63346ed8f16\"",
                           "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/BastionPowershellTest/providers/Microsoft.Network/bastionHosts/testBastion2/bastionHostIpConfigurations/IpConf",
                           "Subnet": {
                             "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/BastionPowershellTest/providers/Microsoft.Network/virtualNetworks/testVnet2/subnets/AzureBastionSubnet"
                           },
                           "PublicIpAddress": {
                             "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/BastionPowershellTest/providers/Microsoft.Network/publicIPAddresses/testIp2"
                           },
                           "ProvisioningState": "Succeeded",
                           "PrivateIpAllocationMethod": "Dynamic"
                         }
                       ]
ResourceGroupName    : BastionPowershellTest
Location             : westeurope
ResourceGuid         :
Type                 : Microsoft.Network/bastionHosts
Tag                  :
TagsTable            :
Name                 : testBastion2
Etag                 : W/"7460e5f6-ad41-438b-a595-a63346ed8f16"
Id                   : /subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/BastionPowershellTest/providers/Microsoft.Network/bastionHosts/testBastion2
```

## <span data-ttu-id="d44f8-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d44f8-120">PARAMETERS</span></span>

### <span data-ttu-id="d44f8-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d44f8-121">-AsJob</span></span>
<span data-ttu-id="d44f8-122">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="d44f8-122">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d44f8-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d44f8-123">-Confirm</span></span>
<span data-ttu-id="d44f8-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d44f8-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d44f8-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d44f8-125">-DefaultProfile</span></span>
<span data-ttu-id="d44f8-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d44f8-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d44f8-127">-Name</span><span class="sxs-lookup"><span data-stu-id="d44f8-127">-Name</span></span>
<span data-ttu-id="d44f8-128">A bazsalika erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="d44f8-128">The bastion resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, BastionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d44f8-129">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d44f8-129">-PublicIpAddress</span></span>
<span data-ttu-id="d44f8-130">A bazsalika nyilvános IP-címobjektuma.</span><span class="sxs-lookup"><span data-stu-id="d44f8-130">The public IP address object for bastion.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: ByPublicIpAddressByVirtualNetwork, ByPublicIpAddressByVirtualNetworkRGNameByVirtualNetworkName, ByPublicIpAddressByVirtualNetworkId
Aliases: PublicIpAddressObject

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d44f8-131">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="d44f8-131">-PublicIpAddressId</span></span>
<span data-ttu-id="d44f8-132">A nyilvános IP-cím, a bazsalika Azure-erőforrásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="d44f8-132">The public Ip address Azure resource Id for bastion.</span></span>

```yaml
Type: String
Parameter Sets: ByPublicIpAddressIdByVirtualNetwork, ByPublicIpAddressIdByVirtualNetworkRGNameByVirtualNetworkName, ByPublicIpAddressIdByVirtualNetworkId
Aliases: PublicIpAddressResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d44f8-133">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="d44f8-133">-PublicIpAddressName</span></span>
<span data-ttu-id="d44f8-134">A nyilvános IP-cím erőforrásneve a bazsalika számára.</span><span class="sxs-lookup"><span data-stu-id="d44f8-134">The public Ip address resource name for bastion.</span></span>

```yaml
Type: String
Parameter Sets: ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetwork, ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetworkRGNameByVirtualNetworkName, ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetworkId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d44f8-135">-PublicIpAddressRgName</span><span class="sxs-lookup"><span data-stu-id="d44f8-135">-PublicIpAddressRgName</span></span>
<span data-ttu-id="d44f8-136">A nyilvános Ip-cím erőforráscsoport neve a bazsalika számára.</span><span class="sxs-lookup"><span data-stu-id="d44f8-136">The public Ip address resource group name for bastion.</span></span>

```yaml
Type: String
Parameter Sets: ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetwork, ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetworkRGNameByVirtualNetworkName, ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetworkId
Aliases: PublicIpAddressResourceGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d44f8-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d44f8-137">-ResourceGroupName</span></span>
<span data-ttu-id="d44f8-138">Az erőforráscsoport neve, ahol létre kell hoznia a bástyát.</span><span class="sxs-lookup"><span data-stu-id="d44f8-138">The resource group name where you need to create bastion.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d44f8-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="d44f8-139">-Tag</span></span>
<span data-ttu-id="d44f8-140">Erőforráscímkéket képviselő hashtable.</span><span class="sxs-lookup"><span data-stu-id="d44f8-140">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d44f8-141">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d44f8-141">-VirtualNetwork</span></span>
<span data-ttu-id="d44f8-142">A bazsalikom virtuális hálózati objektuma.</span><span class="sxs-lookup"><span data-stu-id="d44f8-142">The virtual network object for bastion.</span></span>

```yaml
Type: PSVirtualNetwork
Parameter Sets: ByPublicIpAddressByVirtualNetwork, ByPublicIpAddressIdByVirtualNetwork, ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetwork
Aliases: VirtualNetworkObject

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d44f8-143">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="d44f8-143">-VirtualNetworkId</span></span>
<span data-ttu-id="d44f8-144">A virtuális hálózat Azure-erőforrásazonosítója a bazsalizációhoz.</span><span class="sxs-lookup"><span data-stu-id="d44f8-144">The virtual network Azure resource Id for bastion.</span></span>

```yaml
Type: String
Parameter Sets: ByPublicIpAddressByVirtualNetworkId, ByPublicIpAddressIdByVirtualNetworkId, ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetworkId
Aliases: VirtualNetworkResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d44f8-145">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="d44f8-145">-VirtualNetworkName</span></span>
<span data-ttu-id="d44f8-146">A bazsalika virtuális hálózati erőforrásneve.</span><span class="sxs-lookup"><span data-stu-id="d44f8-146">The virtual network resource name for bastion.</span></span>

```yaml
Type: String
Parameter Sets: ByPublicIpAddressByVirtualNetworkRGNameByVirtualNetworkName, ByPublicIpAddressIdByVirtualNetworkRGNameByVirtualNetworkName, ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetworkRGNameByVirtualNetworkName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d44f8-147">-VirtualNetworkRgName</span><span class="sxs-lookup"><span data-stu-id="d44f8-147">-VirtualNetworkRgName</span></span>
<span data-ttu-id="d44f8-148">A virtuális hálózati erőforráscsoport neve a bástyához.</span><span class="sxs-lookup"><span data-stu-id="d44f8-148">The virtual network resource group name for bastion.</span></span>

```yaml
Type: String
Parameter Sets: ByPublicIpAddressByVirtualNetworkRGNameByVirtualNetworkName, ByPublicIpAddressIdByVirtualNetworkRGNameByVirtualNetworkName, ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetworkRGNameByVirtualNetworkName
Aliases: VirtualNetworkResourceGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d44f8-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d44f8-149">-WhatIf</span></span>
<span data-ttu-id="d44f8-150">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d44f8-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d44f8-151">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d44f8-151">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d44f8-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d44f8-152">CommonParameters</span></span>
<span data-ttu-id="d44f8-153">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d44f8-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d44f8-154">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d44f8-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d44f8-155">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d44f8-155">INPUTS</span></span>

### <span data-ttu-id="d44f8-156">Nincs</span><span class="sxs-lookup"><span data-stu-id="d44f8-156">None</span></span>

## <span data-ttu-id="d44f8-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d44f8-157">OUTPUTS</span></span>

### <span data-ttu-id="d44f8-158">Microsoft.Azure.Commands.Network.Models.PSBastion</span><span class="sxs-lookup"><span data-stu-id="d44f8-158">Microsoft.Azure.Commands.Network.Models.PSBastion</span></span>

## <span data-ttu-id="d44f8-159">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d44f8-159">NOTES</span></span>

## <span data-ttu-id="d44f8-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d44f8-160">RELATED LINKS</span></span>
[<span data-ttu-id="d44f8-161">Get-AzBastion</span><span class="sxs-lookup"><span data-stu-id="d44f8-161">Get-AzBastion</span></span>](./Get-AzBastion.md)

[<span data-ttu-id="d44f8-162">Remove-AzBastion</span><span class="sxs-lookup"><span data-stu-id="d44f8-162">Remove-AzBastion</span></span>](./Remove-AzBastion.md)