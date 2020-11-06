---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 1A2C843C-6962-4B0E-ACBF-A5EFF609A5BE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmss.md
ms.openlocfilehash: e94cc565c2f22134f6bd4092247fbfa1f5a98b8b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494552"
---
# <span data-ttu-id="7be94-101">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="7be94-101">New-AzureRmVmss</span></span>

## <span data-ttu-id="7be94-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7be94-102">SYNOPSIS</span></span>
<span data-ttu-id="7be94-103">Létrehoz egy VMSS.</span><span class="sxs-lookup"><span data-stu-id="7be94-103">Creates a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7be94-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7be94-104">SYNTAX</span></span>

```
New-AzureRmVmss [-ResourceGroupName] <String> -VMScaleSetName <String>
 [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7be94-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7be94-105">DESCRIPTION</span></span>
<span data-ttu-id="7be94-106">A **New-AzureRmVmss** parancsmag létrehoz egy virtuálisgép-készletet (VMSS) az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="7be94-106">The **New-AzureRmVmss** cmdlet creates a Virtual Machine Scale Set (VMSS) in Azure.</span></span>
<span data-ttu-id="7be94-107">Ez a parancsmag a **VirtualMachineScaleSet** objektumot bemenetként veszi fel.</span><span class="sxs-lookup"><span data-stu-id="7be94-107">This cmdlet takes a **VirtualMachineScaleSet** object as input.</span></span>

## <span data-ttu-id="7be94-108">Példák</span><span class="sxs-lookup"><span data-stu-id="7be94-108">EXAMPLES</span></span>

### <span data-ttu-id="7be94-109">Példa 1: VMSS létrehozása</span><span class="sxs-lookup"><span data-stu-id="7be94-109">Example 1: Create a VMSS</span></span>
```
# Common
$LOC = "WestUs";
$RGName = "rgkyvms";

New-AzureRmResourceGroup -Name $RGName -Location $LOC -Force;

# SRP
$STOName = "STO" + $RGName;
$STOType = "Standard_GRS";
New-AzureRmStorageAccount -ResourceGroupName $RGName -Name $STOName -Location $LOC -Type $STOType;
$STOAccount = Get-AzureRmStorageAccount -ResourceGroupName $RGName -Name $STOName; 

# NRP
$SubNet = New-AzureRmVirtualNetworkSubnetConfig -Name ("subnet" + $RGName) -AddressPrefix "10.0.0.0/24";
$VNet = New-AzureRmVirtualNetwork -Force -Name ("vnet" + $RGName) -ResourceGroupName $RGName -Location $LOC -AddressPrefix "10.0.0.0/16" -DnsServer "10.1.1.1" -Subnet $SubNet;
$VNet = Get-AzureRmVirtualNetwork -Name ('vnet' + $RGName) -ResourceGroupName $RGName;
$SubNetId = $VNet.Subnets[0].Id;

$PubIP = New-AzureRmPublicIpAddress -Force -Name ("PubIP" + $RGName) -ResourceGroupName $RGName -Location $LOC -AllocationMethod Dynamic -DomainNameLabel ("PubIP" + $RGName);
$PubIP = Get-AzureRmPublicIpAddress -Name ("PubIP"  + $RGName) -ResourceGroupName $RGName;

# Create LoadBalancer
$FrontendName = "fe" + $RGName
$BackendAddressPoolName = "bepool" + $RGName
$ProbeName = "vmssprobe" + $RGName
$InboundNatPoolName  = "innatpool" + $RGName
$LBRuleName = "lbrule" + $RGName
$LBName = "vmsslb" + $RGName

$Frontend = New-AzureRmLoadBalancerFrontendIpConfig -Name $FrontendName -PublicIpAddress $PubIP
$BackendAddressPool = New-AzureRmLoadBalancerBackendAddressPoolConfig -Name $BackendAddressPoolName
$Probe = New-AzureRmLoadBalancerProbeConfig -Name $ProbeName -RequestPath healthcheck.aspx -Protocol http -Port 80 -IntervalInSeconds 15 -ProbeCount 2
$InboundNatPool = New-AzureRmLoadBalancerInboundNatPoolConfig -Name $InboundNatPoolName  -FrontendIPConfigurationId `
    $Frontend.Id -Protocol Tcp -FrontendPortRangeStart 3360 -FrontendPortRangeEnd 3362 -BackendPort 3370;
$LBRule = New-AzureRmLoadBalancerRuleConfig -Name $LBRuleName `
    -FrontendIPConfiguration $Frontend -BackendAddressPool $BackendAddressPool `
    -Probe $Probe -Protocol Tcp -FrontendPort 80 -BackendPort 80 `
    -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP;
$ActualLb = New-AzureRmLoadBalancer -Name $LBName -ResourceGroupName $RGName -Location $LOC `
    -FrontendIpConfiguration $Frontend -BackendAddressPool $BackendAddressPool `
    -Probe $Probe -LoadBalancingRule $LBRule -InboundNatPool $InboundNatPool;
$ExpectedLb = Get-AzureRmLoadBalancer -Name $LBName -ResourceGroupName $RGName

# New VMSS Parameters
$VMSSName = "VMSS" + $RGName;

$AdminUsername = "Admin01";
$AdminPassword = "p4ssw0rd@123" + $RGName;

$PublisherName = "MicrosoftWindowsServer" 
$Offer         = "WindowsServer" 
$Sku           = "2012-R2-Datacenter" 
$Version       = "latest"
        
$VHDContainer = "https://" + $STOName + ".blob.core.contoso.net/" + $VMSSName;

$ExtName = "CSETest";
$Publisher = "Microsoft.Compute";
$ExtType = "BGInfo";
$ExtVer = "2.1";

#IP Config for the NIC
$IPCfg = New-AzureRmVmssIPConfig -Name "Test" `
    -LoadBalancerInboundNatPoolsId $ExpectedLb.InboundNatPools[0].Id `
    -LoadBalancerBackendAddressPoolsId $ExpectedLb.BackendAddressPools[0].Id `
    -SubnetId $SubNetId;
            
#VMSS Config
$VMSS = New-AzureRmVmssConfig -Location $LOC -SkuCapacity 2 -SkuName "Standard_A2" -UpgradePolicyMode "Automatic" `
    | Add-AzureRmVmssNetworkInterfaceConfiguration -Name "Test" -Primary $True -IPConfiguration $IPCfg `
    | Add-AzureRmVmssNetworkInterfaceConfiguration -Name "Test2"  -IPConfiguration $IPCfg `
    | Set-AzureRmVmssOSProfile -ComputerNamePrefix "Test"  -AdminUsername $AdminUsername -AdminPassword $AdminPassword `
    | Set-AzureRmVmssStorageProfile -Name "Test"  -OsDiskCreateOption 'FromImage' -OsDiskCaching "None" `
    -ImageReferenceOffer $Offer -ImageReferenceSku $Sku -ImageReferenceVersion $Version `
    -ImageReferencePublisher $PublisherName -VhdContainer $VHDContainer `
    | Add-AzureRmVmssExtension -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True

#Create the VMSS
New-AzureRmVmss -ResourceGroupName $RGName -Name $VMSSName -VirtualMachineScaleSet $VMSS;
```

<span data-ttu-id="7be94-110">A következő komplex példa létrehoz egy VMSS.</span><span class="sxs-lookup"><span data-stu-id="7be94-110">The following complex example creates a VMSS.</span></span>
<span data-ttu-id="7be94-111">Az első parancs létrehoz egy erőforráscsoportot a megadott névvel és hellyel.</span><span class="sxs-lookup"><span data-stu-id="7be94-111">The first command creates a resource group with the specified name and location.</span></span>
<span data-ttu-id="7be94-112">A második parancs a **New-AzureRmStorageAccount** parancsmagot használja a tárolási fiók létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="7be94-112">The second command uses the **New-AzureRmStorageAccount** cmdlet to create a storage account.</span></span>
<span data-ttu-id="7be94-113">A harmadik parancs ezt követően a **Get-AzureRmStorageAccount** parancsmagot használja a második parancsban létrehozott tárterület-fiók beszerzéséhez, és az eredményt a $STOAccount változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7be94-113">The third command then uses the **Get-AzureRmStorageAccount** cmdlet to get the storage account created in the second command and stores the result in the $STOAccount variable.</span></span>
<span data-ttu-id="7be94-114">Az ötödik parancs a **New-AzureRmVirtualNetworkSubnetConfig** parancsmagot használja alhálózat létrehozásához, és az eredményt az $SubNet nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7be94-114">The fifth command uses the **New-AzureRmVirtualNetworkSubnetConfig** cmdlet to create a subnet and stores the result in the variable named $SubNet.</span></span>
<span data-ttu-id="7be94-115">A hatodik parancs a **New-AzureRmVirtualNetwork** parancsmagot használja virtuális hálózat létrehozásához, és az eredményt az $VNet nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7be94-115">The sixth command uses the **New-AzureRmVirtualNetwork** cmdlet to create a virtual network and stores the result in the variable named $VNet.</span></span>
<span data-ttu-id="7be94-116">A hetedik parancs a **Get-AzureRmVirtualNetwork** használatával információkat kaphat a hatodik parancsban létrehozott virtuális hálózatról, és az adatokat a $VNet nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7be94-116">The seventh command uses the **Get-AzureRmVirtualNetwork** to get information about the virtual network created in the sixth command and stores the information in the variable named $VNet.</span></span>
<span data-ttu-id="7be94-117">A nyolcadik és a kilencedik parancs a **New-AzureRmPublicIpAddress** és a **Get-AzureRmPublicIpAddress** használatával hozza létre és kapja meg az adott nyilvános IP-címről származó információkat.</span><span class="sxs-lookup"><span data-stu-id="7be94-117">The eighth and ninth command uses the **New-AzureRmPublicIpAddress** and **Get- AzureRmPublicIpAddress** to create and get information from that public IP address.</span></span>
<span data-ttu-id="7be94-118">A parancsok a $PubIP nevű változóban tárolják az adatokat.</span><span class="sxs-lookup"><span data-stu-id="7be94-118">The commands store the information in the variable named $PubIP.</span></span>
<span data-ttu-id="7be94-119">A tizedik parancs a **New-AzureRmLoadBalancerFrontendIpConfig** parancsmagot használja egy frontend terheléselosztás létrehozásához, és az eredményt az $frontend nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7be94-119">The tenth command uses the **New- AzureRmLoadBalancerFrontendIpConfig** cmdlet to create a frontend load balancer and stores the result in the variable named $Frontend.</span></span>
<span data-ttu-id="7be94-120">A tizenegyedik parancs a **New-AzureRmLoadBalancerBackendAddressPoolConfig** segítségével hozza létre a backend-címkészlet konfigurációját, és az eredményt az $BackendAddressPool nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7be94-120">The eleventh command uses the **New-AzureRmLoadBalancerBackendAddressPoolConfig** to create a backend address pool configuration and stores the result in the variable named $BackendAddressPool.</span></span>
<span data-ttu-id="7be94-121">A tizenkettedik parancs a **New-AzureRmLoadBalancerProbeConfig** használatával létrehoz egy szondát, és a szonda adatait a $Probe nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7be94-121">The twelfth command uses the **New-AzureRmLoadBalancerProbeConfig** to create a probe and stores the probe information in the variable named $Probe.</span></span>
<span data-ttu-id="7be94-122">A tizenharmadik parancs a **New-AzureRmLoadBalancerInboundNatPoolConfig** parancsmagot használja a terheléselosztó bejövő hálózati címfordítási (NAT) alkalmazáskészlet-konfiguráció létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="7be94-122">The thirteenth command uses the **New-AzureRmLoadBalancerInboundNatPoolConfig** cmdlet to create a load balancer inbound network address translation (NAT) pool configuration.</span></span>
<span data-ttu-id="7be94-123">A tizennegyedik parancs a **New-AzureRmLoadBalancerRuleConfig** segítségével hoz létre terheléselosztó szabály-konfigurációt, és az eredményt az $LBRule nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7be94-123">The fourteenth command uses the **New-AzureRmLoadBalancerRuleConfig** to create a load balancer rule configuration and stores the result in the variable named $LBRule.</span></span>
<span data-ttu-id="7be94-124">A tizenötödik parancs a **New-AzureRmLoadBalancer** parancsmagot használja a terheléselosztó létrehozásához, és az eredményt az $ActualLb nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7be94-124">The fifteenth command uses the **New-AzureRmLoadBalancer** cmdlet to create a load balancer and stores the result in the variable named $ActualLb.</span></span>
<span data-ttu-id="7be94-125">A tizenhatodik parancs a **Get-AzureRmLoadBalancer** használatával információkat kaphat a tizenötödik parancsban létrehozott terheléselosztó rendszerről, és az adatokat a $ExpectedLb nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7be94-125">The sixteenth command uses the **Get-AzureRmLoadBalancer** to get information about the load balancer that was created in the fifteenth command and stores the information in the variable named $ExpectedLb.</span></span>
<span data-ttu-id="7be94-126">A tizenhetedik parancs a **New-AzureRmVmssIPConfig** parancsmagot használja a VMSS IP-konfigurációjának létrehozásához, és az adatokat a $IPCfg nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7be94-126">The seventeenth command uses the **New-AzureRmVmssIPConfig** cmdlet to create a VMSS IP configuration and stores the information in the variable named $IPCfg.</span></span>
<span data-ttu-id="7be94-127">A XVIII parancs a **New-AzureRmVmssConfig** parancsmagot használja VMSS konfigurációs objektum létrehozásához, és az eredményt az $VMSS nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7be94-127">The eighteenth command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="7be94-128">A tizenkilencedik parancs a **New-AzureRmVmss** parancsmagot használja a VMSS létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="7be94-128">The nineteenth command uses the **New-AzureRmVmss** cmdlet to create the VMSS.</span></span>

## <span data-ttu-id="7be94-129">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7be94-129">PARAMETERS</span></span>

### <span data-ttu-id="7be94-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7be94-130">-ResourceGroupName</span></span>
<span data-ttu-id="7be94-131">A VMSS erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7be94-131">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7be94-132">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="7be94-132">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="7be94-133">Azt a **VirtualMachineScaleSet** -objektumot adja meg, amely a parancsmag által létrehozott VMSS tulajdonságait tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="7be94-133">Specifies the **VirtualMachineScaleSet** object that contains the properties of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7be94-134">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="7be94-134">-VMScaleSetName</span></span>
<span data-ttu-id="7be94-135">Annak a VMSS a nevét adja meg, amelyet a parancsmag hoz létre.</span><span class="sxs-lookup"><span data-stu-id="7be94-135">Specifies the name of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7be94-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7be94-136">-Confirm</span></span>
<span data-ttu-id="7be94-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7be94-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7be94-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7be94-138">-WhatIf</span></span>
<span data-ttu-id="7be94-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7be94-139">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="7be94-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7be94-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7be94-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7be94-141">CommonParameters</span></span>
<span data-ttu-id="7be94-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7be94-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7be94-143">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7be94-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7be94-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7be94-144">INPUTS</span></span>

### <span data-ttu-id="7be94-145">Nincs</span><span class="sxs-lookup"><span data-stu-id="7be94-145">None</span></span>
<span data-ttu-id="7be94-146">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="7be94-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7be94-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7be94-147">OUTPUTS</span></span>

### <span data-ttu-id="7be94-148">Ez a parancsmag semmilyen kimenetet nem hoz létre.</span><span class="sxs-lookup"><span data-stu-id="7be94-148">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="7be94-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7be94-149">NOTES</span></span>

## <span data-ttu-id="7be94-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7be94-150">RELATED LINKS</span></span>

[<span data-ttu-id="7be94-151">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="7be94-151">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="7be94-152">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="7be94-152">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="7be94-153">Újraindítás – AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="7be94-153">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="7be94-154">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="7be94-154">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="7be94-155">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="7be94-155">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="7be94-156">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="7be94-156">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="7be94-157">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="7be94-157">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


