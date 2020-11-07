---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 1A2C843C-6962-4B0E-ACBF-A5EFF609A5BE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVmss.md
ms.openlocfilehash: fc788d40cbcd807ef05be4ab43fcda4371aaa084
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844457"
---
# <span data-ttu-id="09a72-101">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="09a72-101">New-AzVmss</span></span>

## <span data-ttu-id="09a72-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="09a72-102">SYNOPSIS</span></span>
<span data-ttu-id="09a72-103">Létrehoz egy VMSS.</span><span class="sxs-lookup"><span data-stu-id="09a72-103">Creates a VMSS.</span></span>

## <span data-ttu-id="09a72-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="09a72-104">SYNTAX</span></span>

### <span data-ttu-id="09a72-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="09a72-105">DefaultParameter (Default)</span></span>
```
New-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09a72-106">SimpleParameterSet</span><span class="sxs-lookup"><span data-stu-id="09a72-106">SimpleParameterSet</span></span>
```
New-AzVmss [[-ResourceGroupName] <String>] [-VMScaleSetName] <String> [-AsJob] [-ImageName <String>]
 -Credential <PSCredential> [-InstanceCount <Int32>] [-VirtualNetworkName <String>] [-SubnetName <String>]
 [-PublicIpAddressName <String>] [-DomainNameLabel <String>] [-SecurityGroupName <String>]
 [-LoadBalancerName <String>] [-BackendPort <Int32[]>] [-Location <String>] [-VmSize <String>]
 [-UpgradePolicyMode <UpgradeMode>] [-AllocationMethod <String>] [-VnetAddressPrefix <String>]
 [-SubnetAddressPrefix <String>] [-FrontendPoolName <String>] [-BackendPoolName <String>]
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-NatBackendPort <Int32[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09a72-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="09a72-107">DESCRIPTION</span></span>
<span data-ttu-id="09a72-108">A **New-AzVmss** parancsmag létrehoz egy virtuálisgép-készletet (VMSS) az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="09a72-108">The **New-AzVmss** cmdlet creates a Virtual Machine Scale Set (VMSS) in Azure.</span></span>
<span data-ttu-id="09a72-109">Ez a parancsmag a **VirtualMachineScaleSet** objektumot bemenetként veszi fel.</span><span class="sxs-lookup"><span data-stu-id="09a72-109">This cmdlet takes a **VirtualMachineScaleSet** object as input.</span></span>

## <span data-ttu-id="09a72-110">Példák</span><span class="sxs-lookup"><span data-stu-id="09a72-110">EXAMPLES</span></span>

### <span data-ttu-id="09a72-111">Példa 1: VMSS létrehozása</span><span class="sxs-lookup"><span data-stu-id="09a72-111">Example 1: Create a VMSS</span></span>
```
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

<span data-ttu-id="09a72-112">A következő komplex példa létrehoz egy VMSS.</span><span class="sxs-lookup"><span data-stu-id="09a72-112">The following complex example creates a VMSS.</span></span>
<span data-ttu-id="09a72-113">Az első parancs létrehoz egy erőforráscsoportot a megadott névvel és hellyel.</span><span class="sxs-lookup"><span data-stu-id="09a72-113">The first command creates a resource group with the specified name and location.</span></span>
<span data-ttu-id="09a72-114">A második parancs a **New-AzStorageAccount** parancsmagot használja a tárolási fiók létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="09a72-114">The second command uses the **New-AzStorageAccount** cmdlet to create a storage account.</span></span>
<span data-ttu-id="09a72-115">A harmadik parancs ezt követően a **Get-AzStorageAccount** parancsmagot használja a második parancsban létrehozott tárterület-fiók beszerzéséhez, és az eredményt a $STOAccount változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="09a72-115">The third command then uses the **Get-AzStorageAccount** cmdlet to get the storage account created in the second command and stores the result in the $STOAccount variable.</span></span>
<span data-ttu-id="09a72-116">Az ötödik parancs a **New-AzVirtualNetworkSubnetConfig** parancsmagot használja alhálózat létrehozásához, és az eredményt az $SubNet nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="09a72-116">The fifth command uses the **New-AzVirtualNetworkSubnetConfig** cmdlet to create a subnet and stores the result in the variable named $SubNet.</span></span>
<span data-ttu-id="09a72-117">A hatodik parancs a **New-AzVirtualNetwork** parancsmagot használja virtuális hálózat létrehozásához, és az eredményt az $VNet nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="09a72-117">The sixth command uses the **New-AzVirtualNetwork** cmdlet to create a virtual network and stores the result in the variable named $VNet.</span></span>
<span data-ttu-id="09a72-118">A hetedik parancs a **Get-AzVirtualNetwork** használatával információkat kaphat a hatodik parancsban létrehozott virtuális hálózatról, és az adatokat a $VNet nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="09a72-118">The seventh command uses the **Get-AzVirtualNetwork** to get information about the virtual network created in the sixth command and stores the information in the variable named $VNet.</span></span>
<span data-ttu-id="09a72-119">A nyolcadik és a kilencedik parancs a **New-AzPublicIpAddress** és a **Get-AzureRmPublicIpAddress** használatával hozza létre és kapja meg az adott nyilvános IP-címről származó információkat.</span><span class="sxs-lookup"><span data-stu-id="09a72-119">The eighth and ninth command uses the **New-AzPublicIpAddress** and **Get- AzureRmPublicIpAddress** to create and get information from that public IP address.</span></span>
<span data-ttu-id="09a72-120">A parancsok a $PubIP nevű változóban tárolják az adatokat.</span><span class="sxs-lookup"><span data-stu-id="09a72-120">The commands store the information in the variable named $PubIP.</span></span>
<span data-ttu-id="09a72-121">A tizedik parancs a **New-AzureRmLoadBalancerFrontendIpConfig** parancsmagot használja egy frontend terheléselosztás létrehozásához, és az eredményt az $frontend nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="09a72-121">The tenth command uses the **New- AzureRmLoadBalancerFrontendIpConfig** cmdlet to create a frontend load balancer and stores the result in the variable named $Frontend.</span></span>
<span data-ttu-id="09a72-122">A tizenegyedik parancs a **New-AzLoadBalancerBackendAddressPoolConfig** segítségével hozza létre a backend-címkészlet konfigurációját, és az eredményt az $BackendAddressPool nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="09a72-122">The eleventh command uses the **New-AzLoadBalancerBackendAddressPoolConfig** to create a backend address pool configuration and stores the result in the variable named $BackendAddressPool.</span></span>
<span data-ttu-id="09a72-123">A tizenkettedik parancs a **New-AzLoadBalancerProbeConfig** használatával létrehoz egy szondát, és a szonda adatait a $Probe nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="09a72-123">The twelfth command uses the **New-AzLoadBalancerProbeConfig** to create a probe and stores the probe information in the variable named $Probe.</span></span>
<span data-ttu-id="09a72-124">A tizenharmadik parancs a **New-AzLoadBalancerInboundNatPoolConfig** parancsmagot használja a terheléselosztó bejövő hálózati címfordítási (NAT) alkalmazáskészlet-konfiguráció létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="09a72-124">The thirteenth command uses the **New-AzLoadBalancerInboundNatPoolConfig** cmdlet to create a load balancer inbound network address translation (NAT) pool configuration.</span></span>
<span data-ttu-id="09a72-125">A tizennegyedik parancs a **New-AzLoadBalancerRuleConfig** segítségével hoz létre terheléselosztó szabály-konfigurációt, és az eredményt az $LBRule nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="09a72-125">The fourteenth command uses the **New-AzLoadBalancerRuleConfig** to create a load balancer rule configuration and stores the result in the variable named $LBRule.</span></span>
<span data-ttu-id="09a72-126">A tizenötödik parancs a **New-AzLoadBalancer** parancsmagot használja a terheléselosztó létrehozásához, és az eredményt az $ActualLb nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="09a72-126">The fifteenth command uses the **New-AzLoadBalancer** cmdlet to create a load balancer and stores the result in the variable named $ActualLb.</span></span>
<span data-ttu-id="09a72-127">A tizenhatodik parancs a **Get-AzLoadBalancer** használatával információkat kaphat a tizenötödik parancsban létrehozott terheléselosztó rendszerről, és az adatokat a $ExpectedLb nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="09a72-127">The sixteenth command uses the **Get-AzLoadBalancer** to get information about the load balancer that was created in the fifteenth command and stores the information in the variable named $ExpectedLb.</span></span>
<span data-ttu-id="09a72-128">A tizenhetedik parancs a **New-AzVmssIPConfig** parancsmagot használja a VMSS IP-konfigurációjának létrehozásához, és az adatokat a $IPCfg nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="09a72-128">The seventeenth command uses the **New-AzVmssIPConfig** cmdlet to create a VMSS IP configuration and stores the information in the variable named $IPCfg.</span></span>
<span data-ttu-id="09a72-129">A XVIII parancs a **New-AzVmssConfig** parancsmagot használja VMSS konfigurációs objektum létrehozásához, és az eredményt az $VMSS nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="09a72-129">The eighteenth command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="09a72-130">A tizenkilencedik parancs a **New-AzVmss** parancsmagot használja a VMSS létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="09a72-130">The nineteenth command uses the **New-AzVmss** cmdlet to create the VMSS.</span></span>

## <span data-ttu-id="09a72-131">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="09a72-131">PARAMETERS</span></span>

### <span data-ttu-id="09a72-132">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="09a72-132">-AllocationMethod</span></span>
<span data-ttu-id="09a72-133">A méretarány (statikus vagy dinamikus) nyilvános IP-címének kiosztási módja.</span><span class="sxs-lookup"><span data-stu-id="09a72-133">Allocation method for the Public IP Address of the Scale Set (Static or Dynamic).</span></span>  <span data-ttu-id="09a72-134">Ha nincs megadva érték, akkor a felosztás statikus lesz.</span><span class="sxs-lookup"><span data-stu-id="09a72-134">If no value is supplied, allocation will be static.</span></span>

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

### <span data-ttu-id="09a72-135">-AsJob</span><span class="sxs-lookup"><span data-stu-id="09a72-135">-AsJob</span></span>
<span data-ttu-id="09a72-136">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="09a72-136">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="09a72-137">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="09a72-137">-BackendPoolName</span></span>
<span data-ttu-id="09a72-138">Annak a backend-címkészlet a neve, amelyet az ehhez a léptékhez tartozó terheléselosztásban szeretne használni.</span><span class="sxs-lookup"><span data-stu-id="09a72-138">The name of the backend address pool to use in the load balancer for this Scale Set.</span></span>  <span data-ttu-id="09a72-139">Ha nincs megadva érték, akkor létrejön egy új backend-készlet, amelynek a neve megegyezik a méretarány beállítással.</span><span class="sxs-lookup"><span data-stu-id="09a72-139">If no value is provided, a new backend pool will be created, with the same name as the Scale Set.</span></span>

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

### <span data-ttu-id="09a72-140">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="09a72-140">-BackendPort</span></span>
<span data-ttu-id="09a72-141">A kiegyenlítő terheléselosztás által a VM-tel való kommunikációhoz a méretarány beállítása által használt backend-portok száma.</span><span class="sxs-lookup"><span data-stu-id="09a72-141">Backend port numbers used by the Scale Set load balancer to communicate with VMs in the Scale Set.</span></span>  <span data-ttu-id="09a72-142">Ha nincs megadva érték, akkor a rendszer a 3389 és az 5985-es portot fogja használni a Windows VMS rendszerhez, és a 22-ös portot fogja használni a Linux VM-hez.</span><span class="sxs-lookup"><span data-stu-id="09a72-142">If no values are specified, ports 3389 and 5985 will be used for Windows VMS, and port 22 will be used for Linux VMs.</span></span>

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

### <span data-ttu-id="09a72-143">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="09a72-143">-Credential</span></span>
<span data-ttu-id="09a72-144">A virtuális VMs-rendszerhez tartozó rendszergazdai hitelesítő adatok (Felhasználónév és jelszó) ebben a méretarányban jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="09a72-144">The administrator credentials (username and password) for VMs in this Scale Set.</span></span>

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

### <span data-ttu-id="09a72-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09a72-145">-DefaultProfile</span></span>
<span data-ttu-id="09a72-146">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="09a72-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09a72-147">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="09a72-147">-DomainNameLabel</span></span>
<span data-ttu-id="09a72-148">A nyilvános Fully-Qualified tartománynév címkéje (FQDN) ehhez a méretarányhoz.</span><span class="sxs-lookup"><span data-stu-id="09a72-148">The domain name label for the public Fully-Qualified domain name (FQDN) for this Scale Set.</span></span> <span data-ttu-id="09a72-149">Ez a tartománynév első olyan összetevője, amely automatikusan assiged a méretarány-készletre.</span><span class="sxs-lookup"><span data-stu-id="09a72-149">This is the first component of the domain name that is automatically assiged to the Scale Set.</span></span> <span data-ttu-id="09a72-150">Automatikusan hozzárendelt tartománynevek: használja az űrlapot ( <DomainNameLabel> . <Location> . cloudapp.azure.com).</span><span class="sxs-lookup"><span data-stu-id="09a72-150">Automatically assigned Domain names use the form (<DomainNameLabel>.<Location>.cloudapp.azure.com).</span></span> <span data-ttu-id="09a72-151">Ha nincs megadva érték, az alapértelmezett tartománynév-címke lesz az ÖSSZEFŰZ <ScaleSetName> és a <ResourceGroupName> .</span><span class="sxs-lookup"><span data-stu-id="09a72-151">If no value is supplied, the default domain name label will be the concatenation of <ScaleSetName> and <ResourceGroupName>.</span></span>

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

### <span data-ttu-id="09a72-152">-FrontendPoolName</span><span class="sxs-lookup"><span data-stu-id="09a72-152">-FrontendPoolName</span></span>
<span data-ttu-id="09a72-153">Annak a usein a neve, amely a Locate kiegyenlítő méretarányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="09a72-153">The name of the frontend address pool to usein the Scale Set locad balancer.</span></span>  <span data-ttu-id="09a72-154">Ha nincs megadva érték, akkor létrejön egy új felületi címkészlet, amelynek a neve megegyezik a méretarány beállítással.</span><span class="sxs-lookup"><span data-stu-id="09a72-154">If no value is supplied, a new Frontend Address Pool will be created, with the same name as the scale set.</span></span>

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

### <span data-ttu-id="09a72-155">-ImageName</span><span class="sxs-lookup"><span data-stu-id="09a72-155">-ImageName</span></span>
<span data-ttu-id="09a72-156">A virtuális VM-fájl neve ebben a méretarányban.</span><span class="sxs-lookup"><span data-stu-id="09a72-156">The name of the image for VMs in this Scale Set.</span></span> <span data-ttu-id="09a72-157">Ha nincs megadva érték, a program a "Windows Server 2016-adatközpont" képet fogja használni.</span><span class="sxs-lookup"><span data-stu-id="09a72-157">If no value is provided, the "Windows Server 2016 DataCenter" image will be used.</span></span>

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

### <span data-ttu-id="09a72-158">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="09a72-158">-InstanceCount</span></span>
<span data-ttu-id="09a72-159">A virtuális VM-képek száma a méretarányban.</span><span class="sxs-lookup"><span data-stu-id="09a72-159">The number of VM images in the Scale Set.</span></span>  <span data-ttu-id="09a72-160">Ha nincs megadva érték, akkor két példány jön létre.</span><span class="sxs-lookup"><span data-stu-id="09a72-160">If no value is provided, 2 instances will be created.</span></span>

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

### <span data-ttu-id="09a72-161">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="09a72-161">-LoadBalancerName</span></span>
<span data-ttu-id="09a72-162">Az ezzel a Méretaránysal használandó terheléselosztó neve.</span><span class="sxs-lookup"><span data-stu-id="09a72-162">The name of the load balancer to use with this Scale Set.</span></span>  <span data-ttu-id="09a72-163">Új terheléselosztó a méretarány nevének megadásával, ha a program nem ad meg értéket.</span><span class="sxs-lookup"><span data-stu-id="09a72-163">A new load balancer using the same name as the Scale Set will be created if no value is specified.</span></span>

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

### <span data-ttu-id="09a72-164">-Hely</span><span class="sxs-lookup"><span data-stu-id="09a72-164">-Location</span></span>
<span data-ttu-id="09a72-165">Az Azure-hely, ahol ez a méretarány jön létre.</span><span class="sxs-lookup"><span data-stu-id="09a72-165">The Azure location where this Scale Set will be created.</span></span>  <span data-ttu-id="09a72-166">Ha nincs megadva érték, a program a paraméterben hivatkozott további források helyétől kikövetkezteti a helyet.</span><span class="sxs-lookup"><span data-stu-id="09a72-166">If no value is specified, the location will be inferred from the location of other resources referenced in the parameters.</span></span>

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

### <span data-ttu-id="09a72-167">-NatBackendPort</span><span class="sxs-lookup"><span data-stu-id="09a72-167">-NatBackendPort</span></span>
<span data-ttu-id="09a72-168">A bejövő hálózati címfordításhoz tartozó backend port.</span><span class="sxs-lookup"><span data-stu-id="09a72-168">Backend port for inbound network address translation.</span></span>

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

### <span data-ttu-id="09a72-169">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="09a72-169">-PublicIpAddressName</span></span>
<span data-ttu-id="09a72-170">Annak a nyilvános IP-címnek a neve, amellyel az adott méretarányt be szeretné használni.</span><span class="sxs-lookup"><span data-stu-id="09a72-170">The name of the public IP Address to use with this scale set.</span></span>  <span data-ttu-id="09a72-171">Ha nincs megadva érték, akkor létrejön egy új nyilvános IP-azonosító a méretarány nevével.</span><span class="sxs-lookup"><span data-stu-id="09a72-171">A new Public IPAddress with the same name as the Scale Set will be created if no value is provided.</span></span>

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

### <span data-ttu-id="09a72-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09a72-172">-ResourceGroupName</span></span>
<span data-ttu-id="09a72-173">A VMSS erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="09a72-173">Specifies the name of the resource group of the VMSS.</span></span>  <span data-ttu-id="09a72-174">Ha nincs megadva érték, új ResourceGroup fog létrejönni a méretarány nevével.</span><span class="sxs-lookup"><span data-stu-id="09a72-174">If no value is specified, a new ResourceGroup will be created using the same name as the Scale Set.</span></span>

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

### <span data-ttu-id="09a72-175">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="09a72-175">-SecurityGroupName</span></span>
<span data-ttu-id="09a72-176">Annak a hálózati biztonsági csoportnak a neve, amelyre alkalmazni szeretné ezt a méretarányt.</span><span class="sxs-lookup"><span data-stu-id="09a72-176">The name of the network security group to apply to this Scale Set.</span></span>  <span data-ttu-id="09a72-177">Ha nincs megadva érték, akkor létrejön egy alapértelmezett hálózati biztonsági csoport, amelynek a mérete megegyezik a méretarány beállítással.</span><span class="sxs-lookup"><span data-stu-id="09a72-177">If no value is provided, a default network security group with the same name as the Scale Set will be created and applied to the Scale Set.</span></span>

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

### <span data-ttu-id="09a72-178">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="09a72-178">-SubnetAddressPrefix</span></span>
<span data-ttu-id="09a72-179">Annak az alhálózatnak az előtagja, amelyet a ScaleSet használni fog.</span><span class="sxs-lookup"><span data-stu-id="09a72-179">The address prefix of the Subnet this ScaleSet will use.</span></span> <span data-ttu-id="09a72-180">Az alapértelmezett alhálózati beállítások (192.168.1.0/24) akkor érvényesek, ha nincs megadva érték.</span><span class="sxs-lookup"><span data-stu-id="09a72-180">Default Subnet settings (192.168.1.0/24) will be applied if no value is provided.</span></span>

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

### <span data-ttu-id="09a72-181">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="09a72-181">-SubnetName</span></span>
<span data-ttu-id="09a72-182">Annak az alhálózatnak a neve, amely az adott méretarányt használja.</span><span class="sxs-lookup"><span data-stu-id="09a72-182">The name of the subnet to use with this Scale Set.</span></span>  <span data-ttu-id="09a72-183">Ha nincs megadva érték, akkor létrejön egy új alhálózat a méretarány-készlet nevével.</span><span class="sxs-lookup"><span data-stu-id="09a72-183">A new Subnet will be created with the same name as the Scale Set if no value is provided.</span></span>

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

### <span data-ttu-id="09a72-184">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="09a72-184">-UpgradePolicyMode</span></span>
<span data-ttu-id="09a72-185">Ebben a méretarányban a VM-példányokra vonatkozó frissítési házirend üzemmódot adja meg.</span><span class="sxs-lookup"><span data-stu-id="09a72-185">The upgrade policy mode for VM instances in this Scale Set.</span></span>  <span data-ttu-id="09a72-186">A frissítési házirend az automatikus, a manuális vagy a folyamatos frissítést is megadhatja.</span><span class="sxs-lookup"><span data-stu-id="09a72-186">Upgrade policy could specify Automatic, Manual, or Rolling upgrades.</span></span>

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

### <span data-ttu-id="09a72-187">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="09a72-187">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="09a72-188">Azt a **VirtualMachineScaleSet** -objektumot adja meg, amely a parancsmag által létrehozott VMSS tulajdonságait tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="09a72-188">Specifies the **VirtualMachineScaleSet** object that contains the properties of the VMSS that this cmdlet creates.</span></span>

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

### <span data-ttu-id="09a72-189">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="09a72-189">-VirtualNetworkName</span></span>
<span data-ttu-id="09a72-190">Annak a virtuális hálózatnak a neve, amellyel az adott méretarányt használni szeretné.</span><span class="sxs-lookup"><span data-stu-id="09a72-190">The name fo the Virtual Network to use with this scale set.</span></span>  <span data-ttu-id="09a72-191">Ha nincs megadva érték, akkor létrejön egy új virtuális hálózat, amelynek a neve megegyezik a méretarány-Halmazsal.</span><span class="sxs-lookup"><span data-stu-id="09a72-191">If no value is supplied, a new virtual network with the same name as the Scale Set will be created.</span></span>

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

### <span data-ttu-id="09a72-192">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="09a72-192">-VMScaleSetName</span></span>
<span data-ttu-id="09a72-193">Annak a VMSS a nevét adja meg, amelyet a parancsmag hoz létre.</span><span class="sxs-lookup"><span data-stu-id="09a72-193">Specifies the name of the VMSS that this cmdlet creates.</span></span>

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

### <span data-ttu-id="09a72-194">-VmSize</span><span class="sxs-lookup"><span data-stu-id="09a72-194">-VmSize</span></span>
<span data-ttu-id="09a72-195">A megadott méretarányban a VM-példányok mérete.</span><span class="sxs-lookup"><span data-stu-id="09a72-195">The size of the VM instances in this scale set.</span></span>  <span data-ttu-id="09a72-196">Ha nincs megadva méret, az alapértelmezett méret (Standard_DS1_v2) lesz használatos.</span><span class="sxs-lookup"><span data-stu-id="09a72-196">A default size (Standard_DS1_v2) will be used if no Size is specified.</span></span>

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

### <span data-ttu-id="09a72-197">-VnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="09a72-197">-VnetAddressPrefix</span></span>
<span data-ttu-id="09a72-198">A megadott Méretaránysal használt virtuális hálózathoz tartozó cím előtagja.</span><span class="sxs-lookup"><span data-stu-id="09a72-198">The address prefix for the virtual network used with this Scale Set.</span></span>  <span data-ttu-id="09a72-199">Az alapértelmezett virtuális hálózati cím előtag-beállításai (192.168.0.0/16) akkor lesznek használatban, ha nincs megadva érték.</span><span class="sxs-lookup"><span data-stu-id="09a72-199">Default virtual network address prefix settings (192.168.0.0/16) will be used if no value is supplied.</span></span>

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

### <span data-ttu-id="09a72-200">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="09a72-200">-Zone</span></span>
<span data-ttu-id="09a72-201">Az erőforráshoz hozzárendelt IP-címet jelölő elérhetőségi zónák listája.</span><span class="sxs-lookup"><span data-stu-id="09a72-201">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="09a72-202">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="09a72-202">-Confirm</span></span>
<span data-ttu-id="09a72-203">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="09a72-203">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09a72-204">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09a72-204">-WhatIf</span></span>
<span data-ttu-id="09a72-205">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="09a72-205">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="09a72-206">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="09a72-206">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09a72-207">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09a72-207">CommonParameters</span></span>
<span data-ttu-id="09a72-208">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="09a72-208">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09a72-209">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09a72-209">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09a72-210">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="09a72-210">INPUTS</span></span>

### <span data-ttu-id="09a72-211">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="09a72-211">VirtualMachineScaleSet</span></span>
<span data-ttu-id="09a72-212">A ' VirtualMachineScaleSet ' paraméter az "VirtualMachineScaleSet" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="09a72-212">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="09a72-213">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="09a72-213">OUTPUTS</span></span>

### <span data-ttu-id="09a72-214">Ez a parancsmag semmilyen kimenetet nem hoz létre.</span><span class="sxs-lookup"><span data-stu-id="09a72-214">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="09a72-215">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="09a72-215">NOTES</span></span>

## <span data-ttu-id="09a72-216">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="09a72-216">RELATED LINKS</span></span>

[<span data-ttu-id="09a72-217">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="09a72-217">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="09a72-218">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="09a72-218">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="09a72-219">Újraindítás – AzVmss</span><span class="sxs-lookup"><span data-stu-id="09a72-219">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="09a72-220">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="09a72-220">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="09a72-221">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="09a72-221">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="09a72-222">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="09a72-222">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="09a72-223">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="09a72-223">Update-AzVmss</span></span>](./Update-AzVmss.md)


