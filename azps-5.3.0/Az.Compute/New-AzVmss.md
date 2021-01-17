---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1A2C843C-6962-4B0E-ACBF-A5EFF609A5BE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmss.md
ms.openlocfilehash: 4953e914cc52784cd815be80307babfe05f3b63c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480810"
---
# <span data-ttu-id="4bf54-101">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4bf54-101">New-AzVmss</span></span>

## <span data-ttu-id="4bf54-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4bf54-102">SYNOPSIS</span></span>
<span data-ttu-id="4bf54-103">VMSS-t hoz létre.</span><span class="sxs-lookup"><span data-stu-id="4bf54-103">Creates a VMSS.</span></span>

## <span data-ttu-id="4bf54-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4bf54-104">SYNTAX</span></span>

### <span data-ttu-id="4bf54-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4bf54-105">DefaultParameter (Default)</span></span>
```
New-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4bf54-106">SimpleParameterSet</span><span class="sxs-lookup"><span data-stu-id="4bf54-106">SimpleParameterSet</span></span>
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

## <span data-ttu-id="4bf54-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4bf54-107">DESCRIPTION</span></span>
<span data-ttu-id="4bf54-108">A **New-AzVmss** parancsmag virtuálisgép-méretarány-készletet (VMSS) hoz létre az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="4bf54-108">The **New-AzVmss** cmdlet creates a Virtual Machine Scale Set (VMSS) in Azure.</span></span>
<span data-ttu-id="4bf54-109">Az egyszerű paraméterkészlet () segítségével gyorsan létrehozhat előre beállított `SimpleParameterSet` VMSS-eket és kapcsolódó erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="4bf54-109">Use the simple parameter set (`SimpleParameterSet`) to quickly create a pre-set VMSS and associated resources.</span></span> <span data-ttu-id="4bf54-110">Az alapértelmezett paraméterkészletet ( ) akkor használja, ha speciálisabb esetekre van szüksége, amikor a VMSS és az egyes társított erőforrások mindegyik összetevőjét pontosan be kell állítania a létrehozás `DefaultParameter` előtt.</span><span class="sxs-lookup"><span data-stu-id="4bf54-110">Use the default parameter set (`DefaultParameter`) for more advanced scenarios when you need to precisely configure each component of the VMSS and each associated resource before creation.</span></span>

## <span data-ttu-id="4bf54-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4bf54-111">EXAMPLES</span></span>

### <span data-ttu-id="4bf54-112">1. példa: VMSS létrehozása a **`SimpleParameterSet`**</span><span class="sxs-lookup"><span data-stu-id="4bf54-112">Example 1: Create a VMSS using the **`SimpleParameterSet`**</span></span>
```powershell
$vmssName = <VMSSNAME>
# Create credentials, I am using one way to create credentials, there are others as well. 
# Pick one that makes the most sense according to your use case.
$vmPassword = ConvertTo-SecureString <PASSWORD_HERE> -AsPlainText -Force
$vmCred = New-Object System.Management.Automation.PSCredential(<USERNAME_HERE>, $vmPassword)

#Create a VMSS using the default settings
New-AzVmss -Credential $vmCred -VMScaleSetName $vmssName
```

<span data-ttu-id="4bf54-113">A fenti parancs a következőt hozza létre a következő `$vmssName` névvel:</span><span class="sxs-lookup"><span data-stu-id="4bf54-113">The command above creates the following with the name `$vmssName` :</span></span>
* <span data-ttu-id="4bf54-114">Erőforráscsoport</span><span class="sxs-lookup"><span data-stu-id="4bf54-114">A Resource Group</span></span>
* <span data-ttu-id="4bf54-115">Virtuális hálózat</span><span class="sxs-lookup"><span data-stu-id="4bf54-115">A virtual network</span></span>
* <span data-ttu-id="4bf54-116">Terheléselosztás</span><span class="sxs-lookup"><span data-stu-id="4bf54-116">A load balancer</span></span>
* <span data-ttu-id="4bf54-117">Nyilvános IP-cím</span><span class="sxs-lookup"><span data-stu-id="4bf54-117">A public IP</span></span>
* <span data-ttu-id="4bf54-118">A VMSS 2 példánysal</span><span class="sxs-lookup"><span data-stu-id="4bf54-118">the VMSS with 2 instances</span></span>

<span data-ttu-id="4bf54-119">A VMSS-ban a vmss-hez kiválasztott alapértelmezett kép `2016-Datacenter Windows Server` az, a termékváltozat pedig a `Standard_DS1_v2`</span><span class="sxs-lookup"><span data-stu-id="4bf54-119">The default image chosen for the VMs in the VMSS is `2016-Datacenter Windows Server` and the SKU is `Standard_DS1_v2`</span></span>

### <span data-ttu-id="4bf54-120">2. példa: VMSS létrehozása a **`DefaultParameterSet`**</span><span class="sxs-lookup"><span data-stu-id="4bf54-120">Example 2: Create a VMSS using the **`DefaultParameterSet`**</span></span>
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

<span data-ttu-id="4bf54-121">A fenti összetett példa VMSS-et hoz létre, és az alábbiakban látható, hogy mi történik:</span><span class="sxs-lookup"><span data-stu-id="4bf54-121">The complex example above creates a VMSS, following is an explanation of what is happening:</span></span>
* <span data-ttu-id="4bf54-122">Az első parancs létrehoz egy erőforráscsoportot a megadott névvel és helyről.</span><span class="sxs-lookup"><span data-stu-id="4bf54-122">The first command creates a resource group with the specified name and location.</span></span>
* <span data-ttu-id="4bf54-123">A második parancs a **New-AzStorageAccount** parancsmaggal hoz létre tárfiókot.</span><span class="sxs-lookup"><span data-stu-id="4bf54-123">The second command uses the **New-AzStorageAccount** cmdlet to create a storage account.</span></span>
* <span data-ttu-id="4bf54-124">A harmadik parancs ezután a **Get-AzStorageAccount** parancsmag használatával begyűjte a második parancsban létrehozott tárfiókot, és az eredményt a $STOAccount változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="4bf54-124">The third command then uses the **Get-AzStorageAccount** cmdlet to get the storage account created in the second command and stores the result in the $STOAccount variable.</span></span>
* <span data-ttu-id="4bf54-125">Az ötödik parancs a **New-AzVirtualNetworkSubnetConfig** parancsmaggal hoz létre egy alhálózatot, és az eredményt az $SubNet nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="4bf54-125">The fifth command uses the **New-AzVirtualNetworkSubnetConfig** cmdlet to create a subnet and stores the result in the variable named $SubNet.</span></span>
* <span data-ttu-id="4bf54-126">A hatodik parancs a **New-AzVirtualNetwork** parancsmag használatával hoz létre egy virtuális hálózatot, és az eredményt a $VNet.</span><span class="sxs-lookup"><span data-stu-id="4bf54-126">The sixth command uses the **New-AzVirtualNetwork** cmdlet to create a virtual network and stores the result in the variable named $VNet.</span></span>
* <span data-ttu-id="4bf54-127">A hetedik parancs a **Get-AzVirtualNetwork** segítségével információkat kap a hatodik parancsban létrehozott virtuális hálózatról, és az adatokat az $VNet változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="4bf54-127">The seventh command uses the **Get-AzVirtualNetwork** to get information about the virtual network created in the sixth command and stores the information in the variable named $VNet.</span></span>
* <span data-ttu-id="4bf54-128">A nyolcadik és a hetedik parancs a **New-AzPublicIpAddress** és **a Get- AzureRmPublicIpAddress** paranccsal hozza létre és szerezze be az információkat az adott nyilvános IP-címről.</span><span class="sxs-lookup"><span data-stu-id="4bf54-128">The eighth and ninth command uses the **New-AzPublicIpAddress** and **Get- AzureRmPublicIpAddress** to create and get information from that public IP address.</span></span>
* <span data-ttu-id="4bf54-129">A parancsok az adatokat a $PubIP.</span><span class="sxs-lookup"><span data-stu-id="4bf54-129">The commands store the information in the variable named $PubIP.</span></span>
* <span data-ttu-id="4bf54-130">A tizedik parancs a **New- AzureRmLoadBalancerFrontendIpConfig** parancsmagot használja egy frontend terheléseloszlító létrehozásához, és az eredményt a $Frontend.</span><span class="sxs-lookup"><span data-stu-id="4bf54-130">The tenth command uses the **New- AzureRmLoadBalancerFrontendIpConfig** cmdlet to create a frontend load balancer and stores the result in the variable named $Frontend.</span></span>
* <span data-ttu-id="4bf54-131">A tizenegyedik parancs a **New-AzLoadBalancerBackendAddressPoolConfig** segítségével hoz létre egy háttércímkészlet-konfigurációt, és az eredményt a $BackendAddressPool.</span><span class="sxs-lookup"><span data-stu-id="4bf54-131">The eleventh command uses the **New-AzLoadBalancerBackendAddressPoolConfig** to create a backend address pool configuration and stores the result in the variable named $BackendAddressPool.</span></span>
* <span data-ttu-id="4bf54-132">A tizenkettedik parancs a **New-AzLoadBalancerProbeConfig** segítségével létrehoz egy tárolót, és tárolja a mentesítési adatokat a $Probe.</span><span class="sxs-lookup"><span data-stu-id="4bf54-132">The twelfth command uses the **New-AzLoadBalancerProbeConfig** to create a probe and stores the probe information in the variable named $Probe.</span></span>
* <span data-ttu-id="4bf54-133">A tizenharmadik parancs a **New-AzLoadBalancerInboundNatPoolConfig** parancsmaggal hoz létre terheléselegyenlő bejövő hálózati címfordítási (NAT) készlet-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="4bf54-133">The thirteenth command uses the **New-AzLoadBalancerInboundNatPoolConfig** cmdlet to create a load balancer inbound network address translation (NAT) pool configuration.</span></span>
* <span data-ttu-id="4bf54-134">A tizennégyedik parancs a **New-AzLoadBalancerRuleConfig** segítségével hoz létre terheléselegyenlő szabálykonfigurációt, és az eredményt a következő nevű változóban $LBRule.</span><span class="sxs-lookup"><span data-stu-id="4bf54-134">The fourteenth command uses the **New-AzLoadBalancerRuleConfig** to create a load balancer rule configuration and stores the result in the variable named $LBRule.</span></span>
* <span data-ttu-id="4bf54-135">A tizenötödik parancs a **New-AzLoadBalancer** parancsmagot használja a terheléselosztás létrehozására, és az eredményt a következő nevű változóban $ActualLb.</span><span class="sxs-lookup"><span data-stu-id="4bf54-135">The fifteenth command uses the **New-AzLoadBalancer** cmdlet to create a load balancer and stores the result in the variable named $ActualLb.</span></span>
* <span data-ttu-id="4bf54-136">A 15. parancs a **Get-AzLoadBalancer** segítségével információkat kap a tizenötedik parancsban létrehozott terheléselosztásról, és az adatokat az $ExpectedLb változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="4bf54-136">The sixteenth command uses the **Get-AzLoadBalancer** to get information about the load balancer that was created in the fifteenth command and stores the information in the variable named $ExpectedLb.</span></span>
* <span data-ttu-id="4bf54-137">A tizenhét parancs a **New-AzVmssIPConfig** parancsmagot használja a VMSS IP-konfiguráció létrehozásához, és az adatokat a következő nevű változóban $IPCfg.</span><span class="sxs-lookup"><span data-stu-id="4bf54-137">The seventeenth command uses the **New-AzVmssIPConfig** cmdlet to create a VMSS IP configuration and stores the information in the variable named $IPCfg.</span></span>
* <span data-ttu-id="4bf54-138">A tizennyolc parancs a **New-AzVmssConfig** parancsmagot használja a VMSS konfigurációs objektum létrehozásához, és az eredményt a következő nevű változóban $VMSS.</span><span class="sxs-lookup"><span data-stu-id="4bf54-138">The eighteenth command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
* <span data-ttu-id="4bf54-139">A tizenkilencedik parancs a **New-AzVmss** parancsmagot használja a VMSS létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="4bf54-139">The nineteenth command uses the **New-AzVmss** cmdlet to create the VMSS.</span></span>

## <span data-ttu-id="4bf54-140">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4bf54-140">PARAMETERS</span></span>

### <span data-ttu-id="4bf54-141">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="4bf54-141">-AllocationMethod</span></span>
<span data-ttu-id="4bf54-142">A méretaránykészlet nyilvános IP-címének terhelési módja (statikus vagy dinamikus).</span><span class="sxs-lookup"><span data-stu-id="4bf54-142">Allocation method for the Public IP Address of the Scale Set (Static or Dynamic).</span></span>  <span data-ttu-id="4bf54-143">Ha nem ad meg értéket, a terhelés statikus lesz.</span><span class="sxs-lookup"><span data-stu-id="4bf54-143">If no value is supplied, allocation will be static.</span></span>

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

### <span data-ttu-id="4bf54-144">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4bf54-144">-AsJob</span></span>
<span data-ttu-id="4bf54-145">Futtasa a parancsmagot a háttérben, és adja vissza a feladatot az előrehaladás nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="4bf54-145">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="4bf54-146">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="4bf54-146">-BackendPoolName</span></span>
<span data-ttu-id="4bf54-147">Az ebben a méretkészletben a terheléselosztásban használt háttércímkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="4bf54-147">The name of the backend address pool to use in the load balancer for this Scale Set.</span></span>  <span data-ttu-id="4bf54-148">Ha nem ad meg értéket, a rendszer létrehoz egy új háttérkészletet, amely neve megegyezik a méretaránykészlet nevével.</span><span class="sxs-lookup"><span data-stu-id="4bf54-148">If no value is provided, a new backend pool will be created, with the same name as the Scale Set.</span></span>

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

### <span data-ttu-id="4bf54-149">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="4bf54-149">-BackendPort</span></span>
<span data-ttu-id="4bf54-150">A scale set load balancer által a méretarányos készletben a virtuális gépekkel való kommunikációra használt háttérportszámok.</span><span class="sxs-lookup"><span data-stu-id="4bf54-150">Backend port numbers used by the Scale Set load balancer to communicate with VMs in the Scale Set.</span></span>  <span data-ttu-id="4bf54-151">Ha nincs megadva érték, a Windows VMS-hez a 3389-es és az 5985-ös portot, Linuxos VMS-hez pedig a 22-es portot fogja használni.</span><span class="sxs-lookup"><span data-stu-id="4bf54-151">If no values are specified, ports 3389 and 5985 will be used for Windows VMS, and port 22 will be used for Linux VMs.</span></span>

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

### <span data-ttu-id="4bf54-152">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="4bf54-152">-Credential</span></span>
<span data-ttu-id="4bf54-153">A rendszergazdai hitelesítő adatok (felhasználónév és jelszó) a virtuális gépekhez ebben a méretkészletben.</span><span class="sxs-lookup"><span data-stu-id="4bf54-153">The administrator credentials (username and password) for VMs in this Scale Set.</span></span>

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

### <span data-ttu-id="4bf54-154">-DataDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="4bf54-154">-DataDiskSizeInGb</span></span>
<span data-ttu-id="4bf54-155">Az adatlemezek mérete GB-ban.</span><span class="sxs-lookup"><span data-stu-id="4bf54-155">Specifies the sizes of data disks in GB.</span></span>

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

### <span data-ttu-id="4bf54-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bf54-156">-DefaultProfile</span></span>
<span data-ttu-id="4bf54-157">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4bf54-157">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4bf54-158">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="4bf54-158">-DomainNameLabel</span></span>
<span data-ttu-id="4bf54-159">A nyilvános tartománynév tartománynevének Fully-Qualified tartománynév (FQDN) a méretaránykészlethez.</span><span class="sxs-lookup"><span data-stu-id="4bf54-159">The domain name label for the public Fully-Qualified domain name (FQDN) for this Scale Set.</span></span> <span data-ttu-id="4bf54-160">Ez a tartománynév első olyan összetevője, amely automatikusan hozzá van rendelve a méretskálakészlethez.</span><span class="sxs-lookup"><span data-stu-id="4bf54-160">This is the first component of the domain name that is automatically assigned to the Scale Set.</span></span> <span data-ttu-id="4bf54-161">Az automatikusan hozzárendelt tartománynevek a ( . ) űrlapot <DomainNameLabel> <Location> használják. cloudapp.azure.com)</span><span class="sxs-lookup"><span data-stu-id="4bf54-161">Automatically assigned Domain names use the form (<DomainNameLabel>.<Location>.cloudapp.azure.com).</span></span> <span data-ttu-id="4bf54-162">Ha nem ad meg értéket, az alapértelmezett tartománynévfelirat az és. <ScaleSetName> <ResourceGroupName></span><span class="sxs-lookup"><span data-stu-id="4bf54-162">If no value is supplied, the default domain name label will be the concatenation of <ScaleSetName> and <ResourceGroupName>.</span></span>

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

### <span data-ttu-id="4bf54-163">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="4bf54-163">-EnableUltraSSD</span></span>
<span data-ttu-id="4bf54-164">Az UltraSSD-lemezeket használhatja a virtuális gépekhez a méretaránykészletben.</span><span class="sxs-lookup"><span data-stu-id="4bf54-164">Use UltraSSD disks for the VMs in the scale set.</span></span>

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

### <span data-ttu-id="4bf54-165">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="4bf54-165">-EncryptionAtHost</span></span>
<span data-ttu-id="4bf54-166">Ez a paraméter engedélyezi a titkosítást az összes lemezen, beleértve magában az erőforrás-/ideiglenes lemezen is.</span><span class="sxs-lookup"><span data-stu-id="4bf54-166">This parameter will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> <span data-ttu-id="4bf54-167">Alapértelmezett: A gazdaszámítógép titkosítása le lesz tiltva, hacsak ez a tulajdonság nincs igazra állítva az erőforrásra nézve.</span><span class="sxs-lookup"><span data-stu-id="4bf54-167">Default: The Encryption at host will be disabled unless this property is set to true for the resource.</span></span>

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

### <span data-ttu-id="4bf54-168">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="4bf54-168">-EvictionPolicy</span></span>
<span data-ttu-id="4bf54-169">Az alacsony prioritású virtuális gép méretarányának beállítását kiviction házirend.</span><span class="sxs-lookup"><span data-stu-id="4bf54-169">The eviction policy for the low priority virtual machine scale set.</span></span>  <span data-ttu-id="4bf54-170">Csak a "Deallocate" és a "Delete" érték támogatott.</span><span class="sxs-lookup"><span data-stu-id="4bf54-170">Only supported values are 'Deallocate' and 'Delete'.</span></span>

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

### <span data-ttu-id="4bf54-171">-FrontendPoolName</span><span class="sxs-lookup"><span data-stu-id="4bf54-171">-FrontendPoolName</span></span>
<span data-ttu-id="4bf54-172">Az előlapi címkészlet neve, amely a Scale Set terheléselosztásban használható.</span><span class="sxs-lookup"><span data-stu-id="4bf54-172">The name of the frontend address pool to use in the Scale Set load balancer.</span></span>  <span data-ttu-id="4bf54-173">Ha nem ad meg értéket, létrejön egy új előlapi címkészlet, amely a méretaránykészlet nevével megegyezik.</span><span class="sxs-lookup"><span data-stu-id="4bf54-173">If no value is supplied, a new Frontend Address Pool will be created, with the same name as the scale set.</span></span>

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

### <span data-ttu-id="4bf54-174">-HostGroupId</span><span class="sxs-lookup"><span data-stu-id="4bf54-174">-HostGroupId</span></span>
<span data-ttu-id="4bf54-175">Megadja azt a dedikált állomáscsoportot, ahol a virtuális gép méretaránykészlete található.</span><span class="sxs-lookup"><span data-stu-id="4bf54-175">Specifies the dedicated host group the virtual machine scale set will reside in.</span></span>

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

### <span data-ttu-id="4bf54-176">-ImageName</span><span class="sxs-lookup"><span data-stu-id="4bf54-176">-ImageName</span></span>
<span data-ttu-id="4bf54-177">A virtuális gépek képének neve ebben a méretkészletben.</span><span class="sxs-lookup"><span data-stu-id="4bf54-177">The name of the image for VMs in this Scale Set.</span></span> <span data-ttu-id="4bf54-178">Ha nem ad meg értéket, a rendszer a "Windows Server 2016 DataCenter" képet használja.</span><span class="sxs-lookup"><span data-stu-id="4bf54-178">If no value is provided, the "Windows Server 2016 DataCenter" image will be used.</span></span>

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

### <span data-ttu-id="4bf54-179">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="4bf54-179">-InstanceCount</span></span>
<span data-ttu-id="4bf54-180">A VM-képek száma a méretaránykészletben.</span><span class="sxs-lookup"><span data-stu-id="4bf54-180">The number of VM images in the Scale Set.</span></span>  <span data-ttu-id="4bf54-181">Ha nem ad meg értéket, a program 2 példányt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="4bf54-181">If no value is provided, 2 instances will be created.</span></span>

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

### <span data-ttu-id="4bf54-182">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="4bf54-182">-LoadBalancerName</span></span>
<span data-ttu-id="4bf54-183">Az ezzel a méretkészletgel használható terheléselosztási rendszer neve.</span><span class="sxs-lookup"><span data-stu-id="4bf54-183">The name of the load balancer to use with this Scale Set.</span></span>  <span data-ttu-id="4bf54-184">Ha nincs megadva érték, létrejön egy új terheléselosztási eszköz a méretarányos készlet nevével.</span><span class="sxs-lookup"><span data-stu-id="4bf54-184">A new load balancer using the same name as the Scale Set will be created if no value is specified.</span></span>

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

### <span data-ttu-id="4bf54-185">-Location</span><span class="sxs-lookup"><span data-stu-id="4bf54-185">-Location</span></span>
<span data-ttu-id="4bf54-186">Az Azure-hely, ahol ez a méretaránykészlet létrejön.</span><span class="sxs-lookup"><span data-stu-id="4bf54-186">The Azure location where this Scale Set will be created.</span></span>  <span data-ttu-id="4bf54-187">Ha nincs megadva érték, a hely a paraméterekben hivatkozott egyéb erőforrások helyéről lesz kikövetkeztetve.</span><span class="sxs-lookup"><span data-stu-id="4bf54-187">If no value is specified, the location will be inferred from the location of other resources referenced in the parameters.</span></span>

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

### <span data-ttu-id="4bf54-188">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="4bf54-188">-MaxPrice</span></span>
<span data-ttu-id="4bf54-189">Egy alacsony prioritású virtuálisgép-méretarányú készlet számlázásának maximális ára.</span><span class="sxs-lookup"><span data-stu-id="4bf54-189">The max price of the billing of a low priority virtual machine scale set.</span></span>

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

### <span data-ttu-id="4bf54-190">-NatBackendPort</span><span class="sxs-lookup"><span data-stu-id="4bf54-190">-NatBackendPort</span></span>
<span data-ttu-id="4bf54-191">Backend port inbound network address translation.</span><span class="sxs-lookup"><span data-stu-id="4bf54-191">Backend port for inbound network address translation.</span></span>

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

### <span data-ttu-id="4bf54-192">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="4bf54-192">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="4bf54-193">A hibatartományok száma az egyes elhelyezési csoportoknál.</span><span class="sxs-lookup"><span data-stu-id="4bf54-193">Fault Domain count for each placement group.</span></span>

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

### <span data-ttu-id="4bf54-194">-Priority</span><span class="sxs-lookup"><span data-stu-id="4bf54-194">-Priority</span></span>
<span data-ttu-id="4bf54-195">A virtuális gép prioritása a méretaránykészletben.</span><span class="sxs-lookup"><span data-stu-id="4bf54-195">The priority for the virtual machine in the scale set.</span></span>  <span data-ttu-id="4bf54-196">Csak a "Normál", a "Direkt" és az "Alacsony" támogatott értékek támogatottak.</span><span class="sxs-lookup"><span data-stu-id="4bf54-196">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="4bf54-197">A "Regular" normál virtuális géphez való.</span><span class="sxs-lookup"><span data-stu-id="4bf54-197">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="4bf54-198">A "Spot" a direkt virtuális gépekhez való.</span><span class="sxs-lookup"><span data-stu-id="4bf54-198">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="4bf54-199">A "Low" a direkt virtuális gépre is igaz, de a "Spot" (Direkt) szövegre cseréli.</span><span class="sxs-lookup"><span data-stu-id="4bf54-199">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="4bf54-200">Használja a "Spot" (Direkt) használhatja az "Alacsony" helyett.</span><span class="sxs-lookup"><span data-stu-id="4bf54-200">Please use 'Spot' instead of 'Low'.</span></span>

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

### <span data-ttu-id="4bf54-201">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="4bf54-201">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="4bf54-202">Az ezzel a méretkészlethez használható Közelség elhelyezési csoport erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="4bf54-202">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

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

### <span data-ttu-id="4bf54-203">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="4bf54-203">-PublicIpAddressName</span></span>
<span data-ttu-id="4bf54-204">Az ezzel a méretkészletet használva használt nyilvános IP-cím neve.</span><span class="sxs-lookup"><span data-stu-id="4bf54-204">The name of the public IP Address to use with this scale set.</span></span>  <span data-ttu-id="4bf54-205">Ha nem ad meg értéket, a rendszer létrehoz egy új nyilvános IPAddress címet, a méretaránykészlet nevével.</span><span class="sxs-lookup"><span data-stu-id="4bf54-205">A new Public IPAddress with the same name as the Scale Set will be created if no value is provided.</span></span>

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

### <span data-ttu-id="4bf54-206">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bf54-206">-ResourceGroupName</span></span>
<span data-ttu-id="4bf54-207">A VMSS erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4bf54-207">Specifies the name of the resource group of the VMSS.</span></span>  <span data-ttu-id="4bf54-208">Ha nincs megadva érték, a méretaránykészlet nevével egy új Erőforráscsoport jön létre.</span><span class="sxs-lookup"><span data-stu-id="4bf54-208">If no value is specified, a new ResourceGroup will be created using the same name as the Scale Set.</span></span>

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

### <span data-ttu-id="4bf54-209">-ScaleInPolicy</span><span class="sxs-lookup"><span data-stu-id="4bf54-209">-ScaleInPolicy</span></span>
<span data-ttu-id="4bf54-210">A virtuális gép méretarányának beállításakor be kell tartani a szabályokat.</span><span class="sxs-lookup"><span data-stu-id="4bf54-210">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="4bf54-211">Lehetséges értékek: "Alapértelmezett", "LegrégebbiVM" és "LegújabbVM".</span><span class="sxs-lookup"><span data-stu-id="4bf54-211">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="4bf54-212">Az "Alapértelmezett" érték a virtuális gép méretarány-készletének méretaránya esetén először a zónák között lesz kiegyensúlyozott, ha az egy állatövi méretarányú készlet.</span><span class="sxs-lookup"><span data-stu-id="4bf54-212">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="4bf54-213">Ezt követően lehetőség szerint kiegyensúlyozott lesz a hibatartományok között.</span><span class="sxs-lookup"><span data-stu-id="4bf54-213">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="4bf54-214">Az egyes hibatartományok esetén az eltávolításhoz kiválasztott virtuális gépek lesznek a legújabbak, amelyek nem védettek a méretaránytól.</span><span class="sxs-lookup"><span data-stu-id="4bf54-214">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="4bf54-215">A "OldestVM" (LegrégebbiVM) akkor lesz kiválasztva eltávolításra, ha egy virtuális gép méretaránykészletét méretarányosra méretezi.</span><span class="sxs-lookup"><span data-stu-id="4bf54-215">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="4bf54-216">Az állatövi virtuális gép méretaránykészletek esetében a méretaránykészlet először zónák között lesz kiegyensúlyozott.</span><span class="sxs-lookup"><span data-stu-id="4bf54-216">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="4bf54-217">Az egyes zónákban a nem védett legrégebbi virtuális gépek lesznek kiválasztva eltávolításra.</span><span class="sxs-lookup"><span data-stu-id="4bf54-217">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="4bf54-218">"LegújabbVM", amikor egy virtuális gép méretaránykészletét méretarányosra méretezik, a rendszer eltávolítja a méretaránytól nem védett legújabb virtuális gépeket.</span><span class="sxs-lookup"><span data-stu-id="4bf54-218">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="4bf54-219">Az állatövi virtuális gép méretaránykészletek esetében a méretaránykészlet először zónák között lesz kiegyensúlyozott.</span><span class="sxs-lookup"><span data-stu-id="4bf54-219">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="4bf54-220">Az egyes zónákon belül a legújabb, nem védett virtuális gépek lesznek kiválasztva eltávolításra.</span><span class="sxs-lookup"><span data-stu-id="4bf54-220">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

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

### <span data-ttu-id="4bf54-221">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="4bf54-221">-SecurityGroupName</span></span>
<span data-ttu-id="4bf54-222">Az erre a méretaránykészletre alkalmazandó hálózati biztonsági csoport neve.</span><span class="sxs-lookup"><span data-stu-id="4bf54-222">The name of the network security group to apply to this Scale Set.</span></span>  <span data-ttu-id="4bf54-223">Ha nincs megjelölve érték, a rendszer létrehoz és alkalmaz egy, a méretaránykészletével azonos nevű alapértelmezett hálózatbiztonsági csoportot.</span><span class="sxs-lookup"><span data-stu-id="4bf54-223">If no value is provided, a default network security group with the same name as the Scale Set will be created and applied to the Scale Set.</span></span>

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

### <span data-ttu-id="4bf54-224">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="4bf54-224">-SinglePlacementGroup</span></span>
<span data-ttu-id="4bf54-225">Ezzel a beállítással egyetlen elhelyezési csoportban hozhatja létre a méretarányt, az alapértelmezett beállítás több csoport.</span><span class="sxs-lookup"><span data-stu-id="4bf54-225">Use this to create the Scale set in a single placement group, default is multiple groups</span></span>

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

### <span data-ttu-id="4bf54-226">-SkipExtensionsOnOverprovisionedVMs</span><span class="sxs-lookup"><span data-stu-id="4bf54-226">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="4bf54-227">Azt adja meg, hogy a bővítmények nem futnak túlzsúfolt virtuális gépeken.</span><span class="sxs-lookup"><span data-stu-id="4bf54-227">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

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

### <span data-ttu-id="4bf54-228">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="4bf54-228">-SubnetAddressPrefix</span></span>
<span data-ttu-id="4bf54-229">A ScaleSet alhálózat címelőtagja.</span><span class="sxs-lookup"><span data-stu-id="4bf54-229">The address prefix of the Subnet this ScaleSet will use.</span></span> <span data-ttu-id="4bf54-230">Ha nem ad meg értéket, az alhálózat alapértelmezett beállításai (192.168.1.0/24) lesznek érvényesek.</span><span class="sxs-lookup"><span data-stu-id="4bf54-230">Default Subnet settings (192.168.1.0/24) will be applied if no value is provided.</span></span>

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

### <span data-ttu-id="4bf54-231">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="4bf54-231">-SubnetName</span></span>
<span data-ttu-id="4bf54-232">Az ezzel a méretaránykészlettel használt alhálózat neve.</span><span class="sxs-lookup"><span data-stu-id="4bf54-232">The name of the subnet to use with this Scale Set.</span></span>  <span data-ttu-id="4bf54-233">Ha nem ad meg értéket, létrejön egy új alhálózat a méretaránykészlettel azonos néven.</span><span class="sxs-lookup"><span data-stu-id="4bf54-233">A new Subnet will be created with the same name as the Scale Set if no value is provided.</span></span>

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

### <span data-ttu-id="4bf54-234">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="4bf54-234">-SystemAssignedIdentity</span></span>
<span data-ttu-id="4bf54-235">Ha a paraméter jelen van, akkor a méretaránykészletBEN található VM(k) egy automatikusan létrehozott felügyelt rendszer-identitáshoz vannak hozzárendelve.</span><span class="sxs-lookup"><span data-stu-id="4bf54-235">If the parameter is present then the VM(s) in the scale set is(are) assigned a managed system identity that is auto generated.</span></span>

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

### <span data-ttu-id="4bf54-236">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="4bf54-236">-UpgradePolicyMode</span></span>
<span data-ttu-id="4bf54-237">A vm-példányok frissítési házirendmódja ebben a méretkészletben.</span><span class="sxs-lookup"><span data-stu-id="4bf54-237">The upgrade policy mode for VM instances in this Scale Set.</span></span>  <span data-ttu-id="4bf54-238">A frissítési házirend megadhatja az automatikus, a manuális és a folyamatos frissítéseket.</span><span class="sxs-lookup"><span data-stu-id="4bf54-238">Upgrade policy could specify Automatic, Manual, or Rolling upgrades.</span></span>

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

### <span data-ttu-id="4bf54-239">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="4bf54-239">-UserAssignedIdentity</span></span>
<span data-ttu-id="4bf54-240">Annak a felügyelt szolgáltatás-identitásnak a neve, amely a méretaránykészletben a VM(k)hez van hozzárendelve.</span><span class="sxs-lookup"><span data-stu-id="4bf54-240">The name of a managed service identity that should be assigned to the VM(s) in the scale set.</span></span>

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

### <span data-ttu-id="4bf54-241">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="4bf54-241">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="4bf54-242">Megadja a **VirtualMachineScaleSet** objektumot, amely a parancsmag által létrehozott VMSS-tulajdonságokat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="4bf54-242">Specifies the **VirtualMachineScaleSet** object that contains the properties of the VMSS that this cmdlet creates.</span></span>

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

### <span data-ttu-id="4bf54-243">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="4bf54-243">-VirtualNetworkName</span></span>
<span data-ttu-id="4bf54-244">Az ezzel a méretkészlethez használt virtuális hálózat neve.</span><span class="sxs-lookup"><span data-stu-id="4bf54-244">The name fo the Virtual Network to use with this scale set.</span></span>  <span data-ttu-id="4bf54-245">Ha nem ad meg értéket, létrejön egy új virtuális hálózat a méretaránykészlet nevével.</span><span class="sxs-lookup"><span data-stu-id="4bf54-245">If no value is supplied, a new virtual network with the same name as the Scale Set will be created.</span></span>

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

### <span data-ttu-id="4bf54-246">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="4bf54-246">-VMScaleSetName</span></span>
<span data-ttu-id="4bf54-247">A parancsmag által létrehozott VMSS neve.</span><span class="sxs-lookup"><span data-stu-id="4bf54-247">Specifies the name of the VMSS that this cmdlet creates.</span></span>

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

### <span data-ttu-id="4bf54-248">-VmSize</span><span class="sxs-lookup"><span data-stu-id="4bf54-248">-VmSize</span></span>
<span data-ttu-id="4bf54-249">A virtuális gép példányainak mérete ebben a méretkészletben.</span><span class="sxs-lookup"><span data-stu-id="4bf54-249">The size of the VM instances in this scale set.</span></span>  <span data-ttu-id="4bf54-250">Alapértelmezett méret (Standard_DS1_v2) fog használni, ha nincs megadva méret.</span><span class="sxs-lookup"><span data-stu-id="4bf54-250">A default size (Standard_DS1_v2) will be used if no Size is specified.</span></span>

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

### <span data-ttu-id="4bf54-251">-VnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="4bf54-251">-VnetAddressPrefix</span></span>
<span data-ttu-id="4bf54-252">A méretaránykészlethez használt virtuális hálózat címelőtagja.</span><span class="sxs-lookup"><span data-stu-id="4bf54-252">The address prefix for the virtual network used with this Scale Set.</span></span>  <span data-ttu-id="4bf54-253">Ha nem ad meg értéket, a virtuális hálózat címének előtagbeállítása (192.168.0.0/16) lesz használatos.</span><span class="sxs-lookup"><span data-stu-id="4bf54-253">Default virtual network address prefix settings (192.168.0.0/16) will be used if no value is supplied.</span></span>

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

### <span data-ttu-id="4bf54-254">-Zone</span><span class="sxs-lookup"><span data-stu-id="4bf54-254">-Zone</span></span>
<span data-ttu-id="4bf54-255">A rendelkezésre állási zónák listája, amely az erőforráshoz kiosztott IP-címet sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="4bf54-255">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="4bf54-256">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4bf54-256">-Confirm</span></span>
<span data-ttu-id="4bf54-257">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4bf54-257">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4bf54-258">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bf54-258">-WhatIf</span></span>
<span data-ttu-id="4bf54-259">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4bf54-259">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4bf54-260">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4bf54-260">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4bf54-261">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bf54-261">CommonParameters</span></span>
<span data-ttu-id="4bf54-262">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bf54-262">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bf54-263">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4bf54-263">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bf54-264">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4bf54-264">INPUTS</span></span>

### <span data-ttu-id="4bf54-265">System.String</span><span class="sxs-lookup"><span data-stu-id="4bf54-265">System.String</span></span>

### <span data-ttu-id="4bf54-266">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="4bf54-266">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="4bf54-267">System.Collections.Generic.List'1[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4bf54-267">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="4bf54-268">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4bf54-268">OUTPUTS</span></span>

### <span data-ttu-id="4bf54-269">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="4bf54-269">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="4bf54-270">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4bf54-270">NOTES</span></span>

## <span data-ttu-id="4bf54-271">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4bf54-271">RELATED LINKS</span></span>

[<span data-ttu-id="4bf54-272">Get-AzVms</span><span class="sxs-lookup"><span data-stu-id="4bf54-272">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="4bf54-273">Remove-AzVms</span><span class="sxs-lookup"><span data-stu-id="4bf54-273">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="4bf54-274">Restart-AzVms</span><span class="sxs-lookup"><span data-stu-id="4bf54-274">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="4bf54-275">Set-AzVms</span><span class="sxs-lookup"><span data-stu-id="4bf54-275">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="4bf54-276">Start-AzVms</span><span class="sxs-lookup"><span data-stu-id="4bf54-276">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="4bf54-277">Stop-AzVms</span><span class="sxs-lookup"><span data-stu-id="4bf54-277">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="4bf54-278">Update-AzVms</span><span class="sxs-lookup"><span data-stu-id="4bf54-278">Update-AzVmss</span></span>](./Update-AzVmss.md)


