---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1A2C843C-6962-4B0E-ACBF-A5EFF609A5BE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmss.md
ms.openlocfilehash: 97e10d75d17748f1a9e96ada498afe456700f61d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836743"
---
# <span data-ttu-id="fe24f-101">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fe24f-101">New-AzVmss</span></span>

## <span data-ttu-id="fe24f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fe24f-102">SYNOPSIS</span></span>
<span data-ttu-id="fe24f-103">Létrehoz egy VMSS.</span><span class="sxs-lookup"><span data-stu-id="fe24f-103">Creates a VMSS.</span></span>

## <span data-ttu-id="fe24f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fe24f-104">SYNTAX</span></span>

### <span data-ttu-id="fe24f-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fe24f-105">DefaultParameter (Default)</span></span>
```
New-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe24f-106">SimpleParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe24f-106">SimpleParameterSet</span></span>
```
New-AzVmss [[-ResourceGroupName] <String>] [-VMScaleSetName] <String> [-AsJob] [-ImageName <String>]
 -Credential <PSCredential> [-InstanceCount <Int32>] [-VirtualNetworkName <String>] [-SubnetName <String>]
 [-PublicIpAddressName <String>] [-DomainNameLabel <String>] [-SecurityGroupName <String>]
 [-LoadBalancerName <String>] [-BackendPort <Int32[]>] [-Location <String>] [-VmSize <String>]
 [-UpgradePolicyMode <UpgradeMode>] [-AllocationMethod <String>] [-VnetAddressPrefix <String>]
 [-SubnetAddressPrefix <String>] [-FrontendPoolName <String>] [-BackendPoolName <String>]
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-EnableUltraSSD]
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-NatBackendPort <Int32[]>]
 [-DataDiskSizeInGb <Int32[]>] [-DefaultProfile <IAzureContextContainer>] [-SinglePlacementGroup] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe24f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="fe24f-107">DESCRIPTION</span></span>
<span data-ttu-id="fe24f-108">A **New-AzVmss** parancsmag létrehoz egy virtuálisgép-készletet (VMSS) az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="fe24f-108">The **New-AzVmss** cmdlet creates a Virtual Machine Scale Set (VMSS) in Azure.</span></span>
<span data-ttu-id="fe24f-109">Az egyszerű típusparaméter ( `SimpleParameterSet` ) segítségével gyorsan létrehozhat előre beállított VMSS és kapcsolódó erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="fe24f-109">Use the simple parameter set (`SimpleParameterSet`) to quickly create a pre-set VMSS and associated resources.</span></span> <span data-ttu-id="fe24f-110">Az alapértelmezett paramétert () akkor használja, `DefaultParameter` Ha a VMSS és a hozzájuk rendelt erőforrások mindegyik összetevőjének pontos konfigurálására van szükség a létrehozás előtt.</span><span class="sxs-lookup"><span data-stu-id="fe24f-110">Use the default parameter set (`DefaultParameter`) for more advanced scenarios when you need to precisely configure each component of the VMSS and each associated resource before creation.</span></span>

## <span data-ttu-id="fe24f-111">Példák</span><span class="sxs-lookup"><span data-stu-id="fe24f-111">EXAMPLES</span></span>

### <span data-ttu-id="fe24f-112">Példa 1: VMSS létrehozása a **`SimpleParameterSet`**</span><span class="sxs-lookup"><span data-stu-id="fe24f-112">Example 1: Create a VMSS using the **`SimpleParameterSet`**</span></span>
```powershell
$vmssName = <VMSSNAME>
# Create credentials, I am using one way to create credentials, there are others as well. 
# Pick one that makes the most sense according to your use case.
$vmPassword = ConvertTo-SecureString <PASSWORD_HERE> -AsPlainText -Force
$vmCred = New-Object System.Management.Automation.PSCredential(<USERNAME_HERE>, $vmPassword)

#Create a VMSS using the default settings
New-AzVmss -Credential $vmCred -VMScaleSetName $vmssName
```

<span data-ttu-id="fe24f-113">A fenti parancs a következőképpen hozza létre a nevet `$vmssName` :</span><span class="sxs-lookup"><span data-stu-id="fe24f-113">The command above creates the following with the name `$vmssName` :</span></span>
* <span data-ttu-id="fe24f-114">Erőforráscsoport</span><span class="sxs-lookup"><span data-stu-id="fe24f-114">A Resource Group</span></span>
* <span data-ttu-id="fe24f-115">Virtuális hálózat</span><span class="sxs-lookup"><span data-stu-id="fe24f-115">A virtual network</span></span>
* <span data-ttu-id="fe24f-116">A terheléselosztó</span><span class="sxs-lookup"><span data-stu-id="fe24f-116">A load balancer</span></span>
* <span data-ttu-id="fe24f-117">Nyilvános IP-cím</span><span class="sxs-lookup"><span data-stu-id="fe24f-117">A public IP</span></span>
* <span data-ttu-id="fe24f-118">a VMSS két példányban</span><span class="sxs-lookup"><span data-stu-id="fe24f-118">the VMSS with 2 instances</span></span>

<span data-ttu-id="fe24f-119">A VMSS a VMs-rendszerhez kiválasztott alapértelmezett kép `2016-Datacenter Windows Server` és a SKU `Standard_DS1_v2`</span><span class="sxs-lookup"><span data-stu-id="fe24f-119">The default image chosen for the VMs in the VMSS is `2016-Datacenter Windows Server` and the SKU is `Standard_DS1_v2`</span></span>

### <span data-ttu-id="fe24f-120">2. példa: VMSS létrehozása a **`DefaultParameterSet`**</span><span class="sxs-lookup"><span data-stu-id="fe24f-120">Example 2: Create a VMSS using the **`DefaultParameterSet`**</span></span>
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
$VMSS = New-AzVmssConfig -Location $LOC -SkuCapacity 2 -SkuName "Standard_A2" -UpgradePolicyMode "Automatic" `
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

<span data-ttu-id="fe24f-121">A fenti komplex példa létrehoz egy VMSS, az alábbi magyarázattal a mi történik:</span><span class="sxs-lookup"><span data-stu-id="fe24f-121">The complex example above creates a VMSS, following is an explanation of what is happening:</span></span>
* <span data-ttu-id="fe24f-122">Az első parancs létrehoz egy erőforráscsoportot a megadott névvel és hellyel.</span><span class="sxs-lookup"><span data-stu-id="fe24f-122">The first command creates a resource group with the specified name and location.</span></span>
* <span data-ttu-id="fe24f-123">A második parancs a **New-AzStorageAccount** parancsmagot használja a tárolási fiók létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="fe24f-123">The second command uses the **New-AzStorageAccount** cmdlet to create a storage account.</span></span>
* <span data-ttu-id="fe24f-124">A harmadik parancs ezt követően a **Get-AzStorageAccount** parancsmagot használja a második parancsban létrehozott tárterület-fiók beszerzéséhez, és az eredményt a $STOAccount változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="fe24f-124">The third command then uses the **Get-AzStorageAccount** cmdlet to get the storage account created in the second command and stores the result in the $STOAccount variable.</span></span>
* <span data-ttu-id="fe24f-125">Az ötödik parancs a **New-AzVirtualNetworkSubnetConfig** parancsmagot használja alhálózat létrehozásához, és az eredményt az $SubNet nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="fe24f-125">The fifth command uses the **New-AzVirtualNetworkSubnetConfig** cmdlet to create a subnet and stores the result in the variable named $SubNet.</span></span>
* <span data-ttu-id="fe24f-126">A hatodik parancs a **New-AzVirtualNetwork** parancsmagot használja virtuális hálózat létrehozásához, és az eredményt az $VNet nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="fe24f-126">The sixth command uses the **New-AzVirtualNetwork** cmdlet to create a virtual network and stores the result in the variable named $VNet.</span></span>
* <span data-ttu-id="fe24f-127">A hetedik parancs a **Get-AzVirtualNetwork** használatával információkat kaphat a hatodik parancsban létrehozott virtuális hálózatról, és az adatokat a $VNet nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="fe24f-127">The seventh command uses the **Get-AzVirtualNetwork** to get information about the virtual network created in the sixth command and stores the information in the variable named $VNet.</span></span>
* <span data-ttu-id="fe24f-128">A nyolcadik és a kilencedik parancs a **New-AzPublicIpAddress** és a **Get-AzureRmPublicIpAddress** használatával hozza létre és kapja meg az adott nyilvános IP-címről származó információkat.</span><span class="sxs-lookup"><span data-stu-id="fe24f-128">The eighth and ninth command uses the **New-AzPublicIpAddress** and **Get- AzureRmPublicIpAddress** to create and get information from that public IP address.</span></span>
* <span data-ttu-id="fe24f-129">A parancsok a $PubIP nevű változóban tárolják az adatokat.</span><span class="sxs-lookup"><span data-stu-id="fe24f-129">The commands store the information in the variable named $PubIP.</span></span>
* <span data-ttu-id="fe24f-130">A tizedik parancs a **New-AzureRmLoadBalancerFrontendIpConfig** parancsmagot használja egy frontend terheléselosztás létrehozásához, és az eredményt az $frontend nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="fe24f-130">The tenth command uses the **New- AzureRmLoadBalancerFrontendIpConfig** cmdlet to create a frontend load balancer and stores the result in the variable named $Frontend.</span></span>
* <span data-ttu-id="fe24f-131">A tizenegyedik parancs a **New-AzLoadBalancerBackendAddressPoolConfig** segítségével hozza létre a backend-címkészlet konfigurációját, és az eredményt az $BackendAddressPool nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="fe24f-131">The eleventh command uses the **New-AzLoadBalancerBackendAddressPoolConfig** to create a backend address pool configuration and stores the result in the variable named $BackendAddressPool.</span></span>
* <span data-ttu-id="fe24f-132">A tizenkettedik parancs a **New-AzLoadBalancerProbeConfig** használatával létrehoz egy szondát, és a szonda adatait a $Probe nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="fe24f-132">The twelfth command uses the **New-AzLoadBalancerProbeConfig** to create a probe and stores the probe information in the variable named $Probe.</span></span>
* <span data-ttu-id="fe24f-133">A tizenharmadik parancs a **New-AzLoadBalancerInboundNatPoolConfig** parancsmagot használja a terheléselosztó bejövő hálózati címfordítási (NAT) alkalmazáskészlet-konfiguráció létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="fe24f-133">The thirteenth command uses the **New-AzLoadBalancerInboundNatPoolConfig** cmdlet to create a load balancer inbound network address translation (NAT) pool configuration.</span></span>
* <span data-ttu-id="fe24f-134">A tizennegyedik parancs a **New-AzLoadBalancerRuleConfig** segítségével hoz létre terheléselosztó szabály-konfigurációt, és az eredményt az $LBRule nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="fe24f-134">The fourteenth command uses the **New-AzLoadBalancerRuleConfig** to create a load balancer rule configuration and stores the result in the variable named $LBRule.</span></span>
* <span data-ttu-id="fe24f-135">A tizenötödik parancs a **New-AzLoadBalancer** parancsmagot használja a terheléselosztó létrehozásához, és az eredményt az $ActualLb nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="fe24f-135">The fifteenth command uses the **New-AzLoadBalancer** cmdlet to create a load balancer and stores the result in the variable named $ActualLb.</span></span>
* <span data-ttu-id="fe24f-136">A tizenhatodik parancs a **Get-AzLoadBalancer** használatával információkat kaphat a tizenötödik parancsban létrehozott terheléselosztó rendszerről, és az adatokat a $ExpectedLb nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="fe24f-136">The sixteenth command uses the **Get-AzLoadBalancer** to get information about the load balancer that was created in the fifteenth command and stores the information in the variable named $ExpectedLb.</span></span>
* <span data-ttu-id="fe24f-137">A tizenhetedik parancs a **New-AzVmssIPConfig** parancsmagot használja a VMSS IP-konfigurációjának létrehozásához, és az adatokat a $IPCfg nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="fe24f-137">The seventeenth command uses the **New-AzVmssIPConfig** cmdlet to create a VMSS IP configuration and stores the information in the variable named $IPCfg.</span></span>
* <span data-ttu-id="fe24f-138">A XVIII parancs a **New-AzVmssConfig** parancsmagot használja VMSS konfigurációs objektum létrehozásához, és az eredményt az $VMSS nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="fe24f-138">The eighteenth command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
* <span data-ttu-id="fe24f-139">A tizenkilencedik parancs a **New-AzVmss** parancsmagot használja a VMSS létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="fe24f-139">The nineteenth command uses the **New-AzVmss** cmdlet to create the VMSS.</span></span>

## <span data-ttu-id="fe24f-140">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fe24f-140">PARAMETERS</span></span>

### <span data-ttu-id="fe24f-141">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="fe24f-141">-AllocationMethod</span></span>
<span data-ttu-id="fe24f-142">A méretarány (statikus vagy dinamikus) nyilvános IP-címének kiosztási módja.</span><span class="sxs-lookup"><span data-stu-id="fe24f-142">Allocation method for the Public IP Address of the Scale Set (Static or Dynamic).</span></span>  <span data-ttu-id="fe24f-143">Ha nincs megadva érték, akkor a felosztás statikus lesz.</span><span class="sxs-lookup"><span data-stu-id="fe24f-143">If no value is supplied, allocation will be static.</span></span>

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

### <span data-ttu-id="fe24f-144">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fe24f-144">-AsJob</span></span>
<span data-ttu-id="fe24f-145">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="fe24f-145">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="fe24f-146">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="fe24f-146">-BackendPoolName</span></span>
<span data-ttu-id="fe24f-147">Annak a backend-címkészlet a neve, amelyet az ehhez a léptékhez tartozó terheléselosztásban szeretne használni.</span><span class="sxs-lookup"><span data-stu-id="fe24f-147">The name of the backend address pool to use in the load balancer for this Scale Set.</span></span>  <span data-ttu-id="fe24f-148">Ha nincs megadva érték, akkor létrejön egy új backend-készlet, amelynek a neve megegyezik a méretarány beállítással.</span><span class="sxs-lookup"><span data-stu-id="fe24f-148">If no value is provided, a new backend pool will be created, with the same name as the Scale Set.</span></span>

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

### <span data-ttu-id="fe24f-149">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="fe24f-149">-BackendPort</span></span>
<span data-ttu-id="fe24f-150">A kiegyenlítő terheléselosztás által a VM-tel való kommunikációhoz a méretarány beállítása által használt backend-portok száma.</span><span class="sxs-lookup"><span data-stu-id="fe24f-150">Backend port numbers used by the Scale Set load balancer to communicate with VMs in the Scale Set.</span></span>  <span data-ttu-id="fe24f-151">Ha nincs megadva érték, akkor a rendszer a 3389 és az 5985-es portot fogja használni a Windows VMS rendszerhez, és a 22-ös portot fogja használni a Linux VM-hez.</span><span class="sxs-lookup"><span data-stu-id="fe24f-151">If no values are specified, ports 3389 and 5985 will be used for Windows VMS, and port 22 will be used for Linux VMs.</span></span>

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

### <span data-ttu-id="fe24f-152">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="fe24f-152">-Credential</span></span>
<span data-ttu-id="fe24f-153">A virtuális VMs-rendszerhez tartozó rendszergazdai hitelesítő adatok (Felhasználónév és jelszó) ebben a méretarányban jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="fe24f-153">The administrator credentials (username and password) for VMs in this Scale Set.</span></span>

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

### <span data-ttu-id="fe24f-154">-DataDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="fe24f-154">-DataDiskSizeInGb</span></span>
<span data-ttu-id="fe24f-155">Az adatlemezek méretét adja meg GB-ban.</span><span class="sxs-lookup"><span data-stu-id="fe24f-155">Specifies the sizes of data disks in GB.</span></span>

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

### <span data-ttu-id="fe24f-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe24f-156">-DefaultProfile</span></span>
<span data-ttu-id="fe24f-157">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fe24f-157">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe24f-158">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="fe24f-158">-DomainNameLabel</span></span>
<span data-ttu-id="fe24f-159">A nyilvános Fully-Qualified tartománynév címkéje (FQDN) ehhez a méretarányhoz.</span><span class="sxs-lookup"><span data-stu-id="fe24f-159">The domain name label for the public Fully-Qualified domain name (FQDN) for this Scale Set.</span></span> <span data-ttu-id="fe24f-160">Ez a tartománynév első olyan része, amelyet a program automatikusan hozzárendel a méretarányhoz.</span><span class="sxs-lookup"><span data-stu-id="fe24f-160">This is the first component of the domain name that is automatically assigned to the Scale Set.</span></span> <span data-ttu-id="fe24f-161">Automatikusan hozzárendelt tartománynevek: használja az űrlapot ( <DomainNameLabel> . <Location> . cloudapp.azure.com).</span><span class="sxs-lookup"><span data-stu-id="fe24f-161">Automatically assigned Domain names use the form (<DomainNameLabel>.<Location>.cloudapp.azure.com).</span></span> <span data-ttu-id="fe24f-162">Ha nincs megadva érték, az alapértelmezett tartománynév-címke lesz az ÖSSZEFŰZ <ScaleSetName> és a <ResourceGroupName> .</span><span class="sxs-lookup"><span data-stu-id="fe24f-162">If no value is supplied, the default domain name label will be the concatenation of <ScaleSetName> and <ResourceGroupName>.</span></span>

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

### <span data-ttu-id="fe24f-163">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="fe24f-163">-EnableUltraSSD</span></span>
<span data-ttu-id="fe24f-164">A UltraSSD-lemezek használata a virtuális VMs-rendszerhez a méretarány készletében</span><span class="sxs-lookup"><span data-stu-id="fe24f-164">Use UltraSSD disks for the VMs in the scale set.</span></span>

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

### <span data-ttu-id="fe24f-165">-FrontendPoolName</span><span class="sxs-lookup"><span data-stu-id="fe24f-165">-FrontendPoolName</span></span>
<span data-ttu-id="fe24f-166">A Scale set terheléselosztó bővítményben használandó felületi címkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="fe24f-166">The name of the frontend address pool to use in the Scale Set load balancer.</span></span>  <span data-ttu-id="fe24f-167">Ha nincs megadva érték, akkor létrejön egy új felületi címkészlet, amelynek a neve megegyezik a méretarány beállítással.</span><span class="sxs-lookup"><span data-stu-id="fe24f-167">If no value is supplied, a new Frontend Address Pool will be created, with the same name as the scale set.</span></span>

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

### <span data-ttu-id="fe24f-168">-ImageName</span><span class="sxs-lookup"><span data-stu-id="fe24f-168">-ImageName</span></span>
<span data-ttu-id="fe24f-169">A virtuális VM-fájl neve ebben a méretarányban.</span><span class="sxs-lookup"><span data-stu-id="fe24f-169">The name of the image for VMs in this Scale Set.</span></span> <span data-ttu-id="fe24f-170">Ha nincs megadva érték, a program a "Windows Server 2016-adatközpont" képet fogja használni.</span><span class="sxs-lookup"><span data-stu-id="fe24f-170">If no value is provided, the "Windows Server 2016 DataCenter" image will be used.</span></span>

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

### <span data-ttu-id="fe24f-171">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="fe24f-171">-InstanceCount</span></span>
<span data-ttu-id="fe24f-172">A virtuális VM-képek száma a méretarányban.</span><span class="sxs-lookup"><span data-stu-id="fe24f-172">The number of VM images in the Scale Set.</span></span>  <span data-ttu-id="fe24f-173">Ha nincs megadva érték, akkor két példány jön létre.</span><span class="sxs-lookup"><span data-stu-id="fe24f-173">If no value is provided, 2 instances will be created.</span></span>

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

### <span data-ttu-id="fe24f-174">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="fe24f-174">-LoadBalancerName</span></span>
<span data-ttu-id="fe24f-175">Az ezzel a Méretaránysal használandó terheléselosztó neve.</span><span class="sxs-lookup"><span data-stu-id="fe24f-175">The name of the load balancer to use with this Scale Set.</span></span>  <span data-ttu-id="fe24f-176">Új terheléselosztó a méretarány nevének megadásával, ha a program nem ad meg értéket.</span><span class="sxs-lookup"><span data-stu-id="fe24f-176">A new load balancer using the same name as the Scale Set will be created if no value is specified.</span></span>

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

### <span data-ttu-id="fe24f-177">-Hely</span><span class="sxs-lookup"><span data-stu-id="fe24f-177">-Location</span></span>
<span data-ttu-id="fe24f-178">Az Azure-hely, ahol ez a méretarány jön létre.</span><span class="sxs-lookup"><span data-stu-id="fe24f-178">The Azure location where this Scale Set will be created.</span></span>  <span data-ttu-id="fe24f-179">Ha nincs megadva érték, a program a paraméterben hivatkozott további források helyétől kikövetkezteti a helyet.</span><span class="sxs-lookup"><span data-stu-id="fe24f-179">If no value is specified, the location will be inferred from the location of other resources referenced in the parameters.</span></span>

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

### <span data-ttu-id="fe24f-180">-NatBackendPort</span><span class="sxs-lookup"><span data-stu-id="fe24f-180">-NatBackendPort</span></span>
<span data-ttu-id="fe24f-181">A bejövő hálózati címfordításhoz tartozó backend port.</span><span class="sxs-lookup"><span data-stu-id="fe24f-181">Backend port for inbound network address translation.</span></span>

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

### <span data-ttu-id="fe24f-182">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="fe24f-182">-PublicIpAddressName</span></span>
<span data-ttu-id="fe24f-183">Annak a nyilvános IP-címnek a neve, amellyel az adott méretarányt be szeretné használni.</span><span class="sxs-lookup"><span data-stu-id="fe24f-183">The name of the public IP Address to use with this scale set.</span></span>  <span data-ttu-id="fe24f-184">Ha nincs megadva érték, akkor létrejön egy új nyilvános IP-azonosító a méretarány nevével.</span><span class="sxs-lookup"><span data-stu-id="fe24f-184">A new Public IPAddress with the same name as the Scale Set will be created if no value is provided.</span></span>

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

### <span data-ttu-id="fe24f-185">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe24f-185">-ResourceGroupName</span></span>
<span data-ttu-id="fe24f-186">A VMSS erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe24f-186">Specifies the name of the resource group of the VMSS.</span></span>  <span data-ttu-id="fe24f-187">Ha nincs megadva érték, új ResourceGroup fog létrejönni a méretarány nevével.</span><span class="sxs-lookup"><span data-stu-id="fe24f-187">If no value is specified, a new ResourceGroup will be created using the same name as the Scale Set.</span></span>

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

### <span data-ttu-id="fe24f-188">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="fe24f-188">-SecurityGroupName</span></span>
<span data-ttu-id="fe24f-189">Annak a hálózati biztonsági csoportnak a neve, amelyre alkalmazni szeretné ezt a méretarányt.</span><span class="sxs-lookup"><span data-stu-id="fe24f-189">The name of the network security group to apply to this Scale Set.</span></span>  <span data-ttu-id="fe24f-190">Ha nincs megadva érték, akkor létrejön egy alapértelmezett hálózati biztonsági csoport, amelynek a mérete megegyezik a méretarány beállítással.</span><span class="sxs-lookup"><span data-stu-id="fe24f-190">If no value is provided, a default network security group with the same name as the Scale Set will be created and applied to the Scale Set.</span></span>

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

### <span data-ttu-id="fe24f-191">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="fe24f-191">-SinglePlacementGroup</span></span>
<span data-ttu-id="fe24f-192">Ezzel a beállítással létrehozhatja a méretarányt egyetlen Elhelyezés csoportban, az alapértelmezett beállítás több csoport</span><span class="sxs-lookup"><span data-stu-id="fe24f-192">Use this to create the Scale set in a single placement group, default is multiple groups</span></span>

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

### <span data-ttu-id="fe24f-193">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="fe24f-193">-SubnetAddressPrefix</span></span>
<span data-ttu-id="fe24f-194">Annak az alhálózatnak az előtagja, amelyet a ScaleSet használni fog.</span><span class="sxs-lookup"><span data-stu-id="fe24f-194">The address prefix of the Subnet this ScaleSet will use.</span></span> <span data-ttu-id="fe24f-195">Az alapértelmezett alhálózati beállítások (192.168.1.0/24) akkor érvényesek, ha nincs megadva érték.</span><span class="sxs-lookup"><span data-stu-id="fe24f-195">Default Subnet settings (192.168.1.0/24) will be applied if no value is provided.</span></span>

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

### <span data-ttu-id="fe24f-196">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="fe24f-196">-SubnetName</span></span>
<span data-ttu-id="fe24f-197">Annak az alhálózatnak a neve, amely az adott méretarányt használja.</span><span class="sxs-lookup"><span data-stu-id="fe24f-197">The name of the subnet to use with this Scale Set.</span></span>  <span data-ttu-id="fe24f-198">Ha nincs megadva érték, akkor létrejön egy új alhálózat a méretarány-készlet nevével.</span><span class="sxs-lookup"><span data-stu-id="fe24f-198">A new Subnet will be created with the same name as the Scale Set if no value is provided.</span></span>

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

### <span data-ttu-id="fe24f-199">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="fe24f-199">-SystemAssignedIdentity</span></span>
<span data-ttu-id="fe24f-200">Ha a paraméter megtalálható, akkor a méretarányban a VM (s) a (a) rendszer automatikusan generált felügyelt rendszeridentitást rendel.</span><span class="sxs-lookup"><span data-stu-id="fe24f-200">If the parameter is present then the VM(s) in the scale set is(are) assigned a managed system identity that is auto generated.</span></span>

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

### <span data-ttu-id="fe24f-201">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="fe24f-201">-UpgradePolicyMode</span></span>
<span data-ttu-id="fe24f-202">Ebben a méretarányban a VM-példányokra vonatkozó frissítési házirend üzemmódot adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe24f-202">The upgrade policy mode for VM instances in this Scale Set.</span></span>  <span data-ttu-id="fe24f-203">A frissítési házirend az automatikus, a manuális vagy a folyamatos frissítést is megadhatja.</span><span class="sxs-lookup"><span data-stu-id="fe24f-203">Upgrade policy could specify Automatic, Manual, or Rolling upgrades.</span></span>

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

### <span data-ttu-id="fe24f-204">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="fe24f-204">-UserAssignedIdentity</span></span>
<span data-ttu-id="fe24f-205">Annak a felügyelt szolgáltatás-identitásnak a neve, amelyet ki kell osztani a VM (ek) nek a méretarányban.</span><span class="sxs-lookup"><span data-stu-id="fe24f-205">The name of a managed service identity that should be assigned to the VM(s) in the scale set.</span></span>

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

### <span data-ttu-id="fe24f-206">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="fe24f-206">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="fe24f-207">Azt a **VirtualMachineScaleSet** -objektumot adja meg, amely a parancsmag által létrehozott VMSS tulajdonságait tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="fe24f-207">Specifies the **VirtualMachineScaleSet** object that contains the properties of the VMSS that this cmdlet creates.</span></span>

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

### <span data-ttu-id="fe24f-208">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="fe24f-208">-VirtualNetworkName</span></span>
<span data-ttu-id="fe24f-209">Annak a virtuális hálózatnak a neve, amellyel az adott méretarányt használni szeretné.</span><span class="sxs-lookup"><span data-stu-id="fe24f-209">The name fo the Virtual Network to use with this scale set.</span></span>  <span data-ttu-id="fe24f-210">Ha nincs megadva érték, akkor létrejön egy új virtuális hálózat, amelynek a neve megegyezik a méretarány-Halmazsal.</span><span class="sxs-lookup"><span data-stu-id="fe24f-210">If no value is supplied, a new virtual network with the same name as the Scale Set will be created.</span></span>

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

### <span data-ttu-id="fe24f-211">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="fe24f-211">-VMScaleSetName</span></span>
<span data-ttu-id="fe24f-212">Annak a VMSS a nevét adja meg, amelyet a parancsmag hoz létre.</span><span class="sxs-lookup"><span data-stu-id="fe24f-212">Specifies the name of the VMSS that this cmdlet creates.</span></span>

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

### <span data-ttu-id="fe24f-213">-VmSize</span><span class="sxs-lookup"><span data-stu-id="fe24f-213">-VmSize</span></span>
<span data-ttu-id="fe24f-214">A megadott méretarányban a VM-példányok mérete.</span><span class="sxs-lookup"><span data-stu-id="fe24f-214">The size of the VM instances in this scale set.</span></span>  <span data-ttu-id="fe24f-215">Ha nincs megadva méret, az alapértelmezett méret (Standard_DS1_v2) lesz használatos.</span><span class="sxs-lookup"><span data-stu-id="fe24f-215">A default size (Standard_DS1_v2) will be used if no Size is specified.</span></span>

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

### <span data-ttu-id="fe24f-216">-VnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="fe24f-216">-VnetAddressPrefix</span></span>
<span data-ttu-id="fe24f-217">A megadott Méretaránysal használt virtuális hálózathoz tartozó cím előtagja.</span><span class="sxs-lookup"><span data-stu-id="fe24f-217">The address prefix for the virtual network used with this Scale Set.</span></span>  <span data-ttu-id="fe24f-218">Az alapértelmezett virtuális hálózati cím előtag-beállításai (192.168.0.0/16) akkor lesznek használatban, ha nincs megadva érték.</span><span class="sxs-lookup"><span data-stu-id="fe24f-218">Default virtual network address prefix settings (192.168.0.0/16) will be used if no value is supplied.</span></span>

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

### <span data-ttu-id="fe24f-219">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="fe24f-219">-Zone</span></span>
<span data-ttu-id="fe24f-220">Az erőforráshoz hozzárendelt IP-címet jelölő elérhetőségi zónák listája.</span><span class="sxs-lookup"><span data-stu-id="fe24f-220">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="fe24f-221">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fe24f-221">-Confirm</span></span>
<span data-ttu-id="fe24f-222">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fe24f-222">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe24f-223">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe24f-223">-WhatIf</span></span>
<span data-ttu-id="fe24f-224">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fe24f-224">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe24f-225">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fe24f-225">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe24f-226">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe24f-226">CommonParameters</span></span>
<span data-ttu-id="fe24f-227">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fe24f-227">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe24f-228">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe24f-228">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe24f-229">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fe24f-229">INPUTS</span></span>

### <span data-ttu-id="fe24f-230">System. String</span><span class="sxs-lookup"><span data-stu-id="fe24f-230">System.String</span></span>

### <span data-ttu-id="fe24f-231">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="fe24f-231">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="fe24f-232">System. Collections. Generic. list ' 1 [[System. string, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="fe24f-232">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="fe24f-233">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fe24f-233">OUTPUTS</span></span>

### <span data-ttu-id="fe24f-234">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="fe24f-234">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="fe24f-235">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fe24f-235">NOTES</span></span>

## <span data-ttu-id="fe24f-236">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fe24f-236">RELATED LINKS</span></span>

[<span data-ttu-id="fe24f-237">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fe24f-237">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="fe24f-238">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fe24f-238">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="fe24f-239">Újraindítás – AzVmss</span><span class="sxs-lookup"><span data-stu-id="fe24f-239">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="fe24f-240">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fe24f-240">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="fe24f-241">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fe24f-241">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="fe24f-242">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fe24f-242">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="fe24f-243">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fe24f-243">Update-AzVmss</span></span>](./Update-AzVmss.md)


