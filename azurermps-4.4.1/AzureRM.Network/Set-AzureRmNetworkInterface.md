---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DDB38A77-E5C0-47DD-BADD-94488F661CD5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkInterface.md
ms.openlocfilehash: 8403a2e26bbc149db35c9c20cdea3075adb88492
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494807"
---
# <span data-ttu-id="810e9-101">Set-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="810e9-101">Set-AzureRmNetworkInterface</span></span>

## <span data-ttu-id="810e9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="810e9-102">SYNOPSIS</span></span>
<span data-ttu-id="810e9-103">Egy hálózati kapcsolat cél állapotának beállítása.</span><span class="sxs-lookup"><span data-stu-id="810e9-103">Sets the goal state for a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="810e9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="810e9-104">SYNTAX</span></span>

```
Set-AzureRmNetworkInterface -NetworkInterface <PSNetworkInterface> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="810e9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="810e9-105">DESCRIPTION</span></span>
<span data-ttu-id="810e9-106">A **set-AzureRmNetworkInterface** az Azure-hálózati kapcsolat céljának állapotát állítja be.</span><span class="sxs-lookup"><span data-stu-id="810e9-106">The **Set-AzureRmNetworkInterface** sets the goal state for an Azure network interface.</span></span>

## <span data-ttu-id="810e9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="810e9-107">EXAMPLES</span></span>

### <span data-ttu-id="810e9-108">1. példa: hálózati felület beállítása</span><span class="sxs-lookup"><span data-stu-id="810e9-108">Example 1: Configure a network interface</span></span>
```
$Nic = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$Nic.IpConfigurations[0].PrivateIpAddress = "10.0.1.20"
$Nic.IpConfigurations[0].PrivateIpAllocationMethod = "Static"
$Nic.Tag = @{Name = "Name"; Value = "Value"}
Set-AzureRmNetworkInterface -NetworkInterface $Nic
```

<span data-ttu-id="810e9-109">Ez a példa hálózati felületet konfigurál.</span><span class="sxs-lookup"><span data-stu-id="810e9-109">This example configures a network interface.</span></span>
<span data-ttu-id="810e9-110">Az első parancs a NetworkInterface1 nevű hálózati felületet kapja az erőforráscsoport ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="810e9-110">The first command gets a network interface named NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="810e9-111">A második parancs az IP-konfiguráció privát IP-címét állítja be.</span><span class="sxs-lookup"><span data-stu-id="810e9-111">The second command sets the private IP address of the IP configuration.</span></span>
<span data-ttu-id="810e9-112">A harmadik parancs a privát IP-kiosztási módszert a statikus értékre állítja.</span><span class="sxs-lookup"><span data-stu-id="810e9-112">The third command sets the private IP allocation method to Static.</span></span>
<span data-ttu-id="810e9-113">A negyedik parancs a hálózati felületen címkét állít be.</span><span class="sxs-lookup"><span data-stu-id="810e9-113">The fourth command sets a tag on the network interface.</span></span>
<span data-ttu-id="810e9-114">Az ötödik parancs a $Nic változóban tárolt információkat használja a hálózati felület beállításához.</span><span class="sxs-lookup"><span data-stu-id="810e9-114">The fifth command uses the information stored in the $Nic variable to set the network interface.</span></span>

### <span data-ttu-id="810e9-115">2. példa: a DNS-beállítások módosítása hálózati felületen</span><span class="sxs-lookup"><span data-stu-id="810e9-115">Example 2: Change DNS settings on a network interface</span></span>
```
$nic = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.DnsSettings.DnsServers.Add("192.168.1.100")
$nic | Set-AzureRmNetworkInterface
```

<span data-ttu-id="810e9-116">Az első parancs a NetworkInterface1 nevű hálózati felületet kapja, amely az erőforráscsoport ResourceGroup1 található.</span><span class="sxs-lookup"><span data-stu-id="810e9-116">The first command gets a network interface named NetworkInterface1 that exists within resource group ResourceGroup1.</span></span> <span data-ttu-id="810e9-117">A második parancs hozzáadja a DNS Server 192.168.1.100 az interfészhez.</span><span class="sxs-lookup"><span data-stu-id="810e9-117">The second command adds DNS server 192.168.1.100 to this interface.</span></span> <span data-ttu-id="810e9-118">A harmadik parancs ezeket a módosításokat alkalmazza a hálózati felületen.</span><span class="sxs-lookup"><span data-stu-id="810e9-118">The third command applies these changes to the network interface.</span></span> <span data-ttu-id="810e9-119">Ha el szeretne távolítani egy DNS-kiszolgálót, kövesse a fenti, de a csere "parancsot. Adja hozzá a "with" szót. "A második parancs" eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="810e9-119">To remove a DNS server, follow the commands listed above, but replace ".Add" with ".Remove" in the second command.</span></span>

### <span data-ttu-id="810e9-120">3. példa: az IP-forwading engedélyezése hálózati felületen</span><span class="sxs-lookup"><span data-stu-id="810e9-120">Example 3: Enable IP forwading on a network interface</span></span>
```
$nic = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.EnableIPForwarding = 1
$nic | Set-AzureRmNetworkInterface
```

<span data-ttu-id="810e9-121">Az első parancs a NetworkInterface1 nevű meglévő hálózati felületet kapja, és a $nic változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="810e9-121">The first command gets an existing network interface called NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="810e9-122">A második parancs az IP-továbbítás értékét True értékre módosítja.</span><span class="sxs-lookup"><span data-stu-id="810e9-122">The second command changes the IP forwarding value to true.</span></span> <span data-ttu-id="810e9-123">Végül a harmadik parancs alkalmazza a módosításokat a hálózati felületen.</span><span class="sxs-lookup"><span data-stu-id="810e9-123">Finally, the third command applies the changes to the network interface.</span></span> <span data-ttu-id="810e9-124">Ha le szeretné tiltani az IP-továbbítást egy hálózati kapcsolaton, kövesse a minta példáját, de mindenképpen módosítsa a második parancsot "$nic. EnableIPForwarding = 0 ".</span><span class="sxs-lookup"><span data-stu-id="810e9-124">To disable IP forwarding on a network interface, follow the sample example, but be sure to change the second command to "$nic.EnableIPForwarding = 0".</span></span>

### <span data-ttu-id="810e9-125">4. példa: egy hálózati kapcsolat alhálózatának módosítása</span><span class="sxs-lookup"><span data-stu-id="810e9-125">Example 4: Change the subnet of a network interface</span></span>
```
$nic = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$vnet = Get-AzureRmVirtualNetwork -Name VNet1 -ResourceGroupName crosssubcrossversionpeering
$subnet2 = Get-AzureRmVirtualNetworkSubnetConfig -Name Subnet2 -VirtualNetwork $vnet
$nic.IpConfigurations[0].Subnet.Id = $subnet2.Id
$nic | Set-AzureRmNetworkInterface
```

<span data-ttu-id="810e9-126">Az első parancs megkapja a hálózati felületet, és a $nic változóban tárolja a NetworkInterface1.</span><span class="sxs-lookup"><span data-stu-id="810e9-126">The first command gets the network interface NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="810e9-127">A második parancs az alhálózathoz társított virtuális hálózatot kapja meg, amelyhez a hálózati csatoló van társítva.</span><span class="sxs-lookup"><span data-stu-id="810e9-127">The second command gets the virtual network associated with the subnet that the network interface is going to be associated with.</span></span> <span data-ttu-id="810e9-128">A második parancs az alhálózatot kapja, és a $subnet 2 változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="810e9-128">The second command gets the subnet and stores it in the $subnet2 variable.</span></span> <span data-ttu-id="810e9-129">A harmadik parancs az új alhálózat hálózati felületének elsődleges magánhálózati IP-címével társítva.</span><span class="sxs-lookup"><span data-stu-id="810e9-129">The third command associated the primary private IP address of the network interface with the new subnet.</span></span> <span data-ttu-id="810e9-130">Végül az utolsó parancs alkalmazza ezeket a módosításokat a hálózati felületen.</span><span class="sxs-lookup"><span data-stu-id="810e9-130">Finally the last command applied these changes on the network interface.</span></span>

>[!NOTE] 
><span data-ttu-id="810e9-131">Az IP-konfigurációnak dinamikusan kell lennie ahhoz, hogy módosítani tudja az alhálózatot.</span><span class="sxs-lookup"><span data-stu-id="810e9-131">The IP configurations must be dynamic before you can change the subnet.</span></span> <span data-ttu-id="810e9-132">Ha statikus IP-konfigurációval rendelkezik, a folytatás előtt módosítsa majd a dinamikus értékre.</span><span class="sxs-lookup"><span data-stu-id="810e9-132">If you have static IP configurations, change then to dynamic before proceeding.</span></span> 

>[!NOTE]
><span data-ttu-id="810e9-133">Ha a hálózati felület több IP-konfigurációval rendelkezik, a tovább parancsot minden IP-konfigurációnál el kell végeznie, mielőtt végrehajtja a végleges Set-AzureRmNetworkInterface parancsot.</span><span class="sxs-lookup"><span data-stu-id="810e9-133">If the network interface has multiple IP configurations, the forth command must be done for all these IP configurations before the final Set-AzureRmNetworkInterface command is executed.</span></span> <span data-ttu-id="810e9-134">Ezt úgy teheti meg, mint a Forth parancsban, de a "0" helyett a megfelelő számra cseréli.</span><span class="sxs-lookup"><span data-stu-id="810e9-134">This can be done as in the forth command but by replacing "0" with the appropriate number.</span></span> <span data-ttu-id="810e9-135">Ha egy hálózati kapcsolat N IP-konfigurációval rendelkezik, a fenti parancsok N-1-nek léteznie kell.</span><span class="sxs-lookup"><span data-stu-id="810e9-135">If a network interface has N IP configurations, then N-1 of these commands must exist.</span></span>

### <span data-ttu-id="810e9-136">Példa 5: hálózat biztonsági csoportjának társítása és szétválasztása hálózati kapcsolattal</span><span class="sxs-lookup"><span data-stu-id="810e9-136">Example 5: Associate/Dissociate a Network Security Group to a network interface</span></span>
```
$nic = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nsg = Get-AzureRmNetworkSecurityGroup -ResourceGroupName "ResourceGroup1" -Name "MyNSG"
$nic.NetworkSecurityGroup = $nsg
$nic | Set-AzureRmNetworkInterface
```

<span data-ttu-id="810e9-137">Az első parancs a NetworkInterface1 nevű meglévő hálózati felületet kapja, és a $nic változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="810e9-137">The first command gets an existing network interface called NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="810e9-138">A második parancs a MyNSG nevű meglévő hálózati biztonsági csoportot kapja meg, és a $nsg változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="810e9-138">The second command gets an existing network security group called MyNSG and stores it in the $nsg variable.</span></span> <span data-ttu-id="810e9-139">A Forth parancs a $nsgt a $nichez rendeli.</span><span class="sxs-lookup"><span data-stu-id="810e9-139">The forth command assigns the $nsg to the $nic.</span></span> <span data-ttu-id="810e9-140">Végül az ötödik parancs alkalmazza a módosításokat a hálózati felületen.</span><span class="sxs-lookup"><span data-stu-id="810e9-140">Finally, the fifth command applies the changes to the Network interface.</span></span> <span data-ttu-id="810e9-141">Ha hálózati felületen szeretné szétválasztani a hálózat biztonsági csoportjait, egyszerűen cserélje $nsg a Forth parancsra $null segítségével.</span><span class="sxs-lookup"><span data-stu-id="810e9-141">To dissociate network security groups from a network interface, simple replace $nsg in the forth command with $null.</span></span>

## <span data-ttu-id="810e9-142">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="810e9-142">PARAMETERS</span></span>

### <span data-ttu-id="810e9-143">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="810e9-143">-NetworkInterface</span></span>
<span data-ttu-id="810e9-144">Itt adhatja meg azt a **NetworkInterface** -objektumot, amely egy hálózati kapcsolat céljának állapotát jelképezi.</span><span class="sxs-lookup"><span data-stu-id="810e9-144">Specifies a **NetworkInterface** object that represents the goal state for a network interface.</span></span>

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

### <span data-ttu-id="810e9-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="810e9-145">-DefaultProfile</span></span>
<span data-ttu-id="810e9-146">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="810e9-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="810e9-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="810e9-147">CommonParameters</span></span>
<span data-ttu-id="810e9-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="810e9-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="810e9-149">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="810e9-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="810e9-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="810e9-150">INPUTS</span></span>

### <span data-ttu-id="810e9-151">PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="810e9-151">PSNetworkInterface</span></span>
<span data-ttu-id="810e9-152">A ' NetworkInterface ' paraméter az "PSNetworkInterface" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="810e9-152">Parameter 'NetworkInterface' accepts value of type 'PSNetworkInterface' from the pipeline</span></span>

## <span data-ttu-id="810e9-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="810e9-153">OUTPUTS</span></span>

### <span data-ttu-id="810e9-154">Microsoft. Azure. commands. Network. models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="810e9-154">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="810e9-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="810e9-155">NOTES</span></span>

## <span data-ttu-id="810e9-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="810e9-156">RELATED LINKS</span></span>

[<span data-ttu-id="810e9-157">Get-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="810e9-157">Get-AzureRmNetworkInterface</span></span>](./Get-AzureRmNetworkInterface.md)

[<span data-ttu-id="810e9-158">Get-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="810e9-158">Get-AzureRmNetworkInterface</span></span>](./Get-AzureRmNetworkInterface.md)

[<span data-ttu-id="810e9-159">Új – AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="810e9-159">New-AzureRmNetworkInterface</span></span>](./New-AzureRmNetworkInterface.md)

[<span data-ttu-id="810e9-160">Remove-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="810e9-160">Remove-AzureRmNetworkInterface</span></span>](./Remove-AzureRmNetworkInterface.md)
