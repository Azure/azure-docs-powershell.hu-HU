---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 05E6155D-4F0E-406B-9312-77AD97EF66EE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvm
schema: 2.0.0
ms.openlocfilehash: 86a3c32dd8ee191e5a40d95b2d6cded761944c06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493193"
---
# <span data-ttu-id="6415f-101">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6415f-101">New-AzureRmVM</span></span>

## <span data-ttu-id="6415f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6415f-102">SYNOPSIS</span></span>
<span data-ttu-id="6415f-103">Virtuális gépet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="6415f-103">Creates a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6415f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6415f-104">SYNTAX</span></span>

### <span data-ttu-id="6415f-105">SimpleParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6415f-105">SimpleParameterSet (Default)</span></span>
```
New-AzureRmVM [[-ResourceGroupName] <String>] [[-Location] <String>] -Name <String> -Credential <PSCredential>
 [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] [-ImageName <String>]
 [-Size <String>] [-AvailabilitySetName <String>] [-AsJob] [-DataDiskSizeInGb <Int32[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6415f-106">DefaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="6415f-106">DefaultParameterSet</span></span>
```
New-AzureRmVM [-ResourceGroupName] <String> [-Location] <String> [-VM] <PSVirtualMachine> [[-Zone] <String[]>]
 [-DisableBginfoExtension] [-Tag <Hashtable>] [-LicenseType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6415f-107">DiskFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="6415f-107">DiskFileParameterSet</span></span>
```
New-AzureRmVM [[-ResourceGroupName] <String>] [[-Location] <String>] -Name <String>
 [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] -DiskFile <String> [-Linux]
 [-Size <String>] [-AvailabilitySetName <String>] [-AsJob] [-DataDiskSizeInGb <Int32[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6415f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="6415f-108">DESCRIPTION</span></span>
<span data-ttu-id="6415f-109">A **New-AzureRmVM** parancsmag létrehoz egy virtuális gépet az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="6415f-109">The **New-AzureRmVM** cmdlet creates a virtual machine in Azure.</span></span>
<span data-ttu-id="6415f-110">Ez a parancsmag a virtuális gép objektumát bemenetként veszi át.</span><span class="sxs-lookup"><span data-stu-id="6415f-110">This cmdlet takes a virtual machine object as input.</span></span>
<span data-ttu-id="6415f-111">A New-AzureRmVMConfig parancsmag segítségével hozzon létre egy virtuálisgép-objektumot.</span><span class="sxs-lookup"><span data-stu-id="6415f-111">Use the New-AzureRmVMConfig cmdlet to create a virtual machine object.</span></span>
<span data-ttu-id="6415f-112">Más parancsmagok segítségével konfigurálhatja a virtuális gépet, például set-AzureRmVMOperatingSystem, set-AzureRmVMSourceImage, add-AzureRmVMNetworkInterface és set-AzureRmVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="6415f-112">Other cmdlets can be used to configure the virtual machine, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface, and Set-AzureRmVMOSDisk.</span></span>

<span data-ttu-id="6415f-113">A `SimpleParameterSet` VM létrehozásának kényelmes módja, ha a virtuális VM-létrehozási argumentumokat nem kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="6415f-113">The `SimpleParameterSet` provides a convenient method to create a VM by making common VM creation arguments optional.</span></span>

## <span data-ttu-id="6415f-114">Példák</span><span class="sxs-lookup"><span data-stu-id="6415f-114">EXAMPLES</span></span>

### <span data-ttu-id="6415f-115">Példa 1: virtuális gép létrehozása</span><span class="sxs-lookup"><span data-stu-id="6415f-115">Example 1: Create a virtual machine</span></span>
```
PS C:\> New-AzureRmVM -Name MyVm -Credential (Get-Credential)

VERBOSE: Use 'mstsc /v:myvm-222222.eastus.cloudapp.azure.com' to connect to the VM.

ResourceGroupName        : MyVm
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyVm/provi
ders/Microsoft.Compute/virtualMachines/MyVm
VmId                     : 11111111-1111-1111-1111-111111111111
Name                     : MyVm
Type                     : Microsoft.Compute/virtualMachines
Location                 : eastus
Tags                     : {}
HardwareProfile          : {VmSize}
NetworkProfile           : {NetworkInterfaces}
OSProfile                : {ComputerName, AdminUsername, WindowsConfiguration, Secrets}
ProvisioningState        : Succeeded
StorageProfile           : {ImageReference, OsDisk, DataDisks}
FullyQualifiedDomainName : myvm-222222.eastus.cloudapp.azure.com
```

<span data-ttu-id="6415f-116">Ebben a példában a parancsfájl bemutatja, hogy miként hozhat létre virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="6415f-116">This example script shows how to create a virtual machine.</span></span>
<span data-ttu-id="6415f-117">A parancsfájl a virtuális gép felhasználónevét és jelszavát fogja kérni.</span><span class="sxs-lookup"><span data-stu-id="6415f-117">The script will ask a user name and password for the VM.</span></span>
<span data-ttu-id="6415f-118">Ez a parancsfájl számos más parancsmagot használ.</span><span class="sxs-lookup"><span data-stu-id="6415f-118">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="6415f-119">2. példa: virtuális gép létrehozása egyéni felhasználói képből</span><span class="sxs-lookup"><span data-stu-id="6415f-119">Example 2: Create a virtual machine from a custom user image</span></span>
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

$SingleSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix $SubnetAddressPrefix
$Vnet = New-AzureRmVirtualNetwork -Name $NetworkName -ResourceGroupName $ResourceGroupName -Location $LocationName -AddressPrefix $VnetAddressPrefix -Subnet $SingleSubnet
$PIP = New-AzureRmPublicIpAddress -Name $PublicIPAddressName -DomainNameLabel $DNSNameLabel -ResourceGroupName $ResourceGroupName -Location $LocationName -AllocationMethod Dynamic
$NIC = New-AzureRmNetworkInterface -Name $NICName -ResourceGroupName $ResourceGroupName -Location $LocationName -SubnetId $Vnet.Subnets[0].Id -PublicIpAddressId $PIP.Id

$Credential = New-Object System.Management.Automation.PSCredential ($VMLocalAdminUser, $VMLocalAdminSecurePassword);

$VirtualMachine = New-AzureRmVMConfig -VMName $VMName -VMSize $VMSize
$VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -ProvisionVMAgent -EnableAutoUpdate
$VirtualMachine = Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id $NIC.Id
$VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name $OSDiskName -VhdUri $OSDiskUri -SourceImageUri $SourceImageUri -Caching $OSDiskCaching -CreateOption $OSCreateOption -Windows

New-AzureRmVM -ResourceGroupName $ResourceGroupName -Location $LocationName -VM $VirtualMachine -Verbose
```

<span data-ttu-id="6415f-120">Ez a példa egy meglévő sys-prepped, általános egyéni operációs rendszer lemezképet hoz létre, és egy adatlemezt csatol hozzá, kiépít egy új hálózatot, telepíti a virtuális merevlemezt, és futtatja azt.</span><span class="sxs-lookup"><span data-stu-id="6415f-120">This example takes an existing sys-prepped, generalized custom operating system image and attaches a data disk to it, provisions a new network, deploys the VHD, and runs it.</span></span>

<span data-ttu-id="6415f-121">Ez a parancsfájl automatikusan használható a kikészítéshez, mert a helyi virtuális gép rendszergazdai hitelesítő adatait használja a felhasználói interakciót igénylő " **Get-hitelesítőadat** " helyett.</span><span class="sxs-lookup"><span data-stu-id="6415f-121">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>

<span data-ttu-id="6415f-122">Ez a parancsfájl feltételezi, hogy már bejelentkezett az Azure-fiókjába.</span><span class="sxs-lookup"><span data-stu-id="6415f-122">This script assumes that you are already logged into your Azure account.</span></span>
<span data-ttu-id="6415f-123">Bejelentkezési állapotát a **Get-AzureSubscription** parancsmag használatával ellenőrizheti.</span><span class="sxs-lookup"><span data-stu-id="6415f-123">You can confirm your login status by using the **Get-AzureSubscription** cmdlet.</span></span>

## <span data-ttu-id="6415f-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6415f-124">PARAMETERS</span></span>

### <span data-ttu-id="6415f-125">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="6415f-125">-AddressPrefix</span></span>
<span data-ttu-id="6415f-126">A virtuális hálózathoz tartozó cím előtagja, amelyet a VM rendszerhez hoz létre.</span><span class="sxs-lookup"><span data-stu-id="6415f-126">The address prefix for the virtual network which will be created for the VM.</span></span>

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

### <span data-ttu-id="6415f-127">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="6415f-127">-AllocationMethod</span></span>
<span data-ttu-id="6415f-128">A VM rendszerhez létrehozott nyilvános IP-cím IP-kiosztási módja.</span><span class="sxs-lookup"><span data-stu-id="6415f-128">The IP allocation method for the public IP which will be created for the VM.</span></span>

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

### <span data-ttu-id="6415f-129">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6415f-129">-AsJob</span></span>
<span data-ttu-id="6415f-130">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="6415f-130">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="6415f-131">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="6415f-131">-AvailabilitySetName</span></span>
<span data-ttu-id="6415f-132">Az elérhetőségi halmaz nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6415f-132">Specifies a name for the availability set.</span></span>

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

### <span data-ttu-id="6415f-133">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="6415f-133">-Credential</span></span>
<span data-ttu-id="6415f-134">A VM rendszergazdai hitelesítő adatai.</span><span class="sxs-lookup"><span data-stu-id="6415f-134">The administrator credentials for the VM.</span></span>

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

### <span data-ttu-id="6415f-135">-DataDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="6415f-135">-DataDiskSizeInGb</span></span>
<span data-ttu-id="6415f-136">Az adatlemezek méretét adja meg GB-ban.</span><span class="sxs-lookup"><span data-stu-id="6415f-136">Specifies the sizes of data disks in GB.</span></span>

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

### <span data-ttu-id="6415f-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6415f-137">-DefaultProfile</span></span>
<span data-ttu-id="6415f-138">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6415f-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6415f-139">-DisableBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="6415f-139">-DisableBginfoExtension</span></span>
<span data-ttu-id="6415f-140">Jelzi, hogy ez a parancsmag nem telepíti a **BG információs** bővítményt a virtuális gépre.</span><span class="sxs-lookup"><span data-stu-id="6415f-140">Indicates that this cmdlet does not install the **BG Info** extension on the virtual machine.</span></span>

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

### <span data-ttu-id="6415f-141">-DiskFile</span><span class="sxs-lookup"><span data-stu-id="6415f-141">-DiskFile</span></span>
<span data-ttu-id="6415f-142">A virtuális merevlemez-fájl helyi elérési útja, amelyet fel kell tölteni a felhőbe, és létre kell hoznia a VM-et, és az utótagnak ". vhd"-nek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="6415f-142">The local path to the virtual hard disk file to be uploaded to the cloud and for creating the VM, and it must have '.vhd' as its suffix.</span></span>

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

### <span data-ttu-id="6415f-143">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="6415f-143">-DomainNameLabel</span></span>
<span data-ttu-id="6415f-144">A VM teljes tartománynevét (FQDN) tartalmazó aldomain címkéje.</span><span class="sxs-lookup"><span data-stu-id="6415f-144">The subdomain label for the fully-qualified domain name (FQDN) of the VM.</span></span>  <span data-ttu-id="6415f-145">Ez az űrlapon fog szerepelni `{domainNameLabel}.{location}.cloudapp.azure.com` .</span><span class="sxs-lookup"><span data-stu-id="6415f-145">This will take the form `{domainNameLabel}.{location}.cloudapp.azure.com`.</span></span>

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

### <span data-ttu-id="6415f-146">-ImageName</span><span class="sxs-lookup"><span data-stu-id="6415f-146">-ImageName</span></span>
<span data-ttu-id="6415f-147">Az a felhasználóbarát kép neve, amelyen a VM épül.</span><span class="sxs-lookup"><span data-stu-id="6415f-147">The friendly image name upon which the VM will be built.</span></span>  <span data-ttu-id="6415f-148">Ezek a következők: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, Debian, openSUSE-LEAP, RHEL, SLES.</span><span class="sxs-lookup"><span data-stu-id="6415f-148">These include: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, Debian, openSUSE-Leap, RHEL, SLES.</span></span>

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

### <span data-ttu-id="6415f-149">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="6415f-149">-LicenseType</span></span>
<span data-ttu-id="6415f-150">A licenc típusát adja meg, amely azt jelzi, hogy a virtuális gép képe vagy lemeze engedélyezett a helyszíni verzióban.</span><span class="sxs-lookup"><span data-stu-id="6415f-150">Specifies a license type, which indicates that the image or disk for the virtual machine was licensed on-premises.</span></span>
<span data-ttu-id="6415f-151">Ezt az értéket csak a Windows Server operációs rendszert tartalmazó képek esetén használja a rendszer.</span><span class="sxs-lookup"><span data-stu-id="6415f-151">This value is used only for images that contain the Windows Server operating system.</span></span>
<span data-ttu-id="6415f-152">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="6415f-152">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6415f-153">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="6415f-153">Windows_Client</span></span>
- <span data-ttu-id="6415f-154">Windows_Server</span><span class="sxs-lookup"><span data-stu-id="6415f-154">Windows_Server</span></span>

<span data-ttu-id="6415f-155">Ez az érték nem módosítható.</span><span class="sxs-lookup"><span data-stu-id="6415f-155">This value cannot be updated.</span></span>
<span data-ttu-id="6415f-156">Ha ezt a paramétert a frissítéshez adja meg, az értéknek meg kell egyeznie a virtuális gép kezdeti értékével.</span><span class="sxs-lookup"><span data-stu-id="6415f-156">If you specify this parameter for an update, the value must match the initial value for the virtual machine.</span></span>

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

### <span data-ttu-id="6415f-157">-Linux</span><span class="sxs-lookup"><span data-stu-id="6415f-157">-Linux</span></span>
<span data-ttu-id="6415f-158">Azt jelzi, hogy a lemezmeghajtó a Linux VM-re van-e megadva, ha meg van adva; vagy Windows, ha alapértelmezés szerint nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="6415f-158">Indicates whether the disk file is for Linux VM, if specified; or Windows, if not specified by default.</span></span>

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

### <span data-ttu-id="6415f-159">-Hely</span><span class="sxs-lookup"><span data-stu-id="6415f-159">-Location</span></span>
<span data-ttu-id="6415f-160">A virtuális gép helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6415f-160">Specifies a location for the virtual machine.</span></span>

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

### <span data-ttu-id="6415f-161">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6415f-161">-Name</span></span>
<span data-ttu-id="6415f-162">A VM-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="6415f-162">The name of the VM resource.</span></span>

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

### <span data-ttu-id="6415f-163">-OpenPorts</span><span class="sxs-lookup"><span data-stu-id="6415f-163">-OpenPorts</span></span>
<span data-ttu-id="6415f-164">A létrehozott VM-es hálózati biztonsági csoport (NSG) azon portjainak listája, amelyeket meg szeretne nyitni.</span><span class="sxs-lookup"><span data-stu-id="6415f-164">A list of ports to open on the network security group (NSG) for the created VM.</span></span>  <span data-ttu-id="6415f-165">Az alapértelmezett érték a választott kép típusától függ (azaz Windows: 3389, 5985 és Linux: 22).</span><span class="sxs-lookup"><span data-stu-id="6415f-165">The default value depends on the type of image chosen (i.e., Windows: 3389, 5985 and Linux: 22).</span></span>

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

### <span data-ttu-id="6415f-166">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="6415f-166">-PublicIpAddressName</span></span>
<span data-ttu-id="6415f-167">A létrehozott VM új (vagy meglévő) nyilvános IP-címének neve.</span><span class="sxs-lookup"><span data-stu-id="6415f-167">The name of a new (or existing) public IP address for the created VM to use.</span></span>  <span data-ttu-id="6415f-168">Ha nem adja meg, akkor létrejön egy név.</span><span class="sxs-lookup"><span data-stu-id="6415f-168">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="6415f-169">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6415f-169">-ResourceGroupName</span></span>
<span data-ttu-id="6415f-170">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6415f-170">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="6415f-171">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="6415f-171">-SecurityGroupName</span></span>
<span data-ttu-id="6415f-172">A létrehozott VM új (vagy meglévő) hálózati biztonsági csoportja (NSG) neve.</span><span class="sxs-lookup"><span data-stu-id="6415f-172">The name of a new (or existing) network security group (NSG) for the created VM to use.</span></span>  <span data-ttu-id="6415f-173">Ha nem adja meg, akkor létrejön egy név.</span><span class="sxs-lookup"><span data-stu-id="6415f-173">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="6415f-174">-Méret</span><span class="sxs-lookup"><span data-stu-id="6415f-174">-Size</span></span>
<span data-ttu-id="6415f-175">A virtuális gép mérete.</span><span class="sxs-lookup"><span data-stu-id="6415f-175">The Virtual Machine Size.</span></span>  <span data-ttu-id="6415f-176">Az alapértelmezett érték a következő: Standard_DS1_v2.</span><span class="sxs-lookup"><span data-stu-id="6415f-176">The Default Value is: Standard_DS1_v2.</span></span>

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

### <span data-ttu-id="6415f-177">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="6415f-177">-SubnetAddressPrefix</span></span>
<span data-ttu-id="6415f-178">Annak az alhálózatnak a cím előtagja, amelyet a VM-hez fog létrehozni.</span><span class="sxs-lookup"><span data-stu-id="6415f-178">The address prefix for the subnet which will be created for the VM.</span></span>

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

### <span data-ttu-id="6415f-179">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="6415f-179">-SubnetName</span></span>
<span data-ttu-id="6415f-180">A létrehozott VM új (vagy meglévő) alhálózatának neve.</span><span class="sxs-lookup"><span data-stu-id="6415f-180">The name of a new (or existing) subnet for the created VM to use.</span></span>  <span data-ttu-id="6415f-181">Ha nem adja meg, akkor létrejön egy név.</span><span class="sxs-lookup"><span data-stu-id="6415f-181">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="6415f-182">-Címke</span><span class="sxs-lookup"><span data-stu-id="6415f-182">-Tag</span></span>
<span data-ttu-id="6415f-183">Itt adhatja meg, hogy az erőforrások és az erőforráscsoportok a name-Value pairek halmazával legyenek címkézve.</span><span class="sxs-lookup"><span data-stu-id="6415f-183">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="6415f-184">Ha címkéket ad az erőforrásokhoz, az erőforrásokat csoportosíthatja az erőforráscsoportok között, és saját nézeteket hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="6415f-184">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="6415f-185">Minden erőforrás vagy erőforráscsoport legfeljebb 15 címkét tartalmazhat.</span><span class="sxs-lookup"><span data-stu-id="6415f-185">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="6415f-186">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="6415f-186">-VirtualNetworkName</span></span>
<span data-ttu-id="6415f-187">A létrehozott VM új (vagy meglévő) virtuális hálózatának neve.</span><span class="sxs-lookup"><span data-stu-id="6415f-187">The name of a new (or existing) virtual network for the created VM to use.</span></span>  <span data-ttu-id="6415f-188">Ha nem adja meg, akkor létrejön egy név.</span><span class="sxs-lookup"><span data-stu-id="6415f-188">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="6415f-189">-VM</span><span class="sxs-lookup"><span data-stu-id="6415f-189">-VM</span></span>
<span data-ttu-id="6415f-190">A létrehozandó helyi virtuális gépet adja meg.</span><span class="sxs-lookup"><span data-stu-id="6415f-190">Specifies a local virtual machine to create.</span></span>
<span data-ttu-id="6415f-191">A virtuálisgép-objektum beolvasásához használja az New-AzureRmVMConfig parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="6415f-191">To obtain a virtual machine object, use the New-AzureRmVMConfig cmdlet.</span></span>
<span data-ttu-id="6415f-192">Más parancsmagok segítségével konfigurálhatja a virtuális gépet, például set-AzureRmVMOperatingSystem, set-AzureRmVMSourceImage és add-AzureRmVMNetworkInterface.</span><span class="sxs-lookup"><span data-stu-id="6415f-192">Other cmdlets can be used to configure the virtual machine, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, and Add-AzureRmVMNetworkInterface.</span></span>

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

### <span data-ttu-id="6415f-193">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="6415f-193">-Zone</span></span>
<span data-ttu-id="6415f-194">A virtuális gép zóna listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6415f-194">Specifies the zone list of the virtual machine.</span></span>

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

### <span data-ttu-id="6415f-195">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6415f-195">-Confirm</span></span>
<span data-ttu-id="6415f-196">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6415f-196">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6415f-197">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6415f-197">-WhatIf</span></span>
<span data-ttu-id="6415f-198">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6415f-198">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="6415f-199">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6415f-199">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6415f-200">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6415f-200">CommonParameters</span></span>
<span data-ttu-id="6415f-201">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6415f-201">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6415f-202">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6415f-202">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6415f-203">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6415f-203">INPUTS</span></span>

### <span data-ttu-id="6415f-204">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="6415f-204">PSVirtualMachine</span></span>
<span data-ttu-id="6415f-205">A ' VM ' paraméter elfogadja a "PSVirtualMachine" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="6415f-205">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="6415f-206">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6415f-206">OUTPUTS</span></span>

### <span data-ttu-id="6415f-207">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="6415f-207">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="6415f-208">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6415f-208">NOTES</span></span>

## <span data-ttu-id="6415f-209">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6415f-209">RELATED LINKS</span></span>

[<span data-ttu-id="6415f-210">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6415f-210">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="6415f-211">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6415f-211">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="6415f-212">Újraindítás – AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6415f-212">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="6415f-213">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6415f-213">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="6415f-214">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6415f-214">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="6415f-215">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6415f-215">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)

[<span data-ttu-id="6415f-216">Add-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="6415f-216">Add-AzureRmVMDataDisk</span></span>](./Add-AzureRmVMDataDisk.md)

[<span data-ttu-id="6415f-217">Add-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="6415f-217">Add-AzureRmVMNetworkInterface</span></span>](./Add-AzureRmVMNetworkInterface.md)

[<span data-ttu-id="6415f-218">Új – AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="6415f-218">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)

[<span data-ttu-id="6415f-219">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="6415f-219">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)

[<span data-ttu-id="6415f-220">Set-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="6415f-220">Set-AzureRmVMSourceImage</span></span>](./Set-AzureRmVMSourceImage.md)

[<span data-ttu-id="6415f-221">Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="6415f-221">Set-AzureRmVMOSDisk</span></span>](./Set-AzureRmVMOSDisk.md)


