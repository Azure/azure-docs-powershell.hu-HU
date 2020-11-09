---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1A2C843C-6962-4B0E-ACBF-A5EFF609A5BE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmss.md
ms.openlocfilehash: 4953e914cc52784cd815be80307babfe05f3b63c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300776"
---
# <span data-ttu-id="40e4b-101">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="40e4b-101">New-AzVmss</span></span>

## <span data-ttu-id="40e4b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="40e4b-102">SYNOPSIS</span></span>
<span data-ttu-id="40e4b-103">Létrehoz egy VMSS.</span><span class="sxs-lookup"><span data-stu-id="40e4b-103">Creates a VMSS.</span></span>

## <span data-ttu-id="40e4b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="40e4b-104">SYNTAX</span></span>

### <span data-ttu-id="40e4b-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="40e4b-105">DefaultParameter (Default)</span></span>
```
New-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40e4b-106">SimpleParameterSet</span><span class="sxs-lookup"><span data-stu-id="40e4b-106">SimpleParameterSet</span></span>
```
New-AzVmss [[-ResourceGroupName] <String>] [-VMScaleSetName] <String> [-AsJob] [-ImageName <String>]
 -Credential <PSCredential> [-InstanceCount <Int32>] [-VirtualNetworkName <String>] [-SubnetName <String>]
 [-PublicIpAddressName <String>] [-DomainNameLabel <String>] [-SecurityGroupName <String>]
 [-LoadBalancerName <String>] [-BackendPort <Int32[]>] [-Location <String>] [-VmSize <String>]
 [-UpgradePolicyMode <UpgradeMode>] [-AllocationMethod <String>] [-VnetAddressPrefix <String>]
 [-SubnetAddressPrefix <String>] [-FrontendPoolName <String>] [-BackendPoolName <String>]
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-EnableUltraSSD]
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-NatBackendPort <Int32[]>]
 [-DataDiskSizeInGb <Int32[]>] [-ProximityPlacementGroupId <String>] [-HostGroupId <String>]
 [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>] [-ScaleInPolicy <String[]>]
 [-SkipExtensionsOnOverprovisionedVMs] [-EncryptionAtHost] [-PlatformFaultDomainCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-SinglePlacementGroup] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40e4b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="40e4b-107">DESCRIPTION</span></span>
<span data-ttu-id="40e4b-108">A **New-AzVmss** parancsmag létrehoz egy virtuálisgép-készletet (VMSS) az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="40e4b-108">The **New-AzVmss** cmdlet creates a Virtual Machine Scale Set (VMSS) in Azure.</span></span>
<span data-ttu-id="40e4b-109">Az egyszerű típusparaméter ( `SimpleParameterSet` ) segítségével gyorsan létrehozhat előre beállított VMSS és kapcsolódó erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="40e4b-109">Use the simple parameter set (`SimpleParameterSet`) to quickly create a pre-set VMSS and associated resources.</span></span> <span data-ttu-id="40e4b-110">Az alapértelmezett paramétert () akkor használja, `DefaultParameter` Ha a VMSS és a hozzájuk rendelt erőforrások mindegyik összetevőjének pontos konfigurálására van szükség a létrehozás előtt.</span><span class="sxs-lookup"><span data-stu-id="40e4b-110">Use the default parameter set (`DefaultParameter`) for more advanced scenarios when you need to precisely configure each component of the VMSS and each associated resource before creation.</span></span>

## <span data-ttu-id="40e4b-111">Példák</span><span class="sxs-lookup"><span data-stu-id="40e4b-111">EXAMPLES</span></span>

### <span data-ttu-id="40e4b-112">Példa 1: VMSS létrehozása a **`SimpleParameterSet`**</span><span class="sxs-lookup"><span data-stu-id="40e4b-112">Example 1: Create a VMSS using the **`SimpleParameterSet`**</span></span>
```powershell
$vmssName = <VMSSNAME>
# Create credentials, I am using one way to create credentials, there are others as well. 
# Pick one that makes the most sense according to your use case.
$vmPassword = ConvertTo-SecureString <PASSWORD_HERE> -AsPlainText -Force
$vmCred = New-Object System.Management.Automation.PSCredential(<USERNAME_HERE>, $vmPassword)

#Create a VMSS using the default settings
New-AzVmss -Credential $vmCred -VMScaleSetName $vmssName
```

<span data-ttu-id="40e4b-113">A fenti parancs a következőképpen hozza létre a nevet `$vmssName` :</span><span class="sxs-lookup"><span data-stu-id="40e4b-113">The command above creates the following with the name `$vmssName` :</span></span>
* <span data-ttu-id="40e4b-114">Erőforráscsoport</span><span class="sxs-lookup"><span data-stu-id="40e4b-114">A Resource Group</span></span>
* <span data-ttu-id="40e4b-115">Virtuális hálózat</span><span class="sxs-lookup"><span data-stu-id="40e4b-115">A virtual network</span></span>
* <span data-ttu-id="40e4b-116">A terheléselosztó</span><span class="sxs-lookup"><span data-stu-id="40e4b-116">A load balancer</span></span>
* <span data-ttu-id="40e4b-117">Nyilvános IP-cím</span><span class="sxs-lookup"><span data-stu-id="40e4b-117">A public IP</span></span>
* <span data-ttu-id="40e4b-118">a VMSS két példányban</span><span class="sxs-lookup"><span data-stu-id="40e4b-118">the VMSS with 2 instances</span></span>

<span data-ttu-id="40e4b-119">A VMSS a VMs-rendszerhez kiválasztott alapértelmezett kép `2016-Datacenter Windows Server` és a SKU `Standard_DS1_v2`</span><span class="sxs-lookup"><span data-stu-id="40e4b-119">The default image chosen for the VMs in the VMSS is `2016-Datacenter Windows Server` and the SKU is `Standard_DS1_v2`</span></span>

### <span data-ttu-id="40e4b-120">2. példa: VMSS létrehozása a **`DefaultParameterSet`**</span><span class="sxs-lookup"><span data-stu-id="40e4b-120">Example 2: Create a VMSS using the **`DefaultParameterSet`**</span></span>
```powershell
# Common
$LOC = "WestUs";
$RGName = "rgkyvms";

New-AzResourceGroup -Name $RGName -Location $LOC -Force;

# SRP
$STOName = "STO" + $RGName;
$STOType = "Standard_GRS";
New-AzStorageAccount -ResourceGroupName $RGName -Name $STOName -Location $LOC -Type $STOType;
$STOAccount = Get-AzStorageAccount -ResourceGroupName $RGName -Name $STOName; 

# NRP
$SubNet = New-AzVirtualNetworkSubnetConfig -Name ("subnet" + $RGName) -AddressPrefix "10.0.0.0/24";
$VNet = New-AzVirtualNetwork -Force -Name ("vnet" + $RGName) -ResourceGroupName $RGName -Location $LOC -AddressPrefix "10.0.0.0/16" -DnsServer "10.1.1.1" -Subnet $SubNet;
$VNet = Get-AzVirtualNetwork -Name ('vnet' + $RGName) -ResourceGroupName $RGName;
$SubNetId = $VNet.Subnets[0].Id;

$PubIP = New-AzPublicIpAddress -Force -Name ("PubIP" + $RGName) -ResourceGroupName $RGName -Location $LOC -AllocationMethod Dynamic -DomainNameLabel ("PubIP" + $RGName);
$PubIP = Get-AzPublicIpAddress -Name ("PubIP"  + $RGName) -ResourceGroupName $RGName;

# Create LoadBalancer
$FrontendName = "fe" + $RGName
$BackendAddressPoolName = "bepool" + $RGName
$ProbeName = "vmssprobe" + $RGName
$InboundNatPoolName  = "innatpool" + $RGName
$LBRuleName = "lbrule" + $RGName
$LBName = "vmsslb" + $RGName

$Frontend = New-AzLoadBalancerFrontendIpConfig -Name $FrontendName -PublicIpAddress $PubIP
$BackendAddressPool = New-AzLoadBalancerBackendAddressPoolConfig -Name $BackendAddressPoolName
$Probe = New-AzLoadBalancerProbeConfig -Name $ProbeName -RequestPath healthcheck.aspx -Protocol http -Port 80 -IntervalInSeconds 15 -ProbeCount 2
$InboundNatPool = New-AzLoadBalancerInboundNatPoolConfig -Name $InboundNatPoolName  -FrontendIPConfigurationId `
    $Frontend.Id -Protocol Tcp -FrontendPortRangeStart 3360 -FrontendPortRangeEnd 3362 -BackendPort 3370;
$LBRule = New-AzLoadBalancerRuleConfig -Name $LBRuleName `
    -FrontendIPConfiguration $Frontend -BackendAddressPool $BackendAddressPool `
    -Probe $Probe -Protocol Tcp -FrontendPort 80 -BackendPort 80 `
    -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP;
$ActualLb = New-AzLoadBalancer -Name $LBName -ResourceGroupName $RGName -Location $LOC `
    -FrontendIpConfiguration $Frontend -BackendAddressPool $BackendAddressPool `
    -Probe $Probe -LoadBalancingRule $LBRule -InboundNatPool $InboundNatPool;
$ExpectedLb = Get-AzLoadBalancer -Name $LBName -ResourceGroupName $RGName

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
$IPCfg = New-AzVmssIPConfig -Name "Test" `
    -LoadBalancerInboundNatPoolsId $ExpectedLb.InboundNatPools[0].Id `
    -LoadBalancerBackendAddressPoolsId $ExpectedLb.BackendAddressPools[0].Id `
    -SubnetId $SubNetId;
            
#VMSS Config
$VMSS = New-AzVmssConfig -Location $LOC -SkuCapacity 2 -SkuName "Standard_E4-2ds_v4" -UpgradePolicyMode "Automatic" `
    | Add-AzVmssNetworkInterfaceConfiguration -Name "Test" -Primary $True -IPConfiguration $IPCfg `
    | Add-AzVmssNetworkInterfaceConfiguration -Name "Test2"  -IPConfiguration $IPCfg `
    | Set-AzVmssOSProfile -ComputerNamePrefix "Test"  -AdminUsername $AdminUsername -AdminPassword $AdminPassword `
    | Set-AzVmssStorageProfile -Name "Test"  -OsDiskCreateOption 'FromImage' -OsDiskCaching "None" `
    -ImageReferenceOffer $Offer -ImageReferenceSku $Sku -ImageReferenceVersion $Version `
    -ImageReferencePublisher $PublisherName -VhdContainer $VHDContainer `
    | Add-AzVmssExtension -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True

#Create the VMSS
New-AzVmss -ResourceGroupName $RGName -Name $VMSSName -VirtualMachineScaleSet $VMSS;
```

<span data-ttu-id="40e4b-121">A fenti komplex példa létrehoz egy VMSS, az alábbi magyarázattal a mi történik:</span><span class="sxs-lookup"><span data-stu-id="40e4b-121">The complex example above creates a VMSS, following is an explanation of what is happening:</span></span>
* <span data-ttu-id="40e4b-122">Az első parancs létrehoz egy erőforráscsoportot a megadott névvel és hellyel.</span><span class="sxs-lookup"><span data-stu-id="40e4b-122">The first command creates a resource group with the specified name and location.</span></span>
* <span data-ttu-id="40e4b-123">A második parancs a **New-AzStorageAccount** parancsmagot használja a tárolási fiók létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="40e4b-123">The second command uses the **New-AzStorageAccount** cmdlet to create a storage account.</span></span>
* <span data-ttu-id="40e4b-124">A harmadik parancs ezt követően a **Get-AzStorageAccount** parancsmagot használja a második parancsban létrehozott tárterület-fiók beszerzéséhez, és az eredményt a $STOAccount változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="40e4b-124">The third command then uses the **Get-AzStorageAccount** cmdlet to get the storage account created in the second command and stores the result in the $STOAccount variable.</span></span>
* <span data-ttu-id="40e4b-125">Az ötödik parancs a **New-AzVirtualNetworkSubnetConfig** parancsmagot használja alhálózat létrehozásához, és az eredményt az $SubNet nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="40e4b-125">The fifth command uses the **New-AzVirtualNetworkSubnetConfig** cmdlet to create a subnet and stores the result in the variable named $SubNet.</span></span>
* <span data-ttu-id="40e4b-126">A hatodik parancs a **New-AzVirtualNetwork** parancsmagot használja virtuális hálózat létrehozásához, és az eredményt az $VNet nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="40e4b-126">The sixth command uses the **New-AzVirtualNetwork** cmdlet to create a virtual network and stores the result in the variable named $VNet.</span></span>
* <span data-ttu-id="40e4b-127">A hetedik parancs a **Get-AzVirtualNetwork** használatával információkat kaphat a hatodik parancsban létrehozott virtuális hálózatról, és az adatokat a $VNet nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="40e4b-127">The seventh command uses the **Get-AzVirtualNetwork** to get information about the virtual network created in the sixth command and stores the information in the variable named $VNet.</span></span>
* <span data-ttu-id="40e4b-128">A nyolcadik és a kilencedik parancs a **New-AzPublicIpAddress** és a **Get-AzureRmPublicIpAddress** használatával hozza létre és kapja meg az adott nyilvános IP-címről származó információkat.</span><span class="sxs-lookup"><span data-stu-id="40e4b-128">The eighth and ninth command uses the **New-AzPublicIpAddress** and **Get- AzureRmPublicIpAddress** to create and get information from that public IP address.</span></span>
* <span data-ttu-id="40e4b-129">A parancsok a $PubIP nevű változóban tárolják az adatokat.</span><span class="sxs-lookup"><span data-stu-id="40e4b-129">The commands store the information in the variable named $PubIP.</span></span>
* <span data-ttu-id="40e4b-130">A tizedik parancs a **New-AzureRmLoadBalancerFrontendIpConfig** parancsmagot használja egy frontend terheléselosztás létrehozásához, és az eredményt az $frontend nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="40e4b-130">The tenth command uses the **New- AzureRmLoadBalancerFrontendIpConfig** cmdlet to create a frontend load balancer and stores the result in the variable named $Frontend.</span></span>
* <span data-ttu-id="40e4b-131">A tizenegyedik parancs a **New-AzLoadBalancerBackendAddressPoolConfig** segítségével hozza létre a backend-címkészlet konfigurációját, és az eredményt az $BackendAddressPool nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="40e4b-131">The eleventh command uses the **New-AzLoadBalancerBackendAddressPoolConfig** to create a backend address pool configuration and stores the result in the variable named $BackendAddressPool.</span></span>
* <span data-ttu-id="40e4b-132">A tizenkettedik parancs a **New-AzLoadBalancerProbeConfig** használatával létrehoz egy szondát, és a szonda adatait a $Probe nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="40e4b-132">The twelfth command uses the **New-AzLoadBalancerProbeConfig** to create a probe and stores the probe information in the variable named $Probe.</span></span>
* <span data-ttu-id="40e4b-133">A tizenharmadik parancs a **New-AzLoadBalancerInboundNatPoolConfig** parancsmagot használja a terheléselosztó bejövő hálózati címfordítási (NAT) alkalmazáskészlet-konfiguráció létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="40e4b-133">The thirteenth command uses the **New-AzLoadBalancerInboundNatPoolConfig** cmdlet to create a load balancer inbound network address translation (NAT) pool configuration.</span></span>
* <span data-ttu-id="40e4b-134">A tizennegyedik parancs a **New-AzLoadBalancerRuleConfig** segítségével hoz létre terheléselosztó szabály-konfigurációt, és az eredményt az $LBRule nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="40e4b-134">The fourteenth command uses the **New-AzLoadBalancerRuleConfig** to create a load balancer rule configuration and stores the result in the variable named $LBRule.</span></span>
* <span data-ttu-id="40e4b-135">A tizenötödik parancs a **New-AzLoadBalancer** parancsmagot használja a terheléselosztó létrehozásához, és az eredményt az $ActualLb nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="40e4b-135">The fifteenth command uses the **New-AzLoadBalancer** cmdlet to create a load balancer and stores the result in the variable named $ActualLb.</span></span>
* <span data-ttu-id="40e4b-136">A tizenhatodik parancs a **Get-AzLoadBalancer** használatával információkat kaphat a tizenötödik parancsban létrehozott terheléselosztó rendszerről, és az adatokat a $ExpectedLb nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="40e4b-136">The sixteenth command uses the **Get-AzLoadBalancer** to get information about the load balancer that was created in the fifteenth command and stores the information in the variable named $ExpectedLb.</span></span>
* <span data-ttu-id="40e4b-137">A tizenhetedik parancs a **New-AzVmssIPConfig** parancsmagot használja a VMSS IP-konfigurációjának létrehozásához, és az adatokat a $IPCfg nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="40e4b-137">The seventeenth command uses the **New-AzVmssIPConfig** cmdlet to create a VMSS IP configuration and stores the information in the variable named $IPCfg.</span></span>
* <span data-ttu-id="40e4b-138">A XVIII parancs a **New-AzVmssConfig** parancsmagot használja VMSS konfigurációs objektum létrehozásához, és az eredményt az $VMSS nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="40e4b-138">The eighteenth command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
* <span data-ttu-id="40e4b-139">A tizenkilencedik parancs a **New-AzVmss** parancsmagot használja a VMSS létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="40e4b-139">The nineteenth command uses the **New-AzVmss** cmdlet to create the VMSS.</span></span>

## <span data-ttu-id="40e4b-140">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="40e4b-140">PARAMETERS</span></span>

### <span data-ttu-id="40e4b-141">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="40e4b-141">-AllocationMethod</span></span>
<span data-ttu-id="40e4b-142">A méretarány (statikus vagy dinamikus) nyilvános IP-címének kiosztási módja.</span><span class="sxs-lookup"><span data-stu-id="40e4b-142">Allocation method for the Public IP Address of the Scale Set (Static or Dynamic).</span></span>  <span data-ttu-id="40e4b-143">Ha nincs megadva érték, akkor a felosztás statikus lesz.</span><span class="sxs-lookup"><span data-stu-id="40e4b-143">If no value is supplied, allocation will be static.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:
Accepted values: Static, Dynamic

Required: False
Position: Named
Default value: Static
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40e4b-144">-AsJob</span><span class="sxs-lookup"><span data-stu-id="40e4b-144">-AsJob</span></span>
<span data-ttu-id="40e4b-145">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="40e4b-145">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="40e4b-146">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="40e4b-146">-BackendPoolName</span></span>
<span data-ttu-id="40e4b-147">Annak a backend-címkészlet a neve, amelyet az ehhez a léptékhez tartozó terheléselosztásban szeretne használni.</span><span class="sxs-lookup"><span data-stu-id="40e4b-147">The name of the backend address pool to use in the load balancer for this Scale Set.</span></span>  <span data-ttu-id="40e4b-148">Ha nincs megadva érték, akkor létrejön egy új backend-készlet, amelynek a neve megegyezik a méretarány beállítással.</span><span class="sxs-lookup"><span data-stu-id="40e4b-148">If no value is provided, a new backend pool will be created, with the same name as the Scale Set.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40e4b-149">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="40e4b-149">-BackendPort</span></span>
<span data-ttu-id="40e4b-150">A kiegyenlítő terheléselosztás által a VM-tel való kommunikációhoz a méretarány beállítása által használt backend-portok száma.</span><span class="sxs-lookup"><span data-stu-id="40e4b-150">Backend port numbers used by the Scale Set load balancer to communicate with VMs in the Scale Set.</span></span>  <span data-ttu-id="40e4b-151">Ha nincs megadva érték, akkor a rendszer a 3389 és az 5985-es portot fogja használni a Windows VMS rendszerhez, és a 22-ös portot fogja használni a Linux VM-hez.</span><span class="sxs-lookup"><span data-stu-id="40e4b-151">If no values are specified, ports 3389 and 5985 will be used for Windows VMS, and port 22 will be used for Linux VMs.</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40e4b-152">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="40e4b-152">-Credential</span></span>
<span data-ttu-id="40e4b-153">A virtuális VMs-rendszerhez tartozó rendszergazdai hitelesítő adatok (Felhasználónév és jelszó) ebben a méretarányban jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="40e4b-153">The administrator credentials (username and password) for VMs in this Scale Set.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: SimpleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40e4b-154">-DataDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="40e4b-154">-DataDiskSizeInGb</span></span>
<span data-ttu-id="40e4b-155">Az adatlemezek méretét adja meg GB-ban.</span><span class="sxs-lookup"><span data-stu-id="40e4b-155">Specifies the sizes of data disks in GB.</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40e4b-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40e4b-156">-DefaultProfile</span></span>
<span data-ttu-id="40e4b-157">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="40e4b-157">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40e4b-158">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="40e4b-158">-DomainNameLabel</span></span>
<span data-ttu-id="40e4b-159">A nyilvános Fully-Qualified tartománynév címkéje (FQDN) ehhez a méretarányhoz.</span><span class="sxs-lookup"><span data-stu-id="40e4b-159">The domain name label for the public Fully-Qualified domain name (FQDN) for this Scale Set.</span></span> <span data-ttu-id="40e4b-160">Ez a tartománynév első olyan része, amelyet a program automatikusan hozzárendel a méretarányhoz.</span><span class="sxs-lookup"><span data-stu-id="40e4b-160">This is the first component of the domain name that is automatically assigned to the Scale Set.</span></span> <span data-ttu-id="40e4b-161">Automatikusan hozzárendelt tartománynevek: használja az űrlapot ( <DomainNameLabel> . <Location> . cloudapp.azure.com).</span><span class="sxs-lookup"><span data-stu-id="40e4b-161">Automatically assigned Domain names use the form (<DomainNameLabel>.<Location>.cloudapp.azure.com).</span></span> <span data-ttu-id="40e4b-162">Ha nincs megadva érték, az alapértelmezett tartománynév-címke lesz az ÖSSZEFŰZ <ScaleSetName> és a <ResourceGroupName> .</span><span class="sxs-lookup"><span data-stu-id="40e4b-162">If no value is supplied, the default domain name label will be the concatenation of <ScaleSetName> and <ResourceGroupName>.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40e4b-163">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="40e4b-163">-EnableUltraSSD</span></span>
<span data-ttu-id="40e4b-164">A UltraSSD-lemezek használata a virtuális VMs-rendszerhez a méretarány készletében</span><span class="sxs-lookup"><span data-stu-id="40e4b-164">Use UltraSSD disks for the VMs in the scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40e4b-165">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="40e4b-165">-EncryptionAtHost</span></span>
<span data-ttu-id="40e4b-166">Ez a paraméter lehetővé teszi az összes lemez titkosítását, például az erőforrás/Temp diskt az állomáson.</span><span class="sxs-lookup"><span data-stu-id="40e4b-166">This parameter will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> <span data-ttu-id="40e4b-167">Alapértelmezés: az állomáson a titkosítás le lesz tiltva, kivéve ha a tulajdonság értéke igaz az erőforrás esetében.</span><span class="sxs-lookup"><span data-stu-id="40e4b-167">Default: The Encryption at host will be disabled unless this property is set to true for the resource.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40e4b-168">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="40e4b-168">-EvictionPolicy</span></span>
<span data-ttu-id="40e4b-169">A kilakoltatási házirend az alacsony prioritású virtuálisgép-készlethez.</span><span class="sxs-lookup"><span data-stu-id="40e4b-169">The eviction policy for the low priority virtual machine scale set.</span></span>  <span data-ttu-id="40e4b-170">Csak a támogatott értékek "defoglalása" és "Törlés".</span><span class="sxs-lookup"><span data-stu-id="40e4b-170">Only supported values are 'Deallocate' and 'Delete'.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40e4b-171">-FrontendPoolName</span><span class="sxs-lookup"><span data-stu-id="40e4b-171">-FrontendPoolName</span></span>
<span data-ttu-id="40e4b-172">A Scale set terheléselosztó bővítményben használandó felületi címkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="40e4b-172">The name of the frontend address pool to use in the Scale Set load balancer.</span></span>  <span data-ttu-id="40e4b-173">Ha nincs megadva érték, akkor létrejön egy új felületi címkészlet, amelynek a neve megegyezik a méretarány beállítással.</span><span class="sxs-lookup"><span data-stu-id="40e4b-173">If no value is supplied, a new Frontend Address Pool will be created, with the same name as the scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40e4b-174">-HostGroupId</span><span class="sxs-lookup"><span data-stu-id="40e4b-174">-HostGroupId</span></span>
<span data-ttu-id="40e4b-175">A virtuális gép méretarányát tároló dedikált csoport.</span><span class="sxs-lookup"><span data-stu-id="40e4b-175">Specifies the dedicated host group the virtual machine scale set will reside in.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases: HostGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### <span data-ttu-id="40e4b-176">-ImageName</span><span class="sxs-lookup"><span data-stu-id="40e4b-176">-ImageName</span></span>
<span data-ttu-id="40e4b-177">A virtuális VM-fájl neve ebben a méretarányban.</span><span class="sxs-lookup"><span data-stu-id="40e4b-177">The name of the image for VMs in this Scale Set.</span></span> <span data-ttu-id="40e4b-178">Ha nincs megadva érték, a program a "Windows Server 2016-adatközpont" képet fogja használni.</span><span class="sxs-lookup"><span data-stu-id="40e4b-178">If no value is provided, the "Windows Server 2016 DataCenter" image will be used.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40e4b-179">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="40e4b-179">-InstanceCount</span></span>
<span data-ttu-id="40e4b-180">A virtuális VM-képek száma a méretarányban.</span><span class="sxs-lookup"><span data-stu-id="40e4b-180">The number of VM images in the Scale Set.</span></span>  <span data-ttu-id="40e4b-181">Ha nincs megadva érték, akkor két példány jön létre.</span><span class="sxs-lookup"><span data-stu-id="40e4b-181">If no value is provided, 2 instances will be created.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: 2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40e4b-182">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="40e4b-182">-LoadBalancerName</span></span>
<span data-ttu-id="40e4b-183">Az ezzel a Méretaránysal használandó terheléselosztó neve.</span><span class="sxs-lookup"><span data-stu-id="40e4b-183">The name of the load balancer to use with this Scale Set.</span></span>  <span data-ttu-id="40e4b-184">Új terheléselosztó a méretarány nevének megadásával, ha a program nem ad meg értéket.</span><span class="sxs-lookup"><span data-stu-id="40e4b-184">A new load balancer using the same name as the Scale Set will be created if no value is specified.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40e4b-185">-Hely</span><span class="sxs-lookup"><span data-stu-id="40e4b-185">-Location</span></span>
<span data-ttu-id="40e4b-186">Az Azure-hely, ahol ez a méretarány jön létre.</span><span class="sxs-lookup"><span data-stu-id="40e4b-186">The Azure location where this Scale Set will be created.</span></span>  <span data-ttu-id="40e4b-187">Ha nincs megadva érték, a program a paraméterben hivatkozott további források helyétől kikövetkezteti a helyet.</span><span class="sxs-lookup"><span data-stu-id="40e4b-187">If no value is specified, the location will be inferred from the location of other resources referenced in the parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40e4b-188">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="40e4b-188">-MaxPrice</span></span>
<span data-ttu-id="40e4b-189">A legalacsonyabb prioritású virtuálisgép-készlet számlázásának maximális ára.</span><span class="sxs-lookup"><span data-stu-id="40e4b-189">The max price of the billing of a low priority virtual machine scale set.</span></span>

```yaml
Type: System.Double
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40e4b-190">-NatBackendPort</span><span class="sxs-lookup"><span data-stu-id="40e4b-190">-NatBackendPort</span></span>
<span data-ttu-id="40e4b-191">A bejövő hálózati címfordításhoz tartozó backend port.</span><span class="sxs-lookup"><span data-stu-id="40e4b-191">Backend port for inbound network address translation.</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40e4b-192">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="40e4b-192">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="40e4b-193">Az egyes helyekhez tartozó hibák tartománya.</span><span class="sxs-lookup"><span data-stu-id="40e4b-193">Fault Domain count for each placement group.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40e4b-194">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="40e4b-194">-Priority</span></span>
<span data-ttu-id="40e4b-195">A virtuális gép prioritása a méretarány beállításban.</span><span class="sxs-lookup"><span data-stu-id="40e4b-195">The priority for the virtual machine in the scale set.</span></span>  <span data-ttu-id="40e4b-196">Csak a támogatott értékek "normál", "spot" és "Low".</span><span class="sxs-lookup"><span data-stu-id="40e4b-196">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="40e4b-197">"Normál": a normál virtuális gép.</span><span class="sxs-lookup"><span data-stu-id="40e4b-197">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="40e4b-198">A "spot" a direkt virtuális gép.</span><span class="sxs-lookup"><span data-stu-id="40e4b-198">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="40e4b-199">Az "alacsony" a direkt virtuális gép is, de a helyére "spot" lép.</span><span class="sxs-lookup"><span data-stu-id="40e4b-199">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="40e4b-200">Kérjük, hogy az "alacsony" helyett a "spot" értéket használja.</span><span class="sxs-lookup"><span data-stu-id="40e4b-200">Please use 'Spot' instead of 'Low'.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40e4b-201">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="40e4b-201">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="40e4b-202">Annak a közelségi helynek az erőforrás azonosítója, amellyel az adott méretarányt használni szeretné.</span><span class="sxs-lookup"><span data-stu-id="40e4b-202">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases: ProximityPlacementGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40e4b-203">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="40e4b-203">-PublicIpAddressName</span></span>
<span data-ttu-id="40e4b-204">Annak a nyilvános IP-címnek a neve, amellyel az adott méretarányt be szeretné használni.</span><span class="sxs-lookup"><span data-stu-id="40e4b-204">The name of the public IP Address to use with this scale set.</span></span>  <span data-ttu-id="40e4b-205">Ha nincs megadva érték, akkor létrejön egy új nyilvános IP-azonosító a méretarány nevével.</span><span class="sxs-lookup"><span data-stu-id="40e4b-205">A new Public IPAddress with the same name as the Scale Set will be created if no value is provided.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40e4b-206">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40e4b-206">-ResourceGroupName</span></span>
<span data-ttu-id="40e4b-207">A VMSS erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="40e4b-207">Specifies the name of the resource group of the VMSS.</span></span>  <span data-ttu-id="40e4b-208">Ha nincs megadva érték, új ResourceGroup fog létrejönni a méretarány nevével.</span><span class="sxs-lookup"><span data-stu-id="40e4b-208">If no value is specified, a new ResourceGroup will be created using the same name as the Scale Set.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40e4b-209">-ScaleInPolicy</span><span class="sxs-lookup"><span data-stu-id="40e4b-209">-ScaleInPolicy</span></span>
<span data-ttu-id="40e4b-210">A virtuális gép méretarányának beállításakor követendő szabályok.</span><span class="sxs-lookup"><span data-stu-id="40e4b-210">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="40e4b-211">A lehetséges értékek a következők: "alapértelmezett", "OldestVM" és "NewestVM".</span><span class="sxs-lookup"><span data-stu-id="40e4b-211">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="40e4b-212">"Alapértelmezett": Ha egy virtuális gép méretarányát a program átméretezi, a program először a méretarányokat fogja kiegyensúlyozni a zónáknál, ha a zóna zóna.</span><span class="sxs-lookup"><span data-stu-id="40e4b-212">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="40e4b-213">Ezt követően a lehető legtöbbet fogja kiegyensúlyozni a hibák tartományában.</span><span class="sxs-lookup"><span data-stu-id="40e4b-213">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="40e4b-214">Az egyes hibák tartománya alatt az eltávolításra kiválasztott virtuális gépek a legújabbak lesznek, amelyek nem védettek a méretarányban.</span><span class="sxs-lookup"><span data-stu-id="40e4b-214">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="40e4b-215">"OldestVM": Ha egy virtuálisgép-készletet méretarányos, a program a legrégebbi virtuális gépeket választja, amelyek nem védettek a méretarányban.</span><span class="sxs-lookup"><span data-stu-id="40e4b-215">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="40e4b-216">A virtuális gép méretarányos készletei esetében a méretarány először a zónáknál lesz kiegyensúlyozott.</span><span class="sxs-lookup"><span data-stu-id="40e4b-216">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="40e4b-217">Az egyes zónákon belül a legrégebbi virtuális gépeket választják ki a program az eltávolításhoz.</span><span class="sxs-lookup"><span data-stu-id="40e4b-217">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="40e4b-218">"NewestVM": Ha egy virtuálisgép-készletet méretezéssel végeznek, a program az eltávolításhoz a legújabb virtuális gépeket választja, amelyek nem védettek a méretarányban.</span><span class="sxs-lookup"><span data-stu-id="40e4b-218">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="40e4b-219">A virtuális gép méretarányos készletei esetében a méretarány először a zónáknál lesz kiegyensúlyozott.</span><span class="sxs-lookup"><span data-stu-id="40e4b-219">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="40e4b-220">Az egyes zónákon belül a legújabb virtuális gépek, amelyek nem védettek, kiválasztásra kerülnek az eltávolításhoz.</span><span class="sxs-lookup"><span data-stu-id="40e4b-220">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40e4b-221">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="40e4b-221">-SecurityGroupName</span></span>
<span data-ttu-id="40e4b-222">Annak a hálózati biztonsági csoportnak a neve, amelyre alkalmazni szeretné ezt a méretarányt.</span><span class="sxs-lookup"><span data-stu-id="40e4b-222">The name of the network security group to apply to this Scale Set.</span></span>  <span data-ttu-id="40e4b-223">Ha nincs megadva érték, akkor létrejön egy alapértelmezett hálózati biztonsági csoport, amelynek a mérete megegyezik a méretarány beállítással.</span><span class="sxs-lookup"><span data-stu-id="40e4b-223">If no value is provided, a default network security group with the same name as the Scale Set will be created and applied to the Scale Set.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40e4b-224">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="40e4b-224">-SinglePlacementGroup</span></span>
<span data-ttu-id="40e4b-225">Ezzel a beállítással létrehozhatja a méretarányt egyetlen Elhelyezés csoportban, az alapértelmezett beállítás több csoport</span><span class="sxs-lookup"><span data-stu-id="40e4b-225">Use this to create the Scale set in a single placement group, default is multiple groups</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40e4b-226">-SkipExtensionsOnOverprovisionedVMs</span><span class="sxs-lookup"><span data-stu-id="40e4b-226">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="40e4b-227">Azt adja meg, hogy a bővítmények nem futnak az extra túlépített VMs-eszközön.</span><span class="sxs-lookup"><span data-stu-id="40e4b-227">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40e4b-228">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="40e4b-228">-SubnetAddressPrefix</span></span>
<span data-ttu-id="40e4b-229">Annak az alhálózatnak az előtagja, amelyet a ScaleSet használni fog.</span><span class="sxs-lookup"><span data-stu-id="40e4b-229">The address prefix of the Subnet this ScaleSet will use.</span></span> <span data-ttu-id="40e4b-230">Az alapértelmezett alhálózati beállítások (192.168.1.0/24) akkor érvényesek, ha nincs megadva érték.</span><span class="sxs-lookup"><span data-stu-id="40e4b-230">Default Subnet settings (192.168.1.0/24) will be applied if no value is provided.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.1.0/24
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40e4b-231">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="40e4b-231">-SubnetName</span></span>
<span data-ttu-id="40e4b-232">Annak az alhálózatnak a neve, amely az adott méretarányt használja.</span><span class="sxs-lookup"><span data-stu-id="40e4b-232">The name of the subnet to use with this Scale Set.</span></span>  <span data-ttu-id="40e4b-233">Ha nincs megadva érték, akkor létrejön egy új alhálózat a méretarány-készlet nevével.</span><span class="sxs-lookup"><span data-stu-id="40e4b-233">A new Subnet will be created with the same name as the Scale Set if no value is provided.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40e4b-234">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="40e4b-234">-SystemAssignedIdentity</span></span>
<span data-ttu-id="40e4b-235">Ha a paraméter megtalálható, akkor a méretarányban a VM (s) a (a) rendszer automatikusan generált felügyelt rendszeridentitást rendel.</span><span class="sxs-lookup"><span data-stu-id="40e4b-235">If the parameter is present then the VM(s) in the scale set is(are) assigned a managed system identity that is auto generated.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40e4b-236">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="40e4b-236">-UpgradePolicyMode</span></span>
<span data-ttu-id="40e4b-237">Ebben a méretarányban a VM-példányokra vonatkozó frissítési házirend üzemmódot adja meg.</span><span class="sxs-lookup"><span data-stu-id="40e4b-237">The upgrade policy mode for VM instances in this Scale Set.</span></span>  <span data-ttu-id="40e4b-238">A frissítési házirend az automatikus, a manuális vagy a folyamatos frissítést is megadhatja.</span><span class="sxs-lookup"><span data-stu-id="40e4b-238">Upgrade policy could specify Automatic, Manual, or Rolling upgrades.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.UpgradeMode
Parameter Sets: SimpleParameterSet
Aliases:
Accepted values: Automatic, Manual, Rolling

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40e4b-239">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="40e4b-239">-UserAssignedIdentity</span></span>
<span data-ttu-id="40e4b-240">Annak a felügyelt szolgáltatás-identitásnak a neve, amelyet ki kell osztani a VM (ek) nek a méretarányban.</span><span class="sxs-lookup"><span data-stu-id="40e4b-240">The name of a managed service identity that should be assigned to the VM(s) in the scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40e4b-241">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="40e4b-241">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="40e4b-242">Azt a **VirtualMachineScaleSet** -objektumot adja meg, amely a parancsmag által létrehozott VMSS tulajdonságait tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="40e4b-242">Specifies the **VirtualMachineScaleSet** object that contains the properties of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="40e4b-243">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="40e4b-243">-VirtualNetworkName</span></span>
<span data-ttu-id="40e4b-244">Annak a virtuális hálózatnak a neve, amellyel az adott méretarányt használni szeretné.</span><span class="sxs-lookup"><span data-stu-id="40e4b-244">The name fo the Virtual Network to use with this scale set.</span></span>  <span data-ttu-id="40e4b-245">Ha nincs megadva érték, akkor létrejön egy új virtuális hálózat, amelynek a neve megegyezik a méretarány-Halmazsal.</span><span class="sxs-lookup"><span data-stu-id="40e4b-245">If no value is supplied, a new virtual network with the same name as the Scale Set will be created.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40e4b-246">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="40e4b-246">-VMScaleSetName</span></span>
<span data-ttu-id="40e4b-247">Annak a VMSS a nevét adja meg, amelyet a parancsmag hoz létre.</span><span class="sxs-lookup"><span data-stu-id="40e4b-247">Specifies the name of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40e4b-248">-VmSize</span><span class="sxs-lookup"><span data-stu-id="40e4b-248">-VmSize</span></span>
<span data-ttu-id="40e4b-249">A megadott méretarányban a VM-példányok mérete.</span><span class="sxs-lookup"><span data-stu-id="40e4b-249">The size of the VM instances in this scale set.</span></span>  <span data-ttu-id="40e4b-250">Ha nincs megadva méret, az alapértelmezett méret (Standard_DS1_v2) lesz használatos.</span><span class="sxs-lookup"><span data-stu-id="40e4b-250">A default size (Standard_DS1_v2) will be used if no Size is specified.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: Standard_DS1_v2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40e4b-251">-VnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="40e4b-251">-VnetAddressPrefix</span></span>
<span data-ttu-id="40e4b-252">A megadott Méretaránysal használt virtuális hálózathoz tartozó cím előtagja.</span><span class="sxs-lookup"><span data-stu-id="40e4b-252">The address prefix for the virtual network used with this Scale Set.</span></span>  <span data-ttu-id="40e4b-253">Az alapértelmezett virtuális hálózati cím előtag-beállításai (192.168.0.0/16) akkor lesznek használatban, ha nincs megadva érték.</span><span class="sxs-lookup"><span data-stu-id="40e4b-253">Default virtual network address prefix settings (192.168.0.0/16) will be used if no value is supplied.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.0.0/16
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40e4b-254">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="40e4b-254">-Zone</span></span>
<span data-ttu-id="40e4b-255">Az erőforráshoz hozzárendelt IP-címet jelölő elérhetőségi zónák listája.</span><span class="sxs-lookup"><span data-stu-id="40e4b-255">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="40e4b-256">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="40e4b-256">-Confirm</span></span>
<span data-ttu-id="40e4b-257">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="40e4b-257">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40e4b-258">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40e4b-258">-WhatIf</span></span>
<span data-ttu-id="40e4b-259">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="40e4b-259">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40e4b-260">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="40e4b-260">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40e4b-261">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40e4b-261">CommonParameters</span></span>
<span data-ttu-id="40e4b-262">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="40e4b-262">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40e4b-263">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="40e4b-263">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40e4b-264">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="40e4b-264">INPUTS</span></span>

### <span data-ttu-id="40e4b-265">System. String</span><span class="sxs-lookup"><span data-stu-id="40e4b-265">System.String</span></span>

### <span data-ttu-id="40e4b-266">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="40e4b-266">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="40e4b-267">System. Collections. Generic. list ' 1 [[System. string, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="40e4b-267">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="40e4b-268">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="40e4b-268">OUTPUTS</span></span>

### <span data-ttu-id="40e4b-269">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="40e4b-269">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="40e4b-270">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="40e4b-270">NOTES</span></span>

## <span data-ttu-id="40e4b-271">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="40e4b-271">RELATED LINKS</span></span>

[<span data-ttu-id="40e4b-272">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="40e4b-272">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="40e4b-273">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="40e4b-273">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="40e4b-274">Újraindítás – AzVmss</span><span class="sxs-lookup"><span data-stu-id="40e4b-274">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="40e4b-275">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="40e4b-275">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="40e4b-276">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="40e4b-276">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="40e4b-277">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="40e4b-277">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="40e4b-278">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="40e4b-278">Update-AzVmss</span></span>](./Update-AzVmss.md)


