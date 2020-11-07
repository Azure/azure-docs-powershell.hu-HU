---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 05E6155D-4F0E-406B-9312-77AD97EF66EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVM.md
ms.openlocfilehash: 107441c07e958099d330859a5003a2dafcd64bf9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844473"
---
# <span data-ttu-id="d38c8-101">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="d38c8-101">New-AzVM</span></span>

## <span data-ttu-id="d38c8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d38c8-102">SYNOPSIS</span></span>
<span data-ttu-id="d38c8-103">Virtuális gépet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d38c8-103">Creates a virtual machine.</span></span>

## <span data-ttu-id="d38c8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d38c8-104">SYNTAX</span></span>

### <span data-ttu-id="d38c8-105">SimpleParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d38c8-105">SimpleParameterSet (Default)</span></span>
```
New-AzVM [[-ResourceGroupName] <String>] [[-Location] <String>] -Name <String> -Credential <PSCredential>
 [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] [-ImageName <String>]
 [-Size <String>] [-AvailabilitySetName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d38c8-106">DefaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="d38c8-106">DefaultParameterSet</span></span>
```
New-AzVM [-ResourceGroupName] <String> [-Location] <String> [-VM] <PSVirtualMachine> [[-Zone] <String[]>]
 [-DisableBginfoExtension] [-Tag <Hashtable>] [-LicenseType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d38c8-107">DiskFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="d38c8-107">DiskFileParameterSet</span></span>
```
New-AzVM [[-ResourceGroupName] <String>] [[-Location] <String>] -Name <String>
 [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] -DiskFile <String> [-Linux]
 [-Size <String>] [-AvailabilitySetName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d38c8-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="d38c8-108">DESCRIPTION</span></span>
<span data-ttu-id="d38c8-109">A **New-AzVM** parancsmag létrehoz egy virtuális gépet az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="d38c8-109">The **New-AzVM** cmdlet creates a virtual machine in Azure.</span></span>
<span data-ttu-id="d38c8-110">Ez a parancsmag a virtuális gép objektumát bemenetként veszi át.</span><span class="sxs-lookup"><span data-stu-id="d38c8-110">This cmdlet takes a virtual machine object as input.</span></span>
<span data-ttu-id="d38c8-111">A New-AzVMConfig parancsmag segítségével hozzon létre egy virtuálisgép-objektumot.</span><span class="sxs-lookup"><span data-stu-id="d38c8-111">Use the New-AzVMConfig cmdlet to create a virtual machine object.</span></span>
<span data-ttu-id="d38c8-112">Más parancsmagok segítségével konfigurálhatja a virtuális gépet, például set-AzVMOperatingSystem, set-AzVMSourceImage, add-AzVMNetworkInterface és set-AzVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="d38c8-112">Other cmdlets can be used to configure the virtual machine, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>

<span data-ttu-id="d38c8-113">A `SimpleParameterSet` VM létrehozásának kényelmes módja, ha a virtuális VM-létrehozási argumentumokat nem kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="d38c8-113">The `SimpleParameterSet` provides a convenient method to create a VM by making common VM creation arguments optional.</span></span>

## <span data-ttu-id="d38c8-114">Példák</span><span class="sxs-lookup"><span data-stu-id="d38c8-114">EXAMPLES</span></span>

### <span data-ttu-id="d38c8-115">Példa 1: virtuális gép létrehozása</span><span class="sxs-lookup"><span data-stu-id="d38c8-115">Example 1: Create a virtual machine</span></span>
```
PS C:\> New-AzVM -Name MyVm
```

<span data-ttu-id="d38c8-116">Ebben a példában a parancsfájl bemutatja, hogy miként hozhat létre virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="d38c8-116">This example script shows how to create a virtual machine.</span></span>
<span data-ttu-id="d38c8-117">Ez a parancsfájl számos más parancsmagot használ.</span><span class="sxs-lookup"><span data-stu-id="d38c8-117">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="d38c8-118">2. példa: virtuális gép létrehozása egyéni felhasználói képből</span><span class="sxs-lookup"><span data-stu-id="d38c8-118">Example 2: Create a virtual machine from a custom user image</span></span>
```
PS C:\> ## VM Account
# Credentials for Local Admin account you created in the sysprepped (generalized) vhd image
$VMLocalAdminUser = "LocalAdminUser"
$VMLocalAdminSecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force 
## Azure Account
$LocationName = "westus"
$ResourceGroupName = "MyResourceGroup"
# This a Premium_LRS storage account. 
# It is required in order to run a client VM with efficiency and high performance.
$StorageAccount = "Mydisk"

## VM
$OSDiskName = "MyClient"
$ComputerName = "MyClientVM"
$OSDiskUri = "https://Mydisk.blob.core.windows.net/disks/MyOSDisk.vhd"
$SourceImageUri = "https://Mydisk.blob.core.windows.net/vhds/MyOSImage.vhd"
$VMName = "MyVM"
# Modern hardware environment with fast disk, high IOPs performance. 
# Required to run a client VM with efficiency and performance
$VMSize = "Standard_DS3" 
$OSDiskCaching = "ReadWrite"
$OSCreateOption = "FromImage"

## Networking
$DNSNameLabel = "mydnsname" # mydnsname.westus.cloudapp.azure.com
$NetworkName = "MyNet"
$NICName = "MyNIC"
$PublicIPAddressName = "MyPIP"
$SubnetName = "MySubnet"
$SubnetAddressPrefix = "10.0.0.0/24"
$VnetAddressPrefix = "10.0.0.0/16"

$SingleSubnet = New-AzVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix $SubnetAddressPrefix
$Vnet = New-AzVirtualNetwork -Name $NetworkName -ResourceGroupName $ResourceGroupName -Location $LocationName -AddressPrefix $VnetAddressPrefix -Subnet $SingleSubnet
$PIP = New-AzPublicIpAddress -Name $PublicIPAddressName -DomainNameLabel $DNSNameLabel -ResourceGroupName $ResourceGroupName -Location $LocationName -AllocationMethod Dynamic
$NIC = New-AzNetworkInterface -Name $NICName -ResourceGroupName $ResourceGroupName -Location $LocationName -SubnetId $Vnet.Subnets[0].Id -PublicIpAddressId $PIP.Id

$Credential = New-Object System.Management.Automation.PSCredential ($VMLocalAdminUser, $VMLocalAdminSecurePassword); 

$VirtualMachine = New-AzVMConfig -VMName $VMName -VMSize $VMSize
$VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -ProvisionVMAgent -EnableAutoUpdate
$VirtualMachine = Add-AzVMNetworkInterface -VM $VirtualMachine -Id $NIC.Id
$VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name $OSDiskName -VhdUri $OSDiskUri -SourceImageUri $SourceImageUri -Caching $OSDiskCaching -CreateOption $OSCreateOption -Windows

New-AzVM -ResourceGroupName $ResourceGroupName -Location $LocationName -VM $VirtualMachine -Verbose
```

<span data-ttu-id="d38c8-119">Ez a példa egy meglévő sys-prepped, általános egyéni operációs rendszer lemezképet hoz létre, és egy adatlemezt csatol hozzá, kiépít egy új hálózatot, telepíti a virtuális merevlemezt, és futtatja azt.</span><span class="sxs-lookup"><span data-stu-id="d38c8-119">This example takes an existing sys-prepped, generalized custom operating system image and attaches a data disk to it, provisions a new network, deploys the VHD, and runs it.</span></span>

<span data-ttu-id="d38c8-120">Ez a parancsfájl automatikusan használható a kikészítéshez, mert a helyi virtuális gép rendszergazdai hitelesítő adatait használja a felhasználói interakciót igénylő " **Get-hitelesítőadat** " helyett.</span><span class="sxs-lookup"><span data-stu-id="d38c8-120">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>

<span data-ttu-id="d38c8-121">Ez a parancsfájl feltételezi, hogy már bejelentkezett az Azure-fiókjába.</span><span class="sxs-lookup"><span data-stu-id="d38c8-121">This script assumes that you are already logged into your Azure account.</span></span>
<span data-ttu-id="d38c8-122">Bejelentkezési állapotát a **Get-AzureSubscription** parancsmag használatával ellenőrizheti.</span><span class="sxs-lookup"><span data-stu-id="d38c8-122">You can confirm your login status by using the **Get-AzureSubscription** cmdlet.</span></span>

## <span data-ttu-id="d38c8-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d38c8-123">PARAMETERS</span></span>

### <span data-ttu-id="d38c8-124">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="d38c8-124">-AddressPrefix</span></span>
<span data-ttu-id="d38c8-125">A virtuális hálózathoz tartozó cím előtagja, amelyet a VM rendszerhez hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d38c8-125">The address prefix for the virtual network which will be created for the VM.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases: 

Required: False
Position: Named
Default value: 192.168.0.0/16
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d38c8-126">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="d38c8-126">-AllocationMethod</span></span>
<span data-ttu-id="d38c8-127">A VM rendszerhez létrehozott nyilvános IP-cím IP-kiosztási módja.</span><span class="sxs-lookup"><span data-stu-id="d38c8-127">The IP allocation method for the public IP which will be created for the VM.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases: 
Accepted values: Static, Dynamic

Required: False
Position: Named
Default value: Static
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d38c8-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d38c8-128">-AsJob</span></span>
<span data-ttu-id="d38c8-129">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="d38c8-129">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="d38c8-130">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="d38c8-130">-AvailabilitySetName</span></span>
<span data-ttu-id="d38c8-131">Az elérhetőségi halmaz nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d38c8-131">Specifies a name for the availability set.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d38c8-132">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="d38c8-132">-Credential</span></span>
<span data-ttu-id="d38c8-133">A VM rendszergazdai hitelesítő adatai.</span><span class="sxs-lookup"><span data-stu-id="d38c8-133">The administrator credentials for the VM.</span></span>

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

### <span data-ttu-id="d38c8-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d38c8-134">-DefaultProfile</span></span>
<span data-ttu-id="d38c8-135">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d38c8-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d38c8-136">-DisableBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="d38c8-136">-DisableBginfoExtension</span></span>
<span data-ttu-id="d38c8-137">Jelzi, hogy ez a parancsmag nem telepíti a **BG információs** bővítményt a virtuális gépre.</span><span class="sxs-lookup"><span data-stu-id="d38c8-137">Indicates that this cmdlet does not install the **BG Info** extension on the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DefaultParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d38c8-138">-DiskFile</span><span class="sxs-lookup"><span data-stu-id="d38c8-138">-DiskFile</span></span>
<span data-ttu-id="d38c8-139">A virtuális merevlemez-fájl helyi elérési útja, amelyet fel kell tölteni a felhőbe, és létre kell hoznia a VM-et, és az utótagnak ". vhd"-nek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="d38c8-139">The local path to the virtual hard disk file to be uploaded to the cloud and for creating the VM, and it must have '.vhd' as its suffix.</span></span>

```yaml
Type: String
Parameter Sets: DiskFileParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d38c8-140">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="d38c8-140">-DomainNameLabel</span></span>
<span data-ttu-id="d38c8-141">A VM teljes tartománynevét (FQDN) tartalmazó aldomain címkéje.</span><span class="sxs-lookup"><span data-stu-id="d38c8-141">The subdomain label for the fully-qualified domain name (FQDN) of the VM.</span></span>  <span data-ttu-id="d38c8-142">Ez az űrlapon fog szerepelni `{domainNameLabel}.{location}.cloudapp.azure.com` .</span><span class="sxs-lookup"><span data-stu-id="d38c8-142">This will take the form `{domainNameLabel}.{location}.cloudapp.azure.com`.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d38c8-143">-ImageName</span><span class="sxs-lookup"><span data-stu-id="d38c8-143">-ImageName</span></span>
<span data-ttu-id="d38c8-144">Az a felhasználóbarát kép neve, amelyen a VM épül.</span><span class="sxs-lookup"><span data-stu-id="d38c8-144">The friendly image name upon which the VM will be built.</span></span>  <span data-ttu-id="d38c8-145">Ezek a következők: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, Debian, openSUSE-LEAP, RHEL, SLES.</span><span class="sxs-lookup"><span data-stu-id="d38c8-145">These include: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, Debian, openSUSE-Leap, RHEL, SLES.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: Win2016Datacenter
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d38c8-146">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="d38c8-146">-LicenseType</span></span>
<span data-ttu-id="d38c8-147">A licenc típusát adja meg, amely azt jelzi, hogy a virtuális gép képe vagy lemeze engedélyezett a helyszíni verzióban.</span><span class="sxs-lookup"><span data-stu-id="d38c8-147">Specifies a license type, which indicates that the image or disk for the virtual machine was licensed on-premises.</span></span>
<span data-ttu-id="d38c8-148">Ezt az értéket csak a Windows Server operációs rendszert tartalmazó képek esetén használja a rendszer.</span><span class="sxs-lookup"><span data-stu-id="d38c8-148">This value is used only for images that contain the Windows Server operating system.</span></span>
<span data-ttu-id="d38c8-149">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="d38c8-149">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d38c8-150">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="d38c8-150">Windows_Client</span></span> 
- <span data-ttu-id="d38c8-151">Windows_Server</span><span class="sxs-lookup"><span data-stu-id="d38c8-151">Windows_Server</span></span>

<span data-ttu-id="d38c8-152">Ez az érték nem módosítható.</span><span class="sxs-lookup"><span data-stu-id="d38c8-152">This value cannot be updated.</span></span>
<span data-ttu-id="d38c8-153">Ha ezt a paramétert a frissítéshez adja meg, az értéknek meg kell egyeznie a virtuális gép kezdeti értékével.</span><span class="sxs-lookup"><span data-stu-id="d38c8-153">If you specify this parameter for an update, the value must match the initial value for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d38c8-154">-Linux</span><span class="sxs-lookup"><span data-stu-id="d38c8-154">-Linux</span></span>
<span data-ttu-id="d38c8-155">Azt jelzi, hogy a lemezmeghajtó a Linux VM-re van-e megadva, ha meg van adva; vagy Windows, ha alapértelmezés szerint nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="d38c8-155">Indicates whether the disk file is for Linux VM, if specified; or Windows, if not specified by default.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DiskFileParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d38c8-156">-Hely</span><span class="sxs-lookup"><span data-stu-id="d38c8-156">-Location</span></span>
<span data-ttu-id="d38c8-157">A virtuális gép helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d38c8-157">Specifies a location for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d38c8-158">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d38c8-158">-Name</span></span>
<span data-ttu-id="d38c8-159">A VM-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="d38c8-159">The name of the VM resource.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d38c8-160">-OpenPorts</span><span class="sxs-lookup"><span data-stu-id="d38c8-160">-OpenPorts</span></span>
<span data-ttu-id="d38c8-161">A létrehozott VM-es hálózati biztonsági csoport (NSG) azon portjainak listája, amelyeket meg szeretne nyitni.</span><span class="sxs-lookup"><span data-stu-id="d38c8-161">A list of ports to open on the network security group (NSG) for the created VM.</span></span>  <span data-ttu-id="d38c8-162">Az alapértelmezett érték a választott kép típusától függ (azaz Windows: 3389, 5985 és Linux: 22).</span><span class="sxs-lookup"><span data-stu-id="d38c8-162">The default value depends on the type of image chosen (i.e., Windows: 3389, 5985 and Linux: 22).</span></span>

```yaml
Type: Int32[]
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d38c8-163">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="d38c8-163">-PublicIpAddressName</span></span>
<span data-ttu-id="d38c8-164">A létrehozott VM új (vagy meglévő) nyilvános IP-címének neve.</span><span class="sxs-lookup"><span data-stu-id="d38c8-164">The name of a new (or existing) public IP address for the created VM to use.</span></span>  <span data-ttu-id="d38c8-165">Ha nem adja meg, akkor létrejön egy név.</span><span class="sxs-lookup"><span data-stu-id="d38c8-165">If not specified, a name will be generated.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d38c8-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d38c8-166">-ResourceGroupName</span></span>
<span data-ttu-id="d38c8-167">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d38c8-167">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d38c8-168">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="d38c8-168">-SecurityGroupName</span></span>
<span data-ttu-id="d38c8-169">A létrehozott VM új (vagy meglévő) hálózati biztonsági csoportja (NSG) neve.</span><span class="sxs-lookup"><span data-stu-id="d38c8-169">The name of a new (or existing) network security group (NSG) for the created VM to use.</span></span>  <span data-ttu-id="d38c8-170">Ha nem adja meg, akkor létrejön egy név.</span><span class="sxs-lookup"><span data-stu-id="d38c8-170">If not specified, a name will be generated.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d38c8-171">-Méret</span><span class="sxs-lookup"><span data-stu-id="d38c8-171">-Size</span></span>
<span data-ttu-id="d38c8-172">A virtuális gép mérete.</span><span class="sxs-lookup"><span data-stu-id="d38c8-172">The Virtual Machine Size.</span></span>  <span data-ttu-id="d38c8-173">Az alapértelmezett érték a következő: Standard_DS1_v2.</span><span class="sxs-lookup"><span data-stu-id="d38c8-173">The Default Value is: Standard_DS1_v2.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases: 

Required: False
Position: Named
Default value: Standard_DS1_v2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d38c8-174">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="d38c8-174">-SubnetAddressPrefix</span></span>
<span data-ttu-id="d38c8-175">Annak az alhálózatnak a cím előtagja, amelyet a VM-hez fog létrehozni.</span><span class="sxs-lookup"><span data-stu-id="d38c8-175">The address prefix for the subnet which will be created for the VM.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases: 

Required: False
Position: Named
Default value: 192.168.1.0/24
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d38c8-176">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="d38c8-176">-SubnetName</span></span>
<span data-ttu-id="d38c8-177">A létrehozott VM új (vagy meglévő) alhálózatának neve.</span><span class="sxs-lookup"><span data-stu-id="d38c8-177">The name of a new (or existing) subnet for the created VM to use.</span></span>  <span data-ttu-id="d38c8-178">Ha nem adja meg, akkor létrejön egy név.</span><span class="sxs-lookup"><span data-stu-id="d38c8-178">If not specified, a name will be generated.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d38c8-179">-Címke</span><span class="sxs-lookup"><span data-stu-id="d38c8-179">-Tag</span></span>
<span data-ttu-id="d38c8-180">Itt adhatja meg, hogy az erőforrások és az erőforráscsoportok a name-Value pairek halmazával legyenek címkézve.</span><span class="sxs-lookup"><span data-stu-id="d38c8-180">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="d38c8-181">Ha címkéket ad az erőforrásokhoz, az erőforrásokat csoportosíthatja az erőforráscsoportok között, és saját nézeteket hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="d38c8-181">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="d38c8-182">Minden erőforrás vagy erőforráscsoport legfeljebb 15 címkét tartalmazhat.</span><span class="sxs-lookup"><span data-stu-id="d38c8-182">Each resource or resource group can have a maximum of 15 tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: DefaultParameterSet
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d38c8-183">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="d38c8-183">-VirtualNetworkName</span></span>
<span data-ttu-id="d38c8-184">A létrehozott VM új (vagy meglévő) virtuális hálózatának neve.</span><span class="sxs-lookup"><span data-stu-id="d38c8-184">The name of a new (or existing) virtual network for the created VM to use.</span></span>  <span data-ttu-id="d38c8-185">Ha nem adja meg, akkor létrejön egy név.</span><span class="sxs-lookup"><span data-stu-id="d38c8-185">If not specified, a name will be generated.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d38c8-186">-VM</span><span class="sxs-lookup"><span data-stu-id="d38c8-186">-VM</span></span>
<span data-ttu-id="d38c8-187">A létrehozandó helyi virtuális gépet adja meg.</span><span class="sxs-lookup"><span data-stu-id="d38c8-187">Specifies a local virtual machine to create.</span></span>
<span data-ttu-id="d38c8-188">A virtuálisgép-objektum beolvasásához használja az New-AzVMConfig parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="d38c8-188">To obtain a virtual machine object, use the New-AzVMConfig cmdlet.</span></span>
<span data-ttu-id="d38c8-189">Más parancsmagok segítségével konfigurálhatja a virtuális gépet, például set-AzVMOperatingSystem, set-AzVMSourceImage és add-AzVMNetworkInterface.</span><span class="sxs-lookup"><span data-stu-id="d38c8-189">Other cmdlets can be used to configure the virtual machine, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, and Add-AzVMNetworkInterface.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: DefaultParameterSet
Aliases: VMProfile

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d38c8-190">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="d38c8-190">-Zone</span></span>
<span data-ttu-id="d38c8-191">A virtuális gép zóna listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d38c8-191">Specifies the zone list of the virtual machine.</span></span>

```yaml
Type: String[]
Parameter Sets: DefaultParameterSet
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d38c8-192">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d38c8-192">-Confirm</span></span>
<span data-ttu-id="d38c8-193">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d38c8-193">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d38c8-194">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d38c8-194">-WhatIf</span></span>
<span data-ttu-id="d38c8-195">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d38c8-195">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="d38c8-196">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d38c8-196">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d38c8-197">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d38c8-197">CommonParameters</span></span>
<span data-ttu-id="d38c8-198">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d38c8-198">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d38c8-199">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d38c8-199">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d38c8-200">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d38c8-200">INPUTS</span></span>

### <span data-ttu-id="d38c8-201">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="d38c8-201">PSVirtualMachine</span></span>
<span data-ttu-id="d38c8-202">A ' VM ' paraméter elfogadja a "PSVirtualMachine" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="d38c8-202">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="d38c8-203">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d38c8-203">OUTPUTS</span></span>

### <span data-ttu-id="d38c8-204">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="d38c8-204">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="d38c8-205">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d38c8-205">NOTES</span></span>

## <span data-ttu-id="d38c8-206">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d38c8-206">RELATED LINKS</span></span>

[<span data-ttu-id="d38c8-207">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="d38c8-207">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="d38c8-208">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="d38c8-208">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="d38c8-209">Újraindítás – AzVM</span><span class="sxs-lookup"><span data-stu-id="d38c8-209">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="d38c8-210">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="d38c8-210">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="d38c8-211">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="d38c8-211">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="d38c8-212">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="d38c8-212">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="d38c8-213">Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="d38c8-213">Add-AzVMDataDisk</span></span>](./Add-AzVMDataDisk.md)

[<span data-ttu-id="d38c8-214">Add-AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d38c8-214">Add-AzVMNetworkInterface</span></span>](./Add-AzVMNetworkInterface.md)

[<span data-ttu-id="d38c8-215">Új – AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="d38c8-215">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

[<span data-ttu-id="d38c8-216">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="d38c8-216">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="d38c8-217">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="d38c8-217">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="d38c8-218">Set-AzVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="d38c8-218">Set-AzVMOSDisk</span></span>](./Set-AzVMOSDisk.md)


