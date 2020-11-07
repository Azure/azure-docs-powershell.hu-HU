---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azbastion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzBastion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzBastion.md
ms.openlocfilehash: 5bc2bedf3d79f2ee0040f66f7df6506dfa342982
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837234"
---
# <span data-ttu-id="551df-101">New-AzBastion</span><span class="sxs-lookup"><span data-stu-id="551df-101">New-AzBastion</span></span>

## <span data-ttu-id="551df-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="551df-102">SYNOPSIS</span></span>
<span data-ttu-id="551df-103">Bástya-erőforrást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="551df-103">Creates a bastion resource.</span></span>

## <span data-ttu-id="551df-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="551df-104">SYNTAX</span></span>

### <span data-ttu-id="551df-105">ByPublicIpAddressByVirtualNetwork (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="551df-105">ByPublicIpAddressByVirtualNetwork (Default)</span></span>
```
New-AzBastion -ResourceGroupName <String> -Name <String> -PublicIpAddress <PSPublicIpAddress>
 -VirtualNetwork <PSVirtualNetwork> [-AsJob] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="551df-106">ByPublicIpAddressByVirtualNetworkRGNameByVirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="551df-106">ByPublicIpAddressByVirtualNetworkRGNameByVirtualNetworkName</span></span>
```
New-AzBastion -ResourceGroupName <String> -Name <String> -PublicIpAddress <PSPublicIpAddress>
 -VirtualNetworkRgName <String> -VirtualNetworkName <String> [-AsJob] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="551df-107">ByPublicIpAddressByVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="551df-107">ByPublicIpAddressByVirtualNetworkId</span></span>
```
New-AzBastion -ResourceGroupName <String> -Name <String> -PublicIpAddress <PSPublicIpAddress>
 -VirtualNetworkId <String> [-AsJob] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="551df-108">ByPublicIpAddressIdByVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="551df-108">ByPublicIpAddressIdByVirtualNetwork</span></span>
```
New-AzBastion -ResourceGroupName <String> -Name <String> -PublicIpAddressId <String>
 -VirtualNetwork <PSVirtualNetwork> [-AsJob] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="551df-109">ByPublicIpAddressIdByVirtualNetworkRGNameByVirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="551df-109">ByPublicIpAddressIdByVirtualNetworkRGNameByVirtualNetworkName</span></span>
```
New-AzBastion -ResourceGroupName <String> -Name <String> -PublicIpAddressId <String>
 -VirtualNetworkRgName <String> -VirtualNetworkName <String> [-AsJob] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="551df-110">ByPublicIpAddressIdByVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="551df-110">ByPublicIpAddressIdByVirtualNetworkId</span></span>
```
New-AzBastion -ResourceGroupName <String> -Name <String> -PublicIpAddressId <String> -VirtualNetworkId <String>
 [-AsJob] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="551df-111">ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="551df-111">ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetwork</span></span>
```
New-AzBastion -ResourceGroupName <String> -Name <String> -PublicIpAddressRgName <String>
 -PublicIpAddressName <String> -VirtualNetwork <PSVirtualNetwork> [-AsJob] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="551df-112">ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetworkRGNameByVirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="551df-112">ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetworkRGNameByVirtualNetworkName</span></span>
```
New-AzBastion -ResourceGroupName <String> -Name <String> -PublicIpAddressRgName <String>
 -PublicIpAddressName <String> -VirtualNetworkRgName <String> -VirtualNetworkName <String> [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="551df-113">ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="551df-113">ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetworkId</span></span>
```
New-AzBastion -ResourceGroupName <String> -Name <String> -PublicIpAddressRgName <String>
 -PublicIpAddressName <String> -VirtualNetworkId <String> [-AsJob] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="551df-114">Leírás</span><span class="sxs-lookup"><span data-stu-id="551df-114">DESCRIPTION</span></span>
<span data-ttu-id="551df-115">Bástya-erőforrást hoz létre. Ehhez szüksége lesz egy nyilvános IP-címre és egy VirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="551df-115">Creates a bastion resource.This will need a Public Ip Address and a VirtualNetwork.</span></span> <span data-ttu-id="551df-116">Ebben a VirtualNetwork a name AzureBastionSubnet alhálózatnak kell lennie. a ágyéki IP-címet a SKU standard értékkel kell létrehozni.</span><span class="sxs-lookup"><span data-stu-id="551df-116">There must be a subnet with name AzureBastionSubnet in this VirtualNetwork.The Pubic Ip Address must be created with Sku Standard.</span></span>

## <span data-ttu-id="551df-117">Példák</span><span class="sxs-lookup"><span data-stu-id="551df-117">EXAMPLES</span></span>

### <span data-ttu-id="551df-118">Példa 1</span><span class="sxs-lookup"><span data-stu-id="551df-118">Example 1</span></span>
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

### <span data-ttu-id="551df-119">2. példa</span><span class="sxs-lookup"><span data-stu-id="551df-119">Example 2</span></span>
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

## <span data-ttu-id="551df-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="551df-120">PARAMETERS</span></span>

### <span data-ttu-id="551df-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="551df-121">-AsJob</span></span>
<span data-ttu-id="551df-122">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="551df-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="551df-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="551df-123">-Confirm</span></span>
<span data-ttu-id="551df-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="551df-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="551df-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="551df-125">-DefaultProfile</span></span>
<span data-ttu-id="551df-126">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="551df-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="551df-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="551df-127">-Name</span></span>
<span data-ttu-id="551df-128">A bástya erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="551df-128">The bastion resource name.</span></span>

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

### <span data-ttu-id="551df-129">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="551df-129">-PublicIpAddress</span></span>
<span data-ttu-id="551df-130">A bástya nyilvános IP-cím objektuma.</span><span class="sxs-lookup"><span data-stu-id="551df-130">The public IP address object for bastion.</span></span>

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

### <span data-ttu-id="551df-131">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="551df-131">-PublicIpAddressId</span></span>
<span data-ttu-id="551df-132">A Bastion-hez tartozó nyilvános IP-cím Azure Resource ID azonosítója.</span><span class="sxs-lookup"><span data-stu-id="551df-132">The public Ip address Azure resource Id for bastion.</span></span>

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

### <span data-ttu-id="551df-133">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="551df-133">-PublicIpAddressName</span></span>
<span data-ttu-id="551df-134">A bástya nyilvános IP-cím erőforrásának neve.</span><span class="sxs-lookup"><span data-stu-id="551df-134">The public Ip address resource name for bastion.</span></span>

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

### <span data-ttu-id="551df-135">-PublicIpAddressRgName</span><span class="sxs-lookup"><span data-stu-id="551df-135">-PublicIpAddressRgName</span></span>
<span data-ttu-id="551df-136">A bástya nyilvános IP-cím nevű erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="551df-136">The public Ip address resource group name for bastion.</span></span>

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

### <span data-ttu-id="551df-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="551df-137">-ResourceGroupName</span></span>
<span data-ttu-id="551df-138">Az erőforráscsoport neve, ahová a bástya létrehozása szükséges.</span><span class="sxs-lookup"><span data-stu-id="551df-138">The resource group name where you need to create bastion.</span></span>

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

### <span data-ttu-id="551df-139">-Címke</span><span class="sxs-lookup"><span data-stu-id="551df-139">-Tag</span></span>
<span data-ttu-id="551df-140">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="551df-140">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="551df-141">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="551df-141">-VirtualNetwork</span></span>
<span data-ttu-id="551df-142">A bástya virtuális hálózati objektuma.</span><span class="sxs-lookup"><span data-stu-id="551df-142">The virtual network object for bastion.</span></span>

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

### <span data-ttu-id="551df-143">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="551df-143">-VirtualNetworkId</span></span>
<span data-ttu-id="551df-144">A bástya virtuális hálózat Azure Resource ID azonosítója.</span><span class="sxs-lookup"><span data-stu-id="551df-144">The virtual network Azure resource Id for bastion.</span></span>

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

### <span data-ttu-id="551df-145">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="551df-145">-VirtualNetworkName</span></span>
<span data-ttu-id="551df-146">A bástya virtuális hálózati erőforrásának neve.</span><span class="sxs-lookup"><span data-stu-id="551df-146">The virtual network resource name for bastion.</span></span>

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

### <span data-ttu-id="551df-147">-VirtualNetworkRgName</span><span class="sxs-lookup"><span data-stu-id="551df-147">-VirtualNetworkRgName</span></span>
<span data-ttu-id="551df-148">A virtuális hálózat erőforráscsoport neve a bástya számára.</span><span class="sxs-lookup"><span data-stu-id="551df-148">The virtual network resource group name for bastion.</span></span>

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

### <span data-ttu-id="551df-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="551df-149">-WhatIf</span></span>
<span data-ttu-id="551df-150">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="551df-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="551df-151">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="551df-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="551df-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="551df-152">CommonParameters</span></span>
<span data-ttu-id="551df-153">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="551df-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="551df-154">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="551df-154">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="551df-155">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="551df-155">INPUTS</span></span>

### <span data-ttu-id="551df-156">Nincs</span><span class="sxs-lookup"><span data-stu-id="551df-156">None</span></span>

## <span data-ttu-id="551df-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="551df-157">OUTPUTS</span></span>

### <span data-ttu-id="551df-158">Microsoft. Azure. commands. Network. models. PSBastion</span><span class="sxs-lookup"><span data-stu-id="551df-158">Microsoft.Azure.Commands.Network.Models.PSBastion</span></span>

## <span data-ttu-id="551df-159">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="551df-159">NOTES</span></span>

## <span data-ttu-id="551df-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="551df-160">RELATED LINKS</span></span>
[<span data-ttu-id="551df-161">Get-AzBastion</span><span class="sxs-lookup"><span data-stu-id="551df-161">Get-AzBastion</span></span>](./Get-AzBastion.md)

[<span data-ttu-id="551df-162">Remove-AzBastion</span><span class="sxs-lookup"><span data-stu-id="551df-162">Remove-AzBastion</span></span>](./Remove-AzBastion.md)