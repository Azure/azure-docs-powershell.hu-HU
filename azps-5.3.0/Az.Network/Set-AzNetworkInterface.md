---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DDB38A77-E5C0-47DD-BADD-94488F661CD5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterface.md
ms.openlocfilehash: 9b851bcbaa545dee99628dc066956854181df7f7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98481134"
---
# <span data-ttu-id="68489-101">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="68489-101">Set-AzNetworkInterface</span></span>

## <span data-ttu-id="68489-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68489-102">SYNOPSIS</span></span>
<span data-ttu-id="68489-103">Frissíti a hálózati felületet.</span><span class="sxs-lookup"><span data-stu-id="68489-103">Updates a network interface.</span></span>

## <span data-ttu-id="68489-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="68489-104">SYNTAX</span></span>

```
Set-AzNetworkInterface -NetworkInterface <PSNetworkInterface> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68489-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="68489-105">DESCRIPTION</span></span>
<span data-ttu-id="68489-106">A **Set-AzNetworkInterface** frissíti a hálózati felületet.</span><span class="sxs-lookup"><span data-stu-id="68489-106">The **Set-AzNetworkInterface** updates a network interface.</span></span>

## <span data-ttu-id="68489-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="68489-107">EXAMPLES</span></span>

### <span data-ttu-id="68489-108">1. példa: Hálózati felület beállítása</span><span class="sxs-lookup"><span data-stu-id="68489-108">Example 1: Configure a network interface</span></span>
```
$Nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$Nic.IpConfigurations[0].PrivateIpAddress = "10.0.1.20"
$Nic.IpConfigurations[0].PrivateIpAllocationMethod = "Static"
$Nic.Tag = @{Name = "Name"; Value = "Value"}
Set-AzNetworkInterface -NetworkInterface $Nic
```

<span data-ttu-id="68489-109">Ez a példa hálózati felületet konfigurál.</span><span class="sxs-lookup"><span data-stu-id="68489-109">This example configures a network interface.</span></span>
<span data-ttu-id="68489-110">Az első parancs egy NetworkInterface1 nevű hálózati felületet kap az ResourceGroup1 erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="68489-110">The first command gets a network interface named NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="68489-111">A második parancs beállítja az IP-konfiguráció privát IP-címét.</span><span class="sxs-lookup"><span data-stu-id="68489-111">The second command sets the private IP address of the IP configuration.</span></span>
<span data-ttu-id="68489-112">A harmadik parancs statikusra állítja a privát IP-terhelési módot.</span><span class="sxs-lookup"><span data-stu-id="68489-112">The third command sets the private IP allocation method to Static.</span></span>
<span data-ttu-id="68489-113">A negyedik parancs címkét állít be a hálózati felületen.</span><span class="sxs-lookup"><span data-stu-id="68489-113">The fourth command sets a tag on the network interface.</span></span>
<span data-ttu-id="68489-114">Az ötödik parancs a $Nic változóban tárolt információkat használja a hálózati felület beállításához.</span><span class="sxs-lookup"><span data-stu-id="68489-114">The fifth command uses the information stored in the $Nic variable to set the network interface.</span></span>

### <span data-ttu-id="68489-115">2. példa: A DNS-beállítások módosítása hálózati felületen</span><span class="sxs-lookup"><span data-stu-id="68489-115">Example 2: Change DNS settings on a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.DnsSettings.DnsServers.Add("192.168.1.100")
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="68489-116">Az első parancs egy NetworkInterface1 nevű hálózati felületet kap, amely az ResourceGroup1 erőforráscsoportban található.</span><span class="sxs-lookup"><span data-stu-id="68489-116">The first command gets a network interface named NetworkInterface1 that exists within resource group ResourceGroup1.</span></span> <span data-ttu-id="68489-117">A második parancs ezen a felületen hozzáadja a 192.168.1.100-as DNS-kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="68489-117">The second command adds DNS server 192.168.1.100 to this interface.</span></span> <span data-ttu-id="68489-118">A harmadik parancs ezeket a módosításokat a hálózati felületre alkalmazza.</span><span class="sxs-lookup"><span data-stu-id="68489-118">The third command applies these changes to the network interface.</span></span> <span data-ttu-id="68489-119">DNS-kiszolgáló eltávolításához kövesse a fent felsorolt parancsokat, de cserélje le a ". Add" with ". Remove" (Eltávolítás) gombra a második parancsban.</span><span class="sxs-lookup"><span data-stu-id="68489-119">To remove a DNS server, follow the commands listed above, but replace ".Add" with ".Remove" in the second command.</span></span>

### <span data-ttu-id="68489-120">3. példa: IP-továbbítás engedélyezése hálózati felületen</span><span class="sxs-lookup"><span data-stu-id="68489-120">Example 3: Enable IP forwarding on a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.EnableIPForwarding = 1
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="68489-121">Az első parancs egy NetworkInterface1 nevű meglévő hálózati felületet kap, és azt egy másik változóban $nic tárolja.</span><span class="sxs-lookup"><span data-stu-id="68489-121">The first command gets an existing network interface called NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="68489-122">A második parancs igazra módosítja az IP-továbbítás értékét.</span><span class="sxs-lookup"><span data-stu-id="68489-122">The second command changes the IP forwarding value to true.</span></span> <span data-ttu-id="68489-123">Végül a harmadik parancs alkalmazza a módosításokat a hálózati felületen.</span><span class="sxs-lookup"><span data-stu-id="68489-123">Finally, the third command applies the changes to the network interface.</span></span> <span data-ttu-id="68489-124">Ha hálózati felületen szeretné letiltani az IP-továbbítást, kövesse a példát, de a második parancsot mindenképpen módosítsa "$nic. EnableIPForwarding = 0".</span><span class="sxs-lookup"><span data-stu-id="68489-124">To disable IP forwarding on a network interface, follow the sample example, but be sure to change the second command to "$nic.EnableIPForwarding = 0".</span></span>

### <span data-ttu-id="68489-125">4. példa: Hálózati felület alhálózatának módosítása</span><span class="sxs-lookup"><span data-stu-id="68489-125">Example 4: Change the subnet of a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$vnet = Get-AzVirtualNetwork -Name VNet1 -ResourceGroupName crosssubcrossversionpeering
$subnet2 = Get-AzVirtualNetworkSubnetConfig -Name Subnet2 -VirtualNetwork $vnet
$nic.IpConfigurations[0].Subnet.Id = $subnet2.Id
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="68489-126">Az első parancs a NetworkInterface1 hálózati felületet kapja meg, és a $nic tárolja.</span><span class="sxs-lookup"><span data-stu-id="68489-126">The first command gets the network interface NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="68489-127">A második parancs annak az alhálózatnak a virtuális hálózatát kapja meg, amelyhez a hálózati felület társítva lesz.</span><span class="sxs-lookup"><span data-stu-id="68489-127">The second command gets the virtual network associated with the subnet that the network interface is going to be associated with.</span></span> <span data-ttu-id="68489-128">A második parancs az alhálózatot a $subnet 2 változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="68489-128">The second command gets the subnet and stores it in the $subnet2 variable.</span></span> <span data-ttu-id="68489-129">A harmadik parancs a hálózati felület elsődleges privát IP-címét társította az új alhálózattal.</span><span class="sxs-lookup"><span data-stu-id="68489-129">The third command associated the primary private IP address of the network interface with the new subnet.</span></span> <span data-ttu-id="68489-130">Végül az utolsó parancs alkalmazta ezeket a módosításokat a hálózati felületen.</span><span class="sxs-lookup"><span data-stu-id="68489-130">Finally the last command applied these changes on the network interface.</span></span>
>[!NOTE] 
><span data-ttu-id="68489-131">Az IP-konfigurációknak dinamikusnak kell lennie az alhálózat módosítása előtt.</span><span class="sxs-lookup"><span data-stu-id="68489-131">The IP configurations must be dynamic before you can change the subnet.</span></span> <span data-ttu-id="68489-132">Ha statikus IP-konfigurációja van, a folytatás előtt váltsa át dinamikusra.</span><span class="sxs-lookup"><span data-stu-id="68489-132">If you have static IP configurations, change then to dynamic before proceeding.</span></span> 
>[!NOTE]
><span data-ttu-id="68489-133">Ha a hálózati felületnek több IP-konfigurációja van, az összes ilyen IP-konfiguráció esetén el kell végeznie a oda-vissza parancsot, mielőtt végrehajtja az Set-AzNetworkInterface parancsot.</span><span class="sxs-lookup"><span data-stu-id="68489-133">If the network interface has multiple IP configurations, the forth command must be done for all these IP configurations before the final Set-AzNetworkInterface command is executed.</span></span> <span data-ttu-id="68489-134">Ezt a "0" helyett a megfelelő számra cserélheti, mint a oda-vissza parancsban.</span><span class="sxs-lookup"><span data-stu-id="68489-134">This can be done as in the forth command but by replacing "0" with the appropriate number.</span></span> <span data-ttu-id="68489-135">Ha egy hálózati felület N IP-konfigurációval rendelkezik, akkor a parancsok közül N-1-nek kell léteznie.</span><span class="sxs-lookup"><span data-stu-id="68489-135">If a network interface has N IP configurations, then N-1 of these commands must exist.</span></span>

### <span data-ttu-id="68489-136">5. példa: Hálózati biztonsági csoport társítása hálózati felülettel</span><span class="sxs-lookup"><span data-stu-id="68489-136">Example 5: Associate/Dissociate a Network Security Group to a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nsg = Get-AzNetworkSecurityGroup -ResourceGroupName "ResourceGroup1" -Name "MyNSG"
$nic.NetworkSecurityGroup = $nsg
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="68489-137">Az első parancs egy NetworkInterface1 nevű meglévő hálózati felületet kap, és azt egy másik változóban $nic tárolja.</span><span class="sxs-lookup"><span data-stu-id="68489-137">The first command gets an existing network interface called NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="68489-138">A második parancs egy MyNSG nevű meglévő hálózatbiztonsági csoportot kap, és azt a $nsg tárolja.</span><span class="sxs-lookup"><span data-stu-id="68489-138">The second command gets an existing network security group called MyNSG and stores it in the $nsg variable.</span></span> <span data-ttu-id="68489-139">A harmadik parancs hozzárendeli a $nsg a $nic.</span><span class="sxs-lookup"><span data-stu-id="68489-139">The third command assigns the $nsg to the $nic.</span></span> <span data-ttu-id="68489-140">Végül a "oda" parancs alkalmazza a módosításokat a Hálózati felületen.</span><span class="sxs-lookup"><span data-stu-id="68489-140">Finally, the forth command applies the changes to the Network interface.</span></span> <span data-ttu-id="68489-141">Ha hálózati felületről származó hálózati biztonsági csoportokat $nsg a harmadik parancsban, cserélje le a $null.</span><span class="sxs-lookup"><span data-stu-id="68489-141">To dissociate network security groups from a network interface, simple replace $nsg in the third command with $null.</span></span>

## <span data-ttu-id="68489-142">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="68489-142">PARAMETERS</span></span>

### <span data-ttu-id="68489-143">-AsJob</span><span class="sxs-lookup"><span data-stu-id="68489-143">-AsJob</span></span>
<span data-ttu-id="68489-144">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="68489-144">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="68489-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68489-145">-DefaultProfile</span></span>
<span data-ttu-id="68489-146">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="68489-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68489-147">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="68489-147">-NetworkInterface</span></span>
<span data-ttu-id="68489-148">Egy hálózati felületi objektumot ad meg, amely azt az állapotot jelzi, amelyben a hálózati felületet be kell állítani.</span><span class="sxs-lookup"><span data-stu-id="68489-148">Specifies a network interface object representing the state to which the network interface should be set.</span></span>

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

### <span data-ttu-id="68489-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68489-149">CommonParameters</span></span>
<span data-ttu-id="68489-150">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68489-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68489-151">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68489-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68489-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="68489-152">INPUTS</span></span>

### <span data-ttu-id="68489-153">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="68489-153">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="68489-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="68489-154">OUTPUTS</span></span>

### <span data-ttu-id="68489-155">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="68489-155">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="68489-156">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="68489-156">NOTES</span></span>

## <span data-ttu-id="68489-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="68489-157">RELATED LINKS</span></span>

[<span data-ttu-id="68489-158">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="68489-158">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="68489-159">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="68489-159">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="68489-160">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="68489-160">New-AzNetworkInterface</span></span>](./New-AzNetworkInterface.md)

[<span data-ttu-id="68489-161">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="68489-161">Remove-AzNetworkInterface</span></span>](./Remove-AzNetworkInterface.md)
