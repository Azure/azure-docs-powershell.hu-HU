---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 1A2C843C-6962-4B0E-ACBF-A5EFF609A5BE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmss
schema: 2.0.0
ms.openlocfilehash: f93e05448278e2aaa70ff226a5d3618fdad0e6b4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850118"
---
# <span data-ttu-id="476e6-101">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="476e6-101">New-AzureRmVmss</span></span>

## <span data-ttu-id="476e6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="476e6-102">SYNOPSIS</span></span>
<span data-ttu-id="476e6-103">Létrehoz egy VMSS.</span><span class="sxs-lookup"><span data-stu-id="476e6-103">Creates a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="476e6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="476e6-104">SYNTAX</span></span>

### <span data-ttu-id="476e6-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="476e6-105">DefaultParameter (Default)</span></span>
```
New-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="476e6-106">SimpleParameterSet</span><span class="sxs-lookup"><span data-stu-id="476e6-106">SimpleParameterSet</span></span>
```
New-AzureRmVmss [[-ResourceGroupName] <String>] [-VMScaleSetName] <String> [-AsJob] [-ImageName <String>]
 -Credential <PSCredential> [-InstanceCount <Int32>] [-VirtualNetworkName <String>] [-SubnetName <String>]
 [-PublicIpAddressName <String>] [-DomainNameLabel <String>] [-SecurityGroupName <String>]
 [-LoadBalancerName <String>] [-BackendPort <Int32[]>] [-Location <String>] [-VmSize <String>]
 [-UpgradePolicyMode <UpgradeMode>] [-AllocationMethod <String>] [-VnetAddressPrefix <String>]
 [-SubnetAddressPrefix <String>] [-FrontendPoolName <String>] [-BackendPoolName <String>]
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-NatBackendPort <Int32[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="476e6-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="476e6-107">DESCRIPTION</span></span>
<span data-ttu-id="476e6-108">A **New-AzureRmVmss** parancsmag létrehoz egy virtuálisgép-készletet (VMSS) az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="476e6-108">The **New-AzureRmVmss** cmdlet creates a Virtual Machine Scale Set (VMSS) in Azure.</span></span>
<span data-ttu-id="476e6-109">Ez a parancsmag a **VirtualMachineScaleSet** objektumot bemenetként veszi fel.</span><span class="sxs-lookup"><span data-stu-id="476e6-109">This cmdlet takes a **VirtualMachineScaleSet** object as input.</span></span>

## <span data-ttu-id="476e6-110">Példák</span><span class="sxs-lookup"><span data-stu-id="476e6-110">EXAMPLES</span></span>

### <span data-ttu-id="476e6-111">Példa 1: VMSS létrehozása</span><span class="sxs-lookup"><span data-stu-id="476e6-111">Example 1: Create a VMSS</span></span>
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

<span data-ttu-id="476e6-112">A következő komplex példa létrehoz egy VMSS.</span><span class="sxs-lookup"><span data-stu-id="476e6-112">The following complex example creates a VMSS.</span></span>
<span data-ttu-id="476e6-113">Az első parancs létrehoz egy erőforráscsoportot a megadott névvel és hellyel.</span><span class="sxs-lookup"><span data-stu-id="476e6-113">The first command creates a resource group with the specified name and location.</span></span>
<span data-ttu-id="476e6-114">A második parancs a **New-AzureRmStorageAccount** parancsmagot használja a tárolási fiók létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="476e6-114">The second command uses the **New-AzureRmStorageAccount** cmdlet to create a storage account.</span></span>
<span data-ttu-id="476e6-115">A harmadik parancs ezt követően a **Get-AzureRmStorageAccount** parancsmagot használja a második parancsban létrehozott tárterület-fiók beszerzéséhez, és az eredményt a $STOAccount változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="476e6-115">The third command then uses the **Get-AzureRmStorageAccount** cmdlet to get the storage account created in the second command and stores the result in the $STOAccount variable.</span></span>
<span data-ttu-id="476e6-116">Az ötödik parancs a **New-AzureRmVirtualNetworkSubnetConfig** parancsmagot használja alhálózat létrehozásához, és az eredményt az $SubNet nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="476e6-116">The fifth command uses the **New-AzureRmVirtualNetworkSubnetConfig** cmdlet to create a subnet and stores the result in the variable named $SubNet.</span></span>
<span data-ttu-id="476e6-117">A hatodik parancs a **New-AzureRmVirtualNetwork** parancsmagot használja virtuális hálózat létrehozásához, és az eredményt az $VNet nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="476e6-117">The sixth command uses the **New-AzureRmVirtualNetwork** cmdlet to create a virtual network and stores the result in the variable named $VNet.</span></span>
<span data-ttu-id="476e6-118">A hetedik parancs a **Get-AzureRmVirtualNetwork** használatával információkat kaphat a hatodik parancsban létrehozott virtuális hálózatról, és az adatokat a $VNet nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="476e6-118">The seventh command uses the **Get-AzureRmVirtualNetwork** to get information about the virtual network created in the sixth command and stores the information in the variable named $VNet.</span></span>
<span data-ttu-id="476e6-119">A nyolcadik és a kilencedik parancs a **New-AzureRmPublicIpAddress** és a **Get-AzureRmPublicIpAddress** használatával hozza létre és kapja meg az adott nyilvános IP-címről származó információkat.</span><span class="sxs-lookup"><span data-stu-id="476e6-119">The eighth and ninth command uses the **New-AzureRmPublicIpAddress** and **Get- AzureRmPublicIpAddress** to create and get information from that public IP address.</span></span>
<span data-ttu-id="476e6-120">A parancsok a $PubIP nevű változóban tárolják az adatokat.</span><span class="sxs-lookup"><span data-stu-id="476e6-120">The commands store the information in the variable named $PubIP.</span></span>
<span data-ttu-id="476e6-121">A tizedik parancs a **New-AzureRmLoadBalancerFrontendIpConfig** parancsmagot használja egy frontend terheléselosztás létrehozásához, és az eredményt az $frontend nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="476e6-121">The tenth command uses the **New- AzureRmLoadBalancerFrontendIpConfig** cmdlet to create a frontend load balancer and stores the result in the variable named $Frontend.</span></span>
<span data-ttu-id="476e6-122">A tizenegyedik parancs a **New-AzureRmLoadBalancerBackendAddressPoolConfig** segítségével hozza létre a backend-címkészlet konfigurációját, és az eredményt az $BackendAddressPool nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="476e6-122">The eleventh command uses the **New-AzureRmLoadBalancerBackendAddressPoolConfig** to create a backend address pool configuration and stores the result in the variable named $BackendAddressPool.</span></span>
<span data-ttu-id="476e6-123">A tizenkettedik parancs a **New-AzureRmLoadBalancerProbeConfig** használatával létrehoz egy szondát, és a szonda adatait a $Probe nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="476e6-123">The twelfth command uses the **New-AzureRmLoadBalancerProbeConfig** to create a probe and stores the probe information in the variable named $Probe.</span></span>
<span data-ttu-id="476e6-124">A tizenharmadik parancs a **New-AzureRmLoadBalancerInboundNatPoolConfig** parancsmagot használja a terheléselosztó bejövő hálózati címfordítási (NAT) alkalmazáskészlet-konfiguráció létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="476e6-124">The thirteenth command uses the **New-AzureRmLoadBalancerInboundNatPoolConfig** cmdlet to create a load balancer inbound network address translation (NAT) pool configuration.</span></span>
<span data-ttu-id="476e6-125">A tizennegyedik parancs a **New-AzureRmLoadBalancerRuleConfig** segítségével hoz létre terheléselosztó szabály-konfigurációt, és az eredményt az $LBRule nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="476e6-125">The fourteenth command uses the **New-AzureRmLoadBalancerRuleConfig** to create a load balancer rule configuration and stores the result in the variable named $LBRule.</span></span>
<span data-ttu-id="476e6-126">A tizenötödik parancs a **New-AzureRmLoadBalancer** parancsmagot használja a terheléselosztó létrehozásához, és az eredményt az $ActualLb nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="476e6-126">The fifteenth command uses the **New-AzureRmLoadBalancer** cmdlet to create a load balancer and stores the result in the variable named $ActualLb.</span></span>
<span data-ttu-id="476e6-127">A tizenhatodik parancs a **Get-AzureRmLoadBalancer** használatával információkat kaphat a tizenötödik parancsban létrehozott terheléselosztó rendszerről, és az adatokat a $ExpectedLb nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="476e6-127">The sixteenth command uses the **Get-AzureRmLoadBalancer** to get information about the load balancer that was created in the fifteenth command and stores the information in the variable named $ExpectedLb.</span></span>
<span data-ttu-id="476e6-128">A tizenhetedik parancs a **New-AzureRmVmssIPConfig** parancsmagot használja a VMSS IP-konfigurációjának létrehozásához, és az adatokat a $IPCfg nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="476e6-128">The seventeenth command uses the **New-AzureRmVmssIPConfig** cmdlet to create a VMSS IP configuration and stores the information in the variable named $IPCfg.</span></span>
<span data-ttu-id="476e6-129">A XVIII parancs a **New-AzureRmVmssConfig** parancsmagot használja VMSS konfigurációs objektum létrehozásához, és az eredményt az $VMSS nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="476e6-129">The eighteenth command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="476e6-130">A tizenkilencedik parancs a **New-AzureRmVmss** parancsmagot használja a VMSS létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="476e6-130">The nineteenth command uses the **New-AzureRmVmss** cmdlet to create the VMSS.</span></span>

## <span data-ttu-id="476e6-131">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="476e6-131">PARAMETERS</span></span>

### <span data-ttu-id="476e6-132">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="476e6-132">-AllocationMethod</span></span>
<span data-ttu-id="476e6-133">A méretarány (statikus vagy dinamikus) nyilvános IP-címének kiosztási módja.</span><span class="sxs-lookup"><span data-stu-id="476e6-133">Allocation method for the Public IP Address of the Scale Set (Static or Dynamic).</span></span>  <span data-ttu-id="476e6-134">Ha nincs megadva érték, akkor a felosztás statikus lesz.</span><span class="sxs-lookup"><span data-stu-id="476e6-134">If no value is supplied, allocation will be static.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 
Accepted values: Static, Dynamic

Required: False
Position: Named
Default value: Static
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="476e6-135">-AsJob</span><span class="sxs-lookup"><span data-stu-id="476e6-135">-AsJob</span></span>
<span data-ttu-id="476e6-136">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="476e6-136">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="476e6-137">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="476e6-137">-BackendPoolName</span></span>
<span data-ttu-id="476e6-138">Annak a backend-címkészlet a neve, amelyet az ehhez a léptékhez tartozó terheléselosztásban szeretne használni.</span><span class="sxs-lookup"><span data-stu-id="476e6-138">The name of the backend address pool to use in the load balancer for this Scale Set.</span></span>  <span data-ttu-id="476e6-139">Ha nincs megadva érték, akkor létrejön egy új backend-készlet, amelynek a neve megegyezik a méretarány beállítással.</span><span class="sxs-lookup"><span data-stu-id="476e6-139">If no value is provided, a new backend pool will be created, with the same name as the Scale Set.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="476e6-140">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="476e6-140">-BackendPort</span></span>
<span data-ttu-id="476e6-141">A kiegyenlítő terheléselosztás által a VM-tel való kommunikációhoz a méretarány beállítása által használt backend-portok száma.</span><span class="sxs-lookup"><span data-stu-id="476e6-141">Backend port numbers used by the Scale Set load balancer to communicate with VMs in the Scale Set.</span></span>  <span data-ttu-id="476e6-142">Ha nincs megadva érték, akkor a rendszer a 3389 és az 5985-es portot fogja használni a Windows VMS rendszerhez, és a 22-ös portot fogja használni a Linux VM-hez.</span><span class="sxs-lookup"><span data-stu-id="476e6-142">If no values are specified, ports 3389 and 5985 will be used for Windows VMS, and port 22 will be used for Linux VMs.</span></span>

```yaml
Type: Int32[]
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="476e6-143">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="476e6-143">-Credential</span></span>
<span data-ttu-id="476e6-144">A virtuális VMs-rendszerhez tartozó rendszergazdai hitelesítő adatok (Felhasználónév és jelszó) ebben a méretarányban jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="476e6-144">The administrator credentials (username and password) for VMs in this Scale Set.</span></span>

```yaml
Type: PSCredential
Parameter Sets: SimpleParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="476e6-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="476e6-145">-DefaultProfile</span></span>
<span data-ttu-id="476e6-146">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="476e6-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="476e6-147">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="476e6-147">-DomainNameLabel</span></span>
<span data-ttu-id="476e6-148">A nyilvános Fully-Qualified tartománynév címkéje (FQDN) ehhez a méretarányhoz.</span><span class="sxs-lookup"><span data-stu-id="476e6-148">The domain name label for the public Fully-Qualified domain name (FQDN) for this Scale Set.</span></span> <span data-ttu-id="476e6-149">Ez a tartománynév első olyan része, amelyet a program automatikusan hozzárendel a méretarányhoz.</span><span class="sxs-lookup"><span data-stu-id="476e6-149">This is the first component of the domain name that is automatically assigned to the Scale Set.</span></span> <span data-ttu-id="476e6-150">Automatikusan hozzárendelt tartománynevek: használja az űrlapot ( <DomainNameLabel> . <Location> . cloudapp.azure.com).</span><span class="sxs-lookup"><span data-stu-id="476e6-150">Automatically assigned Domain names use the form (<DomainNameLabel>.<Location>.cloudapp.azure.com).</span></span> <span data-ttu-id="476e6-151">Ha nincs megadva érték, az alapértelmezett tartománynév-címke lesz az ÖSSZEFŰZ <ScaleSetName> és a <ResourceGroupName> .</span><span class="sxs-lookup"><span data-stu-id="476e6-151">If no value is supplied, the default domain name label will be the concatenation of <ScaleSetName> and <ResourceGroupName>.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="476e6-152">-FrontendPoolName</span><span class="sxs-lookup"><span data-stu-id="476e6-152">-FrontendPoolName</span></span>
<span data-ttu-id="476e6-153">A Scale set terheléselosztó bővítményben használandó felületi címkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="476e6-153">The name of the frontend address pool to use in the Scale Set load balancer.</span></span>  <span data-ttu-id="476e6-154">Ha nincs megadva érték, akkor létrejön egy új felületi címkészlet, amelynek a neve megegyezik a méretarány beállítással.</span><span class="sxs-lookup"><span data-stu-id="476e6-154">If no value is supplied, a new Frontend Address Pool will be created, with the same name as the scale set.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="476e6-155">-ImageName</span><span class="sxs-lookup"><span data-stu-id="476e6-155">-ImageName</span></span>
<span data-ttu-id="476e6-156">A virtuális VM-fájl neve ebben a méretarányban.</span><span class="sxs-lookup"><span data-stu-id="476e6-156">The name of the image for VMs in this Scale Set.</span></span> <span data-ttu-id="476e6-157">Ha nincs megadva érték, a program a "Windows Server 2016-adatközpont" képet fogja használni.</span><span class="sxs-lookup"><span data-stu-id="476e6-157">If no value is provided, the "Windows Server 2016 DataCenter" image will be used.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="476e6-158">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="476e6-158">-InstanceCount</span></span>
<span data-ttu-id="476e6-159">A virtuális VM-képek száma a méretarányban.</span><span class="sxs-lookup"><span data-stu-id="476e6-159">The number of VM images in the Scale Set.</span></span>  <span data-ttu-id="476e6-160">Ha nincs megadva érték, akkor két példány jön létre.</span><span class="sxs-lookup"><span data-stu-id="476e6-160">If no value is provided, 2 instances will be created.</span></span>

```yaml
Type: Int32
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: 2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="476e6-161">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="476e6-161">-LoadBalancerName</span></span>
<span data-ttu-id="476e6-162">Az ezzel a Méretaránysal használandó terheléselosztó neve.</span><span class="sxs-lookup"><span data-stu-id="476e6-162">The name of the load balancer to use with this Scale Set.</span></span>  <span data-ttu-id="476e6-163">Új terheléselosztó a méretarány nevének megadásával, ha a program nem ad meg értéket.</span><span class="sxs-lookup"><span data-stu-id="476e6-163">A new load balancer using the same name as the Scale Set will be created if no value is specified.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="476e6-164">-Hely</span><span class="sxs-lookup"><span data-stu-id="476e6-164">-Location</span></span>
<span data-ttu-id="476e6-165">Az Azure-hely, ahol ez a méretarány jön létre.</span><span class="sxs-lookup"><span data-stu-id="476e6-165">The Azure location where this Scale Set will be created.</span></span>  <span data-ttu-id="476e6-166">Ha nincs megadva érték, a program a paraméterben hivatkozott további források helyétől kikövetkezteti a helyet.</span><span class="sxs-lookup"><span data-stu-id="476e6-166">If no value is specified, the location will be inferred from the location of other resources referenced in the parameters.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="476e6-167">-NatBackendPort</span><span class="sxs-lookup"><span data-stu-id="476e6-167">-NatBackendPort</span></span>
<span data-ttu-id="476e6-168">A bejövő hálózati címfordításhoz tartozó backend port.</span><span class="sxs-lookup"><span data-stu-id="476e6-168">Backend port for inbound network address translation.</span></span>

```yaml
Type: Int32[]
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="476e6-169">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="476e6-169">-PublicIpAddressName</span></span>
<span data-ttu-id="476e6-170">Annak a nyilvános IP-címnek a neve, amellyel az adott méretarányt be szeretné használni.</span><span class="sxs-lookup"><span data-stu-id="476e6-170">The name of the public IP Address to use with this scale set.</span></span>  <span data-ttu-id="476e6-171">Ha nincs megadva érték, akkor létrejön egy új nyilvános IP-azonosító a méretarány nevével.</span><span class="sxs-lookup"><span data-stu-id="476e6-171">A new Public IPAddress with the same name as the Scale Set will be created if no value is provided.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="476e6-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="476e6-172">-ResourceGroupName</span></span>
<span data-ttu-id="476e6-173">A VMSS erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="476e6-173">Specifies the name of the resource group of the VMSS.</span></span>  <span data-ttu-id="476e6-174">Ha nincs megadva érték, új ResourceGroup fog létrejönni a méretarány nevével.</span><span class="sxs-lookup"><span data-stu-id="476e6-174">If no value is specified, a new ResourceGroup will be created using the same name as the Scale Set.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="476e6-175">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="476e6-175">-SecurityGroupName</span></span>
<span data-ttu-id="476e6-176">Annak a hálózati biztonsági csoportnak a neve, amelyre alkalmazni szeretné ezt a méretarányt.</span><span class="sxs-lookup"><span data-stu-id="476e6-176">The name of the network security group to apply to this Scale Set.</span></span>  <span data-ttu-id="476e6-177">Ha nincs megadva érték, akkor létrejön egy alapértelmezett hálózati biztonsági csoport, amelynek a mérete megegyezik a méretarány beállítással.</span><span class="sxs-lookup"><span data-stu-id="476e6-177">If no value is provided, a default network security group with the same name as the Scale Set will be created and applied to the Scale Set.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="476e6-178">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="476e6-178">-SubnetAddressPrefix</span></span>
<span data-ttu-id="476e6-179">Annak az alhálózatnak az előtagja, amelyet a ScaleSet használni fog.</span><span class="sxs-lookup"><span data-stu-id="476e6-179">The address prefix of the Subnet this ScaleSet will use.</span></span> <span data-ttu-id="476e6-180">Az alapértelmezett alhálózati beállítások (192.168.1.0/24) akkor érvényesek, ha nincs megadva érték.</span><span class="sxs-lookup"><span data-stu-id="476e6-180">Default Subnet settings (192.168.1.0/24) will be applied if no value is provided.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: 192.168.1.0/24
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="476e6-181">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="476e6-181">-SubnetName</span></span>
<span data-ttu-id="476e6-182">Annak az alhálózatnak a neve, amely az adott méretarányt használja.</span><span class="sxs-lookup"><span data-stu-id="476e6-182">The name of the subnet to use with this Scale Set.</span></span>  <span data-ttu-id="476e6-183">Ha nincs megadva érték, akkor létrejön egy új alhálózat a méretarány-készlet nevével.</span><span class="sxs-lookup"><span data-stu-id="476e6-183">A new Subnet will be created with the same name as the Scale Set if no value is provided.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="476e6-184">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="476e6-184">-UpgradePolicyMode</span></span>
<span data-ttu-id="476e6-185">Ebben a méretarányban a VM-példányokra vonatkozó frissítési házirend üzemmódot adja meg.</span><span class="sxs-lookup"><span data-stu-id="476e6-185">The upgrade policy mode for VM instances in this Scale Set.</span></span>  <span data-ttu-id="476e6-186">A frissítési házirend az automatikus, a manuális vagy a folyamatos frissítést is megadhatja.</span><span class="sxs-lookup"><span data-stu-id="476e6-186">Upgrade policy could specify Automatic, Manual, or Rolling upgrades.</span></span>

```yaml
Type: UpgradeMode
Parameter Sets: SimpleParameterSet
Aliases: 
Accepted values: Automatic, Manual, Rolling

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="476e6-187">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="476e6-187">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="476e6-188">Azt a **VirtualMachineScaleSet** -objektumot adja meg, amely a parancsmag által létrehozott VMSS tulajdonságait tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="476e6-188">Specifies the **VirtualMachineScaleSet** object that contains the properties of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="476e6-189">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="476e6-189">-VirtualNetworkName</span></span>
<span data-ttu-id="476e6-190">Annak a virtuális hálózatnak a neve, amellyel az adott méretarányt használni szeretné.</span><span class="sxs-lookup"><span data-stu-id="476e6-190">The name fo the Virtual Network to use with this scale set.</span></span>  <span data-ttu-id="476e6-191">Ha nincs megadva érték, akkor létrejön egy új virtuális hálózat, amelynek a neve megegyezik a méretarány-Halmazsal.</span><span class="sxs-lookup"><span data-stu-id="476e6-191">If no value is supplied, a new virtual network with the same name as the Scale Set will be created.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="476e6-192">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="476e6-192">-VMScaleSetName</span></span>
<span data-ttu-id="476e6-193">Annak a VMSS a nevét adja meg, amelyet a parancsmag hoz létre.</span><span class="sxs-lookup"><span data-stu-id="476e6-193">Specifies the name of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="476e6-194">-VmSize</span><span class="sxs-lookup"><span data-stu-id="476e6-194">-VmSize</span></span>
<span data-ttu-id="476e6-195">A megadott méretarányban a VM-példányok mérete.</span><span class="sxs-lookup"><span data-stu-id="476e6-195">The size of the VM instances in this scale set.</span></span>  <span data-ttu-id="476e6-196">Ha nincs megadva méret, az alapértelmezett méret (Standard_DS1_v2) lesz használatos.</span><span class="sxs-lookup"><span data-stu-id="476e6-196">A default size (Standard_DS1_v2) will be used if no Size is specified.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: Standard_DS1_v2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="476e6-197">-VnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="476e6-197">-VnetAddressPrefix</span></span>
<span data-ttu-id="476e6-198">A megadott Méretaránysal használt virtuális hálózathoz tartozó cím előtagja.</span><span class="sxs-lookup"><span data-stu-id="476e6-198">The address prefix for the virtual network used with this Scale Set.</span></span>  <span data-ttu-id="476e6-199">Az alapértelmezett virtuális hálózati cím előtag-beállításai (192.168.0.0/16) akkor lesznek használatban, ha nincs megadva érték.</span><span class="sxs-lookup"><span data-stu-id="476e6-199">Default virtual network address prefix settings (192.168.0.0/16) will be used if no value is supplied.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: 192.168.0.0/16
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="476e6-200">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="476e6-200">-Zone</span></span>
<span data-ttu-id="476e6-201">Az erőforráshoz hozzárendelt IP-címet jelölő elérhetőségi zónák listája.</span><span class="sxs-lookup"><span data-stu-id="476e6-201">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="476e6-202">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="476e6-202">-Confirm</span></span>
<span data-ttu-id="476e6-203">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="476e6-203">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="476e6-204">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="476e6-204">-WhatIf</span></span>
<span data-ttu-id="476e6-205">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="476e6-205">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="476e6-206">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="476e6-206">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="476e6-207">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="476e6-207">CommonParameters</span></span>
<span data-ttu-id="476e6-208">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="476e6-208">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="476e6-209">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="476e6-209">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="476e6-210">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="476e6-210">INPUTS</span></span>

### <span data-ttu-id="476e6-211">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="476e6-211">VirtualMachineScaleSet</span></span>
<span data-ttu-id="476e6-212">A ' VirtualMachineScaleSet ' paraméter az "VirtualMachineScaleSet" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="476e6-212">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="476e6-213">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="476e6-213">OUTPUTS</span></span>

### <span data-ttu-id="476e6-214">Ez a parancsmag semmilyen kimenetet nem hoz létre.</span><span class="sxs-lookup"><span data-stu-id="476e6-214">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="476e6-215">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="476e6-215">NOTES</span></span>

## <span data-ttu-id="476e6-216">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="476e6-216">RELATED LINKS</span></span>

[<span data-ttu-id="476e6-217">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="476e6-217">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="476e6-218">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="476e6-218">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="476e6-219">Újraindítás – AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="476e6-219">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="476e6-220">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="476e6-220">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="476e6-221">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="476e6-221">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="476e6-222">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="476e6-222">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="476e6-223">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="476e6-223">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


