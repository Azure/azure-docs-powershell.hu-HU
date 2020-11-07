---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 81D55C43-C9A3-4DA7-A469-A3A7550FE9A4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetwork.md
ms.openlocfilehash: b7dc6c405ae1a5a213cedcb4b9737ff23dcf2b36
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679284"
---
# <span data-ttu-id="bbe96-101">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="bbe96-101">New-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="bbe96-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bbe96-102">SYNOPSIS</span></span>
<span data-ttu-id="bbe96-103">Virtuális hálózatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="bbe96-103">Creates a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bbe96-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bbe96-104">SYNTAX</span></span>

```
New-AzureRmVirtualNetwork -Name <String> -ResourceGroupName <String> -Location <String>
 -AddressPrefix <System.Collections.Generic.List`1[System.String]>
 [-DnsServer <System.Collections.Generic.List`1[System.String]>]
 [-Subnet <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSSubnet]>]
 [-Tag <Hashtable>] [-EnableDDoSProtection] [-EnableVmProtection] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bbe96-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bbe96-105">DESCRIPTION</span></span>
<span data-ttu-id="bbe96-106">A **New-AzureRmVirtualNetwork** parancsmag egy Azure virtuális hálózatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="bbe96-106">The **New-AzureRmVirtualNetwork** cmdlet creates an Azure virtual network.</span></span>

## <span data-ttu-id="bbe96-107">Példák</span><span class="sxs-lookup"><span data-stu-id="bbe96-107">EXAMPLES</span></span>

### <span data-ttu-id="bbe96-108">1: virtuális hálózat létrehozása két alhálózattal</span><span class="sxs-lookup"><span data-stu-id="bbe96-108">1:  Create a virtual network with two subnets</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet  = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="bbe96-109">Ebben a példában két alhálózatot tartalmazó virtuális hálózat jön létre.</span><span class="sxs-lookup"><span data-stu-id="bbe96-109">This example creates a virtual network with two subnets.</span></span> <span data-ttu-id="bbe96-110">Először egy új erőforráscsoport jön létre a CentralUS-régióban.</span><span class="sxs-lookup"><span data-stu-id="bbe96-110">First, a new resource group is created in the centralus region.</span></span> <span data-ttu-id="bbe96-111">Ezután a példa két alhálózat memóriában ábrázolt példányait hozza létre.</span><span class="sxs-lookup"><span data-stu-id="bbe96-111">Then, the example creates in-memory representations of two subnets.</span></span> <span data-ttu-id="bbe96-112">A New-AzureRmVirtualNetworkSubnetConfig parancsmag nem hoz létre alhálózatokat a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="bbe96-112">The New-AzureRmVirtualNetworkSubnetConfig cmdlet will not create any subnet on the server side.</span></span> <span data-ttu-id="bbe96-113">Egy frontendSubnet nevű alhálózatot és egy backendSubnet nevű alhálózatot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="bbe96-113">There is one subnet called frontendSubnet and one subnet called backendSubnet.</span></span> <span data-ttu-id="bbe96-114">A New-AzureRmVirtualNetwork parancsmag ezután virtuális hálózatot hoz létre a CIDR 10.0.0.0/16 segítségével a cím előtagként és két alhálózattal.</span><span class="sxs-lookup"><span data-stu-id="bbe96-114">The New-AzureRmVirtualNetwork cmdlet then creates a virtual network using the CIDR 10.0.0.0/16 as the address prefix and two subnets.</span></span>

### <span data-ttu-id="bbe96-115">2: virtuális hálózat létrehozása a DNS-beállításokkal</span><span class="sxs-lookup"><span data-stu-id="bbe96-115">2:  Create a virtual network with DNS settings</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet  = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet -DnsServer 10.0.1.5,10.0.1.6
```

<span data-ttu-id="bbe96-116">Ebben a példában egy virtuális hálózat jön létre két alhálózattal és két DNS-kiszolgálóval.</span><span class="sxs-lookup"><span data-stu-id="bbe96-116">This example create a virtual network with two subnets and two DNS servers.</span></span> <span data-ttu-id="bbe96-117">A DNS-kiszolgálók virtuális hálózaton való megadásának hatásai az, hogy a virtuális hálózatba telepített hálózati adapterek/VMs-kiszolgálók alapértelmezés szerint öröklik ezeket a DNS-kiszolgálókat.</span><span class="sxs-lookup"><span data-stu-id="bbe96-117">The effect of specifying the DNS servers on the virtual network is that the NICs/VMs that are deployed into this virtual network inherit these DNS servers as defaults.</span></span> <span data-ttu-id="bbe96-118">Ezek az alapértelmezett beállítások a NIC-es hálózati adapteren keresztül felülíródnak.</span><span class="sxs-lookup"><span data-stu-id="bbe96-118">These defaults can be overwritten per NIC through a NIC-level setting.</span></span> <span data-ttu-id="bbe96-119">Ha a VNET nem ad meg DNS-kiszolgálókat, és nem a hálózati adaptereken, akkor az alapértelmezett Azure DNS-kiszolgálók használhatók a DNS-feloldáshoz.</span><span class="sxs-lookup"><span data-stu-id="bbe96-119">If no DNS servers are specified on a VNET and no DNS servers on the NICs, then the default Azure DNS servers are used for DNS resolution.</span></span>

### <span data-ttu-id="bbe96-120">3: virtuális hálózat létrehozása hálózati biztonsági csoportra hivatkozó alhálózattal</span><span class="sxs-lookup"><span data-stu-id="bbe96-120">3: Create a virtual network with a subnet referencing a network security group</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
$rdpRule              = New-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
$networkSecurityGroup = New-AzureRmNetworkSecurityGroup -ResourceGroupName TestResourceGroup -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule
$frontendSubnet       = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup
$backendSubnet        = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup
New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="bbe96-121">Ez a példa virtuális hálózatot hoz létre olyan alhálózatokkal, amelyek hálózati biztonsági csoportra hivatkoznak.</span><span class="sxs-lookup"><span data-stu-id="bbe96-121">This example creates a virtual network with subnets that reference a network security group.</span></span> <span data-ttu-id="bbe96-122">Először a példa létrehoz egy erőforráscsoportot tárolóként a létrehozandó erőforrásokhoz.</span><span class="sxs-lookup"><span data-stu-id="bbe96-122">First, the example creates a resource group as a container for the resources that will be created.</span></span> <span data-ttu-id="bbe96-123">Ezután egy hálózati biztonsági csoport jön létre, amely lehetővé teszi a bejövő RDP-elérést, de egyéb módon kényszeríti az alapértelmezett hálózati biztonsági csoport szabályait.</span><span class="sxs-lookup"><span data-stu-id="bbe96-123">Then, a network security group is created that allows inbound RDP access, but otherwise enforces the default network security group rules.</span></span> <span data-ttu-id="bbe96-124">A New-AzureRmVirtualNetworkSubnetConfig parancsmag két alhálózat memóriában ábrázolt példányait hozza létre, amelyek a létrehozott hálózati biztonsági csoportra hivatkoznak.</span><span class="sxs-lookup"><span data-stu-id="bbe96-124">The New-AzureRmVirtualNetworkSubnetConfig cmdlet then creates in-memory representations of two subnets that both reference the network security group that was created.</span></span> <span data-ttu-id="bbe96-125">A New-AzureRmVirtualNetwork parancs a virtuális hálózatot hozza létre.</span><span class="sxs-lookup"><span data-stu-id="bbe96-125">The New-AzureRmVirtualNetwork command then creates the virtual network.</span></span>

## <span data-ttu-id="bbe96-126">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bbe96-126">PARAMETERS</span></span>

### <span data-ttu-id="bbe96-127">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="bbe96-127">-AddressPrefix</span></span>
<span data-ttu-id="bbe96-128">Egy virtuális hálózat IP-címeinek egy-egy IP-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bbe96-128">Specifies a range of IP addresses for a virtual network.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbe96-129">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bbe96-129">-AsJob</span></span>
<span data-ttu-id="bbe96-130">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="bbe96-130">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bbe96-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbe96-131">-DefaultProfile</span></span>
<span data-ttu-id="bbe96-132">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bbe96-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbe96-133">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="bbe96-133">-DnsServer</span></span>
<span data-ttu-id="bbe96-134">Az alhálózat DNS-kiszolgálóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="bbe96-134">Specifies the DNS server for a subnet.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbe96-135">-EnableDDoSProtection</span><span class="sxs-lookup"><span data-stu-id="bbe96-135">-EnableDDoSProtection</span></span>
<span data-ttu-id="bbe96-136">Egy kapcsoló paraméter, amely akkor jelenik meg, ha a DDoS védelem engedélyezve van vagy nem.</span><span class="sxs-lookup"><span data-stu-id="bbe96-136">A switch parameter which represents if DDoS protection is enabled or not.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbe96-137">-EnableVmProtection</span><span class="sxs-lookup"><span data-stu-id="bbe96-137">-EnableVmProtection</span></span>
<span data-ttu-id="bbe96-138">Kapcsoló paraméter, amely azt jelzi, hogy engedélyezve van-e a VM-védelem.</span><span class="sxs-lookup"><span data-stu-id="bbe96-138">A switch parameter which represents if Vm protection is enabled or not.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbe96-139">-Force</span><span class="sxs-lookup"><span data-stu-id="bbe96-139">-Force</span></span>
<span data-ttu-id="bbe96-140">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="bbe96-140">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bbe96-141">-Hely</span><span class="sxs-lookup"><span data-stu-id="bbe96-141">-Location</span></span>
<span data-ttu-id="bbe96-142">A virtuális hálózat területét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bbe96-142">Specifies the region for the virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbe96-143">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bbe96-143">-Name</span></span>
<span data-ttu-id="bbe96-144">Annak a virtuális hálózatnak a neve, amelyet a parancsmag hoz létre.</span><span class="sxs-lookup"><span data-stu-id="bbe96-144">Specifies the name of the virtual network that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbe96-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbe96-145">-ResourceGroupName</span></span>
<span data-ttu-id="bbe96-146">A virtuális hálózatot tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bbe96-146">Specifies the name of a resource group to contain the virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbe96-147">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="bbe96-147">-Subnet</span></span>
<span data-ttu-id="bbe96-148">A virtuális hálózattal társítani kívánt alhálózatok listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="bbe96-148">Specifies a list of subnets to associate with the virtual network.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSSubnet]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbe96-149">-Címke</span><span class="sxs-lookup"><span data-stu-id="bbe96-149">-Tag</span></span>
<span data-ttu-id="bbe96-150">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="bbe96-150">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="bbe96-151">Példa:</span><span class="sxs-lookup"><span data-stu-id="bbe96-151">For example:</span></span>

<span data-ttu-id="bbe96-152">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="bbe96-152">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbe96-153">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bbe96-153">-Confirm</span></span>
<span data-ttu-id="bbe96-154">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bbe96-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbe96-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbe96-155">-WhatIf</span></span>
<span data-ttu-id="bbe96-156">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bbe96-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbe96-157">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bbe96-157">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbe96-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbe96-158">CommonParameters</span></span>
<span data-ttu-id="bbe96-159">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bbe96-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbe96-160">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbe96-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbe96-161">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bbe96-161">INPUTS</span></span>

### <span data-ttu-id="bbe96-162">Nincs</span><span class="sxs-lookup"><span data-stu-id="bbe96-162">None</span></span>
<span data-ttu-id="bbe96-163">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="bbe96-163">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bbe96-164">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bbe96-164">OUTPUTS</span></span>

### <span data-ttu-id="bbe96-165">Microsoft. Azure. commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="bbe96-165">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="bbe96-166">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bbe96-166">NOTES</span></span>

## <span data-ttu-id="bbe96-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bbe96-167">RELATED LINKS</span></span>

[<span data-ttu-id="bbe96-168">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="bbe96-168">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="bbe96-169">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="bbe96-169">Remove-AzureRmVirtualNetwork</span></span>](./Remove-AzureRmVirtualNetwork.md)

[<span data-ttu-id="bbe96-170">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="bbe96-170">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)
