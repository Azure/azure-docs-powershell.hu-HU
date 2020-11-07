---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DDB38A77-E5C0-47DD-BADD-94488F661CD5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterface.md
ms.openlocfilehash: e7deb8cb72d09bf4d9ffb543ca60bc6359ab71d2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669995"
---
# <span data-ttu-id="dd550-101">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="dd550-101">Set-AzNetworkInterface</span></span>

## <span data-ttu-id="dd550-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dd550-102">SYNOPSIS</span></span>
<span data-ttu-id="dd550-103">Hálózati felület frissítése</span><span class="sxs-lookup"><span data-stu-id="dd550-103">Updates a network interface.</span></span>

## <span data-ttu-id="dd550-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dd550-104">SYNTAX</span></span>

```
Set-AzNetworkInterface -NetworkInterface <PSNetworkInterface> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd550-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="dd550-105">DESCRIPTION</span></span>
<span data-ttu-id="dd550-106">A **set-AzNetworkInterface** frissíti a hálózati felületet.</span><span class="sxs-lookup"><span data-stu-id="dd550-106">The **Set-AzNetworkInterface** updates a network interface.</span></span>

## <span data-ttu-id="dd550-107">Példák</span><span class="sxs-lookup"><span data-stu-id="dd550-107">EXAMPLES</span></span>

### <span data-ttu-id="dd550-108">1. példa: hálózati felület beállítása</span><span class="sxs-lookup"><span data-stu-id="dd550-108">Example 1: Configure a network interface</span></span>
```
$Nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$Nic.IpConfigurations[0].PrivateIpAddress = "10.0.1.20"
$Nic.IpConfigurations[0].PrivateIpAllocationMethod = "Static"
$Nic.Tag = @{Name = "Name"; Value = "Value"}
Set-AzNetworkInterface -NetworkInterface $Nic
```

<span data-ttu-id="dd550-109">Ez a példa hálózati felületet konfigurál.</span><span class="sxs-lookup"><span data-stu-id="dd550-109">This example configures a network interface.</span></span>
<span data-ttu-id="dd550-110">Az első parancs a NetworkInterface1 nevű hálózati felületet kapja az erőforráscsoport ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="dd550-110">The first command gets a network interface named NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="dd550-111">A második parancs az IP-konfiguráció privát IP-címét állítja be.</span><span class="sxs-lookup"><span data-stu-id="dd550-111">The second command sets the private IP address of the IP configuration.</span></span>
<span data-ttu-id="dd550-112">A harmadik parancs a privát IP-kiosztási módszert a statikus értékre állítja.</span><span class="sxs-lookup"><span data-stu-id="dd550-112">The third command sets the private IP allocation method to Static.</span></span>
<span data-ttu-id="dd550-113">A negyedik parancs a hálózati felületen címkét állít be.</span><span class="sxs-lookup"><span data-stu-id="dd550-113">The fourth command sets a tag on the network interface.</span></span>
<span data-ttu-id="dd550-114">Az ötödik parancs a $Nic változóban tárolt információkat használja a hálózati felület beállításához.</span><span class="sxs-lookup"><span data-stu-id="dd550-114">The fifth command uses the information stored in the $Nic variable to set the network interface.</span></span>

### <span data-ttu-id="dd550-115">2. példa: a DNS-beállítások módosítása hálózati felületen</span><span class="sxs-lookup"><span data-stu-id="dd550-115">Example 2: Change DNS settings on a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.DnsSettings.DnsServers.Add("192.168.1.100")
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="dd550-116">Az első parancs a NetworkInterface1 nevű hálózati felületet kapja, amely az erőforráscsoport ResourceGroup1 található.</span><span class="sxs-lookup"><span data-stu-id="dd550-116">The first command gets a network interface named NetworkInterface1 that exists within resource group ResourceGroup1.</span></span> <span data-ttu-id="dd550-117">A második parancs hozzáadja a DNS Server 192.168.1.100 az interfészhez.</span><span class="sxs-lookup"><span data-stu-id="dd550-117">The second command adds DNS server 192.168.1.100 to this interface.</span></span> <span data-ttu-id="dd550-118">A harmadik parancs ezeket a módosításokat alkalmazza a hálózati felületen.</span><span class="sxs-lookup"><span data-stu-id="dd550-118">The third command applies these changes to the network interface.</span></span> <span data-ttu-id="dd550-119">Ha el szeretne távolítani egy DNS-kiszolgálót, kövesse a fenti, de a csere "parancsot. Adja hozzá a "with" szót. "A második parancs" eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="dd550-119">To remove a DNS server, follow the commands listed above, but replace ".Add" with ".Remove" in the second command.</span></span>

### <span data-ttu-id="dd550-120">3. példa: az IP-forwading engedélyezése hálózati felületen</span><span class="sxs-lookup"><span data-stu-id="dd550-120">Example 3: Enable IP forwading on a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.EnableIPForwarding = 1
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="dd550-121">Az első parancs a NetworkInterface1 nevű meglévő hálózati felületet kapja, és a $nic változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="dd550-121">The first command gets an existing network interface called NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="dd550-122">A második parancs az IP-továbbítás értékét True értékre módosítja.</span><span class="sxs-lookup"><span data-stu-id="dd550-122">The second command changes the IP forwarding value to true.</span></span> <span data-ttu-id="dd550-123">Végül a harmadik parancs alkalmazza a módosításokat a hálózati felületen.</span><span class="sxs-lookup"><span data-stu-id="dd550-123">Finally, the third command applies the changes to the network interface.</span></span> <span data-ttu-id="dd550-124">Ha le szeretné tiltani az IP-továbbítást egy hálózati kapcsolaton, kövesse a minta példáját, de mindenképpen módosítsa a második parancsot "$nic. EnableIPForwarding = 0 ".</span><span class="sxs-lookup"><span data-stu-id="dd550-124">To disable IP forwarding on a network interface, follow the sample example, but be sure to change the second command to "$nic.EnableIPForwarding = 0".</span></span>

### <span data-ttu-id="dd550-125">4. példa: egy hálózati kapcsolat alhálózatának módosítása</span><span class="sxs-lookup"><span data-stu-id="dd550-125">Example 4: Change the subnet of a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$vnet = Get-AzVirtualNetwork -Name VNet1 -ResourceGroupName crosssubcrossversionpeering
$subnet2 = Get-AzVirtualNetworkSubnetConfig -Name Subnet2 -VirtualNetwork $vnet
$nic.IpConfigurations[0].Subnet.Id = $subnet2.Id
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="dd550-126">Az első parancs megkapja a hálózati felületet, és a $nic változóban tárolja a NetworkInterface1.</span><span class="sxs-lookup"><span data-stu-id="dd550-126">The first command gets the network interface NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="dd550-127">A második parancs az alhálózathoz társított virtuális hálózatot kapja meg, amelyhez a hálózati csatoló van társítva.</span><span class="sxs-lookup"><span data-stu-id="dd550-127">The second command gets the virtual network associated with the subnet that the network interface is going to be associated with.</span></span> <span data-ttu-id="dd550-128">A második parancs az alhálózatot kapja, és a $subnet 2 változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="dd550-128">The second command gets the subnet and stores it in the $subnet2 variable.</span></span> <span data-ttu-id="dd550-129">A harmadik parancs az új alhálózat hálózati felületének elsődleges magánhálózati IP-címével társítva.</span><span class="sxs-lookup"><span data-stu-id="dd550-129">The third command associated the primary private IP address of the network interface with the new subnet.</span></span> <span data-ttu-id="dd550-130">Végül az utolsó parancs alkalmazza ezeket a módosításokat a hálózati felületen.</span><span class="sxs-lookup"><span data-stu-id="dd550-130">Finally the last command applied these changes on the network interface.</span></span>
>[!NOTE] 
><span data-ttu-id="dd550-131">Az IP-konfigurációnak dinamikusan kell lennie ahhoz, hogy módosítani tudja az alhálózatot.</span><span class="sxs-lookup"><span data-stu-id="dd550-131">The IP configurations must be dynamic before you can change the subnet.</span></span> <span data-ttu-id="dd550-132">Ha statikus IP-konfigurációval rendelkezik, a folytatás előtt módosítsa majd a dinamikus értékre.</span><span class="sxs-lookup"><span data-stu-id="dd550-132">If you have static IP configurations, change then to dynamic before proceeding.</span></span> 
>[!NOTE]
><span data-ttu-id="dd550-133">Ha a hálózati felület több IP-konfigurációval rendelkezik, a tovább parancsot minden IP-konfigurációnál el kell végeznie, mielőtt végrehajtja a végleges Set-AzNetworkInterface parancsot.</span><span class="sxs-lookup"><span data-stu-id="dd550-133">If the network interface has multiple IP configurations, the forth command must be done for all these IP configurations before the final Set-AzNetworkInterface command is executed.</span></span> <span data-ttu-id="dd550-134">Ezt úgy teheti meg, mint a Forth parancsban, de a "0" helyett a megfelelő számra cseréli.</span><span class="sxs-lookup"><span data-stu-id="dd550-134">This can be done as in the forth command but by replacing "0" with the appropriate number.</span></span> <span data-ttu-id="dd550-135">Ha egy hálózati kapcsolat N IP-konfigurációval rendelkezik, a fenti parancsok N-1-nek léteznie kell.</span><span class="sxs-lookup"><span data-stu-id="dd550-135">If a network interface has N IP configurations, then N-1 of these commands must exist.</span></span>

### <span data-ttu-id="dd550-136">Példa 5: hálózat biztonsági csoportjának társítása és szétválasztása hálózati kapcsolattal</span><span class="sxs-lookup"><span data-stu-id="dd550-136">Example 5: Associate/Dissociate a Network Security Group to a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nsg = Get-AzNetworkSecurityGroup -ResourceGroupName "ResourceGroup1" -Name "MyNSG"
$nic.NetworkSecurityGroup = $nsg
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="dd550-137">Az első parancs a NetworkInterface1 nevű meglévő hálózati felületet kapja, és a $nic változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="dd550-137">The first command gets an existing network interface called NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="dd550-138">A második parancs a MyNSG nevű meglévő hálózati biztonsági csoportot kapja meg, és a $nsg változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="dd550-138">The second command gets an existing network security group called MyNSG and stores it in the $nsg variable.</span></span> <span data-ttu-id="dd550-139">A harmadik parancs a $nichez rendeli a $nsgt.</span><span class="sxs-lookup"><span data-stu-id="dd550-139">The third command assigns the $nsg to the $nic.</span></span> <span data-ttu-id="dd550-140">Végül a Forth parancs alkalmazza a módosításokat a hálózati felületen.</span><span class="sxs-lookup"><span data-stu-id="dd550-140">Finally, the forth command applies the changes to the Network interface.</span></span> <span data-ttu-id="dd550-141">Ha hálózati felületen szeretné szétválasztani a hálózat biztonsági csoportjait, a harmadik parancsban egyszerűen cserélje $nsgt a $null.</span><span class="sxs-lookup"><span data-stu-id="dd550-141">To dissociate network security groups from a network interface, simple replace $nsg in the third command with $null.</span></span>

## <span data-ttu-id="dd550-142">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dd550-142">PARAMETERS</span></span>

### <span data-ttu-id="dd550-143">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dd550-143">-AsJob</span></span>
<span data-ttu-id="dd550-144">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="dd550-144">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd550-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd550-145">-DefaultProfile</span></span>
<span data-ttu-id="dd550-146">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dd550-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd550-147">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="dd550-147">-NetworkInterface</span></span>
<span data-ttu-id="dd550-148">Egy olyan hálózati kapcsolat objektum, amely a hálózati felületet tartalmazó állapotot adja meg.</span><span class="sxs-lookup"><span data-stu-id="dd550-148">Specifies a network interface object representing the state to which the network interface should be set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterface
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd550-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd550-149">CommonParameters</span></span>
<span data-ttu-id="dd550-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dd550-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd550-151">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd550-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd550-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dd550-152">INPUTS</span></span>

### <span data-ttu-id="dd550-153">Microsoft. Azure. commands. Network. models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="dd550-153">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="dd550-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dd550-154">OUTPUTS</span></span>

### <span data-ttu-id="dd550-155">Microsoft. Azure. commands. Network. models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="dd550-155">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="dd550-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dd550-156">NOTES</span></span>

## <span data-ttu-id="dd550-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dd550-157">RELATED LINKS</span></span>

[<span data-ttu-id="dd550-158">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="dd550-158">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="dd550-159">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="dd550-159">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="dd550-160">Új – AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="dd550-160">New-AzNetworkInterface</span></span>](./New-AzNetworkInterface.md)

[<span data-ttu-id="dd550-161">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="dd550-161">Remove-AzNetworkInterface</span></span>](./Remove-AzNetworkInterface.md)
